# Cluster
A local copy of CLUSTER module, Mirplan and DUPLEX module - plant miRNA software


##SMART TOOLS
============
University of Plovdiv, Dept. Molecular biology, SMART - bio2server.bioinfo.uni-plovdiv.bg

##CLUSTER module (cluster.jar)
~~~~~~~~~~~~

Requirements - Java
USAGE: java -jar clusters.jar sRNA.gff 1 2 3 4

sRNA.gff - GFF file for sRNAs genomic coordinates
1) maximum sRNA cluster size; 
2) minimum size of the window between the two clusters; 
3) the length of the sequences flanking the two clusters that should be free of sRNAs;
4) maximum size of the sequence containing the two clusters (putative foldback sequence) 
  

##MIRPLAN module (mirplan.pl)
~~~~~~~~~~~~

Requirements - Perl, Bioperl, RNA Vienna package v1.8 (RNAfold, Hofacker et al. 2009)
USAGE:perl mirplan.pl file.fasta file.out

file.fasta - sequences in FASTA format
file.out   - output file (contains sequence names which meet miRNA plant precursor criteria, along with free energy value, CG%, seq lenght and folding structure)
file.out.fasta - output file with FASTA sequences

	
##DUPLEX module  (duplex.pl)
~~~~~~~~~~~~~

Requirements - Perl, Bioperl, RNA Vienna package v1.8 (RNAcofold, Hofacker et al. 2009)
USAGE: perl duplex.pl sRNA.gff file.out.fasta [table_file] file.out


sRNA.gff - GFF file for sRNAs genomic coordinates
file.out.fasta - sequences in fasta format from MIRPLAN module
[table_file] - optional tabular file containing sRNA sequences and their corresponding read number
file.out - output file (containing precursor sequence with the two sRNA clusters and predicted sRNA duplexes, with their free energy, seq length and seq reads number)

***
Please cite our paper: "Implementation of a de novo genome-wide computational approach for updating Brachypodium miRNAs" 
Baev V, Milev I, Naydenov M, Apostolova E, Minkov G, Minkov I, Yahubyan G. Genomics. 2011 Feb 28. [Epub ahead of print] PMID: 21371551 http://www.ncbi.nlm.nih.gov/pubmed/21371551***
