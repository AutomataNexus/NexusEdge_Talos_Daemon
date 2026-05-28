# Changelog

## v1.0.0-Release — 2026-05-28

First public release of the NexusEdge Talos Daemon.

### Control Engine
- **44 HVAC control algorithms** — TMC family, PID, linear, on/off, cascade, lead/lag (pump/boiler/chiller), DX+CW AHU, DOAS+DX/changeover, electric heat, VAV/VAV-DX, natatorium, greenhouse, steambundle, zone reheat, fan coil (2-way/4-way), heat pump, resi boiler/furnace/heat pump, pool gas heater/heat pump, pressure booster, RTU, smart home, smart garden, commercial lighting, electrical monitor, water monitor (city/well), water-cooled chiller, cooling tower, VFD pump pack, cascade boiler, MPC advisory
- **OAT-reset setpoint** on steambundle + DOAS algorithms with `last_oat` tracking
- **Chiller OAT lockout** — correct direction (locks out when cold, not hot)
- **Startup timer fix** — all 17 algorithms with min-off timers now pre-load to 86400s so equipment starts on first demand
- **Input filter** — rate-of-change rejection + EMA damping with 5-tick auto-reset for sensor reconnects
- **Sensor FDD** — open/short circuit, drift, stuck sensor detection per controller
- **Safe state** — global safe-state flag persisted to AegisDB, released via UI or CLI
- **Hot-reload** — `site.toml` changes apply without restart, control state preserved

### Hardware I/O
- Polls Sequent Microsystems HATs (MegaBAS, MegaIND, UnivIn16, UOut16, RelInd16, RelInd8) every 1s
- Dedicated writer thread — no poller/writer I2C contention
- Per-board enable/disable + runtime connectivity gating

### CLI
- `nexusedge-talos-daemon release` — release safe state
- `nexusedge-talos-daemon engage` — engage safe state
- `nexusedge-talos-daemon status` — print control status JSON
- `nexusedge-talos-daemon help` — usage

### Embedded Mode
- `run_embedded()` returns `Arc<Engine>` for zero-overhead in-process calls from NexusEdge
- HTTP server on :6100 spawned in background for external tools/debugging
- No HTTP roundtrips between NexusEdge and Talos when embedded

### API
- `/control/status` — all equipment state
- `/control/safe-state` — get/set safe state
- `/control/outdoor-temp` — set site-level OAT
- `/control/site-mode` — set summer/winter mode
- `/control/equipment/:id/param` — tune algorithm parameters
- `/control/equipment/:id/override/:output` — manual overrides
- Full hardware read/write API on :6100

### CI/CD
- SLSA Provenance Level 3 attested releases
- Multi-arch: Pi 5 Bookworm aarch64, Pi 4 Bookworm aarch64, x86_64 Linux
- Docker multi-arch images on GHCR (`ghcr.io/automatanexus/talos-daemon`)
- Separate workflows for Pi 4 Bullseye aarch64 + armhf

### Security
- Updated rustls-webpki, rand, quinn-proto (resolved 6 Dependabot alerts)
- Zero dependency vulnerabilities at release time
