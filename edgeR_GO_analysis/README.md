This file contains the details described in my email to you for each file:

First - I parsed out which of those samples are outliers. It's one control and one exposed sample from family 1, so I removed them and re-ran the initial steps. I've attached two images here. allsamples_mds is prior to removing those outliers (there's a legend this time!:) ) and removeoutliers_mds is what it looks like when I remove those family 1 samples. I think it looks a little better? 

# Some initial results for you to ponder:

## GO analysis

TOL.SUS_GOcategories.csv = GO terms that are significantly over or under expressed in tolerant vs. susceptible animals. From my understanding, this does not use the significance values from the edgeR results directly, as it looks for "whether each GO category is significantly enriched by either up or down-regulated genes" (more on that [here](https://github.com/z0on/GO_MWU/blob/master/README.md) under "How it works", I'm still trying to wrap my brain around it a bit). 

TOL.SUS_GOcategories_tree = a graphical representation of those significant GO categories. Info on how to interpret the tree can be found [here](https://github.com/z0on/GO_MWU/blob/master/README.md) under "The output". 

I can repeat all of this in any combination (i.e. for individual families). When I did so for family 16, there are TONS of DE genes (459 up, 238 down) and a tom of Go terms (222 vs displayed in a tree like I have for TOL.SUS but that one only has 101 terms). 

## DE genes 
TOL.SUS_sigDEgenes.csv = Significantly up (1) and down (2) regulated genes between tolerant and susceptible animals (taking into account exposed vs. control). This result is new since I removed those outlier samples. 

A different approach:
I've only done this for tolerant families so far, but I calculated significant DE genes for each family (1, 16, and 33) between control and exposed and found genes that were significant for all three. I then did an NCBI search for what those genes are, and make a spreadsheet (TOL_commonDEgene_functions.xls). Look at the "GeneFunctions_sorted" tab for info on log fold change and p-values for each family, as well as what the gene is designated as in NCBI.

