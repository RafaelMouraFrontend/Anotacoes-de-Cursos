# AULA 25 - Scripts Inline 

Neste caso ele vai executar uma função boom() depois do texto para comando inline de javascript no link 'javascript:'

```html
<a href="javacript:boom()">
```
## O que significa o void(0)?

```html
<a href="javacript:void(0)">
```
Ele não faz nada, faz com que não retorne nenhum link, não é recomendado usar mais o void, ao inves disso podemos usar um prevent default

## eventos inline

Saber da existencia, pois não é uma boa prática

```html
<a href="javacript:" onclick="boom()">
```
vai fazer a execução da função  boom(); lembrando não é uma boa prática, ao invés disso devemos fazer

```javaScript
<a href="#:" data-js="link">


var $link = doc.querySelector('[data-js="link"]')
$link.addEventListener('click', boom, false);

function boom(event){
    event.preventDefault();
    alert('Booom!!!')
}
```
# Eventos

o que significa um false depois da function dentro de um: 

```js
addEventListener('click', funcao, false);
```
ajuda a propagar o evento de dentro pra fora, caso do  ```  true ```  ele faz o inverso.

## addEventListener

são acumumulativos na adição de eventos

## Alguns eventos além do click

keyup, keydown, input, change

## Observações do que teve na aula

aqui vou discertar sobre algumas coisas não abordadas na anotação de texto qualquer coisa rever o vídeo:

Durante a aula 26 ele fez umas abstrações de addEventListener e removeEventListener


