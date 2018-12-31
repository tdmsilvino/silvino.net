---
title: 'Melhorias no domínio, HTTPS, e Indieweb'
date: Mon, 31 Dec 2018 02:10:20 -0002
draft: false
tags: [pessoal,hugo,indieweb,pt]
---
Essa semana decidi fazer algumas melhorias no meu domínio.

Primeiramente ajustei as configurações de e-mail, que está hospedado no serviço Zoho, habilitei SPF, DKIM e DMARC. Essas configurações ajudam na segurança do e-mail, impendindo que alguém não autorizado possa se passar por usuários do meu domínio.

A segunda coisa que fiz, foi tratar de habilitar HTTPS. E fiz isso usando uma conta gratuita na CND [CloudFlare](https://www.cloudflare.com/). Além do HTTPS, ganhei o uso do cache da CDN que ajuda muito na performance do site.

Por último tratei de migrar o blog. Deixei de usar o Pelican como gerador das páginas estáticas, e passei a usar o [Hugo](https://gohugo.io/). A migração foi finalizada ontem, 30/12/2018, com sucesso.

Deixei de usar o GitHub Pages, para hospedar as páginas, e agora estou usando uma conta gratuita na  [Netlify](https://www.netlify.com/). Tudo ficou muito simples.
 Escrevo as páginas localmente e faço um push para o meu repositório no GitHub, a Netlify detecta as alterações no repositório, e gera as páginas usando o Hugo.

Também fiz algumas alterações no layout e habilitei novas funções da [Indieweb](https://indieweb.org/). Agora posso autenticar em alguns serviços usando o meu domínio.
 Os meus perfis de redes sociais estão linkados o meu domínio. E cada post desse blog, tem metadados indicando a autoria.

Além disso consegui habilitar o uso das [Webmentions](https://indieweb.org/Webmention), que permite que outras pessoas com domínios proprietários façam menções diretamente ao meu domínio.
Para isso o usei o endpoint e o script criado por [Pelle](https://voxpelli.com/2013/12/webmentions-for-static-pages/). Realizei alguns testes e está funcionando bem.

Agora aos próximos passos:
1. Quero testar um método de postagem simplificada, para que eu possa escrever artigos com mais frequencia.
2. Desejo testar a integração com o serviço [Brid.gy](https://brid.gy/), para receber Webmentions para reações nas redes sociais.
3. Também quero usar o padrão [Micropub](https://indieweb.org/Micropub) para realizar os meus posts.

Creio que essa é basicamente uma jornada similar àquela descrita por [Amit Gawande](https://www.amitgawande.com/indiewebify-hugo-website/). Vamos ver se consigo. Espero que sim!

Até mais!