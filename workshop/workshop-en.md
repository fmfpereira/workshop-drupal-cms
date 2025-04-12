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
    - Open VirtualBox and select "Import Appliance".
    - Navigate to the `.ova` file provided on the USB drive and select it.
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