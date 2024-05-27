## Drawing a Multilayer Network

On pen and paper, draw a multilayer network $\mathcal{M} = (\mathcal{G}, \mathcal{C})$ with the following specifications:

**Number of Layers ($M = 3$)**:
- Draw three layers ($G_1$, $G_2$, and $G_3$). Each layer should be a separate graph.

**Nodes in Each Layer**:
- Layer $G_1$ has three nodes: $A$, $B$, and $C$.
- Layer $G_2$ has three nodes: $D$, $E$, and $F$.
- Layer $G_3$ has three nodes: $G$, $H$, and $I$.

**Intralayer Connections**:
- In $G_1$: $A \leftrightarrow B$, $B \leftrightarrow C$ (undirected edges).
- In $G_2$: $D \rightarrow E$, $E \rightarrow F$, $F \rightarrow D$ (directed edges forming a cycle).
- In $G_3$: $G - H - I - G$ (undirected edges forming a triangle).

**Interlayer Connections**:
- Connect node $A$ in $G_1$ to node $D$ in $G_2$.
- Connect node $B$ in $G_1$ to node $H$ in $G_3$.
- Connect node $C$ in $G_1$ to node $I$ in $G_3$.
- Connect node $E$ in $G_2$ to node $G$ in $G_3$.

## Create the Projection Network

Given $\mathcal{M}$, write on pen and paper the projection network $proj(\mathcal{M})$.