The only file necessary to create Honeycomb Structures is main.ipynb

It is a jupyter notebook and can be run that way.
It requires all imports to be downloaded to run.

Parameters to influence the Process are:

within Setup __init__
length: how many warp yarns are used per side without the corners
nomlength: how many cells along the weft are created, it has to be a multiple of 4 (including 0) [each cell has 4 lines]
sigma: the factor of randomization, utilized in gauss distribution
layers: number of cells in the hight of the textile (2 layers create 1 cell)

The way the algorithm works (main components):

simple_rng() is used for creating new randomized lengths (including their constraints) that will be utilized for growing the structure
Weave() combines all functions to growing the structure
oeffnung() and zweischlag() handle the computations for opening and closing cells that are added

The remainder of the functions is used for plotting, handling, creating of weaving plans or are redundand artifacts.
For example commented or overwritten versions of generate_autoclicker() will create different logics of the same idea.

To utilize the script set Parameters as desired and then execute all cells as desired, the script can be run with "Run All".
Especially the picture of the weavingplan will take time to process.
Higher grades of randomization will increade the chance of the algorithm to fail. Either run again, or decrease the difficulty for success:
length = 7, nomlength = 12, sigma = 0.1, layers = 8 should work statistically often.
decreasing length or increasing any of the other parameters increases instability.
