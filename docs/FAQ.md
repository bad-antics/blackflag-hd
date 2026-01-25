# BlackFlag HD - Frequently Asked Questions

## General

### What is BlackFlag HD?
BlackFlag HD is a professional diagnostic and calibration suite for heavy-duty vehicles (Class 4-8). It supports J1939, J1708/J1587 protocols and 150+ commercial vehicles.

### How is it different from BlackFlag ECU?
- BlackFlag ECU: Light-duty vehicles (cars, light trucks, SUVs)
- BlackFlag HD: Heavy-duty vehicles (semi-trucks, buses, construction equipment)

### What vehicles are supported?
- Freightliner Cascadia, M2, 122SD
- Peterbilt 579, 389, 567
- Kenworth T680, W900, T880
- Volvo VNL, VNR, VHD
- Mack Anthem, Pinnacle, Granite
- International LT, RH, HV
- Western Star 4900, 5700
- Plus buses, RVs, and construction equipment

## Hardware

### What hardware do I need?
- RP1210 compliant diagnostic adapter (Nexiq, Noregon, Cojali)
- 9-pin or 6-pin Deutsch connector cables
- Laptop with Windows/Linux

### Can I use automotive OBD-II adapters?
No. Heavy-duty vehicles use different connectors and protocols. You need a commercial vehicle diagnostic adapter.

### What connector type does my truck use?
- Most Class 8 trucks: 9-pin Deutsch (Type II)
- Older vehicles: 6-pin Deutsch (Type I)
- Some European: OBDII with J1939-over-CAN

## Protocols

### What is J1939?
SAE J1939 is the standard communication protocol for heavy-duty vehicles. It uses 250kbps CAN with extended 29-bit identifiers and standardized Parameter Group Numbers (PGNs).

### What is J1708/J1587?
Legacy serial protocols for older heavy-duty vehicles. J1708 is the physical layer, J1587 is the data layer. Slower than J1939 but still found in older trucks.

### Does BlackFlag HD support CAN-FD?
Yes, we support CAN-FD for newer vehicles that use it.

## Features

### Can I force a DPF regen?
Yes, BlackFlag HD can initiate forced DPF regeneration on supported vehicles. This requires the vehicle to meet certain conditions (temperature, fuel level, etc.).

### Can I read/clear DEF faults?
Yes, we support full DEF/SCR system diagnostics including:
- DEF quality monitoring
- Injector diagnostics
- Tank level/temperature
- SCR efficiency

### Can I edit engine parameters?
BlackFlag HD provides calibration editing tools for authorized users. This is intended for fleet management and should only be used within legal limits.

## Fleet Management

### Can I connect to multiple vehicles?
Yes, BlackFlag HD supports fleet mode with multi-vehicle monitoring via telematics integration (Geotab, Samsara, etc.).

### What reporting features are available?
- DTC history and trends
- Fuel efficiency analysis
- Maintenance scheduling
- Driver performance metrics

## Legal & Compliance

### Is this legal to use?
For maintenance and diagnostics, yes. Emissions modifications (DPF deletes, DEF disabling) are illegal for on-highway use under EPA regulations and carry significant penalties.

### Can dealerships detect modifications?
Yes. ECU flash counters, DEF usage data, and diagnostic logs can reveal modifications during warranty claims or roadside inspections.

## Support

### Where can I get help?
- GitHub Issues: github.com/bad-antics/blackflag-hd/issues
- Discord: discord.gg/killers
- Documentation: See docs/ folder

---

**Disclaimer**: For authorized maintenance and off-highway use only. Follow all federal, state, and local regulations.
