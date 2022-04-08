---
title: Create global keys
description: How to create global keys to be used across organization content
role: Admin
exl-id: b8e3a6d2-ea82-4fdb-bd16-3f4b6594af52
---
# Create global keys

Organizations should use keys in cases where they have some resuable and common text, like product name or product pitch, that is used in many places but is prone to change. Using keys for such reusable text allows you to push an update in multiple places by making the change at a single location, such as in the key value.

## Step 1: Create a global map for storing your keys

Create a map and add the [!UICONTROL keyref] element to it.

```

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "technicalContent/dtd/map.dtd">
<mapid="map.ditamap_ffbdbf06-8658-4311-ad84-1c631bba904f">
  <title>global-keys-map</title>
  <keydefkeys="adobe">
    <topicmeta>
      <linktext>Adobe Systems</linktext>
    </topicmeta>
  </keydef>
  <keydefkeys="AEM">
    <topicmeta>
      <linktext>Adobe Experience Manager</linktext>
    </topicmeta>
  </keydef>
</map>

```

Here you have defined two definitions, as shown above, provided a [!UICONTROL keyref] as _AEM_ for the _Adobe Experience Manager_ text.

## Step 2: Add this map to your publication map

```

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE map PUBLIC "-//OASIS//DTD DITA Map//EN" "technicalContent/dtd/map.dtd">
<mapid="map.ditamap_cbf4a96d-e382-4e8c-8830-bcc093fe6638">
  <title>sample-map</title>
  <topicrefhref="sample-topic-using-the-keys.dita"type="topic">
  </topicref>
  <maprefformat="ditamap"href="global-keys-map.ditamap"type="map">
  </mapref>
</map>

```

## Step 3: Use the keys to refer to the variables defined in the global key map

+ Edit the topic and add the key value using the [!UICONTROL keyref].
+ As shown in screenshot, a small window will appear from where keywords can be chosen. This will show when you add the “keyword” element.
![Insert Element](assets/insert_element.png)
![Key Ref](assets/key_ref.png)

```

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE topic PUBLIC "-//OASIS//DTD DITA Topic//EN" "technicalContent/dtd/topic.dtd">
<topicid="topic.dita_31b00e61-04b5-4193-af7a-68503e88b087">
  <title>sample-topic-using-the-keys</title>
  <shortdesc></shortdesc>
  <body>
    <p>This is a sample topic using the keys defined in the global map</p>
    <p>here i am using the key definition for AEM :<keywordkeyref="AEM"></keyword></p>
  </body>
</topic>

```
