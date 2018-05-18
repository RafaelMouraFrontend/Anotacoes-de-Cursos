window.alert('Sinal de alerta')

window.prompt('Qual o seu nome')

window.confirm('Faz uma confirmação retornando true!')


window.document --> representa o documento 

Dá acesso a arvore do DOM (Document objetct model)


document.getElementById('myid')

document.getElementsByClassName('myclass');

document.getElementsByTagName('a');

document.getElementsByName('username');

document.querySelectorAll('input');

document.querySelector('input'); --> vai selecionar apenas o primeiro


var $imputUserName = document.querySelector('#username')


$imputUserName.value = 'Rafael Moura' --> estou setando um valor


console.log($imputUserName.value) -- get no valor apenas visualizando

$imputUserName.addEventListener('click', function(event){
	
	event.preventDefault();

	console.log("O input foi clicado");

},false);

