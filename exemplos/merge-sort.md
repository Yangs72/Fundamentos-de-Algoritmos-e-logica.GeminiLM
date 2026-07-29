# Merge Sort

## Objetivo

Compreender o funcionamento do Merge Sort, sua estratégia de Dividir e Conquistar, sua complexidade, vantagens, limitações e aplicações.

---

## O que é?

O Merge Sort é um algoritmo de ordenação eficiente baseado na estratégia **Dividir e Conquistar (Divide and Conquer)**.

Em vez de ordenar toda a lista de uma vez, ele divide o problema em partes menores, ordena cada uma delas e, por fim, combina essas partes para formar uma lista completamente ordenada.

---

## Como funciona?

O algoritmo executa três etapas principais:

1. **Dividir:** a lista é dividida em duas metades de tamanho aproximadamente igual.
2. **Conquistar:** cada metade é ordenada recursivamente utilizando o próprio Merge Sort.
3. **Combinar:** as duas metades já ordenadas são intercaladas para formar uma única lista ordenada.

Esse processo é repetido até que cada divisão contenha apenas um elemento, que por definição já está ordenado.

---

## Requisitos

O Merge Sort pode ser utilizado em qualquer coleção de elementos comparáveis.

Seu funcionamento depende do uso de recursão e de memória auxiliar para realizar a etapa de intercalação.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(n log n)** |
| Caso médio | **O(n log n)** |
| Pior caso | **O(n log n)** |

Seu desempenho permanece eficiente independentemente da disposição inicial dos dados.

---

## Vantagens

- Excelente desempenho em grandes volumes de dados.
- Complexidade **O(n log n)** em todos os casos.
- Algoritmo estável, preservando a ordem de elementos iguais.
- Baseado na estratégia de Dividir e Conquistar.

---

## Limitações

- Necessita de memória adicional para realizar a intercalação.
- Implementação mais complexa do que algoritmos simples.
- Pode não ser a melhor escolha para listas muito pequenas.

---

## Exemplo intuitivo

Imagine duas pilhas de cartas já organizadas.

Você compara apenas a carta do topo de cada pilha e escolhe a menor para formar uma nova pilha ordenada.

Repete esse processo até que todas as cartas tenham sido reunidas em uma única sequência ordenada.

Essa é exatamente a lógica utilizada na etapa de intercalação (*merge*).

---

## Exemplo em Python

```python
def merge_sort(lista):
    if len(lista) <= 1:
        return lista

    meio = len(lista) // 2

    esquerda = merge_sort(lista[:meio])
    direita = merge_sort(lista[meio:])

    resultado = []
    i = j = 0

    while i < len(esquerda) and j < len(direita):
        if esquerda[i] < direita[j]:
            resultado.append(esquerda[i])
            i += 1
        else:
            resultado.append(direita[j])
            j += 1

    resultado.extend(esquerda[i:])
    resultado.extend(direita[j:])

    return resultado
```

---

## Aplicações

- Ordenação de grandes volumes de dados.
- Processamento de arquivos externos.
- Bancos de dados.
- Sistemas distribuídos.
- Algoritmos de processamento paralelo.

---

## O que aprendi

O Merge Sort resolve problemas grandes dividindo-os em problemas menores e combinando as soluções obtidas. Sua complexidade **O(n log n)** faz dele uma excelente escolha para ordenar grandes conjuntos de dados, embora exija memória adicional durante a execução.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
