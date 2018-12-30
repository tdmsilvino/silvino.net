---
title: 'Usando o Slax Linux'
date: Fri, 20 Sep 2013 13:32:42 +0000
draft: false
tags: [linux, slackware]
---
O [Slax](http://www.slax.org "Slax") é uma versão portável do Linux baseada na distribuição [Slackware](http://slackware.com "Slackware").

O Slax traz o Firefox, mplayer (player multimedia), okular (leitor de PDF), gwenviewer (vizualizador de imagens), muitos outros programas e o desktop KDE em uma imagem de aproximadamente 220Mb e que está disponível em várias línguas.

Para usar o Slax no seu computador você deve fazer o download nesse link [http://www.slax.org/en/download.php](http://www.slax.org/en/download.php "http://www.slax.org/en/download.php") Você verá quatro opções de download: Download for CD - duas imagens ISO (32 bits e 64 bits) que você pode usar numa máquina virtual como o VirtualBox ou queimar num CD/DVD para dar boot no seu computador.

Download for USB - dois arquivos compactados no formato ZIP (32 bits e 64 bits) que você pode usar num pendrive para dar boot no seu computador.

Se a sua máquina tem mais de 4GB de memória RAM e/ou um processador com mais de um núcleo (exemplos dual core, quad core, corei3,5,7) use a versão 64 bits.

Para usar o Slax em Portugês num pendrive acesse a página de download, vá até a linha "Slax Brazilian (Portuguese)" e selecione uma das opções "32 bit ZIP" ou "64 bit ZIP".

Quando download terminar, copie o arquivo ZIP no seu pendrive (na minha máquina o pendrive foi reconhecido como E:\\, use a letra que o Windows detectar) e descompacte o arquivo na raiz do pendrive, entre na pasta E:\\slax\\boot e execute o script bootinst.bat.

Se tudo der certo o seu pendrive já vai estar inicializável.

Obs: Se você já está usando o Linux e quer testar o Slax descompacte o arquivo no pendrive e execute o script slax/boot/bootinst.sh.

Você deve reiniciar a sua máquina com o pendrive conectado em uma porta USB e na tela inicial da BIOS você deve pressionar uma tecla para escolher a opção de boot pelo pendrive (USB disk), essa tecla varia em cada computador, normalmente é uma das teclas F8, F9, F10 ou ESC.

Depois de escolher a opção de boot pelo pendrive (USB disk) você verá a tela de boot do Slax, você pode apertar a tecla TAB para mudar as opções ou simplesmente escolher a opção "Run Slax" e pressionar a tecla ENTER.

Escolhendo essa opção padrão o Slax vai iniciar o no modo gráfico com o KDE.

Se o Slax não reconhecer a placa de rede wireless ou algum outro hardware da sua máquina você deve conectar na Internet usando a placa de rede comum, com um cabo de rede, e abrir a "Central de Programas" e fazer o download do módulo "Linux Firmware" depois reinicie o Slax e tente novamente.

Boa sorte!