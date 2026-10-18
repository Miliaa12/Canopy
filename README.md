# CANOPY

A small TUI app for modular eventdriven monitoring of farm equipment.

## Goals

- **Display, not control.** Canopy is read-only. It visualizes data (GPS,
  seed rate, harvest, etc.); it never sends commands back to equipment.
- **Retro, period-correct styling.** Amber/green phosphor CRT look, matching
  the era and interior of the tractor it's installed in.
- **Physical input, no touch.** Switching between dashboards happens via
  physical buttons matching the tractor's interior, not a touchscreen.
- **Event-driven, MQTT-only.** All data in (sensors) and input (button
  presses) arrives as MQTT messages. No direct hardware APIs or drivers
  inside Canopy itself — anything with sensors or switches publishes to a
  topic, and Canopy just renders whatever it receives.
- **Modular dashboards.** Individual dashboard views are loaded based on
  what's actually connected (i.e. which topics are active), so the same
  build adapts to different tractors/configurations.
- **Embedded deployment.** Runs kiosk-style, autostarted on boot alongside
  the tractor's own ignition — no interactive terminal session in the field.
  Configuration (broker address, calibration, etc.) is handled separately
  via config files or a web UI on the board, not through Canopy itself.
