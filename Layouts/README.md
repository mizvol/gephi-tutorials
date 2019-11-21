# Layouts tutorial

**IMPORTANT.** Install plugins (Multigravity Force Atlas 2, Circle pack, Leiden, Bridging centrality, Clustering coefficient)

### Force-directed layouts.

* Examples

Multigravity Force Atlas 2 |  Yuifan Hu | Fruchterman-Reingold | Open Ord
:-------------------------:|:-------------------------:|:-------------------------:|:-------------------------:
![Multigravity Force Atlas 2](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/force-atlas.gif)  |  ![Yuifan-hu](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/yifan-hu.gif) | ![Fruchterman-Reingold](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/f-r.gif) | ![Open Ord](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/Layouts/images/openord.gif)

* Parameters
	* Multigravity Force Atlas 2 
		* *Scaling*. Control scale of the expansion of the graph. 
		* *Dissuade hubs*. Apply stronger repulshion forces to hubs.
		* *Prevent overlap*. Prevent nodes from overlapping.
	* Yuifan Hu
		* *Step ratio*. High ratio improves quality (at the expense of speed)
		* *Optimal distance*. Controls distance between nodes
		* *Theta*. Smaller Theta gives leads to more accurate results (slower)
	* Fruchterman-Reingold
		* *Gravity*. Attraction strength.
		* *Speed*. Tradeoff between speed and accuracy. Higher values lead to faster but less accurate results
	* Open Ord
		* *Edge Cut (0 to 1)*. Higher values lead to more clustered results.
		* *Num Iterations*. Higher values lead to larger expansion.

### Attributes
    * Node size
    	* *Degree*. Connectivity of a node
    	* *Centrality*
		* *Betweenness*. Number of random walks passing through the node
		* *Bridging*. Measure of bi-partisanship of a node. Nodes that connect multiple communities (serve as bridges) have high bridging centrality
    	* *Page rank*. Importance of a node
    	* *Clustering coefficient*. Determines how close are neighbours of a node to a complete graph
    * Color
    	* Community detection (Louvain, Leiden)
### Attributed layouts
    * Circular layout
    * Radial Axis
	* Splitter
	* Circle pack
### Spatial transformation layouts (to enhance readability)
	* Expansion/Contraction (change scale)
	* Noverlap (prevent overlap of nodes)
	* Label adjust (prevent overlap of labels)

Some information is taken from the official [Gephi tutorial](https://gephi.org/users/tutorial-layouts/).
