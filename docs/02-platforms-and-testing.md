# 02 Platforms and testing

[← Back to README](../README.md)

| Platform | Use | Notes |
|---|---|---|
| **CODESYS** | All four languages, soft PLC, WebVisu HMI, Modbus client | Development is free; check the current soft-PLC runtime/demo limits ⟨verify⟩ |
| **Siemens TIA Portal + PLCSIM** | Re-implement the interlocks and state machine in the Siemens environment | Trial licence ⟨verify the current terms⟩ |
| **Optional hardware** | A secondhand Siemens LOGO! 8 or small S7-1200 driving the rig's pumps | Small spend; real I/O instead of simulation |

**Testing:** simulated or forced I/O, then the **same test record** as the rig ([T1-T5](https://github.com/the-control-cabinet/din-rail-rig-duty-standby-interlocks/blob/main/data/test-record.csv)), so results compare directly across platforms.

**Version control:** PLCopen XML exports committed per change; screenshots of each network/step for readers without the software.
