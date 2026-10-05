# 🌐 Architecture réseau

## Vue globale

L'infrastructure est composée de trois machines virtuelles connectées sur un réseau Host-Only VirtualBox.

```text
                         VirtualBox
                    Réseau Host-Only
                     192.168.56.0/24
                              │
          ┌───────────────────┼───────────────────┐
          │                   │                   │
          ▼                   ▼                   ▼
   ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
   │ server-infra │    │   backend    │    │    client    │
   │              │    │              │    │              │
   │ 192.168.56.130│   │192.168.56.129│    │192.168.56.134│
   └──────┬───────┘    └──────┬───────┘    └──────────────┘
          │                   │
          │                   │
          ▼                   ▼
     Services réseau      Services Web
     & supervision       & applications
