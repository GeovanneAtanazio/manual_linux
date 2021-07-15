# Arquivos no GNU/Linux

Os arquivos são utilizados para gravar dados. Eles, podem conter um texto, uma música, programa, planilha, etc. 

## Nomes e extensões

Para facilitar a identificação, cada arquivo deve ter um nome — lembrando que o GNU/Linux é *case sensitive*. No entanto, muitas vezes, não é possível localizar ou saber como utilizá-lo somente pelo nome, por conta disso, existem as extensões. 

A extensão são os caracteres separados do nome do arquivo por um  `.`, assim: `nome_arquivo.extensao`. O uso de extensões não é obrigatório na maioria das distribuições GNU/Linux, mas é conveniente o seu uso para determinar facilmente o tipo de arquivo e qual programa utilizar para abri-lo.

No GNU/Linux, quando o primeiro caractere do nome é um `.` significa que o arquivo em questão é oculto. Arquivos ocultos são ignorados, ou seja, eles existem, mas não são listados — a não ser que seja explicitado.

## Tipos de arquivos 

No GNU/Linux, existem sete tipos de arquivos, são eles: 
 - Arquivo regular: É o tipo mais comum de arquivo que se pode encontrar em um sistema GNU/Linux. Existem dois tipos de arquivos regulares:
	 -  Arquivo de texto: Seu conteúdo é compreendido pelas pessoas. Ele pode ser uma carta, um *script*, um programa de computador escrito pelo programador, arquivo de configuração, etc.
	 - Arquivo binário: Seu conteúdo somente pode ser entendido por computadores. Ele é gerado por um arquivo de programa através de um processo chamado de compilação.
 - Arquivo de diretório: Armazena arquivos de qualquer tipo, inclusive outros diretórios. 
 - Arquivo de dispositivo: São utilizados para gerenciar os dispositivos de entrada e saída. Eles se subdividem em dois grupos:
	 - Arquivo de caractere: Nele, normalmente, os dados são lidos e escritos diretamente no dispositivo, dispensando o uso de *buffers*.
	 - Arquivos de bloco: Nele, as operações de entrada e saída são realizadas de modo aleatório, em blocos, fazendo o uso de *buffers* intermediários.
 - Arquivo de *socket*: Permite a comunicação entre dois processos que compartilham dados. Ele permite a comunicação até mesmo entre sistemas operacionais diferentes.
 - Arquivo *pipe*: Permite a comunicação entre dois processos executados no mesmo sistema operacional.
 - Arquivo de *link* simbólico: Armazena uma representação textual do caminho para um arquivo referenciado.
 
# Diretórios no GNU/Linux

O diretório é um arquivo utilizado para armazenar conjuntos de arquivos. Com os diretórios é possível manter os arquivos organizados. 

No GNU/Linux não é permitido a existência de dois arquivos com o mesmo nome no mesmo diretório. As exceção são:

 - Arquivos de mesmo nome com extensões diferentes. 
 - Dois arquivos com o mesmo nome, e até com a mesma extensão, com um deles oculto.

## Estrutura  de diretórios do GNU/Linux

O sistema GNU/Linux possui uma estrutura básica de diretórios. Essa estrutura também é conhecida como Árvore de Diretórios, porque é parecida com uma árvore de cabeça para baixo. Cada diretório do sistema tem seus respectivos arquivos que são armazenados conforme regras definidas pela *Filesystem Hierarchy Standard (FHS)* da seguinte forma:

- `/`: Diretório principal do sistema. Dentro dele estão todos os diretórios do sistema.
- `/bin`: É reservado para gravar comandos que serão utilizados por todos os usuários.
- `/boot`: Contém os arquivos necessários para a inicialização do sistema.
- `/cdrom`: Este diretório não faz parte do padrão de hierarquia *FHS*, porém ele ainda é encontrado em algumas distribuições GNU/Linux. É utilizado como local temporário para *CDs* e *DVDs* inseridos no computador — porém, o local padrão para essas mídias é o diretório `/media`.
- `/dev`:  Contém arquivos gerados pelos dispositivos de *hardware*, como processador, placa de vídeo, leitor de mídia etc.
- `/etc`: Guarda a maioria dos arquivos essenciais do sistema operacional do computador local, como configuração usados para controlar uma operação ou programa.
- `/home`: Local destinado para os arquivos dos usuários, com exceção do *root*.
- `/lib`: Contém diretórios e *links* simbólicos compartilhados pelos programas do sistema e módulos do *kernel*.
- `/lost+found`: Local para a gravação de arquivos corrompidos, recuperados após uma verificação do sistema de arquivos — esse tipo de verificação ocorre na primeira reinicialização após um travamento no sistema.
- `/media`: Ponto de montagem de dispositivos removíveis como *pendrives*, *CDs*, *Blu-Ray* etc.
- `/mnt`: Ponto de montagem de subdiretórios temporários de dispositivos não removíveis e arquivos, como imagens ISO.
- `/opt`: É uma área reservada para instalações de pacotes de aplicações que otimizam o funcionamento de determinado programa ou acrescentam novos recursos.
- `/proc`: É usado pelo *kernel* para guardados registros de desempenho e status de processos.
- `/root`: Diretório padrão do usuário *root*.
- `/run`: Fornece às aplicações um local para armazenamento de arquivos temporários que, diferentemente dos arquivos armazenados no `/tmp`, em caso de exclusão causam problemas às aplicações que os utilizam.
- `/sbin`: Reúne arquivos binários acionados pelo sistema em si ou pelo *root* em processos de manutenção.
- `/srv`: Possui dados que são utilizados por serviços armazenados, como *web servers*.
- `/sys`: Sistema de arquivos do *kernel*, que facilitar a troca de informações entre os programas que rodam no espaço do *kernel*, como os *drivers*, com os programas que rodam no espaço do usuário — por isso, esse diretório é usado por diversos programas.
- `/tmp`: Diretório para armazenamento de arquivos temporários criados por programas.
- `/usr`: Contém a maior parte dos programas. Normalmente acessível somente como leitura.
- `/var`: Aqui são armazenados logs e arquivos variados que normalmente seriam escritos em `/usr`.

# Manipulação de arquivos

Abaixo estão listados comandos úteis para a manipulação de arquivos.

## `ls`

 - Utilidade: Listar os arquivos de um diretório.
 - Estrutura: `ls` *`[opções]`* *`[caminhos|arquivos]`*.
 - Opções:
	 - `-a`: Lista todos os arquivos, inclusive os ocultos, de um diretório.
	 -  `-l`:  Lista permissões, donos, grupos, tamanho em *bytes* e data de modificação dos arquivos.
	 - `-lh`: Edita o tamanho dos arquivos mostrando pela opção `-l`, ou seja, o tamanho dos arquivos serão exibidos em *Kbytes*, *Mbytes* ou *Gbytes* — o que o GNU/Linux julgar mais conveniente. 
 - Macetes: 
	  1. `ls -lha` é uma concatenação das opções `-l`, `-h`, `-a`. Quando se trata de listagem, talvez, seja o comando mais completo.
	  2. É possível listar vários diretório com um único comando. Por exemplo, o comando `ls . /` retornará a listagem do diretório atual e do diretório raiz do GNU/Linux.

## `cd`

- Utilidade: Entrar em um diretório. O usuário precisa ter a permissão de execução para entrar no diretório.
- Estrutura: `cd` *`[caminho|diretório]`*.
- Macetes: 
	1.  `cd /`: Levará ao diretório raiz do GNU/Linux.
	2.  `cd ~`: Levará para o diretório padrão do usuário que está operando o GNU/Linux.
	3.  `cd -`: Levará ao último diretório acessado.
	4.  `cd ..`: Levará à um diretório a cima.
	5. `cd ../ [caminho|diretório]`: Levará à um diretório a cima e  entrará, caso exista, no diretório do caminho informado.

## `pwd`

- Utilidade: Mostrar o nome e caminho do diretório atual.

## `mkdir`

- Utilidade: Criar um diretório no GNU/Linux.
-  Estrutura: `mkdir` *`[opções]`* *`[caminhos|diretórios]`*.
- Opções: 
  - `-p`: Caso os diretórios dos níveis acima não existam, eles também serão criados.
  - `-v`: Mostra uma mensagem para cada diretório criado.
- Macetes: 
  1. Para criar um novo diretório, o usuário deve ter permissão de gravação.
  2. É possível criar vários diretório com um único comando. Por exemplo, o comando `mkdir diretorio1 diretório2` criará dois diretórios — o `diretorio1` e o `diretório2`.

## `rmdir`

- Utilidade: Remover um diretório vazio do GNU/Linux.
- Estrutura: `rmdir` *`[caminhos|diretórios]`*.
- Macetes: 
	1. Para remove um diretório, o usuário deve ter permissão de gravação sobre ele.
	2. É possível remover vários diretório com um único comando. Por exemplo, o comando `mkdir diretorio1 diretório2` removerá tanto o `diretorio1` quanto o `diretório2` — desde que ambos estejam vazios.
	3. Para remover um diretório que contém arquivos, basta usar o comando `rm` com a opção `-r` seguida pelo diretório que deseja remover.

## `cat`

- Utilidade: Mostrar o conteúdo de um arquivo binário ou de texto.
- Estrutura:  `cat` *`[opções]`* *`[caminhos|arquivos]`*.
- Opções:
	- `-n`: Mostra o número das linhas enquanto o conteúdo do arquivo é mostrado.

## `touch`

- Utilidade: Criar um arquivo regular em branco
- Estrutura:  `touch` *`[caminhos|arquivos]`*.
- Macetes: 
	1. É possível criar vários arquivos com um único comando. Por exemplo, o comando `touch arquivo1 arquivo2` criará dois arquivos — o `arquivo1` e o `arquivo2`.
	2.  Para escrever algo no arquivo basta utilizar um editor de texto como por exemplo o Nano ou o Vim.

## `rm`

- Utilidade: Remover arquivos.
- Estrutura: `rm` *`[opções]`* *`[caminhos|diretórios]`*.
- Opções: 
	- `-i`: Pergunta antes de remover um arquivos.
	- `-v`: Mostra os arquivos a medida que são removidos.
	- `-r`: Remove arquivos em subdiretórios e em seguida o subdiretório.
- Macetes:
	1. `rm -r` *`[caminho|diretório]`* é utilizado para remover um diretório. 

## `cp`

- Utilidade: Copiar arquivos.
- Estrutura: `cp` *`[opções]`*  *`[origem]`* *`[destino]`*
-  Opções:
	- `-r` Copia arquivos dos diretórios e subdiretórios da origem para o destino.
	- `-v`: Mostra os arquivos a medida que são copiados.
	- `-l`: Faz o *link* simbólico no destino ao invés de copiar os arquivos.

## `mv`

- Utilidade: Mover arquivos.
- Estrutura: `mv` *`[opções]`*  *`[origem]`* *`[destino]`*
-  Opções:
	- `-v`: Mostra os arquivos a medida que são movidos.

## `find`
 
 - Utilidade: Buscar arquivos.
 - Estrutura: `find` *`[diretorio]`*  *`[opções]`* *`[expressão]`*
 - Opções:
     - `-atime`: Procurar arquivos acessados dentro de um intervalo de dias.
	 - `-mtime`: Procurar arquivos modificados dentro de um intervalo de dias.
	 - `-ctime`: Procurar arquivos criados dentro de um intervalo de dias.
	 - `-name`: Procura um arquivo pelo nome — é *case sensitive*.
	 - `-iname`: Procura um arquivo pelo nome — não é *case sensitive*.
	 - `-user`: Procura arquivos pelo usuário.
	 - `-goup`: Procura arquivos pelo grupo.
	 - `-perm`: Procura arquivos pela permissão.
	 - `-type`: Procura um arquivo pelo tipo. Os seguintes tipos são aceitos:
		 - `f`: arquivo regular;
		 - `d`: diretório;
		 - `b`: bloco;
		 - `c`: caractere;
		 - `l`: *link* simbólico;
		 - `p`: *pipe*;	
		 - `s`: *socket*.
 - Macetes: 
	1. Para fazer buscas  com o `-atime`, `-mtime` ou `-ctime` é interessante não somente indicar os dias, mas também especificar o intervalo. O `-` significa "a menos de", enquanto o `+` significa "a mais de". Por exemplo, o comando `find / -atime -2` busca arquivos acessados a menos de dois dias.
	2. É possível concatenar as opções e fazer buscas mais refinadas. Por exemplo: `find / -iname teste -user root`.

# Referências globais

Coringas, ou referências globais, é um recurso usado para especificar um ou mais arquivos do sistema de uma só vez. Este recurso permite fazer a filtragem do que será listado, copiado, apagado, buscados e etc. No GNU/Linux são usados 4 tipos de coringas, são eles:
- `*`: Faz referência a um nome completo ou restante de um arquivo.
- `?`:  Faz referência a uma letra naquela posição.
- `[ ]`: Faz referência a uma faixa de caracteres de um arquivo. Os padrões aceitos estão listados abaixo — caso qualquer um deles for precedido por um `^` significa que a expressão deve desconsiderar os caracteres indicados:    
    - `[a-z][0-9]`: Faz referência aos caracteres de `a` até `z` seguido de um caractere de `0` até `9`.
    - `[a,z][1,0]`: Faz referência aos caracteres `a` e `z` seguido de um caractere `1` ou `0` naquela posição.
    - `[a-z,1,0]`: Faz referência ao intervalo de caracteres de `a` até `z` ou `1` ou `0` naquela posição.   
- `{ }`: Expande e gera strings para pesquisa de padrões de um arquivo/diretório.
    - `X{ab,01}`: Faz referência a sequencia de caracteres `Xab` ou `X01`.
    - `X{a-z,10}`: Faz referencia a sequencia de caracteres `Xa-z` e `X10`.

# Compactadores

Compactadores são programas que diminuem o tamanho de um ou vários arquivo através de algoritmos muito avançados e complexos. A eficiência desses algoritmos pode ser mesurada pela  taxa de compactação — que é o quanto um arquivo foi compactado. Por exemplo, se o tamanho do arquivo for diminuído a metade após a compactação, a taxa de compactação foi de  2:1 ou dois para um.

É importante frisar que não é possível trabalhar diretamente com arquivos compactados. Para manipula-los  é necessário descompactar o arquivo. Entretanto, alguns programas descompactam o arquivo, o abrem e  assim que o trabalho estiver concluído o compactam novamente, tudo isso para facilitar a rotina de trabalho.

## Tipos de compactação

Existem, basicamente, dois tipos de compactação, são elas:

 - Compactação sem perda: Não causa nenhuma perda nas informações contidas no arquivo. 
 - Compactação com perda: É desenvolvida para atingir altas taxas de compactação, porém com perdas parciais dos dados. É aplicada a tipos de arquivos especiais, como músicas e imagens ou arquivos que envolvam a percepção humana.
 
## Arquivos de compactação

Para identificar um arquivo compactado e o programa utilizado para descompactá-lo, basta verificar a extensão do arquivo. Abaixo segue uma listagem dos programas mais comuns de descompactação e como utiliza-los:

- `gzip`:  É capaz de compactar arquivos para a extensão `.gz` e descompactá-los. Possui uma ótima taxa de compactação e velocidade.
	- Estrutura: `gzip` *`[opções]`* *`[arquivos]`*.
	- Opções:
		- `-d`: Descompacta um arquivo.
		- `-l` Lista o conteúdo de um arquivo `.gz`.
		- `-r`: Compacta diretórios e subdiretórios.
- `bzip2`:  É um novo compactador que vem sendo cada vez mais usado porque consegue atingir a melhor compactação em arquivos texto se comparado aos já existentes, em consequência sua velocidade de compactação também é menor; quase duas vezes mais lento que o `gzip`.
	- Estrutura: `bzip2` *`[opções]`* *`[arquivos]`*.
	- Opções:
		- `-d`: Descompacta um arquivo.
		- `-l` Lista o conteúdo de um arquivo `.bz2`.
		- `-r`: Compacta diretórios e subdiretórios.
- `zip`: Utilitário de compactação compatível com arquivos de extensão `.zip`.
	- Estrutura: `zip` *`[opções]`* *`[arquivo-destino]`* *`[arquivo-origem]`*.
	- Opções:
		- `-r`: Compacta diretórios e subdiretórios.
		- `-e`: Permite encriptar o conteúdo de um arquivo `.zip` através de senha. A senha será pedida no momento da compactação.
		- `-y`: Armazena links simbólicos no arquivo `.zip`. Por padrão, os links simbólicos são ignorados durante a compactação.
	- Macetes:
		1. Para a descompactação de arquivos `.zip` no GNU/Linux, é necessário o uso do `unzip` seguido do nome do arquivo que deseja descompactar.
- `rar`: É um compactador que trabalha com arquivos de extensão `.rar`.  
	- Estrutura: `rar` *`[ações]`* *`[opções]`* *`[arquivos]`*.
	- Ações:
		- `a`: Compacta arquivos.
		- `x`: Descompacta arquivos.
	- Opções:
		- `p`: Inclui senha no arquivo. Cuidado, pessoas conectadas ao sistema operacional podem capturar a linha de comando facilmente e descobrir a senha.
- `tar`:  Não é um compactador, ele apenas junta vários arquivos em um só.
	- Estrutura: `tar` *`[opções]`* *`[arquivo-destino]`* *`[arquivo-origem]`*.
	- Opções:
		- `-x`: Extrai arquivos `.tar`.
		- `-t`: Lista o conteúdo de um arquivo `.tar`.
		- `-c`: Cria um novo arquivo `.tar`.
	- Macetes:
		1. É comum encontrar arquivos `.tar` compactados em um arquivo `.gz` — nesses casos a extensão do arquivo será `.tar.gz`. Para descompactá-lo basta utilizar a opção `-z` para chamar o `gzip`.