---
layout: page
title: GraphSym
description: A GAP library
img: assets/img/gaplogo-notext-dark.png
importance: 2
category: dev
---

The GraphSym (graphs with symmetries) library {% cite GraphSym_2024 --file graphsym %} is a package available in GAP {% cite GAP_2025 --file graphsym %}, which is still in an early stage of development.

The GraphSym package contains various collections of graphs with interesting symmetry properties. Each collection of graphs are attained from complete or partial enumerations published in international journals. The papers documenting these enumerations are referenced below, and their authors are included as contributors to the package (unless they are an author of this package). The GraphSym package provides functionality enabling easy access to these graphs, along with several precomputed properties related to many of the graphs stored within. 

### How it works

To download and install the GraphSym package, as well as to get more information on related research, please visit the [GraphSym package homepage](https://rhysje00.github.io/graphsym/) and the package manual of the [GraphSym gap package](https://github.com/rhysje00/graphsym).

Currently, this package deals with finite graphs as  **Digraphs** objects {% cite DIGRAPHS_2024 --file graphsym %}, and much of the functionality provided is based on the very nice code found in the *Visualising and IO* section of the Digraphs manual. 

This package will be developed in parallel with the [AGT package](https://gap-packages.github.io/agt/) to allow in-depth analysis of the algebraic and combinatorial  properties of graphs from many classes.

### Coming soon

The GraphSym package is based on the collections of graphs found at the [GraphSym homepage](https://graphsym.net/). We are currently working on extending this package, and plan to include collections of graphs such as

  * known collections of highly symmetric graphs and maps
  * new collections of low valency Cayley graphs and minimal Cayley graphs,
  * new collections of bi-cayley graphs, and other classes with more than one orbit on vertices,
  * new collections of 3-maniplexes and 4-maniplexes (integrated with the [RAMP package](https://github.com/SupposeNot/RAMP))
  * new packages/integration with other computer algebra systems (e.g Magma, sage and Oscar)  

If you have are interested in certain functionalities or datasets that are currently not available, please let me know!

---  
#### Links  
  
  <!-- * Homepage: [GraphSym homepage](https://gap-packages.github.io/agt/)  -->
  * [GraphSym homepage](https://graphsym.net/)
  * [GraphSym gap package](https://github.com/rhysje00/graphsym)
  * [AGT package](https://gap-packages.github.io/agt/)
  * [RAMP package](https://github.com/SupposeNot/RAMP))
  * Other repositories: [repositories page](/repositories/)

---
## References
---

<div class="publications">

{% bibliography -f graphsym %}

</div>
