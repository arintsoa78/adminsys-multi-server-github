# ⚙️ Services de l'infrastructure

## 🖥️ Server-infra

Le serveur `server-infra` centralise les services d'infrastructure et de supervision.

### DNS — BIND9

BIND9 fournit la résolution DNS interne du domaine :

`adminsys.local`

Les principales machines sont définies dans la zone DNS :

- `server.adminsys.local`
- `backend.adminsys.local`
- `client.adminsys.local`

### NFS

NFS permet le partage de fichiers entre les machines Linux de l'infrastructure.

### Samba

Samba fournit un partage de fichiers accessible via le protocole SMB.

### Prometheus

Prometheus collecte les métriques des différents serveurs.

### Grafana

Grafana permet de visualiser les métriques collectées par Prometheus.

### Node Exporter

Node Exporter collecte les métriques système :

- CPU
- mémoire
- disque
- réseau
- charge système

### cAdvisor

cAdvisor permet de surveiller les ressources utilisées par les conteneurs Docker.

### Alertmanager

Alertmanager gère les alertes générées par Prometheus.

---

## 🖥️ Backend

Le serveur `backend` héberge les services applicatifs :

- Apache
- Application PHP `Vente Voiture`
- FileZilla Server
- Node Exporter

---

## 💻 Client

Le serveur `client` est utilisé pour tester :

- la connectivité réseau ;
- la résolution DNS ;
- l'accès aux applications Web ;
- les partages réseau ;
- la communication entre les serveurs.

---

## 🎯 Objectif

L'ensemble de ces services permet de mettre en place une infrastructure multi-serveurs comprenant :

- des services réseau ;
- des services applicatifs ;
- du partage de fichiers ;
- de la supervision ;
- de la gestion des alertes.
