# Proteus test plan

**Status:** Test cases defined; no independent simulation run performed.

| Test | Procedure | Required observation | Verified |
|---|---|---|---|
| Supply | Probe +12 V and GND | Rails correct | No |
| LM35 | Set temperature to 20 °C | VOUT near 0.200 V | No |
| LM35 | Set temperature to 35 °C | VOUT near 0.350 V | No |
| LM35 | Set temperature to 50 °C | VOUT near 0.500 V | No |
| Threshold | Vary potentiometer, measure wiper | Adjustable reference value | No |
| Polarity | Set temp below reference-equivalent temperature | Record LM358 pin-1 state | No |
| Polarity | Set temp above reference-equivalent temperature | Record LM358 pin-1 state | No |
| Driver | Monitor TIP122 base, collector and motor current | Expected switching/drive | No |
| Flyback | Turn motor off and inspect voltage transient | Suppression is effective | No |
| Indicators | Toggle fan state | Verify red LED tracks supply or motor as intended | No |
| Hysteresis | Sweep slowly around threshold | Assess output chatter | No |

## Recommended data table

| Temperature (°C) | LM35 VOUT (V) | Reference (V) | LM358 output (V) | Motor current (A) | Motor state |
|---:|---:|---:|---:|---:|---|
| 20 | | | | | |
| 30 | | | | | |
| 40 | | | | | |
| 50 | | | | | |
| 60 | | | | | |

**Note:** Expected voltages from LM35 are *nominal* rather than measured results. The screenshot showing 50.0 °C and around 0.502 V is consistent with this transfer characteristic, but this single point does not establish full-system behavior.
