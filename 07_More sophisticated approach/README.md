Part 2: More sophisticated approach
--------------------------------------

In part 1 I used an overlap definition of 1 bp (default setting) to identify genes associated with the peak regions. However, the peaks could be broad, so instead, in order to get a more meaningful definition, we could identify the genes that overlap where most of the reads are concentrated, the peak summit. I will use the information on the position of the peak summit contained in the original peak file and check for overlap of the summits with genes.

Create peak summit file
--------------------------------------

I need to generate a new BED file from the original peak file that contains the positions of the peak summits. The start of the summit is the start of the peak (column 2) plus the location within the peak that has the highest hypothetical DNA fragment coverage (column 5, rounded down to the next smallest integer because some peak summits fall in between to bases). As the end of the peak region, I will simply define start + 1.

Get gene names
-------------------------

The RefSeq genes we downloaded from UCSC did only contain the RefSeq identifiers, but not the gene names. To get a list of gene names in the end, we use another BED file from the Data Libraries.
Hands On: Data upload
Import mm9.RefSeq_genes_from_UCSC.bed from Zenodo or from the data library:
https://zenodo.org/record/1025586/files/mm9.RefSeq_genes_from_UCSC.bed

Repeat workflow
----------------------

It’s time to reuse the workflow I created earlier
https://galaxy-main.usegalaxy.org/u/shunanda_sharkar/h/galaxy-introduction-part-2-peak-to-gene
