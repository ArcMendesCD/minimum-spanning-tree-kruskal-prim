### Árvore Geradora Minima | Minimum Spanning Tree
###### ANDREI MENDES, LAURA YUMI, GIOVANA OLIVEIRA, LETICIA PONTES
###### UNIVERSIDADE DE MARILIA | RESOLUÇÃO DE PROBLEMAS DE GRAFOS

## PT-BR
- Geração de Árvore Geradora Minima utilizando os Metodos de Kruskal e Prim
- Código escrito em Python
- Utilização da biblioteca mathlib para exibir o grafo
- Biblioteca Network para montar o grafo e embelezar a exibição

## ENG
- Minimum Spanning Tree generation utilizing the Kruskal and Prim Algorithms
- Code in Python
- Utilization of the mathlib Library to display the graph
- Utilization of the Network Library to build the connections in the graph
# Prim e Kruskal

# Árvore geradora mínima

É um subconjunto das arestas de um grafo que conecta todos os vértices (nós) sem formar
ciclos e com a menor soma total dos pesos das arestas. Porém ela pode não ser apenas uma,
pode haver múltiplas árvores geradoras mínimas com a mesma soma de pesos.

**Grafo não orientado** : A Árvore geradora mínima é definida para grafos onde as arestas não

têm uma direção.

**Grafo conexo** : Todos os vértices devem ser acessíveis a partir de qualquer outro vértice, o que
significa que não pode haver grupos separados.

**Grafo ponderado** : As arestas têm valores (pesos).

**Soma mínima** : A Árvore procura a combinação de arestas cuja soma dos pesos é a menor
possível.

**Algoritmo guloso** : A busca por uma árvore geradora mínima é um feita por algoritmos gulosos

```
Aplicações:
Logística: Rotas geográficas com menor custo e distancia.
Redes Computacionais: Redes e servidores mais rápidos e eficientes.
```

# Algoritmo de Kruskal

O Algoritmo de Kruskal é um algoritmo guloso que encontra a Árvore Geradora Mínima de um
grafo ponderado e não orientado. Ele funciona conectando vértices usando as arestas de menor
peso, garantindo que não formem ciclos. Armazena o conjunto de vértices para gerar a arvore
geradora

A lógica de Kruskal reflete em criar múltiplas árvores e nessa floresta encontrar a árvore
geradora mínima

**Etapas:**

**Vantagens:**

1. Cada vértice é um conjunto disjunto, ou seja, cada vértice possui seu próprio conjunto.
2. Todas as arestas do grafo são listadas e ordenadas em ordem crescente de peso.
3. Com isso o algoritmo se inicia a partir do menor peso.
4. Para cada aresta, verifica se os dois vértices em que ela se conecta pertence a um conjunto
    disjunto.
    a. Se pertencer a conjuntos diferentes, a aresta é adicionada a arvore geradora e os
       conjuntos são unidos.
    b. Se a aresta conectar vértices que já estão no mesmo conjunto, ela é ignorada.
5. Então um ciclo é completado e voltará à etapa inicial até que percorra todos os vértices do
    grafo.

```
Bom para grafos pequenos
```

**Desvantagens:**

# Algoritmo de Prim

O algoritmo de Prim constrói a árvore geradora mínima expandindo uma árvore a partir de um
único vértice, adicionando consecutivamente a aresta de menor peso que conecta um vértice já
incluído na árvore a um vértice que ainda não foi incluído.

**Etapas:**

**Vantagens:**

**Desvantagens:**

# Código:

```
Custo computacional pequeno
```
```
Custo computacional grande
Pouca eficiência
Ruim para grafos grandes
```
1. O algoritmo começa selecionando um vértice inicial (qualquer vértice, que pode ser
    escolhido pelo usuário).
2. Para cada vértice no grafo, é atribuído um valor padrão chave (key), que representa o peso
    da aresta mais leve que conecta esse vértice à árvore geradora, e um pai (parent), que
    guarda o vértice anterior na árvore.
3. Para o vértice inicial tem sua chave definida como 0, pois é a inicial.
4. O algoritmo mantém um conjunto de vértice que ainda não foram incluídos na árvore
    geradora. Inicialmente, todos os vértices estão nesse conjunto.
5. Enquanto o conjunto de vértices não incluídos não estiver vazio o algoritmo seleciona o
    vértice com a menor chave que ainda não foi incluído na arvore e remove do conjunto de
    vértices não incluídos.
6. Para cada vértice adjacente que ainda não foi incluído na árvore verifica se a chave é maior
    que o peso da aresta que conecta o vértice atual ao adjacente, se for, atualiza a chave desse
    vértice adjacente para o peso da aresta e definimos o pai desse vértice como o vértice que
    acabamos de adicionar na árvore.
7. A cada ciclo uma nova aresta é adicionada á arvore a partir do último vértice incluído.
8. Então o processo é repetido até que todos os vértices estejam incluídos na árvore geradora.

```
Bom para grafos extensos
Eficiente
Custo computacional pequeno
```
```
Ruim para grafos menores
Verificações repetitiva
```
```
GitHub - ArcMendesCD/minimum-spanning-tree-kruskal-prim: ÁRVORE GERADORA MINIMA...
```

