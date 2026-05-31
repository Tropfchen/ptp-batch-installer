# Automatic PTP-format Livery Installer for Microsoft Flight Simulator X-based Simulators

## What this software does

Automates use of `ptp-converter.exe` — the tool OC3 used to unpack .ptp files while installing liveries for P3D.

## Quick Start

1. **Download** the latest release.
2. **Install** PMDG Operations Center 3 (or copy `ptp-converter.exe` into the same folder as `ptp-batch-installer.exe`).
3. **Drag & drop** your livery files onto `ptp-batch-installer.exe`.

Done — liveries and panel files will be unpacked and moved to their proper locations.

## Advanced Use: Command Line

Run the script from a terminal or command prompt.

- **Example: Install to Prepar3D V4 only**:

```bash
ptp-batch-installer.exe -s p3dv4 "air_berlin_738.ptp" "747 Pan Am Clipper.PTP"
```

### Arguments

- `-s` / `--sim`: Specify the simulator by name or path.
- `-n` / `--dry-run`: Simulate the installation (no changes made).
- `-d` / `--discovery`: List found aircraft models.

## For developers

No external dependencies required.

## Issues:

OC3 3.0.281 (May 2026) includes a damaged `ptp-converter.exe`. The only solution is to install an older OC3 version and back up `ptp-converter.exe` from `%appdata%\PMDG`.
Alternatively, you can extract a working `ptp-converter.exe` from other PTP projects that include it (for example, Doguer's "PTP and ZIP Converter").
