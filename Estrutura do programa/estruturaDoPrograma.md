<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> JavaScript Script | Estrutura do programa 
</div>

---

<br>

> Para que seja possível trabalhar com tais quantidades de bits sem ficar perdido, você popde separá-los em partes que representam pedaços de informações. No ambiente JavaScript essas partes são chamadas de _valores_.

<br>

# ESTRUTURA DO PROGRAMA
- [Expressões e afirmações](#expressões-e-afirmações)
- [Ponto e vírgula](#ponto-e-vírgula)
- [Variáveis](#variáveis)
- [Palavra-chaves e palavras reservadas](#palavras-chave-e-palavras-reservadas)
- [Funções](#funções)
- [Fluxo de controle](#fluxo-de-controle)
- [Estrutura de repetição](#estrutura-de-repetição)

A estrutura do programa é um dos pontos mais importantes. Iremos expandir nosso domínio da linguagem para que possamos expressar algo mais significativo. É importante salientar que a estrutura de um programa é a sequência de funções (módulos) que em conjunto irão permitir resolver o problema proposto.

<br>
<br>

# EXPRESSÕES E AFIRMAÇÕES
um fragmento de código que produz um valor é chamado de **expressão**. Os valores são escritos de forma literal como `22` ou `"uma string"` é uma expressão. Uma expressão em parênteses também é considerado uma expressão, bem como operadores binários aplicados a duas expressõues ou um unário aplicado a uma.

Basicamente uma **expressão** consiste em qualquer unidade válida de código que é resolvida como um valor.

> É importante ressaltar que existem dois tipos de expressões, aquelas que atribuem um valor a uma variável e aquelas que possuem um valor.
>
> A expressão `y = 21` é uma expressão que atribui o valor a uma variável, que utiliza o `=` para atribuir o 21 a variável `y`; a expressão em si é avalida como 21.
>
> `21 + 12` é um exemplol do tipo de expressão que possui um valor. É importante ressaltar que está operação utiliza o operador `+` para somar os valores 21 e 12 sem atribuir o resultado 33 a uma variável.

Expressões que o JavaScript utiliza

- Aritmética, como números, por exemplo, `7.323`
- String, como caracteres, por exemplo, `"Melanie"` ou `1221`
- Lógica, como verdadeira ou falsa, por exemplo, `true` ou `false`
- Expressões primárias, como palavras reservadas, por exemplo, `this`
- Expressões lado esquerdo, como por exemplo: `var nomeObjeto = new tipoObjeto([parametro1, parametro2, ..., parametro3])`


<br>
<br>

# PONTO E VÍRGULA
No JavaScript apesar de ser permitido instruções sem ponto e vírgula `;`, é recomendado que se use a cada linha pois sem o fazer, é possível que haja problemas na execução do seu código. O ponto e vírgula, como em muitas linguagens, é o símbolo que informa ao computador que a instrução foi finalizada para o JavaScript.

## Sem o ponto e vírgula pode haver erros em sintaxe

```javascript
console.log("teste");
console.log("testando");
```

Comprimindo, o código ficaria dessa forma

```javascript
console.log('teste')console.log('testando')
```

Gerando o famoso erro:

> Uncaught SyntaxError: Unexpected identifier
> <br>

Desse modo, utilizamos o ponto e vírgula, para que o erro seja prevenido pois separaria as intruções em JavaScript, delimitando a separação dos códigos fazendo com que o JavaScript consiga interpretar de forma concreta. Com isso em mente, é nítido o motivo de quase os programadores experientes em JavaScript recomendarem o uso de ponto e vírgula.

A forma correta do exemplo mostrado seria:

```javascript
console.log("teste");
console.log("testando");
```

<br>
<br>


# VARIÁVEIS
O programa se lembra das coisas que produzimos, expressões, declarações... Quando produzimos valores novos sem necessariamente apagar os antigos pois o JavaScript fornece uma coisa chamada `variável`.

```javascript
var minhaVariavel = 12 * 3;
```

A variável _representada pela palavra especial `var`_, é o indicativo que uma variável vai ser criada, que é seguida pelo nome da variável e se quisérmos imediatamente declararmos o valor dessa variável podemos definir após o operador `=` e uma expressão.

```javascript
var nomeVariavelCriada = expressão;
var idadeAluno = 19;
```

Após a variável ser definida, ela pode ser chamada pelo seu nome

```javascript
var notaPrimeiraProva = 9;
console.log(notaPrimeiraProva + notaPrimeiraProva);
```

Vai ser retornado o valor `18`, pois na segunda linha fizemos a adição da variável `notaDaPrimeiraProva` + `notaDaPrimeiraProva`. Isso acontece pois o valor que essa variável guarda é _9_, logo, 9 + 9 = 18. É importante ressaltar que não existiu nenhuma modificação no valor dessa variável.

Os nomes das variáveis possuem algumas regras, entre elas:

- Não pode ser utilizado palavras reservadas (como `var`)
- Não pode conter espaços
- Dígitos numéricos podem ser incluídos (como `alunoNota10`), mas a variável não pode ser iniciada com um número, (como `30Anos`)
- o nome de uma variável não pode incluir pontuação, exceto pelos caracteres (como `$ e _`)

É importante ressaltar que o nome _variável_ faz jus a sua utilidade. As variáveis podem alterar os seus valores a qualquer momento utilizando o operador `=`, que pode ser utilizado qualquer hora em variáveis existentes para poder desconectar o valor antigo e colocar um atual

```javascript
var luzes = "ligada";

luzes = "desligado";
```

No bloco visto anteriormente, o valor da variável `var luzes` foi definido ainda durante a declaração com a expressão `"ligada"`, entretanto, uma linha a baixo o valor `"ligada"` da variável foi substituído para o valor `"desligado"`.


> Você deve imaginar variáveis como tentáculos, ao invés de caixas. Elas não contêm valores; elas os agarram - duas variáveis podem referenciar o mesmo valor. Somente os valores que o programa mantém tem o poder de ser acessado por ele. Quando você precisa se lembrar de algo, você aumenta o tentáculo para segurar ou recoloca um de seus tentáculos existentes para fazer isso.
> Quando você define uma variável sem fornecer um valor a ela, o tentáculo fica conceitualmente no ar - ele não tem nada para segurar. Quando você pergunta por um valor em um lugar vazio, você recebe o valor `undefined`.

![polvo](assets/images/polvoAnalogiaVariavel.jpg)
###### Exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

<br>

Um exemplo. Para lembrar da quantidade de dólares que Luigi ainda lhe deve, você cria uma variável. E então quando ele lhe paga 35 dólares, você dá a essa variável um novo valor.

```javascript
var luigisDebt = 140;
luigisDebt = luigisDebt - 35;
console.log(luigisDebt);
// 105
```

<br>
<br>

# PALAVRAS-CHAVE E PALAVRAS RESERVADAS
Algumas palavras tem significados especiais, um exemplo é a palavra `var`, que é utilizada na declaração de variáveis. São chamadas de _keywords_ (palavras-chave) as palavras que são reservadas exclusivamente para alguma finalidade baseando na estrutura da linguagem. A lista de palavras reservadas é longa mas algumas delas são:

> `break` `catch` `this` `with` `void` `while` `static` `swtich` `try` `typeof` `private` `yield` `instanceof` `let` `const`

É importante ressaltar que não é extremamente importante memorizar as palavras reservadas, pois existem várias e futuramente novas podem vir a surgir. Lembre-se que este pode ser um problema caso algo não funcionar como esperado.

<br>
<br>

# FUNÇÕES
Uma função é um pedaço de programa envolvido por um valor que pode ser aplicado para executar alguma funcionalidade. O `alert`, por exemplo, é uma função que tem como objetivo mostrar uma pequena caixa de diálogo com uma mensagem.

```javascript
alert("hello, world!");
```

Quando você utiliza uma função, você está _chamando_, _invocando_ ou _aplicando_ uma função.

Para chamar uma função basta utilizar os parênteses depois da expressão que produz um valor de função. No exemplo que foi mostrado a função `alert` utilizou os parênteses para ser chamada e dentro dele é perceptível que temos uma `string` escrita `"hello, world!"`, que aparece na chamada do diálogo. Os valores dentro da função (dentro dos parênteses) são chamados de _arguments_ (argumentos). A função `alert` utiliza apenas um argumento e outras funções utilizam diferentes valores.

<br>
<br>

# FLUXO DE CONTROLE
Em um programa que possui mais que uma declaração, as declarações são executadas de cima para baixo. Por exemplo

<br>

## FLUXO DE CONTROLE EM LINHA RETA

```javascript
var numeroPar = 12;
var numeroImpar = 11;

console.log(numeroPar + numeroImpar);
```

o exemplo utilizado é um exemplo válido, pois como dito anteriormente, a leitura do código é feito de cima para baixo, tendo como último comando o `console.log` que retorna a soma do `numeroPar` e `numeroImpar`. A representação desse fluxo seria uma linha reta:

![linhaReta](assets/images/linhaRetaExemploFluxoReto.png)
###### Exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

<br>
<br>


# EXECUÇÃO CONDICIONAL

## IF / ELSE
Além do fluxo de controle em linha reta, temos também a _execução condicional_, onde escolhemos entre duas rotas diferentes baseadas em um valor lógico (booleano):

![linhaReta](assets/images/controleCondicionalExemplo.png)
###### Exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

<br>

A execução condicional no JavaScript é denominada com a palavra-chave `if`, que nos casos mais simples permite que um código seja executado se _e somente se_ determinada condição existir.

```javascript
var numero = 12;

if (numero === 12) {
  alert("entrou nessa variável");
}
```

No bloco anterior a condicional foi atendida pois a variável `numero` é idêntica (_verificado por causa do sinal de ===_) e desse modo ela disparou a função `alert`. Como percebido no código anterior, utilizamos os parênteses após o `if` para determinarmos o teste lógico e verificar se ele é verdadeiro _retorna `true` caso a expressão for verdadeira_ e _retorna `false` caso a expressão for falsa_.

Podemos utilizar, além do `if` a palavra-chave `else`, que pode ser utilizada juntamente com o `if` para criar dois caminhos distintos de execução. É importante ressaltar que caso a execução condicional `if` possuir um `else`, um dos dois caminhos são atendidos obrigatoriamente...

```javascript
var nomeUsuario = "Carlos";

if (nomeUsuario === "Robson") {
  alert("o nome do usuário não é Carlos");
} else {
  alert("o nome do usuário não é Robson");
}
```

No exemplo anterior a condicional entra no `else`, pois na primeira linha foi definido que o nome do usuário é `"Carlos"` e não `"Robson"`. Isso aconteceu porque o teste condicional verificou se o `nomeUsuario === "Robson"`, ou seja, se o valor da variável `nomeUsuario` possui o valor idêntico a `"Robson"`, o que não aconteceu, desse modo a condição não foi atendida e entrou no bloco `else`.

Se tivermos mais do que dois caminhos para escolher, é possível implementar mútiplos pares de `if/else` que podem ser encadeados:

```javascript
var num = 12;

if (num < 10) {
  alert("pequeno");
} else if (num < 100) {
  alert("medio");
} else {
  alert("grande");
}
```

Seguindo essa lógica, o programa irá verificar se a variável `num` é inferior a 10, se for, chama a função `alert("pequeno")` e termina a sua execução. Se não for, ele irá entrar no segundo teste que é `if(num < 100)` e caso seja verdadeiro, o número está entre 10 e 100 e a função `alert("medio")` será mostrado. Caso contrário, o segundo e último else será escolhido.

![linhaReta](assets/images/controleCondicionalElseIf.png)
###### Exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

<br>

## SWITCH
Além do comando de execução condicional `if`, temos outro comando de execução condicional no JavaScript que herdou uma sintaxe da mesma linha das linguagens de programação _C_ e _Java_.

~~~javascript
switch(prompt("Qual a sua estação favorita?")){
  case "verão":
    console.log("Então você gosta de calor");
    break;
  case "outono":
    console.log("Eu também adoro as folhas cadentes do outono!");
    break;
  case "inverno":
    console.log("Café ou chocolate quente?");
  case "primavera":
    console.log("O verão está vindo aí...");
    break;
  default:
    console.log("Estação informada não foi reconhecida");
    break;
}
~~~

Dentro do bloco envolvido pelo `switch` é possível colocar rótulos `case`. Durante a execução, o programa irá pular para o bloco corresponte ao valor que o `switch` fornece (no caso a informação inserida pelo usuário por causa do `prompt`), caso o valor fornecido pelo usuário seja um valor que não foi definido como um dos `case` o programa irá entrar na linha `default`. 

No programa as declarações são executadas até seja encontrado uma declaração `break`. No nosso programa no `case "inverno":` pode não temos a declaração `break`, logo o interpretador JavaScript irá compartilhar o código entre os `cases`, lendo o `case` que vem abaixo, por isso é importante ter cuidado pois é fácil esquecer um `break` e isso fará com que o programa execute algo de modo o qual você não queira executar.


<br>

# ESTRUTURA DE REPETIÇÃO

## WHILE
Caso quiséssemos imprimir os números de forma crescente de 0 a 12, uma forma que poderíamos fazer isso seria:

```javascript
console.log(0);
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
console.log(6);
console.log(7);
console.log(8);
console.log(9);
console.log(10);
console.log(11);
console.log(12);
```

Entretanto, fazermos isso dessa forma (além de trabalhoso caso seja necessário chegarmos até número grandes) é deselegante. Pensando nisso surgiram os _loops_ de repetição.

![linhaReta](assets/images/loopsDeRepeticao.png)
###### Exemplo retirado do livro Eloquente JavaScript traduzido em português retirados do GitHub - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

<br>

A ideia do _loops de repetição_ é voltarmos a determinado ponto do nosso programa e repetir determinado processamento. Vamos utilizar o código demonstrado anteriormente _(o console.log de 0 até 10)_ e utilizarmos a estrutura de repetição `while`. 

~~~javascript
var number = 0;
while (number <= 12){
  console.log(number);
  number = number + 1;
}
~~~

A declaração iniciada com a palavra `while` é responsável por criar um loop. Após a palavra `while` temos parêteses que funcionam similar a declração `if`. O _loop_ irá se repetir até que a expressão lógica (_o teste lógico dentro dos parênteses_) seja atendida e convertida para o valor booleano seja igual a `true`. 

É importante ressaltar que processamentos envolvidos por chaves são chamados de __blocos__. Com isso em mente, é importante ressaltar que é possível identificar um processamento dentro das chaves: Imprimimos na tela o valor da variável `number` com o `console.log()`. Esse _loop_ irá se repetir até que a variável `number` atinja o valor `12` – esse valor foi definido na expressão lógica dentro dos parêteses. No início de cada repetição será imprimido o valor atual da variável `number` e toda vez que o _loop_ se repete é incrementado por `1`; no início de cada repetição ele é novamente comparador com o número `12` para verificar se a condicional foi atendida.

<br>
<br>

## DO
O _loop_ `do` é uma estrutura de repetição similar ao `while`, a única diferença é que o do irá executar as declarações pelo menos uma vez antes de fazer a verificação se o __loop_ deve ser encerrado ou não.

~~~javascript
do {
  var cidade = prompt("Qual a sua cidade?");
  console.log(cidade)
} while (!cidade);
~~~

No código acima  o programa esse _loop_ será repetido até que a idade do usuário seja inserida pois a verificação lógica possui `!idade`. É importante ressaltar que quando uma variável recebe o valor `""` (uma string vazia) é retornado `false`. O sinal `!` significa __negação__, a variável sempre terá o seu valor oposto. Todas as `strings` exceto o `""` convertem para true, verificando quando algum valor diferente de `""` foi fornecido pelo usuário.

<br>
<br>


## LOOPS FOR
Muito dos loops que conhecemos atualmente utilizam uma variável contadora que monitora a situação do _loop_. Nos exemplos anteriores temos a variável `number` que é atualizado toda vez em que o loop acontece. Por esse padrão ser muito comum, muitas linguagens nos permite utilizar de uma estrutura compreensiva chamada _loop_ `for`.

~~~javascript
for(var number = 0; number <= 2; number = number + 1){
  console.log(number)
}
~~~

O trecho de código anterior faz exatamente o que fizemos anteriormente no [`while`](#while), a única diferença entre eles é que todos os envolvidos para verificar o "estado" do _loop_ estão relacionados, tornando o código mais objetivo e compreensivel. 

Os parênteses após a declaração `for` deve conter dois ponto e vírgula "`;`", A primeira parte inicializa o loop que normalmente definimos uma variável. A segunda parte é aonde verificamos se o _loop_ deve ou não continuar. A última parte atualiza o estado do loop após cada iteração.

<br>

### QUEBRANDO EXECUÇÃO DE UM LOOP
Sabemos que quando temos uma expressão lógica que possua o valor lógico `false` conseguimos parar um _loop_. Entretanto, é importante termos em mente que existem outras declarações que podem parar _loops_.

Existe uma declaração especial conhecida por `break` que tem o poder de finalizar a execução e sair do loop.

~~~javascript
for(var current = 20; ; current++){
  if(current == 12){
    break;
  }
}
~~~

A construção desse `for` não possui o teste lógica que verifica o fim do loop, ou seja... a única forma desse _loop_ parar é quando a declaração `break` contida no bloco for executada.

Caso você acidentalmente escrever uma condição que sempre retorne o valor `true`, seu programa ficará preso em um _loop infinito_. Um loop infinito não vai parar de ser executado até que haja uma declaração `break` ou uma condição que retorne o valor `true`. Na grande maioria dos casos o _loop infinito_ é algo ruim.

A palavra chave `continue` é similar ao `break` pois também é algo que influencia o comportamento do loop. Quando informamos o comando `continue` dentro de um _loop_, o controle de execução pula para fora do corpo e executa novamente a próxima iteração do _loop_  (em palavras simples o _loop_ volta do início e refaz a execução do bloco novamente).

<br>
<br>

# COMENTÁRIOS
Durante a codificação, muitas vezes o código em si não transmite todas as informações necessárias ou a informação é transmitida de forma tão enigmática que é impossível um ser humano (às vezes até quem mesmo criou o código) entender. Nessas ou em outras ocasiões podemos utilizar os comentários para isso.

O comentário em um código é um pedaço que o interpretador JavaScript ignora. No JavaScript temos duas maneiras de escrever comentários. 
- Podemos escrever os comentários em uma única linha
- Podemos escrever os comentários em mútiplas linhas

Para escrevermos o comentário em uma única linha utilizamos dois caracteres barra (`//`) e após a barra digitamos o comentário. 

~~~javascript
// Isso é um comentário e será ignorado pelo interpretador JavaScript
~~~
~~~javascript
// Essa variável recebe o resultado da equação
var resultadoDaEquacao = calcularEquacao(1, 2);
~~~

Nos blocos de código acima percebemos nitidamente os comentários selecionado 



<br>
<br>

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
