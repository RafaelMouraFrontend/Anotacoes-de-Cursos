


// ############ .lenght na função #################

//conta quantos paramenotros podem ser passandos na função

console.log(myFunction.length);



// ############ .toString #################

//converte toda a função em uma string


// ############ .call #################

//chama a funçao e também posso chamar a função passando a referncia this, veja:

function myFunction(a, b, c) {
  console.log(this.lastName, a, b, c);
}

var person = {
  lastName: 'Moura'
};

myFunction.call(person);

//o .call também pode receber os parametros depois do this, veja:

myFunction.call(person, a, b, c);

// ############ .apply #################

//quebra o array em argumentos para a função

arr = [1, 2, 3, 4, 5, 6];

myFunction.apply(person, arr);


// ############ .prototype #################

//ele estende o contrutor da função, veja:

function Person(name, lastName) {

  this.name = name;
  this.lastName = lastName;


}


Person.prototype.fullName = function () {
  return this.name + '' + this.lastName;
};

var fernando = new Person('Rafael', 'Moura');
console.log(fernando.fullName());



// ################ Array LIKE ###################

function myFunction() {
  var result = Array.prototype.reduce.call(arguments, function (acumulate, atual, index) {
      return acumulate + atual;
  });
  console.log(result);


}

myFunction(1,2,3,4,5,6,7,8,9);
