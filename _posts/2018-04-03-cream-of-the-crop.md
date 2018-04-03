---
layout: post
title: Cream of the Crop? The ThinkPad T61p Upgrade
---

The Lenovo ThinkPad T6 series has always been a favourite of mine since I
first saw one in ~2010 when I serviced my friend's T60. To be fair, I shared a
ThinkPad X61t with my father which was honestly awesome for its size (and the
XGA resolution was by no means problematic), but the T60... Oh boy, a bright
SXGA screen, large keyboard (never a fan of the small backspace key on the X6
series), and ATI Radeon X1300 graphics.

Not to present myself more knowledgable than I really was, I honestly cared
for the graphics card than anything else. In my early teens, my brain was filled
with Compiz and a good round of Need for Speed - the GMA 965/X3100 simply
won't deliver the latter, nor would it do the former any better.

*I tried not to salivate too much when I wiped the T60 clean as I was finishing
my work...*

----

That dream came true in the summer of 2016 when I got a 4:3, 14.1-inch T61
from a [ThinkPads Forum](https://forum.thinkpads.com/) member. I specifically
asked for a model with Intel graphics, in concern that NVIDIA wouldn't behave
with Linux (which I found out it does after the upgrade , which I will get
into later).

My T61 came with a beautiful 1400x1050 SXGA+ panel, which was quite a
refreshment from my X250 which I got as a replacement just one year earlier -
which simply wouldn't cut it for my school work as a history major, nothing's
wrong, apart from its narrow and short 12.1 inch screen. I got the laptop
sans-CPU, RAM, HDD, or battery - which was sorted with ~100 USD, which landed
me with...

- Intel Core 2 Duo T9300 @ 2.5GHz.
- 8GB DDR2 800MT/s, KomputerBay.
- 1TB Crucial MX300 (from X250).
- 9 Cell Battery.

I purchased an UltraBay battery as well, to simulate the awesome Power Bridge
system from the X250 - which gave me 6-8hrs of battery life writing documents
(and with WLAN/BT turned off).

The T61 is a great laptop as it was configured, with its absolutely ample
array of ports and extremely sturdy construction (with its magesium alloy
interior frame). Not to mention the ThinkLight, which I really missed from
earlier ThinkPads, remember this...

*The ThinkLight has never been a keyboard lighting by design, it works
plenty well as a lamp at night...*

----

*The art of addition...* The true evil of owning a ThinkPad comes with the
ability to reconstruct your very own to your likings, and T61 could have
been one of the easiest to take apart and upgrade.

My only complaint with my T61 was its inability with video playback at
anything higher than 720p, so I tried Broadcom's CrystalHD, which worked
sufficiently well - until the driver was no longer in active development,
and a Linux Kernel upgrade could turn into hours with fiddling with its
driver source code.

Well, perhaps I shouldn't have looked into the culture of T61, specifically,
the [ThinkPad T61 Wiki](https://t61.wikispaces.com/) by TuuS. That's when
I discovered the existence of a 14-inch, 4:3 T61p model, which offers an
NVIDIA Quadro FX570M graphics card (equivalent to a 8600M GT) - woah, how
could I not have that, not only would I be able to watch videos again, some
Need for Speed: Most Wanted and Carbon would spice my days up tremendeously!

But it turns out that finding a T61p motherboard is not difficult until
you began to look for a 4:3 model. The T61's 4:3 models are rare as is,
as I would imagine the bulk of the machines were purchased as 16:10, 14/15
inch models here in the States, and probably elsewhere. Another issue with
these motherboards is that, with a 35W cTDP on the Quadro and some issues
with the 8000-series NVIDIA mobile graphics chips, which leads to the chips
desoldering themselves, and corrupted video output. With this circumstance
then, the T61p (and all NVIDIA-enabled T61 motherboards in general) seen
two batches of motherboards, the latter of which produced since Q3 of 2008.
With a strong T61 user community even to this day, sourcing a good T61p
motherboard couldn't be more difficult, especially for a good price.

I guess I finally lucked out, as wujstefan from the ThinkPad Forum decided
to sell his T61p motherboards along with some spare parts - now time to
jump on it. I ended up grabbing two for some nearly unreasonable amount of
money, but hey, when would I find the next one? This kind Polish man
offered to send me the motherboards along with two T61 frames just to make
sure they arrive in one piece - and the frames could also be kept as spares.

The parts came in yesterday, and so the surgery begins...!

----

*Please to excuse the lower quality pictures, that I took with my phone,
time has not been a luxury I could afford lately.*

Along with the motherboards I decided to replace my RAM sticks with some
more reputable modules. So I've purchased two sticks of Elpida RAM, which
came with metal heatsinks (!), and runs at a lower voltage (which makes
the former feature less appealing, but hey, it looks damn good).

![[elpida](https://i.imgur.com/NMGbJvg.jpg)](https://i.imgur.com/QofE7K4.jpg)

And so it begins. The T61 is extremely easy to take apart with just one
part held in with clips, the keyboard bezel - which I got a spare from
the same guy just in case. It took me less than 20 minutes until the
motherboard was extraced first from its outer black casing, then the
magnesium structual frame.

Reversing the process obviously reassembles the computer, but I just had
to stop to admire the cooling module of the T61 - it's heavy sure, but why
wouldn't any manufacture stop painting their copper heatsinks black?

![[cooling](https://i.imgur.com/1KAMcdc.jpg)](https://i.imgur.com/5A51k0A.jpg)

With the machine semi-assembled, time to do a power-on test...

![[test-time](https://i.imgur.com/3C5Jc3M.jpg)](https://i.imgur.com/3C5Jc3M.jpg)

Success, on the most part. The motherboard I got was a Merom-generation
motherboard (though from the 2nd batch), and the processor - which I forgot
to mention that I upgraded to a X9000, is from the Penryn generation. The
newer Penryn-based Core 2's came with a digital thermal sensor, which the
Merom motherboards don't support. However, the machine would function and
boot, despite the "Thermal Sensing Error" and two loud beeps.

So to rectify this issue, one could flash the "Middleton" BIOS, which...

- Silences the "Thermal Sensing Error".
- Unlocks SATA 3Gbps speed on the main HDD bay (why not officially?).
- Removes whitelist for wireless and GPS modules.

Or even better, one could get an under-voltage BIOS, made by a 51nb forum
member "highsun", and provided [here](https://forum.51nb.com/forum.php?mod=redirect&goto=findpost&ptid=1472071&pid=25744369).
"highsun" claims that Lenovo runs the NVIDIA GPUs with a higher voltage than
necessary, which generates more heat - and drastically decreases battery
runtime. He further discovered that the T61 came with PCIe
[Active State Power Management](https://en.wikipedia.org/wiki/Active_State_Power_Management)
which was disabled for some reason. "highsun" recommends running NVS140Ms
at 0.9V and the FX570M at 0.95V - as opposed to the 1.15-1.25V defaults.

Flashing the BIOS would require that you make a DOS boot disk, and to
flash the BIOS with the `phlash16.exe` executable from Phoenix - using
the following command line...

```
PHLASH16 BIOS.ROM /S /X /C /MODE=3
```

Where `BIOS.ROM` is the file name of the ROM file you would download from
that Forum page. Before the flashing begins, there will be an error
stating a checksum error, just press Y to continue.

![[flash](https://i.imgur.com/fIxuCy8.jpg)](https://i.imgur.com/HRjoecx.jpg)

After the flash (which should take around 2-3 minutes), the programme will
prompt to reboot the computer - which it wouldn't do. The T61 will be
*powered down* instead of rebooting - so don't worry if nothing displays
on the monitor after you confirmed the prompt, just press your power button
and it should boot right up. The first boot will also output an error
that your CMOS checksum is incorrect, just go into the BIOS setting, and
save your settings again.

At this point, time to replace your clear plate from "T61" to "T61p" to
celebrate this great success!

![[t61p](https://i.imgur.com/9wTipqi.jpg)](https://i.imgur.com/sVRa6pA.jpg)

----

Now, time to do a review of the machine in its new form, is it really the
cream-of-the-crop ThinkPad I was hoping for? And how are the...

["OUT OF THE BOX THERMALS." — Steve Burke](https://www.youtube.com/watch?v=c3PnOsdDPWY)

![[lord-steve](https://i.imgur.com/gQJAVuL.jpg)](https://i.imgur.com/i04wBBe.jpg)

I'm happy to report that it is save to use a Core 2 Duo X9000 @ 2.8GHz and
the Quadro FX570M within a 14-inch T61 chassis, as long as the cooler has
been upgraded for use with a dedicated graphics card (FRU 42W2820), and
a decent thermal interface material has been used. At is stands, with the
0.95V BIOS, the machine idles at...

- 45-47℃ for the CPU
- 45-50℃ for the GPU

The CPU, for its +10W cTDP over the cooler's spec, will heat up
*significantly* under sustained load (say, a Prime95 torture test, which
heated it up dangerously close to 90℃). The graphics chip however, behaved
nicely, running at ~65℃ with a round of Need for Speed: Carbon running at
full effects (no AA) at 1024x768.

![[cooling](https://i.imgur.com/eRVrBA1.jpg)](https://i.imgur.com/kRKN9w2.jpg)

So I'd call it a pass. Not to mention that Need for Speed: Carbon runs at
over 30fps with the stated graphics settings, which is much better than I
anticipated - it's now sort of a gaming ThinkPad - well, within a certain
time scope. I have seen people playing Battlefield 3 on these machines so
I suppose it's not that much of a surprise...

However, one remaining complaint or note would be concerning the power
consumption. The graphics chip, processor, and CCFL backlight (which I
could not praise enough of) are major sources of power consumption, my
T61 now idles at ~15W of power consumption, and jumps to 20-25W when
browsing the web (including YouTube playback), and much higher when playing
games or using graphics intensive applications. The machine will also
*require* a 90W power adapter, as opposed to the 65W one shipped with most
models - otherwise, the battery may not charge when under load, and the
power adapter will also heat up significantly in this case. Though with
two batteries installed, at least battery runtime is till higher than 4
hours, which I can live with.

----

But to answer the question in the title, I'd almost say yes. The T61 has
been packed with as much hardware as it could within the confines of this
relatively compact chassis - and within the official hardware support, the
best hardware has been added to it. The result is, then, performance
reasonably usable by today's standard - as long as you steer clear of
stupidly JavaScript-packed websites like [BBC](https://bbc.co.uk/) and
[CNN](https://cnn.com/) - nothing against liberal media, but damn, strip
down your website or at least provide something more basic, okay?

As to the "almost" part, it comes back to the "evil" of allowing upgrades
and modifications. The T61 could be modded to use FSB1066 Core 2
processors, allowing for going beyond the current X9000 maximum, which
runs on a 800MT/s FSB, and potentially quite a boost on responsiveness.
Not to mention the possibility to use quad-core Core 2's with some
further modifications.

Well, I'd leave it here for now, as the FSB mod requires some soldering
work which I couldn't lie to say I'm capable of, and that it requires
multiplier-unlocked (SPD unlocked) RAM modules so that they could run
within spec given an FSB uplift, which are exceptionally hard to find.
As it stands, I have, if I do say so myself, an exceptional example of
a ThinkPad, with an indefinite lifetime, and no fear for future repairs
and refurbishment - which is not something that could be said for ThinkPads
of today.

![[full-view](https://i.imgur.com/BeKQSke.jpg)](https://i.imgur.com/YOEoXCD.jpg)
