---
layout: post
title: The Silent Box: Episode 1, The Machine
---

So I figured that it's about time for another blog post. Well, this time will be
a series in fact - a series of recordings of playings with my IBM ThinkPad 340,
the oldest ThinkPad in my possession. Breaking down the coming episodes of this
blogging series...

- Episode 1, The Machine,
  a general overview of the machine and some of its stories.
- Episode 2, The Silent Box,
  CF Card HDD upgrade, Windows 95 installation and configuration.
- Episode 3, Optical Treatment,
  addition of a Hewlett-Packard external CD-ROM drive.
- Episode 4, The Silent Box Sings,
  Roland SC-88vl.
- Episode 5, ???.
- ...

In other words, this will be a series of indefinite length, focusing around this
particular machine. Anyways, let's go ahead with Episode 1... But first, some
background and "history talk".

--------------------------------------------------------------------------------

So, ThinkPads... A series of personal or professional portable computers
(laptops, tablets, and the so-called convertibles) introduced by the
International Business Machines Corporations, and later acquired by Lenovo; a
series of computers that does not ask you, not even politely, to move your hands
away from the keyboard; a series of computers that constitutes the most part of
my experience with personal computers; a series of computers that still have not
fail to be my favourite of all, after 14 years and 5 of them (and many more in
collection).

ThinkPad were known to be one of the most expensive laptop computers on the
market by the early 90s, some exceeded by GRID and other illusive, or shall we
say, less popular-oriented computer manufacturers. So heck, they might not be
the "high-end" in terms of "Premium-ness", who cares? They were built to be the
longest lasting laptop money could buy... Easy to clean, easy to repair, easy to
upgrade - in the most case, they still are, although minus all the bold design
decision IBM seemed to be pushing out every other year (remember the 701C, still
looking for one).

In the pre-XATR days[1], ThinkPads were initially carved into three separate
lines:

- The 300 series, budget computers, some manufactured by third-party companies,
like the 300/300C manufactured by Zenith Data Systems. These computers used to
get the lowest emphasis on performance, build quality, and expandability
departments (say, my 340 which has a souped-up Intel 386SX processor and no
rubber-coated case). Later models like the 380s, 385s, and 390s are more
family and entertainment oriented, and provides full integration of drives
(making a tri-spindle[2] configuration) - much like the A series of ThinkPads.
- The 500 series, ultraportables with premium designs. These are probably the
most premium examples of ThinkPads, they are usually found to be the lightest,
yet they come with beautiful designs (oh, people have got to take a look back
at the 560...). This line of computer was later replaced by the X series.
- The 700 series, these are the holy-grails of ThinkPads, from the first 700
tablet, to the 701C "Butterfly", and to the second earliest laptop to integrate
a DVD disc drive, the 770... The 700 series of ThinkPads contains the latest
innovations from IBM and from the world of computer technologies. I wasn't even
born in the mid-90s, but reading the documents about the 770s with the
SelectaDock with 3 full-size PCI slots and a high-frequency Pentium II just
made me wonder how people could afford such a lavish package of technologies...

And of course, in demand of variety, IBM introduced some more lines to the
ThinkPad family:

- The 200 series, even smaller ThinkPads, mostly aimed for Asian markets. The
235 and 240 are just brilliant little machines with little compromise in the
performance department, magic tricks in a tin-box.
- The 600 series, the legendary predecessor to the now legendary T series of
ThinkPads, perfect balance (in fact, it stands up on its base) of performance
and weight.
- The 800 series, yet another holy-grail family of ThinkPads with PowerPC 603
or 604 processors (tasty...) running IBM AIX, Linux, or Windows NT (and all the
other high-end stuff). Prices were over 10,000 U.S. Dollars, yikes!
- The "i" series, or "iSeries", manufactured by Acer... Let's just look on the
bright side, this series contains re-worked and price-reduced versions of
ThinkPads from the 200/300 lines and the 570. Most notably the iSeries 1400 was
the first ThinkPad to come with built-in wireless network support, and the
legendary ThinkLight (I miss it, I really do).

And all that comes later is not exacty in my interest of collection or
playing-around... Right then, to the machine.

--------------------------------------------------------------------------------

As mentioned in the rumbling above, my IBM ThinkPad 340 is one of the low-end
models introduced, for being a machine from the 300 line of ThinkPads. The
ThinkPad 340 was a special one (for it having no trace on the IBM or Lenovo
support sites but on PCCBBS... nah, but seriously...), this is probably the most
limited model of ThinkPad of the almost-Windows 95 era (introduced in late
1994).

The 340's stock configuration was nothing eye-catching, even by 1994 standard:

- IBM 486SLC 25/50MHz.
- 4/8/12MB IC DRAM, non-parity.
- 125MB HDD, AT/ISA IDE interface.
- 9.5 inch monochrome DSTN display (64-level grayscale, 16 emulated colour).
- 1 Type 2/3 PCMCIA slot.
- VGA, DB-9 serial, DB-25 parallel, PS/2.
- 1.44MB/720K floppy drive.
- Optional 28.8/14.4K data/fax modem.

If we take a look at a high-end 755CD, available for roughly the same period...

- Intel Pentium 75/50MHz.
- 8/12/16/24/32/36/40MB IC DRAM, or DIMM adapter.
- 540/810MB, or 1.2GB HDD, AT/ISA IDE interface.
- 10.4 inch 64K-colour TFT display.
- 1 Type 3, or 2 Type 2 PCMCIA slots.
- VGA, DB-9 serial, DB-25 parallel, PS/2.
- 2.88MB/1.44MB/720K floppy drive.
- CD-ROM drive.
- Audio and Video capture/recording.
- IBM Mwave DSP sound card.
- Optional dock with 1/2 ISA slots, SCSI port, extra ports.

There simply isn't any comparison there. Let me just make it clear, the 340 is a
recreation of a high-end laptop from 1992/1993 - while 755CD is a next-gen
Pentium capable of running Windows 95 and Windows NT smoothly, all those
beautiful things.

But it's not to say the 340 is just a cheap sale IBM made (well to be fair it
does feel a lot cheaper than the 755CD that I have), the 340 is a beautiful,
simplistic, cool[3] machine. The machine was never regarded as future-proof by
IBM, as the only documentation available for the 340 on the installation and
configuration of Windows 95 could only be found on MIT's
[mailing list](https://groups.csail.mit.edu/mac/ftpdir/thinkpad/old-archive/HTML/tp-1995/msg01655.html) - as a Windows 95 Beta installation guide for various ThinkPad models. Being
a model based on the older, non PnP-BIOS platform, the system was described to
have issues with PCMCIA cards...


    IBM is testing the following ThinkPad systems with Windows 95
    but only APM BIOS 1.0 is supported.  No PnP BIOS support is
    available on those systems.

        - ThinkPad 750 Family
        - ThinkPad 340 (Monochrome display system)
        - ThinkPad 230Cs

This was the Beta period, but after all, no support for Windows 95 was provided
for this machine. It's colour-screened sibling, the 340CSE did get a BIOS update
and driver updates from IBM. The 340 was effectively limited to DOS, Windows
3.x, and OS/2 Warp 3.0 according to IBM[4].

To understand the decision made by IBM, we have to look back on the hardware
of the 340. The main pain-in-the-arse when attempting to use newer operating
systems (by Microsoft) is the processor itself. The 340 comes with a 486SLC
designed and manufactured by IBM themselves, as a cheaper alternative to
upgrade 386-based PS/2 machines. The 486SLC, 486SLC2, and 486SLC3 are basically
cache-doubled, and frequency-multiplied versions of the Intel 386SL 20MHz chip.
They used 486-derived 32-bit instructions, but still was set on the 386SL pins
(or pin-compatible, so to speak), and uses a 16-bit data path. And like the 386
processors, they are limited to 16MB of RAM[5]. here below is one piece of
information provided by IBM in the "486 Processors - Questions and Answers"
article[6]:

    The IBM 486SLC2 uses the same instruction set as the 486SX, and adds
    instructions for power-saving operation (like the 486SL, which came
    out after the 486SLC2). Also it has a 16K internal cache (versus 8K
    for the 486SL/SX/DX2) for improved performance, and like the 486DX2
    comes in clock-doubling versions. Like the 486SL/SX, and unlike the
    486DX2, the 486SLC2 does not include a floating-point (math co-
    processor) unit, which adversely affects performance, compared to
    the 486DX2, when floating point math is used. Also, the 486SLC2 has
    a 16-bit external bus (to allow systems vendors to save money on
    motherboard design), which reduces performance slightly (about 10%
    versus a 32-bit bus); it also limits the system to no more than 16MB
    of RAM.

Sounds quite well, but if I was to see this back in 1994, I would have avoided
this processor like a plague. If we look at another exerpt from the "Microsoft
Windows 95 Resource Kit" reference guide, page 556:

    DX versus SX processors. Although the minimum requirement to run
    Windows 95 is a 386SX-based processor, the SX processor is not a
    full 32-bit CPU. The SX-based processor accesses memory using 32-bit
    addressing, but it accesses data in 16-bit increments. Although
    Windows 95 will run on an SX-based processor, you will most likely
    not be satisfied with the perceived performance when compared to a
    16-bit operating system such as Windows 3.1

*But Windows 3.1 sucks though, Microsoft...*

I have used Windows 95 on a IBM PS/2 L40sx before, which comes with 4MB of RAM
and a 386SX 20MHz processor. Taking it from the description by IBM comparing a
486SLC2 to some other processors:

    The IBM 486SLC2 processor runs internally at twice the speed of the
    rest of the system, such as 40/20MHz, producing performance faster
    than a 25MHz 486DX, but less than a 50MHz 486DX. The performance of
    IBM's 40/20MHz 486SLC2 is up to 271% better than a 20MHz Intel 386SX,
    up to 99% faster than IBM's 20MHz 386SLC, up to 53% faster than a
    20MHz Intel 486SX, and up to 20% faster than Intel's 25MHz 486SX
    processor. IBM's 50/25MHz 486SLC2 is somewhat faster than Intel's
    486DX-33, but not as fast as the Intel 486DX2-50, due to the lack of
    a built-in floating point unit and the use of a 16-bit bus.

And Windows 95 worked fine without network support enabled on the L40sx... So if
IBM says ~271% faster than a 20MHz 386SX (and mine is a 50/25MHz SLC2...), and
based on my experience with Windows 95 so far on the pathetic 125MB HDD - let
me just say... Don't loose hope, it's not that bad - a CF card upgrade should
improve the situation, more or less.

--------------------------------------------------------------------------------

Let's take a look at the outside of the machine. The 340, as I said many times
in this post, is a very simple subnotebook.

[![tp340-overview](http://i.imgur.com/CjfsuV5.jpg)](http://i.imgur.com/dV7WHCD.jpg)

This is the kind of early ThinkPad models that screams "Bento!" however you look
at it. The 9.5 inch display is enclosed in a 12-inch "form factor" (taken from
the size of my X240/250 hybrid), with most of the ports located at the back of
the machine. The machine looks very clean from the front. With just a floppy
disk drive... All that you needed by the time.

[![tp340-front](http://i.imgur.com/aFBk28s.jpg)](http://i.imgur.com/QdjRPr6.jpg)

Just a closer look at the floppy drive for good measure...

[![tp340-fdd](http://i.imgur.com/xMsL4j5.jpg)](http://i.imgur.com/SeLLuV7.jpg)

A key feature of these early ThinkPads was a very front-centric layout, with the
keyboard and the TrackPoint buttons pushed all the way to the front edge...

[![tp340-trackpoint](http://i.imgur.com/9n2jU61.jpg)](http://i.imgur.com/WdqXnNV.jpg)

The old-styled model display, much like what we have post-40 series[7].

[![tp340-model](http://i.imgur.com/mghWGzX.jpg)](http://i.imgur.com/Ib9VOJX.jpg)

And the 340 was one of the earliest ThinkPads to have a button-based power
switch, rather than the spring loaded ones found on virtually all other models
before Pentium III ThinkPads (roughly). And of course, like a good ThinkPad
should be, it comes with a full array of LED indicators.

[![tp340-led-power](http://i.imgur.com/xEADYCV.jpg)](http://i.imgur.com/gKsYA3g.jpg)

The back side comes with all the standard ports that people should need before
USB became popular.

[![tp340-rear](http://i.imgur.com/ZUeP5du.jpg)](http://i.imgur.com/gIO7cdX.jpg)

And this particular 340 comes with the data/fax modem option.

[![tp340-modem](http://i.imgur.com/tGwlU59.jpg)](http://i.imgur.com/oIrAOL8.jpg)

The bottom is just as simple and easy to understand (and disassemble, you only
needed to remove 3 screws from the bottom to access the keyboard, and therefore
the floppy drive, hard drive, and the motherboard, and all the cards).

[![tp340-bottom](http://i.imgur.com/rwKkA11.jpg)](http://i.imgur.com/nlhd600.jpg)

Given that it is a laptop powered by a ~10W 486SLC2, it gets the Energy Star
compliance certificate...

[![tp340-energystar](http://i.imgur.com/IgXoUjK.jpg)](http://i.imgur.com/Xds3uj0.jpg?1)

The 340, given that it's a monochrome model, comes with a blue IBM badge, which
I personally prefer.

[![tp340-badge](http://i.imgur.com/C9ptFlJ.jpg)](http://i.imgur.com/zKMEv2q.jpg)

--------------------------------------------------------------------------------

Another distinct feature of pre-Pentium III ThinkPads was the graphical "System
Program", or "Easy-Setup" interface - essentially IBM's take on BIOS. I call
this the "Duckling" interface.

[![tp340-system-program](http://i.imgur.com/QuEq9uN.jpg)](http://i.imgur.com/HwR7o3f.jpg)

A date-and-time settings interface, just that.

[![tp340-date](http://i.imgur.com/X7p5sYd.jpg)](http://i.imgur.com/vnK8oaf.jpg)

The all-you-can-see pixel buffet!

[![tp340-pixels](http://i.imgur.com/tUrBYY0.jpg)](http://i.imgur.com/axhzBuh.jpg)

--------------------------------------------------------------------------------

The ultimate goal then, of this series, was to make my 340 functional again - by
my own standard, of course. I have the following main intentions for this
laptop:

- Run Windows 95 on it.
  - PuTTY, with SSH/Serial and Telnet, making it a weather station (Telnet,
    powered by [Weather Undergound](telnet://rainmaker.wundergound.com)).
  - Office 95/97, for my occasional to-do list-making, and blogging needs (it's
    just better to write it on a old computer with little distraction).
  - CD-ROM drive, just general CD music playback...
  - ... Whatever I could manage to put on it, more plans later.
- Run MS-DOS on it (possibly just MS-DOS 7.0 bundled with Windows 95).
  - Roland SC-88vl, and some fun with older games and MIDI music.
  - Disney Sound Source, the ultimate Amiga MOD solution (LOL).

Current wish-list:

- A PCMCIA sound card so my 340 could sing the Windows 95 tune and some fun
  wave files, or even MP3 (if the processor allows).

Let me know about your ideas!

--------------------------------------------------------------------------------

*I just loved the way this computer sits on my desk.*

[![tp340](http://i.imgur.com/2za8KSF.jpg)](http://i.imgur.com/yE3Iohe.jpg)

--------------------------------------------------------------------------------

P.S. For full-size images with full 16.7M colours, check out my Imgur album
[here](http://mingcongbai.imgur.com/).

--------------------------------------------------------------------------------

- [1] X, A, T, R series of ThinkPads, introduced in year 2000. Each represents
  ultraportable, desktop-replacement, professional thin-and-light, and budget
  lines of ThinkPads, respectively.
- [2] Hard Drive, Floppy Drive, and Optical Disc Drive/Zip Drive.
- [3] Both in terms of temperature and sensational sense...!
- [4] According to my own tests, Windows 95 works just fine with some minor
  attentions, Windows NT 3.51/4.0 works but were extremely slow and lacks power
  management support. More on that in Episode 2.
- [5] The 340 comes with 4MB of RAM on board, and there are only 8 or 16MB IC
  DRAM cards available, making it impossible to get any higher than 12MB of RAM.
  If you put a 16MB or even a ridiculous 32MB card into the 340, it will simply
  ignore the card, leaving you with 4MB of RAM.
- [6] Original article
  [here](http://ps-2.kev009.com/pcpartnerinfo/ctstips/b01a.htm).
