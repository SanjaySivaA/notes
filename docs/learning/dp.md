---
title: "DNA-Protein interaction"
---

**Date**: 11/12/2025 

## Index

1. [Inside a PDB file](#inside-a-pdb-file)
2. [About the specific experiment](#about-the-specific-experiment)
3. [Notes](#notes)

**Aim**: No idea, right now trying to come up with code to calculate distance between atoms from some protein database.  

    Mathematically defining binding site based on atomic distance by treating biological molecules as geometric data points.  

<a id="inside-a-pdb-file"></a>
## Inside a PDB file
    * Structure : Represents the entire outcome of the experiment. Contains everything in the 'test tube' - protein, DNA, water molecules, ions etc.  

    * Model : Not quite clear on this one. In X-ray crystallography the protein is frozen. So there is only one model.
              But if it is say NMR Spectroscopy the protein can move which gives rise to multiple models.

    * Chain : The covalently bonded molecules. List of objects identified by their ID's like 'A', 'B'...
              eg: protein(polypeptide chain), dna(polynucleotide chain).

    * Residue : Protein residues(amino acids) and dna residues(A, C, G, T).  

    * Atom : ...

    Metadata is stored in `structure.header` dictionary.

    The *REMARKS* section mentions specific details about the experiment like error estimates, equipment/method used.
    
    Bio.PDB creates the structure, model, chain, residue and atom objects after parsing the file.

    |Col|Content|Bio.PDB Object Created/Updated|Explanation|
    |:---|:---|:---|:--|
    |1-4|ATOM|Type Check|"Tells parser: ""This is a real piece of the molecule."""|
    |7-11|1|Atom.serial_number|Unique ID of the atom in the file.|
    |13-16|O5'|Atom.name|The Dictionary Key. This is the Oxygen at the 5' end.|
    |18-20|DT|Residue.resname|"""Deoxy-Thymidine"" (DNA T)."|
    |22|E|Chain ID|"The parser looks for Chain['E']. If it doesn't exist| it creates it."|
    |23-26|1001|Residue ID|"The parser looks for residue 1001 inside Chain E. If not found| it creates Residue['1001']."|
    |31-54|25.930...|Atom.coord|"A NumPy array [x| y| z]. This is what you subtract to get distance."|
    |77-78|O|Atom.element|Tells the parser this is Oxygen (for mass calc).|

    Atoms have attribiutes that specify which residue that they belong to and what the type of residue is. eg: Heteroatoms
    Explicit non-standard bonds.

<a id="about-the-specific-experiment"></a>
## About the specific experiment

Apparently p53, the protein in the specific **PDB** file that I first saw(1TUP) is a pretty important protein. Functions include 'turning on'
specific genes, acting as a tumor suppressor. It exists as a tetramer but for the experiments, 3 chains were isolated into the crystal.

This makes 1TUP an excellent dataset for studying Binding, but a bad dataset for studying Oligomerization (how the 4 pieces stick together).

<a id="notes"></a>
## Notes

- Seaborn works on top of matplotlib so will have to import matplotlib while working with seaborn