---
title: 'Novidades sobre o Slackware'
date: Sat, 16 Aug 2008 13:46:43 +0000
draft: false
tags: [slackware]
---
No dia 13 de agosto o Patrick, desenvolvedor do Slackware, anunciou que o KDE 4.1 foi incluído no Slackware.

Por enquanto os pacotes estão no -current /testing, mas ele diz que toda a equipe de desenvolvimento, já está usando o KDE 4.1 sem nenhum problema.

Para usar o KDE 4.1 você precisa atualizar o seu sistema para o -current e fazer o download dos pacotes em qualquer um dos mirrors do Slackware.

Se você quiser usar um mirror do Brasil use o link abaixo, baixe toda a estrutura de sub-diretórios: ftp://ftp.slackware-brasil.com.br/slackware-current/testing/packages/kde4/ O arquivo README traz uma série de recomendações que devem ser seguidas.

Além de atualizar o sistema para o -current, você deve remover todos os pacotes relacionados ao KDE 3, incluindo o qt, qca, qca-tls e knemo.

Você deve fazer um backup e depois remover os seguintes diretórios: /etc/kde, $HOME/.kde.

Entre no diretório com os pacotes do KDE 4.1 e use esse comando: upgradepkg --install-new deps/*.tgz extragear/*.tgz kde/*.tgz kde3-compat/*.tgz Dê uma olhada no arquivo README e mãos-à-obra.

Bom, além do KDE 4.1 o time do Slackware desenvolveu um novo logo para o Slackware.

Entre no site slackware.com e confira, o Patrick disse que o logo antigo era muito difícil de ler e de guardar na memória rsrsrsrsrs.

Até mais!