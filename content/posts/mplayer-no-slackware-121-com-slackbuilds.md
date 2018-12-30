---
title: 'Mplayer no Slackware 12.1 com Slackbuilds'
date: Sun, 11 May 2008 18:17:34 +0000
draft: false
tags: [slackware]
---
Boa tarde pessoal.

No meu último [post](http://silvino.net/2008/05/11/usando-slackbuilds-no-slackware-121/ "Slackbuilds no Slackare 12.1") eu expliquei como fazer a instalação de programas usando [Slackbuilds](http://slackbuilds.org "Página oficial do Slackbuilds").

Como exemplo eu mostrei os passos para a instalação do emulador de terminal Yakuake, e é lógico que o procedimento se aplica para todos os demais Slackbuilds.

Porém devemos tomar cuidados com as dependências.

Por exemplo, antes de instalar o Mplayer você de ter os pacotes do Lame, que é usado pelo mencoder para gerar audio em mp3, e da biblioteca Libdvdnav, que é usada ler DVDs e os codecs do Mplayer instalados previamente.

A seguir os links para os Slackbuilds: Lame: [http://slackbuilds.org/repository/12.1/libraries/lame/](http://slackbuilds.org/repository/12.1/libraries/lame/ "Slackbuild para o Lame") Libdvdnav: [http://slackbuilds.org/repository/12.1/libraries/libdvdnav/](http://slackbuilds.org/repository/12.1/libraries/libdvdnav/ "Slackbuild da biblioteca libdvdnav") Todos os codecs para o Mplayer: [http://slackbuilds.org/repository/12.1/multimedia/mplayer-codecs-all/](http://slackbuilds.org/repository/12.1/multimedia/mplayer-codecs-all/ "Slackbuild para os codecs do Mplayer") Em cada um dos links citados você deve executar os passos abaixo: 1.

Fazer o download do Slackbuild e descompactá-lo, isso criará um diretório com o nome do Slackbuild.

2.

Depois você deve fazer o download do código fonte compactado (Download Source) e salvá-lo dentro do diretório do Slackbuild.

3.

Abrir um terminal e entrar no diretório do Slackbuild (supondo que o diretório está no seu Desktop "**cd ~/Desktop/<nome\_do\_slackbuild>**") 4\.

Logar como root, com o comando "**su root**" 5\.

Executar o script do Slackbuild "**./<nome\_do\_slackbuild>.Slackbuild**" 6\.

Instalar o pacote criado no diretório /tmp, com o comando "**installpkg /tmp/<nome\_do\_pacote>.tgz**" Depois que esses três pacotes estiverem instalados, você pode instalar o Mplayer.

O Slackbuild do Mplayer está no link [http://slackbuilds.org/repository/12.1/multimedia/MPlayer/](http://slackbuilds.org/repository/12.1/multimedia/MPlayer/ "Slackbuild do Mplayer").

Você vai usar o mesmo procedimento citado acima, a única diferença é que no segundo passo, além do código fonte compactado, você também deve fazer o download do skin no link [http://www.mplayerhq.hu/MPlayer/skins/Blue-1.7.tar.bz2](http://www.mplayerhq.hu/MPlayer/skins/Blue-1.7.tar.bz2 "Skin Blue para o Mplayer") e salvá-lo dentro do diretório do Slackbuild.

Feito isso é só continuar.

Depois que tudo for instalado você pode apagar os diretórios com os Slackbuilds pois eles não serão mais necessários.

Agora é só curtir.

Até mais!