---
title: PPE Virtualisation Projet 3 - Réseau virtuel isolé (labo de test)

---

# Projet 3 — Réseau virtuel isolé (labo de test)

**1. Créer un commutateur/réseau virtuel de type interne**

Pour créer un réseau virtuel sur VMware workstation il faut faire ainsi:

- Dans VMware cliquer sur 'Edit' -> 'Virtual Network Editor'

- Cliquer sur 'Changes Settings' et accepter les droits

![2026-10-05_13h44_18](https://hackmd.io/_uploads/H1Apxz-oMx.png)

- Cliquer sur 'Add Network'

- Choisir un nouveau VMnet

![2026-10-05_13h45_16](https://hackmd.io/_uploads/H1xeWM-ofl.png)


- Sélectionner 'Host-only'

- Cliquer sur 'Apply' -> 'Ok'

![2026-10-05_13h47_37](https://hackmd.io/_uploads/H1x-Wzbizx.png)

**2. Connecter au moins 2 VM à ce réseau**

- J'ai connecter les VM Windows et ubuntu

![2026-10-05_14h11_25](https://hackmd.io/_uploads/ryRCEf-jfg.png)

**3. Vérifier qu'aucune de ces VM n'a accès à internet ni au réseau physique**

- Pour les deux VM cliquer sur 'Settings' -> 'Network Adapter'

- Vérifier que l'adaptateur est configuré sur 'Custom -> VMnet2'

- Vérifier que 'Connect at the power' est activé

![2026-10-05_14h24_28](https://hackmd.io/_uploads/HJ5GFz-sfl.png)

![2026-10-05_14h27_07](https://hackmd.io/_uploads/SJJQKfZiMe.png)


- Dans chaque VM, ouvrir le terminal et tester le ping de la VM

![2026-10-05_14h50_04](https://hackmd.io/_uploads/S1wrafZofg.png)

![2026-10-05_14h50_42](https://hackmd.io/_uploads/H1jBTfZoMl.png)

- Depuis la 1ère VM essayer de ping la 2nd VM

![2026-10-05_14h53_36](https://hackmd.io/_uploads/ryclCfZiGl.png)

**4. Tester la connectivité entre les VM du labo**

- Ouvrir le terminal sur les deux VM et faire un ping

![2026-10-06_13h49_46](https://hackmd.io/_uploads/rJrYgvMofg.png)

![2026-10-06_13h50_03](https://hackmd.io/_uploads/Hk_YgPGofl.png)

**5. Documenter le schéma réseau et les règles d'isolement**

- Les VM communiquent uniquement via le réseau interne du laboratoire.
- Elles n'ont pas d'accès direct au réseau physique.
- Elles n'ont pas accès à Internet directement.
- Les communications entre les VM du réseau interne sont autorisées.












