# Computador Carroça

![PC da Xuxa](https://github.com/terremoth/pc-carroca/blob/master/pc%20da%20xuxa.jpg)

Seu computador é uma carroça? (leia-se como: computador com requisitos baixos e limitados de hardware, ruim de utilizar)? Não tem problema, vamos torná-lo utilizável. Como apreciador da [The Suckless Universe](http://suckless.org/), e tendo um notebook BEM carroça:  
- Acer Aspire 5250 que foi me dado em 2011
- Processador AMD C-50 de 1GHz só, dual core sem cache
- 4Gb + 4Gb Memória DDR3 1033mhz só, e ainda por cima single channel
- Webcam VGA que grava em 480p e não tem nem 3mp
- HD era de 250gb 5400rpm só, e pus um SSD WD Green, porém sem NAND Cache, infelizmente é SATA 2, mas já melhorou um pouco o cenário
- placa de vídeo AMD Radeon 256mb que nem video em 480p no YouTube roda direito
- sem saída HDMI, sem USB 3 e sem Bluetooth
- bateria viciada, só funciona na tomada
- layout de teclado americano

Com esses requisitos bem desgraçados, eu rodo Laravel (PHP) com MySQL, Vim, com mais 2 abas no terminal abertas e umas 2 a 3 abas no Brave Browser abertas. "Praticamente Tirando leite de pedra", como diriam nossos amigos do nordeste do Brasil. E funciona, roda. Às vezes é lento, mas roda!

Agora que você acredita como meu noteebook é carroça, decidi fazer este post para ajudar as pessoas que tem um computador ruim torná-lo 100% utilizável e funcional. 
Antes de mais nada...

## Ponha um Sistema Operacional adequado
Linux. Sem mais. "Ah mas e o Windows 7/XP aind..." - Não, não é uma opção negociável. "Ah mas eu quero usar pra jogar", então saiba que [Mais de 70% dos jogos da Steam rodam são possíveis de rodar no Linux](https://www.protondb.com/). E com essa carroça aí, você não poderá jogar lá muita coisa. Numa das seções abaixo fiz uma lista de games que sua carroça vai rodar.  

Você vai ter algumas alternativas de Linux boas. O que primeiro vamos ter que analisar é o quão carroça é seu computador. O que veremos abaixo de softwares e ferramentas farão bastante uso da linha de comando (terminal). E nem faça cara de desânimo, largue a preguiça, arregace as mangas e vamos melhorar esse cenário aí.  

Como sistemas operacionals, que já testei no meu notebook carroça, recomendo escolher algum destes:
1. Lubuntu (é a versão mais minimalista do Ubuntu com a interface gráfica LXQT);
2. Slax (essa distro faz milagres em computadores realmente velhos e podres, mas não invente de fazer dual boot com ela, ela é bem mais leve, porém mais limitada que o Lubuntu);
3. Nano Linux (provavelmente a menor distro de todas em tamanho de disco, não deve ter 20mb);
4. Gosta de Arch Linux e se vira bem com linux e linha de comando? Vai de Artix Linux (Arch [sem systemd](https://nosystemd.org/));  
Se não souber, escolha Lubuntu.  

É sério, com essas distros acima, você consegue ressuscitar praticamente qualquer carroça velha.

## Navegador Web
Firefox? Chromium? Icecat? Nem pensar!!! Vão sugar sua RAM e seu processador até travar todo seu sistema que já é podre.
Opções decentes:
1. Brave
2. Midori
3. Dillo
4. Palemoon
5. surf
6. Não consegue nem executar javascript direito? Tente os browsers netsurf, lynx ou w3m

*Eu espero realmente que você não tenha pensado no *Google Chrome* como uma opção!*

## Calculadora
bc, xcalc, apcalc, qalc

## Ferramentas de desenvolvimento
NeoVim e/ou Geany 

## Text editors
NeoVim, nano, leafpad (ui based)

## Reprodução de vídeos
mpv media player 
Exemplo:

```$ mpv https://www.youtube.com/watch?v=XA2WjJbmmoM```
```$ mpv caminho/do/video/arquivo.mp4```

## Reprodução de áudio
mpv
Exemplo:

```$ mpv caminho/do/audio/arquivo.mp3```

### Donwload de vídeos
youtube-dl
OBS: essa ferramenta baixa vídeos não só do youtube, mas de uma centena de sites (incluindo sites adultos #ficaadica).

## Chats
hexchat

## Linguagens de Programação que não irão pesar
c, sh, awk, tex, [A++](https://www.aplusplus.net/), [vlang](https://vlang.io/), [yabasic](http://www.yabasic.de/), [rebol](http://www.rebol.com/), [vimscript](https://learnvimscriptthehardway.stevelosh.com/), [wren](https://github.com/wren-lang/wren-cli/releases), [forth](http://www.softsynth.com/pforth/index.php), [red](https://www.red-lang.org/), [squirrel](http://www.squirrel-lang.org/), [newlisp](http://www.newlisp.org/), [potion](http://perl11.org/potion/index.html), [futhark](https://github.com/diku-dk/futhark), [lua](https://www.lua.org/), GnuCOBOL, CLU, gforth, Snobol, Algol, [Pure](https://agraef.github.io/pure-lang/), [Cobra](http://cobra-language.com/downloads/)

## Precisa jogar na carroça?
Baixe o client da Steam, o Wine e o DOSBox, e abaixo, uma lista de jogos que podem rodar pela idade (não testado).
Para nossa felicidade, o Linux está cada vez mais dando suporte a jogos.

## Games legais que teu computador carroça provavelmente vai rodar
[>>> Clique aqui e Dê uma olhada nesta lista <<<](games.md)  

Num geral, talvez jogos lançados anteriores a 2005...

"Nem esses rodam!"

Se contente então baixando os jogos "bsdgames" e/ou "bsdgames-nonfree"
Exemplo:  
```sudo apt install bsdgames -y```  
E você vai encontrá-los no diretório ```/usr/games``` 

Basta por exemplo você digitar no shell:

```$ /usr/games/snake```

## Leitura de Documentos
### PDF
zathura, xpdf, qpdfview

### Abrir .txt
NeoVim, Nano

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

3. "Vale o esforço de dar vida novamente a este computador?" 

> R: O esforço é pequeno, vale à pena e a sensaçào é gratificante! Se você pensa em jogar fora, ao menos pense em ressuscitar ele e doar para quem não tem, ou pelo menos venda-o. Eu por exemplo me interesso por comprar/receber esses computadores velhos, conheço bastante gente que gosta, e se você chegou até aqui, provavelmente conhece alguém também que curte - quanto mais velha a carroça, mais legal :)

4. "Mas e O VLC não é melhor para reproduzir medias?"

> R: Eu particularmente acho uma ferramenta fantástica e um dos projetos open-source mais legais e úteis que conheço, mas devido a quantidade de recursos, peso em disco, uso de processador e RAM, não será nem de perto uma boa alternativa para sua carroça.

5. "Se eu melhorar meu hardware, como pôr mais memória, um SSD no lugar do meu HD..."

> R: Se você puder fazer upgrades baratos nele, como adicionar mais memória, pôr um SSD no lugar do HD, sua vida já melhora um bocado. Considere procurar por peças na OLX, no Marketplace do Facebook e no mercado livre, é fácil de encontrar peças baratas lá.

## TO-DO
### Leitores/visualizadores de documentos
- doc, docx
- odf
- rtf
- md/markdown
- djvu/mobi
- cdr
- ppt/pptx

