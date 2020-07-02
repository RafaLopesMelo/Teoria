# Regras para UI's

Quando queremos evoluir em determinada habilidade, o primeiro passo é conhecer alguns princípios e regras básicos antes de se aprofundar no assunto, e, obviamente, com a UI não seria diferente.
**Um bom visual não surge, é construído!** A chave para se tornar um bom designer é rigor. Você só vai melhorar suas capacidades de design se fizer um esforço consciente para tal.
Neste post vamos falar um pouco sobre os fundamentos da UI que precisam ser entendidos o quanto antes.

## A luz vem do céu

Isto é provavelmente a coisa não-óbvia mais importante para aprender sobre o design UI: luz vem do céu. Quando a luz vem do céu, ela ilumina o topo das coisas e cria sombras embaixo delas. O topo é mais claro, a base é mais escura.

**Nossas telas são planas, mas gastamos uma grande quantidade de arte fazendo com que pareçam 3D.**

Pense em botões, mesmo que ele seja plano, ainda sim há detalhes de luz manipuláveis.

* O botão não apertado tem uma borda inferior escura. "O Sol não chega lá".  

* O botão não apertado é discretamente mais claro no topo. Isto é porque imita uma superfície iluminada por cima.

* O botão não apertado possui uma sombra sutil.

* O botão apertado, ainda que continue mais escuro embaixo do que em cima, é **escuro por completo**. Isto faz referência à vida real: um botão apertado é mais escuro pois nossos dedos fazem sombra nele. Além disso, "a luz que vem do céu dificilmente chega nas partes mais baixas" (como um botão apertado).

Este exemplo foi apenas de um botão, e ainda sim há 4 pequenos efeitos de luz. Esta é a lição. Agora apenas aplicamos para todas as outras coisas.

### Elementos geralmente mais escuros: 

* Botões apertados

* Campos de Input de texto

* Radio button (não selecionado)

* Checkboxes

### Elementos geralmente mais claros: 

* Botões não apertados

* Popups

* Cards

### E quanto ao design "flat"?

Flat design é autoexplicativo. É um estilo visual em que os elementos não possuem nuances de luz ou sombra, são apenas linhas e formas de cores sólidas.

É uma interface elegante, mas, ainda sim, interfaces com efeitos 3D parecem mais naturais, as sombras nos ajudam a perceber para o que estamos olhando de fato.

 "Flatty" é o meio termo entre um 3D arrojado ("Skeuomorphic") e o flat design. Flatty permanece limpo, continua simples, mas possui **algumas sombras** para toques, deslizes e click's.

Vivemos em uma época de ouro do meio termo, flatty não sobrecarrega a tela e se mantém elegante, uma ótima pedida!

---

## Preto e branco primeiro

	Estilizar em escala de cinza antes de adicionar
	cores simplifica o mias complexo do design
	visual e te força a pensar no layout e
	posicionamento dos elementos.

Designers UX estão muito dentro do "mobile-first" atualmente. Isso significa pensar em como as páginas e interações vão funcionar em um celular antes de imaginar num monitor desktop.

Este tipo de restrição é ótima, clareia o pensar. Você começa a trabalhar no problema mais difícil (app em telas menores), e depois adota soluções para os mais fáceis (app em telas maiores).

Seguindo este pensamento, existe outra restrição similar: estilizar em preto e branco primeiro. Comece com o pior problema, faça um aplicativo usável e bonito de qualquer forma, mesmo sem as cores. **Adicione as cores por último, e, mesmo assim, tenha propósito!**

Ter muitas cores em muitos lugares é uma forma fácil de acabar com o simples. Esta técnica força você a pensar em coisas como espaçamentos, tamanhos e layout primeiro. E isto é primário quando se trata de interfaces simples e limpas!

Para a etapa da coloração, podemos tomar dois caminhos: escala de cinza + duas cores, ou escala de cinza + múltiplas cores de uma mesma tonalidade (hue).

**Usar múltiplas cores de uma ou mais bases de tom é a forma mais confiável de acentuar e neutralizar elementos sem fazer do design uma bagunça**

---

## Duplique os espaços em branco

Para fazer um UI que pareça estilizado, adicione espaço para respirar! É essencial criar uma hierarquia entre os elementos para harmonizar melhor o ambiente que seu site proporciona ao usuário. 

Se você já usou HTML, provavelmente já viu como as palavras se comportam por padrão e se posicionam na página. 
Basicamente, tudo fica esmagado no topo da tela, as fontes são pequenas, não existe absolutamente nenhum espaço entre as linhas, apenas pouquíssimo espaço entre os parágrafos, além de uma justificação nada agradável.
**Esteticamente falando, isto é horrível!**

Se, para você, utiliza como padrão a ausência de espaços em branco, é hora de mudar estes hábitos. Comece a pensar em espaços em branco como padrão, tudo começa com espaços em branco até que adicione elementos na página.

Coloque espaços entre as linhas!
Coloque espaços entre os elementos!
Coloque espaços entre os grupos de elementos!

**Analise o que funciona!**

---

## Tamanho para estabilizar a hierarquia

Quando o assunto é hierarquia visual, tamanho é um assunto essencial. Usando tamanhos apropriados transmitimos uma relação visual entre os elementos, criando um fluxo estável.

Tamanho é um dos motivos pelo qual o uso de grades é tão útil, você pode utilizá-las para ajudar a dimensionar elementos e transmitir importância. 

Uma vez que tenha determinado o tamanho de um elemento, use-o como base para criação dos outros. **	No design, consistência é tudo!**

---

## Aprenda os métodos de sobreposição de imagens e textos

Todo bom designer UI tem que saber colocar textos sobre imagens como um recurso apelativo.

### Method 0: Aplicar textos diretamente na imagem

Certos pontos devem ser levados em consideração para este método:

* A imagem deve ser escura e sem muito contraste.

* O texto tem que ser branco, limpo e simples.

* Teste em todas as telas para garantir que seja legível.

Seja cuidadoso com esta técnica, pode causar efeitos legais, mas **evite ao máximo**.

### Method 1: Sobreponha a imagem inteira

É provavelmente a **forma mais fácil** de colocar texto em imagens. Se a imagem original não for escura o suficiente, você pode sobrepô-la totalmente com uma camada preta translúcida.

Ainda que sobreposição com preto seja mais simples e versátil, é possível também utilizar camadas coloridas também.

### Method 2: Texto na caixa

É a forma mais simples e confiável. Coloque uma caixa preta levemente transparente e algum texto por cima. Se a sobreposição for opaca o suficiente, você pode ter **qualquer imagem** por baixo que o texto continuará legível.

Pode-se utilizar também outras cores de caixa, mas **seja criterioso!**

### Method 3: Borre a imagem

A uma forma incrível de realizar a sobreposição é borrar parte da imagem e adicionar texto por cima. Você pode também utilizar de áreas desfocadas de uma foto, mas tenha certeza de que o texto permaneça sempre sobre estas áreas.

### Method 4: Desvanecer a base

Esta técnica consiste em subitamente escurecer as partes inferiores de uma imagem e adicionar um texto branco sobre ela.

A princípio parece ser apenas um texto branco sobre uma imagem, mas na verdade existe um gradiente desde a metade da imagem com a cor preta e opacidade de 0% a 20%.

É interessante como esta técnica conversa com a **primeira regra: a luz vem do céu!** 

Sempre há a possibilidade de mesclar técnicas, mas, novamente, **seja criterioso!**

## Faça o texto aparecer e desaparecer

Estilizar textos para parecerem bonitos e apropriados é basicamente questão de contraste - faça textos maiores, mas mais claros.

Existem diversas formas de chamar atenção em textos, mas não é recomendado:

* **Sublinhar**: significa links atualmente, não vale a pena forçar qualquer outro significado.

* **Cor de fundo do texto**: incrivelmente comum, a maioria dos sites usa deste recurso para links em ==hover==.

* **Texto cortado**: recue, mago do CSS dos anos 90.

Podemos dividir todas as formas de estilizar textos em dois grupos: 

* **Aumentam a visibilidade**: grande, negrito, letras maiúsculos...

* **Diminuem a visibilidade**: pequeno, menor contraste, menos margem...

**Títulos de páginas são os únicos elementos a serem totalmente estilizados para ter visibilidade**

Se algum elemento precisar de ênfase, utilize dos dois grupos de recursos, isto permite que elementos diferentes possuam variados estilos.

## Use apenas boas fontes

### 1. Work Sans

Algumas vezes precisamos de uma fonte moderna, limpa e só uma pitada de descontração. Esta fonte é perfeita para este caso, ainda que seja pouco usada. Pode ser usada em textos corridos tranquilamente, mesmo com letras pequenas.

### 2. Roboto

Uma incrível fonte faz-tudo. Enquanto é a fonte padrão do Android, continua sendo pouco usada.

### 3. Metropolis

Grande substituta de fontes caras, capaz de passar diferentes ares dependendo do ==case== da fonte.

**Dica**: muitos iniciantes não utilizam do ==uppercase==, se deseja elevar seu nível, explore e abuse das diversas caixas de uma fonte.

### 4. Source Sans Pro

Esta fonte tem características como um caráter neutro, um toque de humanidade (melhor que fontes frias, apenas formas geométricas) e funciona muito bem para interfaces de usuário.

Funciona muito bem com **Source Serif** e **Source Code Pro**.

### 5. IBM Plex Sans

É suavemente peculiar e traz um sentimento mais técnico. è muito bem utilizado com fontes como **Plex Serif** e **Plex Mono**.

### 6. Feather icons

Bem menos utilizados que os ícones Font Awesome, mas que são capazes de trazer elegância e tornam a interface mais limpa.

---

### Referências:

> Artigo de Erik D. Kennedy (parte 1): [https://learnui.design/blog/7-rules-for-creating-gorgeous-ui-part-1.html](https://learnui.design/blog/7-rules-for-creating-gorgeous-ui-part-1.html)

> Artigo de Erik D. Kennedy (parte 2): [https://learnui.design/blog/7-rules-for-creating-gorgeous-ui-part-2.html](https://learnui.design/blog/7-rules-for-creating-gorgeous-ui-part-2.html)

> Artigo de Jonathan Z. White: [https://medium.com/free-code-camp/before-you-can-master-design-you-must-first-master-the-fundamentals-1981a2af1fda](https://medium.com/free-code-camp/before-you-can-master-design-you-must-first-master-the-fundamentals-1981a2af1fda)





 




