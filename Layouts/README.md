# Layouts tutorial

Prepare a relatively small graph (~2000 nodes ~10000 edges)

**IMPORTANT.** Install plugins (Multigravity Force Atlas 2, Circle pack, Leiden, Bridging centrality, Clustering coefficient)

1. Force-directed layouts.

Multigravity Force Atlas 2 |  Yuifan Hu | Fruchterman-Reingold | Open Ord
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
![Multigravity Force Atlas 2](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/force-atlas.gif)  |  ![Yuifan-hu](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/yifan-hu.gif) | ![Fruchterman-Reingold](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/f-r.gif) | ![Open Ord](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/openord.gif)



1. Force-directed layouts
    * Multigravity Force Atlas 2 (Scaling 100, Dissuade hubs)
    * Yuifan Hu (Default)
    * Fruchterman-Reingold (Gravity 0, Speed 100)
    * Open Ord (Default)
2. Attributes
    * Node size
    	* Degree. Connectivity of a node.
    	* Centrality (betweenness (number of random walks passing through the node), bridging (measure of bi-partisanship, nodes that connect multiple communities (serve as bridges) have high bridging centrality))
    	* Page rank (importance of a node).
    	* Clustering coefficient.
    * Color
    	* Community detection (Louvain, Leiden)
3. Attributed layouts
    * Circular layout
    * Radial Axis
	* Splitter
	* Circle pack
4. Spatial transformation layouts (to enhance readability)
	* Expansion/Contraction (change scale)
	* Noverlap (prevent overlap of nodes)
	* Label adjust (prevent overlap of labels)
