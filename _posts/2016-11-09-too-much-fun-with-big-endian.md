---
layout: post
title: (Too much) Fun with Big Endian
---

Using a Big Endian PowerPC as my main desktop is proven to be nothing less
than problematic - it's good - a good practice in filing bug reports, which
I did not seem to be good at.

So, here below is a list of bug reports I have opened so far, as an record
for later reference:

- [Freedesktop.org Bugzilla #98629: OpenGL applications warns "MESA-LOADER: failed to retrieve device information"](https://bugs.freedesktop.org/show_bug.cgi?id=98629)
- [Freedesktop.org Bugzilla #98630: Bad color and glitches on PPC64](https://bugs.freedesktop.org/show_bug.cgi?id=98630)
- [Freedesktop.org Bugzilla #98631: GPU lock ups when starting GDM, SDDM, and Plasma Desktop](https://bugs.freedesktop.org/show_bug.cgi?id=98631)
- [KDE Bugzilla #372202: Wrong coloring when running on Big Endian architecture](https://bugs.kde.org/show_bug.cgi?id=372202)
- [GNOME Bugzilla #774085: Bad coloring on Big Endian architecutre](https://bugzilla.gnome.org/show_bug.cgi?id=774085)
- [QTBUG #56975: QtQuick/QML displayed with wrong colors on Big Endian architecture](https://bugreports.qt.io/browse/QTBUG-56975)

That is indeed a whole suite of bug reports, but in the case of wrong colors
were displayed (especially on those rendered by GLX), I have filed numerous
bug reports across different projects - for the lack of knowledge on the
origin of this issue.

Some main take-aways, however, are collected from my conversation with these
developers:

- Currently, a possible way to work around nouveau-related GPU lock ups on
Big Endian machines is to remove nouveau_dri.so - that said, you will be using
LLVMpipe for your GLX applications - not efficient, but at least it doesn't
lock up any more (also, despite the wrong coloring).
- 64K paging is an absolute no-go for Big Endian PPC with nouveau.
- GNOME is (still) the slowest at responding to issues.

-------------

Still in hope, I am waiting for Plasma on my PowerMac G5.
