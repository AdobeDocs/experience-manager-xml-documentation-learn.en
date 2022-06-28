---
title: Set up custom DITA-OT in [!DNL AEM Guides]
description: Learn how to set up custom DITA-OT in [!DNL Adobe Experience Manager Guides]
role: Admin
---
# Set up custom DITA-OT in [!DNL AEM Guides] for AEM

The steps to add a custom DITA-OT are documented in the section _Use custom DITA-OT plug-ins_ of the _Installation and Configuration Guide_.

On a high level the steps are:

+ Get the basic DITA-OT
  + If you want to obtain copy of out-of-the-box DITA-OT from [!DNL AEM Guides], download it from path `/etc/fmdita/dita_resources/DITA-OT.zip`
  + If you want to obtain a different version then you can download from [dita-ot repo](https://www.dita-ot.org/download)
+ Make changes into DITA-OT like [adding new plugin](https://www.dita-ot.org/dev/topics/plugins-installing.html), or customizing existing plugins (refer example in related links section below)
+ Upload `DITA-OT.zip` received to `/apps/<project-folder>/dita_resources` (create a custom project folder is a recommended approach)
+ Add DITA Profile through **[!UICONTROL Tools]** > **[!UICONTROL Guides]** > **[!UICONTROL DITA Profiles]** (use the DITA-OT path where the custom DITA-OT is uploaded, refer screenshot below)
![DITA Profiles](assets/dita-profile.png)

>[!MORELIKETHIS]
>
>+ [Customizing DITA-OT plugin samples](https://www.dita-ot.org/dev/topics/pdf-customization.html)
