---
title: 'Usando o FreeRIDE no Linux'
date: Tue, 29 Apr 2008 01:19:05 +0000
draft: false
tags: [ruby, slackware]
---
O FreeRIDE (Free Ruby Integrated Development Environment) é um ambiente integrado para desenvolvimento em Ruby, ele foi desenvolvido usando o FxRuby, ou seja, uma versão do  Fox Toolkit para Ruby.

O FreeRIDE inclui um interpretador Ruby, um navedor para documentação do Ruby (conhecido como RI ou Ruby Doc).

Para instalar o FreeRIDE no Linux você deve fazer o download do arquivo freeride-linux-installer-0.9.6.sh no link a seguir  http://rubyforge.org/frs/download.php/10933/freeride-linux-installer-0.9.6.sh Para fazer a instalação você deve dar permissão de execução para o arquivo e executá-lo como root: $ chmod a+x freeride-linux-installer-0.9.6.sh $ su root # ./freeride-linux-installer-0.9.6.sh Você será perguntado em qual diretório o FreeRIDE deve ser instalado, o ideal é instalar o FreeRIDE no diretório padrão.

Veja a tela abaixo: FreeRIDE  - starting installation...

IMPORTANT NOTE -------------- FreeRIDE must be installed in /usr/local/FreeRIDE.

If you want to install it elsewhere a symbolic link will be created from /usr/local/FreeRIDE to the chosen location Choose where to install FreeRIDE \[/usr/local\] : Installing FreeRIDE.

Please wait...

--------------------- MANIFEST --------------------- This is version 0.9.6 of FreeRIDE, the Ruby integrated development environment.

This version is built with the following components: Ruby               1.8.4 Fox Toolkit        1.2.16 Fox Scintilla      1.62 FXRuby             1.2.6 ---------------------------------------------------- FreeRIDE succesfully installed.

Start FreeRIDE with '/usr/local/FreeRIDE/freeride' Agora basta executar o FreeRIDE, no KDE pressione ALT+F2 e aponte para o caminho do executável /usr/local/FreeRIDE/freeride Pronto, agora você pode programar em Ruby usando uma interface gráfica.

Obs: O projeto do FreeRIDE foi interrompido na versão 0.9.6, os donos do projeto decidiram reescrever o FreeRIDE usando outro toolkit chamado wxRuby, que usa wxWidgets.

Veja o link http://freeride.rubyforge.org/wiki/wiki.pl?FreeRIDE_Future.

Para acompanhar o desenvolvimento visite o site http://wxride.ruby-im.net/.

\[\]'s