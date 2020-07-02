# Componentes e Props

Componentes permitem dividir a UI em partes independentes e reutilizáveis. Em essência, são como funções Java Script, aceitam entradas ('props') e retornam elementos React que descrevem o que aparecerá na tela.

---

## Componentes de função

A	maneira mais fácil de de criar um componente é escrevendo uma função JavaScript:

	function Welcome(props) {
		return <h1>Hello,{ props.name } </h1>;
	}

Esta função é um elemento React válido pois recebe um único argumento ('props') com dados e retorna um elemento React. Estes são chamados de **componetes de função**, pois se tratam, literalmente, de funções JavaScript.

---

## Componentes de classe

Pode-se também usar uma classe ES6 para definir um componente:
	
	class Welcome extends React.Component{
		render() {
			return <h1> Hello, { this.props.name } </h1> 
		} 
	}

###  <div align='center'> Ambos os componentes acima são equivalentes do ponto de vista do React!

---



## Compondo Componentes

Componentes podem se referir a outros componentes, podemos assim utilizar a mesma abstração de componente para qualquer nível de detalhe (um botão, um formulário, uma tela, um aplicativo).
É recomendado que as props sejam nomeadas de acordo com o próprio componente, e não de acordo com o contexto em que está inserido!

### <div align='center'>Não tenha medo de dividir componentes em componentes menores!

---

## Props são somente leitura

Independente do tipo de componente em questão, ele **nunca** deve modificar seus próprios props, ou seja, mantendo as funções "puras", como são conhecidas.
Para estes casos existem os "states", que será explicado em outro tópico.

### <div align='center'> Esta é a única regra estrita do React!

----

### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/components-and-props.html](https://pt-br.reactjs.org/docs/components-and-props.html)


