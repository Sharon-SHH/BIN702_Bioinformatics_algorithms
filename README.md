

========================================
# Sankoff - Construction of ancestral sequences
========================================

Objectives: The project is to design and implement a program for constructing ancestral sequences to the internal nodes of phylogeny, from phylogeny and sequences to the leaves of the tree.

Methods : 
- Python
- Muscle for sequence alignment
- Method Fitch Sankoff or homology for predicting ancestral sequences

Result: The expected results are input taking program a phylogeny with sequences homologous to the leaves and then returns a set of ancestral sequences associated with internal nodes of phylogeny, so as to minimize the events of mutations on the branches of the phylogeny.

Instruction:

Software Version: Python 2.7
EXE file:
  muscle3.8.31_i86win32.exe
  PhyML-3.1_win32.exe
Input file: C:\BIN702\ input.fasta
My suggestion is that put all python files and EXE file in the same folder. Input data, input.fasta, is put into path: C:\BIN702. Content in input.fasta can be changed, but not the file name. Other output files are automatically generated by source. The final result is in the Ancestral Sequence.txt.

Step 1:
seqToMultiAlignments.py
Environment require: Bipython (pip install biopython), because Bio.Align.Applications is used.
Exe file used: muscle3.8.31_i86win32.exe. 
Input file: input.fasta
Output file: aligned.fasta

Step 2:
phylogeny.py
Exe file used: PhyML-3.1_win32.exe, phyml.bat 
Environment require: Add the path to PhyML to the Windows system path. There's an example of how to do that here: https://java.com/en/download/help/path.xml)
Input file: input.fasta
Output file: phylogeny.txt, phylogeny.txt_phyml_tree.txt, phylogeny.txt_phyml_stats.txt
The input of PhyML-3.1_win32.exe is Phylip format. Therefore, firstly, convert input.fasta into Phylip format and write them into phylogeny.txt. Then generate phylogeny tree which is written in the phylogeny.txt_phyml_tree.txt.

Step 3:
sankoff.py, myPhylogeneticTree.py
Input: aligned.fasta, phylogeny.txt_phyml_tree.txt
Output: Ancestral Sequence.txt


