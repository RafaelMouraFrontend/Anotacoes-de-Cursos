# AULA 26 - Manipular DOM com performace


Segue exemplo do uso de createDocumentFragment:

```js
var fragment = document.createDocumentFragment();
var childP = document.createElement('p');
var textChildP = document.createTextNode('Texto dentro da tag p');

childP.appendChilld(textChildP);
fragment.appendChild(childP);

document.body.appendChild(fragment);


```

## Posição dos scripts no html importa

aprenda um exemplo do uso de  DOMContentLoad, espera todo o conteúdo do dom ser carregado para então disparar o evento

```js
function afterDomDocumentLoad(){

var fragment = document.createDocumentFragment();
var childP = document.createElement('p');
var textChildP = document.createTextNode('Texto dentro da tag p');

childP.appendChilld(textChildP);
fragment.appendChild(childP);

document.body.appendChild(fragment);

}

document.addEventListener('DOMContentloaded', afterDomDocumentload, false);
```

# afterWindowLoad

Espera todo o evento do window ser carregado para então carregar os scripts, segue o exemplo:


```js
function afterDomDocumentLoad(){
    alert('Carregado depois da imagem carregar')
}

window.addEventListener('load', afterWindowLoad, false);
```


# Técnicas Ninja

Fazendo uma cópia de array



```js
var arr = [1, 2, 3, 4, 5, 6];

var arr2 = arr.slice();

console.log(arr, arr2, arr === arr2);

```


Fazendo uma cópia de array div

```js
var $div = document.querySelectorAll('div');   

var $divCopy = Array.prototype.slice.call($divs);

console.log($div, $divCopy, $div === $divCopy);

```


Mostrando o verdadeiro tipo

```js
var arr = [1,2,3];

console.log(Obj.prototype.toString.call(arr));
```