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

~~~javascript
var calcular = function(numero){
    return numero + numero;
}

console.log(calculo(12));
~~~

No exemplo anterior, declaramos a variável `calcular` e atribuímos o valor dessa variável o bloco da função — essa função possui o `return`, que retorna o valor do processamento. No caso do exemplo, o processamento foi o `numero` + `numero` como está escrito dentro do bloco da função. Abaixo, chamamos a função com o `console.log(calculo(12))`. O valor `12` é o valor do número que foi declarado na chamada da função e o cálculo será efetuado com esse valor.

É importante ressaltar que nem todas as funções retornam um valor, como demonstrado no exemplo acima. 

~~~javascript
var fazerBarulho = function(){
    console.log("AAAAAAAAAAAAAA");
}
fazerBarulho();
~~~

No exemplo anterior, temos o exemplo de uma função que não retorna um valor. Essa função `fazerBarulho` é chamada e o único processamento que ela faz é o `console.log("AAAAAAAAAAAAAA")`. 

Todo os processamento em funções são determinado entre chaves `{}`.

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
