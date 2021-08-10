# Pacotes no GNU/Linux

No GNU/Linux os pacotes podem conter programas, bibliotecas de sistema ou mesmo coisas como papéis de parede e ícones. 

## Gerenciadores de pacotes

Os gerenciadores de pacotes são os  responsáveis pela administração dos pacotes. Nas distribuições GNU/Linux baseadas em RedHat os gerenciadores de pacotes são o `rpm` e o `yum`. Já nas distribuições GNU/Linux baseadas em Debian utiliza-se o `dpkg` e o `apt`. Na tabela a seguir serão apresentadas as diferenças entre eles:

| **`rpm`** | **`yun`** | **`dpkg`** | **`apt`** |
|   :--:  |   :--:  |   :--:   |     :--:    |
|Permite instalar pacotes locais que possuem a extensão `.rpm`. | Serve para fazer a instalação de um pacote compatível com distribuições baseadas em RedHat diretamente de um repositório — com as dependências.|  Permite instalar pacotes locais que possuem a extensão `.deb`.|  Serve para fazer a instalação de um pacote compatível com distribuições baseadas em Debian diretamente de um repositório — com as dependências.|

### Gerenciamento em distribuições Debian

A tabela a seguir condensa alguns comando relacionados ao gerenciador de pacote do `dpkg` veja:

| **Comando** |**Finalidade**|
|     :--:    |      :--:    |
| `dpkg -i` `pacote.deb` | Instalar pacote. |
| `dpkg -l` `pacote` | Verificar se o pacote foi instalado. |
| `dpkg -r` `pacote` | Remover o pacote. |

A tabela a seguir condensa alguns comando relacionados ao gerenciador de pacote do `apt` veja:

| **Comando** |**Finalidade**|
|     :--:    |      :--:    |
| `apt-get install` `pacote` | Instalar pacote. |
| `apt-cache show` `pacote` | Verificar se o pacote foi instalado. |
| `apt-get remove` `pacote` | Remover o pacote. |
| `apt-get update` `pacote` | Atualizar o pacote. |

É importante frisar que o comando `apt-get update` funciona para pacotes instalados com `dpkg`. 

### Gerenciamento em distribuições RedHat

A tabela a seguir condensa alguns comando relacionados ao gerenciador de pacote do `rpm` veja:

| **Comando** |**Finalidade**|
|     :--:    |      :--:    |
| `rpm -i` `pacote.rpm` | Instalar pacote. |
| `rpm -qa` `pacote` | Verificar se o pacote foi instalado. |
| `rpm -e` `pacote` | Remover o pacote. |
| `rpm -Uvh` `pacote.rpm` | Atualizar o pacote. |

A tabela a seguir condensa alguns comando relacionados ao gerenciador de pacote do `yum` veja:

| **Comando** |**Finalidade**|
|     :--:    |      :--:    |
| `yum install` `pacote` | Instalar pacote. |
| `yum remove` `pacote` | Remover o pacote. |
| `yum update` `pacote` | Atualizar o pacote. |

É importante frisar que o comando `rpm -qa` funciona para pacotes instalados com `yum`. 
