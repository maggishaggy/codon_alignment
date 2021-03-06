Performing codon alignment based on amino acid sequences: codon_alignment.pl

Features:
 - Performing codon alignment for coding sequences (CDS)
 - Multiple alignment with MUSCLE (executable MUSCLE file needs to be added to current directory)
 - Customized the threshold for the percentage of non-gap basepairs in a multiple sequence alignment
 - Two codon tables are supported:
        1 - for The Standard Code;
        5 - for The Invertebrate Mitochondrial Code
        Details please refer to http://www.ncbi.nlm.nih.gov/Taxonomy/taxonomyhome.html/index.cgi?chapter=tgencodes#SG2

Prerequisites:
 - Download MUSCLE (https://www.drive5.com/muscle/downloads.htm) and added the executable file to current directory (i.e. codon_alignment directory).

To run the script: 
perl codon_alignment.pl [cds fas] [codon table id] [minimum coverage]

 - [cds fas] 	    CDS sequences in fasta file
 - [codon table id]    1 for Standard Code, 5 for Invertebrate Mitochondrial Code
 - [minimum coverage]  Minimum coverage of non-gap basepairs in the multiple alignment (range from 0 to 1). 
		    For example: 0.7 means sequences after the first round of multiple sequence alignment should have >= 70% of non-gap basepairs

Example: 
 - Go to the example file directory 
 - cd ./examples
 - Make multiple sequence alignments based on COX1 gene (mitochondrial codon table) and remove the sequences with < 70% non-gap basepairs
 - ../codon_alignment.pl COX1.fasta 5 0.7
