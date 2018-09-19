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


* Java
* Python
* C++


Java
```
String name = null;
int number;

java.io.BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
name = in.readLine(); // If the user has not entered anything, assume the default value.
number = Integer.parseInt(in.readLine()); // It reads only String,and we need to parse it.
System.out.println("Name " + name + "\t number " + number);

java.util.Scanner sc = new Scanner(System.in).useDelimiter("\\s");
name = sc.next();  // It will not leave until the user enters data.
number = sc.nextInt(); // We can read specific data.
System.out.println("Name " + name + "\t number " + number);

// The Console class is not working in the IDE as expected.
java.io.Console cnsl = System.console();
if (cnsl != null) {
    // Read a line from the user input. The cursor blinks after the specified input.
    name = cnsl.readLine("Name: ");
    System.out.println("Name entered: " + name);
}
```


Python
```
# TO read string
name = raw_input("What is your name? ") 

# TO read number
age = input("What is your age? ")
print "Your age is: ", age

```


C++
```
#include <iostream>
#include <string>

using namespace std;
int main () {
    int n;
    cin >> n;
    cout << n;
    
    string mystr;
    cout << "What's your name? ";
    getline (cin, mystr);
    cout << "Hello " << mystr << ".\n";
    cout << "What is your favorite team? ";
    getline (cin, mystr);
    cout << "I like " << mystr << " too!\n";
    
    return 0;
}
```


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
* ++: incremento
* --: decremento


Lembre-se que, no fim, a matemática básica vai funcionar, então uma potência pode muito tem ser escreita X * X ao invés de X**2


Uma boa forma de praticar as operações aritméticas é tentar calcular aquelas fórmulas que "nunca" usaremos na vida.

* raizes de: Y = aX² + bX + c
* a² = b² + c²
* IMC = peso / altura²
* Etc



## Exemplos

* Java
* C++
* Python
* Php


### JAVA: código
```java
public class ArithmeticDemo {
    public static void main(String[] args) {

        //a few numbers
        int i = 37;
        int j = 42;
        double x = 27.475;
        double y = 7.22;
        System.out.println("Variable values...");
        System.out.println("    i = " + i);
        System.out.println("    j = " + j);
        System.out.println("    x = " + x);
        System.out.println("    y = " + y);

        //adding numbers
        System.out.println("Adding...");
        System.out.println("    i + j = " + (i + j));
        System.out.println("    x + y = " + (x + y));

        //subtracting numbers
        System.out.println("Subtracting...");
        System.out.println("    i - j = " + (i - j));
        System.out.println("    x - y = " + (x - y));

        //multiplying numbers
        System.out.println("Multiplying...");
        System.out.println("    i * j = " + (i * j));
        System.out.println("    x * y = " + (x * y));

        //dividing numbers
        System.out.println("Dividing...");
        System.out.println("    i / j = " + (i / j));
        System.out.println("    x / y = " + (x / y));

        //computing the remainder resulting from dividing numbers
        System.out.println("Computing the remainder...");
        System.out.println("    i % j = " + (i % j));
        System.out.println("    x % y = " + (x % y));

        //mixing types
        System.out.println("Mixing types...");
        System.out.println("    j + y = " + (j + y));
        System.out.println("    i * x = " + (i * x));
    }
}
```


### Java: saída
```java
Variable values...
    i = 37
    j = 42
    x = 27.475
    y = 7.22
Adding...
    i + j = 79
    x + y = 34.695
Subtracting...
    i - j = -5
    x - y = 20.255
Multiplying...
    i * j = 1554
    x * y = 198.37
Dividing...
    i / j = 0
    x / y = 3.8054
Computing the remainder...
    i % j = 37
    x % y = 5.815
Mixing types...
    j + y = 49.22
    i * x = 1016.58
```


### C++: Código
```cpp
#include <iostream>
int main()
{
  using namespace std;
  float hats, heads;

  cout.setf(ios_base::fixed, ios_base::floatfield); // fixed-point
  cout << "Enter a number: ";
  cin >> hats;
  cout << "Enter another number: ";
  cin >> heads;

  cout << "hats = " << hats << "; heads = " << heads << endl;
  cout << "hats + heads = " << hats + heads << endl;
  cout << "hats - heads = " << hats - heads << endl;
  cout << "hats * heads = " << hats * heads << endl;
  cout << "hats / heads = " << hats / heads << endl;
  return 0;
}
```


### C++: saída
```cpp
Enter a number: 50.25
Enter another number: 11.17
hats = 50.250000; heads = 11.170000
hats + heads = 61.419998
hats - heads = 39.080002
hats * heads = 561.292480
hats / heads = 4.498657
```


### Python:  código
```python
#!/usr/bin/python

a = 21
b = 10
c = 0

c = a + b
print "Line 1 - Value of c is ", c

c = a - b
print "Line 2 - Value of c is ", c 

c = a * b
print "Line 3 - Value of c is ", c 

c = a / b
print "Line 4 - Value of c is ", c 

c = a % b
print "Line 5 - Value of c is ", c

a = 2
b = 3
c = a**b 
print "Line 6 - Value of c is ", c

a = 10
b = 5
c = a//b 
print "Line 7 - Value of c is ", c
```


### Python: saída
```python
Line 1 - Value of c is 31
Line 2 - Value of c is 11
Line 3 - Value of c is 210
Line 4 - Value of c is 2
Line 5 - Value of c is 1
Line 6 - Value of c is 8
Line 7 - Value of c is 2
```


### Php: código
```php
<?php
 $a = 42;
 $b = 20;

 $c = $a + $b;
 echo "Addtion Operation Result: $c <br/>";

 $c = $a - $b;
 echo "Substraction Operation Result: $c <br/>";

 $c = $a * $b;
 echo "Multiplication Operation Result: $c <br/>";

 $c = $a / $b;
 echo "Division Operation Result: $c <br/>";

 $c = $a % $b;
 echo "Modulus Operation Result: $c <br/>";

 $c = $a++; 
 echo "Increment Operation Result: $c <br/>";

 $c = $a--; 
 echo "Decrement Operation Result: $c <br/>";
?>
```


### Php: saída
```php
Addtion Operation Result: 62 
Substraction Operation Result: 22 
Multiplication Operation Result: 840 
Division Operation Result: 2.1 
Modulus Operation Result: 2 
Increment Operation Result: 42 
Decrement Operation Result: 43 
```


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
