regex parte 2

... procura 3 caracteres

\s ----> espaço em branco

\n ----> quebra de linha

\t ---->tabulacao

\d ----> um numero


Negação

[^abc]  não faser match ou a ou b ou c - exclui esse e pega todos os outros	

\W é a negação de todos os alfanumericos

\D negaão de numeros

\S menos os espaços em branco

r{1,2} minimo 1, maximo 2 

r{2,} internvalo aberto

r{2} exatos 2

\s\d? espaço em branco com um numero opicional

/s+ uma ou infinitas vezes os S

\W\W+ duas letras ou mais



^ inicio de string

$ fim de string

flag m - multiline inicio de string geramente

? captura não gulosa

(?:) negar um grupo




metodos string, onde podemos usar regex


'string'.match(/ing/)

.replace(//, string)

.split(/\D/); --- split com regex pra remover e jogar em um array


.search(/\./); -- traz o indice de onde foi encontrado o ponto, e é indiferente a flag /g

var regex = new RegExp('123nando');

regex.text(/z/)

-------------------------------
regex.exec(name); vai executar todaa a procura da regex até retornar null




