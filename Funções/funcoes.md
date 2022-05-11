<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> JavaScript Script | Funções
</div>

---

<br>

> Funções são pedaços de códigos que fazem alguma tarefa e pode ser chamada a qualquer momento durante a execução do programa.

<br>

# FUNÇÕES

- [O que são funções?](#o-que-são-funções)
- [Definindo uma função](#definindo-uma-função)
- [Parâmetros e escopo](#parâmetros-e-escopo)
- [Escopo aninhado](#escopo-aninhado)
- [Notação por declaração](#notação-por-declaração)
- [Arrow functions](#arrow-functions)
- [Pilha de chamadas](#pilha-de-chamadas)
- [Argumentos opcionais](#argumentos-opcionais)

Funções são blocos fundamentais; Funções é um conjunto de instrução que executa um processamento e executa um conjunto de instruções. Podemos, por exemplo, criarmos uma função que calcula a média de uma turma e nos retorna um resultado.

<br>
<br>

# O QUE SÃO FUNÇÕES?

Uma função é um pedaço de programa envolvido por um valor que pode ser aplicado para executar alguma funcionalidade. O `alert`, por exemplo, é uma função nativa do JavaScript que tem como objetivo mostrar uma pequena caixa de diálogo com uma mensagem.

```javascript
alert("Hello, world!");
```

Quando você utiliza uma função, você está _chamando_, _invocando_ ou _aplicando_ uma função.

Para chamar uma função basta utilizar os parênteses depois da expressão que produz um valor de função. No exemplo que foi mostrado a função `alert` utilizou os parênteses para ser chamada e dentro dele é perceptível que temos uma `string` escrita `"hello, world!"`, que aparece na chamada do diálogo. Os valores dentro da função (dentro dos parênteses) são chamados de _arguments_ (argumentos). A função `alert` utiliza apenas um argumento e outras funções utilizam diferentes valores.

Existem seis tipos básicos de valores no JavaScript: _números, Strings, Booleanos, objetos, funções e valores indefinidos_. Quando você desejar criar um valor você só precisa invocar o nome do seu valor; É claro que não são criados do nada, todo valor precisa estar armazenado em algum lugar e se você quiser utilizar uma quantidade enorme dele pode acabar ficando sem bits. Porém é importante ressaltar que a medida em que você não utiliza um valor ele será dissipado, fazendo com que seus bits sejam reciclados e disponibilziando-os para serem usados nas contruções de outros valores.

<br>
<br>

# DEFININDO UMA FUNÇÃO

Uma função possui a definição similar a de uma variável — a única diferença é o valor que vai ser recebido pela variável é uma função.

```javascript
var calcular = function (numero) {
  return numero + numero;
};

console.log(calculo(12));
```

No exemplo anterior, declaramos a variável `calcular` e atribuímos o valor dessa variável o bloco da função — essa função possui o `return`, que retorna o valor do processamento. No caso do exemplo, o processamento foi o `numero` + `numero` como está escrito dentro do bloco da função. Abaixo, chamamos a função com o `console.log(calculo(12))`. O valor `12` é o valor do número que foi declarado na chamada da função e o cálculo será efetuado com esse valor.

É importante ressaltar que nem todas as funções retornam um valor, como demonstrado no exemplo acima.

```javascript
var fazerBarulho = function () {
  console.log("AAAAAAAAAAAAAA");
};
fazerBarulho();
```

No exemplo anterior, temos o exemplo de uma função que não retorna um valor. Essa função `fazerBarulho` é chamada e o único processamento que ela faz é o `console.log("AAAAAAAAAAAAAA")`.

Todo os processamento em funções são determinado entre chaves `{}`.

<br>
<br>

# PARÂMETROS E ESCOPO

Toda variável tem um escopo, podendo ser local ou global. Parâmetros ou declarações criadas em uma função estão no escopo local. Sempre que uma função for chamada, uma nova instância do escopo local é criado; parâmetros declarados com `let` e `const` são declarações locais. Variáveis `let` e `const` declaradas dentro de escopos locais de funções não são visíveis fora do seu escopo.

```JavaScript
let x = 21;
if(1 + 1 === 2){
    let y = 12;
    var z = 10;
    console.log(x + y + z);
    // -> 33
}
// a variável y não é visível aqui
console.log(x + z);
// -> 31
```

No exemplo anterior, vemos que o `console.log` fora da estrutura condicional (`if/else`) retorna o valor 31. Caso declararmos `console.log(x + z + y)`, haveria um erro pois o a variável `y`, que é um let, existe apenas dentro do escopo local. É importante ressaltar que esse comportamento em funções **não se repete**. Caso tentarmos utilizar qualquer variável declarada localmente na função não existiria no escopo global.

```JavaScript
let x = 21;

var soma = function soma(){
    if(1 + 1 === 2){
        let y = 12;
        var z = 10;
        console.log(x + y + z);
        // -> 33
    }
}

// A variável y e z não são visíveis aqui, a não ser que tenham sido declaradas globalmente

console.log(x);
// -> 21
```

Caso tentarmos imprimir a variável `y` ou `z`, da seguinte forma:

```JavaScript
let x = 21;

var soma = function soma(){
    if(1 + 1 === 2){
        let y = 12;
        var z = 10;
        console.log(x + y + z);
        // -> 33
    }
}

// A variável y e z não são visíveis aqui, a não ser que tenham sido declaradas globalmente

console.log(x + y);
// -> ReferenceError: y is not defined
```

Esse erro acontece pois a variável `y` não foi definida no escopo global, somente no escopo local da função.

<br>
<br>

# ESCOPO ANINHADO

O JavaScript não distingue apenas escopos globais e locais de variáveis. Blocos e funções possuem o mesmo comportamento. Funções podem ser criadas dentro de funções, produzindo múltiplos graus de localidade.

###### Exemplo retirado do livro Eloquente JavaScript. Para ver essas informações [clique aqui](https://eloquentjavascript.net/03_functions.html).

```javascript
const receita = function (fator) {
  const ingrediente = function (quantidade, unidade, nome) {
    let ingredienteQuantidade = quantidade * fator;
    if (ingredienteQuantidade > 1) {
      unidade += "s";
    }
    console.log(`${ingredienteQuantidade} ${unidade} ${nome}`);
  };
  ingrediente(1, "xícara", "leite");
  ingrediente(0.25, "colher", "sal");
  ingrediente(0.25, "copo", "suco de limão");
  ingrediente(1, "colher de chá", "pimenta");
};
```

O código anterior a função `ingrediente` pode ver o parâmetro `fator` da função `receita`. Mas é um escopo local, que como as variáveis `ingredienteQuantidade` ou `unidade` não são visíveis na outra função.

O conjunto de ligações visíveis dentro de um bloco é determinado pelo lugar desse bloco no texto do programa. Cada escopo local também pode ver todos os escopos locais que o contêm e todos os escopos podem ver o escopo global. Essa abordagem para a visibilidade de vinculação é chamada de _escopo léxico_.

<br>
<br>

# NOTAÇÃO POR DECLARAÇÃO

Existe uma maneira mais simples de definir uma função no JavaScript. Em vez declarar: `var quadrado = function...`. A palavra-chave `function` também pode ser utilizada no início da declaração...

```JavaScript
function quadrado(x){
    return x * x;
}
```

Definimos a variável `quadrado` e fazemos com que ela referêncie a função em questão, entretanto, é importante ressaltar que existe uma pequena diferença entre essas declarações. Quando declaramos uma função dessa forma,

<br>

# ARROW FUNCTIONS

Uma outra forma de declararmos funções é a _arrow function_. A _arrow function_ é declarada de forma diferente. Em vez de usarmos a palavra `function`, utilizamos uma flecha `=>` feito com o _sinal de igual_ `=` e _maior que_ `>`.

```javascript
const poder = (base, expoente) => {
  let resultado = 1;
  for (let contador = 0; contador < expoente; countador++) {
    resultado *= base;
  }
  return resultado;
};
```

Nas arrow functions, a flecha vem depois dos parâmetros seguindo do bloco da função: `() => {}`

Quando existe somente um parâmetro, o parêntese pode ser omitido. Caso o conteúdo dentro do corpo da função seja uma expressão sozinha em vez de envolver o bloco em chaves, você pode escrever somente a expressão sem necessidade do `return`.

```javascript
const retangulo1 = (x) => {
  return x * x;
};
const retangulo2 = (x) => x * x;
```

Quando estamos definindo uma _arrow function_ e não queremos nenhum parâmetro, basta declarar a função com o parêntese vazio, como no exemplo abaixo:

```javascript
const elefante = () => {
  console.log("Elefante tem tombra!");
};
```

<br>
<br>

# PILHA DE CHAMADAS

É importante entedermos como funciona o fluxo de controle flui por meio das execuções das funções. Veremos abaixo um simples programa realizando algumas chamadas de funções:

```javascript
function diaAtual(dia){
  console.log(`Hoje é:` ${dia});
}
diaAtual("Segunda-feira");
console.log("Tenha um bom dia!");
```

A função anterior funciona dessa forma:

- A chamada da função `diaAtual` faz com que o controle pule para o início dessa função (linha 1);
- Após a chamada da função `diaAtual`, é invocado o `console.log`, que assume o controle e faz o seu trabalho;
- O controle chega ao fim da função `diaAtual` e retorna para o local onde a função foi invocada originalmente (linha 3);
- Por fim, finalmente o controle executa o `console.log("Tenha um bom dia!)`

<br>

###### Abaixo teremos um exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

> Devido ao fato de que a função deve retornar ao local onde foi chamada após finalizar a sua execução, o computador precisa se lembrar do contexto no qual a função foi invocada originalmente. Em um dos casos, console.log retorna o controle para a função greet. No outro caso, ela retorna para o final do programa.
>
> O local onde o computador armazena esse contexto é chamado de call stack (pilha de chamadas). Toda vez que uma função é invocada, o contexto atual é colocado no topo dessa "pilha" de contextos. Quando a função finaliza sua execução, o contexto no topo da pilha é removido e utilizado para continuar o fluxo de execução.
>
> O armazenamento dessa pilha de contextos necessita de espaço na memória do computador. Quando a pilha começar a ficar muito grande, o computador reclamará com uma mensagem do tipo out of stack space (sem espaço na pilha) ou too much recursion (muitas recursões). O código a seguir demonstra esse problema fazendo uma pergunta muito difícil para o computador, que resultará em um ciclo infinito de chamadas entre duas funções. Se o computador tivesse uma pilha de tamanho infinito, isso poderia ser possível, no entanto, eventualmente chegaremos ao limite de espaço e explodiremos a "pilha".

```javascript
function chicken() {
  return egg();
}
function egg() {
  return chicken();
}
console.log(chicken() + " came first.");
// → ??
```

<br>
<br>

# ARGUMENTOS OPCIONAIS

Vamos analisar o código a seguir:

```javascript
function soma(a, b) {
  return a + b;
}

console.log(soma(12, 12, true, "soma"));
// -> 24
```

A função `soma` foi definida com dois parâmetros. Quando chamamos a função passamos 4 parâmetros e mesmo assim o JavaScript não reclama. O JavaScript é capaz de compreender a quantidade de parâmetros que uma função necessita e ignora todo o resto. No caso, temos o resultado `24`, pois os valores `true` e `"soma"` que foram passados por parâmetros foram ignorados.

Caso você passe menos parâmetros do que o necessário, o JavaScript retornará o valor `undefined`. Utilizando o exemplo anterior, caso tivéssemos passado:

```javascript
console.log(soma(12));
// -> NaN
```

O valor `NaN` (Not a Number) é retornado pois o cálculo executado foi `12 + undefined`, consequente da falta de um dos argumentos durante a chamada da função.

O resultado `undefined` pode também ser utilizado para manipular o código. Um exemplo é:

```javascript
function menos(a, b) {
  if (b === undefined) return -a;
  else return a - b;
}

console.log(menos(10));
// -> -10
console.log(menos(10, 5));
// -> 5
```

Esse comportamento acontece porque na primeira chamada da função, omitimos um dos argumentos, logo o valor `b` tornou-se undefined e passou no teste lógico `b === undefined`.  

A chamada a seguir não omitimos nenhum valor dos argumentos e então durante o teste lógica da estrutura de repetição entramos no `else`, retornando `a - b`. 


<br>
<br>

# FUNÇÕES E EFEITOS COLATERAIS
As funções são definidas naquelas que são invocadas para produzir um efeito colateral ou simplesmente retornar alguma valor. São chamadas de funções _puras_ e _impuras_...

As funções puras são aquelas que são chamadas e produzem algum tipo de valor mas não gera os _efeitos colaterais_ — uma função, por exemplo, que não utiliza variáveis globais que pode alterar outros códigos; tem característica de ser sempre chamada com os mesmo argumentos e isso a torna uma função. Em poucas palavras: _A função pura é aquela que não produz nenhum efeito colateral pois não muda qualquer estado na aplicação_.

As funções que não são consideradas puras podem retornar diferentes valores diferentes dependendo baseado em tipos de fatores e produzem efeitos colaterais que podem fazer co que seja mais complicado realizar testes por cima dela.





<br>
<br>


<br/>
<br/>

# FUNÇÕES CRESCENTES
Percebemos que precisamos de uma função em um programa quando estamos escrevendo o mesmo código várias vezes. Quanto mais linhas de códigos temos, mais chances são os erros e mais ilegível o código se torna para os programadores que vão ler. Desse modo, escolhemos um bom nome e determinamos uma função para determinada funcionalidade.

Outro motivo que normalmente precisamos de uma funcionalidade que ainda não foi escrita e por algum motivo precisa ser encapsulada em uma função própria. 

###### Abaixo teremos um exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

> A dificuldade de encontrar um bom nome para uma função é um bom indicativo de quão claro é o conceito que você está tentando encapsular. Vamos analisar um exemplo.

> Nós queremos escrever um programa que imprima dois números, sendo eles o número de vacas e galinhas em uma fazenda com as palavras Cows (vacas) e Chickens (galinhas) depois deles e algarismos zeros antes de ambos os números para que sejam sempre números de três dígitos.

> 007 Cows
>
> 011 Chickens

> Bom, claramente, isso é uma função que exige dois argumentos. Vamos codar.

~~~javascript
function printFarmInventory(cows, chickens) {
  var cowString = String(cows);
  while (cowString.length < 3)
    cowString = “0” + cowString;
  console.log(cowString + “ Cows”);
  var chickenString = String(chickens);
  while (chickenString.length < 3)
    chickenString = “0” + chickenString;
  console.log(chickenString + “ Chickens”);
}
printFarmInventory(7, 11);
~~~

> Adicionar .length após o valor de uma string nos fornecerá o tamanho (quantidade de caracteres) daquela string. Por isso, o laço de repetição while continua adicionando zeros no início da string que representa o número até que a mesma tenha três caracteres.

> Missão cumprida! Porém, no momento em que iríamos enviar o código ao fazendeiro (juntamente com uma grande cobrança, é claro), ele nos ligou dizendo que começou a criar porcos, e perguntou, se poderíamos estender a funcionalidade do software para também imprimir os porcos?

> É claro que podemos. Antes de entrar no processo de copiar e colar essas mesmas quatro linhas outra vez, vamos parar e reconsiderar. Deve existir uma forma melhor. Aqui está a primeira tentativa:

~~~javascript
function printZeroPaddedWithLabel(number, label) {
  var numberString = String(number);
  while (numberString.length < 3)
    numberString = “0” + numberString;
  console.log(numberString + “ “ + label);
}

function printFarmInventory(cows, chickens, pigs) {
  printZeroPaddedWithLabel(cows, “Cows”);
  printZeroPaddedWithLabel(chickens, “Chickens”);
  printZeroPaddedWithLabel(pigs, “Pigs”);
}

printFarmInventory(7, 11, 3);
~~~

> Funcionou! Mas o nome printZeroPaddedWithLabel é um pouco estranho. Ele é uma combinação de três coisas - imprimir, adicionar zeros e adicionar a label correta - em uma única função.

> Ao invés de tentarmos abstrair a parte repetida do nosso programa como um todo, vamos tentar selecionar apenas um conceito.

~~~javascript
function zeroPad(number, width) {
  var string = String(number);
  while (string.length < width)
    string = “0” + string;
  return string;
}

function printFarmInventory(cows, chickens, pigs) {
  console.log(zeroPad(cows, 3) + “ Cows”);
  console.log(zeroPad(chickens, 3) + “ Chickens”);
  console.log(zeroPad(pigs, 3) + “ Pigs”);
}

printFarmInventory(7, 16, 3);
~~~

> Ter uma função com um bom nome descritivo como zeroPad torna fácil para qualquer um ler e entender o código. Além disso, ele pode ser útil em outras situações, além desse programa específico. Você pode usá-lo, por exemplo, para imprimir números corretamente alinhados em uma tabela.

> O quão inteligente e versátil as nossas funções deveriam ser? Nós poderíamos escrever funções extremamente simples, que apenas adicionam algarismos para que o número tenha três caracteres, até funções complicadas, para formatação de números fracionários, números negativos, alinhamento de casas decimais, formatação com diferentes caracteres e por aí vai.

> Um princípio útil é não adicionar funcionalidades, a menos que você tenha certeza absoluta de que irá precisar delas. Pode ser tentador escrever soluções genéricas para cada funcionalidade com que você se deparar. Resista a essa vontade. Você não vai ganhar nenhum valor real com isso e vai acabar escrevendo muitas linhas de código que nunca serão usadas.
> 
<br/>
<br/>


<div align="center">

# AUTOR

</div>

<div class="footer">
    <table align="center">
        <tr>
            <td align="center"> 
		        <a href="https://github.com/yagopeixinho">
			        <img src="https://avatars.githubusercontent.com/u/81770553?v=4" width="100px;" alt="Imagem de Yago Peixinho">    
<br>
		            <sub>
		                <b>Yago Peixinho </b>
		            </sub>
		        </a> 
	        </td> 
        </tr>
   </table>
</div>
<div>

###### REFERÊNCIAS DESSE DOCUMENTO

- https://developer.mozilla.org/pt-BR/
- https://eloquentjavascript.net/

</div>
