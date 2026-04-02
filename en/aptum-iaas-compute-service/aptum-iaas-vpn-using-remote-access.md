---
title: "Connect to a VPC using remote access VPN"
slug: connect-to-a-remote-management-vpn
---

Aptum IaaS provides the ability to connect securely from your home or office to your VPC. Using a pre-shared key with a VPN client on your preferred platform (e.g.: Windows, macOS, Ubuntu...), you will be able to access your instances without having to go through port forwarding on public IP addresses.

## VPC Configuration
**Note:** To perform the following operations, your user account needs to be assigned either the **Editor** or **Owner** role on the target environment.

#### Enable VPN access
Before you can connect to your VPC through a client VPN connection, you need to enable VPN access on the VPC.

1. Navigate to the target Aptum IaaS environment.
1. Select the *Networking* tab.
1. Locate the target VPC.  This is the VPC that you wish to connect to via the VPN.
1. Click the *Remote Access VPN* gear icon for the target VPC.  The *Remote access VPN* page appears.
1. Click on the Hidden Actions menu and select *Enable* to activate VPN access.
1. After a few moments, a pre-shared key will be displayed on the page, in the *Attributes* section.
1. The IP address to connect to is displayed at the top of the card.  Copy and paste this address into your VPN client.
1. Copy and paste this pre-shared key into your VPN client.

#### Create VPN user
1. In the *Remote access VPN* page of the VPC, the list of VPN users is also displayed below the pre-shared key.
1. Click on *Add VPN User*.
1. Fill the *Add VPN User* form.
1. Click on *Submit*.
1. Repeat previous steps for each desired VPN user.

## Connection to VPN
After you've successfully configured your VPC for VPN access, and created at least one VPN user, you are now ready to connect to this VPN to access your instances and applications. When connected to a VPC via VPN, the clients have access to all its tiers (up to 4 subnets).

The following information is required to configure the VPN client:

   - **Public IP:** The VPC's public IP address with tagged with the `VPN` purpose.
   - **Pre-shared key:** The string displayed in the *Attributes* section of the *Remote Access VPN* page.
   - **Username:** a valid VPN account username.
   - **Password:** a valid VPN account password.