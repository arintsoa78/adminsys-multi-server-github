# 🖥️ Serveur Backend

## 📌 Présentation

Le serveur `backend` constitue la partie applicative de l'infrastructure multi-serveurs.

Il héberge les services Web et les applications utilisées dans le laboratoire.

## 🌐 Informations réseau

| Élément | Valeur |
|---|---|
| Hostname | backend |
| Adresse IP LAN | 192.168.56.129 |
| Système | Ubuntu Server |
| Réseau | 192.168.56.0/24 |

## ⚙️ Services

### Apache

Le serveur Apache est utilisé pour héberger les applications Web.

### Application Vente Voiture

Une application Web développée en PHP est déployée sur le serveur.

Elle permet notamment la gestion :

- des clients ;
- des véhicules ;
- des achats ;
- des factures ;
- de l'authentification.

### FileZilla Server

FileZilla Server est utilisé pour les besoins de transfert de fichiers dans l'environnement de laboratoire.

### Node Exporter

Node Exporter permet de récupérer les métriques système du serveur afin de les envoyer vers Prometheus.

## 📁 Organisation

```text
backend/
├── apache/
├── filezilla/
├── vente_voiture/
└── README.md
