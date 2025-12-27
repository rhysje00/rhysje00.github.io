---
layout: page
title: Neumaier graphs
description: New constructions and properties
img: assets/img/srgimages-figure1.jpg
importance: 1
category: res
---


<!--- Table settings 
   cyan-very-light #cfecf5
   pink-very-light #ffeaea
--->

<style>
table {
  border-collapse: collapse;
  width: 100%;
}

th, td {
  padding: 8px;
  text-align: left;
  border-bottom: 1px solid #ddd;
}

td:hover {background-color: #ffeaea;}
</style>


<!--- Download links --->
[16g]:{{ site.url }}/download/graphs/16-9-4-2-4.g
[16m]:{{ site.url }}/download/graphs/16-9-4-2-4.txt
[24g]:{{ site.url }}/download/graphs/24-8-2-1-4.g
[24m]:{{ site.url }}/download/graphs/24-8-2-1-4.txt
[28g]:{{ site.url }}/download/graphs/28-9-2-1-4.g
[28m]:{{ site.url }}/download/graphs/28-9-2-1-4.txt
[40g]:{{ site.url }}/download/graphs/40-12-2-1-4.g
[40m]:{{ site.url }}/download/graphs/40-12-2-1-4.txt
[65g]:{{ site.url }}/download/graphs/65-16-3-1-5.g
[65m]:{{ site.url }}/download/graphs/65-16-3-1-5.txt
[78g]:{{ site.url }}/download/graphs/78-17-4-1-6.g
[78m]:{{ site.url }}/download/graphs/78-17-4-1-6.txt

[310g]:{{ site.url }}/download/graphs/310-39-8-1-10.g
[310m]:{{ site.url }}/download/graphs/310-39-8-1-10.txt

<!---
---
<nav>
  <h4>Table of Contents</h4>
  * placeholder
  {:toc}
</nav>
--->
---
## Contents
{:.no_toc}

* A markdown
{:toc}
---
<!--- Content --->

<br>

## Introduction
---

In the early 1980s, Neumaier {% cite N_1981 --file neumaier_project %} studied regular cliques in edge-regular graphs, and a certain class of designs whose point graphs are strongly regular and contain regular cliques. In his article, he asked if there exists an edge-regular, ***non-strongly regular*** graph which contains regular clique.
 
 Almost 40 years later, Greaves and Koolen finally proved that such graphs exist, and give two general constructions of graphs {% cite GK_2018a GK_2018b --file neumaier_project %}.

Motivated by Neumaier's study of edge-regular graphs with regular cliques, we introduce the following definitions.

>  Neumaier graph
>  :  A non-complete edge-regular graph containing a regular clique.
>
>  Strictly Neumaier graph
>  :  A non-strongly regular Neumaier graph.

After the first constructions of strictly Neumaier graphs were published, there has been an increased interest the study of these graphs (see [References](#references) for some related articles).

## Constructions
---

All currently known constructions (as of {{ "now" | date: '%d/%m/%Y' }}) are found in the following articles. 

  - In {% cite GK_2018a --file neumaier_project %} the authors prove that strictly Neumaier graphs exist, and construct an infinite family of strictly Neumaier graphs.
  -  In {% cite GK_2018a --file neumaier_project %} the authors give a construction of strictly Neumaier graphs that uses antipodal classes in distance-regular graphs.
  - In {% cite EGP_2019 --file neumaier_project %} the authors find the smallest strictly Neumaier graph. Further, for each positive integer $$i$$ they construct a strictly Neumaier graphs containing regular cliques of nexus $$2^i$$. 
  - In {% cite EGKM_2021 --file neumaier_project %}, the authors present a construction of Neumaier graphs containing regular cliques with nexus $$1$$. This construction generalises the two constructions of Neumaier graphs found in {% cite GK_2018a --file neumaier_project %} and {% cite GK_2018b --file neumaier_project %}. 
  - In {% cite ACDKZ_2023 --file neumaier_project %}, number theoretical arguments are used to construct infinitely many strictly Neuamier graphs using the construction from {% cite EGKM_2021 --file neumaier_project %}. 

These constructions make use of tools from algebraic graph theory, finite geometry and number theory. Each new construction can give a connection to another area of mathematics, and help us gain a better understanding of these graphs. This gives continued motivation for constructing strictly Neumaier graphs, whether it be the construction of infinite families or the discovery sporadic examples.

<br>


## Properties
---

Now that several constructions of strictly Neumaier graphs have been observed, interest in the possible algebraic and combinatorial properties of Neumaier graphs has emerged. 

For example, basic parameter restrictions can be found in {% cite EGP_2019 --file neumaier_project %}, and further restrictions were found and used to prove nonexistence results in {% cite ACDKZ_2023 --file neumaier_project %}. The eigenvalues of a Neumaier graph have been studied in {% cite ADDK_2021 --file neumaier_project %}, where it is proved that a Neumaier graph cannot have exactly 4 distinct eigenvalues.

As this class of graphs have not been deeply studied, their are many questions about their possible structure. 
  - Classification of Neumaier graphs with extremal parameters and parameter restrictions have already been found, and is still an area to be explored. 
  - The spectrum of Neumaier graphs are less restricted than strongly regular graphs, but seem to have more structure than edge-regular graphs in general. 
  - Neumaier's original question of existence was motivated by transitivity conditions he observed in strongly regular graphs, so it is natural to also study other transitivity conditions in Neumaier graphs.

<br>

## An open problem
---

Currently, all known strictly Neumaier graph contain regular cliques with nexus $$2^i$$, for a non-negative integer $$i$$. Therefore, one of the major open problems in this area is the following:

> For every integer $$m>0$$, does there exist a strictly Neumaier graph containing an $$m$$-regular clique?

As the definition of Neumaier graphs seems less restrictive than that of strongly regular graphs, it is believed that the answer to this problem is 'yes'. The discovery of any sporadic examples or infinite families of strictly Neumaier graphs having regular cliques with nexus not $$2^i$$ will be a significant step towards solving this problem.

<br>

## Small strictly Neumaier graphs
---

Below is a table containing information about the smallest known strictly Neumaier graphs (as of {{ "now" | date: '%d/%m/%Y' }}). The content of each column is as follows.


Parameters
: All parameter tuples $$(v,k,\lambda;m,s)$$ of the known strictly Neumaier graphs on at most $$310$$ vertices. 

Description
: A short note on the known strictly Neumaier graphs with the corresponding parameters. 

Downloads
: Files containing some of the known strictly Neumaier graphs with the corresponding parameters. The 'gap' files contain a list of graphs in GRAPE format in GAP (see {% cite GRAPE_2018 GAP_4.11.1 --file neumaier_project %}). The 'mat' files contain adjacency matrices of the same graphs. The number in brackets denotes how many graphs are currently stored in the files.

<br>

<div class="datatable-begin"></div>

Parameters             | Description                                                                    | Downloads (#graphs)          |
--------------------   | ----------------------------------------------------------------------------   | --------------------------   |
(16, 9, 4; 2, 4)       | Unique smallest, vertex-transitive {% cite EGP_2019 --file neumaier_project %} | [gap][16g], [mat][16m] (1)   |
(24, 8, 2; 1, 4)       | 4 vertex-transitive, 1 diameter 3 {% cite GK_2018b EGKM_2021 --file neumaier_project %}                                                                                                      | [gap][24g], [mat][24m] (6)   |
(28, 9, 2; 1, 4)       | 2 vertex-transitive, {% cite GK_2018a --file neumaier_project %}               | [gap][28g], [mat][28m] (4)   |
(40, 12, 2; 1, 4)      | 1 vertex-transitive, {% cite EGKM_2021 --file neumaier_project %}              | [gap][40g], [mat][40m] (1)   |
(52, 15, 2; 1, 4)      | 1 vertex-transitive, {% cite GK_2018a --file neumaier_project %}               | NA (1)  |
(64, 35, 18; 4, 8)     | {% cite EGP_2019 --file neumaier_project %}                                    | NA (>2)  |
(65, 16, 3; 1, 5)      | 1 vertex-transitive, {% cite EGKM_2021 ACDKZ_2023 --file neumaier_project %}   | [gap][65g], [mat][65m] (1)   |
(78, 17, 4; 1, 6)      | 8 vertex-transitive, {% cite EGKM_2021 --file neumaier_project %}              | [gap][78g], [mat][78m] (8)   |
(168, 27, 6; 1, 8)     | 1 vertex-transitive, {% cite EGKM_2021 --file neumaier_project %}              | NA  (12)  |
(185, 40, 3; 1, 5)     | 1 vertex-transitive, {% cite ACDKZ_2023 --file neumaier_project %}             | NA  (1)  |
(250, 33, 8; 1, 10)    | 1 vertex-transitive, {% cite EGKM_2021 --file neumaier_project %}              | NA  (16)  |
(256, 135, 70; 8, 16)  | {% cite EGP_2019 --file neumaier_project %}                                    | NA  (>2)  |
(310, 39, 8; 1, 10)    | 1 vertex-transitive, {% cite EGKM_2021 --file neumaier_project %}              | [gap][310g], [mat][310m] (1) |

<div class="datatable-end"></div>  
---

<br>

## References
<div class="publications">
  {% bibliography --file neumaier_project %}
</div>
