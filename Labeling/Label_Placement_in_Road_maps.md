# Label Placement in Road Maps

[Gemsa (2015)](https://link.springer.com/chapter/10.1007/978-3-319-18173-8_16)


## Introduction

This research indicates that placing non-overlapping road labels to maximize the number of idenfied road sections is NP-hard. A polynomial-time algorithm and the improvements on running time are proposed.

## Method
* Notations:
    * $\omega(G)$: the maximum number of vertices of a complete subgraph of the graph.
    * Complete subgraph: a set of nodes for which all the nodes are connected to each other.
* Label $l$ for a road $R$ is a curve $l\subseteq {\rm E}(R)$ whose endpoints must lie on road sections and not on junction edges or junction vertices.
* Polynomial-time algorithm
    * Determine a finite set of candidate positions for the heads and tails of labels
    * Transform tree into subtrees 
    ![](https://i.imgur.com/DaX1Qno.png)
    lowest point: $p\in l$ is the lowest point of $l$ if $d_p \leq d_q$ for any $q\in l$
    vertical curve: $h(l)$ or $t(l)$ is the lowest point of $l$
    * Canonical labeling $L$: an optimal labeling L of T. For each label $l\in L'$ there exists a vertex $v$ in $T'$ with ${\rm E}(v)=h(l)$ or ${\rm E}(v)=t(l)$. 
    ![](https://i.imgur.com/glUkBRw.png)
    * Algorithm 
    ![](https://i.imgur.com/CJp10O5.png)



## Results

Due to the size of the subdivision tree $T'$, there are $O(n^2)$ vertices. For each vertex $u$, the procedure `OptCandidate` needs $O(n^3)$ time, which yields $O(n^5)$ running time in total. As for space complextity, we need $O(n^2)$ storage to store $T'$. The problem can be solved in $O(n^3)$ time and linear space for the special case of trees.

## Discussion
The font size of the labels is not mentioned in this paper.
Will a flexible font size be a relaxation of the problem? In reality, a road map usually contains various font sizes of road labels depends on the available space.
