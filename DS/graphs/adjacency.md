# Adjacency

Graphs are usually representated in 2 ways.

## Adjacency Matrix (less used)

This is a 2D array, where each internal array represents the weight of the connection between current vertex (index of outter array) with another vertex. Example:

```
Graph with 2 vertex without any connections
[
  [0],   // V1
  [0],   // V2
]

Connected graph with 2 vertexes that are connected to each other
[
  [1],   // V1
  [1],   // V2
]

Connected graph with 2 vertexes that are connected to each other, but only from V(0) to V(1)

[
  [1],   // V1
  [0],   // V2
]
```

## Adjacency List

Kinda similar to Matrix, instead we use an object with `to` and `weight` to represend which other vertexes a vertex is connected to. Example:


```
[
  [{"to": 1, "weight": 10}, {"to": 2, "weight": 5}],
  [{"to": 2, "weight": 10}],
  [{"to": 0, "weight": 20}]
]

```


