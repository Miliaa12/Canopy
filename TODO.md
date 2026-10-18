# TODO

## Now

- [ ] Design App event enum: all events (sensor data, button presses) arrive
      as Mqtt(topic, payload); no direct keyboard handling of domain logic
- [ ] Add mqtt integration

## Next

- [ ] Dashboard-switch input via physical buttons published over MQTT
- [ ] Modular dashboard loading: enable/show a dashboard based on which
      topics are actively publishing, not a hardcoded list
- [ ] Seed rate display panel
- [ ] GPS module: parse NMEA sentences into a `Fix` struct

## Later / Ideas

- [ ] Harvest data tracking
- [ ] Retro color theme (amber/green phosphor look)
- [ ] systemd service unit: autostart on boot, restart on crash
- [ ] MQTT disconnect/reconnect handling (stale-data vs. "no signal" state)
- [ ] Config file support (broker address, calibration values, implement
      widths, etc.) — handled outside Canopy per README goals

## Done

- [x] Project scaffold (lib/main split, App + event loop)
- [x] CI, Dependabot, cargo-audit workflows
