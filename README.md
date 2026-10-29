# PLC Re-implementation: The Rig's Logic in All Four IEC 61131-3 Languages (Design Stage)

**The training rig's sequences (interlocks, pump state machine, duty/standby rotation and PID loops) re-implemented on PLC platforms, deliberately using a different IEC 61131-3 language for each job: Ladder, Sequential Function Chart, Structured Text and Function Block Diagram. Then compared with the same logic on ESPHome and on a Trend IQ411 BMS controller, so the portfolio shows one set of logic on three kinds of controller.**

[![YouTube](https://img.shields.io/badge/YouTube-The%20Control%20Cabinet-red?logo=youtube)](https://www.youtube.com/channel/UC5Cupmz7vlfcodpCX7k8iuQ)
[![Portfolio](https://img.shields.io/badge/Portfolio-the--control--cabinet-24292f?logo=github)](https://github.com/the-control-cabinet/the-control-cabinet)
![Domain](https://img.shields.io/badge/BMS-PLC%20IEC%2061131--3-blue)
![Status](https://img.shields.io/badge/Status-Design%20stage-yellow)

> **The short version:**
> - **Ladder (LD):** pump permissives and interlocks, as they're drawn and read on site.
> - **SFC:** the pump state machine (OFF → START → PROVING → RUN → FAULT → LOCKOUT).
> - **Structured Text (ST):** duty/standby with run-hour balancing and failover.
> - **FBD:** the PID flow and thermal loops with the standard PID block and anti-windup.
> - **Platforms:** CODESYS (soft PLC + WebVisu HMI) and Siemens TIA Portal + PLCSIM; optionally a secondhand small PLC to drive the rig's real pumps.
> - **Comms:** reads the ESP32 Modbus server's register map; **tests** reuse the rig test records; **code** is exported as PLCopen XML into Git.

**Portfolio position:** Field/automation level · controller programming (portfolio #13). Same logic as: [duty/standby + interlocks](https://github.com/the-control-cabinet/din-rail-rig-duty-standby-interlocks) (#7/#9) · [PID rig](https://github.com/the-control-cabinet/pid-anti-hunt-control-rig) (#8). Compared with: [Trend IQ411](https://github.com/the-control-cabinet/trend-iq411-commissioning) (#12). Comms: [ESP32 Modbus server](https://github.com/the-control-cabinet/esp32-modbus-server-plant-points)

---

## Documents

| Doc | Contents |
|---|---|
| [01 Programs and languages](docs/01-programs.md) | What is written in which language, and why |
| [02 Platforms and testing](docs/02-platforms-and-testing.md) | CODESYS, TIA Portal, optional hardware; simulation and tests |
| [03 Three-platform comparison](docs/03-three-platform-comparison.md) | ESPHome vs Trend IQ411 vs IEC PLC |

## Roadmap
- [ ] Tag list and conventions
- [ ] CODESYS: interlocks (LD) and state machine (SFC) in simulation
- [ ] Duty/standby (ST) and PID loops (FBD)
- [ ] WebVisu HMI page and Modbus client to the ESP32
- [ ] TIA Portal + PLCSIM re-implementation
- [ ] Three-platform comparison completed with results

## Skills demonstrated (as built)
| Skill | Evidence |
|---|---|
| PLC programming | All four IEC 61131-3 languages, each used for its natural job |
| Structured design | Tag list, conventions, one program per function |
| Testing | Simulated I/O against a shared test record |
| Platform breadth | Same logic on ESPHome, Trend and PLC compared |
| Comms | Modbus client to a field device |

📺 [The Control Cabinet on YouTube](https://www.youtube.com/channel/UC5Cupmz7vlfcodpCX7k8iuQ)

*Built and documented by James · part of [The Control Cabinet BMS portfolio](https://github.com/the-control-cabinet/the-control-cabinet). MIT Licence.*
