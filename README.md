# mikrotik-hotspot-wireless-security.
Wireless security assessment and hardening of a MikroTik-based paid Wi-Fi hotspot
# MikroTik Hotspot Wireless Security Assessment

## Overview
This project documents a hands-on wireless security assessment and hardening of a MikroTik-based paid Wi-Fi hotspot deployed in a home/small-business environment.

The goal was to analyze wireless exposure, identify security risks, and apply defensive controls while maintaining hotspot functionality.

## Network Setup
- MikroTik router with hotspot (captive portal)
- Open SSID for paid access
- User authentication enforced via login page
- RouterOS with Atheros wireless interface

## Tools Used
- NetSpot (Inspector mode)
- MikroTik RouterOS (WinBox)
- Manual Wi-Fi signal mapping
- Android Ping Tools (testing client isolation)

## Assessment Performed
### Wireless Reconnaissance
- Scanned nearby Wi-Fi networks using NetSpot
- Identified signal strength, channels, vendors, and security types
- Observed strong signal near windows indicating possible external exposure

### Security Observations
- Open SSID intentionally configured for hotspot access
- Authentication enforced at application layer (captive portal)
- Potential risk of client-to-client attacks in public Wi-Fi environments

## Hardening Measures Implemented
- Added wireless interface to bridge
- Enabled client isolation using bridge port isolation (horizon)
- Enforced HTTPS-only captive portal login
- Blocked hotspot users from accessing router management IP
- Reduced transmit power to minimize Wi-Fi signal leakage

## Testing & Verification
- Tested client isolation using ping between connected devices
- Confirmed internet access remains functional
- Verified local network communication between users is blocked

## Results
- Hotspot users isolated from each other
- Router management protected from guest access
- Reduced wireless attack surface
- Improved overall hotspot security posture

## Ethical Notice
All testing and configuration were performed on infrastructure owned and authorized by the operator. No unauthorized networks or users were targeted.

## Author
Cybersecurity learner focusing on ethical hacking, wireless security, and network defense.
