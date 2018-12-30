---
title: 'Visão geral do Slackware 12.1'
date: Fri, 09 May 2008 17:54:36 +0000
draft: false
tags: [slackware]
---
Na semana passada fiz a instalação da última versão do Slackware e vou dar uma visão geral do Slackware 12.1.

O processo de instalação não mudou.

Você inicializa a máquina com um CD ou DVD, escolhe um kernel, usa o cfdisk criar as partições, roda o programa setup e segue a sequêcia apresentada no menu (ADDSWAP, TARGET, SOURCE, SELECT, INSTALL, CONFIGURE).

As novidades começam na seção CONFIGURE do instalador.

Agora temos a opção de ativar o suporte à caracters UTF8 no terminal.

Com isso podemos rodar com mais facilidades os programas que apresentam mensagens em outras línguas.

Agora o Slackware traz um pacote do programa scim (Smart Common Input Method) que te permite escrever textos em Chinês simplificado e tradicional, Japonês, Koreano, Árabe, Grego, Russo e muitos idiomas.

Mais serviços foram adicionados ao menu que configura os serviços que serão executados durante o processo de boot.

Depois que finalizei a configuração e sai do instalador, reiniciei a minha máquina e tive mais uma surpresa.

Agora o lilo foi instalado com uma imagem bitmap personalizada para o Slackware 12.1.

Após a inicialização do sistema adicionei um usuário usando o script adduser.

Esse script foi atualizado e agora pergunta se você quer incluir o usuário nos grupos audio, cdrom, floppy, plugdev e video.

Antes a gente tinha que lembrar isso de cabeça e escrever tudo na mão.

Por padrão o Slackware usa o diretório /mnt como ponto de montagem padrão para dispositivos como cdrom, disquete, dvd, etc.

Caso você queira que esses dispositivos sejam montados automáticamente pelo sistema, você deve abrir o arquivo /etc/fstab e comentar as linhas referentes ao cdrom, dvd e disquete.

Fazendo isso o gerenciador de mídia do KDE vai detectar o disco inserido e montá-lo automáticamente pra você.

Na minha opinião o Slackware está melhor do que nunca.

O sistema traz o kernel 2.6.24.5 com suporte à SMP, Xorg 7.3, KDE 3.5.9, XFCE 4.4.2, Fluxbox 1.0, ntfs-3g com suporte completo para leitura e escrita em NTFS, scim com suporte à muitos idiomas, muitos drivers para placas wireless, interpretadores para muitas linguages de script (Ruby 1.8.6_p114, Python 2.5.2, Perl 5.8.8, TCL 8.4.18), Apache 2.2.8 e muito mais.

Slacware 12.1 é o que há! Até mais!