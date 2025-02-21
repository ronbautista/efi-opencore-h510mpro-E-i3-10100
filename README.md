EFI OpenCore H510M-PRO-E i3-10100f

Overview

This repository contains an EFI configuration for setting up macOS on a Hackintosh using OpenCore. The configuration is specifically designed for the following hardware:

Hardware Specifications:

Motherboard: MSI H510M-PRO-E

Processor: Intel Core i3-10100F

GPU: Modified XFX Radeon RX 560

Bootloader: OpenCore

Features

Stable macOS installation with OpenCore

Proper USB mapping

Patched ACPI files for better compatibility

Optimized power management

Native macOS performance on supported components

Compatibility

macOS Versions Tested:

macOS Monterey (12.x)

macOS Ventura (13.x)

Working Components:

GPU acceleration

USB functionality (mapped)

Ethernet connectivity

Audio with AppleALC

Proper SMBIOS configuration

Installation Instructions

Prepare macOS Installer

Create a bootable USB using macOS and OpenCore

Copy EFI to USB

Download the EFI folder and place it in EFI partition of the USB

BIOS Settings (Required Changes)

Disable Secure Boot

Set SATA Mode to AHCI

Disable Fast Boot

Enable Above 4G Decoding

Enable XHCI Hand-off

Boot into macOS Installer

Use the OpenCore boot menu and install macOS

Post-Installation

Mount EFI partition and copy the EFI folder to the macOS drive

Generate SMBIOS using OpenCore Configurator

Notes & Fixes

i3-10100F lacks an iGPU, so macOS must rely entirely on the RX 560 for display output.

Ensure WhateverGreen.kext is included for proper GPU acceleration.

USB mapping is pre-configured but may require adjustments based on your setup.

If experiencing boot issues, check logs and update OpenCore/Kexts as needed.

Resources

OpenCore Official Guide

Hackintosh USB Mapping

Disclaimer

This EFI configuration is provided as-is without any guarantees. Always backup important data before proceeding. Use at your own risk.
