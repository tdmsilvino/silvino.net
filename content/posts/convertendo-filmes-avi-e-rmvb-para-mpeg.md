---
title: 'Convertendo filmes AVI e RMVB para MPEG'
date: Sun, 25 May 2008 12:01:08 +0000
draft: false
tags: [multimedia]
---
Há um tempo atrás eu estava precisando converter uns filmes no formato AVI e RMVB para MPEG.

Depois de ler muitos tutoriais descobri muitas formas de fazer esse tipo de conversão.

Acabei escolhendo o mencoder, que é o codificador do projeto mplayer.

Eu criei um script para converter todos os filmes de um determinado diretório para o formato MPEG afim de gravá-los em um DVD.

Segue o código do script: for filme in \`ls *.avi *.rmvb\`; do filmempeg=\`echo $filme | sed s/.avi/.mpeg/\`; echo "Convertendo $filme para $filmempeg"; mencoder -oac lavc -ovc lavc -of mpeg -mpegopts format=dvd:tsaf -vf scale=720:480,harddup -srate 48000 -af lavcresample=48000 -lavcopts vcodec=mpeg2video:vrc\_buf\_size=1835:vrc_maxrate=9800:vbitrate=5000:keyint=18:vstrict=0:acodec=ac3:abitrate=192:aspect=4/3 -ofps 30000/1001 -o $filmempeg $filme done Esse script cria arquivos MPEG no formato NTSC com uma resolução de 720x480, com 29,97 frames por segundo (30000/1001) e aspecto 4:3.

Você pode alterar o script acima e ajustá-lo às duas necessidades.

Basta consultar a tabela [Format Constraints](http://www.mplayerhq.hu/DOCS/HTML-single/en/MPlayer.html#menc-feat-vcd-dvd "Tabela de formatos de DVD") apresentada no site do Mplayer para obter mais informações e exemplos.

Depois altere a linha do comando mencoder de acordo com o que você precisar.

Obs: A conversão do formato RMVB para MPEG é muito mais lenta, pois o RMVB tem uma taxa de frames váriavel, portanto prefira baixar filmes no formato AVI.

Espero ter ajudado.

Até mais!