<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> operadores | peixinho yago 
</div>

---

<br>

> nesse documento descrevemos expressões e operadores de JavaScript, _incluindo operadores e atribuições, comparações, bit a bit, lógicos,strings e especiais_</i>.

<br>

# operadores em JavaScript

é importante ressaltar que o JavaScript possui tantos operadores _binários_ quanto _urinários_ e um operador ternário que é o condicional.

### o JavaScript possui todos os tipos de operadores a seguir:

- [operadores de atribuição](#operadores-de-atribuição)
- [operadores de comparação](#operadores-de-comparação)
- [operadores aritméticos](#operadores-aritméticos)
- operadores bit a bit
- [operadores lógicos](#operadores-lógicos)
- [operadores de string](#operadores-de-string)
- [operador ternário (condicional)](#operador-ternário)
- operador vírgula
- [operador unário](#operador-urinário)
- operadores relacionais

<br>

# operadores de atribuição

um operador de atribuição atribui um valor ao operando à sua esquerda baseado no valor do operando à sua direita. No javaScript (e em muitas outras linguagens) utilizamos o "=". O "=" atribui o valor do operando à direita ao operando à esquerda. Isto é: _x = y_ atribui o valor de _y_ a _x_.

---

| nome                                                       | operador encurtado | significado  |
| ---------------------------------------------------------- | ------------------ | ------------ |
| atribuição                                                 | x = y              | x = y        |
| atribuição de adição                                       | x += y             | x = x + y    |
| atribuição de subtração                                    | x -= y             | x = x - y    |
| atribuição de multiplicação                                | x \*= y            | x = x \* y   |
| atribuição de divisão                                      | x /= y             | x = x / y    |
| atribuição de resto                                        | x %= y             | x = x % y    |
| atribuição exponencial                                     | x \*\*= y          | x = x \*\* y |
| atribuição bit-a-bit por deslocamento á esquerda           | x <<= y            | x = x << y   |
| atribuição bit-a-bit por deslocamento á direita            | x >>= y            | x = x >> y   |
| atribuiçãode bit-a-bit deslocamento á direita não assinado | x >>>= y           | x = x >>> y  |
| atribuição AND bit-a-bit                                   | x &= y             | x = x & y    |
| atribuição XOR bit-a-bit                                   | x ^= y             | x = x ^ y    |
| atribuição OR bit-a-bit                                    | x \|= y            | x = x \| y   |

<br>

# operadores de comparação

um operador de comparação compara seus operandos e retorna um valor lógico _true ou false_ baseado em se a comparação é verdadeira. As comparações são feitas baseadas em tipos númericos, lógicos, objetos ou strings. no JavaScript as strings são comparadas _com base em ordenação lexográfica utilizando os valores Unicode_. Quando você compara dois operando que não são do mesmo tipo, o JavaScript tenta converter para um tipo apropriado. É importante ressaltar que as únicas exceções a esta regras são os operadores === e o !==. Esses operadores verificam se os operandos são idênticos. Ou seja, não há uma tentativa de converter os operando em outros tipos compatíveis antes de verificar se são iguais.

---

| operador                     | descrição                                                                                                           | exemplos que retornam verdadeiro   |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| igual (==)                   | retorna verdadeiro caso os operandos sejam iguais.                                                                  | 3 == var1 <br>"3" == var1 3 == '3' |
| não igual (!=)               | retorna verdadeiro caso os operandos não sejam iguais.                                                              | var1 != 4<br> var2 != "3"          |
| estritamente igual (===)     | retorna verdadeiro caso os operandos sejam iguais e do mesmo tipo. Veja também Object.is e igualdade em JS (en-US). | 3 === var1                         |
| estritamente não igual (!==) | retorna verdadeiro caso os operandos não sejam iguais e/ou não sejam do mesmo tipo.                                 | var1 !== "3"<br> 3 !== '3'         |
| maior que (>)                | retorna verdadeiro caso o operando da esquerda seja maior que o da direita.                                         | var2 > var1<br> "12" > 2           |
| maior que ou igual (>=)      | retorna verdadeiro caso o operando da esquerda seja maior ou igual ao da direita.                                   | var2 >= var1<br> var1 >= 3         |
| menor que (<)                | Retorna verdadeiro caso o operando da esquerda seja menor que o da direita.                                         | var1 < var2<br> "12" < "2"         |
| menor que ou igual (<=)      | Retorna verdadeiro caso o operando da esquerda seja menor ou igual ao da direita.                                   | var1 <= var2<br> var2 <= 5         |

<br>

# operadores aritméticos

os operadores aritméticos padrões são:

- soma (+)
- subtração (-)
- multiplicação (\*)
- divisão (/)

esses operadores geralmente trabalham da mesma forma em todas as linguagens de programação. Eles são utilizados com valores númericos (sejam literais ou variáveis) como seus operandos e retornam um valor numérico.

```javascript
console.log(1 + 1); // imprime 2
console.log(3 + 1 == 2 + 2); // isso retorna verdadeiro
```

para complementar às operações aritméticas padrões ( +, -, \*, / ), o JavaScript nos disponibiliza operadores aritméticos que podem nos auxiliar durante o dia a dia listados na tabela a seguir:

---

| operador                             | descrição                                                                                                                                                                                                                            | exemplo                                                                                                    |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| módulo (%)                           | operador binário. Retorna o inteiro restante da divisão dos dois operandos.                                                                                                                                                          | 12 % 5 retorna 2.                                                                                          |
| incremento (++)                      | operador unário. Adiciona um ao seu operando. Se usado como operador prefixado <br(++x), retorna o valor de seu operando após a adição. Se usado como operador<br> pósfixado (x++), retorna o valor de seu operando antes da adição. | se x é 3, então ++x define x como 4 e retorna 4, enquanto x++ retorna 3 e, somente então, define x como 4. |
| decremento (--)                      | operador unário. Subtrai um de seu operando.<br> O valor de retorno é análogo àquele do operador de incremento.                                                                                                                      | se x é 3, então --x define x como 2 e retorna 2, enquanto x-- retorna 3 e, somente então, define x como 2. |
| negação (-)                          | operador unário. Retorna a negação de seu operando.                                                                                                                                                                                  | se x é 3, então -x retorna -3.                                                                             |
| adição (+)                           | operador unário. Tenta converter o operando em um número, sempre que possível.                                                                                                                                                       | +"3" retorna 3.<br> <br>+true retorna 1.                                                                   |
| operador de <br>exponenciação (\*\*) | calcula a base elevada á potência do expoente, que é, base expoente                                                                                                                                                                  | 2 ** 3 retorna 8.<br> <br>10 ** -1 retorna 0.1                                                             |

<br>

# operadores lógicos

operadores lógicos são utilizados tipicamente com valores booleanos (lógicos);

| operador         | utilização       | descrição                                                                                                                                                                                                                                           |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AND lógico (&&)  | expr1 && expr2   | (E lógico) - Retorna expr1 caso possa ser convertido para falso; senão, retorna expr2. Assim, quando utilizado com valores booleanos, && retorna verdadeiro caso ambos operandos sejam verdadeiros; caso contrário, retorna falso.                  |
| OU lógico (\|\|) | expr1 \|\| expr2 | (OU lógico) - Retorna expr1 caso possa ser convertido para verdadeiro; senão, retorna expr2. Assim, quando utilizado com valores booleanos, \|\| retorna verdadeiro caso ambos os operandos sejam verdadeiro; se ambos forem falsos, retorna falso. |
| NOT lógico (!)   | !expr            | (Negação lógica) Retorna falso caso o único operando possa ser convertido para verdadeiro; senão, retorna verdadeiro.                                                                                                                               |

outro exemplo de valores que podem ser considerados como **falso** são aqueles valores que são avaliados como _nulo, 0, string vazia ("") ou undefined_.

<br>

## exemplos práticos

##### exemplos retirados do [mnd web docs](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_Operators#operadores_logicos)

---

#### o código a seguir mostra exemplos do operador && (E lógico).

```javascript
var a1 = true && true; // t && t retorna true
var a2 = true && false; // t && f retorna false
var a3 = false && true; // f && t retorna false
var a4 = false && 3 == 4; // f && f retorna false
var a5 = "Gato" && "Cão"; // t && t retorna Cão
var a6 = false && "Gato"; // f && t retorna false
var a7 = "Gato" && false; // t && f retorna false
```

#### o código a seguir mostra exemplos do operador || (OU lógico).

```javascript
var o1 = true || true; // t || t retorna true
var o2 = false || true; // f || t retorna true
var o3 = true || false; // t || f retorna true
var o4 = false || 3 == 4; // f || f retorna false
var o5 = "Gato" || "Cão"; // t || t retorna Gato
var o6 = false || "Gato"; // f || t retorna Gato
var o7 = "Gato" || false; // t || f retorna Gato
```

#### o código a seguir mostra exemplos do operador ! (negação lógica).

```javascript
var n1 = !true; // !t retorna false
var n2 = !false; // !f retorna true
var n3 = !"Gato"; // !t retorna false
```

<br>

# avaliação curto-circuito

as expressão lógicas são testadas pelo valor iniciado da esquerda para a direita. Desse modo, é possível fazer um teste chamado "curto-circuito", utilizando as seguintes regras:

> - false && qualquercoisa é avaliado em curto-circuito como falso.
> - true || qualquercoisa é avaliado em curto-circuito como verdadeiro.

desse modo é possível verificarmos se as regras da lógica avaliada estão corretas, pois, reperando que a parte "qualquercoisa" das expressões acima não são avaliadas de forma que qualquer nova lógica implementada após não produzirá efeito nenhum.

<br>

# operadores de string

além dos operadores de comparação, que podem ser utilizados em valores tring, o operador de _concatenação_ (+) concatena dois valores string, retornando outra string que é a união dos dois operandos.

exemplos:

```javascript
console.log("minha " + "string"); // retorna a mensagem "minha string"
```

```javascript
var inicial = "mundo";
console.log("olá " + inicial); // vai ser imprimido no console a mensagem "olá mundo"
```

existe também um operador de atribuição encurtado += que pode ser utilizado para concatenar strings.

```javascript
var minhaString = "alfa";
minhaString += "beto"; // vai ser guardado na variável minhaString o valor "alfabeto"
```

## template string

como visto acima que para concatenarmos uma string precisamos utilizar o sinal (+) e estaremos juntando uma string. Entretanto, é fortemente recomendado um outro método conhecido por _template string_, que funciona da seguinte forma:

```javascript
const nome = "yago peixinho";
console.log(`meu nome é ${nome}`);
```

é nítido que dessa forma a nossa string se torna mais clara. Vamos ver detalhadamente o que aconteceu...

```javascript
const nome = "yago peixinho"; // aqui é declarado o valor do tipo Char em uma constante que possui o valor "yago peixinho"

console.log(
  `meu nome é ${nome}`
); /* utilizamos o acento grave (``) para determinarmos até aonde a nossa string vai.
exemplo: (`o texto em string vai aqui dentro`).

Para informarmos que queremos que o valor de alguma variável seja considerada, utilizamos o sinal do dólar ($) e cercamos a variável com chaves ({}).
No exemplo é dado ${nome} - levando em conta que o valor dentro da variável será o valor a ser considerado. 

Dessa forma será imprimido no console: meu nome é yago peixinho

*/
```

<br>

# operador ternário

o ternário condicional é o único operador JavaScript que utiliza três operandos. O operador pode ter um de dois valores baseados em uma condição. A sintaxe é:

```javascript
var nomeVariavel = condicao ? valor1 : valor2;
```

basicamente estamos informando que se a _condicao_ for verdadeira, a variável _nomeVariavel_ receberá o _valor1_, se for falsa, receberá o _valor2_.

```javascript
var status = idade >= 18 ? "adulto" : "menor de idade";
console.log(nomeVariavel); // será imprimido no console: "é verdadeiro", pois a condição é verdadeira, logo o valor obtido é "é verdadeiro"
```

esta declaração atribui o valor "adulto" à variável status caso idade seja dezoito ou mais. Caso contrário, atribui o valor "menor de idade".

<br>

# operadores unário


<br>
<br>
<br>

---

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

#### referências desse documento

- https://developer.mozilla.org/pt-BR/
- https://eloquentjavascript.net/

</div>
