# Listas e Chaves 

Primeiramente, é importante rever como transformamos listas em JavaScript.

	const numbers = [ 1, 2, 3, 4, 5 ];
	const doubled = numbers.map((number) => number * 2);

Dado este código acima, usamos a função ==map()== para receber um array e dobrar o valor de cada elemento. Por fim, atribuímos este nova array dobrado à constante doubled.

No React, transformar arrays em listas de elementos é praticamente idêntico a isto.

## Renderizando Múltiplos Componentes

É possível criar coleções de elementos e adicioná-los no JSX usando chaves.

	const numbers = [ 1, 2, 3, 4, 5 ];
	const listItems = numbers.map((number) => {
		<li>{number}</li>});

## Chaves

As chaves ajudam o React a identificar quais itens sofreram alterações, se foram adicionados ou removidos. As chaves devem ser atribuídas aos elementos dentro de um array para dar identidade estável aos elementos:

A melhor forma de escolher uma chave é usar uma **string** que identifica unicamente um item na lista entre os demais, na maioria das vezes é usado um ID:

	const todoItems = todos.map((todo) => {
		<li key = { todo.id }>
			{ todo.text }
		</li>
	})

É possível utilizar também o índice do elemento no array como chave caso não haja um ID, mas é absolutamente não recomendado.

	const todoItems = todos.map((todo, index) => {
		<li key = { index }>
			{ todo.text }
		</li>
	})

 ### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/lists-and-keys.html](https://pt-br.reactjs.org/docs/lists-and-keys.html)
 
