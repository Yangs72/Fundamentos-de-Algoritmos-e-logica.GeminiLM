# Busca Linear

## Objetivo

Compreender o funcionamento da Busca Linear, suas vantagens, limitações e aplicações.

---

## O que é?

A Busca Linear, também conhecida como pesquisa sequencial, é o método mais simples para localizar um elemento em uma coleção de dados.

O algoritmo percorre a lista elemento por elemento até encontrar o valor procurado ou chegar ao final da coleção.

---

## Como funciona?

O algoritmo segue os seguintes passos:

1. Inicia a busca pelo primeiro elemento da lista.
2. Compara o elemento atual com o valor procurado.
3. Se houver correspondência, a busca termina.
4. Caso contrário, passa para o próximo elemento.
5. O processo continua até encontrar o valor ou percorrer toda a lista.

---

## Requisitos

A Busca Linear não exige que os dados estejam ordenados, podendo ser utilizada em qualquer coleção.

---

## Complexidade

| Situação | Complexidade |
|----------|--------------|
| Melhor caso | **O(1)** |
| Caso médio | **O(n)** |
| Pior caso | **O(n)** |

No pior caso, o algoritmo pode precisar verificar todos os elementos da lista.

---

## Vantagens

- Fácil de compreender e implementar.
- Funciona em listas ordenadas e não ordenadas.
- Adequada para coleções pequenas.

---

## Limitações

- Baixa eficiência em listas grandes.
- Pode exigir a verificação de todos os elementos.
- Existem algoritmos mais rápidos para dados ordenados, como a Busca Binária.

---

## Exemplo intuitivo

Imagine procurar uma palavra específica em uma página de texto. Você lê linha por linha, da esquerda para a direita, até encontrar a palavra desejada ou chegar ao final da página.

Esse é o mesmo princípio utilizado pela Busca Linear.

---

## Exemplo em Python

```python
def busca_linear(lista, alvo):
    for indice, valor in enumerate(lista):
        if valor == alvo:
            return indice
    return -1
```

---

## Aplicações

- Pesquisa em listas pequenas.
- Coleções não ordenadas.
- Verificações simples em programas.
- Algoritmos introdutórios de programação.

---

## O que aprendi

A Busca Linear é o algoritmo de pesquisa mais simples de implementar. Apesar de ser menos eficiente em grandes volumes de dados, continua sendo uma solução útil quando os dados não estão ordenados ou quando a simplicidade é mais importante que o desempenho.

---

## Referências

Este conteúdo foi elaborado a partir dos estudos realizados no NotebookLM e revisado pelo autor para fins educacionais.
