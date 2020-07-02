# Manipulando Eventos

Manipular eventos no React é muito semelhante a manipular eventos no DOM. Há apenas algumas diferenças de sintaxe:


 - Eventos em React são nomeados usando camelCase ao invés de letras minúsculas.
- Com o JSX você passa uma função como manipulador de eventos ao invés de um texto.

<br>

	// Em HTML
	
	<button onclick='activateLasers()'>
		Ativar lasers
	</button>
	
<br>

	// Em React 
	
	<button onClick= { activateLasers }>
		Ativar lasers
	</button>

<br>

- Não se pode retornar false para evitar o comportamento padrão no React. No lugar você deve chamar ==preventDefault== explicitamente. Veja como seria para evitar que um link abra uma nova página: 

<br>


	// Em HTML
	
	<a href='#' onclick='console.log('O link foi clicado.'); return false'>
	Clique aqui
	</a>

<br>

	// Em React
	
	function ActionClick() {
		function handleClick(e) {
			e.preventDefault();
			console.log('O link foi clicado.');
		}
		
		return(
		<a href='#' onClick = { handleCLick }>
			Clique aqui
			</>
		)
	}

Neste caso, o "e" é um ==SyntheticEvent==, o React os define de acordo com as especificações W3C.

---

 ### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/handling-events.html](https://pt-br.reactjs.org/docs/handling-events.html)
