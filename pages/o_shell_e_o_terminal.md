# O interpretador de comandos

Popularmente conhecido como *shell*, é o programa responsável por interpretar as instruções enviadas pelo usuário e seus programas ao *kernel*. Ele que executa comandos lidos do teclado ou de um arquivo executável. O GNU/Linux possui diversos tipos de interpretadores de comandos, entre eles o mais usado é o *bash*.

Os comandos podem ser enviados de duas maneiras para o *shell*, são elas:

 - Interativa: Os comandos são digitados e passados ao interpretador de comandos um a um. Neste modo, o computador depende do usuário para executar uma tarefa, ou próximo comando.
 - Não-interativa: São usados *scripts* para o computador executar os comandos na ordem encontrada no arquivo. Neste modo, o computador executa os comandos do arquivo um por um e dependendo do término do comando, o script pode checar qual será o próximo comando que será executado e dar continuidade ao processamento. 

# Terminal virtual

Também conhecido como "console" ou simplesmente "terminal", é um programa que executa um *shell*. Com ele é possível abrir várias seções de trabalho completamente independentes umas das outras. Essas seções podem está conectadas ao *shell* de um computador local ou remoto.

## Uso do terminal

Ao iniciar o terminal ele exibirá uma estrutura semelhante a esta: `usuario@maquina:local$`. Os caractéres antes do `@` são o nome do usuário que está operando a máquina. Após o `@` e antes do `:` é exibido o nome da máquina. Entre o `:` e o `$` é informado o local que está sendo acessado no sistema operacional. O `$` significa que o usuário logado não tem a credencial *root* — caso tivesse o simbolo exibido seria o `#`. Após esse conteúdo, é exibido um `|` ou um `-` ele indica que o terminal está apto a receber comandos e onde o texto inserido será colocado.