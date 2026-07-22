# Busca Binária

## Objetivo

Compreender o funcionamento da Busca Binária, seus requisitos, vantagens, limitações e aplicações práticas.

---

## O que é?

A Busca Binária é um algoritmo de pesquisa utilizado para localizar um elemento em uma coleção de dados ordenada.

Em vez de verificar todos os elementos, o algoritmo reduz pela metade a quantidade de itens analisados a cada etapa, tornando a busca muito mais eficiente.

---

## Como funciona

O algoritmo segue o seguinte processo:

1. Seleciona o elemento central da lista.
2. Compara o valor procurado com o elemento central.
3. Se forem iguais, a busca termina.
4. Se o valor procurado for menor, continua pesquisando apenas na metade esquerda.
5. Se for maior, continua apenas na metade direita.
6. O processo se repete até encontrar o elemento ou concluir que ele não existe.

---

## Requisito

A lista deve estar ordenada.

Sem essa condição, a Busca Binária não funciona corretamente.

---

## Complexidade

| Caso | Complexidade |
|------|--------------|
| Melhor caso | O(1) |
| Caso médio | O(log n) |
| Pior caso | O(log n) |

---

## Vantagens

- Muito rápida em listas grandes.
- Reduz significativamente o número de comparações.
- Excelente desempenho para pesquisas frequentes.

---

## Limitações

- Requer que os dados estejam ordenados.
- Não é a melhor opção para listas pequenas.
- Inserções e remoções frequentes podem exigir nova ordenação.

---

## Aplicações

A Busca Binária é utilizada em diversos contextos, como:

- pesquisa em bancos de dados;
- busca em listas ordenadas;
- sistemas de recomendação;
- otimizações em algoritmos;
- bibliotecas de programação.

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

        elif lista[meio] < alvo:
            esquerda = meio + 1

        else:
            direita = meio - 1

    return -1
```

---

## O que aprendi

A Busca Binária é muito mais eficiente do que a Busca Linear quando os dados estão ordenados.

Seu desempenho cresce de forma logarítmica, tornando-a uma das técnicas fundamentais para o desenvolvimento de algoritmos eficientes.

---

## Referências

Este conteúdo foi produzido com base na base de conhecimento construída no NotebookLM e revisado pelo autor para fins de estudo.
