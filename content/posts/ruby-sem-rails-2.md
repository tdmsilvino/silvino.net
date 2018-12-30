---
title: 'Ruby sem Rails - parte 2'
date: Fri, 04 Apr 2008 17:52:35 +0000
draft: false
tags: [ruby, slackware]
---
_**Usando mod_ruby, eruby e erubis no Slackware**_ O mod\_ruby é um módulo que permite que o Apache execute de forma nativa os scripts feitos em Ruby.

Depois de instalar o mod\_ruby você deve escolher qual será o seu gerador de templates, usando um gerador de templates você pode incluir o código Ruby em páginas HTML e programar no mesmo estilo do ASP e PHP.

Você pode escolher o ERB que já vem incluído na distribuição padrão do Ruby ou pode usar o eRuby que foi escrito em C para ganho de desempenho.

Caso você queira usar o eRuby você precisa instalar ele na sua máquina.

O código fonte do mod_ruby e do eruby podem ser encontrados no site http://modruby.net/, mas se você quer facilidade basta baixar os dois pacotes [](http://fotoleitura.com/downloads/eruby-1.0.5-i486-1tdm.tgz)que fiz para o Slackware 12 e instalar no seu sistema.

Baixe os pacotes [mod_ruby-1.2.6](ftp://linuxpackages.telecoms.bg/Slackware-12.0/Console/mod_ruby/mod_ruby-1.2.6-i486-1tdm.tgz "mod_ruby no linuxpackages.net") e [eruby-1.0.5](ftp://linuxpackages.telecoms.bg/Slackware-12.0/Console/eRuby/eruby-1.0.5-i486-1tdm.tgz "eruby no linuxpackages.net").

Depois use a ferramente installpkg para instalar no Slackware.

Depois de instalar o mod\_ruby e o eruby na sua máquina, você pode instalar também o erubis.

O erubis é um gerador de templates, implementado em Ruby e também usa algumas funções do eRuby.

O erubis é muito rápido, quase três vezes mais rápido do que o ERB e ainda é 10% mais rápido do que o eRuby, tem suporte à várias linguagens (Ruby/PHP/C/Java/Scheme/Perl/Javascript).

Permite que você combine templates com arquivos YAML, para usar arquivos de contexto e tem suporte à Ruby on Rails.

Para instalar o erubis você deve baixar os pacotes abstract e erubis do site http://rubyforge.net e executar os comandos abaixo como root: $ tar xjf abstract\_1.0.0.tar.bz2 $ cd abstract\_1.0.0/ $ su root # ruby setup.rb # exit $ cd ..

$ tar xjf erubis-2.5.0.tar.bz2 $ cd erubis-2.5.0/ # su root # ruby setup.rb $ cp contrib/erubis-run /usr/lib/ruby/1.8/apache Agora vamos configurar a integração com o Apache.

Inclua as linhas abaixo no seu arquivo /etc/httpd/httpd.conf e salve o arquivo.

LoadModule ruby\_module lib/httpd/modules/mod\_ruby.so <IfModule mod\_ruby.c> RubyRequire apache/ruby-run RubyRequire apache/eruby-run RubyRequire apache/erubis-run <Location /erubis> SetHandler ruby-object RubyHandler Apache::ErubisRun.instance </Location> <Files *.rhtml> SetHandler ruby-object RubyHandler Apache::ErubisRun.instance </Files> </IfModule> Depois disso faça com que o usuário apache seja o dono do diretório onde as páginas web estarão.

chown -R apache:apache /var/www Isso é necessário pois o erubis precisa de acesso de escrita no diretório htdocs para criar uma área de cache.

Para fazer um teste copie o arquivo de exemplo da pasta do erubis para dentro da pasta /var/www/htdocs # cp erubis-2.5.0/examples/basic/example.eruby /var/www/htdocs/example.rhtml Agora abra o arquivo example.rhtml no navegador.

Pronto, agora você está rodando Ruby sem Rails! Até mais!