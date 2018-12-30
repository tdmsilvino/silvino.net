---
title: 'Usando o SciTE para programar em Ruby'
date: Fri, 18 Apr 2008 02:18:26 +0000
draft: false
tags: [ruby, slackware]
---
Nessa última semana estive procurando algumas ferramentas gráficas para programar em Ruby.

Hoje eu acabei de testar o [SciTE](http://scintilla.sourceforge.net/SciTE.html "Editor de textos SciTE").

O SciTE foi criado para demonstrar o poder de um componente de edição de textos chamado [Scintilla](http://scintilla.sourceforge.net/ "Componente programável de edição de textos").

Usando o Scintilla você pode criar editores de textos e que podem ser usados para editar o código fonte de programas e chamar compiladores e depuradores externos.

O SciTE ficou tão bom que decidiram dar continuidade ao seu desenvolvimento e ele deixou de ser um programa de demonstração e se tornou um editor completo com suporte à várias linguagens, entre elas C/C++, D, C#, Java, PHP e Ruby.

Quer testar o programa? Baixe o executável já compilado para Linux no link abaixo (o único pré-requisito é ter uma versão do GTK+ igual ou superior à 2.8 na sua máquina) http://prdownloads.sourceforge.net/scintilla/gscite176.tgz?download Assim que terminar o download, você deve descompactar o arquivo gscite176.tgz; a partir desse ponto o programa já está pronto para rodar, mas muitas funções não estarão funcionando.

Para usar todos os recursos do programa você deve fazer o seguinte: 1.

Entre no diretório descompactado e copie o executavél SciTE para o diretório /usr/bin (cd gscite; cp SciTE /usr/bin) 2.

Crie um diretório /usr/share/scite e copie todos os arquivos com a extenção properties para lá (cp *.properties /usr/share/scite) 3.

Copie o arquivo Sci48M.png para o diretório /usr/share/pixmaps (cp Sci48M.png /usr/share/pixmaps) Opicional: Se você quiser ainda pode baixar a tradução do SciTE para Português Brasileiro no endereço a seguir http://groups.google.com/group/scite-interest/web/locale.pt\_BR.properties.

Basta copiar o arquivo de tradução para o diretório /usr/share/scite com o nome locale.properties (cp locale.pt\_BR.properties /usr/share/scite/locale.properties) e reiniciar a aplicação.

Pronto agora sim você pode testar o programa a vontade.

Pressione ALT+F2 e execute o comando SciTE.

Até mais!