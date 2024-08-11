# senac-logicaEalgoritmos



# Variáveis

JavaScript é uma linguagem de __tipagem dinâmica__.
Isso significa que você não necessita declarar o tipo de uma variável antes de sua atribuição.
O tipo será automaticamente determinado quando o programa for processado.
Isso também significa que você pode reatribuir uma mesma variável com um tipo diferente.

Uma variável faz referencia a um espaço na memória do computador.
São utilizadas para guardar informações que serão usadas nos programas.

Criamos a variável nome e atribuimos o valor string de 'natalya' a ela.
em seguida acessamos a variavel e a mostramos na tela.

```
var nome = 'natalya'
console.log(nome)
```

Na __declaração__ usamos as palavras reservadas (var, let ou const):
```
let batata = 'pure'
```

__Reatribuíção:__
```
batata = 'batata-frita'
```

## var

É  mais antiga forma de definir variáveis no javascript, ela pode ser reatribuída e redeclarada. 
Diferentemente da const e da let ela não tem escopo de bloco.

## let

A let junto com a const vieram no es6 (atualização de 2015).
Ela também pode ter o seu valor reatribuido mas não pode ser redeclarado.

## const

A const (constante) não pode ter seu valor reatribuído nem redeclarado.
Diferentemente da let e da var. E assim com a let ela também tem escopo de bloco.

MDN: [var](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/var), [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const), [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)


# Escopo

A grande maioria das linguagens possui o conceito de escopos, e JavaScript não é diferente. Escopo é a acessibilidade de objetos, variáveis e funções em diferentes partes do código.

Em outras palavras, o que determina quais são os dados que podem ser acessados em uma determinada parte do código é o escopo.

## Escopo Gobal

Todos tem acesso a valores que são definidos no escopo global.

## Escopo Local

No escopo local, variaveis que são criadas dentro dele não podem ser acessadas no escopo global(com excessao da var).

Escopos locais são criados através de __funções__ e __blocos__ de código.
Bloco de código é tudo que está dentro de chaves `{}`

```js
// escopo global

if (2 > 1) {
  //escopo local
  const restrito = 'olá'
}
```
console.log(restrito) // ReferenceError: restrito is not defined

agora vamos definir a variável `popular` fora do bloco de if (no escopo global).
Veja que conseguimos acessa-lá de dentro do escopo local.

```js
const popular = 'oi'
if (2 > 1) {
  //escopo local
  console.log(popular)
}
```
# Estrutura de dados: Tipos primitivos




### String X Template string

Exemplo de string:

```js
const frase = 'Olá, mundo!'

console.log(frase)
```

Exemplo de template string:

```js
const nome = 'Alunos'

const templateString = `Olá, ${nome}`

console.log(templateString)
```
### Concatenação de stringss

Concatenar é uma palavra chique da programação que significa "colocar junto". Para colocar strings juntas em JavaScript, usamos o operador (+), o mesmo usamos para adicionar números, mas neste contexto é algo diferente. Vamos tentar este exemplo no console.

```js
var one = "Hello, ";
var two = "how are you?";
var joined = one + two;
joined;
```
O resultado disso é uma variável chamada joined, que contém o valor "Hello, how are you?".

MDN: [Template strings](https://developer.cdn.mozilla.net/pt-BR/docs/Web/JavaScript/Reference/template_strings)

### Números, operadores e calculos matemáticos

* Number -> valores numéricos (podem ser inteiros ou decimais 5 ou 5.0)
  
```js
var num1 = 10;
var num2 = 50;
9 * num1;
num2 / num1;
```

* BigInt (grandes números)

O tipo Number é limitado por isso o tipo de dado BigInt foi criado. Com ele é possível representar inteiros de precisão não exata. Para fazer uso dele você pode adicionar um __n__ ao final do número inteiro ou chamar a função BigInt() como mostrado abaixo:
````
90071992547409910n * 100n
9007199254740991000n
````
com o Number:
````
90071992547409910 * 100
9007199254740990000
````

MDN: [javascript math](https://developer.mozilla.org/pt-BR/docs/Learn/JavaScript/First_steps/Math)
---

### Null (nulo) -> pode ser utilizado para representar um valor vazio

### Undefined -> valor que nao foi definido

### Boolean
`false` e `true`

Muitas vezes, na programação, você precisará de um tipo de dado que só pode ter um de dois valores.
Exemplo:
SIM / NÃO
LIGADO / DESLIGADO
VERDADEIRO / FALSO

Para isso, JavaScript tem um tipo de dado Boolean . Ele só pode receber os valores true ou false.
```js
console.log(10 > 9)
console.log(2 !== "dois")
