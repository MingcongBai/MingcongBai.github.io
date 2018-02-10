---
layout: post
title: The "Y.M.F.", Lenovo ThinkPad L420 - 1/3, Bring In the New
---

**Out with the old, and in with the new.** In many ways, the ThinkPad L420
replaces my last ThinkPad, and the first ThinkPad I've ever owned. Confusing,
I know - and the fact that I wanted to write this blog post as a review and a
commentary on the "modern" designs of ThinkPads and notebook computers in
general really didn't help clearing this claim up.

Let's start by talking about my last ThinkPad - The ThinkPad T61... It was
truly a great partner in my academic and open source related activities. With
its tall and spacious 1400x1050 screen, unquestionable keyboard, and an
exceptionally sturdy chassis, it seemed very strangle (even to myself) that
I decided to swap it out just after a year. Several things happened that aided
me to justify for a replacement...

- The processor, an Intel Core 2 Duo T9300, while still adequate for school
  work, SSH, and light Web browsing, is lacking in its multiprocessing
  performance and newer instruction set support.
    - I obtained a Canon EOS 6D as a gift from my parents for my high school
      graduation, which I felt guilty for leaving it in the camera bag. Setting
      the DSLR up to take pictures in RAW (.CR2 in this case) means that I have
      to process the pictures, and export it in a commonly readable format. I
      found this process incredibly slow on the T61 for its lack of threads and
      in fact, single thread performance (on a single export process). Taking
      more than 2 minutes to export the images alone made it impossible to
      process and organise a trip's worth of pictures (500+).
    - LibreOffice is a shitty software package when it comes to optimisation,
      while writing plain papers it is fast enough on my T61, new windows could
      take more than 5 seconds to draw.
    - Heavy websites with unnecesary JavaScript party tricks, making scrolling
      through a news (!) website an annoying affair - take the BBC homepage
      for example, when would this website stop loading hundreds of elements
      while drawing all sorts of animations, **and** trying to play videos
      automatically. With the only two threads available, browsing heavier
      Web pages has become much like compiling codes with two threads.
    - With the case of Web browsing above, it is no longer possible to maintain
      a sub-15W power consumption even with the `powersave` P-State preset -
      not to mention the significant performance slow-down. It is become more
      arduous to use this computer even for a read of news than I really wanted.
      Sure, I could have used a RSS reader, but some news websites are only
      willing to provide you with a sentence long summary - forcing you to open
      up their pages made with complete arrogance in artistic pursuits and
      ignorance in the need for simplicity.
- The graphics unit, the computer came with a GMA965 (Graphics Media
  Accelerator, heh...) which is not even capable of holding 30fps on 720p
  videos - I have bought a Broadcom CrystalHD to aid with video decoding but
  after all, some applications are just completely unable to utilise it. So
  earlier last year, I purchased a motherboard with a new-old-stock NVIDIA
  Quadro NVS140m GPU in hope of it making 1080p playback possible...
    - I was wrong, very wrong. Sure, I'm now able to playback 1080p videos,
      though in a fashion quite similar to playing 720p videos on a GMA965 -
      unstable framerates and occasional lock ups. The NVIDIA proprietary
      driver for Linux on the other hand, I have to praise for its stability
      over Nouveau (for obvious reasons), and even its Intel counterpart.
    - Creative work... Yes, I'm dumb for expecting Inkscape and GIMP to work
      well on a 2007 laptop. While GIMP simply suffers from slow redraws, which
      I could live with (as someone who used a Pentium MMX laptop until 2007) -
      Inkscape simply refuses to redraw at times of higher loads, making it
      necessary to restart the programme regularly.
    - Remember the power consumption issue I mentioned earlier, well, now you
      have another 10W to worry about - good luck getting more than 3 hours
      of battery life, during which you will suffer with your processor.

So that's enough issues to warrant for a surrender and admit your mistake for
spending money on a 2007 laptop, right? Well wait until you hear about the
Meltdown and Spectre issues, what a fatal blow. According to a benchmark by
Phoronix regarding the effect of KPTI (Kernel Page Table Isolation) and
Retpoline patches in the Linux Kernel, where Michael Larabel tested the
negative performance impact on
[Clarksfield and Penryn ThinkPads](https://www.phoronix.com/scan.php?page=article&item=pre-pcid-kptiretpoline&num=1).

Well in short you are taking some more performance discounts, and I could
certainly feel that with the patches pushed into AOSC OS's updates. With
LibreOffice now taking over 20 seconds to load up on my Crucial MX300 SSD
(granted, on a SATA-II interface, it took less than half that time before),
I called it a quit and started hunting for a new ThinkPad.

--------

*Price is a factor...*

Since I sold my ThinkPad X250 to a friend (afte I got the T61), I have declared
it a personal baseline to never buy a new ThinkPad again. Surely I was out
of my mind? Except I'm not.

I spent less than 500 U.S. Dollars' worth of Chinese Yuan on this machine,
getting an i3-4010U and 4GB of RAM, while spendng another 200 on a 1TB Crucial
MX300. That's already more than 600 dollars spent, and how about another 50 on
a stick of 4GB DDR3L SODIMM to make it roughly usable for some development work,
and another 50 on a sweet A.F. backlit keyboard? Cool, but that i3 is really
not cutting it (I would venture to say that it is marginally slower in my last
X61t in some cases, for its more aggressive powersaving settings; granted, I got
much faster graphics and hardware video codecs), cool, another 200 for a i5
motherboard?

And you see how it goes now, that's close to 1,000 U.S. Dollars down the drain
for a still mediocre performing laptop. Not to mention the pathetic designs
of newer ThinkPads, with their stupendously made "unibody" bottom cover, with
tens of tiny plastic clips that breaks off the first time you take it off; oh
yeah, and that huge chrome Lenovo logo (I get it, it's not an IBM, thanks!)...

Now, how about a sub-200 ThinkPad with significantly superior performance, with
which you could take it apart without a plastic pryer, and freely replacable
processors, SODIMMs, and mPCIe expansion cards? Hell yeah I would take that
over a slim ThinkPad any day of my life.

--------

*The hunt...*

Now, what do I want to get?

- Something fast... Something I won't be concerned entering the stupid and
  bloated Web 2.0 Land with. Oh yeah, I would like 1080p60 playback please?
- Classic keycaps. While I don't hate the new chiclet keyboards, I would still
  like the tall keycaps as I had with the T61 - and the old full-height
  Trackpoints are just more comfortable to use.
- Optical disc drive. I'm not ready to give up my Кино and Red Hot Chilli
  Peppers albums on CDs, and I still have the habbit of backing up my
  photographs on DVDs and send them to my home in China. I still remember
  how much I hated to use the Asus USB CD/DVD-RW drive, for how loud and slow
  it was.
- LED indicators. Need I explain?
- Replaceable parts, namely the CPU, the SODIMMs, and the wireless card. From
  my experience with the X250, it is very expensive to change or fix anything
  with stuff soldered on the motherboard.
- Good cooling. Again, this is one of those things that all human beings want.

Off I went with a browse on the [ThinkPad-Wiki](http://thinkwiki.de/), yes,
the one in German. Right off the bat, the X and X1 series, and any s-suffixed
T series are out of question. I wanted something large enough but not large
enough to warrant as a desktop replacement, so anything 14 inch - right, an E,
L, or T of the Sandy Bridge era...

- T420, L420, or the E420?
- It simply doesn't sound like a good idea to go with an E series, as it costs
  the same on eBay as the other two, and that I'm not a big fan of the rounded
  corners and huge logos.
- Leaving me with the T420 and the L420, with the latter marginally cheaper.
  The two are identical as in upgrade potentials, apart from the screen. While
  the T420 is more refined and premium, having built one for my friend I found
  this particular model lacking in cooling performance, and the screen border
  is disporportionally large on the bottom side.
- The L420 however, lacks a 1600x900 option - leaving me with only 1366x768. But
  I rarely multitask, in the sense of tiling windows, and it's just about
  enough for document writing. It will never be as tall and spacious as the
  T61 either way.

--------

*Bringing it home...*

I went with a L420 in the end, with a 80 U.S Dollars price tag on eBay. The
laptop was to be sold in a lot of 5, but I convinced the seller to sell me just
the one with a fingerprint sensor. Now, onto the exras and replacements...

- 2 * 4GB Corsair ValueSelect DDR3 @ 1333MT/s - 45 USD
- 1 * Atheros AR5B22 - 4 USD
- 1 * Intel Core i7-2860QM (bought and returned a 2640M) - 70 USD
- 1 * Russian layout keyboard - 40 USD
- 1 * Replacement palmrest (original came with a cracked palmrest) - 10 USD

Carried over from the T61 are...

- 1 * 1TB Crucial MX300
- 1 * ExpressCard to USB 3.0 Adapter

And the total comes to just over 200 USD, with six extra (logical) cores, faster
RAM modules, and SATA-III, it is hard to say it's not a great upgrade from the
T61. Now, before I make this part way too long, I'll start working on Part II
of this blogging series, in which I would review this L420 from my own
perspective.
