# 📚 Documentation — NEXWARDEN-LABS

![PROJET](https://img.shields.io/badge/PROJET-BANCAIRE-blue) ![STATUT](https://img.shields.io/badge/STATUT-EN_COURS-orange)

> Documentation technique de l'architecture bancaire sécurisée multi-zones.

---

## 📁 Contenu prévu

| Document | Description |
|----------|-------------|
| `architecture-overview.md` | Vue d'ensemble de l'architecture |
| `vlan-segmentation.md` | Détail de la segmentation VLAN |
| `security-zones.md` | Description des zones de sécurité |
| `ids-integration.md` | Intégration IDS/IPS Suricata |
| `soc-workflow.md` | Workflow SOC et monitoring |

---

## 🏗️ Zones architecturales

- **DMZ** — Services exposés (Web, DNS, Mail)
- **Core Banking** — Transactions et données sensibles
- **Zone SOC** — Monitoring, Wazuh SIEM, alertes
- **Zone Admin** — Accès restricté administration

---

*NEXWARDEN-LABS — Alexandre Dossoukpevi | Architecte Cybersécurité & Réseaux*
