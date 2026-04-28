# 🗺️ Diagrammes — Architecture Bancaire Sécurisée

![PROJET](https://img.shields.io/badge/PROJET-BANCAIRE-blue) ![STATUT](https://img.shields.io/badge/STATUT-EN_COURS-orange)

> Schémas d'architecture réseau de l'infrastructure bancaire multi-zones (Draw.io / PNG).

---

## 📁 Diagrammes prévus

| Fichier | Description |
|---------|-------------|
| `architecture-globale.png` | Vue globale de l'architecture |
| `dmz-topology.png` | Topologie de la DMZ |
| `vlan-segmentation.png` | Plan de segmentation VLAN |
| `soc-dataflow.png` | Flux de données SOC/monitoring |
| `ids-deployment.png` | Placement des sondes IDS |

---

## 🏗️ Zones représentées

```
[Internet]
    |
[Firewall Périmétrique]
    |
    +--- [DMZ: Web / DNS / Mail]
    |         |
    +--- [Core Banking: Transactions]
    |         |
    +--- [Zone SOC: Wazuh / Suricata]
    |
[Zone Admin]
```

---

*NEXWARDEN-LABS — Alexandre Dossoukpevi | Architecte Cybersécurité & Réseaux*
