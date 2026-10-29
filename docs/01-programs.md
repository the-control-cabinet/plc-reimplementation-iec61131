# 01 Programs and languages

[← Back to README](../README.md)

| Program | Language | Content | Source sequence |
|---|---|---|---|
| `Interlocks` | **LD** | Low-level permissive, hand/off/auto, lockout latch with reset, pilot lights | [#9 interlocks](https://github.com/the-control-cabinet/din-rail-rig-duty-standby-interlocks/blob/main/docs/03-interlocks-state-machine.md) |
| `PumpStateMachine` | **SFC** | Steps OFF/START/PROVING/RUN/FAULT/LOCKOUT; transitions on demand, proof, timers | #9 state diagram |
| `DutyStandby` | **ST** | Lead selection by run hours, weekly rotation, failover, idle-pump exercise | [#7 duty/standby](https://github.com/the-control-cabinet/din-rail-rig-duty-standby-interlocks/blob/main/docs/02-duty-standby.md) |
| `FlowLoop`, `ThermalLoop` | **FBD** | Standard PID block, output limits, anti-windup, manual/auto bumpless transfer | [#8 PID rig](https://github.com/the-control-cabinet/pid-anti-hunt-control-rig) |
| `Alarms` | ST / FBD | Latching, acknowledgement, priority per the alarm strategy | [Alarm strategy](https://github.com/the-control-cabinet/alarm-and-trend-strategy) |
| `ModbusIO` | Configuration | Modbus client reading the ESP32 register map | [Modbus server](https://github.com/the-control-cabinet/esp32-modbus-server-plant-points) |

**Conventions:** a tag list (I/O, internal, HMI) with naming rules; one program per function; comments on every network/step; constants for all setpoints and timers.
