# Lecture 2 - Connectedness

## Graph Definitions

> **Note**: Some of the defs are pretty nebulous so we will clarify underneath
> Also this will be written in more of a proof style, probably better explained
> going back and making some clarifications! :smile:

- **Path**: Graph whose vertices can be ordered s.t. two vertices are adjacent IFF consecutive.\
Sequence of vertices that are not repeated
- **Cycle**: Graph whose vertices can be placed on a cirtcle s.t two vertices are adjacent if consecutive on the circle.
- **Length**: Number of edges in a path or cycle. $P_n$ or $C_n$ (Note: $P_n$ and $C_n$ remain under isomorphism for $G$)
- **Subgraph**: Any graph $H$ with $V(H) \subseteq V(G)$ and $E(H) \subseteq E(G)$ 
- **Endpoints**: For path $P$ of degree-1 its vertices $u,v$ are its endpoints
- **Connected Components**: Maximally connected subgraphs of $G$ (maximal in terms of verts and edges)

## Lemmas about Connectedness 

> **Note**: Recall that lemmas are small propositions we prove on the way to proving a bigger theorem!

**Lemma**: \
Let $G : \text{Graph}$, Let $R :$ Relation  st $R$ is on $V(G)$ 
where $uRv$ is true if $G$ contains a $(u, v)$-path
THEN
1. $\forall v \in V(G), \space vRv$
2. $\forall u, v \in V(G), \space uRv \iff vRu$
3. $\forall a, b, c \in V(G), \space aRb \land bRc \implies aRc$

**Proof**: \
We show lemma 3 by the following: Choose paths $P_1$ and $P_2$ in $G$ s.t.
1. $a$ is an endpoint of $P_1$ 
2. $c$ is an endpoint of $P_2$ 
3. $V(P_1) \cap V(P_2) \neq \emptyset$ 

Subject to 1, 2, 3; choose $P_2$ such that $|E(P_1)| + |E(P_2)|$ is minimal.
Such a choice exists since we could take $P_1$ to be any $(a, b)$-path

Let $v_1$ be the endpoint of $P_1$ st $v_1 \neq a$. If $V(P_1) \cap V(P_2) \neq {v_1}$,
then let $P^{\prime}_{1}$ be the path obtained by deleting $v_1$ from $P_1$.
Then $V(P^\prime_1) \cap V(P_2) \neq \emptyset$ \
$\therefore \space$ 
$P^\prime_1$ and $P_2$ contradict the minimality of $P_1$ and $P_2$ \
$\therefore \space V(P_1) \cap V(P_2) = \{v_1\}$.

Similarly let $v_2$ be an endpoint of $P_2$ s.t. $v_2 \neq c$ \
by minimality $V(P_1) V(P_2) = \{v_2\}$ thus $v_1 = v_2$ so $P_1 \cup P_2$ is an $(a,c)$-path \
$Q.E.D.$

## More Lemmas Using this Proof

**Definition**:
Given $G, H : Graph$, $G \cup H$ is the graph whose vertex set is $V(G) \cup V(H)$ and
whose edge set is $E(G) \cup E(H)$ 

**Lemma**:  
A graph $G$ is connected $\iff \lnot \exists$ partition of $V(G)$ into two non-empty parts $x, y$ s.t.
there are no edges with one endpoint in $x$ and another in $y$.

**Proof**: ($\Rightarrow$) If such a partition $x, y$ existed then $G$ would not contain any
path with one endpoint in $x$ and the other endpoint in $y$

($\Leftarrow$) Suppose $G$ is disconnected. Let $u,v \in V(G)$ be vertices not joined by a path in $G$ \
Let $X = \{x \in V(G) : G \text{ contains a } (u, x)\text{-path} \}$ \
Let $Y = V(G)/X$

$X \neq \emptyset$ since $u \in X$ and $Y \neq \emptyset$ since $v \in Y$

Assume to the contrary: \
Suppose $\exists x \in X, y \in Y \mid x,y \in E(G)$ \

Then: \
$G$ contains a $(u,x)$-path. \
Since  $x,y \in V(G)$, $G$ contains an $(x,y)$-path. By transitivity $G$ contains a $(u,v)$-path
which contradicts the fact that $y \notin X$ \
$\text{Q.E.D.}$ 


