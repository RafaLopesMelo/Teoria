# Ciclo de Vida

Ao nosso redor, tudo passa por um ciclo de vida: nascimento, crescimento e, em algum momento, a morte. Isto é o método do ciclo de vida do React, os componentes podem ser montados (nascer), crescer (receber atualizações) e ser desmontados (morrer).

Em aplicações com muitos componentes, é essencial limpar os recursos utilizados por eles quando são destruídos. Para isso e diversas outras coisas, podemos chamar métodos pré-definidos para realizar certas instruções de acordo com a fase de vida do componente.

---

## As quatro fases de um elemento React

### Inicialização:

Nesta fase, o componente React se prepara para sua inicialização , configurando os estados iniciais e props padrões, se houverem. Veja:

	// Indica como o componente será renderizado
	
	class ContraMusicPlayer extends React.Componente 
		constructor(props) {
			super(props);
			this.state = {
				volume: 70,
				status: 'pause'
			}
		};
		
		ContraMusicPlayer.defaultProps = {
			theme: 'dark'
		};

> O ==defaultProps== é uma propriedade componente para definir todo o valor padrão das props, e podem ser substituídos por novos valores também.
---

### Montagem

Depois da inicialização, o nosso componente React está pronto para ser montado no DOM do navegador. Esta fase fornece métodos básicos que podem ser chamados antes e depois da montagem. Os métodos chamados nessa fase são:

#### ComponentWillMount: 

É executado quando o componente estiver prestes a ser montado no DOM da página. Assim, após este método ser executado, componente criará um nó no navegador. **Este método é executado uma única vez em um ciclo de vida de um componente e antes de sua renderização.**

#### render 

Monta o componente no navegador, é um método puro e, portanto, dá a mesma saída para as mesmas entradas.

#### componentDidMount

É executado depois que o componente foi montado no DOM. **Este método é executado uma única vez em um ciclo de vida e logo após sua renderização, neste momento podemos inicializar bibliotecas JS. **
**Este também é o melhor momento para fazer chamadas à ==API==.**

---

### Atualização

Esta fase começa quando o componente React já nasceu no navegador e cresce recebendo atualizações através do envio de novas props ou mudanças de estado. 

> Os métodos disponíveis quando o estado atual é atualizado são:

#### shouldComponentUpdate

Diz ao React quando ele deve re-renderizar o componente ou ignorar quando recebe novas props ou estado. Quando este método retorna true, o componente é re-renderizado, caso contrário não (por padrão, este método retorna true). Observe:

	shouldComponentUpdate(nextProps, nextState) {
	
		let shouldUpdate = nextProps.status !== this.props.status;	
		return shouldUpdate
	}

#### componentWillUpdate, render, componentDidUpdate 
	
Estes são equivalentes respectivamente ao ==componentWillMount==, ==render== e ==componentDidMount== da fase da montagem. O último, neste caso, é utilizado para reativar as bibliotecas de terceiros com a intenção de mantê-las atualizadas.

> Os métodos disponíveis quando novas props são enviadas ao componente:

#### componentWillReceiveProps

É executado quando as props mudaram e não foram processadas ainda. Este método é usado para sincronizar o estado e as props do componente, sendo que as vezes um depende do outro. **Não existe um método similar em se tratando de estados.**

> O resto dos métodos são exatamente iguais aos relacionados a estados.

----

### Desmontagem

Nesta fase, o componente é desmontado no DOM e possui apenas um método:

#### componentWillUnmount

É o último do ciclo de vida e é executado imediatamente antes do componente ser removido do DOM. **Este método é utilizado para apagar as informações residuais do componente, como token de autenticação e informações no LocalStorage:** 

	componentWillUnmount() {
		this.chart.destroy();
		this.resetLocalStorage();
		this.clearSession();
	}
	
---

### Referências:

> Artigo de Edmo Lima no Medium: [https://medium.com/creditas-tech/m%C3%A9todos-do-ciclo-de-vida-de-componentes-reactjs-um-mergulho-profundo-332ed7b3b782](https://medium.com/creditas-tech/m%C3%A9todos-do-ciclo-de-vida-de-componentes-reactjs-um-mergulho-profundo-332ed7b3b782)

>  
		
