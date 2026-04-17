---
title: "Aptum IaaS:  Configuration du client VPN IPSec Microsoft Windows"
slug: aptum-iaas-ipsec-client-config-windows
---

Les instructions suivantes s'appliquent à Microsoft Windows 10 utilisant son client VPN natif :

#### Créer une connexion VPN réseau

1. Allez à *Menu Démarrer* > *Paramètres* > *Réseau et Internet*.
![Paramètres](img/Win-4-Settings.png)
2. Cliquez sur *VPN*.
![Configuration de VPN](img/Win-5-VPN.png)
3. Cliquez sur *Ajouter une connexion VPN*.
![Ajouter connexion](img/Win-6-Add-Connection.png)
4. Sur la page *Ajouter une connexion VPN* :
- **Fournisseur VPN :** *Windows (intégré)*
- **Nom de la connexion :** Entrez un nom pour votre connexion VPN (par exemple, **acme-vpn**)
- **Nom ou adresse du serveur :** Entrez l’adresse IP publique indiquée sur la page *VPN d’accès distant*
- **Type de VPN :** Sélectionnez *L2TP/IPSec avec clé pré-partagée*
- **Clé pré-partagée :** Entrez la clé pré-partagée indiquée sur la page *VPN d’accès distant*
- **Type d’informations de connexion :** Sélectionnez *Nom d’utilisateur et mot de passe*
- **Nom d’utilisateur :** Entrez le nom d’utilisateur du compte VPN créé par votre administrateur
- **Mot de passe :** Entrez le mot de passe du compte VPN
![Détails de connexion](img/Win-7-Connection-Details.png)
5. Cliquez sur *Sauvegarder*. La page *VPN* s'affichera et la nouvelle connexion apparaîtra dans la liste des connexions.
![Sélectionner la connexion](img/Win-8-Select-Connection.png)


#### Établir une connexion VPN
1. Allez à *Menu Démarrer* > *Paramètres* > *Réseau et Internet* > *VPN*.
2. Cliquez sur la connexion VPN souhaitée, puis sur le bouton *Se connecter*.
![Connecter](img/Win-9-Connect.png)
3. Le VPN est maintenant connecté.

<!-- ![Connected](img/Win-10-Connected.png) -->
