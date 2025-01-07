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

`repeat` - controla a repetição do elemento(imagem) utilizado para preencher o fundo. Pode ser do tipo `no-repeat`, em que não haverá repetição, do tipo `repeat`, em que haverá repetição, e dod tipos `repeat-x` e `repeat-y`, em que haverá repetição no respectivo eixo

`position` - controla a posição do elemento(imagem) dentro do setor. Pode ser do tipo `center`, para centralizar, `top` para colocar no topo, `bottom`, para colocar no final, `right`, para direita, e `left`, para a esquerda

Para facilitar o processo, é possível colocar o color, imagem, repeat e position todos dentro de um único `background`, bastando separálos por espaços. Ex.: `background: cor url(localdaimagem) tipoderepetição posição;`

### Boder

Indicado por `border`, adiciona uma borda no setor. É preciso indicar a espessura, o tipo e a cor da borda para que ela apareça. Ex.: `border: espessura tipo cor;`. Existem vários tipos, mas os pricipais são `solid`, uma borda sólida, `dotted`, vários pontos, e deshed, vários traços.

Caso queira que a borda apareça somente em uma dos lados, é possível colocar depois do `border` um `-lado`. Ex.: `border-top`, `border-bottom`, `border-right` e `border-left`

Caso queira deixar a borda arredondada, é possível usar o `border-radius` com o quando ele será arredondado em pixels

### Magin

Indicado por `margin`, adiciona uma margem ao redor do setor

Pode ser prosseguido por `-top`, `-bottom`, `-right` ou `-left` para indicar a posição da margem

Tambem pode ser organizado dentro da própria `margin` colocando cada distância com referência no sentido horário. EX.: `margin: cima direita baixo esquerda`

### Padding

Indicado por `padding`, funciona como uma margem, mas ao ínves de só afastar o conteúdo, ele preenche o espaço com as carácterísticas do setor

Pode ser prosseguido por `-top`, `-bottom`, `-right` ou `-left` para indicar a posição da preenchimento

Tambem pode ser organizado dentro da própria `padding` colocando cada distância com referência no sentido horário. EX.: `padding: cima direita baixo esquerda`. Caso seja específicado somente um valor, todas as direções receberam o preenchimento referente a ele  

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

### Display

Indicado por `display`, define o comportamento do setor em relação relação às suas características e aos outros elementos da página. Possui quatro tipos principais:

`none` - o elemento não é mostrado

`inline` - os elementos se comportam como parte de uma única linha com caracteríscas de formatação definidas, tais como margem e tamanho, se adaptando somente ao tamanho do conteúdo. Além disso, como todos os elementos fazem parte da mesma linha, elas são mostradas de forma seguida (uma alinhada à outra)

`block` - os elementos se comportam como parte de um bloco separado que pode assumir características próprias de formatação, controlando margens e tamanho, sendo não só possível, mas também necessário em alguns casos, uma vez que o tipo block possui algumas configurações que nem sempre se encaixam no necessário para a página, como a largura em 100%. Devido ao fato de o bloco estar isolado em relação aos outros elementos, há uma quebra de linha padrão para o próximo elemento

`inline-block` - mistura características dos dois elementos, permitindo que seja feita a formatação do setor, mas também que eles possam ser alinhados

As tags já possuem um tipo de display padronizado, mas que pode ser modificado a depender da necessidade. Dentre as tags em block se destacam os titulos(h), parágrafos(p), tags semanticas como header, section e footer, entre outras. Dentre tags com inline estão o de links(a), imagens(img) entre outros

### Z-Index

Indicada por `z-index`, define a prioridade do setor em relação a sobre posição dos elementos, indo de -1 até 999, em que quanto maior for, maior a preferência para o elemento se sobrepor ao outro

### Position

Indicada por `position`, ela define ela posição do elemento em relação a algo, determinado pelo tipo, que pode ser:

`static` - em que ele não se move, fica na sua posição original

`relative` - em que ele se move em relação à sua posição original, sendo este deslocamneto determinado pelas propriedades `top`, `right`, `bottom` e `left`

`fixed` - matém o elemento em uma determinada posição independente da rolagem. Útil para fazer cabeçalho fixo ou botão de "entre em contato". É também possível deslocá-lo de sua posição original utilizando as propriedades `top`, `right`, `bottom` e `left`, mas nesse casso, a posição é relativa a tela

`absolute` - a posição do elemento é dada em relação ao setor que está inserido, determinado pelas propriedades `top`, `right`, `bottom` e `left`. Ex.: h1 dentro do body: a posição será relativa ao body; p dentro de div, a posição será dada em relação à div; div2 dentro da div1, a posição será dada em relação à div1. Para o funcionamento adequando do absolute, o setor acima do que está sendo usado não pode ser do tipo static, caso seja, a posição do elemento será dada em relação ao primeiro não static da que aparecer na hierarquia

`stick` - acompanha a rolagem, mas ficando sempre dentro do espaço definido em que está inserida

### Overflow

Indicada por `overflow`, define como a ocorrerá a visibilidade do conteúdo quando ele não se adequa à altura do setor. Possui vários tipos, como `visible`, em que o conteúdo é mostrado mesmo que vá além da altura definida, `hidden`, em que o conteúdo que fica para fora do espaço estipulado é escondido, `scroll`, em que adiciona uma barra de rolagem no setor para que o conteúdo possa ser visto, e, por fim, o `auto`, que se assemelha ao scroll, mas só o cria quando é necessário

A propriedade overflow só tem função quando o setor recebe uma definição para sua altura

O overflow também é utilizado para definir a existência ou não da barra de rolagem na página, isso por meio das prorpriedade `overflow-y` e `overflow-x`, que controlará a barra de rolagem do respectivoo eixo. Para faze-lá sumir, basta usar o parâmetro hidden

### Float

Indicado por `float`, define um setor como não pertencente ao fluxo comum da página, isolando-o no canto esquerdo ou direito, fazendo com que os demais itens se adequem ao espaço que sobra do lado

Caso queira que o fluxo normal seja retomado depois de um certo ponto, é possível usar a tag `clear:both` dentro do setor que retomará o fluxo

### Opacity

Indicado por `opacity`, controla a opacidade do conteúdo. Ela vai de 0.0 até 1.0, sendo 1.0 o 100% e 0.0 o 0%. Útil para efeito de transparência e criação de botões

### Text shadow e Box shadow 

Indicada por `text-shadow`, define um sombreamento para um texto. Seus parâmetros são definidos todos na mesma linha e os dois primeiros defininem a distância no eixo x e y, em px, o próximo é o blur/desfoque, também em px, e a cor. Algumas dicas referentes ao text shadow são: usar o efeito com distânciamento em 0 para criar um desfoque, adicionar mais de um efeito ao parâmetro separando eles por sombre e também procurar alguns efeitos já prontos na internet para implementar ou usar de inspiração

Indicada por `box-shadow`, funciona da mesma maneita que o text shadow, mas seu efeito é aplicado em um setor inteiro. Uma dica de uso para o box shadow é a criação de cards usando `box-shadow:0 4px 8px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19)`. Esse uso do box shadow é praticamente um padrão. Para o box shadow também é útil pesquisas na internet para se implementar ou se inspirar

## Botões

Para criar botões com links é possível utilizar o `:hover` após a indicação do setor para que ele tenha uma mudança quanto o ponteiro do mouse está por cima dele. 

Grafia: `setor:hover {}`

Ex: mudar de cor, aumentar o tamanho, prencher o espaço com cor, sublinhar etc

## Efeito dropdown

O efeito dropdown é a aquele em que um item de uma navbar se expande ao passar com o cursor do mouse por cima

Para fezê-lo usando somente css existem algumas dicas:

* quando se colococa uma tag/classe/id em frente a um `setor:hover` somente com um espaço seperando-os, ao passar o ponteiro pelo setor, a ação será feita no setor que está na sequência. A ideia é usar esse mecanismo para trocar o diplay de none para algum que corresponda a necessidade do dropdown (geralmente block) 

* o position dos li's usados para criar a navbar deve ser se algum tipo diferente do static (geralmente relative), isso porque o tipo da ul pertencente ao li que chamará o menu deve ser absolute, já que sua posição deve ser dada em relação à este li

* O top do ul com os conteúdos do dropdown deve ser de 100%, isso para que ele sempre seja mostrado diretamente a baixo do li que o chamará. O left deverá ser 0, uma vez que o li e o ul devem estar alinhados

* é interessantes que todos os li's da navbar tenham o mesmo tamanho, pois além de deixa-lá mais bonita, garante que os itens do dropdown também fiquem alinhados com o li que o chama

* o ul que será mostrado no dropdown deve ter margin e padding iguais a 0, pois, caso contrário, os itens não ficarão alinhados 

## Especificidade 

Especificidade se refere a como os CSS organiza a hierarquia das estilizações e qual vai ser lida pelo navegador

O primeiro tipo que vem na hierarquia é o inline, aquele que em que o style é colocado diretamente na tag, seguido então do interno e por último do externo

Porém, quando há uma class, ela possui uma hierarquia superior aos tipos interno e externo, então mesmo que estilo da class esteja sendo definido num arquivo externo, a class vai se sobrepor. Em resumo, a classe tem uma hierarquia superior à qualquer seletor simples (h1, p etc)

A mesma situação vale para os id's, que sobrepõem a tudo, então, na hierarquia: id > class > seletor simples, independente de uma ser interno e o outro ser externo

Resumindo: inline > id > seletor simples com classe > classe > seletor simples, em que caso algum eles se repita em no externo e no interno, o interno prevalece

## Regra important 

Caso coloque `!important` entre o : e ; de uma estilização, ela irá ignorar as regras de especificidade e prevalecerá na hierarquia. Essa regra pode ser uso para casos pontuais, mas é remondável que se evite o uso dela, uma vez que o cógigo pode se tornar extremamente confuso com o abuso desse recurso

## Efeito de gradiente

Para criar uma efeito de gradiente para o background utiliza-se o parâmetro `background-image: linear-gradient(direção, cor1, cor2, cor...)`. A direção pode ser definida pelo ângulo, com o valor seguido por deg, ou por indicação verbal, com 'to' seguido da direção em inglês, podendo ser colocada um direção do eixo x e outra do y para indicar uma diagonal

Também existe gradiente radial, que é definido por `background-image: radial-gradient(cor1, cor2, cor...)`

É possível adicionar um valor em porcentagem após cada cor para definir até que ponto ela ocupará na tela

## Dicas para efeitos de texto

É muito normal que falte espaço para terminados texto em setor, sendo necessário então algumas adaptações para que a leitura do site não seja prejudicada

Dentre alguma delas estão o uso da propriedade `white-space: nowrap;` que configura os texto para que ele não faça uma quebra de linha. Essa propriedade somada a um overflow do tipo hidden já faz que com que o texto grande não ocupe todo o espaço em disponível. Entretanto, ao utilizar esse método, o recorte entre a parte que é mostrada e a que não é do conteúdo fica brusco e estranho. Para melhorar essa situação é possível utilizar a propriedade `text-overflow: ellipsis`, que adicionará reticências antes do recorte, gerando um efeito visual melhor

Quando esse método é utilizado em cards, também é possível utilizar a propriedade o hover para modificar as propriedades do texto e do próprio card para tornálo dinâmico, com o seu tamanho se expandindo para mostrar todo seu conteúdo. Exemplo disso é deixar o `height: auto;` para que o card se adapte ao conteúdo e também usar o `white-space: normal;`, para que todo o conteúdo seja mostrado normalmente

## Media Queries

Media queries é um dos recursos/conceito mais importantes dentro do css. Sua função consite em definir determinados comportamentos para o site a depender do tipo de dispositivo em que o ele será exibido e o seu tamanho. O principal exemplo do uso de media queries está na adaptação de sites para que eles funcionem bem em dispositivos com diferentes tamanhos de telas, como celulares, tablets e computadores.

Alguns exemplos de parâmetros de media queries que são usados para tornar o site responsivo em diferentes dispositivos 

* Smartphones (600px para baixo): `@media only screen and (max-width: 600px) {...}`

* Dispositivos um pouco maiores, mas ainda pequenos (Pequenos Tablets e Smartphones + largos, 600px para cima): `@media only screen and (min-width: 600px) {...}`

* Dispostivos Médios (Tablets deitados, 768px para cima): `@media only screen and (min-width: 768px) {...}`

* Dispostivos Largos (laptops/desktops, 992px para cima): `@media only screen and (min-width: 992px) {...}` 

* Super Largos (Telas maiores laptops, desktops e até TVs, 1200px para cima): `@media only screen and (min-width: 1200px) {...}`

## Flexbox

Flexbox é um display extremamente útil, pois ele pode se configurado para se adaptar à diferentes dituações de tamnaho de tela. Para usar o flexbox basta colcar o parâmentro `display: flex;` para o setor

O tipo flex aceita uma série de outros parâmentros como:

`flex-direction` - que define a maneita de como o item estará disposto na página. Existem vários tipos, como `column` em que sua disposição ocorre ocupando toda à coluna diponível, semelhante ao tipo block. Existe também o `row`, que dispõe o conteúdo ao decorrer da linha, tal como o tipo inline-block. Também é possível adicionar um `-reverse` após o tipo para que mude o direcionamento padrão, em ao invés de ser da esquerda para direita, seria da direita para esquenda por ex

`flex-wrap` - define a quebra de linha ao fim da página para o setor. Por padrão, o tipo definido para wrap é o `nowrap`, em que não há quebra de linhas, porém, ao utilizar `wrap` ele fará a quebra de linha de acordo com o necessário para o tamanho do dispositivo

`flex-flow` - é uma junção das duas anteriores, em que basta colcocar primeiro o parâmetro do direction e depois o wrap separado por espaço

`justify-content` - controla o alinhamento horizontal dos itens. Possuem vários tipos, mas os principais são: `flex-start`, que faz o alinhamento à direita, `flex-end`, que faz o alinhamento a esquerda, `center`, que centraliza os itens, `space-between`, que matém todos numa mesma distância ocupando toda a largura disponível, e `space-around`, que cria um espaçamento uniforma em volta dos elementos

`align-items` - controla o alinhamento vertical dos itens. Possuem vários tipos, mas os principais são: `flex-start`, que faz o alinhamento à cima, `flex-end`, que faz o alinhamento em baixo, e `center`, que centraliza os itens

`align-content` - funcioo como o align items, porém atua de forma a tentar manter juntos todos os elementos, enquanto o de item espalha o conteúdo ao redor do espaço para ocupá-lo com o tipo de alinhamento

`flex-grow` - colocado dentro dos setores de uma div principal, estipula a varição de crecimento desses setores em relação aos outros, com o valor dado sendo uma relação de multiplicação do valor 

`flex` - colocado dentro dos setores de uma div principal, define a porcentagem do espaço que utilizará para dispor o conteúdo. Por meio desse parâmetro é possível configurar um grid para disposição do conteúdo
