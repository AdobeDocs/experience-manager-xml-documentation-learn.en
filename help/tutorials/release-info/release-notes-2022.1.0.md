---
title: Release Notes for [!DNL AEM Guides], January 2022 release
description: January release of [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: b2da77fa-f17c-440b-be59-acaafcd9a57c
---
# January release of [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Upgrade to the January release

Upgrade your current [!DNL Adobe Experience Manager Guides] as a Cloud Service (later referred as [!DNL AEM Guides] as a Cloud Service) setup by performing the following steps:
1. Check out the Cloud Services' Git code and switch to the branch configured in the Cloud Services pipeline corresponding to the environment you want to upgrade.
2. Update `<dox.version>` property in `/dox/dox.installer/pom.xml` file of your Cloud Services Git code to 2022.1.78.
3. Commit the changes and run the Cloud Services pipeline to upgrade to the January release of [!DNL AEM Guides] as a Cloud Service.

## Compatibility matrix

This section lists the compatibility matrix for the software applications supported by [!DNL AEM Guides] as a Cloud Service January 2022 release. 

### FrameMaker and FrameMaker Publishing Server

| FMPS | FrameMaker |
| --- | --- |
| Not compatible | 2020 Update 4 and above |
| | |


### Oxygen Connector

| [!DNL AEM Guides] Cloud Release | Oxygen Connector Windows | Oxygen Connector Mac | Edit in Oxygen Windows | Edit in Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.1.0 | 2.4.0 | 2.4.0 | 2.2 | 2.2 |
|  |  |  |  |  |


## New features and enhancements

### Article-based publishing

With January release, we have introduced an article-based publishing feature integrated within the Web Editor. You can use the article-based publishing feature to incrementally generate output of one or more topics or publish your content to a knowledgebase platform.

This feature allows the users to build the DITA map in an additive fashion and publish topics as and when they are ready. Once you have published your map, use the article-based publishing feature to achieve incremental publishing for the updated articles only.

![Article-based publishing](assets/article-based-publishing.png)

In addition to AEM, you can use this unique feature to publish your articles to any knowledgebase portals such as Salesforce. This feature also comes with an OOTB content template, built on top of AEM core components, which lets you create a knowledge-based repository of the technical content. What’s great about this template is that it is completely customizable to suit your organizational requirements and can also support use cases like corporate intranet portals.
You can also filter the articles based on their document state and modified time. 

This on-the-go need-based article publishing not only gives you complete control on your content publishing, but also reduces the overall time to publish your updated content.
As you publish your articles using this template, it can also pass on the metadata to your published pages.
For more details, see *Article-based publishing from the Web Editor* in the User Guide.

### Improved Web Editor

There are a lot of enhancements and new features that are introduced in the Web Editor:

* Support for subject scheme has also been added in the Web Editor. You can now create and use subject scheme using the Subject Scheme panel. With the addition of subject scheme, you can now use own corporate metadata and taxonomy.

![Subject scheme](assets/subject-scheme-panel.png)

* A new glossary hotspot tool has been introduced in this version to manage glossaries in bulk. Using this tool, you can quickly convert text to glossary and glossary to terms in bulk for a selected map or open topics. 

![Glossary hotspot](assets/glossary-hotspot-tool.png)

* Added refresh functionality in Reusable Content panel that allows you to quickly refresh the reusable content in reference files.
* New working copy indicator shows you whether your current (working copy) of file is in sync with the saved version or not.

![Version indicator](assets/version-update-indicator.png)

* Search filter in the Repository Panel and file browse dialog has been enhanced to give more filtering options, which can be further customized.

![Search filters in repository](assets/repository-filter-search.png)

* You can now upload .docx files from the Web Editor.

### Author with FrameMaker

Now you can author and publish your documents in FrameMaker. FrameMaker ships with an out-of-the-box connector to Adobe Experience Manager. In FrameMaker you get an easy-to-use interface that allows you to maintain versions of your documents in a distributed and collaborative environment. 

Once you have created your content, FrameMaker allows you to publish your documents in different formats - PDF, HTML5, EPUB, and DITA. You can also perform the various file management operations like checkout, checkout with dependents, check-in, refresh, and so on. 
To author with FrameMaker  in [!DNL AEM Guides] as a Cloud Service use FrameMaker version 2020.4 and above.

### New translation dashboard

A new translation dashboard has been introduced in the Web Editor with the following features:

* Sorting, searching, and filtering of topics list.
* Filter content by reference type - direct or indirect references.
* Easy navigation to find an existing project while initiating a translation request.
* Introduced a multi-language translation mechanism to avoid creating multiple projects for each language when translation request is initiated for more than one language.
* Introduced a configuration to hide the translation tab in map dashboard. By default, it is visible. You can choose to translate content using either the map dashboard or the Web Editor.

![Translation dashboard](assets/translation-from-web-editor.png)

### Enhanced publishing

* Authors can now pass map- and topic-level metadata to DITA-OT publishing. This is helpful when custom PDF templates are designed to use file metadata properties like tags, author, document state, and more.

![DITA-OT metadata](assets/custom-meta-data-output-preset.png)

* A new configuration has been added to allow users to retain or delete the versions of the topics being deleted when **Delete and Create** option is used in the AEM Site output generation.

### Improved file handling

The following improvements can now be seen while working with files in AEM Assets:
* A new file upload experience and a new dialog for choosing a conflict resolution strategy has been introduced.

![File upload conflict](assets/file-upload-name-conflict.png)

* Ability to create a new version of uploaded file with an ability to prevent overwriting a checked-out file.
* Now you can see a preview of images directly from the Version History view. Also, for DITA and non-DITA files, Version History shows the current version information separately.  

![Version history thumbnail](assets/version-history-preview-image.png)

* Whenever the user creates a DITA file, the default filename appears in small casing to be inline with Native AEM folder creation scenario. 

### New report export feature

Reports are very useful in identifying the health of your content. [!DNL AEM Guides] as a Cloud Service provides various reports to take control of your content. Now, you can not only view the reports, but also export the report data in a CSV file to view and share with your larger team. Report data can give you a quick glance of any broken links or missing images.

![Report export](assets/export-report.png)

### Improved Oxygen DAM refresh experience

When you refresh files from AEM Server in Oxygen, a warning message is displayed if you have unsaved files in your current Oxygen session. You can choose to cancel the refresh operation to save any unsaved files. Without this feature, users were losing any unsaved information in their documents. 


### Other feature enhancements

* You can now create a new **Dita Project** template under the **/apps/projects/templates** path.
* Now download the default **ui_config.json** file from your folder profiles. This can be used to merge custom changes from the existing **ui_config.json** file while upgrading.
* You do not need to clear the browser cache even when new versions of JS files are present.

## Fixed issues

The bugs fixed in various areas are listed below:

### Web Editor

* Conrefs appear in red color even when they are not broken. (8239)
* Value for conditional attribute is not auto populated when Add All Properties is selected in the DITAVAL editor. (8234)
* Authors are unable to insert an image in a topic using relative path. (8112)
* Review task page not showing the multimedia files if spaces are present in the file name. (8111)
* Ph conref added in table cell are displayed in red color. (8083)
* Links in review task will not get updated when the files under review are moved. (8080)
* Web Editor does not correctly render images that have scaling property set to 75% or higher. (8073)
* GIF images are rendered as static images in the Web Editor. (8024)
* A conkeyref in a note element is not displayed in the Web Editor preview or in the output. (8006)
* xref to an element that itself is a conref is not resolved in the editor. (7933)
* Title having key is not rendered correctly in the editor preview and the Repository panel. (7909)
* Snippets with special characters are not stored correctly. (7908)
* Saving a topic after formatting MathML equations results in an error. (7954)
* keydef having (tm) are not rendered properly in the editor and the AEM site output contained duplicate TM symbols. (7859)
* Dragging and dropping a snippet does not work as per the DTDs. (7758)
* HTML is ignoring custom defined dimensions for graphics. (7718)
* conrefend attribute does not update when the source file is moved. (7698)
* Working with Reference topic type documents leads to several UI issues. (7656)
* DITAVAL files are not shown when author adds ditavalref in a map. (7594)
* Unexpected space is found in each blank `<entry>` element when outputclass attribute is added to `<tgroup>` element. (7532)
* Source button does not work for topics opened via map dashboard. (7465)
* Pretty print inserts blank lines and spaces that can be seen when the file is opened in FrameMaker or Oxygen. (7408)
* Maps with href="/" in any of the topics do not publish on AEM sites. (7405)
* Performance issues found in the editor when the root map has large number of keydefs. (7400)
* Document state for a map with custom template is not getting inherited from its corresponding states profile. (7359)
* `<tm>` element incorrectly rendered as a block element. (7286)
* Duplicate templates are displayed in editor templates panel when a new template is created. (5814)
* Templates defined in ui_config for images for setting additional attribute is not applicable for drag/drop cases. (5713)
* Incorrect default appearance of uicontrol in menucascade. (5483)
* Custom templates for Topic/Map do not show new name in the UI. It shows the name as "Topic"/"Map" rather than showing the configured name. (4958)
* Ability to clear rootmap from the user preferences settings. (8534)
* A newly created map collection is not listed, even after refreshing the page.(8603)
* Unlocked topic cannot be closed. (8545)
* Switching between source and author mode marks the topic as dirty and requires the content to be saved again.(8524)
* Reuse content panel crashes on searching special characters `[` or `*` .(8279)
* Cursor is not displayed in search bar when insert element dialog is opened using the keyboard shortcut Alt+Enter.(7912)
* Search option only searches in file names and not in content. (7784)


### Oxygen Connector

* Files whose parent folder has special characters give error while loading in Oxygen. (8054)
* When a newly created document is opened in Oxygen, it throws "Cannot find GUID" error. (7856)
* Check-in option is disabled after the file is checked-out from AEM using Edit in Oxygen. (7471)


### Review

* Real time synchronization is not working for comments. (7661)

### Map dashboard

* Unable to see conref content in title of a topic in map dashboard's topics or reports tab. (8263)
* AEM Sites Output | jcr:title of the generated site page does not update when DITA topic title is updated. (8131)
* Download MAP does not download the video files used inside the topics. (8070)
* Media files are not downloading when the object Tag is used through the download bookmap API. (8057)
* Incorrect report is shown in Reports tab if any topic has conref to file whose title starts with conref. (4698)
* Apply Labels dialog on the Baseline tab does not display labels in dropdown. (8455)

### Publishing

* PDF creation fails for the first time when Enable Versioning is selected. (8053, 8294)
* White-space character is auto-added after a 'tm; tag in AEM Site output. (7964)
* Unable to view YouTube videos in AEM Site output. (7401)
* Filter by label fails for referenced content after the user clicks on browse all topics in the baseline tab of map dashboard. (7388) 
* Publishing topic with element `<tm>` having property value SM or reg is displayed incorrectly in generated output. (7239)
* Baseline publishing with image is not picking the image's latest version in published output. (7231)
* Relatable referenced topics is shown in baseline tab. (5424)
* Incremental publish for a topic with conkeyref in its title does not work as expected. (4474)
* Page title is not used for output URL generation even though that setting is checked. (8257)
* Baseline publishing picking the current version of the images instead of the frozen node. This is also seen if an image has space or special characters in the file name. (8274, 8322)
* Incremental publish fails for DITA map with type subject scheme having mapref. (8218)
* Null gets added whenever a map is added to Bulk Publish Dashboard. (8695)
* On using baseline publishing with image as conref in the topic, the image is not published in the output. (8564)
* Publishing fails with an exception if baseline used in AEM site publishing is deleted. (8572)
* Topic regeneration is not working. (8091)
* Issues exist with publishing footnotes in tables. (4709)

### AEM Assets

* Performance issues found while performing selection/deletion on huge content set in Assets UI. (8238)
* Saved search feature (smart collection) breaks if DITA Predicate is added to Search filters. (8048)
* Reverting image to older version does not work. (DXML-7903)
* Delete option is also visible for authors who do not have permission for delete. (7322)
* CCMS overlay for Assets Editor breaks rendering of Delete option. (8093)
* Document profile is not getting deleted. (8604)
* References break on performing "Select All" and moving the multimedia/Dita_Content to some other folder. (8621)
* Incorrect references  occur in source on moving the assets. (8627)
* Fixed list view doesn’t get loaded. (8542)

### Content import

* HTML to DITA conversion | Table with 'tr' having empty 'td' entries causes additional rows in output. (8132)
* HTML to DITA conversion | HTML having a table with multiple tbody fails with exception. (7940)
* HTML to DITA conversion | errors out if source HTML has comments. (7937)
* Importing DITA 1.3 DITA files causes some href to transform into malformed links. (8019)

## Known issues

Adobe has identified the following known issues for [!DNL AEM Guides] as a Cloud Service January 2022 release. 


### Known issues with workaround

Use the given workaround for the following known issues:

* The web authentication is not working for the Oxygen connector on Mac.
**Workaround**: Use the Oxygen connector on Windows for now.

* In the Firefox browser, the review comments cannot be imported without opening the side-by-side view.
**Workaround**: Use the Chrome browser for now.

* References break on moving the images or multimedia files that have space(s) in the file names.
**Workaround**: Rename the file and remove the spaces from the file name before moving them.

* The map dashboard does not load intermittently in the latest version of the Chrome browser.
**Workaround**: Refresh the map dashboard page.

### Other known issues

* If Oxygen is connected with [!DNL AEM Guides] solution using web authentication, then logout fails.
* Review tasks cannot be reassigned to the users.
* Issues are present in the Map collection UI like the text is distorted and **Select All** functionality is not working correctly.
