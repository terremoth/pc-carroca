# Computador Carroça
Teu computador é uma carroça? Não tem problema, vamos torná-lo utilizável

## Ponha um Sistema Operacional adequado
Linux. Sem mais. "Ah mas e o Windows 7/XP aind..." - Não, não é uma opção negociável.
Você vai ter algumas alternativas de Linux boas. O que primeiro vamos ter que analisar é o quão carroça é teu computador. O que veremos abaixo de softwares e ferramentas fará bastante uso da linha de comando (terminal/shell).
Como sistemas operacionals, que já testei no meu notebook carroça, recomendo:
1. Lubuntu (é a versão mais minimalista do Ubuntu com interface gráfica, usando a LXDE/LXQT)
2. Slax (essa distro faz milagres em computadores realmente velhos, mas não invente de fazer dual boot com ela)
3. Nano Linux (provavelmente a menor distro de todas em tamanho de disco)
4. Puppy Linux (cheio de frufrus, mas costuma rodar em carroças)
5. Gosta de Arch Linux e se vira bem com linux? Vai de Artix Linux

É sério, com essas distros acima, você consegue ressuscitar praticamente qualquer carroça.

## Navegador Web
Firefox? Brave? Chromium? Nem pensar!!! Vão sugar sua RAM e seu processador até travar todo seu sistema.
Opções decentes:
1. Midori
2. Dillo
3. surf
3. Não consegue nem executar javascript direito? Vai de Netsurf

- Eu espero realmente que você não tenha pensado no Google Chrome como uma opçào!

## Calculadora
bc

## Ferramentas de desenvolvimento
Vim. Sem mais! (colocar aqui link para .vimrc sem plugins)

## Reprodução de vídeos
mpv media player 
Exemplo:
$ mpv https://www.youtube.com/watch?v=XA2WjJbmmoM 
$ mpv caminho/do/video/arquivo.mp4

## Reprodução de áudio
mpv
Exemplo:
$ mpv caminho/do/audio/arquivo.mp3

### Donwload de vídeos
youtube-dl
OBS: essa ferramenta baixa vídeos não só do youtube, mas de uma centena de sites (incluindo sites adultos #ficaadica).

## Chats
pidgin

## Linguagens de Programação que não irão pesar
C, sh, awk, yabasic

## Precisa jogar na carroça?
Baixe o client da Steam, o Wine e o DOSBox, e abaixo, uma lista de jogos que podem rodar pela idade (não testado).
Para nossa felicidade, o Linux está cada vez mais dando suporte a jogos.

## Games legais que teu computador carroça provavelmente vai rodar
1. Counter Strike 1.6
2. GTA Vice City
3. Portal 1
4. DOOM's
5. Age Of Empires 1 e 2
6. Max Payne 1
7. Just Cause 1
8. Need For Speed Underground 2
9. Vampire - The Masquerade Bloodlines
10. Diablo 2
11. Half Life 1
12. Call of Duty 1

Num geral, talvez jogos anteriores a 2005...

"Nem esses rodam!"

Se contente então baixando os jogos "bsdgames" e/ou "bsdgames-nonfree"
Exemplo: sudo apt install bsdgames -y
E você vai encontrá-los na pasta /usr/games 

Basta por exemplo você digitar no shell:
$ /usr/games/snake

## Leitura de Documentos
### PDF
xpdf

### DOC, DOCx

### ODF

### RTF

### MD/Markdown

### TXT
Vim

### DJVU

### MOBI

### CDR

### PPT, PPTx

#### FAQ (Frequently ANSWERED Questions)
1. "Linux é difícil". 

R: Não, é você quem está se fazendo de. Você nem tentou ainda. Não estamos mais em 2002 e é ridiculamente fácil instalar linux na sua máquina, já há suporte para dezenas de linguas, incluindo português obviamente. Usar o terminal é facil, você só precisa saber escrever(! avá). As ferramentas citadas acima mal precisam de manual, e as que tem, como VIM, já tem tutorial a rodo em português.

2. "VIM é difícil... Não consigo nem sair do editor... Como eu saio do VIM? Já tentei de tudo... 
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

R: Era só ter pressionado ESC e digitado :q!

3. "Vale o esforço de dar vida novamente a este computador?" 

R: O esforço é pequeno, vale à pena e a sensaçào é gratificante! Se você pensa em jogar fora, ao menos pense em ressuscitar ele e doar para quem não tem, ou pelo menos venda-o. Eu por exemplo me interesso por comprar/receber esses computadores velhos, conheço bastante gente que gosta, e se você chegou até aqui, provavelmente conhece alguém também que curte - quanto mais velha a carroça, mais legal :)

4. "Mas e O VLC não é melhor para reproduzir medias?"

R: Eu particularmente acho uma ferramenta fantástica e um dos projetos open-source mais legais e úteis que conheço, mas devido a quantidade de recursos, peso em disco, uso de processador e RAM, não será nem de perto uma boa alternativa para sua carroça.

5. "Se eu melhorar meu hardware, como pôr mais memória, um SSD no lugar do meu HD..."

R: Aí seu computador deixa de ser uma carroça e foge do escopo deste guia.

