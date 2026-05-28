# Privacy Policy

## NexusEdge Community Edition

**Effective Date:** May 3, 2026
**Last Updated:** May 3, 2026

AutomataNexus LLC ("Company", "we", "us") respects your privacy. This Privacy Policy describes how NexusEdge Community Edition ("Software") handles data.

---

### 1. Data We Do NOT Collect

NexusEdge Community Edition is designed to operate locally on your controller. The Software does **not**:

- Transmit telemetry or usage analytics to AutomataNexus servers
- Upload sensor readings, equipment data, or control outputs to any cloud service
- Collect personally identifiable information (PII)
- Track user behavior within the application
- Use cookies, fingerprinting, or any tracking technology
- Share data with third-party analytics, advertising, or data broker services

### 2. Data Stored Locally

The Software stores the following data **on the controller's local storage only**:

| Data Type | Location | Purpose | Retention |
|---|---|---|---|
| Sensor readings | Local database | Historical trend data, alarm evaluation | Configurable (default 90 days) |
| Alarm history | Local database | Alarm tracking and acknowledgment | Configurable (default 90 days) |
| Audit trail | Local database | Change tracking for control mutations | Configurable (default 90 days) |
| Credentials | Encrypted local vault | SMTP passwords, API keys, weather keys | Until manually deleted |
| Site configuration | Local config file | Equipment and I/O mapping | Permanent |
| License key | Encrypted local vault | Pro subscription verification | Until subscription ends |

All local data is under your control. You may delete it at any time by removing the data directories.

### 3. Network Communications

The Software makes the following outbound network connections:

| Destination | Purpose | Data Sent | When |
|---|---|---|---|
| OpenWeatherMap API | Weather data for OAT (outdoor air temperature) | ZIP code, API key | Every 10 minutes (configurable) |
| Stripe API | Pro subscription verification | License key, controller ID | On startup + daily check |
| Stripe Checkout | Subscription purchase | Redirects to Stripe's hosted payment page | When user clicks "Upgrade to Pro" |

**No sensor data, equipment data, or control outputs are ever transmitted off the controller** unless you explicitly configure NexusBMS cloud reporting (a Pro feature).

### 4. Stripe Payment Data

When you subscribe to NexusEdge Pro, payment is processed by Stripe, Inc. We do not store credit card numbers, bank account details, or other payment instruments on the controller or on our servers. Stripe's privacy policy applies to payment processing: https://stripe.com/privacy

We receive from Stripe:
- Subscription status (active/canceled/past_due)
- Customer email (for support correspondence)
- Subscription tier and billing period

### 5. Pro Feature: NexusBMS Cloud Reporting

If you upgrade to NexusEdge Pro and enable cloud reporting, equipment metrics are transmitted to the cloud instance you configure. This is:
- **Opt-in only** — disabled by default
- **User-configured destination** — you specify the host, typically on your own private network
- **Equipment telemetry only** — sensor readings, valve positions, alarm states. No PII.

### 6. Hailo NPU Inference

Inference using the Hailo NPU runs entirely on the local controller. Model weights, input data, and inference results never leave the device. NexusRT communicates only with the Hailo PCIe hardware via kernel ioctl — no network communication.

### 7. nexus-serve LLM Inference

nexus-serve runs locally on the controller. Language model inference is performed on-device using locally stored model weights. No prompts, completions, or model data are transmitted to external servers.

### 8. Children's Privacy

NexusEdge is industrial HVAC control software. It is not directed at children under 13 and we do not knowingly collect data from children.

### 9. Data Security

- Credentials are encrypted at rest using AES-256-GCM
- Network communications use WireGuard-encrypted tunnels when configured
- No default passwords — all credentials are user-configured

### 10. Your Rights

Since NexusEdge stores data locally on hardware you control, you have full rights to:
- **Access** — read any data file on the controller
- **Delete** — remove data directories at any time
- **Export** — query the local database directly for your historical data
- **Restrict** — disable weather polling, cloud reporting, or any network feature

### 11. Changes to This Policy

We may update this Privacy Policy. Changes will be noted in the CHANGELOG and the "Last Updated" date above. Continued use of the Software after changes constitutes acceptance.

### 12. Contact

For privacy questions or concerns:

AutomataNexus LLC
Fort Wayne, Indiana, USA
Email: devops@automatanexus.com
Web: https://automatanexus.com

---

Copyright (c) 2026 AutomataNexus LLC. All rights reserved.
