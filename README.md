# BlackFlag HD

**Professional Heavy Duty ECU Diagnostic & Tuning Suite**

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows" />
  <img src="https://img.shields.io/badge/.NET-8.0-purple?style=for-the-badge&logo=dotnet" />
  <img src="https://img.shields.io/badge/License-GPL--3.0-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Heavy%20Duty-Class%204--8-orange?style=for-the-badge" />
</p>

## Overview

BlackFlag HD is the heavy-duty counterpart to [BlackFlag ECU](https://github.com/bad-antics/blackflag-ecu), specifically designed for **Class 4-8 commercial vehicles**, including medium and heavy-duty trucks, buses, construction equipment, agricultural machinery, and fleet vehicles.

## Supported Vehicle Classes

| Class | GVWR | Examples |
|:-----:|------|----------|
| 4 | 14,001-16,000 lbs | Ford F-450, Ram 4500, Hino 155 |
| 5 | 16,001-19,500 lbs | Ford F-550, Ram 5500, Isuzu NPR |
| 6 | 19,501-26,000 lbs | Freightliner M2 106, Hino 268 |
| 7 | 26,001-33,000 lbs | Kenworth T370, Peterbilt 337 |
| 8 | 33,001+ lbs | Kenworth T680, Peterbilt 579, Volvo VNL |

## Features

### ECU Communication
- **J1939 CAN** - SAE J1939 protocol for HD diesel engines
- **J1708/J1587** - Legacy serial protocol support
- **J1850 VPW** - GM medium duty
- **ISO 15765** - OBD-II compliant systems
- **Proprietary Protocols** - Cummins, Detroit, PACCAR, Volvo

### Diagnostic Capabilities
- Read/Clear DTCs (Active & Inactive)
- Live data streaming (250+ parameters)
- Freeze frame data
- Component testing
- Injector coding
- DPF regeneration commands
- SCR/DEF system monitoring
- Aftertreatment diagnostics

### Tuning Functions
- ECM calibration read/write
- Speed limiter adjustment
- Idle parameter modification
- PTO configuration
- Governor settings
- Torque curve editing
- Emissions system parameters (off-road/competition only)

### Fleet Management
- VIN decoding
- Odometer verification
- Trip data export
- Maintenance scheduling
- Multi-vehicle scanning

## Supported Manufacturers

### Engines
| Manufacturer | Engine Series | Years |
|--------------|---------------|-------|
| Cummins | ISB, ISC, ISL, ISX, X15 | 2007-2024 |
| Detroit Diesel | DD13, DD15, DD16, Series 60 | 2007-2024 |
| PACCAR | MX-11, MX-13, PX-7, PX-9 | 2010-2024 |
| Navistar | MaxxForce 7, 9, 10, 11, 13, A26 | 2007-2024 |
| Volvo | D11, D13, D16 | 2007-2024 |
| Mack | MP7, MP8 | 2007-2024 |
| CAT | C7, C9, C13, C15, C18 | 2004-2017 |
| Hino | J05E, J08E, A09C | 2010-2024 |
| Isuzu | 4HK1, 6HK1, 6WG1 | 2008-2024 |

### Transmissions
| Manufacturer | Models |
|--------------|--------|
| Eaton Fuller | Automated & Manual |
| Allison | 1000-4700 Series |
| ZF | AS Tronic, TraXon |
| Volvo | I-Shift |
| Detroit | DT12 |

### Trucks & Chassis
- Freightliner (Cascadia, M2, 122SD)
- Kenworth (T680, T880, W990)
- Peterbilt (579, 389, 567)
- Volvo (VNL, VNR, VHD)
- Mack (Anthem, Pinnacle, Granite)
- International (LT, HX, MV)
- Western Star (4900, 5700, 49X)

### Buses
- Thomas Built
- Blue Bird
- IC Bus
- Gillig
- New Flyer

### Construction & Agriculture
- Caterpillar
- John Deere
- Case IH
- Komatsu
- Hitachi
- Volvo CE

## Hardware Requirements

### Recommended J2534 Devices
- Nexiq USB-Link 2/3
- Noregon DLA+ 2.0
- INLINE 7 (Cummins)
- Dearborn DPA5
- DrewTech CarDAQ-Plus3

### Minimum PC Specs
- Windows 10/11 64-bit
- Intel i5 / AMD Ryzen 5
- 8GB RAM
- USB 3.0 port

## Installation

```powershell
# Download latest release
Invoke-WebRequest -Uri "https://github.com/bad-antics/blackflag-hd/releases/latest" -OutFile "BlackFlagHD-Setup.exe"

# Run installer
.\BlackFlagHD-Setup.exe
```

## Quick Start

1. Connect J2534 device to vehicle's 9-pin or 6-pin diagnostic port
2. Launch BlackFlag HD
3. Select vehicle/engine type
4. Auto-detect ECMs on the network
5. Begin diagnostics or calibration

## Documentation

- [J1939 Protocol Guide](docs/J1939_PROTOCOL.md)
- [Connector Pinouts](docs/CONNECTORS.md)
- [Vehicle Database](data/vehicles.json)
- [Fault Code Reference](docs/DTC_REFERENCE.md)
- [Calibration Guide](docs/CALIBRATION.md)

## Legal Disclaimer

This software is intended for **professional use only** by qualified technicians. Modifications to emissions control systems are prohibited on public roads in most jurisdictions. Use for competition, off-road, or agricultural applications where legally permitted.

## Related Projects

- [BlackFlag ECU](https://github.com/bad-antics/blackflag-ecu) - Light duty automotive tuning
- [NullSec Tools](https://github.com/bad-antics/nullsec-tools) - Security research utilities

## License

GPL-3.0 - See [LICENSE](LICENSE) for details.

---

**BlackFlag HD** - *Professional Heavy Duty Diagnostics*

## 🚛 Heavy Duty Coverage

### Class 4-5 (14,001-19,500 lbs)
- **Ford** - F-450, F-550
- **Ram** - 4500, 5500
- **GM** - 4500HD, 5500HD

### Class 6-7 (19,501-33,000 lbs)
- **Freightliner** - M2 106, M2 112
- **Kenworth** - T270, T370
- **Peterbilt** - 325, 337, 348
- **International** - MV, HV Series

### Class 8 (33,001+ lbs)
- **Freightliner** - Cascadia, Columbia
- **Kenworth** - W990, T680, T880
- **Peterbilt** - 389, 579, 567
- **Volvo** - VNL, VNR
- **Mack** - Anthem, Pinnacle

## 🔧 Engine Support

| Engine | Years | Features |
|--------|-------|----------|
| Cummins ISX15 | 2010-2025 | DPF/EGR/DEF delete, power tunes |
| Detroit DD13/DD15 | 2014-2025 | Emissions, fuel maps, speed |
| Paccar MX-13 | 2013-2025 | Performance, emissions |
| Volvo D13 | 2014-2025 | Full calibration support |


<!-- Updated: 2026-01-25 13:42:30 -->

<!-- Updated: 2026-01-25 13:52:20 -->

<!-- Updated: 2026-01-25 14:00:01 -->

<!-- Updated: 2026-01-28 18:00:14 -->
