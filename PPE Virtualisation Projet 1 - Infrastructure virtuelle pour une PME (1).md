---
title: PPE Virtualisation Projet 1 - Infrastructure virtuelle pour une PME

---

# Projet 1 — Infrastructure virtuelle pour une PME

**1. Installer l'hyperviseur sur la machine hôte**

- Installation de l'hyperviseur VMware

![2026-10-05_08h43_07](https://hackmd.io/_uploads/SyvLPploMg.png)

**2. Créer 3 VM avec des rôles distincts (fichiers, impression, application).**

- Les 3 vm ont bien été créé mais je n'avais pas de cable ethernet donc je n'ai pas pu faire l'istallation complète

![2026-10-07_10h06_47](https://hackmd.io/_uploads/ry3i6OmoGe.png)

**3. Configurer le réseau virtuel pour que les VM communiquent entre elles et avec l'extérieur**

- Avant de vouloir configurer le réseau virtuel, il faut d'abord vérifier que les vm sont sur la même 'Network connection'

VM -> Settings -> Network Adapter -> Sélectionner 'NAT' -> vérifier que 'Connected' et 'COnnected at the power' sont cochés

![2026-10-05_09h43_14](https://hackmd.io/_uploads/SJvjBCliGx.png)

- Il faut vérifier le réseau VMware

Edit -> Virtual Network Editor -> VM8net

![2026-10-05_09h55_24](https://hackmd.io/_uploads/H1fZdRxizg.png)

**4. Allouer les ressources selon les besoins estimés de chaque rôle**

| VM | Système | vCPU | RAM | Disque |
|---|---|---|---|---|
| SRV-FICHIERS | Ubuntu Server | 1 à 2 | 2 Go | 20 Go (système) + 50 Go (données) |
| SRV-IMPRESSION | Windows 11 | 2 | 4 Go | 64 Go |
| SRV-APP | Ubuntu Server | 2 | 4 Go | 30 Go |

**5. Démarrez et validez le fonctionnement des 3 VM**

- Les 3 vm démarrent et fonctionnent

![2026-10-07_10h36_50](https://hackmd.io/_uploads/rJOQrY7oGx.png)

![2026-10-07_10h38_38](https://hackmd.io/_uploads/r1S4HFXjGx.png)

![2026-10-07_10h38_38](https://hackmd.io/_uploads/rkwNStXiGl.png)

























