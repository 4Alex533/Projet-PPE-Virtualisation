---
title: PPE Virtualisation Projet 5 - Comparatif d'hyperviseurs pour un cahier des charges client

---

# Projet 5 - Comparatif d'hyperviseurs pour un cahier des charges client

**1. Définir les critères de comparaison (coût, licences, facilité d'administration, performances, écosystème)**

| Critère                       | VMware Workstation                                             | VMware ESXi                                                                      |
| ----------------------------- | -------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| **Coût**                      | Gratuit pour un usage personnel selon les conditions actuelles | Version gratuite disponible selon l'offre, fonctionnalités avancées sous licence |
| **Licences**                  | Logiciel installé sur un système Windows/Linux                 | Hyperviseur de type 1 installé directement sur le serveur                        |
| **Facilité d'administration** | Très simple avec une interface graphique locale                | Administration plus orientée serveur, notamment via interface Web                |
| **Performances**              | Bonnes, mais dépend du système hôte                            | Très bonnes car les ressources sont directement dédiées à l'hyperviseur          |
| **Écosystème**                | Adapté aux postes de travail, tests et laboratoires            | Adapté aux serveurs, datacenters et infrastructures professionnelles             |

**2. Installer et tester au moins deux hyperviseurs différents avec un cas d'utilisation identique. **

- VMware Workstation : installation et test d'une VM Ubuntu réalisés avec succès.

(L'image de screenpresso ne veut pas s'afficher)

- VMware ESXi : installation et configuration de l'hyperviseur testées. La création et l'exécution d'une VM n'ont pas pu être réalisées, car aucun serveur physique compatible n'était disponible pour l'installation d'ESXi.

![2026-10-06_14h56_07](https://hackmd.io/_uploads/BkJ-e_zjMx.png)

**3. Mesurer/observer les différences notables.**

| Critère | VMware Workstation Pro | VMware ESXi |
|---|---|---|
| Type | Type 2 (hébergé) | Type 1 (bare-metal) |
| Installation | Application sur Windows/Linux | Système dédié sur un serveur |
| Matériel supporté | Tout PC compatible avec l'OS hôte | Liste de compatibilité stricte (HCL) |
| Ressources consommées | Hyperviseur + OS hôte + autres applications | Hyperviseur seul, très léger |
| Administration | Interface graphique locale | Client web, vCenter pour plusieurs hôtes |
| Usage visé | Poste de travail, labo, tests, développement | Production, serveurs, centres de données |
| Fonctions avancées | Snapshots, clones, réseaux virtuels | + vMotion, DRS, HA, vSAN (avec vSphere/vCenter sous licence) |
| Accès à l'hôte | L'OS hôte reste utilisable en parallèle | Machine dédiée à la virtualisation |
| Disponibilité | Dépend de l'OS hôte (mises à jour, redémarrages) | Conçu pour tourner en continu |

**4. Construire un tableau comparatif**

# Comparatif VMware Workstation Pro vs VMware ESXi

## 1. Tableau comparatif

| Catégorie | Critère | VMware Workstation Pro | VMware ESXi | Avantage |
|---|---|---|---|---|
| **Architecture** | Type | Type 2 (hébergé) | Type 1 (bare-metal) | ESXi |
| | Installation | Application sur Windows/Linux | Système dédié sur un serveur | Workstation |
| | Matériel supporté | Tout PC compatible avec l'OS hôte | Liste de compatibilité stricte (HCL) | Workstation |
| **Performances** | Ressources consommées | Hyperviseur + OS hôte + autres applications | Hyperviseur seul, très léger | ESXi |
| | Densité de VM | Limitée par l'OS hôte | Élevée | ESXi |
| | Surcoût de virtualisation | Plus élevé (couche OS hôte) | Minimal | ESXi |
| **Administration** | Interface | Interface graphique locale | Client web, vCenter pour plusieurs hôtes | Selon le contexte |
| | Gestion de plusieurs hôtes | Non | Oui (vCenter) | ESXi |
| | Prise en main | Immédiate | Demande une formation | Workstation |
| **Fonctionnalités** | Snapshots, clones | Oui | Oui | Égalité |
| | Réseaux virtuels | NAT, Host-only, bridged, LAN segment | vSwitch, VLAN | Égalité |
| | vMotion, DRS, HA, vSAN | Non | Oui (avec vSphere/vCenter sous licence) | ESXi |
| **Exploitation** | Accès à l'hôte | L'OS hôte reste utilisable en parallèle | Machine dédiée à la virtualisation | Workstation |
| | Disponibilité | Dépend de l'OS hôte (mises à jour, redémarrages) | Conçu pour tourner en continu | ESXi |
| | Usage visé | Poste de travail, labo, tests, développement | Production, serveurs, centres de données | Selon le besoin |
| **Coût** | Licence | Gratuit pour tous les usages depuis novembre 2024 | Abonnement, minimum de 16 cœurs | Workstation |
| | Matériel nécessaire | Un PC suffit | Serveur dédié | Workstation |

## 2. Mesures

| Mesure | Outil | Workstation | ESXi | Écart |
|---|---|---|---|---|
| RAM consommée au repos (hôte compris) | Gestionnaire des tâches / `top` | | | |
| Temps de démarrage de la VM | Chronomètre | | | |
| Débit disque (lecture/écriture) | `fio` / CrystalDiskMark | | | |
| Débit réseau entre deux VM | `iperf3` | | | |
| Performances CPU | `sysbench cpu` | | | |
| Temps de snapshot / clone | Chronomètre | | | |
| Nombre de VM avant saturation | Test de charge | | | |

## 3. Recommandation par usage

| Contexte du client | Choix recommandé | Justification |
|---|---|---|
| Poste de développeur, tests, labo de formation | **Workstation Pro** | Gratuit, simple, souple |
| Quelques VM sur un PC existant | **Workstation Pro** | Pas de matériel dédié |
| Serveurs en production, disponibilité exigée | **ESXi** | Performances, stabilité, haute disponibilité |
| Plusieurs hôtes à centraliser | **ESXi + vCenter** | Gestion unifiée, migration à chaud |
| Budget serré en production | À étudier | Envisager aussi Proxmox ou Hyper-V |

## 4. Conclusion

> À rédiger après les mesures : synthèse et recommandation argumentée selon le cahier des charges du client.


















