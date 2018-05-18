# AULA 26 - API DOM

## .parentNode ---> pega o nó pai

```js
var $main = document.querySelector('.main');
console.log($main.parentNode);
```
No caso traz o nó pai; exclusicamente nesse exemplo ele é ```body``` que nada mais é do que seu nó pai.


## .childNodes --> pega todos os nós filhos

```js
var $main = document.querySelector('.main');
console.log($main.childNodes);
```

nesse caso ele retorna uma nodelist, ele também conta quebras de linha como nós filhos

## .firstChild

```js
var $main = document.querySelector('.main');
console.log($main.fistChild);
```
tras o nó filho, nesse caso exclusicamente traz o #text, que significa uma quebra de linha

## .lasttChild

```js
var $main = document.querySelector('.main');
console.log($main.lastChild);
```
tras o nó filho, nesse caso exclusicamente traz o #text, que significa uma quebra de linha

## .nextSibling

```js
var $main = document.querySelector('.main');
console.log($main.nextSibling);
```
tras o proximo nó tag irmão, nesse caso exclusicamente traz o script se não houver quebra de linha, que significa uma quebra de linha.

## .previusSibling

```js
var $main = document.querySelector('.main');
console.log($main.previusSibling);
```
tras o anterior nó tag irmão, nesse caso exclusicamente traz o script se não houver quebra de linha, que significa uma quebra de linha


## .nodeType

Traz o tipo de nó

```js
var $main = document.querySelector('.main');
console.log($main.nodetype);
```

nesse caso retorna um numero 3, que é o tipo de nó do main.

## nodeValue

retorno de conteúde textual

```js
var $main = document.querySelector('.main-content');
console.log($main.fistChild.nodevalue);
```

## nodeName

retorna o nome do nó com 

##  .children 

Essa propriedade não é padronizada, trás nós de HTMLColection

# Elementos

## .firstElementChild

Primeiro elemento que é filho. Ignorando comentários e quebras de linhas

## .lastElementChilg

Último elemento que é filho. Ignorando comentários e quebras de linhas

## .nextElementSibling

trás o proximo elemento que é irmão

 ## .previusElementSibling

trás o anterior elmento que é irmão

## .childElementCount

Ele conta quantos elementos filhos, exemplo:

```js
var $main = document.querySelector('.main-content');
console.log($main.childElementCount);
```
# Metodos

## hasAttribute(name)

Pergunta se a tag tem um atributo, exemplo:

```js
var $main = document.querySelector('.main-content');
console.log($main.hasAttribute('class'));
```

## hasAttributes(name)

Ele verifica se tem mais de um atributo

```js
var $main = document.querySelector('.main-content');
console.log($main.hasAttributes());
```

## .appendChild(child)

ele concatena o conteudo escolhido ao final do filho

exemplo:

```js
var $main = document.querySelector('.main');
var $mainContent = document.querySelector('.main-content');
var $mainHeader = document.querySelector('.main-header');
$mainContent.appendChild($mainHeader);
```

## insertBefore(node, beforeWhom);

Inseri antes do nó /
Exemplo:

```js
var $main = document.querySelector('.main');
var $mainContent = document.querySelector('.main-content');
var $mainHeader = document.querySelector('.main-header');
var $mainText = $mainContent.firstChild;

$mainContent.insertBefore($mainHeader, $firstText);
```

## .cloneNode(true)

Faz um clone do nó / Exemplo:

```js
var $main = document.querySelector('.main');
var $mainContent = document.querySelector('.main-content');
var $mainHeader = document.querySelector('.main-header');
var $mainText = $mainContent.firstChild;

var $cloneMainHeader = $maiHeader.nodeClone(true);

$mainContent.appendChild($cloneMainHeader);
```

## .hasChildNodes()

Faz a pergunta - tem nós filhos?

Segue Exemplo:

```js
var $main = document.querySelector('.main');
var $mainContent = document.querySelector('.main-content');
var $mainHeader = document.querySelector('.main-header');
var $h1 = $mainHeader.firstChild;

console.log($h1.hasChildNodes());

$mainContent.appendChild($cloneMainHeader);
```

## .removeChild(child)

Remove o filho... segue exemplo:

```js
var $main = document.querySelector('.main');
var $mainContent = document.querySelector('.main-content');
var $mainHeader = document.querySelector('.main-header');
var $h1 = $mainHeader.firstChild;

$mainHeader.removeChild($h1);
```

## .replaceChild(new, old);

faz a troca dentro de um filho, exemplo:

```js
var $main = document.querySelector('.main');
var $mainContent = document.querySelector('.main-content');
var $mainHeader = document.querySelector('.main-header');
var $mainFooter = document.querySelector('.main-footer');

$main.repaceChild($maisHeader, $mainFooter);
```


## document.createTextNode('Opa!')

Adiciona um novo texto ao nó

```js
var $newText = document.createTextNode('Opa!');

$main.appendChild($newText);
```

# Atributos

## .id

pega o atribudo id

```js
var $main = document.querySelector('.main');

console.log($main.id);
```

esse no caso vai retornar a id de main


## pegar a classe

```js
var $main = document.querySelector('.main');

console.log($main.className);
```

## outra forma de pegar a classe: .getAttribute(attr);

Esse sempre vai pegar o atributo em forma de string

## setAttribute(attr, value);

muda o atribudo do nó / exemplo:

```js
var $main = document.querySelector('.main');

console.log($main.setAttribute('data-js', 'data-newJS'););
```