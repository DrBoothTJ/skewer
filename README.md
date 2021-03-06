# skewer
A simple script for generating GC-Skew plots from DNA sequences.

## Usage
```
python skewer.py nucleotidesequence.fasta 500 50
```
Where the three arguments are:

1. A '.fasta' or '.gbk' file containing a nucleotide sequence.
2. The window size for the analysis.
3. The step size for the analysis.

It is very important to set an appropriate window and step sizes for the anaylsis. I recommend using a step size that will result in around 1,000 steps. E.g. for a sequence of 50 kb use a step size of 50. Ensure that the window size is **at least** the same size as the step. In future versions, `skewer.py` will be able to reccomend appropriate values for you.

The GC plot will be saved as skewer.html in the current directory. A table (.csv) of values will also be saved in the same directory.

## Example Data
Example data and output is provided in the 'example_data' folder. 

This script was origionally made to search for GRINS (genetic repeats of intense nucleotide skews) as described by Nivina et al. in their paper: [GRINS: Genetic elements that recode assembly-line polyketide synthases and accelerate their diversification](https://www.pnas.org/doi/10.1073/pnas.2100751118). As such, I have used the polyketide synthase tylactone as a test case.

The example data contains the input file (a .fasta file containing records for the nucleotide sequences of each gene in the tylactone gene cluster, and a record of the entire sequence of the BGC) and the output files (individual '.html' and '.csv' files for each record in the input file).

## To Do
1. Automatically calculate reccomended step and window sizes,
2. Plot genbank features over the skew plot,
3. Write the resulting data to a .csv file,
4. Add % completeion for longer analyses,
5. Compile into a software package.
