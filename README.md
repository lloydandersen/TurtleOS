# TurtleOS

**Live in the shell.**

A radical new exokernel operating system built for developers who want full control.

We are not another Linux distribution.  
We are not a competitor to Windows 11, macOS, or Linux.  
**We are the replacement.**

---

### Philosophy

TurtleOS gives applications and LibOSes direct, explicit control over hardware. The exokernel only multiplexes resources safely and provides revocation. Everything else belongs in userspace.

### Mantras

- Buy a new computer.
- Backwards compatibility is death.
- Developers are in charge — not the OS.
- All code in the exokernel is **C23**. No C++.
- If you cannot write code, do not use TurtleOS.
- Porting is forbidden. Write for TurtleOS.
- Use every transistor. Performance, efficiency, and security come from the hardware.
- All running code is trusted. Security is external.
- Clean, developer-focused, hardware-exposed.

---

### Hardware Support

TurtleOS aggressively targets **modern, high-performance 64-bit platforms**.

We currently **do not** offer official support for Apple M-series chips.

**Tested Single-Board Computers** (used for multi-architecture validation):

- **LattePanda IOTA** – Palm-sized x86 SBC (Intel N150, 8GB RAM / 64GB eMMC)
- **Orange Pi RV2** – RISC-V AI SBC (8GB RAM, 2 TOPS NPU, WiFi 5, BT5.0, Gigabit Ethernet, M.2 NVMe)
- **Orange Pi 4 Pro** – ARM64 SBC (12GB LPDDR5, Allwinner A733, 8-core 2.0GHz, 3 TOPS NPU, WiFi 6, BT5.4)

These boards enable affordable testing across **x86-64**, **ARM64**, and **RISC-V**. While we test on these platforms, future optimization will focus on the latest high-end chips in each architecture.

**Minimum RAM**: Designed to run comfortably under **512 MB**.

The system self-optimizes on first boot for your exact hardware.

---

### Use Cases

- **GPU Clusters & High-Performance Computing**: True exokernel design gives direct hardware access, making it ideal for high-throughput GPU/accelerator workloads where every cycle matters.
- **Desktop on Modern Minimal Hardware**: Even on relatively modest but recent hardware, TurtleOS often feels significantly faster and more responsive than heavier traditional operating systems on more expensive machines.
- **Research & Systems Experimentation**: Perfect for developers who want to build custom LibOSes, explore new scheduling policies, memory models, or driver architectures.
- **Embedded / Edge Performance Systems**: Low memory footprint with maximum hardware utilization.

---

### Key Features

- **True Exokernel**: Minimal kernel. Applications and LibOSes control scheduling, memory policy, filesystems, networking, and drivers.
- **Turtle Hatch** — Self-optimizing boot: Generic image detects hardware and rebuilds the entire system with PGO, LTO, cache-aware layout, and architecture-specific optimizations.
- **Custom C23 Compiler Suite**: Ships with the OS. Only C23 is supported. Full hardware targeting and auto-optimization for every application.
- **Full LibOS Kit**: Batteries-included library operating systems for gaming, databases, web, media, scientific computing, and more.
- **Head Mode (Default)**: Includes a curated set of native TurtleOS applications built with the LibOS kit — showcasing what’s possible with direct hardware access.
- **Live in the Shell**: The terminal is the primary interface — fast, powerful, scriptable, and deeply integrated with the exokernel.

---

### For Developers

- Write once, run optimally on *your* hardware.
- Full hardware exposure: direct access to caches, TLBs, power states, CXL, modern IOMMU, vector units (AVX-512, AMX, SVE2), etc.
- Instant revocation: The exokernel can immediately kill runaway applications and reclaim resources.
- No binary blobs. Strict internal development standards.
- First-class diagnostics and profiling tools.

---

### Development Schedule

TurtleOS uses a unique versioning scheme:

- **Major versions** are based on the **year** (e.g. `2026`, `2027`).
- **Minor updates** use letters (`2026a`, `2026b`).
- **Security updates** append numbers (`2026a.1`, `2026a.2`).

**Years are not compatible with each other.** Expect major, radical changes between yearly releases.

---

### Building & Running

1. Download the generic TurtleOS image (UEFI only).
2. Boot on supported hardware.
3. Let **Turtle Hatch** — the system will detect your hardware and rebuild itself optimized for your exact CPU, cache hierarchy, and devices.
4. Reboot into a blazing-fast, hardware-native system.

**Requirement**: You must be willing to write code. TurtleOS is not for users who want "it just works" with 20-year-old binaries.

---

### Status

Early development. We are currently building the exokernel core, capability system, physical memory manager, and initial LibOS framework.

We do not accept outside patches. All core code is written by the TurtleOS team.

---

**"Live in the shell."**

Made for people who understand systems and want to push hardware to its absolute limit.
