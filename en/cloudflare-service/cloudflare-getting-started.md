---
title: "Cloudflare: Getting started"
slug: cloudflare-getting-started
---


Aptum is retiring our legacy DNS platform and moving all services to Cloudflare, which offers improved performance and reliability. Your DNS zones \(domain names\) and their records have already been migrated - no DNS data has been lost, and your current DNS service is unaffected while both systems are running.

## Accessing your new portal

If you are the technical lead but did not receive credentials, please coordinate with your account’s primary contact. Your primary contact on file has received an email with access to the Aptum Portal, where your DNS services now live.

If you haven't received it or need access for additional team members, please let us know.

## What you need to do

### Before you begin

-   You must have the login credentials to the Aptum Portal
-   You must have the URL and login credentials for your domain registrar

### About this task

Follow these steps to update your domain registrar and complete the DNS migration. Most updates take 15 to 20 minutes to complete, and up to 24 hours to update globally.

### Procedure

1.  Log in to the Aptum Portal using the access credentials emailed to your primary contact.

2.  From the **Services** menu within the Aptum Portal, select **Cloudflare**. When the **Environments** page appears, select the environment where your domains have been added.

    **Tip:** The name of the migrated environment will be in the format `Imported-YYYY-MM-DD`.

3.  Select a domain with the **Pending name servers** status. Use either the **Likely registrar** feature, or navigate to [lookup.icann.org](http://lookup.icann.org/) to identify your domain registrar.

4.  Locate and note your new name server assignments for each domain in the Aptum Portal.

    These new name server assignments point to the Cloudflare name servers.

5.  In a separate browser tab or window, log into the portal for your domain registrar and locate the name server records for your domain.

6.  Update your the name server records to point to the Cloudflare name servers you noted earlier.

7.  Return to the Aptum Portal, select the **…** icon next to the domain entry to start a name server scan.

    The scan may take up to 24 hours to complete.

8.  You will need to repeat steps 3 through 7 for every domain in the `Imported-YYYY-MM-DD` list.


## We are here to help

The Aptum Customer Care team is available to assist you through this process. Whether you need help finding your new name servers in the portal, guidance on updating records at your registrar, or would like to schedule a call to walk through your specific setup, please don't hesitate to reach out.

Contact us at \[support email\] or \[phone number\]. You can also reference our migration documentation here: \[Link to documentation\].

