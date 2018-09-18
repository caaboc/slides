## Conteitos básicos

* Lendo e escrevendo
* Variáveis
* Operações
* Condicionais
* Laços
* Funções



## Lendo e escrevendo

Podemos dizer que o conceito mais básico em uma linguagem é a comunicação.
La lingua falada, o saber ouvir e falar, na linguagem de programação, o saber ler e escrever.


Apesar de que, a interação humana nem sempre seja necessária para a leitura e a escrita em um código, todo código tende a receber uma entrada e devolver algum tipo de saída.


A exemplo, em uma `página web`, um formulário poderá servir de entrada para o `sistema web`, gerando um usuário cadastrado como saída a `página web` e também poderá gerar uma entrada de dados para o `banco de dados`, que servirá de entrada que armazerá as informações.


A forma mais simples de se mandar uma entrada à um código é através das funções de *"ouvir"* que as linguagens têm. Assim como para a escrita.


**SPOILLER ALERT!!**


Imagina você conversando consigo. O programa também é capaz disso, quando enviamos dados entre as funções/métodos, e esperamos que ele rertorne algo e assim seguir o fluxo.

Pode acontecer também de *"ficar no vácuo"*, tipo quando usamos funções **void** (que retornam nada). Mas, isso são cenas de espisódios posteriores.



## Exemplos




## Variáveis

> Uma referência para um determinado conteúdo.


O conteúdo dentro de uma variável pode ser diversos, mas primordialmente são:

* Números
* Textos
* Lógico (boolean)


Uma linguagem de programação pode definir as variáveis de forma estática ou dinâmica.

É o que chamamos de linguagem fortemente tipada (estática) ou de tipagem dinâmica.


# Brincando nas analogias


## Tipagem forte (estática)

Imagina que as variáveis são como caixas. Cada caixa tem um temanho diferente e formato diferente, tipo aqueles jogos de encaixar peças geométricas.

<img src="http://www.mabelilivros.com/meusarquivos/312.jpg" />


Então caixa caixa possui um espaço que só é possível colocar pessas do mesmo formato. Assim, por exemplo:

* Números: São caixas quadradas vermelhas, que possuem diferentes tamanhos (dependendo do tipo do número).
* Textos: São caixas redondas azuis (cilindro), que possuem também diferentes.
* Condicionais: Seriam caixas triangulares de cores verde, que possue tamanho único.


O conteúdo só irá caber em uma determinada caixa. Se seu formato for diferente do formato da caixa, o conteúdo não permanece dentro, portanto, ocasionando um erro no programa.

> "Cada um no seu quadrado."


## Tipagem dinâmica

Utilizar tipagem dinâmica é como usar sacolas para guardar coisas. A sacola se molda ao conteúdo dentro dela e a como esse conteúdo está disposto.

<img src="https://mamaplasticos.com.br/wp-content/uploads/2018/08/sacola-al%C3%A7a-camiseta-colorida.png" />


Portanto, uma sacola que continha um número dentro, poderá ter agora texto, uma função, um objeto, uma classe. A sacola não faz distinção do que entra dentro dela. Ela é reciclável, podendo durar a execução inteira mudando o conteúdo interno.



## Números

Precisamos lembrar de algo que um dia achamos que nunca iriamos usar na vida: `Conjunto numéricos`


Basicamente (ou que em "90%+" das vezes usará) existem dois tipos de números:

* Inteiros (ex: -1, -2, -1231231, 0, 31231231, 2, 15)
* Racionais (ex: qualquer coisa com casa decimal, 1.0, 2.1, 0.13213, -0.123123)



## Textos

Variáveis que contém textos, são textos mesmo...

A grande diferença vai ocorrer em linguagens fortemente tipadas (Ex: Java, C++, etc) que vai existir um tipo primitivo `character ou char` e uma lista de caracteres chamadas `Strings`.

Em linguagens dinâmicas não há (necessariamente) essa disntinção explicita.



## Lógicos

As variáveis lógicas guardam valores binários, `true` ou `false`, podendo haver outros tipos de valores que podem corresponder a um desses dois.

Particularmente, utilizo bastante essas variáveis para simplificar operações lógicas (o que também poderia ser feito com funções/métodos), tornando o código mais legívele entendível.



## Exemplos de utilização

* Java
* C++
* Php
* Javascript
* Python


Java

```java
public static void main (String[] args) {
    boolean condicional = true;

    char letra = "a";
    String texto = 'textao';
    
    byte inteiroMiudin =  10; // pode ser entre -128 e 127
    short inteirinho = -1; // pode ser entre -32.768 e 32.767
    int inteiro = 312312; // pode ser entre -2.147.483.648 e 2.147.483.647.
    long inteirozao = 132.1231321; // pode ser entre -9.223.372.036.854.775.808L e 9.223.372.036.854.775.807L.

    float racional = 1.31231321;
    double racionalGrandao = 4816417289.41823746128349102341;
}
```


C++

```cpp
int main () {
    bool condicional = true;
    char letra = "a";

    short inteirinho = -1; // pode ser entre -32.768 e 32.767 +-
    int inteiro = 312312; // pode ser entre -2.147.483.648 e 2.147.483.647.
    long inteirozao = 132.1231321; // pode ser entre -2.147.483.648 até 2.147.483.647 uma forma explicita de dizer

    unsigned short inteirinho_maior_que_zero = -1; // pode ser entre -32.768 e 32.767 +-
    unsigned int inteiro_maior_que_zero = 312312; // pode ser entre -2.147.483.648 e 2.147.483.647.
    unsigned long inteirozao_maior_que_zero = 132.1231321; // pode ser entre -2.147.483.648 até 2.147.483.647 uma forma explicita de dizer

    float racional = 1.31231321;
    double racional_grandao = 4816417289.41823746128349102341;

} 

```


PHP

```php
<?php
$sacola = TRUE;     // a boolean
$sacola  = "foo";   // a string
$sacola = 'foo';    // a string
$sacola = 12;       // an integer
$sacola = 1.0;      // an float
```


Javascript

```javascript
let sacola
sacola = 10         // inteiro
sacola = 10.2       // float (racional, ponto flutuante)
sacola = 'texto'    // texto (string)
sacola = 't'        // texto (string/letra)
sacola = false      // lógico (boolean)
```


Python

```python
sacola = 10         // inteiro
sacola = 10.2       // float (racional, ponto flutuante)
sacola = 4+3j       // complex (racional, ponto flutuante)
sacola = 'texto'    // texto (string)
sacola = 't'        // texto (string/letra)
sacola = False      // lógico (boolean)

```



## Operações

* Aritméticas
* Lógicas



## Aritiméticas

Da boa e velha matemática do primário, as 4 operações básicas que serão encontradas em praticamente todas (se não todas) as linguagens:

* +: somar
* -: subtrair
* *: multiplicar
* /: dividir


Existem outras operações, como potência, resto da divisão, raiz quadrada etc, mas cada linguagem tem sua forma de representar. Sendo as mais comuns:

* **: para potências
* %: para resto de divizão
* sqrt(): função que retorna a raíz de um número


Lembre-se que, no fim, a matemática básica vai funcionar, então uma potência pode muito tem ser escreita X * X ao invés de X**2


Uma boa forma de praticar as operações aritméticas é tentar calcular aquelas fórmulas que "nunca" usaremos na vida.

> raizes de: Y = aX² + bX + c
> a² = b² + c²
> IMC = peso / altura²
> Etc



## Exemplos

... a ser feito D:



## Condicionais

> *"Ser ou não ser, eis a questão..."*


Os condicionais e suas operações são responsáveis pelo tratamento dos dados e ou do fluxo do sistema.


### Os tipos de operadores

Mais comuns da matemática:
** >, >= (maior ou igual que), <, <= (menor ou igual que) **

Adicionais:
** && (E/AND), || (OU/OR) **


<table>
    <thead>
        <th>Operações</th>
        <th>Resultado</th>
    </thead>
    <tbody>
        <tr><td> true && true </td><td> true </td></tr>
        <tr><td> true && false </td><td> false </td></tr>
        <tr><td> false && true </td><td> false </td></tr>
        <tr><td> false && false </td><td> false </td></tr>
        <tr><td> true || true </td><td> true </td></tr>
        <tr><td> true || false </td><td> true </td></tr>
        <tr><td> false || true </td><td> true </td></tr>
        <tr><td> false || false </td><td> false </td></tr>
    </tbody>
</table>
