---
title: PPE Virtualisation Projet 2 - Snapshots et plan de reprise d'une VM critique

---

# Projet 2 — Snapshots et plan de reprise d'une VM critique

**1. Créer une VM de test avec une application simpe installée**

- Création d'une vm Windows 11 avec la création d'un nouveau dossier avec des fichiers

![2026-10-05_10h09_40](https://hackmd.io/_uploads/B13IiAlsfe.png)

![2026-10-05_10h29_01](https://hackmd.io/_uploads/Hk4xgyWszx.png)

**2. Prendre un instantané avant une modification volontaire (ex. installation d'une mise à jour)**

- Pour prendre un instantané (Snapchot) il faut passer pas ces étapes:

Sélectionner la VM -> Cliquer sur 'VM' -> 'Snapchot' -> 'Take Snapchot' -> Nommer le Snapchot -> Cliquer sur Take Snapchot

**3. Simuler un incident (suppression de fichier, panne applicative)**

- Suppression le dossier du bureau

![2026-10-05_10h39_12](https://hackmd.io/_uploads/H1hPfkZsMx.png)

![2026-10-05_10h39_49](https://hackmd.io/_uploads/HJ1Of1bjGl.png)

- Quand je retourne dans 'Bureau' on peux voir que le dossier à bien été supprimé

![2026-10-05_10h40_36](https://hackmd.io/_uploads/BJInzy-oMe.png)

**4. Restaurer la VM a partir du snapshot**

- Pour restaurer la VM a partir du snapshot il faut aller dans 'VM' - 'Snapshot' -> Sélectionner 'Revert to snapshot' -> cliquer sur 'Yes'

![2026-10-05_10h51_10](https://hackmd.io/_uploads/H1rGSyZiGl.png)

**5. Mesurer le temps de restauration**

- Le temps de restauration du snapshot est environ de 2m15

6. Rédiger un plan de reprise (RTO/RPO simplifiés.)

**Plan de reprise**: En cas de suppression accidentelle de fichiers, la VM sera restaurée à partir du dernier snapshot disponible. Le RPO correspond au dernier point de sauvegarde, les modifications effectuées après celui-ci pouvant être perdues.


























