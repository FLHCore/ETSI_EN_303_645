# Table B.1: Implementation of provisions for consumer IoT security

| Clause number and title | Reference | Status | Support | Detail |
| :--- | :--- | :--- | :--- | :--- |
| **5.0 Reporting implementation** | | | | |
| | Provision 5.0-1 | M | | |
| **5.1 No universal default passwords** | | | | |
| | Provision 5.1-1 | MF (a) | | |
| | Provision 5.1-2 | MF (b) | | |
| | Provision 5.1-2A | R | | |
| | Provision 5.1-3 | MF (c) | | |
| | Provision 5.1-4 | MF (d) | | |
| | Provision 5.1-5 | MCF (14, e) | | |
| **5.2 Implement a means to manage reports of vulnerabilities** | | | | |
| | Provision 5.2-1 | M | | |
| | Provision 5.2-2 | R | | |
| | Provision 5.2-3 | R | | |
| **5.3 Keep software updated** | | | | |
| | Provision 5.3-1 | RF (f) | | |
| | Provision 5.3-2 | MC (15) | | |
| | Provision 5.3-3 | MF (g) | | |
| | Provision 5.3-4A | RF (g) | | |
| | Provision 5.3-4B | RF (h) | | |
| | Provision 5.3-5 | RF (g) | | |
| | Provision 5.3-6A | RF (h) | | |
| | Provision 5.3-6B | RF (i) | | |
| | Provision 5.3-7 | MF (g) | | |
| | Provision 5.3-8 | MC (12) | | |
| | Provision 5.3-9 | RF (g) | | |
| | Provision 5.3-10 | MF (j) | | |
| | Provision 5.3-11 | RC (12) | | |
| | Provision 5.3-12 | RC (12) | | |
| | Provision 5.3-13 | M | | |
| | Provision 5.3-14 | RC (3) | | |
| | Provision 5.3-15A | RC (3) | | |
| | Provision 5.3-15B | RC (3) | | |
| | Provision 5.3-16 | M | | |
| **5.4 Securely store sensitive security parameters** | | | | |
| | Provision 5.4-1 | MF (k) | | |
| | Provision 5.4-2 | MF (l) | | |
| | Provision 5.4-3 | M | | |
| | Provision 5.4-4 | MF (m) | | |
| **5.5 Communicate securely** | | | | |
| | Provision 5.5-1 | M | | |
| | Provision 5.5-2 | R | | |
| | Provision 5.5-3 | R | | |
| | Provision 5.5-4 | R | | |
| | Provision 5.5-5 | MF (n) | | |
| | Provision 5.5-6 | RF (o) | | |
| | Provision 5.5-7 | MF (o) | | |
| | Provision 5.5-8 | MC (16) | | |
| **5.6 Minimize exposed attack surfaces** | | | | |
| | Provision 5.6-1 | MF (p) | | |
| | Provision 5.6-2 | M | | |
| | Provision 5.6-3 | R | | |
| | Provision 5.6-4A | MF (q) | | |
| | Provision 5.6-4B | RF (r) | | |
| | Provision 5.6-5 | R | | |
| | Provision 5.6-6 | R | | |
| | Provision 5.6-7 | R | | |
| | Provision 5.6-8 | R | | |
| | Provision 5.6-9 | R | | |
| **5.7 Ensure software integrity** | | | | |
| | Provision 5.7-1 | R | | |
| | Provision 5.7-2 | RF (s) | | |
| **5.8 Ensure that personal data is secure** | | | | |
| | Provision 5.8-1 | RF (t) | | |
| | Provision 5.8-2 | MF (u) | | |
| | Provision 5.8-3 | MF (v) | | |
| **5.9 Make systems resilient to outages** | | | | |
| | Provision 5.9-1 | R | | |
| | Provision 5.9-2 | R | | |
| | Provision 5.9-3 | R | | |
| **5.10 Examine system telemetry data** | | | | |
| | Provision 5.10-1 | RF (w) | | |
| **5.11 Make it easy for users to delete user data** | | | | |
| | Provision 5.11-1 | M | | |
| | Provision 5.11-2 | RF (x) | | |
| | Provision 5.11-3 | R | | |
| | Provision 5.11-4 | R | | |
| **5.12 Make installation and maintenance of devices easy** | | | | |
| | Provision 5.12-1 | R | | |
| | Provision 5.12-2 | R | | |
| | Provision 5.12-3 | R | | |
| **5.13 Validate input data** | | | | |
| | Provision 5.13-1A | M | | |
| | Provision 5.13-1B | M | | |
| **6 Data protection provisions for consumer IoT** | | | | |
| | Provision 6-1 | M | | |
| | Provision 6-2 | MF (y) | | |
| | Provision 6-3A | MF (y) | | |
| | Provision 6-3B | MF (y) | | |
| | Provision 6-4 | RF (w) | | |
| | Provision 6-5 | MF (w) | | |
| | Provision 6-6 | MF (z) | | |
| | Provision 6-7 | RF (aa) | | |
| | Provision 6-8 | RF (z) | | |

---

### Condition:
3) software components are not updateable;
12) an update mechanism is implemented;
14) the consumer IoT device has no resource constraint determined by the use case that prevents the implementation of a mechanism which makes successful brute-force attacks on authentication mechanisms via network interfaces impracticable;
15) the consumer IoT device has no resource constraint determined by the use case that prevents the implementation of an update mechanism;
16) existence of critical security parameters that relate to the consumer IoT device;

### Feature, capability or mechanism that needs to be present for the corresponding provision to apply:
- a) passwords can be used to authenticate users against the device or for machine-to-machine authentication;
- b) pre-installed unique per device passwords can be used to authenticate users against the device or for machine-to-machine authentication;
- c) cryptographic authentication mechanisms, including password based mechanisms, can be used to authenticate users against the consumer IoT device or for machine-to-machine authentication;
- d) authentication mechanisms can be used to authenticate users against the consumer IoT device;
- e) authentication mechanisms can be used for authenticating users or devices via network interfaces;
- f) software components that are not immutable due to security reasons;
- g) software components of the device can be updated;
- h) automatic software updates are supported;
- i) update notifications are provided when software updates are available;
- j) software updates can be delivered over a network interface;
- k) sensitive security parameters exist in persistent storage;
- l) hard-coded unique per device identities are used in the consumer IoT device for security purposes;
- m) critical security parameters are used for integrity or authenticity checks of software updates or for protection of communication with associated services;
- n) the consumer IoT device allows security-relevant changes in configuration via a network interface;
- o) critical security parameters used by the device can be communicated outside of the device;
- p) unused network or network accessible logical interfaces exist;
- q) debug interfaces exist on the device;
- r) debug interfaces that are physical ports exist on the device;
- s) secure boot or other mechanism to detect unauthorized changes to IoT device software are supported by the device;
- t) the consumer IoT device sends personal data to associated services;
- u) the consumer IoT device sends sensitive personal data to associated services;
- v) the consumer IoT device includes external sensing capabilities;
- w) telemetry data can be collected from consumer IoT devices and products;
- x) personal data can be stored by an associated service;
- y) the consumer IoT device processes personal data on the basis of consumers' consent;
- z) the consumer IoT device processes personal data;
- aa) capabilities to collect data from consumer IoT devices or to processed data on the consumer IoT device, whose purpose is solely to compute an aggregate result.