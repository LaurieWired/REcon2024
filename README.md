<div align="center">

![logo](media/bad_unboxing_logo.png)

---

[![GitHub stars](https://img.shields.io/github/stars/LaurieWired/REcon2024)](https://github.com/LaurieWired/REcon2024/stargazers)
[![Follow @lauriewired on Twitter](https://img.shields.io/twitter/follow/lauriewired?style=social)](https://twitter.com/lauriewired)

</div>

---

# Manipulating Android Malware to Self-Unpack

Malicious Android applications use packing as the core technique to conceal payloads from manual and automated analysis. But what if we could force malicious Android applications to drop their payloads by unpacking themselves?

# Description

This presentation will introduce an automated and platform-independent method to autonomously unpack Android APKs. Java-based Android packers generate a unique stub per app whose sole purpose is to decrypt and load the malicious payload from inside Android’s Application subclass. I will describe the process for extracting and translating the Dalvik Bytecode, resources, and native code from these stubs into self-unpacking entities. Because the Android Framework is built on top of Java, the automation process must strip all Android-specific API calls and replace them with equivalent Java invocations. 

The new app can then be produced in one of two forms: a purely Java application that avoids Android emulator requirements, or a defanged version of the original APK after bytecode manipulation. This technique eradicates the need to write custom decryptors for packed Android applications while remaining entirely packer-agnostic.
I will demonstrate and equip attendees with BadUnboxing, a new open-source tool that automatically generates benign versions of Android malware to dump malicious payloads. I will also share my methodology for repackaging defanged APKs.

# Slides

Slides Available Here: [Slides](https://github.com/LaurieWired/REcon2024/blob/main/REcon_2024_Slides.pdf)

# BadUnboxing Repository
The [BadUnboxing](https://github.com/LaurieWired/BadUnboxing) repository contains a tool written to automatically generate custom unpackers for Android malware.



