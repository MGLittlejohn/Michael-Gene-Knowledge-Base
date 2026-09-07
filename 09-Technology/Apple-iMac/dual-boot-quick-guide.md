# Late-2012 iMac — macOS / Linux Dual-Boot Quick Guide

## Startup Rule
When turning on or restarting the iMac, hold the **Option** key until the startup-drive screen appears.

## Boot macOS Sequoia
1. Turn on or restart the iMac.
2. Immediately hold **Option**.
3. Choose the **EFI Boot** entry with the blue OpenCore icon.
4. Press Return/Enter and allow OpenCore to start macOS Sequoia.

Because this older iMac uses OpenCore for newer macOS support, use the OpenCore boot path rather than treating the unsupported macOS installation as a normal native boot.

## Boot Linux Mint
1. Turn on or restart the iMac.
2. Immediately hold **Option**.
3. Choose the Linux EFI boot entry, not the blue OpenCore macOS entry.
4. Press Return/Enter.

## If the Wrong Entry Is Chosen
Allow the machine to boot if practical, restart, hold Option, and choose the other entry. Do not modify partitions merely because the wrong startup icon was selected.

## Historical Disk Layout
A prior working configuration recorded approximately:
- 601 GB for macOS Sequoia
- 150 GB for Linux Mint
- EFI boot partition(s)

Treat these sizes as historical configuration notes, not instructions to repartition the machine.

## Preservation Rule
Do not erase, repartition, or reinstall either operating system as a first troubleshooting step. Preserve the working disks and boot entries while diagnosing host/boot/virtualization problems.
