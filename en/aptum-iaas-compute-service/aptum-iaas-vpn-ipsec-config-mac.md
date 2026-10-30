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
1. Click on *Options* in the sidebar.
1. Confirm that the toggle for *Send all traffic over VPN connection* is set to **off**.
1. Click on *DNS* in the sidebar.
1. Click on the `+` icon and enter the IP address of one or more valid name servers.  The Google name server at `8.8.8.8` should work.
1. Click *Create*.
1. The new VPN is now listed on the *VPN* page.  Click the toggle switch to connect the VPN.
   ![VPN List](img/Mac-6-VPN-List.png)

#### Configure a route for the VPN traffic

1. Open *Applications* > *Terminal*.
1. Confirm that the VPN you created appears in the list of network services: `sudo networksetup -listallnetworkservices`
1. Add the route to the network configuration: `sudo networksetup -setadditionalroutes "acme-vpn" 10.0.0.0/16 255.255.255.0 ""`
   - Use the network identifier you identified in step 3, e.g. `acme-vpn`.
   - Use the CIDR of your VPC as displayed in Aptum Portal.
   - Be sure to include the empty quotes at the end.
1. Confirm that the route appears in the list of routes: `sudo networksetup -getadditionalroutes "acme-vpn"`
   - Use the network identifier you identified in step 3, e.g. `acme-vpn`.
1. The route is now permanently configured and will persist after a system reboot.


#### Make the VPN available on the menu bar

Optionally, you may enable the VPN module in the menu bar to access it more easily:
1. Open *System Settings* > *Menu Bar*.
1. Scroll to the *VPN* menu bar control.
1. Click the toggle switch to display the VPN module in the menu bar.
   ![Show in Menu Bar](img/Mac-7-Show-In-Menu-Bar.png)
1. You can now connect to the VPN from the menu bar.
   ![Connect from Menu Bar](img/Mac-8-Connect-From-Menu-Bar.png)