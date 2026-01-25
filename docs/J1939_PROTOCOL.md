# J1939 Protocol Reference

## Overview

SAE J1939 is the standard CAN-based protocol for heavy-duty vehicles, operating at 250 kbps on a twisted-pair bus.

## CAN Identifier Structure (29-bit Extended)

```
| Priority | Reserved | Data Page | PDU Format | PDU Specific | Source Addr |
|  3 bits  |  1 bit   |   1 bit   |   8 bits   |    8 bits    |   8 bits    |
```

## Message Types

### PDU1 (Destination Specific)
- PF = 0-239 (0x00-0xEF)
- PS = Destination Address
- Point-to-point communication

### PDU2 (Broadcast)
- PF = 240-255 (0xF0-0xFF)
- PS = Group Extension
- All nodes receive

## Common Parameter Groups (PGN)

| PGN | Name | Description |
|----:|------|-------------|
| 61444 | EEC1 | Electronic Engine Controller 1 |
| 61443 | EEC2 | Electronic Engine Controller 2 |
| 65262 | ET1 | Engine Temperature 1 |
| 65263 | EFL/P1 | Engine Fluid Level/Pressure 1 |
| 65265 | CCVS | Cruise Control/Vehicle Speed |
| 65266 | LFE | Fuel Economy |
| 65269 | AI | Ambient Conditions |
| 65270 | IC1 | Inlet/Exhaust Conditions 1 |
| 65271 | VEP1 | Vehicle Electrical Power 1 |
| 65272 | TF | Transmission Fluids |
| 65276 | DASH | Dash Display |
| 65279 | WFI | Water in Fuel Indicator |
| 65132 | TCO1 | Tachograph |
| 65131 | EBC1 | Electronic Brake Controller 1 |

## Engine Parameters (EEC1 - PGN 61444)

| Byte | Parameter | Units |
|:----:|-----------|-------|
| 1-2 | Engine Torque | % |
| 3 | Driver Demand | % |
| 4 | Actual Torque | % |
| 5-6 | Engine Speed | RPM |
| 7 | Source Address | - |
| 8 | Starter Mode | - |

## Request Protocol (PGN 59904)

To request data from an ECU:
```
CAN ID: 0x18EA00FF (Request to all)
Data: [PGN_LSB, PGN_MID, PGN_MSB]
```

## Transport Protocol

### Connection Mode (TP.CM - PGN 60416)
Used for messages > 8 bytes

| Byte | Field |
|:----:|-------|
| 1 | Control Byte |
| 2-3 | Total Message Size |
| 4 | Total Packets |
| 5 | Max Packets |
| 6-8 | PGN Being Transferred |

### Data Transfer (TP.DT - PGN 60160)

| Byte | Field |
|:----:|-------|
| 1 | Sequence Number |
| 2-8 | Data |

## Address Claiming (PGN 60928)

NAME field structure (64 bits):
- Identity Number (21 bits)
- Manufacturer Code (11 bits)
- ECU Instance (3 bits)
- Function Instance (5 bits)
- Function (8 bits)
- Reserved (1 bit)
- Vehicle System (7 bits)
- Vehicle System Instance (4 bits)
- Industry Group (3 bits)
- Arbitrary Address Capable (1 bit)

## Common Source Addresses

| Address | Device |
|:-------:|--------|
| 0x00 | Engine #1 |
| 0x01 | Engine #2 |
| 0x03 | Transmission |
| 0x0B | Brakes (ABS) |
| 0x0F | Retarder (Engine) |
| 0x10 | Retarder (Driveline) |
| 0x11 | Cruise Control |
| 0x21 | Body Controller |
| 0x28 | Cab Climate |
| 0x31 | Instrument Cluster |
| 0xF9 | Off-board Tool |

## DTC Structure

| Byte | Field |
|:----:|-------|
| 1-2 | SPN (Suspect Parameter Number) |
| 3 | SPN MSB + FMI |
| 4 | Occurrence Count |
| 5 | SPN Conversion |

### FMI Codes (Failure Mode Identifier)

| FMI | Description |
|:---:|-------------|
| 0 | Data Valid Above Normal |
| 1 | Data Valid Below Normal |
| 2 | Data Erratic/Intermittent |
| 3 | Voltage Above Normal |
| 4 | Voltage Below Normal |
| 5 | Current Below Normal |
| 6 | Current Above Normal |
| 7 | Mechanical Not Responding |
| 8 | Abnormal Frequency |
| 9 | Abnormal Update Rate |
| 10 | Abnormal Rate of Change |
| 11 | Root Cause Unknown |
| 12 | Bad Device or Component |
| 13 | Out of Calibration |
| 14 | Special Instructions |
| 15 | Data Valid Above Normal (Least) |
| 16 | Data Valid Above Normal (Moderate) |
| 17 | Data Valid Below Normal (Least) |
| 18 | Data Valid Below Normal (Moderate) |
| 19 | Received Network Data Error |
| 31 | Condition Exists |

---

*BlackFlag HD - J1939 Protocol Reference v1.0*
