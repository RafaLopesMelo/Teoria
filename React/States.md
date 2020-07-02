# States

O state do componente é similar às props, mas é privado e totalmente controlado pelo próprio componente.

## Usando o State Corretamente

Existem três coisas que você deve saber sobre setState():

### Não modifique o State diretamente

Isso não renderizará novamente o componente:

	// Errado
	this.state.comment = 'Hello';

Ao invés disso, use a função setState():

	// Certo
	this.setState({ comment: 'Hello' });

Em um componente de classe, o único lugar em que se pode atribuir **this.state** diretamente é no construtor.

### Atualizações de State podem ser assíncronas:

O React pode agrupar várias chamadas setState() em uma única atualização para melh0or desempenho.
Como o this.props e this.state podem ser atualizados de forma _assíncrona_, você não pode confiar em seus valores para calcular o o próximo state.
Por exemplo, a seguinte instrução pode não retornar o valor desejado:

	// Errado
	this.setState({
		counter: this.state.counter + this.props.increment
	})

Ao invés disso, utilize uma segunda forma de usar o setState, passando uma função no lugar de um objeto, recebendo os state e as props atuais do componente como argumento:

	// Correto
	this.setState((state, props) => {
		return {
			counter: state.counter + props.increment;
		}
	})
	// Pode-se utilizar uma função regular no lugar da arrow 
	function


 >Assíncrona = No decorrer da execução do código, uma função assíncrona não é necessariamente finalizada antes do resto do algoritmo, ao invés disso ela retorna uma Promise, o fluxo corre normalmente, e quando a função for finalizada, esta Promise é resolvida com o retorno desta função assíncrona. Estas situações acontecem quando há uma instrução que pode demorar alguns ms para ser completada, como uma consulta ao banco de dados.

### Atualizações de State são mescladas

Os states podem possuir diversas variáveis independentes: 

	this.state = {
		posts: [],
		comments: []
	};

Sendo assim, um setState({ comments }), deixa this.state.posts intacto, mas substitui completamente this.state.comments.

## Os dados fluem para baixo

Nem compontes pai ou filho podem saber se um determinado componente é stateful o stateless, e não devem se importar se ele é definido por uma função ou classe.
É por isso que o state é chamado de local ou encapsulado, ele não é acessível a nenhum outro componente que não seja o que o possui e define.

Um componente pode escolher passar seu state como props para seus componentes filhos:

	<h2> It is { this.state.date } </h2>
	ou
	<Data date = { this.state.date }/>

O componente Data receberia o ==date== e não saberia se ele veio do state ou das props do componente pai, ou se foi digitado manualmente. 

>Isso é comumente chamado de fluxo de dados "top-down" ou "unidirecional". Qualquer state é sempre propriedade de um componente específico e só pode afetar os componentes "abaixo" deles na árvore.

---

### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/state-and-lifecycle.html](https://pt-br.reactjs.org/docs/state-and-lifecycle.html)
