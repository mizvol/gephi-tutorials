# SigmaJS Exporter tutorial. From Gephi to the Web

In this tutorial we will learn:
 * How to prepare a graph layout before publishing it online.
 * How to export SigmaJS template and customize it.
 * How to publish your interactive graph visualization online using GitHub pages.

1. **IMPORTANT.** Install all necessary plugins before starting this tutorial (Multigravity Force Atlas 2, Circle Pack, Label Adjust, SigmaJS exporter).
![Plugins](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/SigmaJS%20exporter/images/Plugins.png)
2. Open GEXF file in Gephi (`File->Open...`). In this example, we are going to work with a subsample of English Wikipedia. The most popular pages over the period 16-31 August 2018.
3. Compute (any) layout. Let's start with **Multigravity Force Atlas 2**.

Parameters:
* Scaling: 10
* Edge Weight Influence: 0
* Dissuade hubs: True
4. Export **SigmaJS template** (`File->Export->SigmaJS template`). Fill in all required fields.
5. Go to the exported folder and start a simple python HTTP server to test your visualization. Depending on Python version, in terminal, type the following command.

* Python 3.X `python -m http.server`
* Python 2.7 `python -m SimpleHTTPServer`

Now, you can interact with your graph using a web-browser. Go to http://localhost:8000/ and play with it.

That is all we need to do to publish our visualization online. Although, as we can see, the graph looks quite raw and it is hard to interact with it. Let's compute more attributes and make the graph look nicer and more user-friendly.

6. Compute attributes.
* Modularity (Use weights: `False`)
* Average Degree
![Modularity](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/SigmaJS%20exporter/images/modularity-degree.gif)
7. Color nodes according to their modularity class and make their size coorespond to their degree.
![Attributes](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/SigmaJS%20exporter/images/color-and-size.gif)
8. Use **Circle Pack layout** to rearrange nodes according to attributes. Use modularity and degree as parameters.
* Hierarchy1: Modularity
* Hierarchy2: Degree
![CirclePack](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/SigmaJS%20exporter/images/CirclePack.png)
9. Adjust the scale and labels. Use **Expansion layout** to increase the scale of the layout. Display labels, reduce the font size and use **Label Adjust layout** to prevent overlapping node labels.
![LabelAdjust](https://raw.githubusercontent.com/mizvol/gephi-tutorials/master/SigmaJS%20exporter/images/scale.gif)
10. The layout looks more user-friednly now. Export SigmaJS template once again and check it on localhost (steps 4 and 5).
11. *Optional.* You can adjust properties of the visualization using the config file that you can find in the folder with our SigmaJS template. Play with SigmaJS config file:
* Choose node sizes.
* Adjust label thresholds.
12. *Optional.* If you are familiar with HTML/CSS, you can customise the style of the web page.
13. Now, we can publish everything to GitHub pages.
    * Create a GitHub repository.
    * Go to the settings of your repository and find GitHub pages section. Specify `master branch` as source. 
    * Clone the repository.
    * Copy the exported SigmaJS template that we have prepared to the cloned folder.
    * Push the files to the repository.
    * Check the website with your interactive visualization (https://[YOUR-GITHUB-USER-NAME].github.io/[VIS-REPOSITORY-NAME]/network/)
    * Et voila. You have just published your interactive graph visualization online.
