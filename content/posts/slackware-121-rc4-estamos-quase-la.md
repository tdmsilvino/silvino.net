---
title: 'Slackware 12.1 rc4 - estamos quase lá!'
date: Thu, 01 May 2008 13:05:33 +0000
draft: false
tags: [slackware]
---

Ontem a noite tivemos mais atividade no -current. O Patrick lançou o Slackware 12.1 rc4 devido à um patch de segurança que foi aplicado no kernel 2.6.24.5, segue a tradução:

Quarta Abr 30 20:36:48 CDT 2008
12.1 RC4.  Nós acreditamos que este deve ser o último.
a/kernel-generic-2.6.24.5-i486-2.tgz:  Patch aplicado para corrigir um problema de segurança
 em fs/dnotify.c.  O uso do dnotify (largamente substituido por inotify nos sistemas 2.6.x)
 poderia causar um DoS local, ou possívelmente um buraco local para o root.  Nós falamos que
 não fariamos mudanças agora a não ser que algo fosse "crítico" -- e parace que conseguimos
o que desejávamos.  ;-)  Esse problema também será corrigido nas versões anteriores do kernel
o mais rápido possível.  O patch pode ser encontrado em source/k/linux-2.6.24.5-CVE-2008-1375-patch/.
Para informações adicionais (quando o candidato CVE estiver aberto), veja:
    http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2008-1375
 Todos os pacotes do kernel listados abaixo também devem ser considerados correções de segurança.
Todos os pacotes relativos ao kernel foram atulizados com o patch de segurança e recompilados, de quebra o Patrick atualizou o programa slackpkg do [Piter Punk](http://stoa.usp.br/piterpk/profile/ "Piter Punk").

Leia o changelog no endereço [ftp://ftp.slackware.com/pub/slackware/slackware-current/ChangeLog.txt](ftp://ftp.slackware.com/pub/slackware/slackware-current/ChangeLog.txt "Changelog do -current") Até mais!