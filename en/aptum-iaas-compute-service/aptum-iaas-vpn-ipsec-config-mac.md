---
title: "Aptum IaaS:  macOS IPSec VPN Client Configuration"
slug: aptum-iaas-ipsec-client-config-mac
---

This operating system provides a native IPSec VPN client. Here are the steps to set up a VPN connection:

#### Create the VPN connection

1. Open *System Settings* > *Network*.
   ![Add VPN](img/Mac-4-Add-VPN.png)
1. Click on the **...** popup menu, then on **Add VPN Configuration** > **L2TP over IPSec**:
   - **Display name:** Enter a name for your VPN connection (e.g., **acme-vpn**)
   - **Configuration:** Leave this as the default
   - **Server address:** Enter the public IP address from the *Remote access VPN* page
   - **Account name:** Enter the username for the VPN user created for you by your administrator
   - **User authentication:** Select *Password*
   - **Password:** Enter the password specified for the VPN user
   - **Machine authentication:** Select *Shared secret*
   - **Shared secret**: Enter the pre-shared key from the *Remote access VPN* page
   - **Group name:** Leave this blank
   ![VPN configuration](img/Mac-5-Configuration.png)
1. Click *Create*.
1. The new VPN is now listed on the *VPN* page.  Click the toggle switch to connect the VPN.
   ![VPN List](img/Mac-6-VPN-List.png)

Optionally, you may enable the VPN module in the menu bar to access it more easily:
1. Open *System Settings* > *Menu Bar*.
1. Scroll to the *VPN* menu bar control.
1. Click the toggle switch to display the VPN module in the menu bar.
   ![Show in Menu Bar](img/Mac-7-Show-In-Menu-Bar.png)
1. You can now connect to the VPN from the menu bar.
   ![Connect from Menu Bar](img/Mac-8-Connect-From-Menu-Bar.png)