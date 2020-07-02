# Renderizando Elementos

> Elementos são os menores blocos de construção de aplicativos React.

<br>
Os elementos React são objetos simples que utilizam menos recursos que o DOM do navegador.

<br>

> Não confunda elementos com o conceito de 'componentes', na verdade os elementos **formam** os componentes

<br>

Em algum lugar do seu código HTML existe uma div como a seguinte:

	<div id='root'> </div>

Ela é chamada de raíz pois tudo dentro dela será renderizado pelo React DOM. Aplicações exclusivamente React geralmente possuem uma única raíz no DOM, porém podem conter quantos nós raíz precisar.

Para renderizar um elemento React em um nó raíz, utilize um código como este:

	const element = <h1> Hello, World! </h1>
	reactDOM.render(element, document.getElementById('root'))

Elementos React são **imutáveis**, ou seja, não se pode alterar seus elementos filhos ou atributos.
Mantendo esta ideia, a única forma possível de atualizar a interface é re-renderizá-la a cada determinado espaço de tempo, como no seguinte exemplo:

	function tick() {
		const element = (
			<div>
				<h1> Hello, World! </h1>
				<h2> It is { New Date().toLocaleTimeString } </h2>
				</div>
		);
		ReactDOM.render(element, document.getElementById('root'))
	}
	setInterval(tick, 1000);
<br>


##  O React DOM compara os elementos novos com os filhos e aplica somente as atualizações necessárias na página, eliminando possíveis bugs!

---

### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/rendering-elements.html](https://pt-br.reactjs.org/docs/rendering-elements.html)


