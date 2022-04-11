<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> valores | peixinho yago 
</div>

---

<br>

> para que seja possível trabalhar com tais quantidades de bits sem ficar perdido, você popde separá-los em partes que representam pedaços de informações. No ambiente JavaScript essas partes são chamadas de _valores_.

<br>

# estrutura do programa

## sumário
- [expressões e afirmações](#expressões-e-afirmações)
- [ponto e vírgula](#ponto-e-vírgula)
- [variáveis](#variáveis)
- [palavra-chaves e palavras reservadas](#palavras-chave-e-palavras-reservadas)

a estrutura do programa é um dos pontos mais importantes. Iremos expandir nosso domínio da linguagem para que possamos expressar algo mais significativo. É importante salientar que a estrutura de um programa é a sequência de funções (módulos) que em conjunto irão permitir resolver o problema proposto. 

<br>

# expressões e afirmações
um fragmento de código que produz um valor é chamado de __expressão__. Os valores são escritos de forma literal como `22` ou `"uma string"` é uma expressão. Uma expressão em parênteses também é considerado uma expressão, bem como operadores binários aplicados a duas expressõues ou um unário aplicado a uma.

basicamente uma __expressão__ consiste em qualquer unidade válida de código que é resolvida como um valor. 

> é importante ressaltar que existem dois tipos de expressões, aquelas que atribuem um valor a uma variável e aquelas que possuem um valor.
>
> a expressão `y = 21` é uma expressão que atribui o valor a uma variável, que utiliza o `=` para atribuir o 21 a variável `y`; a expressão em si é avalida como 21.
>
> `21 + 12` é um exemplol do tipo de expressão que possui um valor. É importante ressaltar que está operação utiliza o operador `+` para somar os valores 21 e 12 sem atribuir o resultado 33 a uma variável.

expressões que o JavaScript utiliza
- aritmética, como números, por exemplo, `7.323`
- string, como caracteres, por exemplo, `"Melanie"` ou `1221`
- lógica, como verdadeira ou falsa, por exemplo, `true` ou `false` 
- expressões primárias, como palavras reservadas, por exemplo, `this`
- expressões lado esquerdo, como por exemplo: `var nomeObjeto = new tipoObjeto([parametro1, parametro2, ..., parametro3])`

no livro Eloquente JavaScript é citado da seguinte forma uma expressão:

> Se uma expressão corresponde a um fragmento de senteça, _uma afirmação_, no JavaScript, corresponde a uma dfrase compelta em linguagem humana. Um programa é simplesmente uma lista de afirmações.

<br>

# ponto e vírgula
no JavaScript apesar de ser permitido instruções sem ponto e vírgula `;`, é recomendado que se use a cada linha pois sem o fazer, é possível que haja problemas na execução do seu código. O ponto e vírgula, como em muitas linguagens, é o símbolo que informa ao computador que a instrução foi finalizada para o JavaScript.

## sem o ponto e vírgula pode haver erros em sintaxe

~~~javascript
console.log('teste')
console.log('testando')
~~~

comprimindo, o código ficaria dessa forma

~~~javascript
console.log('teste')console.log('testando')
~~~

gerando o famoso erro:
> Uncaught SyntaxError: Unexpected identifier
<br>

desse modo, utilizariamos o ponto e vírgula, para que o erro seja previnindo pois separaria as intruções em JavaScript, delimitando a separação dos códigos fazendo com que o JavaScript consiga interpretar de forma concreta. Com isso em mente, é nítido o motivo de quase (se não todos) os programadores experientes em JavaScript recomendarem o uso de ponto e vírgula. 

a forma correta do exemplo mostrado seria:

~~~javascript
console.log('teste');
console.log('testando');
~~~

<br>

# variáveis
o programa se lembra das coisas que produzimos, expressões, declarações... Quando produzimos valores novos sem necessariamente apagar os antigos pois o JavaScript fornece uma coisa chamada `variável`.

~~~javascript
var minhaVariavel = 12 * 3;
~~~

a variável _representada pela palavra especial `var`_, é o indicativo que uma variável vai ser criada, que é seguida pelo nome da variável e se quisérmos imediatamente declararmos o valor dessa variável podemos definir após o operador `=` e uma expressão.

~~~javascript
var nomeVariavelCriada = expressão;
var idadeAluno = 19;
~~~

após a variável ser definida, ela pode ser chamada pelo seu nome

~~~javascript
var notaPrimeiraProva = 9;
console.log(notaPrimeiraProva + notaPrimeiraProva)
~~~
vai ser retornado o valor `18`, pois na segunda linha fizemos a adição da variável `notaDaPrimeiraProva` + `notaDaPrimeiraProva`. Isso acontece pois o valor que essa variável guarda é _9_, logo, 9 + 9 = 18. É importante ressaltar que não existiu nenhuma modificação no valor dessa variável.

os nomes das variáveis possuem algumas regras, entre elas:
- não pode ser utilizado palavras reservadas (como `var`)
- não pode conter espaços
- dígitos numéricos podem ser incluídos (como `alunoNota10`), mas a variável não pode ser iniciada com um número, (como `30Anos`)
- o nome de uma variável não pode incluir pontuação, exceto pelos caracteres (como `$ e _`)

é importante ressaltar que o nome _variável_ faz jus a sua utilidade. As variáveis podem alterar os seus valores a qualquer momento utilizando o operador `=`, que pode ser utilizado qualquer hora em variáveis existentes para poder desconectar o valor antigo e colocar um atual

~~~javascript
var luzes = "ligada"

luzes = "desligado"
~~~

no bloco visto anteriormente, o valor da variável `var luzes` foi definido ainda durante a declaração com a expressão `"ligada"`, entretanto, uma linha a baixo o valor `"ligada"` da variável foi substituído para o valor `"desligado"`. 

<br>

##### a seguir teremos um exemplo do livro Eloquente JavaScript traduzido em português retirados do github - repositório eloquente-javascript. Para ver essas informações [clique aqui](https://github.com/braziljs/eloquente-javascript/blob/master/chapters/02-estrutura-do-programa.md).

---
<br>

> Você deve imaginar variáveis como tentáculos, ao invés de caixas. Elas não contêm valores; elas os agarram - duas variáveis podem referenciar o mesmo valor. Somente os valores que o programa mantém tem o poder de ser acessado por ele. Quando você precisa se lembrar de algo, você aumenta o tentáculo para segurar ou recoloca um de seus tentáculos existentes para fazer isso.
> Quando você define uma variável sem fornecer um valor a ela, o tentáculo fica conceitualmente no ar - ele não tem nada para segurar. Quando você pergunta por um valor em um lugar vazio, você recebe o valor `undefined`.

![polvo](assets/polvoAnalogiaVariavel.jpg)

Um exemplo. Para lembrar da quantidade de dólares que Luigi ainda lhe deve, você cria uma variável. E então quando ele lhe paga 35 dólares, você dá a essa variável um novo valor.

```javascript
var luigisDebt = 140;
luigisDebt = luigisDebt - 35;
console.log(luigisDebt);
// 105
```
---

<br>

# palavras-chave e palavras reservadas
algumas palavras tem significados especiais, um exemplo é a palavra `var`, que é utilizada na declaração de variáveis. São chamadas de _keywords_ (palavras-chave) as palavras que são reservadas exclusivamente para alguma finalidade baseando na estrutura da linguagem. A lista de palavras reservadas é longa mas algumas delas são:
> `break` `catch` `this` `with` `void` `while` `static` `swtich` `try` `typeof` `private` `yield` `instanceof` `let` `const`

é importante ressaltar que não é extremamente importante memorizar as palavras reservadas, pois existem várias e futuramente novas podem vir a surgir. Lembre-se que este pode ser um problema caso algo não funcionar como esperado.

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
