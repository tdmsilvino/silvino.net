---
title: 'Arquivos .3gp no Mplayer'
date: Sat, 17 May 2008 21:12:20 +0000
draft: false
tags: [slackware]
---
Hoje precisei copiar alguns vídeos do celular da minha cunhada.

A gente queria converter os vídeos e postar no Youtube.

Todos os vídeos do celular estavam no formato 3gp e ao abrí-los no mplayer o vídeo foi reproduzido porém o som estava mudo.

Decidi executar o mplayer pela linha de comando para verificar as mensagens de erro e descobri que o mplayer não conseguia encontrar o codec libamr_nb e por isso não reproduzia o som.

Ao fazer um pesquisa no Google, descobri as peças que estavam faltando.

O formato de arquivo 3gp foi definido pelo grupo [3GPP - 3rd Generation Partnership Project](http://www.3gpp.org/About/about.htm) que é composto por vários fabricantes da área de telecomunicações, afim de ditar os padrões a serem usados nos aparelhos de terceira geração, como os celulares GSM.

Para ativar o suporte à arquivos 3gp no mplayer dentro do Slackware, nós podemos usar os scripts disponíveis no site Slackbuilds.org.

Você precisa baixar os arquivos referentes às bibliotecas [amrnb](http://slackbuilds.org/repository/12.1/audio/amrnb/ "Biblioteca amrnb") e [amrwb](http://slackbuilds.org/repository/12.1/audio/amrwb/ "Biblioteca amrwb").

Antes de executar o Slackbuild da biblioteca amrnb você deve baixar o arquivo [26104-700.zip](http://www.3gpp.org/ftp/Specs/archive/26_series/26.104/26104-700.zip) no mesmo diretório do script Slackbuild.

Já para a biblioteca amrwb você deve baixar o arquivo [26204-700.zip](http://www.3gpp.org/ftp/Specs/archive/26_series/26.204/26204-700.zip) no mesmo diretório do Slackbuild antes de executar o script para a geração do pacote.

Depois que você instalar os pacotes para as bibliotecas amrnb e amrwb, você deve recompilar o mplayer para que ele detecte as novas bibliotecas e passe a usá-las.

Para fazer isso você também pode usar Slackbuilds como expliquei no meu post [Mplayer no Slackware 12.1 com Slackbuilds](http://silvino.net/2008/05/11/mplayer-no-slackware-121-com-slackbuilds/).

Até mais!