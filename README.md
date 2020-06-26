# Computador Carroça
Teu computador é uma carroça (leia: computador com requisitos baixos e limitados de hardware, ruim de utilizar)? Não tem problema, vamos torná-lo utilizável. Como apreciador da [The Suckless Universe](http://suckless.org/), e tendo um notebook carroça (Acer Aspire 5250) decidi fazer este post para ajudar as pessoas a terem um computador ruim porém 100% utilizável e funcional. 
Antes de mais nada...

## Ponha um Sistema Operacional adequado
Linux. Sem mais. "Ah mas e o Windows 7/XP aind..." - Não, não é uma opção negociável.
Você vai ter algumas alternativas de Linux boas. O que primeiro vamos ter que analisar é o quão carroça é seu computador. O que veremos abaixo de softwares e ferramentas farão bastante uso da linha de comando (terminal), nem faça essa cara de desânimo, larga a preguiça, arregaça as mangas e vamos melhorar esse cenário aí.

Como sistemas operacionals, que já testei no meu notebook carroça, recomendo:
1. Lubuntu (é a versão mais minimalista do Ubuntu com a interface gráfica LXQT);
2. Slax (essa distro faz milagres em computadores realmente velhos e podres, mas não invente de fazer dual boot com ela, ela é bem mais leve, porém mais limitada que o Lubuntu);
3. Nano Linux (provavelmente a menor distro de todas em tamanho de disco, não deve ter 20mb);
4. Gosta de Arch Linux e se vira bem com linux e linha de comando? Vai de Artix Linux (Arch [sem systemd](https://nosystemd.org/));

É sério, com essas distros acima, você consegue ressuscitar praticamente qualquer carroça velha.

## Sobre interfaces gráficas, desktop environments e window managers
Antes precisamos entender a diferença de um desktop environment de um window manager e ver os 2 tipos de window managers

## Navegador Web
Firefox? Brave? Chromium? Nem pensar!!! Vão sugar sua RAM e seu processador até travar todo seu sistema que já é podre.
Opções decentes:
1. Midori
2. Dillo
3. Palemoon
4. surf
5. Não consegue nem executar javascript direito? Tente os browsers netsurf, lynx ou w3m

*Eu espero realmente que você não tenha pensado no Google Chrome como uma opção!*

## Calculadora
bc, xcalc, apcalc, qalc

## Ferramentas de desenvolvimento
vim. Sem mais! 

## Text editors
vim, nano, leafpad (ui based)

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
c, sh, awk, [vlang](https://vlang.io/), [yabasic](http://www.yabasic.de/), [rebol](http://www.rebol.com/), [vimscript](https://learnvimscriptthehardway.stevelosh.com/), [wren](https://github.com/wren-lang/wren-cli/releases), [forth](http://www.softsynth.com/pforth/index.php), [red](https://www.red-lang.org/), [squirrel](http://www.squirrel-lang.org/), [newlisp](http://www.newlisp.org/), [potion](http://perl11.org/potion/index.html)

## Precisa jogar na carroça?
Baixe o client da Steam, o Wine e o DOSBox, e abaixo, uma lista de jogos que podem rodar pela idade (não testado).
Para nossa felicidade, o Linux está cada vez mais dando suporte a jogos.

## Games legais que teu computador carroça provavelmente vai rodar
1. Counter Strike (vulgo 1.6)
2. GTAs (III e Vice City)
3. Portal 1
4. DOOM's
5. Age Of Empires (1 e 2)
6. Max Payne 1
7. Just Cause 1
8. Need For Speed Underground (1 e 2)
9. Vampire - The Masquerade Bloodlines
10. Diablo 2
11. Half Life 1
12. Call of Duty 1
13. The Elder Scrolls (I, II, III)
14. Quake's (1, 2 e 3)

Num geral, talvez jogos anteriores a 2005...

"Nem esses rodam!"

Se contente então baixando os jogos "bsdgames" e/ou "bsdgames-nonfree"
Exemplo: sudo apt install bsdgames -y
E você vai encontrá-los na pasta /usr/games 

Basta por exemplo você digitar no shell:

```$ /usr/games/snake```

## Leitura de Documentos
### PDF
xpdf, qpdfview

### Abrir .txt
Vim

#### FAQ (Frequently ANSWERED Questions)

1. "Linux é difícil". 

R: Não, é você quem está se fazendo de. Você nem tentou ainda. Não estamos mais em 2002 e é ridiculamente fácil instalar linux na sua máquina, já há suporte para dezenas de linguas, incluindo português obviamente. Usar o terminal é facil, você só precisa saber escrever(! avá). As ferramentas citadas acima mal precisam de manual, e as que tem, como VIM, já tem tutorial a rodo em português.

2. "VIM é difícil... Não consigo nem sair do editor... Como eu saio do VIM? Já tentei de tudo... 
```quit
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

R: O esforço é pequeno, vale à pena e a sensaçào é gratificante! Se você pensa em jogar fora, ao menos pense em ressuscitar ele e doar para quem não tem, ou pelo menos venda-o. Eu por exemplo me interesso por comprar/receber esses computadores velhos, conheço bastante gente que gosta, e se você chegou até aqui, provavelmente conhece alguém também que curte - quanto mais velha a carroça, mais legal :)

4. "Mas e O VLC não é melhor para reproduzir medias?"

R: Eu particularmente acho uma ferramenta fantástica e um dos projetos open-source mais legais e úteis que conheço, mas devido a quantidade de recursos, peso em disco, uso de processador e RAM, não será nem de perto uma boa alternativa para sua carroça.

5. "Se eu melhorar meu hardware, como pôr mais memória, um SSD no lugar do meu HD..."

R: Se você puder fazer upgrades baratos nele, como adicionar mais memória, pôr um SSD no lugar do HD, sua vida já melhora um bocado. Considere procurar por peças na OLX, no Marketplace do Facebook e no mercado livre, é fácil de encontrar peças baratas lá.

## TO-DO
### Leitores/visualizadores de documentos
- doc, docx
- odf
- rtf
- md/markdown
- djvu/mobi
- cdr
- ppt/pptx

### other
- (colocar aqui link para meu .vimrc sem plugins)
- install tux games
