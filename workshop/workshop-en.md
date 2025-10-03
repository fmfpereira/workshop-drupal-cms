# DrupalCMS and AI Workshop

## Prepare the Local Development Environment (Optional)

<details>

<summary>Details</summary>

### Install and Configure DDEV

DDEV simplifies the setup of development environments for web projects. For this workshop, DDEV is pre-installed and configured for the Drupal CMS project. For more information on installing and configuring DDEV, see:

- Installation: [https://ddev.readthedocs.io/en/stable/users/install/ddev-installation](https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/)
- Drupal Quickstart Guide: [https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms](https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms)

### Get and Start the Project

- Clone the workshop repository: [https://gitlab.com/fmfpereira/workshop-drupal-cms](https://gitlab.com/fmfpereira/workshop-drupal-cms "null")
    - Execute the command: `git clone https://gitlab.com/fmfpereira/workshop-drupal-cms.git`
- Start DDEV: `ddev start`
- Install dependencies: `ddev composer install`
- Access the Drupal website via: [https://drupalcms.ddev.site](https://drupalcms.ddev.site "null")

</details>

## Install Drupal CMS

1.  **Access the Drupal website**
    - When visiting the website for the first time, the user will be redirected to the Drupal installation page.
2.  **Configure the Installation**:
    - Select the blog functionality.
    - Define the website name.
    - Create a user and define a secure password.
        - The first user to register will automatically be designated as the site's super administrator.
    - Wait for the installation to complete.

<details>

<summary>Examples</summary>

![Drupal CMS installation screen](images/install.jpg){width=60%}

![Drupal CMS installation in progress.](images/install-running.jpg){width=60%}

</details>

## Add Functionalities with Recipes (Add-ons)

1.  **Explore the Dashboard**:
    - After installation, the Drupal dashboard will be displayed.
2.  **Install Recommended Add-ons**:
    - Select "_Choose recommended add-ons_".
    - Install the following add-ons:
	    - Blog
        - Events
        - Forms
        - News
        - Search
3.  **View New Content**:
    - In the Dashboard, explore the new listings and content entries: blogs, news, events, and contact form.

<details>

<summary>Examples</summary>

![Drupal CMS Dashboard](images/dashboard-install-add-ons.jpg){width=60%}

![Installing add-ons](images/recipes-install.jpg){width=60%}

![Overview of recent content in the Drupal CMS Dashboard](images/dashboard-recent-content.jpg){width=60%}

</details>

## Install and Activate Multilingual Support

### Install the Modules

1.  Navigate to "_Extend_" and then "_List_".
2.  Activate the "_Language_", "_Interface translation_", and "_Content translation_" modules.

### Configure Multilingual Support

The Coffee Module comes pre-installed and allows quick access to any administration page with just a few keystrokes.

1.  **Use the Coffee Module**:
    - Activate Coffee with `Alt + D` (or the corresponding shortcut).
    - Search for "_Languages_" and select the option.
2.  **Install the Portuguese (Portugal) Language**:
    - Add the Portuguese (Portugal) language.
    - Wait for the Drupal translations to download.
3.  **Configure the Language Switcher Block**:
    - Navigate to "_Structure_" and then "_Block layout_".
    - Add the "_Language switcher_" block to the desired region (e.g., Content above).
4.  **Configure the Content Translation Module**:
    - Navigate to "_Configuration_" and then "_Regional and Language_" and then "_Content Language and Translation_".
    - Select "_Content_", select all content types, set as "*Translatable*" and activate the "*Show language selector*" option.

<details>

<summary>Examples</summary>

![Use the Coffee module to quickly find language settings in Drupal.](images/coffee-languages-settings.jpg){width=60%}

![Select new language](images/languages-overview-add-new-language.jpg){width=60%}

![Add a new language](images/add-new-language.jpg){width=60%}

![Translation update message](images/update-translations.jpg){width=60%}

![Link to block management](images/structure-block-layout-link.jpg){width=60%}

![Block overview](images/block-overview-add-block.jpg){width=60%}

![Add language switcher block](images/add-language-switcher-block.jpg){width=60%}

![Link to the content translation module configuration](images/configure-content-translation-link.jpg){width=60%}

![Configure translation by content type](images/enable-content-translation-options-content-type.jpg){width=60%}

![Change the homepage language](images/homepage-select-language.jpg){width=60%}

</details>

## Create Content (Optional)

1.  **Create News, Blog Posts, and Events**:
    - Navigate through the news, blog, and event listings.
    - Create new content.
2.  **Manage Content Options**:
    - Observe the publishing, scheduling, SEO, and authorship options.

By default, when creating new content, a revision is automatically generated. The content is not published immediately, being initially defined as a draft. To publish the content, use the option available in the right sidebar and set the status to "*published*". Additionally, it is possible to customize various content settings, such as:

- Preventing the content from appearing in search results.
- Scheduling the publication and unpublication of the content.
- Modifying the content's URL.
- Changing the author and publication date.

<details>

<summary>Examples</summary>

![Link to the news page via the Drupal CMS Dashboard](images/dashboard-news-page.jpg){width=60%}

![Link to add news in the listing](images/news-overview-new-content.jpg){width=60%}

![Create new news as a draft](images/new-draft-news.jpg){width=60%}

![Publish a news item](images/new-published-news.jpg){width=60%}

</details>

## Translate Content (Optional)

- Edit one of the pages created earlier.
    - If translating the homepage, edit and re-save the English version (there is a bug in Drupal where it is only possible to translate content created before the activation of translations when the original content is re-saved).
- Change the site's language to Portuguese.
- Translate other relevant content and see the result.

<details>

<summary>Examples</summary>

![Link to the option to translate the homepage.](images/translate-homepage-tab.jpg){width=60%}

![Link to add the translation in Portuguese](images/add-translation-operation.jpg){width=60%}

![Translate the homepage.](images/create-translation.jpg){width=60%}

</details>

## Update the Website and Modules

1.  **Activate the Diff Module**:
    - Navigate to "*Extend*" and then "*List*".
    - Activate the "Diff" module.
    - This module is intentionally outdated to demonstrate how to perform an update.
2.  **Update Outdated Modules**:
    - Navigate to "*Extend*" and then "*Update extensions*".
    - Update the "*Diff*" module (and other outdated modules).

<details>

<summary>Examples</summary>

![Activate the diff module](images/enable-diff-module.jpg){width=60%}

![Drupal CMS ready to update the diff module](images/update-ready.jpg){width=60%}

</details>

## Manage Content Revisions (Optional)

1.  **Access the Content List**:
    - Navigate to the "*Content*" section in the left sidebar.
2.  **Edit and Create Revisions**:
    - Edit an existing content and save the changes.
    - View the available revisions in the "*Revisions*" tab.
3.  **Restore Previous Revisions**:
    - Explore the option to restore previous versions of the content.
    - Use the "*Compare Revisions*" function to view the differences.

<details>

<summary>Examples</summary>

![Complete list of content](images/content-overview-news.jpg){width=60%}

![Link to access the content's revisions page](images/node-revisions-link.jpg){width=60%}

![List of content revisions](images/node-revisions-list.jpg){width=60%}

![Difference between revisions](images/revisions-diff.jpg){width=60%}

</details>

## Install AI Support Modules

1.  **Activate the "*AI Assistant*" Recipe**:
    - Navigate to "*Dashboard*"
    - Select "_Choose recommended add-ons_".
    - Install the "*AI Assistant*" add-on.
    - Select the OpenAI provider and add the API key.
    - Ask the chatbot assistant: `What can you do ?`
2. **Add and configure the AI Assistant (Chatbot) block for the default theme**
    - Navigate to "_Structure_" and then "_Block layout_".
    - Add the "_AI DeepChat Chatbot_" block to the Content region.
    - Select "_Drupal CMS Assistant_" as the "_AI Assistant_".
    - On the "_Styling settings_" select the following options:
	    - "_Width_": _400_ 
	    -  "_Height_": _400_ 
	    - "_Placement_": _Bottom right_ 
	- Save
3. **Configure the AI Assistant (Chatbot) block for the admin theme**
    - Navigate to "_Structure_" and then "_Block layout_".
    - Select the "_Gin_" theme.
    - Edit the "_Drupal Agent Chatbot_" block on the Content region.
    - On the "_Styling settings_" select the following options:
	    - "_Width_": _400_ 
	    -  "_Height_": _400_ 
	    - "_Placement_": _Bottom right_ 
	- Save
4.  **Install the Remaining Support Modules**
    - Navigate to "*Extend*" and then "*List*" and enable the following modules:
	    - AI CKEditor integration
	    - AI Translate
	    - AI Agents Explorer
	    - AI Agents Extra
	    - AI Agents Form Integration
	    - AI Audio Field
	    - AI Media Image

<details>

<summary>Examples</summary>

![Start](images/AI/1_Start_AI.png){width=60%}

![Ai Recipe](images/AI/2_AI_Recipe.png){width=60%}

![Config Provider](images/AI/3_Config_Provider.png){width=60%}

![Open Chatbot](images/AI/4_Open_ChatBot.png){width=60%}

![Talk Chatbot](images/AI/5_Talk_ChatBot.png){width=60%}

![AI Agents Installation](images/AI/19_AI_Agents_Installation.png){width=60%}

![Enable AI CKEditor](images/AI/35_Enable_AI_CKEditor.png){width=60%}

![Enable AI Translate](images/AI/36_Enable_AI_Translate.png){width=60%}

![Enable AI Media](images/AI/65_Enable_AI_Media.png){width=60%}

![Enable AI Audio](images/AI/66_Enable_AI_Audio.png){width=60%}

</details>

## Configure AI Support Modules

1.  **List the Available Agents**:
    - Activate Coffee with `Alt + D` (or the corresponding shortcut).
    - Search for "*AI Agent Settings*" and select the option.
    - The list has 10 Agents. You can see the description of each one to know what each one allows you to do. Alternatively, you can also ask the chatbot what each agent does.
2.  **Configure the AI Assistant (Chatbot)**
    - Navigate to "*Configuration*" and then "*AI*" and then "*AI Assistants*".
    - Edit the "*Drupal Agent Assistant*"
    - Activate all the agents that were previously installed.
3.  **Configure the AI Module Defaults.**
    - Navigate to "*Configuration*" and then "*AI*" and then "*AI Default Settings*".
    - In "*Translate text*" set the "*Chat proxy to LLM*" to "*Default provider*" and set "*gpt-4o*" as the "*Default model*".
    - All other supported options will default to OpenAI as the default provider.
4.  **Create the AI Support Vocabularies to be Used in CKEditor.**
    - Before configuring the CKEditor, you need to have 2 vocabularies and their respective terms created: "*Languages*" and "*AI Tones*".
    - Ask the chatbot to create a "*Languages*" vocabulary with the 10 most spoken languages in Europe.
        - `Generate a taxonomy vocabulary named "Languages" with the 20 most spoken languages of European country's`
    - Ask the chatbot to suggest a Vocabulary for "*AI Tone*":
        - `What do you suggest to create a taxonomy vocabulary for "AI Tone"`
    - Confirm the creation and ask to add the terms ***Technical*** and ***Childish***.
        - `Yes, and also add the terms Technical and Childish`
    - Check the creation of the two vocabularies and their terms.
5.  **Configure the CKEditor**
    - Activate Coffee with `Alt + D` (or the corresponding shortcut).
    - Search for "*Text formats and editors*" and select the option.
    - Configure the "*Content*" format.
    - Drag the "*AI Ckeditor*" button from the "*Available buttons*" bar to the "*Active toolbar*".
    - In the AI Tools Plugin settings:
        - Tone:
            - Enabled
            - Choose default vocabulary for tone options: AI Tones
            - AI provider: gpt-4o
        - Fix spelling
            - Enabled
        - Translate:
            - Enabled
            - Choose default vocabulary for translation options: Languages
            - AI provider: gpt-4o
        - Generate with AI:
            - Enabled
            - AI provider: gpt-4o
        - Summarize:
            - Enabled
            - AI provider: gpt-4o

<details>

<summary>Examples</summary>

![Return AI Agents Page](images/AI/20_Return_AI_Agents_Page.png){width=60%}

![AI Agents Settings](images/AI/21_AI_Agents_Settings.png){width=60%}

![AI Assistants](images/AI/22_AI_Assistants.png){width=60%}

![Edit AI Assistant](images/AI/23_Edit_AI_Assistant.png){width=60%}

![Select Agents AI](images/AI/24_Select_Agents_AI_Assistant.png){width=60%}

![AI General](images/AI/25_AI_General.png){width=60%}

![AI Chatbot Conf](images/AI/85_block_layout.png){width=60%}

![AI Chatbot Conf](images/AI/86_block_layout_add_chatbot_settings.png){width=60%}

![AI Chatbot Conf](images/AI/87_chatbot_block_config.png){width=60%}

![AI Chatbot Conf](images/AI/88_block_layout_admin_theme.png){width=60%}

![AI Chatbot Conf](images/AI/89_block_layout_edit_chatbot_settings.png){width=60%}

![AI Chatbot Conf](images/AI/90_chatbot_block_config.png){width=60%}

![Translate Provider](images/AI/52_Translate_Provider.png){width=60%}

![AI Image Bulk](images/AI/38_AI_Image_Bulk.png){width=60%}

![Create Taxonomy European languages](images/AI/39_Create_Taxonomy_European_Languages.png){width=60%}

![Check Taxonomy](images/AI/40_Check_Taxonomy.png){width=60%}

![AI Tone Suggestions](images/AI/41_AI_Tone_Suggestions.png){width=60%}

![Create Tone Taxonomy](images/AI/42_Create_Tone_Taxonomy.png){width=60%}

![Check Tone Taxonomy](images/AI/43_Check_Tone_Taxonomy.png){width=60%}

![Coffee Text Formats](images/AI/44_Coofee_Text_Formats.png){width=60%}

![Text Formats](images/AI/45_Text_formats.png){width=60%}

![Add AI Button Toolbar](images/AI/46_Add_AI_Button_Toolbar.png){width=60%}

![CKEditor AI Tools](images/AI/47_CKEditor_AI_Tools.png){width=60%}

![AI Tone](images/AI/48_AI_Tone.png){width=60%}

![AI Translate](images/AI/49_AI_Translate.png){width=60%}

![AI Generate](images/AI/50_AI_Generate.png){width=60%}

</details>

## Use AI

### Automatically Add Alt Text for an Image

- Navigate to "*Media*" and then "*Add Media*" and then "*Image*".
- Upload an image.
- Select "*Generate with AI*".

<details>

<summary>Examples</summary>

![Add Image](images/AI/30_Add_Image.png){width=60%}

![Image AI Alt Text](images/AI/31_Image_AI_Alt_Text.png){width=60%}

</details>

### Generate text in CKEditor

- Navigate to "*Create*" and then "*News item*".
- In the CKEditor toolbar, select the "*AI Assistant*" button and then the "*Generate with AI*" option.
- In the AI prompt, write:
    - `A text about Festa do Software Livre: its origin, history, and notable communities`.
- Finish by clicking "*Save changes to editor*".
- Select some text and, in the "*AI Assistant*" button, the "*Summarize*" option.
    - Copy and paste the text into "*Description*".
- Select some text and, in the "*Ai Assistant*" button, the "*Tone*" option.
    - Choose any tone from the list. Try the "*Childish*" option. Choose multiple tones and check the text by clicking "*Change the tone*".
    - To finish, click "*Save changes to editor*".
- Once again, select some text, click the "*Ai Assistant*" button and then the "*Translate*" option.
    - Choose a language, click "*Translate*" and finish with "*Save changes to editor*".
    - Write a title and click "*Save*".
- For fixing spell, add some erros by delete some letter on a few words, and select the text.
    - Click the "Ai Assistant" and choose "Fix spelling"
    - Click "Fix spelling" and "Save changes to editor"

<details>

<summary>Examples</summary>

![Create News Item](images/AI/53_Create_news_Item.png){width=60%}

![AI Generate News](images/AI/54_AI_Generate_News.png){width=60%}

![Text Summarize](images/AI/55_Text_Summarize.png){width=60%}

![AI Generate Summary](images/AI/56_AI_Generate_Summary.png){width=60%}

![AI Tone](images/AI/57_AI_Tone.png){width=60%}

![AI Tone Generation](images/AI/58_AI_Tone_Generation.png){width=60%}

![AI Translate](images/AI/59_AI_Translate.png){width=60%}

![AI Translation](images/AI/60_AI_Translation.png){width=60%}

![Title Save](images/AI/61_Title_Save.png){width=60%}

</details>

### Translate content

- In the top right, on the side of the "Edit" button, click the 3 dots and then "*Translate*".
- Click "*Translate using gpt-4o*", wait for the AI's automatic translation, and check the results.

<details>

<summary>Examples</summary>

![AI Translation Option](images/AI/63_AI_Translation_Option.png){width=60%}

</details>

### Add an AI image

- Edit the news.
- Click "*Add Media*".
- In the "*Image Source*" list, select "*Generate Image with AI*".
- In the prompt, write
    - `An image of the Douro River and its iconic bridges`.
- Select the model, the image size, the quality, and the style.
- Click "*Generate Image*" and wait.
    - If you don't like the image, click "*Generate Image*" again and/or refine the prompt.
- If you like the image, click "*Save to media Library*".
- Select the image in the gallery and click "*Insert Selected*".
- Save the news.

<details>

<summary>Examples</summary>

![Content](images/AI/67_Content.png){width=60%}

![Add Media](images/AI/68_Add_Media.png){width=60%}

![Option Generate Image AI](images/AI/69_Option_Generate_Image_AI.png){width=60%}

![AI Image Prompt](images/AI/70_AI_Image_Prompt.png){width=60%}

![AI Image Options](images/AI/71_AI_Image_Options.png){width=60%}

![AI Image Generate](images/AI/72_AI_Image_Generate.png){width=60%}

![Save Image Library](images/AI/73_Save_Image_Library.png){width=60%}

![Image Insert](images/AI/74_Image_Insert.png){width=60%}

![Save with Image](images/AI/75_Save_With_Image.png){width=60%}

</details>

### Activate text-to-speech

- Ask the Drupal agent chatbot to create a new field of type "*AI Audio field*" in the news content type.
    - `Using the AI Audio Field module, create on the News content type, a translatable field called "Transcription"`
- Edit the news.
- Select some text and copy/paste it into the "*Transcription*" field.
- Select a provider, a model, an audio format, and a voice.
- Finish with "*Generate Audio*".
- You can repeat the image and audio procedures for content in another language.

<details>

<summary>Examples</summary>

![Chatbot Ask Create Transcription Field](images/AI/76_Chatbot_Ask_Create_Transcription_Field.png){width=60%}

![Chatbot Create Field](images/AI/77_Chatbot_Create_Field.png){width=60%}

![Edit News Audio](images/AI/78_Edit_News_Audio.png){width=60%}

![Audio Select Text](images/AI/79_Audio_Select_Text.png){width=60%}

![Generate Transcription Audio](images/AI/80_Generate_Transcription_Audio.png){width=60%}

![Audio Generated](images/AI/81_Audio_Generated.png){width=60%}

![Back to Site](images/AI/82_Back_To_Site.png){width=60%}

</details>