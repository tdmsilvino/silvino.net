---
title: 'Usando Slackbuilds no Slackware 12.1'
date: Sun, 11 May 2008 16:46:05 +0000
draft: false
tags: [slackware]
---
Boa tarde para todos! Após atualizar o meu sistema para o Slackware 12.1 precisei instalar alguns programas como o Yakuake e o Mplayer.

Fiz uma visita no [linuxpackages.net](http://www.linuxpackages.net/search_view.php?orderby=p_date&advance=DESC&ver=12.1 "Pacotes para o Slackware") e vi que por enquanto só temos 6 pacotes atualizados para o Slackware 12.1.

Isso faz sentido, pois os pacotes do linuxpackages são mantidos pela comunidade e nem todo mundo tem tempo livre pra ficar atualizando pacotes (eu mesmo não atualizei os meus três pacotes que enviei para lá, hehehe).

Portanto a galera que quer instalar os programas deve partir para a instalação a partir do código fonte: baixar o fonte, descompactar, dar uma olhada nos arquivos README e INSTALL e finalmente compilar o programa usando os comandos "**./configure --prefix=/usr && make && make install**".

Esses são os passos para instalar um programa direto do código fonte: 1.

Baixar o código fonte em /usr/src e descompactá-lo 2.

Entrar no diretório do código fonte e ler os arquivos README e INSTALL para obter instruções detalhadas sobre a instalação do programa.

3.

Passar vários parâmetros para o comando configure, para ver a lista completa execute **./cofigure --help**.

Se você não passar nenhum parâmetro para o comando configure, o seu programa será instalado em /usr/local e os arquivos serão divididos nos subdiretórios de /usr/local (por exemplo, os arquivos de configuração ficarão em /usr/local/etc).

Para que isso não aconteça você deve passar no mínino as opções mais comuns ao comando configure, como no exemplo a seguir: **./configure --prefix=/usr --sysconfdir=/etc --localstatedir=/var** 4\.

Depois de rodar o configure você deve executar o comando **make**, para compilar o código fonte, e o **make install**, para instalar o programa compilado.

Ao invés de usar o make install você pode usar o comando **checkinstall -S** para gerar um pacote do Slackware que será instalado pelo **installpkg**.

Obs: O checkinstall pode ser obtido em [http://www.asic-linux.com.mx/~izto/checkinstall/download.php](http://www.asic-linux.com.mx/~izto/checkinstall/download.php "Homepage do Checkinstall").

5\.

Para desintalar um programa instalado com o comando **make install**, você deve manter o diretório com o código fonte compilado e executar o comando **make uninstall**.

Todo esse processo é muito complicado e cansativo, e se você esquecer de passar uma determinada opção para o comando configure, talvez o seu programa não funcionará como esperado.

Para automatizar o processo de geração de pacotes para o Slackware a comunidade criou o projeto [Slackbuilds.org](http://slackbuilds.org "Página oficial do Slackbuilds").

Slackbuilds são scripts que contêm todos os passos necessários para a criação de um pacote.

No final do processo o pacote será movido para o diretório /tmp para ser instalado no Slackware, usando o **pkgtool**.

Todos os pacotes oficiais do Slackware vêm com um Slackbuild incluído.

Vamos supor que você queira instalar o emulador de terminal [Yakuake](http://yakuake.kde.org "Emulador de terminal") usando um script Slackbuild.

Para isso você deve acessar o link [http://slackbuilds.org/repository/12.1/system/yakuake/](http://slackbuilds.org/repository/12.1/system/yakuake/) e baixar o código fonte no link abaixo do título "Download Source" e o script de instalação no link abaixo do título "Download Slackbuild".

Agora você deve descompactar o arquivo do Slackbuild, nesse caso yakuake.tar.gz, fazendo isso será criado um diretório chamado yakuake, mova o arquivo do código fonte para dentro do diretório yakuake.

Agora abra um terminal e acesse o diretório yakuake como root e execute o scritpt **./yakuke.Slackbuild**.

Esse script descompactará o código fonte dentro do diretório /tmp/SBo/yakuake-2.8.1 e fará todos os passos necessários para a criação de um pacote do Slackware.

No final do processo você terá um pacote pronto no diretório /tmp.

Para instalá-lo execute o comando **installpkg /tmp/yakuake-2.8.1-i486-1_SBo.tgz**, pronto o yakuake está pronto para usar.

Usando um script do slackbuilds.org você pode gerar os seus próprios pacotes sem passar por todas as complicações que o processo manual causaria.

Até mais!