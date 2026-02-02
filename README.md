# ops-toolkit-usb

# ops-toolkit-usb

## Overview
This repository documents the creation and organization of a dedicated "Ops Toolkit" USB drive. This drive serves as a portable field kit for system recovery, OS provisioning, and offline technical reference.

## Hardware & Software
- **Media:** 32GB USB 3.0 Flash Drive
- **Method:** Dedicated Bootable Installer (No multi-boot overhead)
- **OS Image:** Ubuntu 24.04.3 LTS (Noble Numbat)

## Why This Matters (Security/Ops Perspective)
- **Air-Gapped Reference:** Provides critical manuals and tools when network access is unavailable.
- **Integrity:** Using a dedicated installer ensures a clean, predictable baseline for every rebuild.
- **Efficiency:** Reduces "Time to Restore" (TTR) for failed hardware.

## Drive Structure
- `/isos/` - Verified OS images.
- `/manuals/` - PDF documentation for Ubiquiti, DW Spectrum, and AWS Security.
- `/scripts/` - Baseline configuration scripts for new Linux installs.

## Lessons Learned
- **Flashing vs. Copying:** Confirmed that flashing an ISO creates a bootable partition table, overwriting existing data.
- **UEFI Compatibility:** Verified that modern HP hardware requires GPT/UEFI formatting for the installer to be recognized.
