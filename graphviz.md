---
title: Graphviz
---

<http://graphviz.org>

Output SVG
----------

```bash
dot file.dot -Tsvg -o output.svg
```

Plain graph
-----------

```
digraph graph_name {
  A [label="Node A"] // sample comment
  B [label="Node B"]
  A->B [label="commands", fontcolor=red]
  X->Y->Z
}
```


