# Lecture 1 - Review of Graph Theory

## What is a Graph

A graph is an object with edges and vertices as a set (generally)

Graphs can be formalized in the following manner...

**Professor's Definition**:\
$V(G) : \{ \text {vertices} v | v \in G\}$\
$E(G) : \{ \text{edges } e | e \in G\}$\
$R : \text{Relation of edge } e \text{ joining vertices } x \text{ and } y$

$Let G : Graph ⇒  G := (V(G), E(G), R)$ 

> **Note**: The professor probably meant for R to be analogous to $\phi$ in a directed multigraph.
> Modifying the wikipedia definition might serve us a little better here for clarity sake.
> I love formalism so I tweak about this.
> Also I think that this relation R has a pretty nebulous definition here, how do we have a binary
> relation with 3 things we need to relate? Is this even a binary relation? Am I losing sleep?

**Modified Wikipedia Definition**:\
$V(G) : \{ \text{vertices } v \mid  v \in G\}$ \
$E(G) : \{ \text{edges } e \mid e \in G\}$ \
$\phi : E(G) → \{(x,y) \mid (x,y) ∈ V² ∧ x≠y\}$ 

$\text{Let } G : Graph ⇒  G : (V(G), E(G), \phi)$
## Where do Graphs Come From?

In the real world graphs are everywhere, here are a few examples:
- Maps, Social Networks, Internet, Matrices (bipartite), Symmetric Matrices, Groups,
Quantum States, Radar or Network Coverage, Scheduling Patterns, etc.

> **Note**: RF coverage graphs are often called *semi-algebraic graphs*. Cool I guess.

> **Another Note**: We can represent Groups as graphs. Graphs are a more general object than groups.
Some group theory stuff has analogies in graph theory which is also cool too. 

## Fundamentals of Graph Theory

Graph theory came about from Euler's **Königsberg Bridge Problem** in 1736

We have 4 islands with 7 bridges, is there a way to walk all 7 bridges only once? No.\
Tried to solve using vertices as landmasses and edges as bridges.

> **Proof**: Suppose there was such a walk, let u,v, be starting and ending vertices of the walk.
> Then every vertex besides possibly u and v is incicent to an even number of edges in G.
> But this vertex has > 2 vertices incident to an odd number of edges, thus a contradiction. **QED**

## Graph Terminology

**Incedent**: for edge $e \in E(G)$ and vertex $v \in V(G)$ : $v$ is incident to $e$ if $v$ is an endpoint of $e$\
**Adjacent**: u,v ∈ V(G) | e ∈ E(G) with endpoints u,v\
**Loop**: e ∈ E(G) | endpoints of e are equal\
**Parallel**: e, f ∈ E(G) | endpoints of e, f are the same\
**Simple**: G does not contain parallel edges ⇒  G: (V(G), E(G)) | e ∈ E(G) ⊂ V(G) ∧ |e| = 2\

## Graph Isomorphisms

**Isomorphism**: for graphs $G$, $H$:\
$\exists f: V(G) \to  V(H) :  \forall u, v \in V(G),\space uv \in E(G) \iff f(u)f(v) \in E(H)$\
Essentially just showing a bijection between vertex sets

**Degree**: Deg of vertex $v \in V(G)$ is the number of edges incident to $v$
- Degree can be denoted like $d_{G}(v)$

> **Note**: Graph isomorphism runs in quasi-polynomial time. (Something like: ${2^{(logn)}}^{2}$)
> **Another Note**: Graph isomorphism time complexity is:
> - Known to **not be in P** 
> - Known to **not be in NP-Complete** 
> - Known to be **in NP** 


