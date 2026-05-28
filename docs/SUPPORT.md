# Support

## Getting Help

### Community (Free Tier)

- **GitHub Issues** — [Report bugs and request features](https://github.com/AutomataNexus/NexusEdge-HailoCommunityEdition/issues)
- **Documentation** — [User Guide](https://nexusedgehailo.automatanexus.com/user-guide.html)
- **Algorithm Reference** — Available in-app on the Logic page (43 whitepapers)
- **Installation Guide** — [Install docs](https://nexusedgehailo.automatanexus.com/install.html)

### Developer ($29/mo — 1 controller)

Everything in Community, plus:
- **Email support** — devops@automatanexus.com (48-hour response)
- **On-device Sage AI assistant** — Ask questions about your equipment directly in the app
- **Remote access** — Cloudflare tunnel + Tailscale VPN

### Business ($99/mo — up to 5 controllers)

Everything in Developer, plus:
- **Priority email support** — 24-hour response
- **Remote diagnostics** — We can connect to your controller via Tailscale (with your permission)
- **Configuration review** — We'll review your site.toml and algorithm parameters
- **Multi-location dashboard** — View all controllers from the AN Console

### Enterprise ($299/mo — up to 25 controllers)

Everything in Business, plus:
- **Dedicated support channel**
- **Custom algorithm development** — We build algorithms for your specific equipment
- **On-site commissioning assistance** (travel expenses apply)
- **SLA** — 4-hour response for critical issues

### Enterprise+ (26-50 controllers) / Top Tier (50+)

Contact us for custom pricing: devops@automatanexus.com

## Before Reporting an Issue

1. **Check the version** — Run `nexusedge --version` or check Settings page
2. **Check the logs** — Logs page in the UI, or `journalctl -u nexusedge -n 100`
3. **Check hardware** — Verify I2C connections: `i2cdetect -y 1`
4. **Check Hailo** — Verify NPU: `hailortcli fw-control identify`
5. **Search existing issues** — Someone may have already reported it

## Useful Information to Include

- NexusEdge version
- Raspberry Pi model (Pi 4 / Pi 5)
- Hailo module (H8 / H10H / none)
- I/O boards (MegaBAS stack count, other boards)
- `site.toml` snippet (redact sensitive info)
- Relevant log output
- Screenshots of the issue

## Emergency: Equipment Not Responding

If the controller is not responding and equipment is in an unsafe state:

1. **Use physical manual overrides** — Every properly installed HVAC system has manual switches
2. **Power cycle the Pi** — Unplug and replug
3. **Safe state is default** — On boot, all outputs are OFF until the operator releases safe state

**NexusEdge is not a life-safety system.** All safety interlocks must be physically wired independently of software control.

---

AutomataNexus LLC — Wolcottville, Indiana 46795, USA
