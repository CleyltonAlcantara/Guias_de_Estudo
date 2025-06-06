# Linguagem C - Guia Completo

### ÍNDICE DE CONTEÚDO

- [Introdução sobre a linguagem C](#introdução-sobre-a-linguagem-c)
- [Variáveis](#variáveis)
- [Tipos de dados](#variáveis)
- [Operadores](#operadores)
  - [Operadores aritméticos](#operadores-aritméticos)
  -  [Operadores relacionais](#operadores-relacionais)
  - [peradores lógicos](#operadores-lógicos)
  - [Operadores bit-a-bit]()
  - [Operadores especiais]()
    - [sizeof()]()
    - [Endereço (&) e ponteiro(*)]()
    - [Operador Ternário]()
- [Estruturas de controle de fluxo]()
  - [if, if-else]()
  - [switch]()
  - [for]()
  - [while]()
  - [do-while]()
- [Funções]()
- [Vetores e matrizes]()
- [Ponteiros]()
- [Structs]()
- [Strings]()
- [Constantes]()
- [Modificadores de tipo]()
- [Modificadores de Armazenamento]()
- [Diretivas de pré-compilação]()
- [Compilador GCC]()
  - [Compilando um código em linguagem C com o GCC]()
- [Criando bibliotecas em linguagem C]()
- [Baixe o e-book Domine a Linguagem C]()
- [Saiba Mais sobre a linguagem C]()

<br><br>

# Introdução sobre a linguagem C
A linguagem C é uma linguagem de programação de alto nível que foi criada nos anos 1970 para desenvolvimento de sistemas operacionais. Ela é amplamente utilizada em sistemas embarcados.

A seguir é apresentado um resumo das principais estruturas da linguagem C. Serão apresentados as Estruturas Básicas, Tipos de Dados, Operadores, Estruturas de Controle de Fluxo, Funções, Vetores e Matrizes, Ponteiros e Structs.

<br><br>

# Variáveis
As variáveis são locais de armazenamento em memória onde os dados podem ser armazenados e manipulados durante a execução de um programa.

Aqui está um exemplo de como declarar e atribuir um valor a uma variável em C:

```c

#include <stdio.h>
 
int main(void) {
  // Declara uma variável inteira chamada "idade"
  int idade;
 
  // Atribui o valor 25 à variável "idade"
  idade = 25;
 
  printf("Minha idade é: %d\n", idade);
 
  return 0;
}
```
Neste exemplo, a variável “idade” é declarada como um inteiro. Ela é então atribuída o valor 25 através da atribuição de valor “idade = 25”. O valor da variável “idade” é então exibido na tela através da função printf().

O resultado da execução deste programa seria: “Minha idade é: 25”.

<br><br>

# Tipos de dados 
A linguagem C possui vários tipos de dados, como inteiros, ponto flutuante, caracteres e booleanos.

Veja como usar diferentes tipos de dados em C:

```c
#include <stdio.h>
 
int main(void) {
  // Declara uma variável inteira chamada "idade" e atribui o valor 25
  int idade = 25;
 
  // Declara uma variável de ponto flutuante chamada "altura" e atribui o valor 1.80
  float altura = 1.80;
 
  // Declara uma variável de caractere chamada "sexo" e atribui o valor 'M'
  char sexo = 'M';
 
  // Declara uma variável booleana chamada "casado" e atribui o valor verdadeiro
  _Bool casado = 1;
 
  printf("Idade: %d\nAltura: %f\nSexo: %c\nCasado: %d\n", idade, altura, sexo, casado);
 
  return 0;
}
```
Neste exemplo, são declaradas quatro variáveis de diferentes tipos: inteiro, ponto flutuante, caractere e booleano. Cada uma delas é atribuída um valor apropriado e, em seguida, é exibida na tela através da função printf().

O resultado da execução deste programa:

![image](https://github.com/user-attachments/assets/3ca215c2-1053-4e62-9a7a-2e8a789aa11f)

<br><br>

# Operadores 
Os operadores são símbolos especiais utilizados para realizar operações matemáticas e lógicas. 

## Operadores aritméticos
Os operadores aritméticos são usados para realizar operações matemáticas básicas em C, como adição, subtração, multiplicação e divisão. 

| Operador | Operação |
| -------- | -------- |
| +	| soma |
| – |	subtração |
| *	| multiplicação |
| /	| divisão inteira |
| %	| módulo |
| ++	| incremento |
| —	| decremento |

```c
#include <stdio.h>

int main(void) {
int a = 5, b = 3;

int soma = a + b;
printf("soma de %d e %d é %d\n", a, b, soma);

int subtracao = a - b;
printf("subtracao de %d e %d é %d\n", a, b, subtracao);

int mult = a * b;
printf("multiplicação de %d e %d é %d\n", a, b, mult);

int divisao = a / b;
printf("divisao de %d e %d é %d\n", a, b, divisao);

int mod = a % b;
printf("resto da divisão de %d e %d é %d\n", a, b, mod);
   
a++;
printf("incremento: %d\n", a);
   
b--;
printf("decremento: %d\n", b);

return 0;
}
```

Resultado:

![image](https://github.com/user-attachments/assets/fd5687cc-8c4e-447d-9f36-560ac156896e)

<br>

## Operadores relacionais
Os operadores relacionais são usados para comparar dois valores em C e produzir um valor lógico (verdadeiro(1) ou falso(0)) como resultado.

| Operador |	Operação |
| -------- | --------- |
| == |	igual |
| != |	diferente |
| >	| maior do que |
| <	| menor do que |
| >=	| maior ou igual |
| <=	| menor ou igual |

Exemplo:

```c
#include <stdio.h>

int main(void) {
int a = 5, b = 3;
//Igualdade
int resultado = (a == b);
printf("%d == %d é %d\n", a, b, resultado);
//Diferença
resultado = (a != b);
printf("%d != %d é %d\n", a, b, resultado);
//Maior
resultado = (a > b);
printf("%d > %d é %d\n", a, b, resultado);
//Menor
resultado = (a < b);
printf("%d < %d é %d\n", a, b, resultado);
//Maior ou igual
resultado = (a >= b);
printf("%d >= %d é %d\n", a, b, resultado);
//Menor ou Igual
resultado = (a <= b);
printf("%d <= %d é %d\n", a, b, resultado);

return 0;
}
```
Resultado: 

![image](https://github.com/user-attachments/assets/efef4eab-8f58-46c9-8dbd-3d30f69f17a2)

<br><br>

## Operadores lógicos

Os operadores lógicos são usados para combinar expressões booleanas em C e produzir um valor lógico (verdadeiro ou falso) como resultado. 

| Operador	| Operação |
| --------- | -------- |
| &&	| AND  (E) |
| \|\|	| OR (OU) |
| !	| NOT (NÃO) |

Exemplo:

```c
#include <stdio.h>

int main(void) {
int a = 1, b = 1;

//AND (E)
int resultado = (a && b);
printf("%d && %d é %d\n", a, b, resultado);
//OR (OU)
resultado = (a || b);
printf("%d || %d é %d\n", a, b, resultado);
//NOT (NÃO)
resultado = !a;
printf("!%d é %d\n", a, resultado);
//Combinação de operadores lógicos
resultado = (a && b) || !a;
printf("(%d && %d) || !%d é %d\n", a, b, a, resultado);

return 0;
}
```

Resultado:

![image](https://github.com/user-attachments/assets/c639c30b-6013-482f-8fe7-ad1b2d97ffc6)

<br><br>

## Operadores bit-a-bit
Os operadores bit-a-bit são usados para realizar operações bit-a-bit em C. Eles são úteis quando você precisa trabalhar com números binários diretamente. 

| Operador |	Operação |
| -------- | --------- |
| &	| AND (E) |
| \|	| OR (OU) |
| ^	| XOR (OU-EXCLUSIVO0 |
| ~	| NOT (NÃO) |
| <<	| deslocamento de bits à esquerda |
| >>	| deslocamento de bits à direita |

Exemplo:

```c
#include <stdio.h>

int main(void) {
int a = 5, b = 3;

//AND
int resultado = (a & b);
printf("%d & %d é %d\n", a, b, resultado);
//OR
resultado = (a | b);
printf("%d | %d é %d\n", a, b, resultado);
//XOR
resultado = (a ^ b);
printf("%d ^ %d é %d\n", a, b, resultado);
//NOT
resultado = (~a);
printf("~%d é %d\n", a, resultado);
//deslocamento de bits à esquerda
resultado = (a << 1);
printf("%d << 1 é %d\n", a, resultado);
//deslocamento de bits à direita
resultado = (a >> 1);
printf("%d >> 1 é %d\n", a, resultado);

return 0;
}
```

Resultado:

![image](https://github.com/user-attachments/assets/71ed7a4c-a20e-48e2-9396-d6452fb3c026)

<br><br>

## Operadores especiais

### sizeof()

O operador sizeof() é usado para descobrir o tamanho, em bytes, de uma variável ou tipo de dados em C. Ele é útil para determinar o espaço de armazenamento necessário para uma determinada variável ou estrutura. 















