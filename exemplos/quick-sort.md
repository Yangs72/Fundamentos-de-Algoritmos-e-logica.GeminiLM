# Quick Sort

## Objetivo

Compreender o funcionamento do Quick Sort, o conceito de pivô, sua complexidade, vantagens, limitações e aplicações.

---

## O que é?

O Quick Sort é um algoritmo de ordenação baseado na estratégia **Dividir e Conquistar (Divide and Conquer)**.

Seu funcionamento gira em torno da escolha de um **pivô**, utilizado como referência para dividir os elementos em duas partes: menores e maiores que ele.

Após essa divisão, o algoritmo ordena cada parte recursivamente até que toda a lista esteja organizada.

---

## Como funciona?

O algoritmo executa três etapas principais:

1. Escolhe um elemento da lista para ser o **pivô**.
2. Reorganiza a lista de forma que:
   - elementos menores ou iguais ao pivô fiquem à esquerda;
   - elementos maiores fiquem à direita.
3. Aplica o Quick Sort recursivamente nas duas partições.

Como a ordenação acontece diretamente na própria lista (*in-place*), não existe uma etapa de combinação como ocorre no Merge Sort.

---

## Requisitos

O Quick Sort pode ser aplicado em qualquer coleção de elementos comparáveis.

Seu funcionamento depende da escolha de um pivô e do particionamento correto dos elementos.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(n log n)** |
| Caso médio | **O(n log n)** |
| Pior caso | **O(n²)** |

O pior caso ocorre quando o pivô gera partições muito desbalanceadas, como pode acontecer em listas já ordenadas dependendo da estratégia de escolha do pivô.

---

## Vantagens

- Excelente desempenho na prática.
- Baixo consumo de memória adicional (*in-place*).
- Muito eficiente para grandes conjuntos de dados.
- Amplamente utilizado em bibliotecas de programação.

---

## Limitações

- Pode apresentar desempenho **O(n²)** no pior caso.
- Não é um algoritmo estável.
- A escolha inadequada do pivô pode reduzir sua eficiência.

---

## Exemplo intuitivo

Imagine organizar pessoas em uma fila utilizando uma pessoa como referência.

Todos os que são menores ficam à esquerda.

Todos os maiores ficam à direita.

Depois, cada grupo repete exatamente o mesmo processo até que toda a fila esteja organizada.

Essa é a ideia do Quick Sort.

---

## Exemplo em Python

```python
def quick_sort(lista):
    if len(lista) <= 1:
        return lista

    pivo = lista[len(lista) // 2]

    menores = [x for x in lista if x < pivo]
    iguais = [x for x in lista if x == pivo]
    maiores = [x for x in lista if x > pivo]

    return quick_sort(menores) + iguais + quick_sort(maiores)
```

---

## Aplicações

- Bibliotecas de ordenação.
- Sistemas operacionais.
- Bancos de dados.
- Processamento de grandes volumes de dados.
- Algoritmos que exigem alta eficiência.

---

## O que aprendi

O Quick Sort utiliza um pivô para dividir o problema em partes menores e ordenar cada uma delas recursivamente. Sua complexidade média de **O(n log n)** e o baixo consumo de memória fazem dele um dos algoritmos de ordenação mais utilizados na prática, embora sua eficiência dependa da escolha do pivô.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
