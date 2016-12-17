---
layout: post
title: A Sky Full of Bases... And Hands Full of TODOs!
---

Right, it's about time to ping the blog again...

Late November and early December's been quite fulfilling, and there couldn't
be anything better than celebrating the community's 5th anniversay - can't
belive it's been half a decade - and I almost forgot to write the news
article (just before I climbed up the bed... the next minute I began creeping
on my keyboard, and begging Chai for an anniversary banner - which he made
in his favourite game of Minecraft). Even better than that, AOSC OS's ARM
port finally saw its first mass debut in the format of SD card images -
Icenowy... She's a genius with all the mass building and mainline kernel
adaptations - couldn't have managed it without her.

But anyways. *Bases* (or `*-base`) is a new concept that I started to think
about when building the last batch of AOSC OS AMD64 releases in September.
When I started building a non-split (packages) system as the new AOSC OS, I
did not anticipate how complex the dependency trees would have become. It's
practically impossible to build a system in one go without leaving some
packages out - and time to rebuild the tarball again... another 30 minutes
down the drain. Additionally, with the insane growth in amount of ports - now
six, will be seven in just a month or so (MIPS64el) - it became increasingly
difficult to keep track of things/features that needed to be introduced
in order to create a production level system base (in the case of the two
big endian PowerPC ports, I did not realize there are important utilities
like `ifconfig` were left out until I tried to build a `base` tarball,
and I suddenly realized how young - simple, and naive - the port was). Before
I got carried out by these fond memories, `*-base` packages are essentially
meta packages for multiple desktop environments - but additionally, packages
describing functionalities in an AOSC OS distribution were also created:

- `network-base`, network connection/diagnostic/security functionalities.
- `studio-base`, audio/video studio/production functionalities.

Unlike the common...

- `gnome-base`, a basic GNOME desktop installation.
- `kde-base`, a basic KDE Plasma desktop installation.

When a new user comes to a new Linux distribution - or even to Linux - they
usually wouldn't know what to install to get certain things ready, or in
better wording - "... so that I can $DO_FOO". A classic example would be
productivity functionality - in which case, LibreOffice as the gold standard of
productivity suite on Linux (nix in general if you would admit) forms the
center piece of this functionality, but usually one may want to be able to
scan and print documents, and moreover, print and scan with appropriate
capabilities like the driver themselves (Hewlett Packard and Canon alike) and
enhanced functions like OCR (tesseract will do, but with language data
included) - so our `productivity-base` has the following dependencies, well,
roughly (because I already forgot):

- `productivity-base`, productivity functionalities.
  - `libreofice` - LibreOffice productivity suite.
  - ...
  - `print-base` - printing/spooling functionalities.
    - `cups` - Common UNIX Printing System.
    - `hplip` - Open source collection of Hewlett Packard
                printer/scanner drivers.
    - ...
  - `scan-base` - scanning functionalities.
    - `simple-scan` - A GTK+ sanning utility (the only good choice so far).
    - ...
    - `tesseract` - Tesseract OCR.

*(Also note that `productivity-base` could depend on other `*-base` packages)*

So, now if you install `productivity-base`, you can drop right in and start
writing documents, scanning faxes, ... You get the idea - I might sound old
fashioned, but Google Drive simply wouldn't cut sometimes...

Anyways, this is the basic principle of the `*-base` packages, or simply
*Bases*: meta/collection packages providing certain capabilities and
functionalities to AOSC OS, and moreover, to provide just enough of the
functionalities for out-of-box experience (like, your printer will work
after you installed `print-base`).

*So why "Bases" the name?*

Honestly, just to be regarded as a "catch-phrase" when someone would want to
get such "special" packages out of the 4000+ in the repository.

There are problems however. Lion Yang complained that in the case of
`golang-base`, most people would just go ahead and install `go`, as it is
just a shorter package name, and the existence is just not "prominent" enough
in the context of APT (our standard package manager frontend).

And unfortunately I could not think of a straightforward way to solve this
issue - and `*-base` packages will serve better in distribution-building
(say, when I build a KDE tarball, I would know which ones to install to create
a system release with the least top-level dependencies... complex concept,
if you don't quite get what I'm saying here, IRC me - JeffBai) and porting
(as mentioned above, so the developer would know what still needed to be
built for a bare-minimum collection of packages for a port to be functional,
or "behave like AOSC OS") context.

Maybe patching APT will do a better job... I don't know, not exactly available
for those kind of tasks yet.

Speaking of things to-do in the coming moons, I am trying to set up some
semi-breaks for myself - some week-long, or even two-week-long periods each
season to free myself from day-to-day packaging - and build system release
updates during those periods, usually taking 5 days or so, and the rest at my
own disposal. Taking breaks is only for better working efficiency and mood
in general... Not gonna lie. Before then, I would need to make a more concrete
schedule for these semi-breaks.

-------------------------------

*... And I've finally got myself an Alienware Alpha R2 so that I could play
Elite: Dangerous at near 60fps. Quite happy about the little machine so far,
might post a brief review later.*
