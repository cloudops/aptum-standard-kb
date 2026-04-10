---
title: "Cloudflare: Ajouter un enregistrement DNS"
slug: cloudflare-ajouter-enregistrement-dns
---


## À propos de cette tâche

Cet article vous guidera tout au long du processus d'ajout d'un nouvel enregistrement DNS à un domaine DNS Cloudflare.

## Avant de commencer

- Votre environnement Cloudflare doit déjà exister
- Le domaine cible doit déjà exister dans l'environnement
- Le registraire hébergeant ce nom de domaine doit pointer vers les serveurs de noms Cloudflare
- Le domaine doit être actif

## Procédure

1. Accédez à votre service Cloudflare via le menu **Services**, cliquez sur l'environnement cible depuis la page du service, puis sur le domaine cible.

2. Cliquez sur le bouton **Ajouter un enregistrement DNS**.

3. Dans la boîte de dialogue **Ajouter un enregistrement DNS**, sélectionnez le type d'enregistrement et entrez les valeurs.

   Chaque type d'enregistrement de ressource a ses propres champs ; modifier le champ **Type** modifiera donc les champs affichés.

4. Sélectionnez une durée de vie (TTL) pour cet enregistrement.

   Cette option détermine la durée pendant laquelle un client DNS mettra l'enregistrement en cache avant de le redemander au système DNS.

5. (Optionnel) Entrez un commentaire qui sera ajouté à l'enregistrement. Ce commentaire est interne à l'enregistrement et ne s'affichera pas dans la liste des enregistrements.

6. Cliquez sur le bouton **Valider**.


## Résultats

- Le nouvel enregistrement DNS est maintenant affiché sur la page du domaine cible.
- L'enregistrement est maintenant résolu lors d'une requête auprès du système DNS.

