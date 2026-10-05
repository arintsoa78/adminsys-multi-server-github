# 💻 Client

## 📌 Présentation

La machine `client` représente le poste client de l'infrastructure multi-serveurs.

Elle permet d'effectuer les tests d'accès aux différents services déployés sur les serveurs.

## 🌐 Informations réseau

| Élément | Valeur |
|---|---|
| Hostname | client |
| Adresse IP LAN | 192.168.56.134 |
| Système | Ubuntu |
| Réseau | 192.168.56.0/24 |

## 🔎 Tests réalisés

Depuis cette machine, les services de l'infrastructure peuvent être testés, notamment :

- connectivité réseau ;
- résolution DNS ;
- accès aux services Web ;
- accès aux partages réseau ;
- communication avec le serveur Backend ;
- vérification de la supervision.

## 🔗 Architecture

```text
                    Réseau local
                 192.168.56.0/24
                        │
          ┌─────────────┼─────────────┐
          │             │             │
          ▼             ▼             ▼
     server-infra     backend       client
     .130             .129          .134
          │             │             │
          └─────────────┴─────────────┘
