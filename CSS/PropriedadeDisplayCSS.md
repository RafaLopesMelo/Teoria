# Propriedade Display CSS3

Provavelmente o maior causador das dores de cabeça dos programadores iniciantes ao trabalhar com CSS é a propriedade display.
Ela é a responsável por "barrar" certos estilos atribuídos aos elementos HTML dependendo de qual display está configurado para eles.

Neste post vou tentar esclarecer ao máximo conceitos relacionados aos principais valores possíveis e suas peculiaridades. Alguns demandam um estudo mais avançado, como o display flex e o display grid. Por isso, logo menos farei um post relacionado a eles.

Mas vamos logos ao que interessa!

## Display: Block

Faz com que os elementos HTML sejam renderizados como um bloco,  possuem um espaço em branco embaixo e em cima e **não permitem outros elementos ao lado**, exceto quando for declarado com a propriedade **float**.
Resumindo, tentar colocar um elemento com display block ao lado de outro pode causar muita dor de cabeça e exigir muita gambiarra. Para fazer issto existem outras possibilidades.

	Há diversos elementos que possuem esta propriedade como padrão, como
	as tags <p>, <h1>-<h6>, <section>, <header>, <footer> e <form>.

## Display: Inline

Faz com que os elementos HTML sejam renderizados como frases: todos os elementos em linha com um espaço entre eles, possuem sempre a menor largura e altura possível, sendo as propriedades *height* e *width* ignoradas.
Basicamente, o elemento passa a se comportar com um texto, cada "palavra" ocupa apenas o espaço de que precisa e ponto.

	Elementos que possuem esta propriedade como padrão são: a tag <span> e atag <a>.

## Display: Inline-Block 

Faz com que os elementos HTML possuam característica tanto display inline quanto block, sendo assim, são colocados um ao lado do outro, mas passam a aceitar as propriedades *height* e *width*.

Segue uma imagem bastante ilustrativa de cada propriedade:

<img src="https://i1.wp.com/www.tutorialbrain.com/wp-content/uploads/2019/06/CSS-Display.png?fit=474%2C379&ssl=1" alt="Exemplos dos displays mais básicos">

## Display: None

Faz com que o elemento HTML não seja renderizado, ou seja, se torna invisível na página. Além de invisível, ele não ocupa espaço na tela, sendo assim, não atrapalha o layout.
Pode parecer meio estranho e inútil querer sumir completamente com um elemento que você mesmo criou, mas diversas técnicas de efeitos bem interessantes em CSS são possíveis utilizando desta propriedade.

	São poucos os elementos que utilizam esta propriedade como padrão, o
	principal exemp-lo é a tag <script>

## Display: List-Item

Faz com que os elementos com esta propriedade sejam renderizados como uma lista, ou seja, aparecerá um marcador em cada item e serão dispostos um embaixo do outro.

	Este é o valor padrão de uma <ul> ou <ol>.

## Display: Table

Faz com que os elementos HTML sejam dispostos em forma de tabela. Os elementos aninhados a eles devem ser renderizados como table-row ou table-cell (respectivamente linhas ou colunas).

## Display: Grid

Este é um dos valores que exigem um pouco mais de estudo e aprofundamento, mais tarde haverá um post a respeito.
Basicamente, ele faz com que o elemento passe a ser um container dividido em linhas e colunas, como uma grade, facilitando o posicionamento e organização do layout.

## Display: Flex

Outro que exige um entendimento melhor para poder ser usado da melhor forma. Este é provavelmente o valor mais utilizado atualmente quando se quer organizar itens dentro de um container.
Eu, pessoalmente, vejo ele como um "facilitador de vidas" e utilizo muito em meus projetos.
Ele, em resumo, enfileira os itens em uma direção, como uma lista. Existem diversas configurações de alinhamento e posicionamento e vão ser explicadas uma a uma no post que farei especificamente sobre ele.
A grande vantagem de seu uso é tornar a página mais responsiva e dinâmica sem a "burocracia" do display grid.

Abaixo há uma comparação entre os dois últimos valores apresentados: 

<img src="https://qph.fs.quoracdn.net/main-qimg-273858213285396edb57d9bb175825d6" />

Espero que tenham gostado do conteúdo! E esperem por mais posts... :)

### Referências: 

> Site da W3Schools: [https://www.w3schools.com/cssref/pr_class_display.asp](https://www.w3schools.com/cssref/pr_class_display.asp)
>
> Site Maujor: [https://www.maujor.com/tutorial/propriedade-css-display.php](https://www.maujor.com/tutorial/propriedade-css-display.php)
>
> Site css-tricks: [https://css-tricks.com/almanac/properties/d/display/](https://css-tricks.com/almanac/properties/d/display/)











