<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> JavaScript Script | Operadores
</div>

---

<br>

> Nesse documento descrevemos expressões e operadores de JavaScript, _incluindo operadores e atribuições, comparações, bit a bit, lógicos,strings e especiais_</i>.

<br>

# OPERADORES EM JAVASCRIPT
- [Operadores de atribuição](#operadores-de-atribuição)
- [Operadores de comparação](#operadores-de-comparação)
- [Operadores aritméticos](#operadores-aritméticos)
- [Operadores lógicos](#operadores-lógicos)
  - [Avaliação curto-circuito](#avaliação-curto-circuito)
- [Operadores de string](#operadores-de-string)
  - [Template String](#template-string)
- [Operador ternário](#operador-ternário)
- [Operador unário](#operador-unário)

Primeiramente, é importante ressaltar que o JavaScript possui tantos operadores _binários_ quanto _urinários_ e um operador ternário que é o condicional.

<br>
<br>

# OPERADORES DE ATRIBUIÇÃO
Um operador de atribuição atribui um valor ao operando à sua esquerda baseado no valor do operando à sua direita. No javaScript (e em muitas outras linguagens) utilizamos o "`=`". O "`=`" atribui o valor do operando à direita ao operando à esquerda. Isto é: `x = y` atribui o valor de `y` a `x`.

| Nome                                                       | Operador encurtado | Significado  |
| ---------------------------------------------------------- | ------------------ | ------------ |
| Atribuição                                                 | x = y              | x = y        |
| Atribuição de adição                                       | x += y             | x = x + y    |
| Atribuição de subtração                                    | x -= y             | x = x - y    |
| Atribuição de multiplicação                                | x \*= y            | x = x \* y   |
| Atribuição de divisão                                      | x /= y             | x = x / y    |
| Atribuição de resto                                        | x %= y             | x = x % y    |
| Atribuição exponencial                                     | x \*\*= y          | x = x \*\* y |
| Atribuição bit-a-bit por deslocamento à esquerda           | x <<= y            | x = x << y   |
| Atribuição bit-a-bit por deslocamento à direita            | x >>= y            | x = x >> y   |
| Atribuição de bit-a-bit deslocamento à direita não assinado | x >>>= y           | x = x >>> y  |
| Atribuição AND bit-a-bit                                   | x &= y             | x = x & y    |
| Atribuição XOR bit-a-bit                                   | x ^= y             | x = x ^ y    |
| Atribuição OR bit-a-bit                                    | x \|= y            | x = x \| y   |

<br>
<br>

# OPERADORES DE COMPARAÇÃO
Um operador de comparação compara seus operandos e retorna um valor lógico `true` ou `false` baseado em se a comparação é verdadeira. As comparações são feitas baseadas em tipos númericos, lógicos, objetos ou strings. no JavaScript as strings são comparadas _com base em ordenação lexográfica utilizando os valores Unicode_. Quando você compara dois operando que não são do mesmo tipo, o JavaScript tenta converter para um tipo apropriado. É importante ressaltar que as únicas exceções a esta regras são os operadores === e o !==. Esses operadores verificam se os operandos são idênticos. Ou seja, não há uma tentativa de converter os operando em outros tipos compatíveis antes de verificar se são iguais.

| Operador                     | Descrição                                                                                                           | Exemplos que retornam verdadeiro   |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| Igual (==)                   | Retorna verdadeiro caso os operandos sejam iguais.                                                                  | 3 == var1 <br>"3" == var1 3 == '3' |
| Não igual (!=)               | Retorna verdadeiro caso os operandos não sejam iguais.                                                              | var1 != 4<br> var2 != "3"          |
| Estritamente igual (===)     | Retorna verdadeiro caso os operandos sejam iguais e do mesmo tipo. Veja também Object.is e igualdade em JS (en-US). | 3 === var1                         |
| Estritamente não igual (!==) | Retorna verdadeiro caso os operandos não sejam iguais e/ou não sejam do mesmo tipo.                                 | var1 !== "3"<br> 3 !== '3'         |
| Maior que (>)                | Retorna verdadeiro caso o operando da esquerda seja maior que o da direita.                                         | var2 > var1<br> "12" > 2           |
| Maior que ou igual (>=)      | Retorna verdadeiro caso o operando da esquerda seja maior ou igual ao da direita.                                   | var2 >= var1<br> var1 >= 3         |
| Menor que (<)                | Retorna verdadeiro caso o operando da esquerda seja menor que o da direita.                                         | var1 < var2<br> "12" < "2"         |
| Menor que ou igual (<=)      | Retorna verdadeiro caso o operando da esquerda seja menor ou igual ao da direita.                                   | var1 <= var2<br> var2 <= 5         |

<br>
<br>

# OPERADORES ARITMÉTICOS
Os operadores aritméticos padrões são:

- Soma (`+`)
- Subtração (`-`)
- Multiplicação (`*`)
- Divisão (`/`)

Esses operadores geralmente trabalham da mesma forma em todas as linguagens de programação. Eles são utilizados com valores númericos (sejam literais ou variáveis) como seus operandos e retornam um valor numérico.

```javascript
console.log(1 + 1); // imprime 2
console.log(3 + 1 == 2 + 2); // isso retorna verdadeiro
```

Para complementar às operações aritméticas padrões (` +, -, \*, / `), o JavaScript disponibiliza operadores aritméticos que podem nos auxiliar durante o dia a dia listados na tabela a seguir:

---

| Operador                             | Descrição                                                                                                                                                                                                                            | Exemplo                                                                                                    |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| Módulo (%)                           | Operador binário. Retorna o inteiro restante da divisão dos dois operandos.                                                                                                                                                          | 12 % 5 retorna 2.                                                                                          |
| Incremento (++)                      | Operador unário. Adiciona um ao seu operando. Se usado como operador prefixado <br(++x), retorna o valor de seu operando após a adição. Se usado como operador<br> pósfixado (x++), retorna o valor de seu operando antes da adição. | Se x é 3, então ++x define x como 4 e retorna 4, enquanto x++ retorna 3 e, somente então, define x como 4. |
| Decremento (--)                      | Operador unário. Subtrai um de seu operando.<br> O valor de retorno é análogo àquele do operador de incremento.                                                                                                                      | Se x é 3, então --x define x como 2 e retorna 2, enquanto x-- retorna 3 e, somente então, define x como 2. |
| Negação (-)                          | Operador unário. Retorna a negação de seu operando.                                                                                                                                                                                  | Se x é 3, então -x retorna -3.                                                                             |
| Adição (+)                           | Operador unário. Tenta converter o operando em um número, sempre que possível.                                                                                                                                                       | +"3" retorna 3.<br> <br>+true retorna 1.                                                                   |
| Operador de <br>exponenciação (\*\*) | Calcula a base elevada á potência do expoente, que é, base expoente                                                                                                                                                                  | 2 ** 3 retorna 8.<br> <br>10 ** -1 retorna 0.1                                                             |

<br>
<br>

# OPERADORES LÓGICOS
Operadores lógicos são utilizados tipicamente com valores booleanos (lógicos);

| Operador         | Utilização       | Descrição                                                                                                                                                                                                                                           |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AND lógico (&&)  | expr1 && expr2   | (E lógico) - Retorna expr1 caso possa ser convertido para falso; senão, retorna expr2. Assim, quando utilizado com valores booleanos, && retorna verdadeiro caso ambos operandos sejam verdadeiros; caso contrário, retorna falso.                  |
| OU lógico (\|\|) | expr1 \|\| expr2 | (OU lógico) - Retorna expr1 caso possa ser convertido para verdadeiro; senão, retorna expr2. Assim, quando utilizado com valores booleanos, \|\| retorna verdadeiro caso ambos os operandos sejam verdadeiro; se ambos forem falsos, retorna falso. |
| NOT lógico (!)   | !expr            | (Negação lógica) Retorna falso caso o único operando possa ser convertido para verdadeiro; senão, retorna verdadeiro.                                                                                                                               |

Outro exemplo de valores que podem ser considerados como `falso` são aqueles valores que são avaliados como `nulo`, `0`, string vazia (`""`) ou `undefined`.

<br>

## EXEMPLOS PRÁTICOS
###### EXEMPLOS RETIRADOS DO [MND WEB DOCS](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_Operators#operadores_logicos)
---

#### O código a seguir mostra exemplos do operador && (E lógico).

```javascript
var a1 = true && true; // t && t retorna true
var a2 = true && false; // t && f retorna false
var a3 = false && true; // f && t retorna false
var a4 = false && 3 == 4; // f && f retorna false
var a5 = "Gato" && "Cão"; // t && t retorna Cão
var a6 = false && "Gato"; // f && t retorna false
var a7 = "Gato" && false; // t && f retorna false
```

#### O código a seguir mostra exemplos do operador || (OU lógico).

```javascript
var o1 = true || true; // t || t retorna true
var o2 = false || true; // f || t retorna true
var o3 = true || false; // t || f retorna true
var o4 = false || 3 == 4; // f || f retorna false
var o5 = "Gato" || "Cão"; // t || t retorna Gato
var o6 = false || "Gato"; // f || t retorna Gato
var o7 = "Gato" || false; // t || f retorna Gato
```

#### O código a seguir mostra exemplos do operador ! (negação lógica).

```javascript
var n1 = !true; // !t retorna false
var n2 = !false; // !f retorna true
var n3 = !"Gato"; // !t retorna false
```

<br>

## AVALIAÇÃO CURTO-CIRCUITO

As expressão lógicas são testadas pelo valor iniciado da esquerda para a direita. Desse modo, é possível fazer um teste chamado "curto-circuito", utilizando as seguintes regras:

> - `false && qualquercoisa` é avaliado em curto-circuito como falso.
> - `true || qualquercoisa` é avaliado em curto-circuito como verdadeiro.

Desse modo é possível verificarmos se as regras da lógica avaliada estão corretas, pois, analisando que a parte `qualquercoisa` das expressões acima não são avaliadas de forma que qualquer nova lógica implementada após não produzirá efeito nenhum.

<br>
<br>

# OPERADORES DE STRING
Além dos operadores de comparação, que podem ser utilizados em valores String, o operador de _concatenação_ (`+`) concatena dois valores string, retornando outra string que é a união dos dois operandos.

```javascript
console.log("Minha " + "String"); // retorna a mensagem "Minha String"
```

```javascript
var inicial = "mundo";
console.log("Olá " + inicial); // vai ser imprimido no console a mensagem "Olá mundo"
```

Existe também um operador de atribuição encurtado += que pode ser utilizado para concatenar strings.

```javascript
var minhaString = "Alfa";
minhaString += "beto"; // vai ser guardado na variável minhaString o valor "Alfabeto"
```

<br>

## TEMPLATE STRING
Como visto anteriormente, para concatenarmos uma string precisamos utilizar o sinal (`+`) e estaremos juntando uma string. Entretanto, é fortemente recomendado um outro método conhecido por _template string_, que funciona da seguinte forma:

```javascript
const nome = "Yago Peixinho";
console.log(`Meu nome é ${nome}`);
```

É nítido que dessa forma a nossa string se torna mais clara. Vamos ver detalhadamente o que aconteceu...

```javascript
const nome = "Yago Peixinho"; //Aaqui é declarado o valor do tipo Char em uma constante que possui foi atribuído o valor "Yago Peixinho"

console.log(
  `Meu nome é ${nome}`
); /* Utilizamos o acento grave (``) para determinarmos até aonde a nossa string vai. (`o texto em string vai aqui dentro`).

Para informarmos que queremos que o valor de alguma variável seja considerada, utilizamos o sinal do dólar ($) e cercamos a variável com chaves ({}).
No exemplo é dado ${nome} - levando em conta que o valor dentro da variável será o valor a ser considerado. 

Dessa forma será imprimido no console: meu nome é Yago Peixinho

*/
```

<br>
<br>

# OPERADOR TERNÁRIO
O operador ternário condicional é o único operador JavaScript que utiliza três operandos. O operador pode ter um de dois valores baseados em uma condição. A sintaxe é:

```javascript
var nomeVariavel = condicao ? valor1 : valor2;
```

Basicamente estamos informando que se a `condicao` for verdadeira, a variável `nomeVariavel` receberá o `valor1`, se for falsa, receberá o `valor2`.

~~~javascript
var status = idade >= 18 ? "Adulto" : "Menor de idade";
~~~

Esta declaração atribui o valor `"Adulto"` à variável status caso idade seja dezoito ou mais. Caso contrário, atribui o valor `"menor de idade"`.

<br>
<br>

# OPERADOR UNÁRIO
O operador unário é uma operação realizada apenas com um operando. Por exemplo, o operador `delete` apaga um objeto, uma propriedade do objeto ou um determinado elemento em alguma posição específica de uma matriz.

~~~javascript
delete nomeObjeto;
delete nomeObjeto.propriedade;
delete nomeObjeto[indice];
~~~

`nomeObjeto` é o nome de um objeto... `propriedade` é uma propriedade existente no objeto e `índice` é um inteiro que representa a localização de um elemento na matriz. Você pode usar o operador `delete` para deletar variáveis declaradas implícitamente, mas não aquelas declaradas com `var`. Um exemplo de declaração implícita é `nomeVariavel = 12`, pois não utilizamos o nome reservado *var*; é importante ressaltar também que variáveis declaradas de forma explícita são consideradas variáveis globais.

Caso o operador `delete` seja bem-sucedido, ele defina a propriedade ou elemento para `undefined`. O operador `delete` retorna verdadeiro se a operação foi possível e retorna falso caso a operação não for possível.

##### _Exemplos retirados do [mnd web docs](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_Operators#operadores_logicos)_

~~~javascript
x = 42; 
var y = 43;

delete x; // Retorna true, pois pode ser apagado por ter sido declarada implicitamente
delete y; // Retorna false, pois não pode ser apagada por ter sido declarada implicitamente
~~~

~~~javascript 
meuObj = new Number();
meuObj.h = 4; // Cria  propriedade h

delete meuObj.h; // Retorna true, pois pode apagar as propriedades de um objeto definidas pelo usuário
delete meuObj; // Retorna true pois pode ser apagado por ter sido declarado implicitamente
~~~

~~~javascript 
delete Math.PI; // Retorna false, pois não é possível apagarmos propriedades predefinidas
~~~

<br>

## APAGANDO ELEMENTO DOS ARRAYS
A princípio é importante ressaltar que quando você apaga um elemento de um array, o tamanho do array não é afetado. Caso você apague o elemento `carros[4]`, o elemento `carros[4]` ainda permanecerá na mesma posição, tornando-se um elemento `undefined`. 

Quando é utilizado um `delete` em um elemento do array, aquele elemento é removido imediatamente no array e o valor daquele array que foi deletado é substituído para `undefined` e o valor continua sendo endereçável retornando `undefined` porém qualquer comparação com esse elemento deletado será considerada negativa.

~~~javascript
var comidasFavoritas = new Array('Pizza', 'Hamburguer', 'Batatas', 'Chocolate');

delete comidasFavoritas[3];

if(3 in comidasFavoritas){
    // Isto não será executado
}
~~~

Caso você queira que o elemento de um array exista mas não quer que ele tenha um valor definido, utilize `undefined` em vez do `delete`. Desse modo o elemento daquela matriz ainda existe, porém com um valor indefinido.

~~~javascript
var comidasFavoritas = new Array('Pizza', 'Hamburguer', 'Batatas', 'Chocolate');

comidasFavoritas[3] = undefined;

if(3 in comidasFavoritas){
    // Isto será executado
}
~~~


<br>
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
