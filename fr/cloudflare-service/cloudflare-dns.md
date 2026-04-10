---
title: "Cloudflare: DNS"
slug: cloudflare-dns
---


Cet article présente le service DNS de Cloudflare, permettant de créer et de gérer des domaines, des enregistrements et des comptes via l'environnement Aptum Portal.

## Aperçu

Le service DNS de Cloudflare offre une résolution de noms performante pour les applications à grande échelle, avec une distribution mondiale et une sécurité renforcée. Aptum Portal s'intègre à ce service DNS en permettant la gestion des zones, notamment l'ajout et la suppression d'enregistrements DNS. Cette intégration permet d'administrer plusieurs zones à partir d'un seul environnement Aptum Portal.

Pour que la résolution DNS fonctionne correctement, votre domaine doit être configuré avec votre registraire de noms de domaine pour pointer vers les serveurs de noms de Cloudflare. Cloudflare héberge les enregistrements DNS \(aussi appelés **enregistrements de ressources**\) de votre domaine. L'interface d'Aptum Portal offre un moyen simple de gérer ces enregistrements de ressources, en complément de vos autres services cloud.

![Diagramme illustrant les relations entre les principales entités d'Aptum Portal et de Cloudflare](img/cloudflare-dns-entities.png)

Pour optimiser les performances et la sécurité, vous pouvez également configurer Cloudflare pour qu'il gère le trafic de vos enregistrements A, AAAA et CNAME. Lorsqu'un client effectue une requête DNS pour le nom d'hôte d'un enregistrement DNS géré par proxy, Cloudflare retourne l'adresse IP de ses serveurs frontaux. Lorsqu'un client effectue une requête HTTP ou HTTPS, il l'envoie aux serveurs de Cloudflare, qui la transmettent au serveur d'origine, c'est-à-dire celui identifié dans votre enregistrement DNS. Le contenu de cette requête est retourné au client et mis en cache sur les serveurs de Cloudflare pour un accès plus rapide.

## Environnements

Pour commencer à utiliser les ressources Cloudflare, créez un nouvel environnement dans le service Cloudflare d'Aptum Portal. Lors de la création d'un nouvel environnement, un compte sera automatiquement créé dans Cloudflare et associé à cet environnement d'Aptum Portal.

![Capture d'écran de la page Environnements du service Cloudflare](img/cloudflare-env-list.png)

En cas d'erreur lors de la création d'un nouvel environnement, il est possible que la clé API Cloudflare utilisée pour établir la connexion au service ne dispose pas des autorisations nécessaires. Contactez votre administrateur Cloudflare et assurez-vous que le compte principal dispose des autorisations suivantes pour cette clé API :

-   `Zone.Zone Settings`
-   `Zone.Zone`
-   `Zone.DNS`
-   `Global xauth key`

## Domaines

En cliquant sur un environnement, vous accéderez à la liste des domaines gérés dans cet environnement, où vous pourrez ajouter de nouveaux domaines. Lors de l'ajout d'un domaine, vous avez la possibilité de demander au système d'analyser votre domaine et d'importer les enregistrements de ressources existants. Une fois le domaine ajouté, il restera à l'état `Pending namerservers` jusqu'à ce que le registraire de domaine soit configuré pour pointer vers les serveurs de noms Cloudflare.

![Capture d'écran de l'onglet Domaines d'un environnement Cloudflare, mettant en évidence les fonctionnalités clés](img/cloudflare-domain-list.png)

1. **Liste des domaines**

   Dans la zone principale de l'espace de travail, la liste de tous les domaines de l'environnement sélectionné s'affiche.

2. **Champ de recherche**

   Entrez du texte dans la boîte de recherche pour filtrer la liste des domaines. Le système effectuera une recherche par nom et par date de dernière modification, et affichera les domaines correspondants.

3. **Ajouter un domaine**

   Cliquez pour définir un domaine à héberger sur Cloudflare.

   Vous pouvez également importer les enregistrements DNS existants du domaine cible lors de sa création.

4. **Fiche de domaine**

   Chaque fiche comprend le nom du domaine, l'état de sa configuration, le type d'abonnement et la date de dernière modification.

   Cliquez sur une fiche pour accéder à sa page de détails.

5. **Menu des actions cachées**

   Chaque fiche de domaine possède un menu des actions cachées. Cliquez dessus pour accéder à la liste des opérations les plus fréquemment utilisées.


## Enregistrements DNS

Cliquez sur un domaine pour afficher ses serveurs de noms actuels et leurs adresses IP, ainsi que la liste de tous ses enregistrements DNS.

Si le système détecte que le registraire de domaine n'a pas configuré ce domaine pour utiliser les serveurs DNS de Cloudflare, un message d'information s'affichera, indiquant que cette étape est nécessaire. Il fournira également les serveurs de noms et leurs adresses IP tels qu'ils doivent être configurés chez le registraire.

La liste des enregistrements DNS contiendra les champs standards pour chaque enregistrement de ressource et indiquera également si le trafic pour ce nom d'hôte est redirigé vers un proxy.

![Capture d'écran de la page des enregistrements DNS](img/cloudflare-dns-records.png)

