---
title: "Cloudflare: Ajouter un domaine"
slug: cloudflare-ajouter-domaine
---


## À propos de cette tâche

Cet article vous guidera tout au long du processus d'ajout d'un nouveau domaine à un environnement Cloudflare.

## Avant de commencer

- Votre environnement Cloudflare doit déjà exister.

## Procédure

1. Accédez à votre service Cloudflare via le menu **Services** et cliquez sur l'environnement cible depuis la page du service.

2. Cliquez sur le bouton **Ajouter un domaine**. La page **Ajouter un domaine** s'affiche.

3. Entrez le nom de domaine complet à ajouter.

   Il n'est pas nécessaire d'ajouter le point final. Le système l'ajoutera automatiquement.

   Vous pouvez cocher la case **Quick Scan for Records** pour que le système importe les enregistrements de ressources existants en interrogeant les serveurs de noms actuels.

4. Cliquez sur **Valider**.

5. Si vous avez coché la case **Quick Scan for Records**, cliquez sur votre domaine lorsque la page de l'environnement s'affiche, puis vérifiez que tous les enregistrements de ressources requis ont bien été importés.

   Il est possible que certains enregistrements soient omis lors de la recherche. Si c'est le cas, ajoutez-les manuellement.


## Résultats

- Le domaine est maintenant répertorié dans l'environnement cible.

- Si l'importation a été sélectionnée, vous avez vérifié que tous les enregistrements ont été importés et que les enregistrements manquants ont été ajoutés manuellement.

