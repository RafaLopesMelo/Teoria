# Renderização Condicional

### Em React, você pode criar componentes distintos que encapsulam comportamento que você precisa. Então, você pode renderizar apenas alguns dos elementos, dependendo do estado da sua aplicação.

Renderização condiconal em React funciona da mesma forma que condições funcionam em JavaScript. Basta utilizar os operadores condicionais do JavaScript, como o if, para criar elementos representando o estado atual, e deixe o React atualizar a UI para correspondê-los.
Veja o exemplo:

	// Renderiza componentes diferentes com base no login do usuário
	
	function Greetings(props) {
		const isLoggedIn = props.isLoggedIn;
		if (isLoggedIn) {
			return <UserGreeting />
		}
		return <GuestGreeting />
	}

## If inline com o operador &&

Este operador é utilizado entre chaves da seguinte forma: se a condição é ==true==, p elemento logo após o && será renderizado, se for false, o React apenas irá ignorar, observe:

	 function MailBox(props) {
		const unreadMessages = props.unreadMessages;
		return (
			<h1> Hello! </h1>
			{ unreadMessages.length > 0 &&
				<h2>
					You have {unreadMessages.length} unread messages. 
				</h2>
			}
		)
	}

## If-Else inline com Operador Condicional

Outra forma de renderizar elementos inline é utilizar o operador condicional em JavaScript ==condição ? true : false== . Veja: 

	render() {
		const isLoggedIn = this.state.isLoggedIn;
		return (
			<div>
				The user is { isLoggedIn ? 'currently' : 'not'} logged in. }
			</div>
		);
	}

## Evitando que um componente seja renderizado

Para tal, basta retornar o valo ==null== ao invés de um resultado renderizável:

	function WarningBanner() {
		if(!props.warn) {
			return null;
		}

---

### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/conditional-rendering.html](https://pt-br.reactjs.org/docs/conditional-rendering.html)

