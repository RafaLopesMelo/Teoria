# React.lazy e Suspense

## React.lazy

A função React.lazy permite a você renderizar uma importação dinâmica como se fosse um componente comum. Veja:

	// Sem React.lazy:
		import Component from './Component'

	// Com React.lazy:
		const Component = React.lazy(() => import('./Component'))

Esta função faz com que "Component" seja carregado apenas quando for necessário pela primeira vez.

React.lazy recebe uma função que deve retornar um import(). Este por sua vez retorna uma Promise que é resolvida para um módulo com export default que contém um componente React.

## Suspense

O componente lazy pode ser renderizado dentro de um componente Suspense, que nos permite mostrar um elemento fallback (como um indicador de carregamento) enquanto o carregamento do elemento lazy é aguardado.

	import React, { Suspense } from 'react';

	const Component  = React.lazy(() => import('./Component'));
	
	function MyComponent() {
		return (
			<>
				<Suspense fallback = {<div>Loading...</div>} />
					<Component />
				</Suspense>
			</>	
	}

A prop fallback aceita qualquer elemento React que você deseja renderizar enquanto se espera o componente ser carregado. É possível colocar Suspense em qualquer lugar acima do componente dinâmico, podendo até ter vários componentes dinâmicos envolvidos em um único Suspense.

 ### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/code-splitting.html#reactlazy](https://pt-br.reactjs.org/docs/code-splitting.html#reactlazy)
