# Busca Binária

## Objetivo

Entender como funciona a Busca Binária, seus requisitos, vantagens, limitações e aplicações práticas.

---

## O que é a Busca Binária?

A Busca Binária é um algoritmo utilizado para localizar um elemento em uma coleção de dados **ordenada**.

Seu princípio é simples: em vez de percorrer todos os elementos da lista, o algoritmo analisa o elemento central e descarta metade dos dados a cada comparação. Essa estratégia reduz significativamente a quantidade de verificações necessárias.

---

## Como funciona

O algoritmo segue os seguintes passos:

1. Seleciona o elemento localizado no meio da lista.
2. Compara esse elemento com o valor procurado.
3. Se forem iguais, a busca é encerrada.
4. Se o valor procurado for menor, continua apenas na metade esquerda.
5. Se for maior, continua apenas na metade direita.
6. O processo é repetido até encontrar o elemento ou concluir que ele não está presente.

Essa técnica é conhecida como **Dividir para Conquistar (Divide and Conquer)**.

---

## Requisitos

Para que a Busca Binária funcione corretamente, os dados precisam estar **ordenados**.

Caso contrário, o algoritmo poderá descartar a metade errada da lista e produzir resultados incorretos.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(1)** |
| Caso médio | **O(log n)** |
| Pior caso | **O(log n)** |

A complexidade logarítmica faz com que o número de comparações cresça muito lentamente, mesmo quando a quantidade de dados aumenta.

---

## Vantagens

- Excelente desempenho em listas grandes.
- Poucas comparações para localizar um elemento.
- Algoritmo simples e eficiente quando os dados já estão ordenados.

---

## Limitações

- Só funciona corretamente com dados ordenados.
- Se a coleção sofre muitas inserções e remoções, manter a ordenação pode gerar um custo adicional.
- Para listas pequenas, o ganho de desempenho pode ser pouco significativo.

---

## Exemplo intuitivo

Imagine que você precisa adivinhar um número entre **1 e 100**.

Na busca linear você começaria por 1, depois 2, depois 3...

Na Busca Binária, o primeiro palpite seria **50**.

Se o número procurado for menor, todas as opções acima de 50 são descartadas.

Se for maior, todas as opções abaixo de 50 deixam de ser consideradas.

A cada tentativa, metade das possibilidades é eliminada.

---

## Exemplo em Python

```python
def busca_binaria(lista, alvo):
    esquerda = 0
    direita = len(lista) - 1

    while esquerda <= direita:
        meio = (esquerda + direita) // 2

        if lista[meio] == alvo:
            return meio

        if lista[meio] < alvo:
            esquerda = meio + 1
        else:
            direita = meio - 1

    return -1
```

---

## Aplicações

A Busca Binária é utilizada em diversos contextos, como:

- Pesquisa em listas ordenadas.
- Bancos de dados.
- Sistemas de busca.
- Bibliotecas de programação.
- Algoritmos de otimização.

---

## O que aprendi

A Busca Binária demonstra como a escolha do algoritmo influencia diretamente o desempenho de um programa.

Ao eliminar metade dos elementos a cada comparação, ela consegue localizar informações de forma muito mais eficiente do que uma busca sequencial, desde que os dados estejam ordenados.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
