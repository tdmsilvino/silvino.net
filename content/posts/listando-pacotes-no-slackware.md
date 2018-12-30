---
title: 'Listando pacotes no Slackware'
date: Sat, 17 May 2008 16:56:10 +0000
draft: false
tags: [slackware]
---

Boa tarde. Todos os pacotes que são instalados no Slackware ficam guardados em /var/log/packages. Isso significa que sempre que você quiser saber se tem um determinado pacote instalado você deve listar o conteúdo do diretório /var/log/packages e procurar pelo pacote desejado. Essa é a forma mais rápida, a outra forma de consultar os pacotes instalados é executar como root a ferramenta pkgtool e ir na opção view, então pkgtool listará todos os pacotes instalados. Como eu já estava cansado de ficar executando o comando "ls /var/log/packages/pacotetal*" decidi criar um script que me ajudasse nessa tarefa. Eu queria algo bem simples, algo bem parecido com o comando ls. Então criei o script abaixo e o nomeei lspkg. Dá uma olhada no script:

#!/bin/bash
cd /var/log/packages/
package_list=\`echo $* | sed s/" "/"* "/g | sed s/$/$"*"/ \`
for package in $package_list ; do
	if \[ -e $package \] ;
	then
	number\_of\_fields=\`echo $package | gawk -F "-" '{ split($0,fields); print length(fields) }'\`
		if \[ $number\_of\_fields == 5 \] ;
		then
			name=\`echo $package | cut -d - -f 1,2\`
			version=\`echo $package | cut -d - -f 3\`
			arch=\`echo $package | cut -d - -f 4\`
			build=\`echo $package | cut -d - -f 5\`
		else
			name=\`echo $package | cut -d - -f 1\`
			version=\`echo $package | cut -d - -f 2\`
			arch=\`echo $package | cut -d - -f 3\`
			build=\`echo $package | cut -d - -f 4\`
		fi
			echo -e -n "Package: 33\[1m$name33\[0m - "
			echo -n  "version: $version - "
			echo -n "arch: $arch - "
			echo "build: $build"
	else
		package\_not\_found=\`echo $package | tr -d "*"\`
		echo -e "The package 33\[1m$package\_not\_found was not found33\[0m in your system."
	fi
done
Agora é só copiar esse código para um arquivo de texto e salvá-lo como lspkg, você também deve dar permissão de execução para esse arquivo e copiá-lo para /usr/bin.

Depois de fazer o procedimento acim, faça um teste.

Veja o resultado quando executei na minha máquina: bash-3.1$ lspkg ruby bash pkgtoo teste Package: ruby - version: 1.8.6_p114 - arch: i486 - build: 1 Package: bash - version: 3.1.017 - arch: i486 - build: 2 Package: pkgtools - version: 12.1.0 - arch: noarch - build: 7 The package teste was not found in your system.

Caso você tenha alguma sugestão para melhorar esse script faça o seu comentário.

Até mais!