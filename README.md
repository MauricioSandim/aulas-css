# Anotações 

## Tipos de uso do CSS

inline - dentro da tag

interno - no style dentro do head

externo - em um arquivo css externo chamado por um link dentro do HTML

## Seletores e Classes 

Para estilizar um site eu devo indicar a qual parte o estilo será dado

A seleção mais simples envolve tags, em que basta eu colocar a tag no arquivo css para dar um estilo. Porém é possível selecionar a parte que deve ser estilizada com outros recursos, como:

class - indicado com `.` no css, pode ser usado em mútiplas partes do html(não pode ser iniciado com um número). Também é possível fazer com que determinadas estilizações atreladas a uma class se aplique somente a um tipo de conteúdo, colocando a tag do conteúdo antes da class no css, ex: `tag.class {}`

id - dado no html, nomeia um trecho do conteúdo para que ele seja único na estilização, precisa ser indicado com `#` no css (o id não pode ser repetido e nem inciado em um número) 

\* - passa o estilo para todas as tags simultaneamente

Se múlttplas partes da estilização tiverem as mesmas características, pode-se colocá-las juntas separadas por uma vírgula para que todas elas recebem a estilização juntas, evitando redundâncias e simplificando o código

## Propriedades CSS

### Color 

Indicado pela tag `color`, define a cor da do texto. A cor pode ser indicado por um nome pré definido, mas é mais indicado utilizar o código hexadecimal, precedido por #, ou o padrão RGB da cor, indicado por rgb(000, 000, 000)

### Width e Height

Indicados por `width` e `height`, define a largura e altura do setor

Também existe o `max-width`, que indica o tamanho máximo que o setor pode ter (útil para o sistema de reponsividade) 

### Background

Define o que será mostrado no fundo do site. Ele é indicado por `background-`e o tipo que será atribuído. Os tipos podem ser:

`color` - para definir uma cor 

`image` - para definir uma imagem. A indicação da imagem deve ser feita por `url("local da imagem")`

`size` - usado para definir o preenchimento da imagem no fundo. Pode ser do tipo `contain`, que mantém a imagem nas suas proporções originais, criando um mosaico para preenchimento, ou `cover`, que esticará a imagem para ela se adaptar ao espaço que deve ser preenchido

`repeat` - controla a repetição do elemento(imagem) utilizado para preencher o fundo. Pode ser do tipo `no-repeat`, em que não haverá repetição, do tipo `repeat`, em que haverá repetição e dos tipos `repeat-x` e `repeat-y`, em que haverá repetição no respectivo eixo

`position` - controla a posição do elemento(imagem) dentro do setor. Pode ser do tipo `center`, para centralizar, `top` para colocar no topo, `bottom`, para colocar no final, `right`, para direita, e `left`, para a esquerda

Para facilitar o processo, é possível colocar o color, imagem, repeat e position todos dentro de um único `background`, bastando separálos por espaços. Ex.: `background: cor url(localdaimagem) tipoderepetição posição;`

### Boder

Indicado por `border`, adiciona uma borda no setor. É preciso indicar a espessura, o tipo e a cor da borda para que ela apareça. Ex.: `border: espessura tipo cor;`. Existem vários tipos, mas os pricipais são `solid`, uma borda sólida, `dotted`, vários pontos, e deshed, vários traços.

Caso queira que a borda apareça somente em uma dos lados, é possível colocar depois do `border` um `-lado`. Ex.: `border-top`, `border-bottom`, `border-right` e `border-left`

Caso queira deixar a borda arredondada, é possível usar o `border-radius` com o quando ele será arredondado em porcentagem ou pixels

### Magin

Indicado por `margin`, adiciona uma margem ao redor do setor

Pode ser prosseguido por `-top`, `-bottom`, `-right` ou `-left` para indicar a posição da margem

Tambem pode ser organizado dentro da própria `margin` colocando cada distância com referência no sentido horário. EX.: `margin: cima direita baixo esquerda`

### Padding

Indicado por `padding`, funciona como uma margem, mas ao ínves de só afastar o conteúdo, ele preenche o espaço com as carácterísticas do setor

Pode ser prosseguido por `-top`, `-bottom`, `-right` ou `-left` para indicar a posição da preenchimento

Tambem pode ser organizado dentro da própria `padding` colocando cada distância com referência no sentido horário. EX.: `padding: cima direita baixo esquerda`. caso seja específicado somente um valor, todas as direções receberam o preenchimento referente a ele  

### Text

Idincado por `text-`, define vária propriedades do texto. Pode ter vários tipos como:

`align` - define o alinhamento do texto, com vária opções como no centro, direita, esqueda, justificado etc

`decoration` - adiciona uma linha no texto, podendo ser `line-through`, que corta o texto, `underline`, que faz um sublinhado, `overline`, que faz a linha por cima do texto, e `none`, que tira o qualquer linha

`tranform` - transforma o texto para alguma característica específica, como caixa alta (`uppercase`), caixa baixa (`lowercase`) ou deixa somente a letra maiúscula (`capitalize`)

`indent` - identa o texto em um tamanho específicado em px, criando o efeito de uma parágrafo

Outras tags utilizadas na estilização de texto, mas que não fazer parte da tag text, são: 

`letter-spacing` - define o espaçamento em px entre as letras do texto. Também pode ser usado com valores negativos para aproximar as letras

`line-height` - define a altura da linha (geralmente definido com casas decimais)

`word-spacing` - define o espaçamento entre palavras em px

### Font

Indicado por `font-`, define características da fonte utilizada nos textos. Pode ser de vários tipos:

`family` - define qual fonte o texto vai usar

`size` - define qual vai ser o tamanho da fonte em px

`style` - define o estilo da fonte, como itálico, obliquo e o normal

`weight` - define a grossura da fonte, podendo ser indicada por um valor ou pelo `bold` para que ela fique em negrito

Para adicionar uma fonte externa vinda do google fontes no projeto, basta entrar na fonte desejada, ir na parte de import, colocar o parte precedida pelo @ dentro no início do arquivo css e depois chamar a fonte no family com o nome indicado no site. Lemrbrando que fonte possui direitos autorais, mas as do google podem ser usadas sem problemas

## Botões

Para criar botões com links é possível utilizar o `:hover` após a indicação do setor para que ele tenha uma mudança quanto o ponteiro do mouse está por cima dele. 

Grafia: `setor:hover {}`

Ex: mudar de cor, aumentar o tamanho, prencher o espaço com cor, sublinhar etc

