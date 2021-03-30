# elegant-embryos

deep-learning for metadata extraction from the _C. elegans_ embryo. 

[![Binder](https://camo.githubusercontent.com/bfeb5472ee3df9b7c63ea3b260dc0c679be90b97/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f72656e6465722d6e627669657765722d6f72616e67652e7376673f636f6c6f72423d66333736323626636f6c6f72413d346434643464)](https://github.com/Mainakdeb/elegant-embryos)


This repository contains work surrounding DevoLearn models and the _C. elegans_ embryo in general

### [Exploring Spatial distribution of cells in C. elegans embryo Using 3D Interactive Plots](explore_cell_movement_data.ipynb)
The EPIC dataset contains time series data surrounding the embryogenesis of the C. elegans embryo. I had to Extract the X, Y, Z coordinates of each cell (of all lineages), extract the timestamps of each cell in sequence, using which I generated the following plots.

1. A plot showcasing cell positions through time. 

<img src="/images/3d_plot_rotate_zoom_1.gif" width=300/> <img src="/images/3d_plot_timelapse_1.gif" width=285/>


2. Visualizing single cell movement through time. This example shows the movement of the cell of lineage 'Dpa' through time.

<img src="/images/Dpa_-9_track_compressed.gif" width=285/> <img src="/images/Dpa_-9_track_zoom_compressed.gif" width=285/>

Gaining insights from static plots can be difficult at times, this is where these interactive plots can help by enabling users to rotate, zoom, animate plots (with respect to time), rather than being stuck with just one point of time and perspective.

### [Post Processing outputs from the DevoLearn lineage population model](post_process_lineage_population_model.ipynb)
Post processing algorithms modify the outputs from the neural-network in order to further increase the accuracy of the predictions. I implemented a post processing algorithm on the lineage population model from DevoLearn, which exploits an inherent pattern in the data and modifies the model outputs accordingly, resulting in better accuracy (about 30% less loss) as highlighted in figure below.

<img src="/images/postprocess_lineage_population_1.png" width=800 />


