# ⚙️ Configurations — NEXWARDEN-LABS

![PROJET](https://img.shields.io/badge/PROJET-BANCAIRE-blue) ![STATUT](https://img.shields.io/badge/STATUT-EN_COURS-orange)

> Configurations réseau de l'architecture bancaire sécurisée multi-zones.

---

## 📁 Contenu prévu

| Fichier | Description |
|---------|-------------|
| `vyos-core.conf` | Configuration VyOS Core Banking |
| `vyos-dmz.conf` | Configuration VyOS DMZ |
| `vyos-soc.conf` | Configuration VyOS Zone SOC |
| `vlan-plan.md` | Plan d'adressage VLAN |
| `firewall-rules.conf` | Règles firewall Zone-Based |
| `suricata-banking.rules` | Règles Suricata spécifiques banking |

---

## 🏗️ Architecture

```
Zone DMZ          192.168.10.0/24
Zone Core Banking  192.168.20.0/24
Zone SOC          192.168.30.0/24
Zone Admin        192.168.40.0/24
```

---

*NEXWARDEN-LABS — Alexandre Dossoukpevi | Architecte Cybersécurité & Réseaux*
