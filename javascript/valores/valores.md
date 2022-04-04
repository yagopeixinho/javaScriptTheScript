<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> valores | peixinho yago 
</div>

---

<br>

> para que seja possível trabalhar com tais quantidades de bits sem ficar perdido, você popde separá-los em partes que representam pedaços de informações. No ambiente JavaScript essas partes são chamadas de _valores_.

<br>

# valores em JavaScript

Existem seis tipos básicos de valores no JavaScript: _números, Strings, Booleanos, objetos, funções e valores indefinidos_. Quando você desejar criar um valor você só precisa invocar o nome do seu valor; É claro que não são criados do nada, todo valor precisa estar armazenado em algum lugar e se você quiser utilizar uma quantidade enorme dele pode acabar ficando sem bits. Porém é importante ressaltar que a medida em que você não utiliza um valor ele será dissipado, fazendo com que seus bits sejam reciclados e disponibilziando-os para serem usados nas contruções de outros valores.

# números

os valores de tipo _número_ em um programa são escritos assim:

```javascript
13;
```

colocar esse valor em um programa fará com que os padrões de bits referente ao número 13 sejam criados e passem a existir na memória do computador.

## números fracionais

números fracionais são escritos utilizando um ponto

```javascript
2.81;
```

para números muitos grandes ou pequenos você pode utilziar a notação científica adicionando um "e" (de "expoente") seguido do valor do expoente:

```javascript
2.9998e8;
```

# números especiais

no JavaScript podemos encontrar três valores especiais que são considerados números mas não se comportam como números normais.

`Infinity` e `-Infinity`, que são valores utilizados para representar os infinitos positivos e negativos, sendo que o cálculo `Infinity - 1` continua sendo `Infinity`, assim como quaisquer variação dessa conta. Portanto, é necessário salientar que não é válido confiarmos em cálculos baseados no valor inifito, pois esse valor não é sólido matematicamente falando e rapidamente nos levará a um número especial: `NaN`.

`NaN` é a abreviação de _"not a number"_, mesmo sendo um valor do tipo número, esse valor é recebido como resultado quando, por exemplo, tentar calcular `0/0` ou `Infinity - Infinity` ou então realizar quaisquer outras operações numéricas que não resultem em um número preciso e significativo.

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
