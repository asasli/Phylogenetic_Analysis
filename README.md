# Phylogenetic Analysis

## A) COVID-19 COMPLETE GENOME (Greece: Athens)

### 1. Extracting the data

Data is extracted from [NCBI for VIRUS COVID-19](https://www.ncbi.nlm.nih.gov/labs/virus/vssi/#/virus?SeqType_s=Nucleotide&VirusLineage_ss=Severe%20acute%20respiratory%20syndrome%20coronavirus%202,%20taxid:2697049&Country_s=Greece). The downloaded data concernes Nucleotide (complete genome) of COVID-19 from different patients submitted from Athens, Greece. The accession numbers which are to be used for the fylogenetic analysis are
* MT459832
* MT459833
* MT459834
* MT459835
* MT459836

### 2. Compute the distance between the sequences

*Assumptions *
* No coding parts are included
* Jukes-Cantor model: real distance is given by the form $d=-\frac{3}{4}ln\left(1-\frac{4}{3}D\right)$
* D is the observed distance D=$\frac{miss-matches}{length\quad of\quad the\quad sequence}$ 

### 3. Estimate the Phylogenetic Tree
We use the UPGMA method:
 1. Find the minimum value for the distance D[i,j].
 
 2. Merge sequences i and j.
 
 3. Let x denote the node with wich i, j are conected. Setting L=D[i,j]/2 ensures that elements i and j are equidistant from x.
 
 4. Update the initial distances D. The new matrix has $(N-1)^2$ values and the elements i,j have been replaced by the node x. The new distance between the node x and the others sequences (s) is calculated as $D'[s,x]=\frac{D[i,s]+D[j,s]}{2}$.
 
 5. Repeat.

 ## B) Prostaglandin Synthesis

Data:
* [Bos Taurus (Cow)](https://www.ncbi.nlm.nih.gov/nuccore/198282106)
* [Ovis aries(Sheep)](https://www.ncbi.nlm.nih.gov/nuccore/57164168)
* [Rattus norvegicus (Rat)](https://www.ncbi.nlm.nih.gov/nuccore/415637)
* [Xenopus laevis(Frog)](https://www.ncbi.nlm.nih.gov/nuccore/117307525)
* [Mesochaetopterus taylori ((Marine worm)](https://www.ncbi.nlm.nih.gov/nuccore/933798131)
* [Sus scrofa (Wild pig)](https://www.ncbi.nlm.nih.gov/nuccore/AJ001201.1)
