# 03 Three-platform comparison

[← Back to README](../README.md)

The same rig logic on three kinds of controller:

| Aspect | ESPHome (ESP32) | Trend IQ411 (BMS DDC) | IEC 61131-3 PLC |
|---|---|---|---|
| Programming model | YAML + C++ lambdas | Strategy modules in SET | LD / SFC / ST / FBD |
| Built-in BMS features | Few (built in HA) | Schedules, alarms, BMS networking | Built by the programmer |
| Interlocks | Lambdas / templates | Logic modules gating drivers | Ladder: the site-standard view |
| State machines | Hand-coded | Logic + latches | SFC: native |
| PID | ESPHome PID climate | Loop module | PID function block |
| Diagnostics | Logs, HA history | SET monitoring, controller displays | Online monitoring, forcing, trace |
| Change control | Git (YAML) | Strategy files | PLCopen XML in Git |
| Typical use | Prototyping, IoT | Commercial buildings (common in the UK) | Industrial and packaged plant |

**Results (fill in after build):** engineering hours, lines/blocks, test pass rates and observations per platform.
