# LEIA OU MORRA

Nesta página pretendo mostrar como compilar seu proprio kernel do Linux de forma mínima. Vai servir para qualquer Linux.  
**Porém**, nesse mesmo diretório, estarei colocando também kernels `.deb` especificamente para o Acer Aspire 5250, portanto **não instale esses se você não tem o mesmo notebook nem um sistema operacional debian-like**.  

Dito isto, vamos ao tutorial

## Compilando seu próprio Kernel
### Requisitos
- (opcional porém recomendado) Outro computador mais potente e rápido para compilar, afinal você não quer esperar metade de dia inteiro para ter o kernel compilado no seu notebook carroça.  
- saber mexer o básico no linux
- paciência (é uma virtude inclusive)

## Baixar o kernel
Na máquina que você quer instalar o novo kernel (no meu caso, no meu notebook da xuxa), abra o terminal e baixe o último kernel que você quer instalar, 
no meu caso eu quis baixar a última versão stable do momento, a 6.15.4:

```sh
wget https://cdn.kernel.org/pub/linux/kernel/v6.x/linux-6.15.4.tar.xz
```
Se quiser baixar outra só copiar o link de outra versão em [https://www.kernel.org/pub/linux/kernel/](https://www.kernel.org/pub/linux/kernel/)

Agora descompacte:

```sh
tar -xf linux-6.15.4.tar.xz
```
entre no diretório do kernel:
```sh
cd linux-6.15.4
```

Agora atualize seu linux, no meu caso como é um debian-like:
```sh
sudo apt update && sudo apt upgrade -y
```

Agora você precisa instalar as ferramentas para compilar o kernel, mesmo que você vá compilar em outra máquina como farei, precisa nas 2 para rodar alguns scripts:
```sh
sudo apt install build-essential libncurses-dev bison flex libssl-dev libelf-dev bc perl debhelper libdw-dev
```

Agora vamos pegar e gerar um arquivo de "`.config`" da configuração atual e mínima do seu notebook carroça:
```sh
scripts/kconfig/streamline_config.pl > .config.min
```
Esse "scripts" é uma pasta que está dentro do kernel baixado, portanto não se esqueça de ter seguido as etapas anteriores para estar na mesma pasta.  

Agora execute para mover para:

```sh
mv .config.min .config
```

E então execute:
```sh
yes '' | make olddefconfig
```

Se der algum "warning" ou "not found" de configs, fique tranquilo, pode ignorar.  

Etapa **opcional** e avançada, caso queira tirar manualmente algum módulo, driver etc, do seu kernel que será compilado.  
Dá para você tirar drivers/modulos como bluetooth, usb3 caso não tenha, hdmi entre outras coisas que notebooks velhos não tem mas o kernel vai acabar colocando:
```sh
make menuconfig
```

Pronto, independente de ter ou não feito a etapa opcional anterior, terá em ambas gerado um ".config" nessa mesma pasta onde você está (dentro da pasta do kernel) com tudo que é necessário nesse arquivo para gerar um kernel enxuto e simples.  

Agora, CASO você vá compilar na outra máquina mais potente, como eu fiz:  

Vá nela, refaça o processo acima: baixe o kernel, descompacte, entre na pasta, instale as mesmas dependencias, e copie o `.config` do notebook gargalado para dentro da pasta do kernel do computador mais potente.
A gente tá basicamente pegando a `.config` do seu notebook carroça e mandando o seu computador mais potente compilar um kernel para o notebook velho.  
A gente só precisava até então saber quais módulos e drivers precisarão ser compilados para o notebook carroça.

Agora, independente se você vai compilar o kernel no notebook carroça, ou em outra máquina mais potente, certifique-se de que ainda está dentro da pasta do kernel - que é no mesmo lugar do arquivo .config deve estar, execute:
```sh
make -j$(nproc)
```

Agora vai levar vários minutos. Levou um pouco mais de 1 hora e meia no meu computador mais potente, e certamente teria levado umas 8 horas (pelo menos) no meu notebook carroça. Agora tem que esperar...

![image](https://github.com/user-attachments/assets/1bf1a284-0a69-4f11-a9be-20ebf4a2e92d)

Depois de compilado, se não der nenhum "Error: ..." terá sido criada algumas pastas no mesmo diretório do seu kernel. Ignore. Vamos compilar os modulos agora:

```sh
make modules -j$(nproc)
```
Essa parte é até que rápida. Na minha máquina mais potente levou 5 minutos.  

Depois de terminar, vamos agora criar um pacote "`.deb`" do seu kernel para poder instalar no seu notebook carroça:

```sh
make bindeb-pkg
```

Se não mostrar nenhum "Error" no final, deu certo. O kernel ".deb" foi colocado no diretório acima (anterior) ao da pasta do seu kernel, que é onde você está agora, portanto execute:
```sh
cd ../
```

se você der um comando `ls` você verá algo como:

```
~ $ ls 
linux-6.15.4         linux-headers-6.15.4_6.15.4-3_amd64.deb    linux-image-6.15.4_6.15.4-3_amd64.deb  linux-upstream_6.15.4-3_amd64.buildinfo
linux-6.15.4.tar.xz  linux-image-6.15.4-dbg_6.15.4-3_amd64.deb  linux-libc-dev_6.15.4-3_amd64.deb      linux-upstream_6.15.4-3_amd64.changes
```
O que é cada um:

`linux-6.15.4` - É o diretório onde você estava  
`linux-6.15.4.tar.xz` - O arquivo que você tinha descompactado que virou a pasta onde você estava  
`linux-image-6.15.4_6.15.4-3_amd64.deb` -	Kernel e módulos (principal e o que instalaremos)  
`linux-headers-6.15.4_6.15.4-3_amd64.deb` - Headers (úteis se for compilar drivers de terceiros)  
`linux-libc-dev_6.15.4-3_amd64.deb` - Headers da libc para compilar coisas  
`linux-image-6.15.4-dbg_6.15.4-3_amd64.deb` - Kernel com símbolos de depuração (opcional e grande se vc quiser fazer debugging)  
`linux-upstream_6.15.4-3_amd64.changes` -	Log da compilação (metadado do build, ignora)  
`linux-upstream_6.15.4-3_amd64.buildinfo` - Informações do ambiente de build (ignora)  

Agora o principal: `linux-image-6.15.4_6.15.4-3_amd64.deb`, renomeei para `linux-image-6.15.4-3_amd64.deb`, para não repetir 2 vezes a versão no nome do arquivo.  

Pegue esse arquivo e mande/copie para o notebook carroça (pus no Google Drive e baixei pelo carroça), ou, caso já esteja nele, em ambos os casos vá na pasta onde você baixou ou colocou o .deb e instale:

```sh
sudo dpkg -i linux-image-6.15.4-3_amd64.deb
```
e
```sh
sudo update-grub2
```

Pronto, instalado, mas você quer que ele seja executado e usado, então vamos reiniciar o notebook carroça, entrar no grub e mudar para este mais recente:
```sh
sudo reboot
```

Quando tiver reiniciando, fique pressionando `shift` para ele entrar na tela inicial do grub caso ela não apareça sozinha.

Na tela do grub vá em "Advanced options" e mude para o Kernel 6.15.4 na lista (ou para a versão do kernel que você acabou de instalar) e dê enter. Pronto.

### Caso der algum erro
e não inicializar por algum motivo, anote ou tire foto do erro para pesquisar depois. Reinicie seu computador ligando e desligando pelo botão de power dele mesmo, 
e na tela do grub de novo, vá em "Advanced options" e volte pro kernel que tava antes que funcionava, tente descobrir o motivo e conserte, e então refaça as etapas acima corrigindo onde necessário.  

**Se tudo der certo** e tenha iniciado corretamente, abra o terminal e digite:

```sh
uname -r
```

E você verá algo como `6.15.4` ou a versão que você escolheu. Isso significa que deu tudo certo e está funcionando conforme esperado!  
Parabéns, você compilou e pôs em produção o kernel do Linux, ou digamos, o Linux propriamente dito! Fim.
