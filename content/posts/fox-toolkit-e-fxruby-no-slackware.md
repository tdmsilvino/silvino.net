---
title: 'FOX Toolkit e FXRuby no Slackware'
date: Tue, 29 Apr 2008 01:57:18 +0000
draft: false
tags: [ruby, slackware]
---
O FOX é um toolkit baseado no C++ para desenvolvimento de aplicações gráficas (também conhecidas como GUIs) de forma fácil e eficaz.

O FOX oferece uma coleção vasta e crescente de controles e provê muitas facilidades como arrastar e soltar (drag and drop), seleções e também widgets do OpenGL para manipulação de gráficos 3D.

O FOX também implementa ícones, imagens, e itens de conveniência para o usuário como ajuda e dicas (tooltips).

Tooltips podem ser usadas em objetos 3D.

Para mais detalhes visitem a homepage no endereço http://www.fox-toolkit.org/ Esse toolkit tem ligações (bindings) para várias linguagens.

Para programar em Python use FXPy, em Eiffel use EiffelFox e para programar em Ruby use FXRuby.

Existem alguns projetos grandes usando FXRuby, entre eles o [FreeRIDE](http://freeride.rubyforge.org/ "IDE para Ruby") que abordei no [post anterior](http://silvino.net/2008/04/28/usando-o-freeride-no-linux/ "Usando o FreeRIDE no Linux"), o gerenciador de banco de dados [DbTalk](http://www.insula.cz/dbtalk "Gerenciador de banco de dados") e o gerenciador de projetos [Mondrian](http://www.mondrian-ide.com/ "Gerenciador de projetos").

Veja mais detalhes na homepage http://www.fxruby.org/.

Se você usa o Slackware 12 e quer instalar o FOX, você pode baixar o pacote [fox-1.6.32-i486-1tdm.tgz](http://fotoleitura.com/downloads/fox-1.6.32-i486-1tdm.tgz "Pacote para Slackware 12.0").

Se você não usa o Slackware você deve pesquisar no repositório da sua distro preferida ou baixar o código fonte e compilar usando o famoso trio "./configure && make && make install".

Obs: não deixe de executar ./configure --help para ver quais opções você vai querer ativar.

Depois de instalar o FOX você deve instalar o FXRuby usando o comando gem.

$ su root # gem install fxruby Veja os exemploes em de código em /usr/lib/ruby/gems/1.8/gems/fxruby-1.6.14/examples/ $ ls -m /usr/lib/ruby/gems/1.8/gems/fxruby-1.6.14/examples/ babelfish.rb, bounce.rb, browser.rb, button.rb, custom\_table\_item.rb, datatarget.rb, dctest.rb, dialog.rb, dilbert.rb, dirlist.rb, dragdrop.rb, dragsource.rb, dropsite.rb, foursplit.rb, gltest.rb, glviewer.rb, groupbox.rb, header.rb, hello2.rb, hello.rb, iconlist.rb, icons, image.rb, imageviewer.rb, inputs.rb, iRAA.rb, mditest.rb, pig.rb, raabrowser.rb, RAA.rb, ratio.rb, README, rulerview.rb, scintilla-test.rb, scribble-orig.rb, scribble.rb, shutter.rb, splitter.rb, styledtext.rb, tabbook.rb, table.rb, textedit, unicode.rb $ ruby /usr/lib/ruby/gems/1.8/gems/fxruby-1.6.14/examples/hello.rb Pronto agora você pode se divertir fazendo programas multiplataformas usando FXRuby.

Quem quiser ir a fundo no assunto pode até comprar o livro do FXRuby http://www.pragprog.com/titles/fxruby.

\[\]'s