# Node WebRTC f/ source for armv6 RaspberryPI Zero
Build Node-WebRTC From Source for armv6 Raspberry PI Zero
2019/August

This tutorial is about building NodeJS WRTC Module from source code, targeting the ARMv6 on a Raspberry PI Zero, using an AMD/Intel x86 Desktop PC with GNU/Linux as the development system.
The procedure also builds the WebRTC library (used by the NodeJS WRTC Module).

A cross compiler (x86 to armv6) is needed, so in August/2019 I searched for a recent version of the a Cross GCC Compiler to use and did NOT found one (a GCC version 5.4 was/is needed), so I decide to investigate about how to build one myself, which turn out to be quite easy, by using the Crosstool-NG builder.

I succeed, and the result is that WebRTC DataChannel is working on the RPI Zero.

WebTorrent
I was very happy to see that WebTorrent is also working on the RPI Zero, using the same binary result achieved by the compilation process.


Here are the 3 steps, in its overview/simple form:

1) Using Crosstool-NG and the provided configuration file, build your own cross compiler x86 to ARMv6.

2) Then, go to the Node-Wrtc Github page and follow the provided preparations instructions (install needed soft, etc), that already exists for cross compilation for ARMv7 and ARMv8.

3) Use the 2 modified scripts provided here, replace the existing originals with these (modified) ones, and run the cross compilation process.
