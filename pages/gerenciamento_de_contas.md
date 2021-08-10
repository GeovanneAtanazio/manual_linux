# Manipulação de contas

Abaixo estão listados comandos úteis para a manipulação de contas.

## `adduser`

- Utilidade:  Adicionar um usuário.
- Estrutura: `adduser` *`[usuário]`*.
- Macetes: 
	1. Para adicionar um usuário em um grupo extra basta usar o comando `adduser`, seguido pelo nome do usuário e pelo nome do grupo, assim: `adduser usuário grupo`.
	2. Por padrão, quando um novo usuário é adicionado, é criado um grupo com o mesmo nome do usuário.

## `addgroup`

- Utilidade:  Adicionar um grupo.
- Estrutura: `adduser` *`[grupo]`* .

## `passwd`

- Utilidade:  Alterar senha.
- Estrutura: `adduser` *`[usuário]`*.

## `su`

- Utilidade:  Alternar usuário.
- Estrutura: `su` *`[usuário]`*.
- Macetes: 
	1. Para alternar para o usuário root é só utilizar o comando `sudo su`.

## `userdel`

- Utilidade:  Exclui um usuário.
- Estrutura: `userdel` *`[opções]`* *`[usuário]`*.
- Opções:
	- `-r`: Apaga também o diretório `home` do usuário.

## `groupdel`

- Utilidade:  Exclui um usuário.
- Estrutura: `userdel`  *`[grupo]`*.
- Macetes: 
	1. Não é possível remover o grupo primário de um usuário. Para isso é preciso remova o usuário primeiro.

