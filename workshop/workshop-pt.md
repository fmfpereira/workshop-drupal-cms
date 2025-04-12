# Preparar o Ambiente de Desenvolvimento Local

## O DDEV está instalado no meu host

- Clonar o repositório do workshop: [https://gitlab.com/fmfpereira/workshop-drupal-cms](https://gitlab.com/fmfpereira/workshop-drupal-cms)
    - Executar o comando: `git clone https://gitlab.com/fmfpereira/workshop-drupal-cms.git`
- Iniciar o DDEV: `ddev start`
- Instalar as dependências: `ddev composer install`
- Aceder ao website Drupal através de: [https://drupalcms.ddev.site](https://drupalcms.ddev.site)

## O DDEV não está instalado no meu host

1. **Instalar o VirtualBox**:
    - Descarregar o VirtualBox a partir de: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
    - Executar o instalador e seguir as instruções padrão.
2. **Importar a Aplicação Virtual (OVA)**:
    - Descarregar o ficheiro OVA em https://drive.google.com/drive/folders/1bC3XBcNKhuYoTwvBIyC4aqspNKqmQ8e9
    - Abrir o VirtualBox e selecionar "Importar Aplicação".
    - Selecionar o ficheiro `.ova`.
    - Garantir a seleção da opção "Generate new MAC addresses for all network adapters".
    - Confirmar e aguardar a importação da máquina virtual.
3. **Iniciar a Máquina Virtual**:
    - Selecionar a máquina virtual importada e clicar em "Iniciar".
    - Fazer login com as credenciais padrão: utilizador "drupal" e palavra-passe "drupal".

### Configurar o DDEV (Servidor Local)

O DDEV simplifica a configuração de ambientes de desenvolvimento para projetos web.
Para este workshop, o DDEV já está pré-instalado e configurado para o projeto Drupal CMS.
Para mais informações sobre a instalação e configuração do DDEV, consultar:
- Instalação: [https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/](https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/)
- Guia Rápido Drupal: [https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms](https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms)

**Iniciar o Projeto DDEV**:
- Abrir o terminal/linha de comandos.
- Navegar até a pasta do projeto Drupal CMS: `cd Sites/workshop-drupal-cms/ddev`
- Iniciar o DDEV: `ddev start`
- Abrir o Navegador da máquina virtual.
- Aceder ao website Drupal através de: [https://drupalcms.ddev.site](https://drupalcms.ddev.site)

## Instalar o Drupal CMS

1. **Aceder à Página de Instalação**: [https://drupalcms.ddev.site](https://drupalcms.ddev.site)
    - Ao visitar o website pela primeira vez, seremos redirecionados para a página de instalação do Drupal.
2. **Configurar a Instalação**:
    - Selecionar uma funcionalidade ou avançar o primeiro passo.
    - Definir o nome do website.
    - Criar um utilizador e definir uma palavra-passe segura.
        - O primeiro utilizador a registar-se será automaticamente designado como super administrador do site.
    - Aguardar a conclusão da instalação.

![Ecrã de instalação do Drupal CMS](images/install.jpg){width=60%}

![Instalação do Drupal CMS a decorrer.](images/install-running.jpg){width=60%}

## Adicionar Funcionalidades com Receitas (Add-ons)

1. **Explorar o Dashboard**:
    - Após a instalação, o dashboard do Drupal será exibido.
2. **Instalar Add-ons Recomendados**:
    - Selecionar "*Choose recommended add-ons*".
    - Instalar os seguintes add-ons:
        - Events
        - News
        - Forms
        - Search
        - Blog
3. **Visualizar Novos Conteúdos**:
    - No Dashboard explorar as novas listagens e entradas de conteúdo: blogs, notícias, eventos e formulário de contacto.

![Dashboard do Drupal CMS](images/dashboard-install-add-ons.jpg){width=60%}

![Instalação de add-ons](images/recipes-install.jpg){width=60%}

![Visão geral do conteúdo recente no Dashboard do Drupal CMS](images/dashboard-recent-content.jpg){width=60%}

### Ativar o suporte multilingue

O Módulo Coffee já vem instalado e permite aceder rapidamente a qualquer página de administração com apenas algumas teclas.
1. **Utilizar o Módulo Coffee**:
    - Ativar o Coffee com `Alt + D` (ou atalho correspondente).
    - Pesquisar por "Languages" e selecionar a opção.
2. **Instalar o Idioma Português (Portugal)**:
    - Adicionar o idioma Português (Portugal).
    - Aguardar o download das traduções do Drupal.
3. **Configurar o Bloco de Mudança de Idioma**:
    - Navegar para "Structure" e depois "Block layout".
    - Adicionar o bloco "Language switcher" à região desejada (ex. Content above)
4. **Configurar o Módulo Content Translation**:
    - Navegar para "Configuration" e depois "Regional and Language" e depois "Content Language and Translation".
    - Selecione 'Content', selecione os tipos de conteúdo, defina como 'Translatable' e ative a opção 'Show language selector'.

![Usar o módulo Coffee para encontrar rapidamente as configurações de idioma no Drupal.](images/coffee-languages-settings.jpg){width=60%}

![Selecionar novo idioma](images/languages-overview-add-new-language.jpg){width=60%}

![Adicionar um novo idioma](images/add-new-language.jpg){width=60%}

![Mensagem de atualização de traduções](images/update-translations.jpg){width=60%}

![Link para a gestão de blocos](images/structure-block-layout-link.jpg){width=60%}

![Vista geral de blocos](images/block-overview-add-block.jpg){width=60%}

![Adicionar bloco de alteração de idioma](images/add-language-switcher-block.jpg){width=60%}

![Link para a configuração do módulo de tradução de conteúdo](images/configure-content-translation-link.jpg){width=60%}

![Configurar a tradução por tipo de conteúdo](images/enable-content-translation-options-content-type.jpg){width=60%}

![Alterar o idioma da página inicial](images/homepage-select-language.jpg){width=60%}

## Criar Conteúdo

1. **Criar Notícias, Entradas de Blog e Eventos**:
    - Navegar nas listagens de notícias, blog e eventos.
    - Criar novos conteúdos.
2. **Gerir Opções de Conteúdo**:
    - Observar as opções de publicação, agendamento, SEO e autoria.

Por defeito, ao criar um novo conteúdo, é gerada automaticamente uma revisão. O conteúdo não é publicado de imediato, sendo definido inicialmente como rascunho.
Para publicar o conteúdo, utilize a opção disponível no painel lateral direito e defina o estado como "publicado".
Adicionalmente, é possível personalizar diversas configurações do conteúdo, tais como:
- Impedir que o conteúdo apareça nos resultados de pesquisa.
- Agendar a publicação e despublicação do conteúdo.
- Modificar o URL do conteúdo.
- Alterar o autor e a data de publicação.

![Link para a página de notícias via Dashboard do Drupal CMS](images/dashboard-news-page.jpg){width=60%}

![Link para adicionar notícias na listagem](images/news-overview-new-content.jpg){width=60%}

![Criar nova notícia como rascunho](images/new-draft-news.jpg){width=60%}

![Publicar uma noticia](images/new-published-news.jpg){width=60%}

## Traduzir conteúdo

- Editar uma das páginas criadas anteriormente.
    - Se traduzir a homepage, editar e re-gravar a versão inglesa (existe um bug no Drupal em que só é possível traduzir conteúdo criado antes da ativação das traduções quando o conteúdo original é regravado)
- Mudar o idioma do site para português.
- Traduzir outros conteúdos relevantes e ver o resultado.

![Link para a opção de traduzir a página inicial.](images/translate-homepage-tab.jpg){width=60%}

![Link para adicionar a tradução em Português](images/add-translation-operation.jpg){width=60%}

![Traduzir a página inicial.](images/create-translation.jpg){width=60%}

## Atualizar o Website e Módulos

1. **Ativar o Módulo Diff**:
    - Navegar para "Extend" e depois "List".
    - Ativar o módulo "Diff".
    - Este módulo está propositalmente desatualizado para demonstrar como realizar uma atualização.
2. **Atualizar Módulos Desatualizados**:
    - Navegar para "Extend" e depois "Update extensions".
    - Atualizar o módulo "Diff" (e outros módulos desatualizados).

![Ativar o modulo diff](images/enable-diff-module.jpg){width=60%}

![Drupal CMS preparado para atualizar o módulo diff](images/update-ready.jpg){width=60%}

## Gerir Revisões de Conteúdo

1. **Aceder à Lista de Conteúdo**:
    - Navegar para a secção "Content" na barra lateral esquerda.
2. **Editar e Criar Revisões**:
    - Editar um conteúdo existente e salvar as alterações.
    - Visualizar as revisões disponíveis na aba "Revisions".
3. **Restaurar Revisões Anteriores**:
    - Explorar a opção de restaurar versões anteriores do conteúdo.
    - Utilizar a função "Compare Revisions" para visualizar as diferenças.

![Lista completa de conteúdo](images/content-overview-news.jpg){width=60%}

![Link para aceder à página de revisões do conteúdo](images/node-revisions-link.jpg){width=60%}

![Lista de revisões do conteúdo](images/node-revisions-list.jpg){width=60%}

![Diferença entre as revisões](images/revisions-diff.jpg){width=60%}