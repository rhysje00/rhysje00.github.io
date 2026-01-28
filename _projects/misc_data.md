---
layout: page
title: Other data
description: Collections of miscellaneous objects 
img: assets/img/fp-nb.svg
importance: 1
category: dat
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

Datasets of mathematical objects are an important tool for future research. On this page, I list such datasets and give methods to access them.


## Self-promotion
---

The table below contains miscellaneous objects I have constructed during my research. They may or may not end up being used in my research, but I hope somebody finds some use in them!

<br>
<div class="datatable-begin"></div>

Name             | Description                                                                    | Access           |
--------------------   | ----------------------------------------------------------------------------   | --------------------------   |
Sylvester designs      | Contains all Sylvester designs with automorphism group of size at least 20, as GAP designs {%cite DESIGN_2019 --file misc_data %}. I used {%cite BCSW_2020 --file misc_data %}, {%cite S_2023 --file misc_data %} and {%cite ORBITER --file misc_data %} to construct these designs.| [gap](/download/SylvesterDesigns.g)|
Ree unital on $$^2G_2(27)$$      | The blocks of the Ree unital defined on $$^2G_2(27)$$. Each line of the txt file contains space-separated integers that defined a block.   | [zip](/download/ReeUnital_27_allblocks.txt.zip)(35MB)   |

<div class="datatable-end"></div>  

<br>

## External sources
---

In the table below I list some datasets that you might also find useful.

<br>
<div class="datatable-begin"></div>

Name             | Description                                                                    | Access           |
--------------------   | ----------------------------------------------------------------------------   | --------------------------   |
Martson Conder's homepage      | Maps on surfaces, quotients of triangle groups, symmetric graphs and polytopes.| [link](https://www.math.auckland.ac.nz/~conder/)|
Atlas of small regular polytopes      | All regular polytopes with at most 2000 flags (excluding 1024, 1536) | [link](https://www.abstract-polytopes.com/atlas/)|
Atlas of regular polytopes for small almost simple groups | All regular polytopes with automorphism group being almost simple of order at most 1M | [link](https://www.math.auckland.ac.nz/~dleemans/polytopes/)|
Extended group enumeration      | A table describing the enumeration of the groups of order at most 50,000  | [link](https://groups.quendi.de/)   |
MathBases      | A list of mathematical databases.  | [link](https://mathbases.org/)   |
LMFDB      | A database of objects arising in the study of number theory and arithmetic geometry.  | [link](https://www.lmfdb.org/)   |

<div class="datatable-end"></div>  

<br>



---
## References
---

<div class="publications">

{% bibliography --cited -f misc_data %}

</div>
