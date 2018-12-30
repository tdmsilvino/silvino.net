---
title: 'Ruby sem Rails'
date: Thu, 20 Mar 2008 22:47:11 +0000
draft: false
tags: [ruby]
---
**_O Ruby e o Rails_** Na semana passada comecei a estudar a linguagem [Ruby](http://ruby-lang.org/).

Li alguns tutoriais e fiquei muito empolgado com a facilidade de uso e com o método de programação.

A linguagem Ruby é muito flexivel, nela quase tudo é tratado como um objeto.

Se você não acredita e quer ver com seus próprios olhos, dê uma olhada no shell interativo do tutorial [TryRuby](http://tryruby.hobix.com/%20) (em inglês) ou instale o Ruby na sua máquina e siga o tutorial [Ruby em Vinte Minutos](http://www.ruby-lang.org/pt/documentacao/ruby-em-vinte-minutos/) (bom e velho Português do Brasil!).

Aprendi trabalhar com variáveis, fazer loops, criar classes, blocos, etc., porém foi muito difícil encontrar um bom tutorial que me explicasse como usar a liguagem Ruby para gerar páginas dinâmicas, sem usar o framework [Rails](http://rubyonrails.org/).

Tudo o que eu procurava na web me levava ao Rails.

Acredito que isso faz muitas pessoas desistirem de continuar estudando a linguagem.

Quero deixar claro que não tenho nada contra o Rails.

O Rails é um ótimo framework, faz as coisas se tornarem muito simples, porém fica dificil para o iniciante em Ruby separar o que faz parte do framework e o que faz parte da linguagem em si.

E na verdade a pessoa terá que aprender a usar o framework e os novos métodos do Ruby ao mesmo tempo.

Se você conhece alguém possa tirar suas dúvidas, acredito que aprender os dois simultâneamente é o caminho a seguir, porém, se como eu você é auto-didata, você pode passar mais um pouco de tempo aprendendo a usar a linguagem Ruby antes de partir para Rails.

O Rails foi desenvolvido para aumentar a produtividade, mas se você tem muitas dúvidas sobre Ruby você não será produtivo e pode acabar se confundindo.

Por outro lado, se as suas dúvidas quanto a linguagem forem sanadas, você realmente alcançará a produtividade desejada.

**_O Ruby sem o Rails_** Antes de sair procurando na web decidi entar no diretório de instalação do Ruby para revirar o código fonte de alguns scripts e ver se encontrava algo que me apontasse o caminho das pedras.

Abri o meu terminal e fiz aquela pergunta que todo bom usuário do Slackware faz "whereis ruby", uma das respostas apontava para "/usr/lib/ruby/" entrei nesse diretório e encontrei os scripts do Ruby 1.8, alguns minutos depois cheguei ao arquivo erb.rb (outro ponto forte do Ruby, todo script vem com muita documentação incluída em seu código fonte).

O ERB é um sistema de template poderoso e de fácil uso, que permite embutir o Ruby dentro de arquivos de texto, xml e até mesmo arquivos HTML.

Todo código Ruby que for incluido dentro de tags <% %> será executado como um script Ruby.

No fim da documentação encontrei o que estava procurando, segue a tradução: # Há uma variedade de soluções para geração de templates disponíveis em vários projetos feitos em Ruby: # * O grande irmão do ERB, eRuby, trabalha da mesma forma mas é escrito em C para performance; # * Amrita (bom para produzirHTML/XML); # * cs/Template (C para performance); # * RDoc, distribuído com Ruby, usa o seu próprio motor para gerar templates, o qual pode ser usado em qualquer lugar; # * e outros; faça uma busca no RAA.

# Rails, o framework para aplicações web, usa ERB para criar views.

Isso era tudo o que eu precisava saber.

Apartir disso começei a pesquisar na web sobre ERB e eRuby.

O eRuby pode executar o código Ruby incluido dentro de páginas HTML e em conjunto com o mod_ruby você pode fazer o Apache servir suas páginas dinâmicas escritas em Ruby (essas páginas levam a extensão .rhtml).

Para trabalhar com sessões e recuperar dados de formulários do HTML pelo método POST, você deve criar um objeto CGI dentro do código Ruby e esse objeto fará o trabalho pesado para você.

No tutorial de Ruby do [Eustáquio Rangel](http://www.eustaquiorangel.com/downloads/tutorialruby.pdf) você encontra um exemplo de uso do objeto CGI.

Consulte o site do [mod_ruby](http://modruby.net/en/) para pegar o código fonte dos e fazer a integração com o Apache.

No próximo post vou explicar a integração com o Apache e fornecer os pacotes para instalação no Slackware.

Vou ficando por aqui.

Até mais!