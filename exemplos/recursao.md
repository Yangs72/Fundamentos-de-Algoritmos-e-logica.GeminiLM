# Recursão

## Objetivo

Compreender o conceito de recursão, seu funcionamento, vantagens, limitações e aplicações na programação.

---

## O que é?

Recursão é uma técnica de programação em que uma função chama a si mesma para resolver um problema.

A ideia é dividir um problema maior em problemas menores e semelhantes, repetindo esse processo até chegar a um caso que possa ser resolvido diretamente.

---

## Como funciona?

Uma função recursiva segue duas partes fundamentais:

1. **Caso Base:** condição que encerra a recursão e impede chamadas infinitas.
2. **Chamada Recursiva:** a função chama a si mesma utilizando um problema menor, aproximando-se do caso base.

Durante a execução, cada chamada é armazenada na **pilha de chamadas (Call Stack)** do programa. Quando o caso base é alcançado, as chamadas são resolvidas na ordem inversa até retornar ao ponto inicial.

---

## Requisitos

Para que uma função recursiva funcione corretamente, ela deve possuir:

- Um caso base bem definido.
- Uma chamada recursiva que aproxime o problema do caso base.

Sem esses dois elementos, o programa pode entrar em recursão infinita e provocar um erro de estouro de pilha (*Stack Overflow*).

---

## Complexidade

A complexidade de algoritmos recursivos depende da quantidade de chamadas realizadas.

Em muitos casos, ela é descrita por **equações de recorrência**.

Exemplo:

- Merge Sort → **Θ(n log n)**

---

## Vantagens

- Código mais organizado e elegante.
- Facilita a resolução de problemas recursivos.
- Muito utilizada em algoritmos do tipo **Dividir e Conquistar**.

---

## Limitações

- Pode consumir mais memória devido à pilha de chamadas.
- Em alguns casos, é menos eficiente do que soluções iterativas.
- Se mal implementada, pode causar recursão infinita.

---

## Exemplo intuitivo

Imagine uma pilha de caixas.

Para pegar a caixa que está no fundo, primeiro é necessário retirar uma caixa de cada vez.

Depois de alcançar o objetivo, as caixas são recolocadas na ordem inversa.

Esse comportamento é semelhante ao funcionamento da pilha de chamadas utilizada pela recursão.

---

## Exemplo em Python

```python
def fatorial(n):
    if n == 1:
        return 1
    return n * fatorial(n - 1)
```

---

## Aplicações

- Cálculo de fatoriais.
- Sequência de Fibonacci.
- Merge Sort.
- Quick Sort.
- Percurso de árvores.
- Busca em grafos.

---

## O que aprendi

A recursão é uma técnica poderosa para resolver problemas que podem ser divididos em partes menores. Seu correto funcionamento depende da definição de um caso base e de chamadas recursivas que reduzam gradualmente o problema até sua solução.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
