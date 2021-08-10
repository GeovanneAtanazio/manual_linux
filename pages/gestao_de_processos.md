# Processos no GNU/Linux

Os programas e comandos executados em um sistema operacional geram processos. No GNU/Linux, um processo é constituído por:

 - *Process Identification* (*PID*): Identificador que é criado assim que o processo inicia.
 - *Parent Process Identification* (*PPID*): Alguns processos possuem um processo pai, esse, é identificado pelo *PPID*.
 - *User Identification* (*UID*): Identificador do usuário que iniciou o processo.
 
## Status dos processos
 
Os processos também possuem status. Eles são:

- R (*runing*): O processo está em execução no momento.
- D (*uninterruptible sleep*): O processo não pode ser interrompido.
- W (*paging*): O processo possui uma prioridade maior que o convencional
- S (*sleep*): É o processo que está ativo, mas não está sendo executado.
- Z (*zombie*): Quando o processo continua consumindo recurso, mas não tem mais utilidade.
- T (*stopped*): É o processo que foi interrompido.

# Manipulação de processos

Abaixo estão listados comandos úteis para a manipulação de processos.

## `ps`

- Utilidade: Exibir os processos em andamento no momento que o comando é executado.
- Estrutura: `ps` *`[opções]`* .
- Opções:
	- `u`: Mostra o nome de usuário que iniciou o processo e hora em que o processo foi iniciado.
	- `w`: Mostra a continuação da linha atual na próxima linha ao invés de cortar o restante que não couber na tela.
	- `--sort:` *`[coluna]`*:  Organiza a saída do comando `ps` de acordo com a coluna escolhida. É possível utilizar as colunas: `pid`, `utime`, `ppid`, `rss`, `size`, `user`, `priority`.

##  `top`

- Utilidade: Exibir de forma contínua detalhes dos processo executados — Para sair basta apertar a tecla `q`.
- Estrutura: `top` *`[opções]`* .

## `htop`

- Utilidade: A mesma do `top`, porém as informações são exibidas de forma mais legível.
- Estrutura: `htop`.

## `kill`

- Utilidade: Matar um processo.
- Estrutura: `kill` *`[opções]`* *`[PID]`*.
- Opções:
	- `-9`: Mata o processo imediatamente, sem chances de salvar os dados ou apagar os arquivos temporários criados por ele. 
	- `-1`: Mata o processo e sobe ele novamente.
- Macetes: 
	1. O comando `kill` necessita do *PID* como parâmetro. Para descobrir o *PID* de um processo de forma fácil e rápida basta utilizar o comando `pgrep` e informar o nome do processo que se deseja saber o *PID*.
