---
layout: page
title: Neumaier graphs
description: Constructions, nexus values and open problems
img: assets/img/tetrahedron.svg
importance: 1
category: res
---

<style>
table { border-collapse: collapse; width: 100%; }
th, td { padding: 8px; text-align: left; border-bottom: 1px solid var(--global-divider-color); }
td:hover { background-color: var(--global-card-bg-color); }
#references { margin-top: 3rem; }
</style>

[16g]: {{ site.url }}/download/graphs/16-9-4-2-4.g
[16m]: {{ site.url }}/download/graphs/16-9-4-2-4.txt
[24g]: {{ site.url }}/download/graphs/24-8-2-1-4.g
[24m]: {{ site.url }}/download/graphs/24-8-2-1-4.txt
[28g]: {{ site.url }}/download/graphs/28-9-2-1-4.g
[28m]: {{ site.url }}/download/graphs/28-9-2-1-4.txt
[40g]: {{ site.url }}/download/graphs/40-12-2-1-4.g
[40m]: {{ site.url }}/download/graphs/40-12-2-1-4.txt
[65g]: {{ site.url }}/download/graphs/65-16-3-1-5.g
[65m]: {{ site.url }}/download/graphs/65-16-3-1-5.txt
[78g]: {{ site.url }}/download/graphs/78-17-4-1-6.g
[78m]: {{ site.url }}/download/graphs/78-17-4-1-6.txt
[310g]: {{ site.url }}/download/graphs/310-39-8-1-10.g
[310m]: {{ site.url }}/download/graphs/310-39-8-1-10.txt

_Literature reviewed: 17 October 2026._

## Contents

<nav aria-label="Page contents">
  <ul>
    <li><a href="#introduction">Introduction</a></li>
    <li><a href="#constructions">Constructions</a></li>
    <li><a href="#properties">Properties</a></li>
    <li><a href="#an-open-problem">An open problem</a></li>
    <li><a href="#small-strictly-neumaier-graphs">Small strictly Neumaier graphs</a></li>
    <li><a href="#references">References</a></li>
  </ul>
</nav>

## Introduction

In 1981, Neumaier {% cite N_1981 --file neumaier_project %} studied regular cliques in edge-regular graphs and asked whether an edge-regular graph containing a regular clique must be strongly regular. Greaves and Koolen answered this question negatively by constructing graphs with a regular clique that are edge-regular but not strongly regular {% cite GK_2018a GK_2018b --file neumaier_project %}.

> **Neumaier graph**
> : A non-complete edge-regular graph containing a regular clique.
>
> **Strictly Neumaier graph**
> : A Neumaier graph that is not strongly regular.

A regular clique has **nexus** $$e$$ if every vertex outside the clique has exactly $$e$$ neighbours in it. We write the parameters of a Neumaier graph as $$(v,k,\lambda;e,s)$$: the graph has $$v$$ vertices and valency $$k$$, adjacent vertices have $$\lambda$$ common neighbours, and it contains an $$e$$-regular clique of size $$s$$.

Since the first constructions, strictly Neumaier graphs have provided examples connecting algebraic graph theory, finite geometry, number theory and computation. Recent work has substantially expanded both the known constructions and the range of possible nexuses.

## Constructions

Greaves and Koolen gave the first infinite family of strictly Neumaier graphs {% cite GK_2018a --file neumaier_project %}, followed by a construction using antipodal classes in distance-regular graphs {% cite GK_2018b --file neumaier_project %}.

Evans, Goryainov, Konstantinova and Mednykh developed a general construction with nexus one and a related switching operation {% cite EGKM_2023 --file neumaier_project %}. Abiad, Castryck, De Boeck, Koolen and Zeijlemaker combined this construction with number-theoretic arguments involving Jacobi sums to obtain further infinite families {% cite ACDKZ_2023 --file neumaier_project %}.

More recently, Abiad, Castryck, De Boeck, Khramova and van Veluw have developed a finite-ring framework that unifies several earlier constructions {% cite ACCKV_2026 --file neumaier_project %}. It yields three new families, based on finite-field norm maps, dual numbers over $$\mathbb F_4$$, and quotients of the Eisenstein integers. Each contains infinitely many strictly Neumaier graphs with nexus one.

Constructions with power-of-two nexus began with Evans, Goryainov and Panasenko, who determined the unique smallest strictly Neumaier graph, with parameters $$(16,9,4;2,4)$$, and constructed two infinite sequences with nexus $$2^i$$ for every positive integer $$i$$ {% cite EGP_2019 --file neumaier_project %}. Evans, Goryainov, Ryabov and Zhao subsequently used relative difference sets to construct an infinite family of strictly Neumaier Cayley graphs with nexus $$2^i$$ for every positive even integer $$i$$ {% cite EGRZ_2027 --file neumaier_project %}. Their work also gives a criterion and an algorithm for constructing Neumaier Cayley graphs whose regular cliques form a spread of subgroup cosets.

The known nexuses are no longer restricted to powers of two. The small-graph study of Abiad, De Boeck and Zeijlemaker already reports examples with parameters $$(64,28,12;3,8)$$ and $$(64,42,26;5,8)$$, crediting computations communicated by Goryainov in 2023 {% cite ADZ_2024 --file neumaier_project %}. These examples also occur in the subsequent Cayley enumeration {% cite EGRZ_2027 --file neumaier_project %}.

Greaves and Tan's construction using cyclotomy over products of finite fields provides strictly Neumaier examples with **every nexus** $$e\in\{1,2,\ldots,20\}$$, as well as further values {% cite GT_2026a --file neumaier_project %}. The construction also contains strongly regular graphs, so its strictness conditions matter when choosing examples. It settles many individual cases of the general existence question, but does not settle it for arbitrary nexus.

Greaves and Tan have also constructed an infinite family of strictly Neumaier graphs of coherent rank five {% cite GT_2026b --file neumaier_project %}. For every prime power $$q\geq7$$ with $$q\equiv3\pmod4$$, their construction gives parameters

$$
\left(
(q+1)q(q-2),\;
\frac{(q+1)^2(q-2)}{2},\;
\frac{(q+1)(q^2+q-8)}{4};\;
\frac{(q-1)^2}{2},\;
q(q-2)
\right).
$$

In particular, the nexus is

$$
e=\frac{(q-1)^2}{2}.
$$

The choices $$q=7,11,19,23,27$$ give nexuses $$18,50,162,242,338$$, respectively. This supplies infinitely many strictly Neumaier graphs whose nexus is not a power of two. The smallest member of this family has parameters $$(280,160,96;18,35)$$. The construction uses Hadamard matrices and mutually appropriate Latin squares; its graphs also have exactly five distinct adjacency eigenvalues.

## Properties

### Small graphs and parameter restrictions

Basic parameter restrictions appear in {% cite EGP_2019 --file neumaier_project %}, with further nonexistence results in {% cite ACDKZ_2023 --file neumaier_project %}. Abiad, De Boeck and Zeijlemaker give a theoretical proof of the uniqueness of the 16-vertex example, construct a graph with parameters $$(25,12,5;2,5)$$ from a Latin square, and use integer programming to exclude several other parameter sets {% cite ADZ_2024 --file neumaier_project %}. Such exclusions concern particular parameter sets, rather than ruling out a nexus at every order.

### Eigenvalues and coherent rank

Abiad, De Bruyn, D'haeseleer and Koolen proved that a Neumaier graph cannot have exactly four distinct eigenvalues {% cite ADDK_2021 --file neumaier_project %}. Examples with exactly five eigenvalues are now known: De Bruyn, Evans, Goryainov and Koolen construct 1063 pairwise nonisomorphic graphs with parameters $$(48,14,2;1,4)$$, of which 25 have exactly five eigenvalues {% cite DBEGK_2026 --file neumaier_project %}. Their [graph6 data](https://zenodo.org/records/19072050) is available separately.

Coherent rank measures the dimension of a graph's coherent closure. The family described above establishes the existence of strictly Neumaier graphs of coherent rank five {% cite GT_2026b --file neumaier_project %}. Questions remain about the smallest possible order at this rank and the structure of the coherent closure.

### Smallest eigenvalue and colourings

Yang and Koolen prove that only finitely many strictly Neumaier graphs have smallest eigenvalue at least $$-3$$ {% cite YK_2025 --file neumaier_project %}. Abiad, De Bruyn and van Veluw show that a Hoffman-colourable Neumaier graph must be strongly regular; consequently, strictly Neumaier graphs are not Hoffman colourable {% cite ADBV_2026 --file neumaier_project %}.

## An open problem

Although examples are known for every nexus from 1 to 20 and for further unbounded sequences of values, the general existence question remains {% cite GT_2026a EGRZ_2027 --file neumaier_project %}:

> For every positive integer $$e$$, does there exist a strictly Neumaier graph containing an $$e$$-regular clique?

The new families show that nexuses need not be powers of two. The remaining challenge is to obtain a strictly Neumaier graph for an arbitrary prescribed positive nexus. An infinite sequence of realized nexuses does not by itself answer this question.

## Small strictly Neumaier graphs

The following table lists strictly Neumaier graphs on at most 310 vertices. The Cayley counts refer to graphs admitting a spread of subgroup cosets {% cite EGRZ_2027 --file neumaier_project %}.

The GAP files contain lists of graphs in GRAPE format, and the matrix files contain adjacency matrices of the same graphs {% cite GRAPE_2018 GAP_4.11.1 --file neumaier_project %}. Numbers in the Downloads column count graphs in the linked collection. A dash means that no download is linked here.

<div class="table-responsive" markdown="1">

| Parameters             | Description                                                                                                                   | Downloads (#graphs)                                             |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| (16, 9, 4; 2, 4)       | Unique smallest, vertex-transitive {% cite EGP_2019 ADZ_2024 --file neumaier_project %}                                       | [gap][16g], [mat][16m] (1)                                      |
| (24, 8, 2; 1, 4)       | Four vertex-transitive examples; a diameter-three example is also known {% cite GK_2018b EGKM_2023 --file neumaier_project %} | [gap][24g], [mat][24m] (6)                                      |
| (25, 12, 5; 2, 5)      | A Latin-square construction {% cite ADZ_2024 --file neumaier_project %}                                                       | —                                                               |
| (28, 9, 2; 1, 4)       | Two vertex-transitive examples {% cite GK_2018a --file neumaier_project %}                                                    | [gap][28g], [mat][28m] (4)                                      |
| (40, 12, 2; 1, 4)      | A vertex-transitive example {% cite EGKM_2023 --file neumaier_project %}                                                      | [gap][40g], [mat][40m] (1)                                      |
| (48, 14, 2; 1, 4)      | A construction gives 1063 examples, including 25 with five eigenvalues {% cite DBEGK_2026 --file neumaier_project %}          | [graph6 collection](https://zenodo.org/records/19072050) (1063) |
| (52, 15, 2; 1, 4)      | A vertex-transitive example {% cite GK_2018a --file neumaier_project %}                                                       | —                                                               |
| (60, 14, 4; 1, 6)      | An example from the antipodal construction {% cite GK_2018b ADZ_2024 --file neumaier_project %}                               | —                                                               |
| (64, 28, 12; 3, 8)     | 18 Cayley examples with a subgroup-coset spread {% cite EGRZ_2027 --file neumaier_project %}                                  | —                                                               |
| (64, 35, 18; 4, 8)     | 1380 Cayley examples with a subgroup-coset spread {% cite EGRZ_2027 --file neumaier_project %}                                | —                                                               |
| (64, 42, 26; 5, 8)     | A Cayley example with a subgroup-coset spread {% cite EGRZ_2027 --file neumaier_project %}                                    | —                                                               |
| (65, 16, 3; 1, 5)      | A vertex-transitive example {% cite EGKM_2023 ACDKZ_2023 --file neumaier_project %}                                           | [gap][65g], [mat][65m] (1)                                      |
| (78, 17, 4; 1, 6)      | Eight vertex-transitive examples {% cite EGKM_2023 --file neumaier_project %}                                                 | [gap][78g], [mat][78m] (8)                                      |
| (112, 36, 10; 2, 7)    | A cyclotomic construction with coherent rank six {% cite GT_2026a --file neumaier_project %}                                  | —                                                               |
| (133, 42, 13; 2, 7)    | A cyclotomic construction with coherent rank six {% cite GT_2026a --file neumaier_project %}                                  | —                                                               |
| (168, 27, 6; 1, 8)     | Twelve reported examples, including one vertex-transitive {% cite EGKM_2023 --file neumaier_project %}                        | —                                                               |
| (185, 40, 3; 1, 5)     | A vertex-transitive example {% cite ACDKZ_2023 --file neumaier_project %}                                                     | —                                                               |
| (208, 72, 26; 4, 13)   | A cyclotomic construction with coherent rank six {% cite GT_2026a --file neumaier_project %}                                  | —                                                               |
| (232, 35, 6; 1, 8)     | A cyclotomic construction {% cite GT_2026a --file neumaier_project %}                                                         | —                                                               |
| (243, 34, 7; 1, 9)     | A norm-map construction {% cite ACCKV_2026 --file neumaier_project %}                                                         | —                                                               |
| (250, 33, 8; 1, 10)    | Sixteen reported examples, including one vertex-transitive {% cite EGKM_2023 --file neumaier_project %}                       | —                                                               |
| (256, 135, 70; 8, 16)  | Examples from the power-of-two families {% cite EGP_2019 --file neumaier_project %}                                           | —                                                               |
| (280, 160, 96; 18, 35) | Coherent rank five and five distinct eigenvalues {% cite GT_2026b --file neumaier_project %}                                  | —                                                               |
| (310, 39, 8; 1, 10)    | A vertex-transitive example {% cite EGKM_2023 --file neumaier_project %}                                                      | [gap][310g], [mat][310m] (1)                                    |

</div>

## References

<div class="publications">
  {% bibliography --file neumaier_project %}
</div>
