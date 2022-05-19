<div class="header">
    <img align="center" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/640px-Unofficial_JavaScript_logo_2.svg.png" width="100"/> JavaScript Script | Estrutura de dados
</div>

---

<br>

>

<br>

# ESTRUTURA DE DADOS

- [Objetos](#objetos)

Cada linguagem de programação possui uma estrutura de dados. As estruturas de dados é necessária para que diversos tipos de processamentos, organizações e fluxos de informações possa ser criado, armazenado e manipulado pelo programa.

<br>
<br>

# OBJETOS

Os objetos _object literal syntax_ é um conjunto de propriedade envolvido por chaves `{}` que armazenam propriedades que podem ser adicionadas ou removidas. Essas propriedades podem assumir qualquer tipo de valores, desde outros objetos, até arrays, nos permitindo a construção de uma estrutura de dados mais complexa, a seguir temos um objeto literal criado para armazenar as informações de um usuário:

```javascript
var bairroUsuario = "São Bernado";

var usuario1 = {
  nome: "Carlos Alberto",
  quantidadeFilhos: 4,
  corDosOlhos: corDosOlhos,
};
```

No bloco de código anterior, criamos um _objeto_ e o atribuímos na variável `usuario1`. As propriedades desse _objeto_ são respectivamente: `nome, quantidadeFilhos, corDosOlhos`. É perceptível que na propriedade `nome` atribuímos a _String_ `Carlos Alberto` com a expressão `nome: "Carlos Alberto`. A seguir atribuímos a propriedade `quantidadeFilhos` com valor do tipo _Number_ `4` e a cor dos olhos atribuímos a variável `corDosOlhos` contendo o valor `"Verde"` que foi previamente declarada.

Uma coisa interessante é que declaramos uma variável como valor na propriedade de um _objeto_. Mais interessante ainda é que podemos além disso, declarar _Arrays_, _Funções_ e _Objetos_.

Ainda utilizando o exemplo anterior, vamos acrescentar mais algumas propriedades...

```javascript
var corDosOlhos = "Verde";
var anoAtual = 2022;
var anoNascimento = 1976;

var diasDeTrabalho = ["Seg", "Ter", "Quar", "Qui"];

var endereco = {
    numero: "2841",
    bairro: "Limoeiro",
    logradouro: "Avenida Bernado",
    cep: "52242-110",
    complemento: "Apartamento 420 do bloco A"
};

function idadeUsuario(anoNascimento, anoAtual) {
  return anoAtual - anoNascimento;
};

var usuario1 = {
  nome: "Carlos Alberto",
  filhos: 4,
  corDosOlhos: corDosOlhos,
  idadeUsuario: idadeUsuario(anoNascimento, anoAtual),
  diasDeTrabalho: diasDeTrabalho, 
  endereco: endereco 
};
```

Agora deixamos o nosso objeto mais complexo e completo, pois declaramos devido a criação de um objeto atribuido a variável `endereco`, um _Array_, que foi atribuido a variável `diasDeTrabalho` e a `idadeUsuario`, que recebe uma função. Existem várias formas de trazer valores para propriedades de _objetos_ de forma mais organizada, como as utilizadas anteriormente como _Arrays_, _Funções_ e _Objetos_.

O estado final do objeto ficou: 

~~~javascript
console.log(usuario1);

{
  nome: 'Carlos Alberto',
  filhos: 4,
  corDosOlhos: 'Verde',
  idadeUsuario: 46,
  diasDeTrabalho: [ 'Seg', 'Ter', 'Quar', 'Qui' ],
  endereco: {
    numero: '2841',
    bairro: 'Limoeiro',
    logradouro: 'Avenida Bernado',
    cep: '52242-110',
    complemento: 'Apartamento 420 do bloco A'
  }
} 
~~~

É perceptível também que utilizamos a vírgula "`,`" para separamos as propriedades, sendo a vírgula da última propriedade opcional:

```javascript
var endereco = {
  numero: "2841",
  bairro: "Limoeiro",
  logradouro: "Avenida Bernado",
  cep: "52242-110",
  complemento: "Apartamento 420 do bloco A",
};

var telefone = {
  numero: "9999-9999",
  ddi: "55",
  ddd: "83",
  tipo: "Celular"
};
```

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
