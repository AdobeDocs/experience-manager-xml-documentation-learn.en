---
title: AEM Guides releases
description: Latest AEM Guides releases and pre-requisite AEM versions
exl-id: 780697a9-bdc6-40c2-b258-64639fe30f88
---
# [!DNL AEM Guides] Releases

[!DNL Adobe Experience Manager Guides] is an application deployed onto AEM. It is a powerful, enterprise-grade component content management solution (CCMS) which enables native DITA support in Adobe Experience Manager, empowering AEM to handle DITA-based content creation and delivery. 

## UUID vs Non-UUID Explained

[!DNL AEM Guides] packages are available in two modes - UUID build and non-UUID builds.

Customers will need to decide between UUID and non-UUID mode at the time of first setup (please connect with your Customer Success Manager to help you make the decision based on your usecase).

When upgrading from one version of [!DNL AEM Guides] to a newer version, customers will need to ensure they pick the same mode (UUID / non-UUID) to match their existing mode. A non-UUID build should not be directly upgrade to a UUID build. Moving from non-UUID build to UUID build would need content migration. 

**Upgrading Builds**

When you are upgrading from an older version to a newer version of [!DNL AEM Guides], you might need to execute some migration scripts. Refer to Release Notes and version specific documentation for upgrade instructions.

Not all upgrade paths are directly supported. For example, direct upgrade to version 4.0 is possible only from version 3.8. 
If you are on a version prior to 3.8, then refer to your version-specific documentation for upgrade instructions [Help Archive](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).
Please reach out to your customer success manager to validate the upgrade path. 

**[!DNL AEM Guides] Builds**

The following list contains the latest [!DNL AEM Guides] packages available for installation on AMS or On-Prem, corresponding AEM versions (pre-requisites), download links of packages, and other helpful information. It is recommended to only use the latest build of [!DNL AEM Guides]. If for some reason, you need access to older builds, please connect with your account's Customer Success Manager.

>[!NOTE]
>
>Reach out to your Customer Success Manager for access to [!DNL AEM Guides] builds for AEM as a Cloud Service.

| [!DNL AEM Guides] Release  | Release Notes  |   AEM Pre-requisite |   Build Download Links |
|---|---|---|---|
| **AEM Guides 4.0**  |  [4.0.x Release Notes](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html) | **Non-UUID and UUID 4.0.3**<br> AEM 6.5 SP12, SP11, SP10, or SP9 <br>Java: 11 or 8 <br><br> <br>**Non-UUID and UUID 4.0.2** <br> AEM 6.5 SP12, SP11, SP10, or SP9 <br>Java: 11 or 8 <br><br> **Non-UUID and UUID 4.0** <br> AEM 6.5 SP11, SP10 or SP9 | **Non-UUID**: <br> **AEM 6.5** <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-hotfix-4.0.3.1.zip)<br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.0.2.10.zip)  <br> [4.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-non-uuid/com.adobe.fmdita-6.5-4.0.70.zip)  <br><br> **UUID** <br>**AEM 6.5**  <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-hotfix-4.0.3.1.zip) <br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.0.2.10.zip)<br> [4.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-uuid/com.adobe.fmdita-6.5-uuid-4.0.70.zip) |
| **AEM Guides 3.8.5** <br> 3.8.5 is a SP release on top of 3.8. <br>3.8 release must not be installed standalone as 3.8.5 SP contains a critical fix. <br>Customers must first install 3.8 and then SP 3.8.5. |  [3.8.x Release Notes](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-3-8.html) |  **Non-UUID** <br> AEM 6.5 SP9 or SP8 <br> AEM 6.4 SP8 <br> AEM 6.3 SP3 <br><br> **UUID** <br> AEM 6.5 SP9 or SP8 | **Non-UUID**: <br> **AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.5-hotfix-3.8.5.2.zip) <br>[3.8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.5-3.8.166.zip)<br> **AEM 6.4** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.4-hotfix-3.8.5.1.zip) <br>[3.8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.4-3.8.166.zip) <br> **AEM 6.3** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.3-hotfix-3.8.5.1.zip) <br>[3.8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.3-3.8.166.zip) <br><br> **UUID** <br>**AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5uuid/com.adobe.fmdita.uuid-6.5-hotfix-3.8.5.2.zip) <br> [3.8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8uuid/com.adobe.fmdita.uuid-6.5-3.8.168.zip)|
