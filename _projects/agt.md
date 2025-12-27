---
layout: page
title: AGT
description: A GAP package
img: assets/img/GAP4_icon.png
importance: 1
category: dev
---

The AGT (algebraic graph theory) package {% cite AGT_2020 --file agt_project %} is a package available in GAP {% cite GAP_4.11.1 --file agt_project %}, which is still at an early stage of development. The official release version of the AGT package is available in the standard distribution of GAP.

The AGT package contains a methods used for the determination of  various algebraic and regularity properties of graphs, as well as certain substructures of graphs. The package also contains a library of strongly regular graphs (35000+ graphs), intended to be a useful resource for computational experiments. 

All of the functions in this package deal with finite simple graphs in GRAPE format {% cite GRAPE_2018 --file agt_project %}. Behind the scenes, we also use the Digraphs package {%cite DIGRAPHS_2019 --file agt_project %} to format and efficiently store and access the graphs in the strongly regular graph library. 

Some of the functions I plan to add to the package soon are:

  * A large library of graph constructors. These will initially involve merging the [gap-graphs package](https://github.com/jaanos/gap-graphs) written by Jano&#353; Vidali into the AGT package. 
  * Further eigenvalue calculations for regular graphs.
  * Functions related to transitivity properties of graphs.
  * Functions related to codes in graphs. 

---  
#### Links  
  
  * Homepage: [AGT homepage](https://gap-packages.github.io/agt/) 
  * Development version: [gap-packages AGT](https://github.com/gap-packages/agt). 
  * Other repositories: [repositories page](/repositories/)

---
## References
---

<div class="publications">

{% bibliography --cited -f agt_project %}

</div>
