# Home Lab - Enterprice Network (Day 1)
## Goal
Simulate a small enterprise network with Windows Server and Linux services

## Architecture
- Hypev-V Internal Switch
- DC01 (Windows Server) - 10.10.10.10
- LINUX01 (Ubuntu Server) - 10.10.10.20

## Implemented
- Created Hyper-V virtual switch.
- Deployed 2 virtual machines.
- Configured static IP addressing.
- Verified network connectivity (ping between hosts).

## Tools
- Hyper-V.
- Windows Server.
- Ubuntu Server.

## Network Design

Windows Server (DC01) was configured with two network adapters:

- Adapter 1: Internal Virtual Switch (CORP-SWITCH)
  - Used for isolated lab communication between servers.

- Adapter 2: External Virtual Switch.
  - Used for external network access (interner connectivity / updates).

This simulates like a real enterprise scenario where a domain controller can:

- operate inside a secure internal network.
- still access external resources for updates and administration tasks.

## Security Consideration

The domain controller is exposed to external network only for updates and administration.
Internal services are isolated within the CORP-SWITCH network.

## Ip config

<img width="574" height="347" alt="{F8C869F8-FBC6-4565-BEBA-20485C404BBC}" src="https://github.com/user-attachments/assets/7e9b3138-504d-457d-86d4-a40b2876d16f" />
<img width="465" height="272" alt="{7205C454-3D9C-42EC-A911-3545AF8456AD}" src="https://github.com/user-attachments/assets/5107fa11-3822-4519-ac35-b2bf6168157a" />


## Pings

<img width="980" height="511" alt="{6F30347E-C489-43FB-A683-6CAF69CF4FBD}" src="https://github.com/user-attachments/assets/faa9f521-c1d2-4179-8a0b-b5e9dd380151" />
<img width="531" height="255" alt="{49BF6F43-E763-49E0-A0BF-FA61AAC21087}" src="https://github.com/user-attachments/assets/35afea5e-0051-4c55-97df-b85a028f4d9a" />

## Nginx

<img width="386" height="53" alt="{62DE9009-908A-434C-BD0D-5F2F0B7F5A07}" src="https://github.com/user-attachments/assets/67dca5b0-adee-484e-8572-9991e3c727d1" />

## VM List

<img width="911" height="254" alt="{5DD17D3A-CAF5-42B7-B5DD-146D430EFAF8}" src="https://github.com/user-attachments/assets/53041dc7-9d2f-4f16-82e7-1f8b8e8847a8" />


## Notes / Issues
- Initial network connectivity failed due to incorrect switch configuration.
- Learned difference between Internal vs External virtual switch.
