# AJAX

Asyn javaScript and XML

1- instanciando uma requisição ajax

```js
var ajax = new XMLHttpRequest(); 

```
2- abrir uma conexão
```js
ajax.open(<protocolo>, <url>);
```
3- enviar os dados para o servidor se tiverem dados
```js
ajax.send(<data>);
```
## Na prática!

```js
    var ajax = new XMLHttpRequest();
    ajax.open('GET', '/');

    ajax.send();
```

```js
    var ajax = new XMLHttpRequest();
    ajax.open('GET', '/');

    ajax.send();

    ajax.addEventListener('readystatechange', function(){
        console.log('Terminou requisição', ajax.readyState);
    }, false);
```

Manipulando requisições

```js
    var ajax = new XMLHttpRequest();
    ajax.open('GET', '/data/data.js');

    ajax.send();

    console.log('Carregando...');

    ajax.addEventListener('readystatechange', function(){
        if(isRequestOk()){
            console.log('Ok!!!', ajax.responseText);
        }
    }, false);

    function isRequestOk(){
        return ajax.readyState === 4  && ajax.status === 200;
    }
```
Manipurando JSON
```js
    var ajax = new XMLHttpRequest();
    ajax.open('GET', '/');

    ajax.send();

    console.log('Carregando...');

    ajax.addEventListener('readystatechange', function(){
        if(isRequestOk()){
            var data = JSON.parse(ajax.responseText)
            console.log('Ok!!!', data.message);
        }
    }, false);

    function isRequestOk(){
        return ajax.readyState === 4  && ajax.status === 200;
    }
```

Manipurando XML
```js
    var ajax = new XMLHttpRequest();
    ajax.open('GET', '/data.xml');

    ajax.send();

    console.log('Carregando...');

    ajax.addEventListener('readystatechange', function(){
        if(isRequestOk()){
            
            console.log('Ok!!!', ajax.responseXML);
        }
    }, false);

    function isRequestOk(){
        return ajax.readyState === 4  && ajax.status === 200;
    }
```

## Tratamentos de erros no ajax

```js
    var ajax = new XMLHttpRequest();
    ajax.open('GET', '/data.xml');

    ajax.send();

    console.log('Carregando...');
    var response = '';
    ajax.addEventListener('readystatechange', function(){
        if(isRequestOk()){
            try{
                response = JSON.parse(ajax.responseText);
            }
            catch(e){
                response = ajax.responseText;
            }
        }
    }, false);

    function isRequestOk(){
        return ajax.readyState === 4  && ajax.status === 200;
    }
```