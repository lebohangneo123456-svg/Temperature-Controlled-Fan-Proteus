# Safety, verification and limitations

- The Proteus schematic and screenshots are supplied as-is; no runtime simulation was independently performed.
- The supply is 12 V. Verify each component's manufacturer data sheet for supply and common-mode limitations before physical construction.
- An LM358 used as a comparator is not a precision dedicated comparator; output levels and switching behavior depend on supply, common-mode limits and loading.
- The visible comparator polarity appears to implement a **fan-on-cool** condition. Correct pin mapping if the intended function is **fan-on-hot**.
- The potentiometer's likely upper reference of about 0.429 V corresponds to 42.9 °C, not 50 °C; confirm with voltage probes.
- The TIP122 is a Darlington BJT. Verify its required base current, voltage drop, heat dissipation and motor stall-current rating before using a physical motor.
- Confirm the flyback diode's cathode is at +12 V and anode at the motor's switched low-side node.
- The red LED appears connected across the supply and should not be described as motor-status feedback without rewiring.
- Without hysteresis the fan may chatter at the trigger point. Add positive feedback or a controller with hysteresis if needed.
- Keep the circuit as an educational low-voltage experiment; it is not a certified thermostat, motor driver or safety controller.
