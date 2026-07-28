# Bubble Sort

## Objetivo

Compreender o funcionamento do Bubble Sort, sua complexidade, vantagens, limitações e aplicações.

---

## O que é?

O Bubble Sort é um algoritmo de ordenação simples e um dos mais utilizados para fins didáticos.

Seu funcionamento consiste em comparar elementos vizinhos e trocá-los de posição quando estão na ordem incorreta. Após cada passagem pela lista, o maior elemento "flutua" para sua posição correta no final da sequência.

---

## Como funciona?

O algoritmo executa os seguintes passos:

1. Percorre a lista comparando pares de elementos adjacentes.
2. Se o elemento da esquerda for maior que o da direita, eles trocam de posição.
3. Ao final da primeira passagem, o maior elemento estará na última posição.
4. O processo é repetido até que toda a lista esteja ordenada.

---

## Requisitos

O Bubble Sort pode ser aplicado em qualquer lista de elementos comparáveis, sem necessidade de ordenação prévia.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(n)** |
| Caso médio | **O(n²)** |
| Pior caso | **O(n²)** |

O melhor caso ocorre quando a lista já está ordenada e a implementação possui uma verificação para detectar que nenhuma troca foi realizada.

---

## Vantagens

- Fácil de compreender.
- Simples de implementar.
- Excelente para fins de aprendizagem.

---

## Limitações

- Baixa eficiência em listas grandes.
- Realiza muitas comparações e trocas.
- Existem algoritmos de ordenação significativamente mais rápidos.

---

## Exemplo intuitivo

Imagine organizar cartas de baralho.

Você compara duas cartas vizinhas por vez. Se estiverem na ordem errada, troca suas posições.

Após percorrer todas as cartas, a maior terá chegado ao final.

Repetindo esse processo diversas vezes, todas as cartas ficam ordenadas.

---

## Exemplo em Python

```python
def bubble_sort(lista):
    n = len(lista)

    for i in range(n):
        trocou = False

        for j in range(0, n - i - 1):
            if lista[j] > lista[j + 1]:
                lista[j], lista[j + 1] = lista[j + 1], lista[j]
                trocou = True

        if not trocou:
            break

    return lista
```

---

## Aplicações

- Ensino de algoritmos.
- Introdução à lógica de programação.
- Pequenas listas de dados.
- Demonstração de técnicas de ordenação.

---

## O que aprendi

O Bubble Sort é um algoritmo simples e intuitivo que facilita o entendimento dos conceitos de ordenação. Apesar de não ser indicado para grandes volumes de dados devido à sua complexidade quadrática, é uma excelente ferramenta para aprender como algoritmos de ordenação funcionam.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
