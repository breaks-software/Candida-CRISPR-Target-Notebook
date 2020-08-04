# Candida-CRISPR-Target-Notebook
If you want to speed up processing and identification of target gRNA sequences for introduction to Candida species via CRISPR techniques, this Jupyter notebook can help.  After the user fills in a sequence of forms and selects Run all, the code will;
1. pull the full sequence for your target species from the [Candida Genome Database](http://www.candidagenome.org)
1. automatically fill in the form on the [Eukaryotic Pathogen CRISPR gRNA Design Tool](http://grna.ctegd.uga.edu/) (EuPaGDT), submit the request, and collect the potential gRNA sequence targets
1. automatically fill in the form on the [RNAFold Web Server](http://rna.tbi.univie.ac.at//cgi-bin/RNAWebSuite/RNAfold.cgi) for all of the gRNA sequence targets, submits the request, then collect the results,
1. and finally, generate a table that includes the key columns from both sets of results, and download both CSV and HTML versions of the results table.

The nice thing about this is that the notebook does all of the waiting for the different servers for you.  If, for example, the EuPaGDT generates a lot of results that need to be submitted to the RNA Fold Server, you don't have to manually process them one by one.  The notebook does that for you, consolidating the information from both servers into one table.  And if you get the process started then walk away only to return after Google Colab has disconnected you, the notebook as already downloaded the results to your local Downloads directory.

## Requirements
This Jupyter Notebook uses features that are only available in [Google Colaboratory](https://colab.research.google.com/).  For example, we can easily hide code to avoid distraction by using forms.  For this reason, you are encouraged to use the notebook from there.

## Usage
[We assume that you are familiar with using [Jupyter Notebooks](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/What%20is%20the%20Jupyter%20Notebook.html#).]

### Steps in sequence
The first few times you use this, it is best to step through each of the steps in the notebook in sequence.  If there are fields to fill in, ensure that the default values are what you need, or change them to meet your needs before you click on the Run button.

### All at once
After you are familiar with the steps, and the various options you have at each point, you can easily fill in the fields for all of the forms in the notebook, then select to "Run all".

## Citations
If you use this notebook as part of work that is to be published, please add the following citations for the underlying tools to your published work:
* (refer to [How to Cite CGD](http://www.candidagenome.org/HowToCite.shtml) for the Candida Genome Database)
* Duo Peng and Rick Tarleton. EuPaGDT: a web tool tailored to design CRISPR guide RNAs for eukaryotic pathogens. Microbial Genomics. 2015. doi: 10.1099/mgen.0.000033
* Gruber AR, Lorenz R, Bernhart SH, Neuböck R, Hofacker IL. The Vienna RNA Websuite. Nucleic Acids Research, Volume 36, Issue suppl_2, 1 July 2008, Pages W70-W74, DOI: 10.1093/nar/gkn188
* Lorenz, R. and Bernhart, S.H. and Höner zu Siederdissen, C. and Tafer, H. and Flamm, C. and Stadler, P.F. and Hofacker, I.L. "ViennaRNA Package 2.0", Algorithms for Molecular Biology, 6:1 page(s): 26, 2011
