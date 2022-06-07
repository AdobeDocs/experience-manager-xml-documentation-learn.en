---
title: Release Notes | Adobe Experience Manager Guides as a Cloud Service, May 2022 release
description: Latest release of Adobe Experience Manager Guides as a Cloud Service
exl-id: 7928a300-5ec9-492c-b9be-02b6f87638c6
---
# Latest release of Adobe Experience Manager Guides as a Cloud Service 

## Upgrade to the latest release

Upgrade your current Adobe Experience Manager Guides as a Cloud Service (later referred as *AEM Guides as a Cloud Service*) setup by performing the following steps:
1. Check out the Cloud Services' Git code and switch to the branch configured in the Cloud Services pipeline corresponding to the environment you want to upgrade.
2. Update `<dox.version>` property in `/dox/dox.installer/pom.xml` file of your Cloud Services Git code to 2022.5.144.
3. Commit the changes and run the Cloud Services pipeline to upgrade to the latest release of AEM Guides as a Cloud Service.

## Compatibility matrix

This section lists the compatibility matrix for the software applications supported by AEM Guides as a Cloud Service May 2022 release. 

### FrameMaker and FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Not compatible | 2020 Update 4 and above |
| | |

*Baseline and conditions created in AEM are supported in FMPS releases starting from 2020.2.

### Oxygen Connector

| AEM Guides as a Cloud Release | Oxygen Connector Windows | Oxygen Connector Mac | 
| --- | --- | --- |
| 2022.5.0 | 2.6.9 | 2.6.9 | 
|  |  |  |  


## New features and enhancements

AEM Guides as a Cloud Service provides many enhancements and new features in the latest release:

### Enhanced Web Editor

* **Create maps based on customized templates** 

Now you get the powerful feature to create customized map templates. You can use them to create DITA maps along with the topic templates and map templates referenced in the map template. 

![dita templates](assets/dita-templates.png)

You can also refer to other map templates and topic templates from the customized map template. The referred map templates can refer to various map templates, topic templates, topics, maps, images, videos, and other assets.

![create dita templates](assets/create-dita-template.png)

The customized map template can help you very easily replicate the map templates and the entire referred folder structure. These customized templates are especially useful to create and recreate multiple maps which have recursive structures and references. 

* The **Insert Keyword** feature has been improved. You can now more easily find a Keyword to be inserted as the keywords are listed in alphabetical order. You can also search keyword(s) by typing a search string in the Search box. 

![insert keyword](assets/insert-keyword.png)

* Now in the Repository View files are loaded in batches. 75 files are loaded at a time. This batch loading is efficient, and you can access the files faster in comparison to loading all the files existing in a folder.

![load more files](assets/load-more-files.png)

* You can render SVG images that include embedded data or links in all XML editor screens including but not limited to Preview and Author view.

* The default XSD/DTD can be updated to the latest version 

### Improved Translation Process

* **Ability to create a scoping translation project**
If you need to create only the scope for a project to be translated, you can select **Create a new scoping translation project**. This will not send the copies for translation and the original translation status of the files is maintained. 
 
![scoping translation project](assets/scoping-translation-project.png)

* If you reject the translation for one or more topics in a translation job, the In Progress translation status of all the rejected topics reverts to their original status. 

* The **Languages** list displays the language folders along with their language codes. For example, French (fr) and German (de).

* The translation feature now also supports the language code which includes both country and language. For example, `fr-fr`, `en-us`. 

![translation languaged](assets/translation-languages.png)

* On loading a DITA map that is outside the language folder, no exception is logged at the backend.

For more details on translation, see *Translate documents from the Web Editor* section in Using Adobe Experience Manager Guides as a Cloud Service.


### Enhanced Publishing

* You can also access the **Publish Dashboard** from the Outputs tab while you generate output from the map dashboard. A list of all active publishing tasks is available in the Publish Dashboard. 

![queued outputs](assets/queued-output.png)

* From the map dashboard you can select multiple DITAVAL files to generate conditionalized content. You can maintain the file order by adding or deleting files. You can also hover over the file name to see the path in the AEM repository where the file is stored. 

* **Deprecated Feature** 
AEM as a Cloud Service no longer supports the generation of DITA output format for FrameMaker documents. This DITA option has also been removed from the Output Presets of the Map dashboard.

### Improved Article-based publishing

XML Editor provides the ability to map more than one product category to an article while publishing to a Salesforce profile.

### Other Feature Enhancements

* The Preview mode also supports `deliveryTarget` conditional processing attribute in DITA. It is available as an option in the drop-down filter along with **audience**, **platform**, **product**, props, **otherprops**. 
* Option has been provided to forcefully sync between the AEM server in Oxygen and the local system.

## Fixed issues

The bugs fixed in various areas are listed below:

* On the Web Editor's review panel, the user is not able to reply to the review comments. (9667)
* Application gets blank on clicking a blank folder after refreshing it via the Options menu. (9639)
* A new version is getting created when we **Save and Close** the checked-in file. (9638)
* Close button is not displayed when **Save as New version** check box is enabled. (9637)
* The correct PDF not published if it is first published via a separate PDF for each chapter and then a single PDF file (Create separate PDF files is unchecked). (9632)
* Map dashboard is throwing metadata issue for non-admin users. (9620)
* Once a baseline is created, the status is set to failed on UI (get status call is failing) if the server is having more than 10000 files. (9608)
* Storing large data in properties results in a publishing error as split publish workflow fails. (9586)
* Conditional Attributes Filters state is not preserved on switching between Preview to Source and again Preview mode. (9553)
* Bookmap name is coming blank in the Repository view in case no name is given via the `mainbooktitle` tag. (9538)
* HTTP 400 error occurs while opening a file uploaded using Oxygen. (9535)
* The Presets of a previously opened map remain visible in Output tab on opening a map with no presets defined. (9523)
* The search functionality for Tags and Attributes is not working in the Outline panel. (9506)
* Newly created Collection is not visible until the browser is refreshed the browser. (9505)
* Conditional Attributes labels (not the values) appear in source mode on adding all the conditions via the "Add all props" option. (9501)
* Files are checked out automatically on reverting to any version. (9482)
* Incorrect timestamp differences are displayed in Assets UI on reverting a file version. (9480)
* Multiple items from search results are added while inserting items in topicref element of DITA map. (9474)
* If the setting **Create New Version for Uploaded File** is ON, a new version is created on reverting and saving on any frozen node. (9473)
* Display text of Key Reference and Content Key Reference is not maintained on changing the link URL, if the display text is not added while defining key reference. (9458)
* In Version History, version number and label are not displayed for the current version. (9446)
* Editor freezes when certain content files are opened in the editor. (9443)
* Search in Repository panel and topicref browse dialog freezes the screen when the content is large. (9432)
* Metadata passed to AEM site output does not honor the baseline of the content. (9416)
* Oxygen checks out an incorrect version of a topic after a version revert in AEM. (9411)
* Failed baseline disables editing in the Preset tab of the map dashboard. (9403)
* Error always gets logged on the creation of new content. (9388)
* Newly created DITA assets are always checked out by another user. (9387)
* Rename element is not working correctly while converting topicref to glossref. (9380)
* Version Label is not coming as dropdown in **Save as New Version** dialog. (9379)
* Conditions are not getting applied on switching between different versions from **Show Diff** dropdown. (9366)
* Multiple issues occur on using Preview filters. (9365)
* Unable to insert non-DITA and DITAVAL assets in topicref. (9363)
* Approved translation does not integrate to the target language when the target language code contains five characters like `fr_ca`. (9357)
* Not able to search files using **Find Files in Folder** from the **More Options** menu and the app becomes unresponsive. (9337)
* Browse dialog hangs if large number of keys are present. (9332)
* DITAVAL files not working while doing article-based publishing. (9330)
* Order of footnotes is incorrect in the AEM Site output. (9327)
* Search is not automatically performed when select path is changed. (9323)
* When the translation is done, an additional version is created for the translated asset. (9310) 
* Unable to delete the Administrator users in the folder profile. (9306)
* Root map updated from Content Key Reference is not set until the page is refreshed. (9302)
* Web Authentication not working in Oxygen. (9296)
* Web links with encoded characters are not working properly. (9227)
* File is not checked out when opened in Oxygen. (9217)
* Refresh checked out files is not working on logging with Web authentication in Oxygen. (9179)
* Translation and Baseline tabs are visible for some time on the Map dashboard. (9146)
* Experience or feature issues occur on reloading Folder Profile. (9103)
* Deleting page layout editor doesn't close it from the center panel in the Author view. (9087)
* Validation error occurs in the Web Editor on removing an image and then saving the new version of the document. (8985)
* Unable to view all the `glossrefs` in the Glossary panel (content specific). (8886)
* `xref` without text is not being displayed in article-based publishing output. (8764)
* References break on moving images or multimedia files which have a space in the file names. (8624)
* References break on choosing `Select All` and moving the multimedia files or DITA content to another folder. (8622)
* Output jobs with status like ‘Waiting’ or ‘Executing’ do not get cleaned up in the Publish Dashboard.  (8569)
* Output purging feature fails if large number of leftover output history nodes are present. (8568)
* DITA Add on package prevents the DAM duplicate asset detection. (8417)
* Create review task button enabled for non-DITA files. (8401)
* Insert references dialog opens on adding subjectref to a map using UI. (8212)
* Unexpected space found in each blank `entry` element when outputclass attribute is added to `tgroup` element. (7532)
* Repository panel doesn't display checked in or checked out file lock icons as soon as the action is completed. (5817)
* Lock icon is displayed in the repository view even when the file is checked in from the editor.  (5756)
* Sites are missing in AEM presets under the Output tab. (9567)
* XML Editor hangs on trying to edit some DITA files. (9537)
* Performing a search in XML Editor causes the page to freeze. (9452) 
* Download map with baseline not working if the content is moved to some other folder. (9331)
* Reupload fails in Oxygen when the file(s) already exist in AEM at the same location. (9328)
* Position of highlighting is incorrect in Side-By-Side view. (9305)
* After check-in of a document from Oxygen to AEM, Japanese content in the document gets replaced by question marks (???). (9276)
* Uploading files from Oxygen to AEM fails. (9157)
* Email notification is not being sent when a review task is being re-assigned in the Inbox. (8376)

## Known issues

Blank page displays intermittently on opening the editor.
