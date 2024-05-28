## Example of a Multilayer Network

Consider a multilayer network $\mathcal{M} = (\mathcal{G}, \mathcal{C})$ where:

- $\mathcal{G} = {G_1, G_2, G_3}$, consisting of three layers.
- Each layer $G_\alpha = (X_\alpha, E_\alpha)$ is defined as follows:
    - Layer $G_1$:
        - Nodes: $X_1 = {A, B, C}$
        - Edges: $E_1 = {(A, B), (B, C)}$

    - Layer $G_2$:
        - Nodes: $X_2 = {D, E, F}$
        - Edges: $E_2 = {(D, E), (E, F), (F, D)}$

    - Layer $G_3$:
        - Nodes: $X_3 = {G, H, I}$
        - Edges: $E_3 = {(G, H), (H, I), (I, G)}$

- $\mathcal{C}$, the set of interconnections between nodes of different layers, is defined as: $\mathcal{C} = {(A, D), (B, H), (C, I), (E, G)}$

The set $E(\mathcal{M}) = E_1 \cup E_2 \cup E_3 \cup \mathcal{C}$ includes all intralayer and interlayer connections.

## Example of a Walk

Consider a walk of length $4$ in the multilayer network $\mathcal{M}$:

- Starting Node: $A$ in layer $G_1$.
- Walk Sequence:
    - $(A, B)$ in $G_1$.
    - $(B, H)$ in $\mathcal{C}$ (interlayer connection from $G_1$ to $G_3$).
    - $(H, I)$ in $G_3$.
    - $(I, C)$ in $\mathcal{C}$ (interlayer connection from $G_3$ to $G_1$).

So, the walk is: ${A^1_1, (A, B), B^1_2, (B, H), H^3_3, (H, I), I^3_4, (I, C), C^1_5}$.

If the edges $(A, B)$, $(H, I)$, and $(I, C)$ are weighted, the length of the walk can be defined as the sum of the inverse of the corresponding weights. For example, if the weights are $w_{AB}$, $w_{HI}$, and $w_{IC}$, respectively, then the length of the walk is $\frac{1}{w_{AB}} + \frac{1}{w_{HI}} + \frac{1}{w_{IC}}$.

If the walk starts and ends at the same node, it is considered a closed walk. In this example, the walk is not closed because it starts at $A$ and ends at $C$.