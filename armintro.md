## An introduction to exploitation on ARM
### Part 1: Getting set up

This tutorial will cover the basics of **exploit development** on the **ARM platform**. This is aimed at beginners interested in exploit development and **hacking** so you shouldn't need too much knowledge on this subject before reading. You should, however, have a basic understanding of how a CPU works, binary, hex, what assembly code is and how to program in C.

To follow along with this tutorial you will need a **32 bit** ARM device. As I focus most of my work on iPhones and iOS, I will use an **iPhone 4** for this tutorial. This device has the **Apple A4 chip (S5L8930X)** which is an **ARMv7 (32 bit)** processor. You can use any other 32 bit iOS device for this tutorial but the iPhone 4 is probably the best device as it's latest supported version is 7.1.2 which is publicly jailbreakable whereas other 32 bit devices' latest versions may not be publicly jailbreakable and so you may have to wait for a new jailbreak release before being able to follow along with this tutorial.

If you have a **64 bit (ARM64)** device, you can still attempt to follow along with this but there will be some complications so you may have difficulty following it exactly.

To get started you'll need to install a few tools that'll allow you to compile C code on-device and debug it. Add http://cydia.radare.org to your Cydia sources and install `radare2-arm32`. This will install the **radare debugger** onto your device which will be useful later for analysing code and disassembling programs to understand how they work.

Also add http://coolstar.org/publicrepo and install `LLVM+Clang`. This will allow you to compile C programs on-device without the assistance of a computer. You'll also need an **SDK (Software Development Kit)**. I'm currently using the iPhoneOS8.1.sdk on my device. You can download these online or move them over to your device from Xcode on your Mac.

![alt text][logo]

[logo]: https://github.com/Billy-Ellis/Billy-Ellis.github.io/clang.png

The other 2 essential things are `iFile` and an iOS terminal emulator of your choice (in my case, `MTerminal`). I assume the majority of people will already have these 2 applications installed.
