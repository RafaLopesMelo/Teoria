# O JSX no React

## Introduzindo

Observe esta declaração de variável:

	const element = <h1> Hello World </h1>

Esta sintaxe não se refere a um HTML e muito menos a uma string.

Ela é chamada de JSX, uma extensão de sintaxe para JavaScript, ela é utilizada com o React para descever como a UI vai ser renderizada e produz elementos do framework.

No JSX é possível adicionar **qualquer** expressão JavaScript dentro de chaves, veja:

	const name = 'Rafael Lopes de Melo'
	const element = <h1> Hello, { name }! <h1>
	ReactDOM.render(
		element,
		document.getElementById('root'));

Depois da compilação, as expressões JSX se tornam chamadas normais de função que retornam objetos em JavaScript, ou seja, é possível utilizar JSX dentro de  **if** ou **for**.

	function getGreeting(user) {
	  if (user) {
	    return <h1> Hello,{user}!</h1>;} 
	  else {
		return <h1>Hello, Stranger.</h1>;}}

<br><div align='center'>**Ao setar atributos num elemento React, não utilize de chaves juntamente com aspas, use apenas chaves para expressões JavaScript e aspas para valores literais!**</div>
	
<br>

___
___

<br>

## JSX é seguro?

É seguro incorporar entradas de usuário em JSX. Todos os inputs são convertidos para string antes de serem renderizados, evitando ataques conhecidos como **XSS (cross-site-scripting)** ou **"Ataques de Injeção"**.

<br>

___
___

<br>

## JSX representa objetos

O Babel compila JSX para chamadas React.createElement().

Estes dois exemplos são idênticos:

	const element = (
		<h1 className='greeting>
		Hello, World!
		<h1>);
<br>

	const element = React.createElement(
		'h1',
		{ className = 'greeting' },
		'Hello, World!');

#### Construindo um objeto, em essência, como este:

	const element = {
	type: 'h1',
	props: {
		className = 'greeting',
		children = 'Hello, World!'
	}};

---

### Referências:

> Site oficial do React: [https://pt-br.reactjs.org/docs/introducing-jsx.html](https://pt-br.reactjs.org/docs/introducing-jsx.html)


