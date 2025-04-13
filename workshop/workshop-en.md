# Prepare the Local Development Environment

## DDEV is installed on my host

- Clone the workshop repository: [https://gitlab.com/fmfpereira/workshop-drupal-cms](https://gitlab.com/fmfpereira/workshop-drupal-cms)
  - Execute the command: `git clone https://gitlab.com/fmfpereira/workshop-drupal-cms.git`
- Start DDEV: `ddev start`
- Install dependencies: `ddev composer install`
- Access the Drupal website via: [https://drupalcms.ddev.site](https://drupalcms.ddev.site)

## DDEV is not installed on my host

1. **Install VirtualBox**:
    - Download VirtualBox from: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
    - Run the installer and follow the standard instructions.
2. **Import the Virtual Application (OVA)**:
    - Download the OVA file available [here](https://drive.google.com/drive/folders/1bC3XBcNKhuYoTwvBIyC4aqspNKqmQ8e9)
    - Open VirtualBox and select "Import Appliance".
    - Select the `.ova` file.
    - Ensure the option "Generate new MAC addresses for all network adapters" is selected.
    - Confirm and wait for the virtual machine to import.
3. **Start the Virtual Machine**:
    - Select the imported virtual machine and click "Start".
    - Log in with the default credentials: user "drupal" and password "drupal".

### Configure DDEV (Local Server)

DDEV simplifies the configuration of development environments for web projects.
For this workshop, DDEV is already pre-installed and configured for the Drupal CMS project.
For more information on installing and configuring DDEV, see:

- Installation: [https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/](https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/)
- Drupal Quickstart: [https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms](https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms)

**Start the DDEV Project**:

- Open the terminal/command line.
- Navigate to the Drupal CMS project folder: `cd Sites/workshop-drupal-cms/ddev`
- Start DDEV: `ddev start`
- Open the Virtual Machine's Browser.
- Access the Drupal website via: [https://drupalcms.ddev.site](https://drupalcms.ddev.site)

## Install Drupal CMS

1. **Access the Installation Page**: [https://drupalcms.ddev.site](https://drupalcms.ddev.site)
    - When you visit the website for the first time, you will be redirected to the Drupal installation page.
2. **Configure the Installation**:
    - Select a feature or proceed with the first step.
    - Define the website name.
    - Create a user and set a secure password.
        - The first user to register will automatically be assigned as the site's super administrator.
    - Wait for the installation to complete.

![Drupal CMS installation screen](images/install.jpg){width=60%}

![Drupal CMS installation in progress.](images/install-running.jpg){width=60%}

## Add Features with Recipes (Add-ons)

1. **Explore the Dashboard**:
    - After installation, the Drupal dashboard will be displayed.
2. **Install Recommended Add-ons**:
    - Select "*Choose recommended add-ons*".
    - Install the following add-ons:
        - Events
        - News
        - Forms
        - Search
        - Blog
3. **View New Content**:
    - On the Dashboard, explore the new listings and content entries: blogs, news, events, and contact form.

![Drupal CMS Dashboard](images/dashboard-install-add-ons.jpg){width=60%}

![Installation of add-ons](images/recipes-install.jpg){width=60%}

![Overview of recent content on the Drupal CMS Dashboard](images/dashboard-recent-content.jpg){width=60%}

### Enable multilingual support

The Coffee module comes pre-installed and allows quick access to any administration page with just a few keystrokes.

1. **Use the Coffee Module**:
    - Activate Coffee with `Alt + D` (or the corresponding shortcut).
    - Search for "Languages" and select the option.
2. **Install the Portuguese (Portugal) Language**:
    - Add the Portuguese (Portugal) language.
    - Wait for the Drupal translations to download.
3. **Configure the Language Switcher Block**:
    - Navigate to "Structure" and then "Block layout".
    - Add the "Language switcher" block to the desired region (e.g., Content above).
4. **Configure the Content Translation Module**:
    - Navigate to "Configuration" and then "Regional and Language" and then "Content Language and Translation".
    - Select 'Content', select the content types, set them as 'Translatable', and enable the 'Show language selector' option.

![Use the Coffee module to quickly find language settings in Drupal.](images/coffee-languages-settings.jpg){width=60%}

![Select new language](images/languages-overview-add-new-language.jpg){width=60%}

![Add a new language](images/add-new-language.jpg){width=60%}

![Translation update message](images/update-translations.jpg){width=60%}

![Link to block management](images/structure-block-layout-link.jpg){width=60%}

![Block overview](images/block-overview-add-block.jpg){width=60%}

![Add language switcher block](images/add-language-switcher-block.jpg){width=60%}

![Link to the content translation module configuration](images/configure-content-translation-link.jpg){width=60%}

![Configure translation by content type](images/enable-content-translation-options-content-type.jpg){width=60%}

![Change the language of the homepage](images/homepage-select-language.jpg){width=60%}

## Create Content

1. **Create News, Blog Posts, and Events**:
    - Navigate to the news, blog, and events overviews.
    - Create new content.
2. **Manage Content Options**:
    - Observe the publishing, scheduling, SEO, and authorship options.

By default, when you create new content, a revision is automatically generated. The content is not published immediately and is initially set as a draft.
To publish the content, use the option available in the right sidebar and set the status to "published".
Additionally, you can customize various content settings, such as:

- Preventing content from appearing in search results.
- Scheduling content publication and unpublication.
- Modifying the content URL.
- Changing the author and publication date.

![Link to the news page via the Drupal CMS Dashboard](images/dashboard-news-page.jpg){width=60%}

![Link to add news in the listing](images/news-overview-new-content.jpg){width=60%}

![Create new news as a draft](images/new-draft-news.jpg){width=60%}

![Publish news](images/new-published-news.jpg){width=60%}

## Translate Content

- Edit one of the pages created previously.
  - If translating the homepage, edit and re-save the English version (there is a bug in Drupal where it is only possible to translate content created before the activation of translations when the original content is re-saved).
- Change the site language to Portuguese.
- Translate other relevant content and see the result.

![Link to the option to translate the homepage.](images/translate-homepage-tab.jpg){width=60%}

![Link to add the translation in Portuguese](images/add-translation-operation.jpg){width=60%}

![Translate the homepage.](images/create-translation.jpg){width=60%}

## Update the Website and Modules

1. **Enable the Diff Module**:
    - Navigate to "Extend" and then "List".
    - Enable the "Diff" module.
    - This module is intentionally outdated to demonstrate how to perform an update.
2. **Update Outdated Modules**:
    - Navigate to "Extend" and then "Update extensions".
    - Update the "Diff" module (and other outdated modules).

![Enable the diff module](images/enable-diff-module.jpg){width=60%}

![Drupal CMS ready to update the diff module](images/update-ready.jpg){width=60%}

## Manage Content Revisions

1. **Access the Content List**:
    - Navigate to the "Content" section in the left sidebar.
2. **Edit and Create Revisions**:
    - Edit existing content and save the changes.
    - View the available revisions in the "Revisions" tab.
3. **Restore Previous Revisions**:
    - Explore the option to restore previous versions of the content.
    - Use the "Compare Revisions" function to view the differences.

![Complete content list](images/content-overview-news.jpg){width=60%}

![Link to access the content revisions page](images/node-revisions-link.jpg){width=60%}

![List of content revisions](images/node-revisions-list.jpg){width=60%}

![Difference between revisions](images/revisions-diff.jpg){width=60%}

Aqui está a tradução para inglês, mantendo todo o markdown e os caminhos das imagens intactos:

---

## Drupal CMS with AI

### How to install, configure and use AI in Drupal

![Start](images/AI/1_Start_AI.png){width=60%}  
Install the "AI Assistant" recipe  
![Ai Recipe](images/AI/2_AI_Recipe.png){width=60%}  
Select the AI provider and enter the API Key  
![Config Provider](images/AI/3_Config_Provider.png){width=60%}  
After installation, the Chatbox appears at the bottom right  
![Open Chatbot](images/AI/4_Open_ChatBot.png){width=60%}  
We can then ask **What can you do?** and wait for the response  
![Talk Chatbot](images/AI/5_Talk_ChatBot.png){width=60%}  
Using ALT+D, we can search for **AI** and select AI  
![Coffee AI](images/AI/6_Coffee_AI.png){width=60%}  
Select "Provider Settings"  
![Conf Page](images/AI/7_AI_Conf_Page.png){width=60%}  
Here we have a list of AI Providers. Currently, only the two installed by default.  
![AI Providers Page](images/AI/8_AI_Providers_Page.png){width=60%}  
Let's use "Browse Modules" to search for other providers by searching for **AI Provider**  
![Extend Search AI Provider](images/AI/9_Extend_Search_AI_Provider.png){width=60%}  
In the list, you can optionally uninstall the "Anthropic Provider" since it’s installed by default but not used. We will install the "Ollama Provider".  
Ollama allows us to install various AI models on our own PC.  
![Install AI provider](images/AI/10_Unninstall_Install_AI_Provider.png){width=60%}  
Currently, most AI modules in Drupal are in alpha or beta, so they need to be installed manually, as we will demonstrate. The following steps have already been completed for this workshop and are for informational purposes only.  
![Error Non Stale Realease](images/AI/11_Error_Non_Stable_Release.png){width=60%}  
To install manually, go to [Drupal.org](www.drupal.org/project/ai_provider_ollama), find the module, and copy the installation instructions.  
![Ollama Page](images/AI/12_Ollama_Page.png){width=60%}  
In the project folder, on the command line, run DDEV:  
**ddev composer require 'drupal/ai_provider_ollama:^1.0@beta'**  
![DDEV Install AI Provider](images/AI/13_DDEV_Install_AI_Provider_Ollama.png){width=60%}  
After the module is installed, we can configure it.  
![Ollama Provider Installation](images/AI/14_Ollama_Provider_Installation.png){width=60%}  
In the settings, enter the address (localhost, local network server, docker) and the port.  
![Ollama Provider Config](images/AI/15_Ollama_Provider_Config.png){width=60%}  
![AI Providers Page](images/AI/16_AI_Providers_Page.png){width=60%}  
Let’s view the list of AI Agents.  
![AI Settings Page](images/AI/17__AI_Settings.png){width=60%}  
By default, 3 AI Agents are installed. AI interprets what these agents do — they act as bridges between the system and the AI model. They convert AI decisions into valid system commands. For example, if AI “decides” that a field should be created, the agent knows which endpoint to call or function to invoke.  
![AI Agents Settings Page](images/AI/17_AI_Sgents_Settings_Page.png){width=60%}  
We can edit the agents... But I don’t recommend it!  
![Edit AI Agent](images/AI/18_Edit_AI_Agent.png){width=60%}  
Let’s install 3 more AI Agents. These are still experimental but will enable a few more actions.  
![AI Agents Installation](images/AI/19_AI_Agents_Installation.png){width=60%}  
Using ALT+D, search for **Agents** and go to "AI Agent Settings"  
![Return AI Agents Page](images/AI/20_Return_AI_Agents_Page.png){width=60%}  
We now see 6 AI Agents listed, and we can read their descriptions to understand what each one does.  
![AI Agents Settings](images/AI/21_AI_Agents_Settings.png){width=60%}  
Now let’s configure the AI Assistant (Chatbot).  
![AI Assistants](images/AI/22_AI_Assistants.png){width=60%}  
![Edit AI Assistant](images/AI/23_Edit_AI_Assistant.png){width=60%}  
We need to configure the Chatbot to use the agents we installed so the AI can access their features.  
![Select Agents AI](images/AI/24_Select_Agents_AI_Assistant.png){width=60%}  
![AI General](images/AI/25_AI_General.png){width=60%}  
![Return AI Conf](images/AI/26__Return_AI_Conf.png){width=60%}  
We have the option to configure a different AI Provider for each action type. Since we only have one, the defaults work, except for "Embeddings," which needs to be configured as shown.  
![AI Settings](images/AI/27__Ai_Settings_1.png){width=60%}  
Let’s update the "AI Image Alt Text Settings"  
![Return AI Conf](images/AI/28__Return_AI_Conf.png){width=60%}  
Enable the **Autogenerate on upload** option. There’s also a "Hide Button" option, but I don’t recommend it — if you're not satisfied with the generated Alt Text, the button lets you try again.  
![Alt Text Settings](images/AI/29_Alt_Text_Settings.png){width=60%}  
Now we can choose one of two options:

1. From the menu - Create - Image  
2. From the menu - Media - +Add Media  
![Add Image](images/AI/30_Add_Image.png){width=60%}  
After uploading the image, Alt Text should be generated by AI. If you're not happy with it, you can click "Generate with AI" to try again.  
![Image AI Alt Text](images/AI/31_Image_AI_Alt_Text.png){width=60%}  
Now let’s ask the Chatbot to install a module: **Enable AI Image Bulk Text Module**  
![Chatbot Install AI Image Bulk](images/AI/32_Chatbot_Install_AI_Image_Bulk_Alt_Text.png){width=60%}  
Let’s verify the installation.  
![Extend Confirm Image Bulk](images/AI/33_Extent_Confirm_Image_Bulk.png){width=60%}  
Searching for **Bulk** should show it’s installed. Let’s also clear the Chatbot history.  
![Chatbot Clear History](images/AI/34_Chatbot_Clear_History.png){width=60%}  
Let’s install more modules: **AI CKEditor Integration**  
![Enable AI CKEditor](images/AI/35_Enable_AI_CKEditor.png){width=60%}  
**AI Translate**  
![Enable AI Translate](images/AI/36_Enable_AI_Translate.png){width=60%}  
Using **ALT+D**, search for **Bulk** and select **Bulk Generate Alt Text AI**  
![Coffe AI Image Bulk](images/AI/37_Coffee_AI_Image_Bulk.png){width=60%}  
This list is empty, but if this were an update to a live site with hundreds or thousands of images lacking Alt Text, we could use AI to generate it for all of them.  
Now let’s use the Chatbox to create what Drupal calls **Taxonomies** — simple lists that can be used in various ways.  
Let’s ask the Chatbox: **Generate a Taxonomy with the language of all European countries**  
![AI Image Bulk](images/AI/38_AI_Image_Bulk.png){width=60%}  
We always need to confirm before AI performs an action.  
![Create Taxonomy European languages](images/AI/39_Create_Taxonomy_European_Languages.png){width=60%}  
A summary of what was done is presented, with a link to confirm.  
![Check Taxonomy](images/AI/40_Check_Taxonomy.png){width=60%}  
Confirmed! Taxonomy created.  
Let’s create another one, but slightly differently. Ask: **What do you suggest to create a taxonomy for "AI Tone"**  
![AI Tone Suggestions](images/AI/41_AI_Tone_Suggestions.png){width=60%}  
AI gives some suggestions, and we ask it to proceed, adding the terms **Technical** and **Childish**  
![Create Tone Taxonomy](images/AI/42_Create_Tone_Taxonomy.png){width=60%}  
Done! Let’s confirm.  
![Check Tone Taxonomy](images/AI/43_Check_Tone_Taxonomy.png){width=60%}  
Imagine how much time you saved! Using **ALT+D**, search for **Text** and select **Text formats and editors**  
![Coffee Text Formats](images/AI/44_Coofee_Text_Formats.png){width=60%}  
Drupal integrates CKEditor, allowing intuitive text content creation and editing. Let’s configure CKEditor.  
![Text Formats](images/AI/45_Text_formats.png){width=60%}  
To enable AI when creating/editing content, we need to add the respective button and drag it from **Available buttons** to the **Active toolbar**  
![Add AI Button Toolbar](images/AI/46_Add_AI_Button_Toolbar.png){width=60%}  
Placing the AI button in the **Active Toolbar** reveals a new option below called **AI Tools**. Let’s configure the **Tone**  
![CKEditor AI Tools](images/AI/47_CKEditor_AI_Tools.png){width=60%}  
"AI Tone" refers to the style, attitude, or "voice" AI adopts when communicating.  
So here we select the taxonomy we previously created: **AI Tone**. We can define the **Provider** if more than one exists, and enable it under **Enable**  
![AI Tone](images/AI/48_AI_Tone.png){width=60%}  
Here we select the taxonomy **European Languages**, the **Provider**, and enable it under **Enable**  
![AI Translate](images/AI/49_AI_Translate.png){width=60%}  
Under **Generate with AI**, we select the **Provider** and enable it  
Same for **Summarize**, and click **Save** at the top right.  
![AI Generate](images/AI/50_AI_Generate.png){width=60%}
