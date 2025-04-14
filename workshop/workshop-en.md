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

## Drupal CMS with AI

### How to install, configure and use AI in Drupal

![Start](images/AI/1_Start_AI.png){width=60%}

Install the "AI Assistant" recipe

![Ai Recipe](images/AI/2_AI_Recipe.png){width=60%}

Select the AI ​​provider, and enter the API Key

![Config Provider](images/AI/3_Config_Provider.png){width=60%}

After installation, the Chatbox appears at the bottom right.

![Open Chatbot](images/AI/4_Open_ChatBot.png){width=60%}

We can then ask `What can you do?` and wait for the answer.

![Talk Chatbot](images/AI/5_Talk_ChatBot.png){width=60%}

Using the ALT+D keys, we can search for **AI** and select AI

![Coffee AI](images/AI/6_Coffee_AI.png){width=60%}

Select "Provider Settings"

![Conf Page](images/AI/7_AI_Conf_Page.png){width=60%}

Here we have a list of AI Providers. Currently only the two installed by default.

![AI Providers Page](images/AI/8_AI_Providers_Page.png){width=60%}

Let's use "Browse Modules" to search for other providers by searching for **AI Provider"

![Extend Search AI Provider](images/AI/9_Extend_Search_AI_Provider.png){width=60%}

In the list you can optionally uninstall "Anthropic Provider" as it is installed by default but not used. Let's install "Ollama Provider".
Ollama allows us to install several AI models on our own PC.

![Install AI provider](images/AI/10_Unninstall_Install_AI_Provider.png){width=60%}

At the moment, most AI modules in Drupal do not have a stable version (alpha or beta) and therefore need to be installed manually, as we will demonstrate. The next steps have already been taken for this workshop, so they are for informational purposes only.

![Error Non Stale Realease](images/AI/11_Error_Non_Stable_Release.png){width=60%}

To do the manual installation, you have to go to [Drupal.org](www.drupal.org/project/ai_provider_ollama), search for the module and copy the installation instructions.

![Ollama Page](images/AI/12_Ollama_Page.png){width=60%}

On the command line, in the project folder, we run DDEV:
`ddev composer requires 'drupal/ai_provider_ollama:^1.0@beta`

![DDEV Install AI Provider](images/AI/13_DDEV_Install_AI_Provider_Ollama.png){width=60%}

After installing the module we can configure it.

![Ollama Provider Installation](images/AI/14_Ollama_Provider_Installation.png){width=60%}

In the configuration we put the address (localhost, server on the local network, docker) and the port.

![Ollama Provider Config](images/AI/15_Ollama_Provider_Config.png){width=60%}

![AI Providers Page](images/AI/16_AI_Providers_Page.png){width=60%}

Let's see the list of AI Agents.

![AI Settings Page](images/AI/17__AI_Settings.png){width=60%}

By default, 3 AI Agents are installed. AI interprets what Agents serve as bridges between the system and the AI ​​model. It converts AI decisions into valid commands for the system. For example, if the AI ​​“decides” that a field needs to be created, the agent knows which endpoint to call or which function to invoke.

![AI Agents Settings Page](images/AI/17_AI_Sgents_Settings_Page.png){width=60%}

We can edit the agents... But I don't recommend it!

![Edit AI Agent](images/AI/18_Edit_AI_Agent.png){width=60%}

Let's install 3 more AI Agents. These are still experimental, but will allow for some more actions.

![AI Agents Installation](images/AI/19_AI_Agents_Installation.png){width=60%}

Using ALT+D, and searching for **Agents** we go to "AI Agent Settings"

![Return AI Agents Page](images/AI/20_Return_AI_Agents_Page.png){width=60%}

We can see that the list now has 6 AI Agents, and we can see the description of each one so we can know what each one allows us to do.

![AI Agents Settings](images/AI/21_AI_Agents_Settings.png){width=60%}

Now let's configure the AI ​​Assistant (Chatbot).

![AI Assistants](images/AI/22_AI_Assistants.png){width=60%}

![Edit AI Assistant](images/AI/23_Edit_AI_Assistant.png){width=60%}

We have to configure the Chatbot to use the agents we installed so that the AI ​​has access to its functionalities.

![Select Agents AI](images/AI/24_Select_Agents_AI_Assistant.png){width=60%}

![AI General](images/AI/25_AI_General.png){width=60%}

![Return AI Conf](images/AI/26__Return_AI_Conf.png){width=60%}

We have the option to configure an AI Provider for each type of action, as we only have one provider the defaults work, except for "Embeddings" which must be configured as indicated.

![AI Settings](images/AI/27__Ai_Settings_1.png){width=60%}

Let's change the "AI Image Alt Text Settings" settings

![Return AI Conf](images/AI/28__Return_AI_Conf.png){width=60%}

Activate the **Autogenerate on upload** option, we still have the "Hide Button" option, but I do not recommend it because if we are not satisfied with the generated Alt Text, we have the button to try again.

![Alt ​​Text Settings](images/AI/29_Alt_Text_Settings.png){width=60%}

Now we can choose one of two options:

1. In the menu - Create - Image
2. In the menu - Media - +Add Media

![Add Image](images/AI/30_Add_Image.png){width=60%}

After uploading the image, an Alt Text must be generated by the AI, if we are not satisfied with the result we have the **Generate with AI** button to try again.

![Image AI Alt Text](images/AI/31_Image_AI_Alt_Text.png){width=60%}

Now let's ask the Chatbot to install a module. `Enable AI Image Bulk Text Module`

![Chatbot Install AI Image Bulk](images/AI/32_Chatbot_Install_AI_Image_Bulk_Alt_Text.png){width=60%}

Let's check if it was installed.

![Extend Confirm Image Bulk](images/AI/33_Extent_Confirm_Image_Bulk.png){width=60%}

Looking for **Bulk** should indicate that it is installed. We will also clear the Chatbot history.

![Chatbot Clear History](images/AI/34_Chatbot_Clear_History.png){width=60%}

Let's take the opportunity to install other modules. **CKEditor AI Integration**

![Enable AI CKEditor](images/AI/35_Enable_AI_CKEditor.png){width=60%}

**AI Translate**

![Enable AI Translate](images/AI/36_Enable_AI_Translate.png){width=60%}

Using **ALt+D** we will search for **Bulk** and select **Bulk Generate Alt Text AI**

![Coffee AI Image Bulk](images/AI/37_Coffee_AI_Image_Bulk.png){width=60%}

This list is empty, but if this were an update to an existing site with hundreds or thousands of images without Alt Text, we could create AI Alt Text for all of them.
We will use Chatbox to create what in Drupal we call **Taxonomies**. They are simple lists that can be used in multiple ways.
Let's ask in Chatbox, `Generate a Taxonomy with tha language of all European country's`

![AI Image Bulk](images/AI/38_AI_Image_Bulk.png){width=60%}

We always need to confirm before the AI ​​does something.

![Create Taxonomy European languages](images/AI/39_Create_Taxonomy_European_Languages.png){width=60%}

A summary of what was done is presented, with a link so we can confirm.

![Check Taxonomy](images/AI/40_Check_Taxonomy.png){width=60%}

Confirmed! Taxonomy created.
Let's create another one, but in a slightly different way. Let's ask: `What do you suggest to create a taxonomy for "AI Tone"`

![AI Tone Suggestions](images/AI/41_AI_Tone_Suggestions.png){width=60%}

The AI ​​makes some suggestions, and we ask you to do what it suggests, adding the terms **Technical** and **Childish**

![Create Tone Taxonomy](images/AI/42_Create_Tone_Taxonomy.png){width=60%}

Done ! Let's confirm.

![Check Tone Taxonomy](images/AI/43_Check_Tone_Taxonomy.png){width=60%}

Imagine how much time they saved! Using **ALT+D**, we will search for **Text** and select **Text Formats and Editors**

![Coffee Text Formats](images/AI/44_Coofee_Text_Formats.png){width=60%}

Drupal has integrated CKEditor, which allows us to create and edit text content in a very intuitive way. Let's configure CKEditor.

![Text Formats](images/AI/45_Text_formats.png){width=60%}

To enable the use of AI when creating/editing content we have to add the respective button and drag it from the **Available buttons** bar to the **Active toolbar**

![Add AI Button Toolbar](images/AI/46_Add_AI_Button_Toolbar.png){width=60%}

When you place the AI ​​button on the **Active Toolbar**, a new option appears in the menu below called **AI Tools**. Let's set up **Tone**

![CKEditor AI Tools](images/AI/47_CKEditor_AI_Tools.png){width=60%}

"AI Tone" refers to the style, attitude, or "voice" an AI adopts when communicating.
So here we will select the taxonomy we created before **AI Tone**, we can define the **Provider** if we have more than one, and activate it in **Enable**

![AI Tone](images/AI/48_AI_Tone.png){width=60%}

Here we select the **European Languages** taxonomy, select **Provider** and activate **Enable**

![AI Translate](images/AI/49_AI_Translate.png){width=60%}

In **Generate with AI** we select **Provider** and activate it in **Enable**
Same for **Summarize** and **Save** at the top right.

![AI Generate](images/AI/50_AI_Generate.png){width=60%}

Go to "AI Default Settings"

![Codde AI Settings](images/AI/51_Coffee_AI_Settings.png){width=60%}

Let's configure **Translate Text** with **Chat Proxy to LLM** provider and **gpt-4o** model.
In the left menu, **Create** - **News Item**

![Translate Provider](images/AI/52_Translate_Provider.png){width=60%}

In the CKEditor bar, we select the **AI Assistant** button, and select the **Generate with AI** option.

![Ceate News Item](images/AI/53_Create_news_Item.png){width=60%}

In the AI ​​prompt, we write `A text about FEUP, in Porto, Portugal. It's origin, history, famous people and events`
Always be specific. And don't be surprised if you get multiple different results when you click **Generate**.
The generated text has not been verified, you should always do this to avoid hallucinations!!
Finish by clicking **Save Changes to Editor**

![AI Generate News](images/AI/54_AI_Generate_News.png){width=60%}

We select some text, and in the **AI Assistant** button the **Summarize** option

![Text Summarize](images/AI/55_Text_Summarize.png){width=60%}

Clicking the **Summarize** button will create a summary of the previously selected text.
Copy text and close window with **X**

![AI Generate Summary](images/AI/56_AI_Generate_Summary.png){width=60%}

Paste the text into **Description**.
Select some text and in the **Ai Assistant** button the **Tone** option

![AI Tone](images/AI/57_AI_Tone.png){width=60%}

Here we can choose any tone from the list. Personally I like the **Childish** option :P
We can choose multiple tones and check the text by clicking on **Change the tone**, to finish **Save changes to editor**

![AI Tone Generation](images/AI/58_AI_Tone_Generation.png){width=60%}

Again selecting some text, **Ai Assistant** button, **Translate** option

![AI Translate](images/AI/59_AI_Translate.png){width=60%}

We can choose a language, click on "Translate", finish with **Save changes to editor**

![AI Translation](images/AI/60_AI_Translation.png){width=60%}

We give it a title, and click **Save**

![Title Save](images/AI/61_Title_Save.png){width=60%}

In the bar click on **Translate**

![Translate Content](images/AI/62_Translate_Content.png){width=60%}

Click on **Translate using gpt-4o**, and wait for the AI ​​to automatically translate

![AI Translation Option](images/AI/63_AI_Translation_Option.png){width=60%}

Let's install some more modules.

![Translated Return Extended](images/AI/64_Translated_Return_Extend.png){width=60%}

Enable **AI Media Image**

![Enable AI Media](images/AI/65_Enable_AI_Media.png){width=60%}

Enable **AI Audio Field**

![Enable AI Audio](images/AI/66_Enable_AI_Audio.png){width=60%}

In the left menu **Content**, and **Edit** the 'News Item' about FEUP in English

![Content](images/AI/67_Content.png){width=60%}

Click **Add Media**

![Add Media](images/AI/68_Add_Media.png){width=60%}

In the **Image Source** list select **Generate Image with AI**

![Option Generate Image AI](images/AI/69_Option_Generate_Image_AI.png){width=60%}

In the prompt write **University event. Inside. With stands.**

![AI Image Prompt](images/AI/70_AI_Image_Prompt.png){width=60%}

Select template, image size, quality and style.

![AI Image Options](images/AI/71_AI_Image_Options.png){width=60%}

Click **Generate Image** and wait.
If the image is not to your liking, you can click **Generate Image** again, and even refine the prompt beforehand.

![AI Image Generate](images/AI/72_AI_Image_Generate.png){width=60%}

If you like the image, click **Save to media Library**

![Save Image Library](images/AI/73_Save_Image_Library.png){width=60%}

Select the image in the gallery, and click **Insert Selected**

![Image Insert](images/AI/74_Image_Insert.png){width=60%}

Let's record the news in **Save (this translation)**
Remembering that after creating the translation of this content, the button changed from **Save** to **Save (this translation)**

![Save with Image](images/AI/75_Save_With_Image.png){width=60%}

The Content Type for news already exists, but we will use the Chatbot to create an additional field in this content type.
Let's be very specific and use the following prompt, `Using the AI ​​​​Audio Field module, create on the News content type, a translatable field called "Transcription"`

![Chatbot Ask Create Transcription Field](images/AI/76_Chatbot_Ask_Create_Transcription_Field.png){width=60%}

The AI ​​lists all the steps to be taken and asks for confirmation.

![Chatbot Create Field](images/AI/77_Chatbot_Create_Field.png){width=60%}

Let's edit the 'news Item' about FEUP in English again.

![Edit News Audio](images/AI/78_Edit_News_Audio.png){width=60%}

We select some text, and scroll....

![Audio Select Text](images/AI/79_Audio_Select_Text.png){width=60%}

Below **Transcript**, we paste the text into the **Text** field.
We select a provider, a model, an audio format, and a voice. Finish with **Generate Audio**

![Generate Transcription Audio](images/AI/80_Generate_Transcription_Audio.png){width=60%}

Listen to the result by clicking play. Fantastic!!
In the sidebar we change the status from **Draft** to **Published** and at the top **Save (this translation)**

![Audio Generated](images/AI/81_Audio_Generated.png){width=60%}

We can repeat the image and audio procedures for content in another language.
See the results by clicking on **Back to Site** at the top left

![Back to Site](images/AI/82_Back_To_Site.png){width=60%}

News in ENG, with text, image and audio file.
Click on the language menu.

![News EN](images/AI/83_News_EN.png){width=60%}

News with image, text and audio file in PT.

![News PT](images/AI/84_News_PT.png){width=60%}
