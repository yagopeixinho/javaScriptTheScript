<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> Valores | Yago Peixinho
</div>

---

<br>

> Para que seja possível trabalhar com tais quantidades de bits sem ficar perdido, você popde separá-los em partes que representam pedaços de informações. No ambiente JavaScript essas partes são chamadas de _valores_.

<br>

# Valores em JavaScript
- [Números](#operadores-em-javascript)
- [Strings](#strings)
- [Booleanos](#valores-booleanos)


Existem seis tipos básicos de valores no JavaScript: _números, Strings, Booleanos, objetos, funções e valores indefinidos_. Quando você desejar criar um valor você só precisa invocar o nome do seu valor; É claro que não são criados do nada, todo valor precisa estar armazenado em algum lugar e se você quiser utilizar uma quantidade enorme dele pode acabar ficando sem bits. Porém é importante ressaltar que a medida em que você não utiliza um valor ele será dissipado, fazendo com que seus bits sejam reciclados e disponibilziando-os para serem usados nas contruções de outros valores.

<br>

# Números

Os valores de tipo _número_ em um programa são escritos assim:

```javascript
13;
```

Colocar esse valor em um programa fará com que os padrões de bits referente ao número 13 sejam criados e passem a existir na memória do computador.

## Números fracionais

Números fracionais são escritos utilizando um ponto

```javascript
2.81;
```

Para números muitos grandes ou pequenos você pode utilziar a notação científica adicionando um "e" (de "expoente") seguido do valor do expoente:

```javascript
2.9998e8;
```

## Números especiais

No JavaScript podemos encontrar três valores especiais que são considerados números mas não se comportam como números normais.

`Infinity` e `-Infinity`, que são valores utilizados para representar os infinitos positivos e negativos, sendo que o cálculo `Infinity - 1` continua sendo `Infinity`, assim como quaisquer variação dessa conta. Portanto, é necessário salientar que não é válido confiarmos em cálculos baseados no valor inifito, pois esse valor não é sólido matematicamente falando e rapidamente nos levará a um número especial: `NaN`.

`NaN` é a abreviação de _"not a number"_, mesmo sendo um valor do tipo número, esse valor é recebido como resultado quando, por exemplo, tentar calcular `0/0` ou `Infinity - Infinity` ou então realizar quaisquer outras operações numéricas que não resultem em um número preciso e significativo.

<br>

# Strings
As Strings são utilizadas para representar textos seu conteúdo é declarado utilizando aspas simples ou duplas, o seu conteúdo vai entre elas; é importante ressaltar que a aspa inicial e final devem ser idênticas, portanto se você iniciou uma string com (`"`), o final da sua `String` deve conter (`"`) também. 

~~~javascript
"Olá, eu sou uma string, prazer em conhecer você!"
'Eu também sou uma string, porém com aspas simples'
~~~

### Newlines
No JavaScript uma grande parte dos valores podem ser colocados entre aspas de modo em que o JavaScript transformará esse elemento um valor do tipo `String`. Desse modo, imagine que queremos colocar aspas dentro de aspas? De qualquer modo, os caracteres _newlines_ (quebra de linhas quando pressionamos a tecla _Enter_) também não pode ser utilizada dentro de uma `String`.
> As Strings devem permanecer em linha única!

Para que seja possível quebrar a linha de uma string, eis a notação utilizada: 

Toda vez que um caractere de barra invertida `\` for encontrada dentro de uma `String` indica que o caractere seguinte possui uma indicação especial chamada __escapar o caractere__ - uma aspa que se encontra logo após uma barra invertida não indica a finalização da `String` mas que faz parte do texto. O caractere `n` após uma barra invertida é considerado uma quebra de linha e o `t` é considerado um caractere de tabulação: `"você está lendo a primeira linha\nE agora você está lendo a segunda linha"`.

<br>


# Valores Booleanos
Na programação, frequentemente precisamos utilizar um valor que possa nos ajudar a distinguir entre duas possibilidades.

## Comparações
eEssa é uma maneira de produzir valores booleanos:

~~~javascript
console.log(3 > 2)
// -> true

console.log(3 < 2)
// -> false
~~~

Geralmente os valores de comparações resultam em algum resultado `true` ou `false`.

No JavaScript existe apenas um valor que não é igual a ele mesmo, que é o valor NaN, que significa "not a number", que em português significa "não é um número".

~~~javascript
console.log(NaN == NaN)
~~~

`NaN` é utilizado como retorno indicativo de que o resultado de alguma operação que não tenha sentido.

<br>

# Valores indefinidos
No JavaScript é muito comum nos depararmos com os valores `null` e `undefined`. O valor `undefined` é geralmente utilizado quando uma variável não possui nenhum valor, o `null` é utilizado quando queremos intencionalmente definir que existe a ausência de qualquer valor em determinada variável.


<br>
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

#### Referências nesse documento
- https://developer.mozilla.org/pt-BR/
- https://eloquentjavascript.net/

</div>
