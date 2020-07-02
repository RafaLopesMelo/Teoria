# React Hooks

Hooks são funções que permitem a você ligar-se aos recursos de ==state== e ==ciclo de vida== do React a partir de **componentes funcionais**.

Eles **não funcionam** dentro de **componentes de classe**.

## Hook de State

O Hook de State nos permite utilizar estados dentro de um componente funcional, funcionalidade que só existia dentro de componentes de classe.
Este Hook recebe um único valor, correspondente ao valor inicial do estado, podemos passar um número, string, array, objeto, etc.
Ele sempre retorna um par de valores: o estado atual e uma função que atualiza o estado, por isso utilizamos a seguinte sintaxe:


	import React, { useState } from 'react';
	
	function Example() {
		const [ counter, setCounter ] = useState(0);
	}

## Hook de Efeito

O Hook de Efeito, ==useEffect== , segue a mesma funcionalidade do ==componentDidMount==, ==componentDidUpdate== e ==componenteWillUnmount==, que eram apenas possíveis em **componentes de classe**. Nele, mudamos o título do documento, buscamos dados ou fazendo chamadas à API, por exemplo.

Os Hooks de Efeito são declarados **dentro do componente**, para que tenham acesso às props e states. Por padrão, o React executa o useEffect **após cada renderização**, incluindo a primeira (componentDidMount e componentDidUpdate). Efeitos também podem "limpar" (component- WillUnmount) **retornando** uma função após a execução deles.

Podemos utilizar **diversos Hooks de Efeito** num mesmo componente para separar lógicas não relacionadas. Não há problemas quanto a isto, todos os efeitos serão aplicados **na ordem** em que foram declarados a cada especificação.

Observe um exemplo de uso do Hook de Efeito:

	import React, { useEffect, useState } from 'react';

	export default function HookExample() {

		const [ counter, setCounter ] = useState(0);
	
		useEffect(() => {
		
			document.title = setCounter(counter + 1);
			return () => { setCounter(0) }
			
		}, [ counter ])
	}

O primeiro parâmetro é uma **função** que será executada a **cada renderização**, já o segundo parâmetro é opcional e limita este Efeito a ser executado apenas quando **determinada prop ou state atualizar**. O return localizado no primeiro parâmetro se trata de uma função que será executada quando o **componente for desmontado**, equivale ao ==componentWillUnmount==.

## Hook de contexto

O Contexto é indicado para compartilhar dados que podem ser considerados "globais" para a árvore de componentes. Usuário autenticado e idioma preferido são bons usos.

O contexto do React é inicializado com o React createContext no topo da aplicação, juntamente com um valor inicial, no caso, o tema "claro", caso omitido, utilizará o valor do Provider mais próximo. 

	// Contexto de tema, neste caso
	// src/ThemeContext.js
	
	import React from 'react';
	
	const ThemeContext = React.createContext('light');
	
	export default ThemeContext;

O component Context's Provider pode ser usado para passar o tema atual para a árvore abaixo, neste caso, passamos o tema "escuro", Provider's podem ser aninhados para substituir valores mais ao fundo da árvore:

	// src/ComponentA.js
	
	import React from 'react';
	import ThemeContext from './ThemeContext';
	
	const A = () => {
		<ThemeContext.Provider value="dark">
			<ToolBar /> 
		</ThemeContext.Provider>
	}; 

Todos os componentes que utilizam o useContext() que são descendentes dos Providers são renderizados novamente sempre que o "value" do Provider for atualizado.

O useContext() aceita um contexto e retorna seu valor atual, este valor é definido pela prop "value" do Provider mais próximo.

Caso a re-renderização seja custosa, você pode otimizá-lo com memoization.

	const themes = {
		light: {
			foreground: "#000000",
			background: "#eeeeee"
		},
		dark: {
			foreground: "#ffffff",
			background: "#222222"
		}
	};
	
	const ThemeContext = React.createContext(themes.light);
	
	function App() {
		return (
			<ThemeContext.Provider value={themes.dark}>
				<ToolBar />
			</ThemeContext.Provider>
		);
	}
	
	function ToolBar(props) {
		return (
			<div>
				<ThemedButton />
			</div>
		);
	}
	
	function ThemedButton() {
		const theme = useContext(ThemeContext);
		return (
			<button style={{ background: theme.background, color: theme.foreground }}>
				I am styled by theme context! 
			</button>
		);
	}		


	  

## Regras dos Hooks

### Não use Hooks  dentro de Loops, regras condicionais ou funções aninhadas.

Isto permite que os Hooks sejam executados sempre na mesma ordem a cada renderização, do contrário, ocorrerá bugs no React. Ao invés disto, você pode utilizar Loops, Condicionais e Funções Aninhadas **dentro** do Hook. 

	// Errado
	if (name !== '') {
		useEffect(() => {})	
	}

	// Correto
	useEffect(() => {
		if (name !==) {}
	})

### Use Hooks apenas dentro de funções do React

Não use use hooks dentro de funções comuns do JavaScript. Ao invés disso, você pode:

*  Chamar Hooks em componentes React

* Chamar hooks dentro de hooks customizados

---

### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/hooks-state.html](https://pt-br.reactjs.org/docs/hooks-state.html)






