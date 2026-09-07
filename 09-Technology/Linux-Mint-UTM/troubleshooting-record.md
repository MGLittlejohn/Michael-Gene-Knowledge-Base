# Linux Mint / UTM — Troubleshooting Record

## Purpose
Preserve the exact September 2026 stopping point so future troubleshooting resumes from known facts rather than starting over.

## Host
- Late-2012 27-inch Intel iMac
- 3.4 GHz quad-core Intel Core i7
- NVIDIA GeForce GTX 680MX 2 GB
- 32 GB RAM
- macOS Sequoia 15.7.9 via OpenCore Legacy Patcher
- OCLP root patch v2.4.1

## Virtualization Setup
- UTM version: 4.7.5 (118)
- Guest: Linux Mint
- XRDP installed for remote access
- Goal: remote access to Linux Mint from MacBook Air

## VM Settings at Stopping Point
- VM RAM temporarily reduced from 8192 MiB to 4096 MiB during troubleshooting
- Display: `virtio-gpu-pci`
- Auto-resize: enabled
- Retina: off
- No display changes made at the stopping point

## Confirmed Behavior
- Mac typing behaves normally with UTM closed.
- Starting the Linux VM causes UTM itself to crash.
- Crash report identified:
  - Crashed Thread 0
  - `EXC_BAD_INSTRUCTION (SIGILL)`
  - Termination Reason Namespace SIGNAL
  - Code 4: `Illegal instruction: 4`

## Working Diagnosis Direction
Because the iMac has 32 GB of RAM and the failure presents as an illegal-instruction crash, memory shortage was not considered the primary cause. The next troubleshooting session should focus on UTM / Intel CPU / newer macOS / OCLP compatibility before changing the Linux guest installation.

## Do Not Do Yet
- Do not reinstall Linux Mint.
- Do not delete or recreate the VM.
- Do not alter the VM disk or networking simply to test guesses.
- Do not make unnecessary display changes.

## Next Steps
1. Confirm UTM build compatibility with this Intel/OCLP host.
2. Review CPU/emulation/virtualization settings that could produce SIGILL.
3. Preserve the existing VM disk while testing host-side configuration.
4. Once UTM is stable, RAM may be restored/increased from the temporary 4096 MiB setting.
5. Resume XRDP/MacBook Air remote-access testing only after the VM launches reliably.
