# Introdução a lógica de programação 

Cada linguagem de programação têm sua própria estrutura de dados embutida, e essa estrutura frequentemente difere uma da outra.  Vamos conhecer os tipos de dados disponíveis na linguagem JavaScript e que propriedades eles possuem.

Isso envolve o estudo de... Tipos primitivos, objetos, operadores, variáveis e estruturas condicionais.

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

### Null (nulo)

Pode ser utilizado para representar um valor vazio

### Undefined alor que nao foi definido

### Boolean
`false` e `true`

Muitas vezes, na programação, você precisará de um tipo de dado que só pode ter um de dois valores.
Exemplo:
- SIM / NÃO
- LIGADO / DESLIGADO
- VERDADEIRO / FALSO

Para isso, JavaScript tem um tipo de dado Boolean . Ele só pode receber os valores true ou false.
```js
console.log(10 > 9)
console.log(2 !== "dois")
```

# Operadores

## Operadores Matemáticos

```
+  mais
-  menos
*  multiplicação
/  divisão
%  modulo (ou resto)
** potencia
```

## Operadores de Atribuição

a = 2 -> atribui valor de 2 para a


## Operadores Lógicos

```
&&  significa E
||  significa OU
```

## Operadores de Comparação

```
==   igual
===  igual
>    maior que
<    menor que
>=   maior igual a
<=   menor igual a
!==  diferente
!=   diferente
 ```

### Triple equals vs Double equals
```
2 == 2 // true
2 === 2 // true
2 === "2" // false
2 == "2" // true
```

O double equals vai tentar nos ajudar na comparação, e ao notar que
estamos tentando comparar tipos diferentes (string e number) ele vai tentar converter a string para number. No caso acima ele consegue e por isso temos o resultado true.

Entao por baixo dos panos o que aconteceu foi:
``2 == Number("2") //true``

Com o triple equals o javascript nunca tenta converter os valores. Por isso, o resultado false.

Sendo assim, __recomenda-se usar o triple equals__ para evitar surpresas.

E a internet não perdoa as surpresas:

![meme1](https://www.freecodecamp.org/news/content/images/2019/07/best-js-meme-to-date-2.png)

### Vamos estudar mais sobre o assunto?

[História e memes do JavaScrip](https://www.youtube.com/playlist?list=PLh2Y_pKOa4UeJOI2P-N6J8nGyV3aCuO3O)

[const, let e var](https://medium.com/@natalya.peixoto/var-const-e-let-qual-a-diferen%C3%A7a-338ff0c7a972)

[Eloquent Javascript](https://braziljs.github.io/eloquente-javascript/chapters/valores-tipos-operadores/)

[Valores Verdadeiros e falsos - Truthy e falsy](https://developer.mozilla.org/pt-BR/docs/Glossario/Truthy#:~:text=Nesta%20p%C3%A1gina&text=Em%20JavaScript%2C%20um%20valor%20truthy,de%20tipo%20em%20contextos%20booleanos)





