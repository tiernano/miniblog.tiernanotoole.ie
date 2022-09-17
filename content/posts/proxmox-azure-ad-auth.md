---
title: Proxmox auth with Azure AD
Date: 2022-09-17T23:00:00+00:00
tags: ["homelab", "100daysofhomelab", "Tutorials"]
---
I use [Office365](https://geni.us/iRLLz) for email and other bits and pieces, and I have Azure AD included. While digging around the [Proxmox](https://proxmox.com/en/) interface, I found the option of authenticating Proxmox with Azure AD. So, how do you do it? 

First, go to [portal.azure.com](https://portal.azure.com) and login. To the Azure AD section and, assuming you have an Azure AD setup, select App Registration in the side bar and select New Registration.

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.24.10.png)

Next Enter a name for your proxmox application, make sure Accounts in this org directory is selected and enter the url of your proxmox server. Make sure application type is set to Web:

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.26.10.png)

Click Register, and on the next page, select Certificates & secrets. Click new client secret:

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.26.50.png)

Enter a name and a expiry date.

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.27.05.png)

you will need to take note of the value of the secret.

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.27.19.png)

Back under overview, take note of the Application (client) ID and then click Endpoints.

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.28.46.png)

take the URL from the OpenID Connect section, removing the /.well-known/openid-configuration part. The url should look like:

`https://login.microsoftonline.com/<yourid>/v2.0`

Next, login to your Proxmox server, and under data center, select Realms. Select add and Open ID Connect.

![](https://res.cloudinary.com/tiernanotoole/w_400,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.42.56.png)

Issuer URL is the URL from the Endpoints. Set the Realm name as you want, enter the Client ID and Key and tick the box for Auto Create Users and Default. Then hit add.

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.40.25.png)

Log out, and login with the new Realm. It will redirect you to the Azure Ad login, ask do you approve (if already logged in) and then redirects you back. At this stage, you cant see anything...

Log back out and in as your default admin user, click the Permissions section and click add:

![](https://res.cloudinary.com/tiernanotoole/w_600,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.46.09.png)

Select User Permissions

![](https://res.cloudinary.com/tiernanotoole/w_400,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.46.20.png)

find you user and give them the required access.

![](https://res.cloudinary.com/tiernanotoole/w_400,c_scale,f_auto,q_auto,dpr_auto/miniblog/Screenshot_2022-09-17_at_23.46.34.png)]

Log out, select Azure AD and log back in as your user, and heay presto, you are now in will full admin access! Happy Days!