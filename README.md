# 🖥️ Infrastructure Multi-Serveurs — Administration Systèmes & Réseaux

## 📌 Présentation

Projet pratique d'administration systèmes et réseaux réalisé dans un environnement virtualisé avec plusieurs serveurs Ubuntu.

L'objectif est de mettre en place une infrastructure réseau locale intégrant différents services d'administration, de partage de fichiers, de résolution DNS et de supervision.

## 🏗️ Architecture

L'infrastructure est composée de trois machines virtuelles :

| Machine | Adresse IP | Rôle |
|---|---|---|
| server-infra | 192.168.56.130 | Infrastructure, services réseau et supervision |
| backend | 192.168.56.129 | Serveur applicatif / Web |
| client | 192.168.56.134 | Machine cliente |

### Réseau

```text
                    Réseau Host-Only
                  192.168.56.0/24
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
   server-infra       backend         client
   192.168.56.130   192.168.56.129  192.168.56.134
          │
          │
    ┌─────┴─────────────────────┐
    │                            │
    ▼                            ▼
  Services                   Monitoring
  réseau                    Prometheus
  DNS / NFS / Samba           Grafana
