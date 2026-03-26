# 🏦 NEXWARDEN-LABS – Architecture Bancaire Sécurisée

![Status](https://img.shields.io/badge/statut-en%20cours-orange?style=for-the-badge)
![Security](https://img.shields.io/badge/focus-cybersécurité-blue?style=for-the-badge)
![Type](https://img.shields.io/badge/type-projet%20professionnel-green?style=for-the-badge)

> **Projet professionnel actuel** : Conception et sécurisation d'une architecture réseau bancaire multi-zones avec segmentation stricte, IDS/IPS actif et monitoring SOC centralisé.

---

## 🎯 Objectif

Simuler et sécuriser une **infrastructure bancaire réaliste** respectant les standards de sécurité bancaire :
- Segmentation réseau stricte (DMZ, Core Banking, Back-Office, SOC)
- Protection périmétrique (firewall VyOS, règles ACL)
- Détection d'intrusion en temps réel (IDS/IPS Suricata)
- Monitoring et corrélation des événements (Wazuh, ELK Stack)
- Tests de résilience face aux attaques courantes

Ce projet démontre une **approche architecte cybersécurité** pour des environnements critiques.

---

## 🏗️ Architecture Réseau
## 🗺️ Diagramme de l'Architecture Complète

![Architecture NEXWARDENLABS - GNS3 + VMware](LAB.png)

*Topologie complète avec DMZ, Data-Center, Monitoring SOC, Zone APT, Firewall VyOS, Suricata, Wazuh, ELK, etc.*
### Zones de sécurité

| Zone | Fonction | Technologies | Niveau de confiance |
|------|----------|--------------|--------------------|
| **WAN (Internet)** | Zone externe, source des attaques | Simulation d'attaquant (Kali Linux) | ❌ Non fiable |
| **DMZ** | Services exposés (Web, FTP, RDP) | Windows Server 2022, Nginx | ⚠️ Exposition contrôlée |
| **LAN (Core Banking)** | Postes de travail, applications métier | Windows 11, serveurs internes | ✅ Zone protégée |
| **SOC / Monitoring** | Centre de surveillance sécurité | Ubuntu + Suricata, Wazuh, ELK | 🔒 Zone hautement sécurisée |

### Équipements de sécurité

- **Pare-feu principal** : pfSense (rôle de routeur + filtrage)
- **Routeur d'entreprise** : VyOS (routing avancé, NAT, DHCP, ACL)
- **IDS/IPS** : Suricata (détection en temps réel + alertes)
- **SIEM** : Wazuh + ELK Stack (centralisation des logs)
- **Segmentation** : VLANs isolés avec politiques d'accès strictes

---

## 🔐 Sécurité Implémentée

✅ **Firewall VyOS avec règles strictes**
- Blocage par défaut (deny all)
- Autorisation explicite des flux légitimes
- Journalisation de toutes les connexions

✅ **Segmentation VLAN + ACL**
- VLAN 10 : DMZ (services exposés)
- VLAN 20 : LAN (utilisateurs internes)
- VLAN 30 : SOC (monitoring)
- Interdiction de communication directe DMZ ↔ LAN

✅ **IDS/IPS actif (Suricata)**
- Règles de détection personnalisées
- Alertes en temps réel via Gotify
- Blocage automatique des scans réseau

✅ **Monitoring centralisé**
- Logs agrégés dans Wazuh
- Dashboards de visualisation (Kibana)
- Corrélation d'événements de sécurité

---

## 🧪 Scénarios de Tests Réalisés

| Attaque simulée | Détection | Résultat |
|-----------------|-----------|----------|
| Scan réseau (Nmap UDP/TCP) depuis WAN → DMZ | ✅ Détecté | Alerté + Bloqué |
| Scan interne LAN → DMZ (reconnaissance) | ✅ Détecté | Alerté en temps réel |
| Tentative d'accès non autorisé DMZ → LAN | ✅ Bloqué | Règle firewall active |
| Exfiltration de données | ✅ Détecté | Logs SOC générés |

### Résultats

- **100% des attaques simulées détectées** par Suricata
- **Flux bancaires isolés** et contrôlés via VLAN + ACL
- **Logs centralisés** et analysables dans le SIEM
- **Alertes instantanées** envoyées aux administrateurs (Gotify)

---

## 🧠 Compétences Démontrées

`Architecture réseau` `Cybersécurité bancaire` `Segmentation VLAN` `IDS/IPS` `Firewall avancé` `VyOS` `Suricata` `Wazuh` `ELK Stack` `GNS3` `Virtualisation` `Analyse SOC` `Détection d'intrusion` `Tests de pénétration` `Documentation technique`

---

## 📊 Environnement Technique

### Logiciels
- **Virtualisation** : VMware Workstation Pro 17
- **Simulation réseau** : GNS3
- **Systèmes** : Ubuntu Server 22.04, Windows Server 2022, Windows 11, Kali Linux
- **Sécurité** : pfSense, VyOS, Suricata, Wazuh, Snort
- **Monitoring** : ELK Stack (Elasticsearch, Logstash, Kibana), Gotify

### Configuration matérielle
- Processeur : Intel Core i7 (12ème génération)
- RAM : 16 Go
- Stockage : 512 Go SSD
- Réseau : Interfaces bridge, host-only, NAT, custom LAN segments

---

## 📂 Structure du Projet

```
nexwarden-labs/
├── architecture/
│   └── diagrams/           # Schémas réseau (zones, flux, topologie)
├── configs/
│   ├── vyos/              # Configurations VyOS (NAT, ACL, VLAN)
│   ├── suricata/          # Règles IDS personnalisées
│   ├── pfsense/           # Configurations pare-feu
│   └── vlans/             # Plan d'adressage et segmentation
├── reports/
│   ├── tests-intrusion.md # Résultats des tests de sécurité
│   └── alertes-suricata/  # Captures d'alertes générées
├── scripts/
│   └── monitoring/        # Scripts Python pour automatisation alertes
└── docs/
    ├── installation.md    # Guide de mise en place
    └── methodologie.md    # Approche et justifications techniques
```

---

## 🔗 Liens Associés

- **Portfolio NEXWARDEN** : [Voir le portfolio](https://github.com/Alex987411/NEXWARDEN)
- **Dépôt principal NEXWARDEN** : [Alex987411/NEXWARDEN](https://github.com/Alex987411/NEXWARDEN)
- **Section académique (IDS Suricata)** : [academic/ids-suricata-memoire](https://github.com/Alex987411/NEXWARDEN/tree/main/academic/ids-suricata-memoire)

---

## 🎓 Contexte

Ce projet **professionnel en cours** s'inscrit dans une démarche de montée en compétences en architecture cybersécurité appliquée aux environnements bancaires. Il fait suite à un projet académique de mémoire sur la mise en place d'un IDS Suricata (voir section académique du dépôt NEXWARDEN).

**Du lab à l'architecture réelle** :
- Les Labs 01 et 02 (NEXWARDEN) ont permis d'acquérir les fondamentaux (attaque/défense, détection).

---

- **nexwarden-labs (ce projet)** = projet professionnel d'architecture bancaire sécurisée complète.

- **LinkedIn** : [Alexandre DOSSOUKPEVI](https://www.linkedin.com/in/nexwarden)
- **Email** : Disponible sur demande via LinkedIn
- **GitHub** : [Alex987411](https://github.com/Alex987411)

---

## 📄 Licence

MIT License – Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

> **Note** : Ce projet est en cours de développement et sera enrichi régulièrement (diagrammes, configurations détaillées, rapports de tests complets).
