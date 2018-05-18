
# Metodo de retorno Async

setTimeout(functiom(){

	console.log('mostrar setTimeout')

}, 1000);


setInterval(function(){

	console.log('Executar');

},1000); // Repete a cada 1000 milisegundos



## Async função recursiva

var counter = 0;

function timer(){
	console.log('timer', counter++);
	setTimeout (timer, 1000);

}
timer();


## Async função recursiva - parando

var counter = 0;

function timer(){
	console.log('timer', counter++);
	if(counter > 10)
		return;
	setTimeout (timer, 1000);

}
timer();

## Diferença entre setTimeout e setInterval

O setTimeout recursivo é mais performatico que o setInterval

function timer(){
	console.log('timer', counter++);
	if(counter > 10)
		return;
	setTimeout (timer, 1000);

}
timer(); 


## Parando o temporizador

var counter = 0;

var $button = doc.querSelector('[data-js="button"]');

var temporizador;

function timer(){
	console.log('timer', counter++);
	if(counter > 20)
		return;
	temporizador = setTimeout(timer, 1000);
	
}

timer();

$button.addEventListener('click', function(){

	clearTimeout(temporizador).

},false);




