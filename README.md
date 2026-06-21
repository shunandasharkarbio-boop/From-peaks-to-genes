# From-peaks-to-genes

I stumbled upon a paper (Li et al. 2012) called “The histone acetyltransferase MOF is a key regulator of the embryonic stem cell core transcriptional network”. The paper contains the analysis of possible target genes of an interesting protein called Mof. The targets were obtained by ChIP-seq in mice and the raw data is available through GEO. However, the list of genes is neither in the supplement of the paper, nor part of the GEO submission. The closest thing we could find is a file in GEO containing a list of the regions where the signal is significantly enriched (so called peaks):

1	3660676	3661050	375	210	62.0876250438913	-2.00329386666667
1	3661326	3661500	175	102	28.2950833625942	-0.695557142857143
1	3661976	3662325	350	275	48.3062708406486	-1.29391285714286
1	3984926	3985075	150	93	34.1879823073944	-0.816992
1	4424801	4424900	100	70	26.8023246007435	-0.66282
Table 1 Subsample of the available file

The goal of this exercise is to turn this list of genomic regions into a list of possible target genes.


Agenda
------------------

In this tutorial, I will deal with:

-Pretreatments
-Data upload
-Part 1: Naive approach
File preparation
Analysis
Visualization
Extracting workflow
-Part 2: More sophisticated approach
Preparation
Create peak summit file
Get gene names
Repeat workflow
Share my work -0https://galaxy-main.usegalaxy.org/u/shunanda_sharkar/h/from-peaks-to-genes
