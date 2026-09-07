# Linux Mint in UTM — Everyday Quick Guide

## Start Linux
1. Open UTM in macOS.
2. Select the Linux virtual machine.
3. Click Play.
4. Log in to Linux Mint if prompted.

## Release the Mouse
Press **Control + Option** together once to release the pointer from Linux back to macOS.

## Hide / Show the macOS Dock
Press **Option + Command + D**.

## Shared Folder
- macOS: `Documents/Shared-Linux`
- Linux: `~/utm-share`

If the shared folder fails to mount after a known-good configuration, `sudo mount -a` was previously used as a remount step. Diagnose before changing persistent mount configuration.

## Stop Linux Safely
Use Linux Mint's Shut Down command or run:

```bash
sudo poweroff
```

For a normal restart:

```bash
sudo reboot
```

## Important Troubleshooting Note
This quick guide describes the everyday workflow. The separate `troubleshooting-record.md` preserves the September 2026 UTM crash stopping point. Do not reinstall or recreate the VM merely because the host-side UTM application is unstable.
