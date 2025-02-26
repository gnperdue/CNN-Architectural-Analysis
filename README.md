# CNN-Architectural-Analysis
Codes and data related to paper:

## Files Summary
Each folder [MINERvA-Vertex-Finding](MINERvA-Vertex-Finding) and [MINERvA-Hadron-Multiplicity](MINERvA-Hadron-Multiplicity) contains two sub-folders: Code and Data. There you can find the data and the analysis code that was used to produce the results in the paper.

### [Get-attributes-code](Get-attributes-code):
Contains necessary Python code objects to extract architectural attributes from the networks. Some of the documentations here were written by its original author, [Jesse Hamer](https://github.com/jhamer90811). [(link to original documentation of codes)](https://github.com/jhamer90811/MINERvA_NOvA_network_analysis)

- [caffe.proto](Get-attributes-code/caffe.proto) and [caffe_pb2.py](Get-attributes-code/caffe_pb2.py) contains the original Caffe network protobuf file, as well as the Python class compiled by Google's protobuf software. One minor modification was made to the original protobuf file in order to implement the "gradient scaler layer". Besides this, the file is the same as can be found on [Caffe's repository](https://github.com/BVLC/caffe). It should be noted that these files merely implement networks as protobuf messages. For full neural network functionality (like training and prediction), the user will need a deeper, more complete install of Caffe.

- [Network_prototxt_samples](/Get-attributes-code/Network_prototxt_samples/) contains examples of the original MINERvA's network prototxt and output files from which we extracted the architectural attributes and the network's accuracy from.

## Raw data source

We have stored the raw prototxt files from MENNDL, from which the features are extracted from. If you have access to the Wilson Cluster at Fermilab, the file paths are the following (as of August, 2019):

**Image files that the networks were trained on:** `/data/jhamer/minerva_imgs/hadmultkineimgs_127x94_me1Amc.hdf5` (6.7 GB)

**NOTE:** Human Performance Benchmark for Hadron Mutliplicity problem in paper is evaluated on ramdomly drawn input images on the same data set.

**MINERvA Vertex Finding Networks:**
- First Population: `/data/jhamer/minerva_networks/networks/` (8.1 GB)
- Second Population: `/lfstev/e-938/aghosh12/minerva_174plane/logs` (343 GB)

**MINERvA Hadron Multiplicity Networks:** `/lfstev/e-938/aghosh12/minerva_multi/logs` (1.1 TB)

**Singularity recipe to build an image:** [Link](https://github.com/Duchstf/CNN-Architectural-Analysis-SingularityImg)

Interested parties that do not have access to computing resources at Fermilab
should contact the authors (feel free to [open an issue](https://github.com/Duchstf/CNN-Architectural-Analysis/issues))
and we will make all reasonable efforts to supply the files.

Note that file sizes above may include other supporting information that is
not directly tied to this project.
