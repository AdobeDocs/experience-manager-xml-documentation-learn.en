---
title: Spell check and find/replace
description: Using spell check and find/replace in AEM Guides
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
---
# Spell Check and Find/Replace

The AEM Guides Editor has powerful spell check and Find and Replace capabilities.

>[!VIDEO](https://video.tv.adobe.com/v/342768)

Correct a spelling error

1. Locate an error in an open topic, shown with a red underline.

2. Press and hold Ctrl + click the secondary mouse button within the word.

3. Choose the correct spelling from the suggestions.

If the correct spelling is not suggested, you can always manually edit the word. 

## Switch to AEM Spell Check

You may want to use a spell check tool other than the browser’s default dictionary.

1. Navigate to **Editor Settings**.

2. Select the **General** settings tab. 

    ![Spell Check Config](images/lesson-11/configure-dictionary.png)

3. There are two options:

    • **Browser Spell Check** — the default setting where spell check uses the browser’s built-in dictionary.

    • **AEM Spell Check** — use this to build a custom word list using AEM’s custom dictionary. 

4. Choose **AEM Spell Check**.

5. Click [!UICONTROL **Save**].

Configure a custom dictionary

The Administrator can change the settings so that the AEM dictionary recognizes custom words such as company names.

1. Navigate to the **Tools** pane.

2. Log in to **CRXDE Lite**.

    ![AEM UI CRXDE Lite Icon](images/lesson-11/crxde-lite.png)

3. Navigate to the **_/apps/fmdita/config node_**.

    ![CRXDE Lite Config Node](images/lesson-11/config-node.png)


4. Create a new file.

    a. Right-click on the config folder.
    b. Choose **Create > Create File**.
 
    ![New Dictionary File Creation](images/lesson-11/new-dictionary-file.png)


    c. Name the file _**user_dictionary.txt**_.
 
    ![User Dictionary text](images/lesson-11/user-dictionary.png)


    d. Click [!UICONTROL **OK**].

5. Open the file.

6. Add a list of words you want to include in your custom dictionary.

7. Click [!UICONTROL **Save All**].

8. Close the file.

Authors may need to restart their Web Editor session to get the updated custom word list in the AEM Dictionary. 

## Find and Replace in a single file

1. Click the Find and Replace icon on the top toolbar.

    ![Find Replace Icon](images/lesson-11/find-replace-icon.png)

2. In the bottom toolbar, type a word or phrase.

3. Click [!UICONTROL **Find**].

4. If required, type a word to replace the found word.

5. Click [!UICONTROL **Replace**].

## Find and Replace across the Repository

1. Navigate to the **Repository**.

2. Click the [!UICONTROL **Find and Replace**] icon at the bottom left of the screen.

3. Click the [!UICONTROL **Show Settings**] icon.

4. Choose either

    • **Checkout file before replace** — if enabled by an Administrator, the file will be checked out automatically before replacing search terms.

    • **Whole word only** — restricts the search to return only the exact word or phrase entered.

    ![Find Replace in Repository](images/lesson-11/repository-find-replace.png)

 
5. Click the [!UICONTROL **Apply Filter**] icon to select the path in the Repository where you want to perform the search.

6. Enter the terms to Find and Replace.

7. If required, select **Create new version after replace**.

8. Click [!UICONTROL **Find**].

9. Open the desired file and use the arrows to navigate from one found result to the next.
 
    ![Find Replace Navigation UI](images/lesson-11/find-replace-navigation.png)
