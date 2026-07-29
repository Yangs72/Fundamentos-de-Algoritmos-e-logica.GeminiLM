# Insertion Sort

## Objetivo

Compreender o funcionamento do Insertion Sort, sua complexidade, vantagens, limitações e aplicações.

---

## O que é?

O Insertion Sort (Ordenação por Inserção) é um algoritmo simples de ordenação que organiza os elementos inserindo cada novo item na posição correta dentro da parte da lista que já está ordenada.

Seu funcionamento é semelhante à forma como muitas pessoas organizam cartas de baralho nas mãos.

---

## Como funciona?

O algoritmo segue os seguintes passos:

1. Considera o primeiro elemento da lista como ordenado.
2. Seleciona o próximo elemento da lista.
3. Compara esse elemento com os anteriores, da direita para a esquerda.
4. Desloca os elementos maiores uma posição para a direita.
5. Insere o elemento na posição correta.
6. Repete o processo até que todos os elementos estejam ordenados.

---

## Requisitos

O Insertion Sort pode ser utilizado em qualquer coleção de elementos comparáveis, sem necessidade de ordenação prévia.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(n)** |
| Caso médio | **O(n²)** |
| Pior caso | **O(n²)** |

O melhor caso ocorre quando a lista já está ordenada. O pior caso acontece quando a lista está em ordem inversa.

---

## Vantagens

- Fácil de compreender e implementar.
- Muito eficiente para listas pequenas.
- Apresenta bom desempenho quando os dados já estão quase ordenados.
- Utiliza pouca memória adicional.

---

## Limitações

- Baixa eficiência para grandes volumes de dados.
- Realiza muitas comparações e deslocamentos no pior caso.
- É superado por algoritmos mais eficientes em listas grandes.

---

## Exemplo intuitivo

Imagine que você está organizando cartas de baralho.

Você mantém as cartas da mão sempre em ordem.

Ao receber uma nova carta, compara-a com as cartas já organizadas e a insere exatamente na posição correta.

O Insertion Sort utiliza essa mesma estratégia para ordenar uma lista.

---

## Exemplo em Python

```python
def insertion_sort(lista):
    for i in range(1, len(lista)):
        chave = lista[i]
        j = i - 1

        while j >= 0 and lista[j] > chave:
            lista[j + 1] = lista[j]
            j -= 1

        lista[j + 1] = chave

    return lista
```

---

## Aplicações

- Ensino de algoritmos.
- Ordenação de listas pequenas.
- Coleções quase ordenadas.
- Componentes internos de algoritmos híbridos.

---

## O que aprendi

O Insertion Sort organiza os elementos inserindo cada novo item na posição correta dentro da parte já ordenada da lista. Apesar de possuir complexidade quadrática no pior caso, é uma excelente opção para listas pequenas ou quase ordenadas devido à sua simplicidade e baixo consumo de memória.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
