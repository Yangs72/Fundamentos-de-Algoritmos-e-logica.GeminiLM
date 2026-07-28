# Selection Sort

## Objetivo

Compreender o funcionamento do Selection Sort, sua complexidade, vantagens, limitações e aplicações.

---

## O que é?

O Selection Sort é um algoritmo de ordenação que organiza uma lista selecionando, a cada passagem, o menor elemento da parte ainda não ordenada e posicionando-o em seu lugar correto.

Seu funcionamento é baseado na seleção sucessiva do menor valor disponível até que toda a lista esteja ordenada.

---

## Como funciona?

O algoritmo segue os seguintes passos:

1. Percorre toda a parte não ordenada da lista procurando o menor elemento.
2. Troca esse elemento com o primeiro elemento da parte não ordenada.
3. Considera o primeiro elemento como ordenado.
4. Repete o processo para a próxima posição da lista.
5. Continua até que todos os elementos estejam ordenados.

---

## Requisitos

O Selection Sort pode ser utilizado em qualquer coleção de elementos comparáveis, sem necessidade de ordenação prévia.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(n²)** |
| Caso médio | **O(n²)** |
| Pior caso | **O(n²)** |

Embora a quantidade de elementos analisados diminua a cada passagem, o algoritmo continua realizando um número quadrático de comparações.

---

## Vantagens

- Fácil de compreender.
- Simples de implementar.
- Realiza poucas trocas de elementos em comparação com outros algoritmos simples.

---

## Limitações

- Baixa eficiência para grandes volumes de dados.
- Realiza muitas comparações.
- É superado por algoritmos mais eficientes, como Merge Sort e Quick Sort.

---

## Exemplo intuitivo

Imagine organizar uma fila de pessoas por altura.

Primeiro, você procura a pessoa mais baixa entre todas e a coloca na primeira posição.

Depois procura a menor entre as pessoas restantes e a coloca na segunda posição.

O processo continua até que todas estejam organizadas.

---

## Exemplo em Python

```python
def selection_sort(lista):
    n = len(lista)

    for i in range(n):
        menor = i

        for j in range(i + 1, n):
            if lista[j] < lista[menor]:
                menor = j

        lista[i], lista[menor] = lista[menor], lista[i]

    return lista
```

---

## Aplicações

- Ensino de algoritmos.
- Introdução aos métodos de ordenação.
- Pequenas coleções de dados.
- Situações em que o número de trocas deve ser reduzido.

---

## O que aprendi

O Selection Sort organiza os elementos escolhendo repetidamente o menor valor disponível e posicionando-o corretamente. Apesar de sua simplicidade, sua complexidade quadrática o torna inadequado para grandes volumes de dados.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
