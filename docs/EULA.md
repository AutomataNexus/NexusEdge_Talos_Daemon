# End-User License Agreement (EULA)

## NexusEdge Hailo Community Edition

**Version:** 2.0
**Effective Date:** May 16, 2026
**Licensor:** AutomataNexus LLC, Wolcottville, Indiana, USA

---

This End-User License Agreement ("EULA") is a legal agreement between you ("End User", "you", or "your") and AutomataNexus LLC ("Licensor", "we", "us", or "our") for the use of NexusEdge Hailo Community Edition, its binary components, AI models, control algorithms, and all associated documentation and materials (collectively, the "Licensed Software").

**BY DOWNLOADING, INSTALLING, COPYING, OR OTHERWISE USING THE LICENSED SOFTWARE, YOU ACKNOWLEDGE THAT YOU HAVE READ, UNDERSTOOD, AND AGREE TO BE BOUND BY THE TERMS OF THIS EULA. IF YOU DO NOT AGREE, DO NOT DOWNLOAD, INSTALL, OR USE THE LICENSED SOFTWARE.**

---

### 1. DEFINITIONS

**"Open Source Components"** — Source code explicitly distributed under the Apache License 2.0 and identified as open source in the repository. As of Version 2.0, this includes the Leptos frontend UI framework, Tauri shell bridge, site configuration parsers, and shared type definitions. The specific files covered are identified by an Apache-2.0 header or listed in the NOTICE file.

**"Proprietary Binary Components"** — All pre-compiled binary components distributed without source code, including but not limited to:
- The NexusEdge single binary (Talos control engine, AegisDB, NexusVault, web server, inference engine)
- NexusRT (Hailo NPU inference via libhailort FFI)
- All compiled control algorithms (42 algorithms as of v2.0, including but not limited to TMC, PID, cascade, lead/lag, zone reheat, and all equipment-type-specific algorithms)
- The Sobek Neural Network Suite (Nehebkau LSTM models, Medjed GRU models, all .axonml weight files, all .hef compiled Hailo execution files)
- Sage LLM (on-device language model, weights, harness, and inference runtime)
- nexus-serve (model inference server)
- The AxonML on-controller training pipeline

**"Pro Features"** — Functionality gated behind a paid subscription tier (Developer, Business, or Enterprise), including but not limited to:
- Email notifications (FerrumMail integration)
- SMS notifications (NexusPulse/Telnyx integration)
- BACnet/IP and Modbus communication protocols
- NexusOracle/Sage AI assistant
- Remote fleet management via Tailscale
- Multi-location dashboard (Business/Enterprise)
- Team management and role-based access (Business/Enterprise)
- Priority support (Enterprise)
- Custom algorithm development (Enterprise)

**"Community Features"** — Functionality available without a paid subscription, including:
- All 42 deterministic control algorithms
- On-device Sobek AI inference (anomaly detection + predictive maintenance)
- AegisDB time-series storage
- NexusVault credential management
- NexusShield security middleware
- Single-controller operation
- Local UI dashboard

**"Controller"** — A single Raspberry Pi 5 (or compatible single-board computer) running one instance of the Licensed Software.

**"Subscription Tier"** — The service level purchased by the End User: Community (free, 1 controller), Developer ($29/mo, 1 controller), Business ($99/mo, up to 5 controllers), Enterprise ($299/mo, up to 25 controllers), Enterprise+ (26-50 controllers, contact us), or Top Tier (50+ controllers, contact us). Feature availability is determined by the active Subscription Tier.

**"AI Models"** — The Sobek Neural Network Suite consisting of 48 pre-trained models (24 Nehebkau LSTM + 24 Medjed GRU) compiled for Hailo-8 and Hailo-10H silicon, plus any Sage LLM model weights distributed with or deployed to the Licensed Software.

**"Control Algorithms"** — The 42 deterministic HVAC control algorithms embedded in the Licensed Software binary, including all parameter schemas, FDD (Fault Detection and Diagnostics) logic, safety interlocks, and setpoint computation.

---

### 2. LICENSE GRANT

**2.1 Open Source Components.** The Open Source Components are licensed under the Apache License 2.0. You may use, modify, and redistribute them in accordance with that license. A copy of the Apache License 2.0 is provided in the LICENSE-APACHE file.

**2.2 Proprietary Binary Components.** Subject to the terms of this EULA, the Licensor grants you a limited, non-exclusive, non-transferable, revocable license to:
- Install and use the Proprietary Binary Components on Controllers you own or operate;
- Use the embedded Control Algorithms to manage HVAC equipment under your direct physical control;
- Use the embedded AI Models for on-device inference on Controllers you own or operate;
- Use the on-controller training pipeline to fine-tune AI Models using your own operational data.

**2.3 Subscription Tier Features.** Pro Features are licensed only to End Users with an active, valid Subscription Tier that includes the specific feature. Accessing, enabling, bypassing, or circumventing feature gating for any Pro Feature without the corresponding active subscription constitutes a material breach of this EULA.

**2.4 Controller Limits.** The number of Controllers you may operate under a single license is determined by your Subscription Tier:
- Community: 1 Controller
- Developer: 1 Controller
- Business: up to 5 Controllers
- Enterprise: up to 25 Controllers
- Enterprise+: up to 50 Controllers (contact us)
- Top Tier: 50+ Controllers (contact us for custom pricing)

Operating Controllers in excess of your Subscription Tier limit constitutes a breach of this EULA.

**2.5 AI Model License.** The AI Models are licensed for inference and on-controller fine-tuning only. You may NOT:
- Extract, export, convert, or redistribute AI Model weights in any format;
- Use AI Model weights to train, distill, or initialize other models;
- Deploy AI Model weights on hardware or in environments not controlled by the Licensed Software;
- Reverse-engineer model architectures or training procedures from the distributed weights.

**2.6 Control Algorithm License.** The Control Algorithms are embedded in the Proprietary Binary Components and licensed for on-controller execution only. You may NOT:
- Extract, decompile, or isolate individual algorithm implementations;
- Reimplement algorithms based on observation of their input/output behavior for commercial purposes;
- Use algorithm whitepapers (distributed as documentation) to build competing implementations.

---

### 3. RESTRICTIONS

You shall NOT, and shall not permit any third party to:

**(a) Reverse Engineering.** Reverse engineer, disassemble, decompile, or otherwise attempt to derive the source code, algorithms, data structures, or internal architecture of any Proprietary Binary Component, AI Model, or Control Algorithm.

**(b) Circumvention.** Remove, disable, bypass, or circumvent any technological protection measure, including but not limited to anti-tamper checks, license verification, feature gating, subscription tier enforcement, string obfuscation, binary hardening, or ed25519 signature verification.

**(c) Modification.** Modify, patch, instrument, or alter any Proprietary Binary Component, including but not limited to attaching debuggers, injecting code, altering executable segments, hooking system calls, or intercepting internal API communications between components.

**(d) Extraction.** Extract, isolate, or use NexusRT, nexus-serve, Sage, the Talos control engine, AegisDB, or any individual Proprietary Binary Component independently of the Licensed Software without a separate commercial license from the Licensor.

**(e) Competition.** Use the Licensed Software, its documentation, its algorithm whitepapers, its AI Model architectures, or any knowledge derived from its operation to develop, train, or improve a competing HVAC control platform, building automation system, or edge AI inference product.

**(f) Redistribution.** Transfer, sublicense, rent, lease, sell, lend, or make available the Licensed Software or any Proprietary Binary Component to any third party, except as expressly permitted for Controllers under your management.

**(g) Model Redistribution.** Extract, copy, upload, or redistribute any AI Model weights (.axonml files, .hef files, .gguf files) outside of Controllers licensed under this EULA.

**(h) Credential Access.** Attempt to extract, intercept, or exfiltrate any credentials, API keys, SMTP configurations, Stripe keys, signing keys, or vault contents embedded in or managed by the Licensed Software.

**(i) AI Safety Bypass.** Attempt to manipulate, jailbreak, prompt-inject, or otherwise cause the Sage LLM or any AI component to bypass its safety guardrails, access restricted tools, modify control outputs, or perform actions outside its designed operational scope.

**(j) Notices.** Remove, alter, obscure, or deface any proprietary notices, labels, marks, watermarks, or attribution in any component of the Licensed Software.

---

### 4. INTELLECTUAL PROPERTY

**4.1 Ownership.** The Licensed Software and all copies, modifications, and derivative works thereof are proprietary to the Licensor. All right, title, and interest in and to the Licensed Software, including all intellectual property rights therein, are and shall remain with the Licensor.

**4.2 Patents.** The Control Algorithms, AI Model architectures, thermal momentum control (TMC) methodology, and NexusEdge system architecture are the subject of pending patent applications. Use of the Licensed Software does not grant any patent license except as necessary to use the Licensed Software as expressly authorized by this EULA.

**4.3 Trademarks.** "NexusEdge", "AutomataNexus", "Talos", "AegisDB", "NexusVault", "NexusShield", "NexusCompress", "AxonML", "Sobek", "Nehebkau", "Medjed", "Sage", "NexusRT", "FerrumMail", "NexusPulse", "TMC" (Thermal Momentum Control), and associated logos are trademarks of AutomataNexus LLC. This EULA does not grant any trademark license.

**4.4 ORCID.** All algorithms, AI models, and system architecture are attributed to Andrew Jewell Sr. (ORCID: 0009-0005-2158-7060).

---

### 5. DATA AND PRIVACY

**5.1 Local Processing.** The Community Edition performs all data processing locally on the Controller. No sensor data, control outputs, or operational telemetry is transmitted to AutomataNexus LLC or any third party by default.

**5.2 Optional Services.** Pro subscription features (email, SMS, remote access) transmit data through AutomataNexus LLC proxy services as described in the Privacy Policy. These services are opt-in and require explicit configuration.

**5.3 Training Data.** Data used for on-controller AI model retraining remains on the Controller and is not transmitted externally. Trained model weights remain on the Controller.

**5.4 Telemetry.** The Licensed Software does not include telemetry, analytics, or phone-home functionality. License validation occurs only during initial activation and subscription verification.

---

### 6. SAFETY DISCLAIMER

**THE LICENSED SOFTWARE CONTROLS HVAC EQUIPMENT THAT CAN DIRECTLY AFFECT HUMAN COMFORT, HEALTH, AND SAFETY, INCLUDING HEATING SYSTEMS CAPABLE OF CAUSING FIRES OR BURNS, COOLING SYSTEMS CAPABLE OF CAUSING FREEZE DAMAGE, AND PRESSURIZED SYSTEMS CAPABLE OF CAUSING PHYSICAL INJURY.**

**THE END USER IS SOLELY AND ENTIRELY RESPONSIBLE FOR:**

(a) Ensuring all safety interlocks, freeze protection, high-limit shutdowns, pressure relief valves, and emergency stops are physically wired independently of software control and tested regularly;

(b) Validating all algorithm behavior, setpoints, and control outputs in their specific installation before relying on automated control for any duration;

(c) Compliance with all applicable building codes, mechanical codes, electrical codes, fire codes, plumbing codes, and safety standards in their jurisdiction;

(d) Maintaining physical access to manual overrides for all controlled equipment at all times;

(e) Ensuring that no AI component (Sobek, Sage, or any model) has been configured to directly control equipment outputs — AI components are designed for observation and prediction only, with a strict air gap from control outputs;

(f) Regular inspection and maintenance of all controlled equipment independently of software diagnostics.

**THE LICENSOR MAKES NO WARRANTY THAT THE SOFTWARE WILL OPERATE WITHOUT ERROR, THAT CONTROL OUTPUTS WILL ALWAYS BE APPROPRIATE, THAT AI PREDICTIONS WILL BE ACCURATE, OR THAT SAFETY INTERLOCKS WILL FUNCTION CORRECTLY IN ALL CIRCUMSTANCES.**

---

### 7. NO WARRANTY

THE LICENSED SOFTWARE IS PROVIDED "AS IS" AND "AS AVAILABLE" WITHOUT WARRANTY OF ANY KIND, EXPRESS, IMPLIED, OR STATUTORY. THE LICENSOR SPECIFICALLY DISCLAIMS ALL WARRANTIES, INCLUDING BUT NOT LIMITED TO WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, TITLE, NON-INFRINGEMENT, ACCURACY, RELIABILITY, AVAILABILITY, AND FREEDOM FROM COMPUTER VIRUSES OR OTHER HARMFUL CODE.

THE LICENSOR DOES NOT WARRANT THAT (A) THE SOFTWARE WILL MEET YOUR REQUIREMENTS; (B) THE SOFTWARE WILL BE UNINTERRUPTED, TIMELY, SECURE, OR ERROR-FREE; (C) THE RESULTS OBTAINED FROM USE OF THE SOFTWARE WILL BE ACCURATE OR RELIABLE; OR (D) ANY ERRORS IN THE SOFTWARE WILL BE CORRECTED.

---

### 8. LIMITATION OF LIABILITY

IN NO EVENT WILL THE LICENSOR, ITS OFFICERS, DIRECTORS, EMPLOYEES, AGENTS, OR AFFILIATES BE LIABLE FOR ANY INDIRECT, INCIDENTAL, SPECIAL, CONSEQUENTIAL, EXEMPLARY, OR PUNITIVE DAMAGES ARISING OUT OF OR RELATED TO THIS EULA OR THE USE OF THE LICENSED SOFTWARE, INCLUDING BUT NOT LIMITED TO DAMAGES FOR LOSS OF PROFITS, LOSS OF DATA, EQUIPMENT DAMAGE, PROPERTY DAMAGE, PERSONAL INJURY, BUSINESS INTERRUPTION, OR LOSS OF GOODWILL, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

THE LICENSOR'S TOTAL AGGREGATE LIABILITY UNDER THIS EULA SHALL NOT EXCEED THE GREATER OF (A) THE AMOUNTS ACTUALLY PAID BY THE END USER FOR THE LICENSED SOFTWARE IN THE TWELVE (12) MONTHS IMMEDIATELY PRECEDING THE EVENT GIVING RISE TO THE CLAIM, OR (B) ONE HUNDRED UNITED STATES DOLLARS (USD $100.00).

THE LIMITATIONS IN THIS SECTION APPLY REGARDLESS OF THE THEORY OF LIABILITY, WHETHER BASED ON CONTRACT, TORT (INCLUDING NEGLIGENCE), STRICT LIABILITY, OR ANY OTHER LEGAL THEORY.

---

### 9. INDEMNIFICATION

You agree to indemnify, defend, and hold harmless the Licensor and its officers, directors, employees, agents, and affiliates from and against any and all claims, liabilities, damages, losses, costs, and expenses (including reasonable attorneys' fees) arising out of or related to (a) your use of the Licensed Software; (b) your breach of this EULA; (c) any damage to persons or property resulting from HVAC equipment controlled by the Licensed Software under your operation; or (d) your violation of any applicable law or regulation.

---

### 10. SUBSCRIPTION AND PAYMENT

**10.1 Free Tier.** The Community tier is provided at no cost and includes Community Features only. The Licensor reserves the right to modify Community Features at any time.

**10.2 Paid Tiers.** Paid subscriptions (Developer, Business, Enterprise) are billed monthly or annually through Stripe. Subscription terms, pricing, and feature availability are as published at https://nexusedgehailo.automatanexus.com at the time of purchase.

**10.3 Feature Changes.** The Licensor may add features to any tier at any time. The Licensor will not remove features from a paid tier during an active billing period without 30 days' written notice.

**10.4 Cancellation.** You may cancel your subscription at any time. Pro Features will remain active until the end of the current billing period. No refunds are provided for partial billing periods.

---

### 11. TERMINATION

**11.1 Automatic Termination.** This EULA terminates automatically and immediately if you breach any provision, including but not limited to reverse engineering, circumvention, or exceeding Controller limits.

**11.2 Termination by Licensor.** The Licensor may terminate this EULA at any time for any reason with 30 days' written notice to your registered email address.

**11.3 Effect of Termination.** Upon termination, you must immediately: (a) cease all use of the Licensed Software; (b) uninstall the Licensed Software from all Controllers; (c) destroy all copies of Proprietary Binary Components and AI Models in your possession; (d) certify in writing that you have complied with the foregoing.

**11.4 Survival.** Sections 3 (Restrictions), 4 (Intellectual Property), 6 (Safety Disclaimer), 7 (No Warranty), 8 (Limitation of Liability), 9 (Indemnification), and this Section 11.4 survive termination.

---

### 12. EXPORT COMPLIANCE

You agree to comply with all applicable export and re-export control laws and regulations, including the Export Administration Regulations ("EAR") maintained by the U.S. Department of Commerce and sanctions programs maintained by the Office of Foreign Assets Control ("OFAC") of the U.S. Department of the Treasury. You represent and warrant that you are not located in, under the control of, or a national or resident of any country to which the United States has embargoed goods or services.

---

### 13. GOVERNING LAW AND DISPUTE RESOLUTION

**13.1 Governing Law.** This EULA is governed by and construed in accordance with the laws of the State of Indiana, United States, without regard to its conflicts of law provisions.

**13.2 Jurisdiction.** Any legal action or proceeding arising under this EULA shall be brought exclusively in the state or federal courts located in LaGrange County, Indiana, and you hereby consent to the personal jurisdiction and venue of such courts.

**13.3 Injunctive Relief.** You acknowledge that any breach of Sections 3, 4, or 5 of this EULA may cause irreparable harm to the Licensor for which monetary damages would be insufficient. The Licensor shall be entitled to seek injunctive or other equitable relief in addition to any other remedies available at law or in equity.

---

### 14. MISCELLANEOUS

**14.1 Entire Agreement.** This EULA constitutes the entire agreement between you and the Licensor regarding the Licensed Software and supersedes all prior and contemporaneous agreements, proposals, and representations.

**14.2 Severability.** If any provision of this EULA is found to be unenforceable or invalid, that provision shall be limited or eliminated to the minimum extent necessary so that the EULA shall otherwise remain in full force and effect.

**14.3 Waiver.** The failure of the Licensor to enforce any right or provision of this EULA shall not constitute a waiver of such right or provision.

**14.4 Assignment.** You may not assign or transfer this EULA without the Licensor's prior written consent. The Licensor may assign this EULA without restriction.

**14.5 Amendments.** The Licensor reserves the right to modify this EULA at any time. Material changes will be communicated via the registered email address or through the Licensed Software's update mechanism. Continued use of the Licensed Software after notification constitutes acceptance of the modified terms.

**14.6 Force Majeure.** The Licensor shall not be liable for any failure or delay in performance due to circumstances beyond its reasonable control.

---

### 15. CONTACT

AutomataNexus LLC
Wolcottville, Indiana 46795, USA
andrew.jewellsr@automatanexus.com
https://automatanexus.com
ORCID: 0009-0005-2158-7060

---

Copyright © 2026 AutomataNexus LLC. All rights reserved.

NexusEdge, AutomataNexus, Talos, AegisDB, NexusVault, NexusShield, NexusCompress, AxonML, Sobek, Nehebkau, Medjed, Sage, NexusRT, FerrumMail, NexusPulse, and TMC are trademarks of AutomataNexus LLC.
