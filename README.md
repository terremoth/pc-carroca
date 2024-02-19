# Computador Carroça

![PC da Xuxa](https://github.com/terremoth/pc-carroca/blob/master/pc%20da%20xuxa.jpg)

Seu computador é uma carroça? (leia-se como: computador com requisitos baixos e limitados de hardware, ruim de utilizar)? Não tem problema, vamos torná-lo utilizável. Como apreciador da [The Suckless Universe](http://suckless.org/), e tendo um notebook BEM carroça:  
- Acer Aspire 5250 que foi me dado em 2011
- Processador AMD C-50 de 1GHz só, dual core com míseros 1mb de cache
- 4Gb + 4Gb Memória DDR3 1033mhz só, e ainda por cima single channel
- Webcam VGA que grava em 480p e não tem nem 3mp
- HD era de 250gb 5400rpm só, e pus um SSD WD Green, porém sem NAND Cache, infelizmente é SATA 2, mas já melhorou um pouco o cenário. (sempre quando for fazer upgrade de disco, procure por SSD's que tenham NAND Cache, por exemplo os da Crucial MX500 ou Samsung EVO)
- placa de vídeo AMD Radeon 6250 (512mb memoria/1ghz velocidade de memória/280mhz velocidade do nucleo), que nem video em 480p no YouTube roda direito
- sem saída HDMI, sem USB 3 e sem Bluetooth
- bateria viciada, só funciona na tomada
- layout de teclado americano
- WiFi só de 2.4ghz

posso te garantir que com esses requisitos bem desgraçados, eu rodo Laravel (PHP) com MySQL, NeoVim, com mais 2 abas no terminal abertas e umas 2 a 3 abas no Brave Browser abertas. "Praticamente Tirando leite de pedra". E funciona, roda. Às vezes é lento, mas roda!

Agora que você acredita como meu notebook é carroça, decidi fazer este guia para ajudar as pessoas que tem um computador ruim torná-lo 100% utilizável e funcional. 
Antes de mais nada...

## Ponha um Sistema Operacional adequado
Linux. Sem mais. "Ah mas e o Windows 7/XP aind..." - Não, não é uma opção negociável. "Ah mas eu quero usar pra jogar", então saiba que [Mais de 70% dos jogos da Steam já são possíveis de rodar no Linux](https://www.protondb.com/). E com essa carroça aí, você não poderá jogar lá muita coisa. Numa das seções abaixo fiz uma lista de games que sua carroça vai rodar.  

Você vai ter algumas alternativas de Linux boas. O que primeiro vamos ter que analisar é o quão carroça é seu computador. O que veremos abaixo de softwares e ferramentas farão bastante uso da linha de comando (terminal). E nem faça cara de desânimo, largue a preguiça, arregace as mangas e vamos melhorar esse cenário aí.  

Como sistemas operacionals, que já testei no meu notebook carroça, recomendo escolher algum destes:
1. [Lubuntu](https://lubuntu.me/) (é a versão mais minimalista do Ubuntu com a interface gráfica LXQT);
2. [Slax](https://www.slax.org/) (essa distro faz milagres em computadores realmente velhos e podres, mas não invente de fazer dual boot com ela, ela é bem mais leve, porém mais limitada que o Lubuntu);
3. [SliTaz](https://www.slitaz.org/) - distro Linux extremamente pequena, ressuscitadora de máquina velha
4. [TinyCore](http://tinycorelinux.net/) - distro muito minimalista
5. [Nano Linux](https://sourceforge.net/p/nanolinux/wiki/Home/) (provavelmente a menor distro de todas em tamanho de disco e uso de memória, ela não deve pesar mais que 25mb);
6. Quer ser um pouco mais "hardcore" e testar distros REALMENTE minimalistas? Existe a distro [Void](https://voidlinux.org/) e a [Alpine](https://www.alpinelinux.org/) (que é ainda mais minimalista usável que void)
7. Gosta de Arch Linux e se vira bem com linux e linha de comando? Vai de [Artix Linux](https://artixlinux.org/) que é o (Arch Linux [sem systemd](https://nosystemd.org/)), use st como terminal, dash ou mksh como shell, dwm + dmenu como window manager e vc terá um ambiente extremamente suckless;

Se não souber qual distribuição acima escolher, escolha [Lubuntu](https://lubuntu.me/).  

É sério, com essas distros acima, você consegue ressuscitar praticamente qualquer carroça velha.

### Notas para instalação nos Linux

Se você for um usuário antigo, que tem mais conhecimento em linux, tente instalar o sistema de arquivos XFS ou F2FS que são [drasticamente mais rápidos que Ext4 e BTRFS](https://www.phoronix.com/scan.php?page=article&item=linux-58-filesystems&num=1) e [link 2](https://www.phoronix.com/scan.php?page=article&item=linux-50-filesystems&num=1). Assim a velocidade de leitura e escrita no seu HD/SSD será ainda mais rápida.  

Na instalação do seu Linux, muitas vezes irá aparecer se você quer bootar ele usando softwares proprietários ou livres (livres ou "abertos" dependendo da nomenclatura que eles escolherem usar). Escolha os livres, simplesmente pelo fato de que como sua carroça é antiga, na maioria das vezes os firmwares proprietários não são atualizados há anos, diferente dos firmwares open source e/ou livres.

## Navegador Web, qual usar na carroça?
Firefox? Chrome? Icecat? Nem pensar!!! Vão sugar sua RAM e seu processador até travar todo seu sistema que já é podre.

Opções decentes (menos piores):
1. Brave
2. Falkon
3. Chromium
4. Midori
5. Palemoon
6. Dillo
7. surf
8. Não consegue nem executar javascript direito? Tente os browsers netsurf, lynx ou w3m, que são navegadores web pela linha de comando!

## Calculadora
bc, xcalc, apcalc, qalc

## Ferramentas de desenvolvimento
Via Terminal: [NeoVim](https://github.com/neovim/neovim), [Helix](https://github.com/helix-editor/helix)   
Via GUI: [VSCodium](https://github.com/VSCodium/vscodium) (Clne do VSCode sem ser bloated e totalmente livre),  [Geany IDE](https://github.com/geany/geany) (provavelmente a IDE mais leve que existe),  [Lapce](https://github.com/lapce/lapce) (Rust-based programming text-editor)


## Editores de texto simples (do tipo blocos de notas)
Via GUI: [LeafPad](https://github.com/tarot231/leafpad), [FeatherPad](https://github.com/tsujan/FeatherPad)  
Via Terminal: [nano](https://github.com/madnight/nano) (`sudo apt install nano`)

## Reprodução de vídeos
mpv media player  

Exemplo:

```$ mpv https://www.youtube.com/watch?v=XA2WjJbmmoM```   
```$ mpv caminho/do/video/arquivo.mp4```  

## Edição de vídeos (sim, é possível!)
> direto pela linha de comando!  
   
use o software `ffmpeg`
 

## Reprodução de áudio
mpv   

Exemplo:   

```$ mpv caminho/do/audio/arquivo.mp3```

### Download de vídeos
youtube-dl   

OBS: essa ferramenta baixa vídeos não só do youtube, mas de uma centena de sites (incluindo sites adultos).

## Chats
hexchat, irssi, weechat

## Linguagens de Programação pequenas, minimalistas que usam pouca RAM e pouco espaço em disco:
C puro, ShellScript (nativo nos linux), awk (nativo nos linux), tex, [A++](https://www.aplusplus.net/), [vlang](https://vlang.io/), [yabasic](http://www.yabasic.de/), [rebol](http://www.rebol.com/), [vimscript](https://learnvimscriptthehardway.stevelosh.com/) (nativo depois de instalar vim ou neovim), [wren](https://github.com/wren-lang/wren-cli/releases), [forth](http://www.softsynth.com/pforth/index.php), [StrongTalk](https://www.strongtalk.org/index.html), [LibertyEiffel](https://www.liberty-eiffel.org/), [red](https://www.red-lang.org/), [squirrel](http://www.squirrel-lang.org/), [newlisp](http://www.newlisp.org/), [potion](http://perl11.org/potion/index.html), [futhark](https://github.com/diku-dk/futhark), [lua](https://www.lua.org/), [GnuCOBOL](https://gnucobol.sourceforge.io/), [CLU](https://pmg.csail.mit.edu/CLU.html), [gforth](https://gforth.org/), [Snobol](https://www.regressive.org/snobol4/), Algol, [Pure](https://agraef.github.io/pure-lang/), [Cobra](http://cobra-language.com/downloads/) e [Clean](https://clean-lang.org/)

Linguagens como Python, Ruby, Java, C#, Pascal, Node (JS) são todas pesadas em questão de espaço e uso de memória (runtime e REPL). Eu pesquisei listas de pacotes e fiz muitos testes para trazer essas informações para vocês mastigada.

## Precisa jogar na carroça?
Baixe o client da Steam, o Wine e o DOSBox, e abaixo, uma lista de jogos que podem rodar pela idade (não testado).
Para nossa felicidade, o Linux está cada vez mais dando suporte a jogos.

## Games legais que teu computador carroça provavelmente vai rodar
[>>> Clique aqui e Dê uma olhada nesta lista <<<](games.md)  

Num geral, talvez jogos lançados anteriores a 2006...

"Nem esses rodam!"

Se contente então baixando os jogos de terminal (jogos pra jogar na linha de comando): pacote "bsdgames" e "bsdgames-nonfree"
Exemplo:  

```sudo apt install bsdgames -y```  

E você vai encontrá-los no diretório ```/usr/games``` 

Basta por exemplo você digitar no shell:

```$ /usr/games/snake```  

Tem mais de 30 jogos de linha de comando para você se divertir, todos ASCII-based (desenhados com texto/caracteres)

Outra opção é jogar [NetHack](https://nethack.org), podendo ser local ou on-line, por exemplo no servidor [hardfought](https://hardfought.org) ou [alt.org](https://alt.org/nethack/).

## Leitura de Documentos

### PDF
zathura, xpdf, qpdfview

### Abrir .txt
LeafPad, FeatherPad, Nano


#### FAQ (Frequently ANSWERED Questions)

1. "Linux é difícil". 

R: Não, é você quem está se fazendo de. Você nem tentou ainda. Não estamos mais em 2002 e é ridiculamente fácil instalar linux na sua máquina, já há suporte para dezenas de linguas, incluindo português obviamente. Usar o terminal é facil, você só precisa saber escrever(! avá). As ferramentas citadas acima mal precisam de manual, e as que tem, como VIM, já tem tutorial a rodo em português.

2. "VIM é difícil... Não consigo nem sair do editor... Como eu saio do VIM? Já tentei de tudo... 
```
quit
exit
^C
die
out
^C
helpme
^C
^Cshutdown"
...
```

R: Era só ter pressionado ESC e digitado :q!  
Para você aprender vim ou neovim, basta digitar ``vimtutor pt`` no terminal.

3. "Vale o esforço de dar vida novamente a este computador?" 

> R: O esforço é pequeno, vale à pena e a sensaçào é gratificante! Se você pensa em jogar fora, ao menos pense em ressuscitar ele e doar para quem não tem, ou pelo menos venda-o. Eu por exemplo me interesso por comprar/receber esses computadores velhos, conheço bastante gente que gosta, e se você chegou até aqui, provavelmente conhece alguém também que curte - quanto mais velha a carroça, mais legal :)

4. "Mas e O VLC não é melhor para reproduzir medias?"

> R: Eu particularmente acho uma ferramenta fantástica e um dos projetos open-source mais legais e úteis que conheço, mas devido a quantidade de recursos, peso em disco, uso de processador e RAM, não será nem de perto uma boa alternativa para sua carroça.

5. "Se eu melhorar meu hardware, como pôr mais memória, um SSD no lugar do meu HD..."

> R: Se você puder fazer upgrades baratos nele, como adicionar mais memória, pôr um SSD no lugar do HD, sua vida já melhora um bocado. Considere procurar por peças na OLX, no Marketplace do Facebook e no mercado livre, é fácil de encontrar peças baratas lá.

## AVANÇADO

ALERTA!!! Se você fizer isso abaixo, seu computador irá ficar vulnerável a alguns tipos de falhas de segurança. Em detrimento, acelerará o tempo de boot e um pouco a velocidade do computador num geral. É um tradeoff que você pode escolher correr. Não me responsabilizo caso seu linux seja hackeado ou invadido no futuro. Em computadores que não vão ficar conectados na internet com frequência não tem problema ter essa linha.

Você consegue acelerar um pouco seu computador carroça, se adicionar essa linha na variável `GRUB_CMDLINE_LINUX` no arquivo `/etc/default/grub`:  

`noibrs noibpb nopti nospectre_v2 nospectre_v1 l1tf=off nospec_store_bypass_disable no_stf_barrier mds=off mitigations=off`  

Ficando assim: `GRUB_CMDLINE_LINUX="noibrs noibpb nopti nospectre_v2 nospectre_v1 l1tf=off nospec_store_bypass_disable no_stf_barrier mds=off mitigations=off"`  

Agora salve o arquivo, e rode o comando:  
```sh
$ sudo update-grub2
```
para ele re-gerar os arquivos de boot.

## TO-DO
### Leitores/visualizadores de documentos
- doc, docx
- odf
- rtf
- md/markdown
- djvu/mobi
- cdr
- ppt/pptx
 
### upgrades
- hardware
- arch linux wiki performance tunning
- streaming gaming platforms

