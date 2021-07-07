# O que é GNU/Linux?

O GNU/Linux é um sistema operacional *Open Source* composto pelo *kernel* Linux, criado em 1991 por Linus Torvalds, e pelo conjunto de ferramentas GNU, lançado em 1983 por Richard Stallman.

## As distribuições GNU/Linux

No mundo todo existem grupos de pessoas, empresas e organizações que decidem usar o GNU/Linux como base para criar e distribuir, de diferentes formas, sistemas operacionais com outros *softwares*. Esses novos sistemas são chamados de distribuições GNU/Linux.

Existem distribuições que não nascem diretamente do GNU/Linux, mas sim de outras. Atualmente, as  distribuições GNU/Linux mais populares nasceram a partir do Debian ou do Red Hat.

# Arquivos no GNU/Linux

Os arquivos são utilizados para gravar dados. Eles, podem conter um texto, uma música, programa, planilha, etc. 

## Nomes e extensões

Para facilitar a identificação, cada arquivo deve ter um nome — lembrando que o GNU/Linux é *case sensitive*. No entanto, muitas vezes, não é possível localizar ou saber como utiliza-lo somente pelo nome, por conta disso, existem as extensões. 

A extensão são os caracteres separados do nome do arquivo por um  `.`, assim: `nome_arquivo.extensao`. O uso de extensões não é obrigatório na maioria das distribuições GNU/Linux, mas é conveniente o seu uso para determinar facilmente o tipo de arquivo e qual programa utilizar para abri-lo.

No GNU/Linux, quando o primeiro caractere do nome é um `.` significa que o arquivo em questão é oculto. Arquivos ocultos são ignorados, ou seja, eles existem, mas não são listados — a não ser que seja explicitado.

## Tipos de arquivos 

Existem dois tipos de arquivos, são eles: 

 - Arquivos de texto: Seu conteúdo é compreendido pelas pessoas. Um arquivo texto pode ser uma carta, um *script*, um programa de computador escrito pelo programador, arquivo de configuração, etc.
 - Arquivos binários: Seu conteúdo somente pode ser entendido por computadores. Um arquivo binário é gerado por um arquivo de programa através de um processo chamado de compilação.

# Diretórios no GNU/Linux

O diretório é o local utilizado para armazenar conjuntos de arquivos. Com os diretórios é possível manter os arquivos organizados. 

## Características dos diretórios GNU/Linux

 - O GNU/Linux é *case sensitive* e essa característica se aplica tanto aos arquivos quanto aos diretórios.
 - Assim como nos arquivos, os diretórios iniciados com `.` são ocultos.
 - No GNU/Linux não é permitido a existência de dois arquivos com o mesmo nome no mesmo diretório. As exceção são:
	 - Arquivos de mesmo nome com extensões diferentes. 
	 - Dois arquivos com o mesmo nome, e até com a mesma extensão, com um deles oculto.
 - No GNU/Linux não é permitido a existência de subdiretórios com o mesmo nome dentro do mesmo diretório. A exceção é:
	 - Dois subdiretórios com o mesmo nome, mas um deles oculto.
 - No GNU/Linux não é permitido a existência de um subdiretório e um arquivo com o mesmo nome. A exceção é: 
	 - Um subdiretório e um arquivo com o mesmo nome, porém um deles sendo oculto.

## Estrutura  de diretórios do GNU/Linux

O sistema GNU/Linux possui uma estrutura básica de diretórios. Essa estrutura também é conhecida como Árvore de Diretórios, porque é parecida com uma árvore de cabeça para baixo. Cada diretório do sistema tem seus respectivos arquivos que são armazenados conforme regras definidas pela *Filesystem Hierarchy Standard (FHS)* da seguinte forma:

- `/`: Diretório principal do sistema. Dentro dele estão todos os diretórios do sistema.
- `/bin`: É reservado para gravar comandos que serão utilizados por todos os usuários.
- `/boot`: Contém os arquivos necessários para a inicialização do sistema.
- `/cdrom`: Este diretório não faz parte do padrão de hierarquia *FHS*, porém ele ainda é encontrado em algumas distribuições GNU/Linux. É utilizado como local temporário para *CDs* e *DVDs* inseridos no computador — porém, o local padrão para essas mídias é o diretório `/media`.
- `/dev`:  Contém arquivos gerados pelos dispositivos de *hardware*, como processador, placa de vídeo, leitor de mídia etc.
- `/etc`: Guarda a maioria dos arquivos essenciais do sistema operacional do computador local, como configuração usados para controlar uma operação ou programa.
- `/home`: Local destinado para os arquivos dos usuários, com excessão do *root*.
- `/lib`: Contém diretórios e *links* simbólicos compartilhados pelos programas do sistema e módulos do *kernel*.
- `/lost+found`: Local para a gravação de arquivos ou diretórios corrompidos recuperados após uma verificação do sistema de arquivos — esse tipo de verificação ocorre na primeira reinicialização após um travamento no sistema.
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

# O interpretador de comandos

Popularmente conhecido como *shell*, é o programa responsável por interpretar as instruções enviadas pelo usuário e seus programas ao *kernel*. Ele que executa comandos lidos do teclado ou de um arquivo executável. O GNU/Linux possui diversos tipos de interpretadores de comandos, entre eles o mais usado é o *bash*.

Os comandos podem ser enviados de duas maneiras para o *shell*, são elas:

 - Interativa: Os comandos são digitados e passados ao interpretador de comandos um a um. Neste modo, o computador depende do usuário para executar uma tarefa, ou próximo comando.
 - Não-interativa: São usados *scripts* para o computador executar os comandos na ordem encontrada no arquivo. Neste modo, o computador executa os comandos do arquivo um por um e dependendo do término do comando, o script pode checar qual será o próximo comando que será executado e dar continuidade ao processamento. 

## Terminal virtual

Também conhecido como "console" ou simplesmente "terminal", é um programa que executa um *shell*. Com ele é possível abrir várias seções de trabalho completamente independentes umas das outras. Essas seções podem está conectadas ao *shell* de um computador local ou remoto.