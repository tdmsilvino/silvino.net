---
title: 'Usando o dvdauthor para editar DVD''s'
date: Sat, 14 Jun 2008 15:02:21 +0000
draft: false
tags: [multimedia]
---
O dvdauthor pega os seus arquivos MPEG e gera arquivos IFO, BUP e VOB para gravar em um DVD.

Você pode usar um arquivo de configuração no formato XML ou parâmetros na linha de comando para dizer ao dvdauthor como ele deve criar os arquivos VOB.

Com o dvdauthor você pode criar menus e criar capítulos para cada título do seu DVD.

Abaixo estou mostrando um exemplo de arquivo de configuração do dvdauthor: <dvdauthor dest="dvd"> <vmgm/> <titleset> <titles> <pgc> <vob file="filme01.mpeg" chapters="0:00:20.00,0:10:20.00,0:20:20.00" /> <vob file="filme02.mpeg" chapters="0:00:20.00,0:10:20.00,0:20:20.00" /> </pgc> </titles> </titleset> </dvdauthor> O arquivo de configuração deve estar localizado no mesmo diretório dos arquivos MPEG.

No exemplo acima eu usei a opção "file" para indicar o nome dos arquivos e a opção "chapters" para indicar uma lista de capitulos, essa lista deve ser separada por vírgulas e deve estar no formato H:MM:ss.frac, isso indica que no exemplo acima o primeiro capítulo deve ser criado aos 20 segundos do começo do filme.

Depois de criar o arquivo de configuração basta entrar no mesmo diretório dos filmes e executar o comando "dvdauthor -c dvd.xml".

O dvdauthor criará um diretório chamado "dvd" com os subdiretórios AUDIO\_TS e VIDEO\_TS, nesses diretórios você tem os arquivos necessários para gerar um DVD.

Para gravar um DVD você pode usar o comando "growisofs -dvd-compat -Z /dev/dvd -dvd-video dvd".

Se você preferir usar o K3b para queimar o DVD, você deve usar a opção "Novo Projeto de DVD de Vídeo" na aba "Ínicio Rápido" e você só precisará copiar os arquivos de dentro do diretório VIDEO\_TS para o diretório VIDEO\_TS no seu projeto de DVD de vídeo.

Pronto agora você pode usar o Linux para editar os seus DVD's.

Obs: Para instalar o dvdauthor no Slackware 12.1 você pode usar o Slackbuild que pode ser encontrado nessa URL http://slackbuilds.org/repository/12.1/multimedia/dvdauthor/ Até mais!