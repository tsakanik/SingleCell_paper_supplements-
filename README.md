# SingleCell_paper_supplements-
Code for figure and result presented in eLife paper reproduction

		Instructions for running the codes in R and MatLab 
1.	R -code
R scripts that are provided are for loading the data, perform the PCA analysis and the unsupervised clustering as discussed in the Online Methods Section. We provide two scripts in R, one for the 3 state analysis case (HSC, LMPP & PreMegE) and one for the whole dataset; “mainScript_HLP.R” and “mainScript_wholeDataSet.R” respectively.
In each script file, we state in the form of comments, the figures from the manuscript that are reproduced, the analysis taken place, the dependencies required and how to install them. 
The input data for either case (3 states or whole dataset) are located In the R code/Data folder.  
2.	MatLab –code
The scripts provided are for reproducing the results that follow the cell clustering into states. Specifically, those scripts have been developed to implement the formation of the trajectory of cells in the probability space, the identification of key-player genes, μstates definition and gene regulatory network inference with genie3 algorithm. Details on all methods implemented can be found in the Online Methods Section. 
In order to run the 2 main scripts (, one for the 3 state analysis case (HSC, LMPP & PreMegE) and one for the whole dataset), one should download and “add to path” from within MatLab (right click on the folder and “Add to Path/Selected Folder and Subfolders”) the following 3 toolboxes:
1.	http://www.cs.ubc.ca/~murphyk/Software/BDAGL/. Visualization toolbox for directed acyclic graphs. 
2.	http://www.montefiore.ulg.ac.be/~huynh-thu/GENIE3.html. Genie3 Algorithm: MatLab implementation. 
3.	https://www.mathworks.com/matlabcentral/fileexchange/23661-violin-plots-for-plotting-multiple-distributions--distributionplot-m-. Violin plot toolbox.
After adding those toolboxes into MatLab’s path, one should either run “mainSubPop_GRNs_HLP.m” for the analysis of the 3-state (HSC, LMPP, PreMegE) dataset or “mainSubPop_GRNs_WholeDataset.m” for the complete dataset. 
By running either file, in the pop-up window the user should indicate the folder where the three csvs files exported from the R-code, are located. This will load into MatLab the PCs, posteriors and expression values of each cell of the dataset. Then the user is prompted to input the “starting” state and the “destination” state for the state transition under consideration (in the 3 state case the starting case is HSC and the destination is LMPP). In the case of taking under consideration the complete dataset, all cases should be considered. After that, an excel file is created in the working directory which contains all the information of the constructed trajectory. The user has to input the corresponding filename into the MatLab’s Comand Window when asked and then the analysis continues towards μstates’ definition, “key-player” genes identification and finally GRNs’ for each microstate reconstruction.  



