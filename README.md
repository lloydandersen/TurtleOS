# TurtleOS

**Live in the shell.**

A radical new exokernel operating system built for developers who want full control.

We are not another Linux distribution.  
We are not a competitor to Windows 11, macOS, or Linux.  
**We are the replacement.**

### Philosophy

TurtleOS gives applications and LibOSes direct, explicit control over hardware. The exokernel only multiplexes resources safely and provides revocation. Everything else belongs to user space.

**Mantras**
- Buy a new computer.
- Backwards compatibility is death.
- Developers are in charge — not the OS.
- All code in the exokernel is C23. No C++.
- If you cannot write code, do not use TurtleOS.
- Porting is forbidden. Write for TurtleOS.
- Use every transistor. Performance, efficiency, and security come from the hardware.
- All running code is trusted. Security is external.
- Clean, developer-focused, hardware-exposed.

### Hardware Support

We aggressively target only modern, high-performance platforms:

**x86-64**
- Intel: Core 13th/14th/15th gen, Core Ultra (Meteor Lake+), Xeon Scalable (Sapphire Rapids+)
- AMD: Ryzen 7000/9000 series, Threadripper 7000+, EPYC 9004/9005 series

**ARM64**
- Recent Apple Silicon, Ampere Altra, Qualcomm Snapdragon X Elite/Plus, and other high-end implementations

**RISC-V**
- Top-tier cores (especially those popular in China). Older chips accepted due to ecosystem realities.

**Minimum RAM**: Designed to run comfortably under **512 MB**.  
The system self-optimizes on first boot for your exact hardware.

### Key Features

- **True Exokernel**: Minimal kernel. Apps and LibOS control scheduling, memory policy, file systems, networking, drivers, etc.
- **Turtle Hatch** — Self-optimizing boot: Generic image → detects hardware → recompiles entire system with PGO, LTO, cache-aware layout, and architecture-specific intrinsics.
- **Custom C23 Compiler Suite** ships with the system. Only C23. No legacy ANSI C. Full hardware targeting and auto-optimization for every app.
- **Full LibOS Kit**: Batteries-included library operating systems for common domains (gaming, databases, web, media, scientific computing, etc.). Build any app without fighting abstractions.
- **Head Mode (Default)**: Comes with a curated set of native TurtleOS applications built using the included LibOS kit. Demonstrates what is possible when you have direct hardware access.
- **Live in the Shell**: The terminal is the primary interface. Powerful, fast, scriptable, and deeply integrated with the exokernel.

### For Developers

- Write once, run optimally on your hardware.
- Full hardware exposure: direct access to caches, TLBs, power states, CXL, modern IOMMU, vector units (AVX-512, AMX, SVE2), etc.
- The exokernel can instantly kill runaway applications and revoke capabilities.
- No binary blobs. No out-of-tree patching. Strict internal development standards.
- Diagnostics and profiling tools are first-class citizens.

### Building & Running

1. Download the generic TurtleOS image (UEFI only).
2. Boot on supported hardware.
3. Let the Turtle Hatch — the system will rebuild itself for your exact CPU, cache hierarchy, and devices.
4. Reboot into a blazing-fast, hardware-native system.

**Requirement**: You must be willing to write code. TurtleOS is not for users who want "it just works" with 20-year-old binaries.

### Status

Early development. We are building the exokernel core, capability system, physical memory manager, and initial LibOS framework.

**We do not accept outside patches.**  
All core code is written by the TurtleOS team.

---

**"Live in the shell."**

Made for people who understand systems and want to push hardware to its limit.
