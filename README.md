# mac-gfx-research
# Reverse Engineered IOAcceleratorFamily2 & IOSurface Framework

**Complete reverse engineering of Apple's GPU acceleration frameworks, paired with the last Intel GPU driver provided by Apple**

![Status: Educational/Research](https://img.shields.io/badge/Status-Educational%20Only-blueviolet)
![Platform: macOS](https://img.shields.io/badge/Platform-macOS-lightgrey)
![Framework: IOAcceleratorFamily2](https://img.shields.io/badge/Framework-IOAcceleratorFamily2-blue)
![Framework: IOSurface](https://img.shields.io/badge/Framework-IOSurface-green)

## Overview

This repository contains **complete, line-by-line reverse engineered C implementations** of Apple's proprietary graphics acceleration frameworks, alongside the **last Intel GPU driver officially provided by Apple**. This represents thousands of hours of painstaking reverse engineering work to understand how macOS achieves hardware-accelerated graphics.

> **⚠️ IMPORTANT: This is for EDUCATIONAL PURPOSES ONLY**
> 
> This code is provided **solely to study and understand** how Apple's graphics drivers work internally. It is **not intended for production use**, nor does it replace any official Apple frameworks. All code is presented as a research artifact of reverse engineering efforts.

## What This Repository Contains

### Reverse Engineered Frameworks (C Code)

| Component | Description | Original Framework |
|-----------|-------------|-------------------|
| **IOAcceleratorFamily2** | Complete GPU acceleration framework used by Metal, OpenGL, and Quartz Extreme | `/System/Library/Extensions/IOAcceleratorFamily2.kext` |
| **IOSurface** | Shared memory management for GPU-accelerated graphics across processes | `/System/Library/Frameworks/IOSurface.framework` |


### Intel GPU Driver (Apple's Last Release)

The **last Intel graphics driver provided by Apple** (before transitioning to Apple Silicon) has been fully reverse engineered to understand:

## Educational Value

This repository serves as a **comprehensive case study** for:

1. **IOKit Driver Development** - Understanding how IOKit user-clients communicate with kernel drivers
2. **GPU Memory Management** - Learning about GTT, PPGTT, and GPU virtual addressing
3. **Display Pipeline Architecture** - How scanout works from IOSurface to displayed pixels
4. **Firmware Loading** - How GuC firmware is loaded and initialized
5. **Selector-Based IPC** - The selector mechanism in IOKit
6. **Reverse Engineering Methodology** - Approaches for analyzing binary kexts

## ⚖️ Legal & Ethical Notice

```
THIS MATERIAL IS PROVIDED SOLELY FOR EDUCATIONAL AND RESEARCH PURPOSES.

The code in this repository is a product of reverse engineering and is
provided to advance understanding of computer graphics architecture and
operating system internals.

All trademarks, framework names, and product names are the property of
their respective owners. Apple, macOS, IOKit, IOAcceleratorFamily2,
IOSurface, Metal, Quartz Extreme, and QuartzGL are trademarks of Apple Inc.

No claim of ownership is made over any proprietary code, nor is this
intended to replace or circumvent any official frameworks or drivers.
```

**Tools Used:**
- Ghidra

---

## How to Use This Repository for Learning

1. **Start with the Selector Maps** - Understand how user-clients communicate
2. **Trace the IOSurface Lifecycle** - From creation to scanout
3. **Study the GTT Implementation** - The heart of GPU memory management
4. **Analyze the GuC Firmware Flow** - Modern Intel GPU scheduling

---
