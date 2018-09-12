## Conteitos básicos

* Variáveis
* Condicionais
* Laços
* Funções



## Variáveis

> Uma referência para um determinado conteúdo.


O conteúdo dentro de uma variável pode ser diversos, mas primordialmente são:

* Números
* Textos
* Lógico (boolean)


Uma linguagem de programação pode definir as variáveis de forma estática ou dinâmica.

É o que chamamos de linguagem fortemente tipada (estática) ou de tipagem dinâmica.


# Viajando nas analogias


## Tipagem forte (estática)

Imagina que as variáveis são como caixas. Cada caixa tem um temanho diferente e formato diferente. Então podemos imaginar que:

* Números: São caixas quadradas vermelhas, que possuem diferentes tamanhos (dependendo do tipo do número).
* Textos: São caixas redondas azuis (cilindro), que possuem também diferentes.
* Condicionais: Seriam caixas triangulares de cores verde, que possue tamanho único.


O conteúdo só irá caber em uma determinada caixa. Se seu formato for diferente do formato da caixa, o conteúdo não permanece dentro, portanto, ocasionando um erro no programa.

> "Cada um no seu quadrado."


## Tipagem dinâmica

Utilizar tipagem dinâmica é como usar sacolas para guardar coisas. A sacola se molda ao conteúdo dentro dela e a como esse conteúdo está disposto.

Portanto, uma sacola que continha um número dentro, poderá ter agora texto, e a sacola não se limitará ao que irá ser posto dentro dela. Assim, uma sacolá com número, passou a ser uma sacola com texto.


## Números

Precisamos lembrar de algo que um dia achamos que nunca iriamos usar na vida: `Conjunto numéricos`


Basicamente (ou que em "90%+" das vezes usará) existem dois tipos de números:

* Inteiros (ex: -1, -2, -1231231, 0, 31231231, 2, 15)
* Racionais (ex: qualquer coisa com decimal, 1.0, 2.1, 0.13213, -0.123123)



## Exemplos

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
