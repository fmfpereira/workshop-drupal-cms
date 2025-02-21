## Preparar o Ambiente de Desenvolvimento Local

1. **Instalar o VirtualBox**:
    
    - Descarregar o VirtualBox a partir de: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
    - Executar o instalador e seguir as instruções padrão.
2. **Importar a Aplicação Virtual (OVA)**:
    
    - Abrir o VirtualBox e selecionar "Importar Aplicação".
    - Navegar até o ficheiro `.ova` fornecido na pen USB e selecionar.
    - Garantir a seleção da opção "Generate new MAC addresses for all network adapters".
    - Confirmar e aguardar a importação da máquina virtual.
3. **Iniciar a Máquina Virtual**:
    
    - Selecionar a máquina virtual importada e clicar em "Iniciar".
    - Fazer login com as credenciais padrão: utilizador "ectl" e palavra-passe "ectl".

### Configurar o DDEV (Servidor Local)

O DDEV simplifica a configuração de ambientes de desenvolvimento para projetos web.
Para este workshop, o DDEV já está pré-instalado e configurado para o projeto Drupal CMS.
Para mais informações sobre a instalação e configuração do DDEV, consultar:
- Instalação: [https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/](https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/)
- Guia Rápido Drupal: [https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms](https://ddev.readthedocs.io/en/latest/users/quickstart/#drupal-drupal-cms)

**Iniciar o Projeto DDEV**:
    
- Abrir o terminal/linha de comandos.
- Navegar até a pasta do projeto Drupal CMS: `cd Sites/drupalcms`
- Iniciar o DDEV: `ddev start`
- Abrir o Navegador da maquina virtual.
- Aceder o website Drupal através de: [https://drupal-cms.ddev.site](https://drupal-cms.ddev.site)

## Instalar o Drupal CMS

1. **Aceder à Página de Instalação**: https://drupal-cms.ddev.site
    - Ao visitar o website pela primeira vez, seremos redirecionados para a página de instalação do Drupal.
2. **Configurar a Instalação**:
    - Selecionar a opção "Blog".
    - Definir o nome do website.
    - Criar um utilizador e definir uma palavra-passe segura.
	    - O primeiro utlizador registado será o super administrador do site.
    - Aguardar a conclusão da instalação.

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
3. **Visualizar Novos Conteúdos**:
    - No Dashboard explorar as novas listagens e entradas de conteúdo: blogs, notícias, eventos e formulário de contacto.

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
- Alterar o autor e a data de publicação."

## Gerir Revisões de Conteúdo

1. **Aceder à Lista de Conteúdo**:
    - Navegar para a secção "Content" na barra lateral esquerda.
2. **Editar e Criar Revisões**:
    - Editar um conteúdo existente e salvar as alterações.
    - Visualizar as revisões disponíveis na aba "Revisions".
3. **Restaurar Revisões Anteriores**:
    - Explorar a opção de restaurar versões anteriores do conteúdo.

## Gerir Módulos

Antes de ativar um módulo, é necessário descarregá-lo.
Por defeito, o Drupal CMS já inclui alguns módulos disponíveis. Alguns estão ativados e outros aguardam ativação.

### Listar e ativar modulos disponiveis

**Explorar a Lista de Módulos**:
- Navegar para "Extend" e depois "List".
- Observar os módulos disponíveis, ativados e não ativados.
- Ativar os módulos "Language" e "Interface translation".

### Instalar - Listar, descarregar e ativar novos módulos.
  
  **Explorar a Lista de Módulos**:
- Navegar para *Browse modules*.
- Observar e Explorar os módulos disponíveis, como "Admin toolbar".

### Traduzir o Website para Português

O Modulo Coffee já vem instalado permite aceder rapidamente a qualquer página de administração com apenas algumas teclas.

1. **Utilizar o Módulo Coffee**:
    - Ativar o Coffee com `Alt + D` (ou atalho correspondente).
    - Pesquisar por "Languages" e selecionar a opção.
2. **Instalar o Idioma Português (Portugal)**:
    - Adicionar o idioma Português (Portugal).
    - Aguardar o download das traduções do Drupal.
3. **Configurar o Bloco de Mudança de Idioma**:
    - Navegar para "Structure" e depois "Block layout".
    - Adicionar o bloco "Language switcher" à região desejada (ex. Content above)
4. **Traduzir Conteúdo**:
    - Aceder à página inicial.
    - Mudar o idioma do site para português.
    - Traduzir a página inicial e outros conteúdos relevantes e ver o resultado.

### Atualizar o Website e Módulos

1. **Atualizar Módulos Desatualizados**:
    - Navegar para "Extend" e depois "Update extensions".
    - Atualizar o módulo "Diff" (e outros módulos desatualizados).
2. Experimentar o novo módulo para comparar Revisões de Conteúdo**:
    - Editar um conteúdo e criar uma nova revisão.
    - Selecionar na aba a opção "Revisions"
    - Utilizar a função "Compare Revisions" para visualizar as diferenças.