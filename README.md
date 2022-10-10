# LAMMPS_Mig_Bar_Energies
This repository contains the Excel sheets used in the machine learning (ML) models for predicting the migration barrier energies in the Manzoor, A., Arora, G., Jerome, B., Linton, N., Norman, B, and Aidhy, D.S., “Machine learning based methodology to predict point defect energies in multi-principal element alloys,” Frontiers in Materials, vol. 8, 2021, pp. 1-15 paper. Each structure that was made for this project was a face-centered cubic (FCC) structure consisting of 864 atoms total. 2052 migration barrier energy calculations were performed for each structure.


Found in this repository are four different folders named: "binaries", "ternaries", "quaternaries", and "quinaries". Each folder will contain an Excel files with multiple sheets specifying the composition of that alloy. 

	In the "binariess" folder, there is one Excel file containing sheets for each of the binary alloys for this project, so NiCu, NiCr, NiCo, FeNi, FeCu, FeCr, FeCo, CrCu, CrCo, and CoCu.
	
	In the "ternaries" folder, there are 8 Excel files with multiple compositions for each of the ternary alloy in separate sheets. There is also an Excel file containing the equiatomic ternary alloy data for each of the ternary alloys.
	
	In the "quaternaries" folder, there are 5 Excel files with multiple compositions for each of the quaternary alloys.
	
	In the "quinaries" folder, there is one Excel file with separate sheets for the compositions the migration barrier energies were calculated for.
	
	


Each Excel sheet will have the same header consisting of: 
	
	Descriptors:
		"Mig_Fe", "Mig_Ni", "Mig_Cr", "Mig_Co", and "Mig_Cu" in that order with a 1 or a 0 in that column, signifying which type of atom is migrating (i.e., if the order of the values in those columns were 1 0 0 0 0, this would specify that it is an Fe atom). 
		
		"RDT", which is the distance between the migrating atom and the vacancy position.
		
		"CNN Vac X a", "CNN Vac X aT", "CNN Vac X b", "CNN Vac X bT", "MNN Vac X a", "MNN Vac X aT", "NNCB Vac X a", "NNCB Vac X aT", "NNCB Vac X b", "NNCB Vac X bT", and "BNN Vac X", for each element type X, following the nomenclature in Figure 1 from the paper. Where CNN Vac = common nearest neighbor to the migrating atom and vacancy site, MNN Vac is the middle nearest neighbor to the vacancy, NNCB Vac is the common back nearest neighbor to the vacancy, and BNN Vac is the back nearest neighbor to the vacancy. The X signifies the type of element in that position, if there is a 1 under "MNN Vac Ni a", this would mean that the atom in that MNN Vac position is a Ni atom and so on for the others. If there is a 0, this signifies that atom type is not present in that situation.
		
		"CNN Vac a dist", "CNN Vac aT dist", "CNN Vac b dist", "CNN Vac bT dist", "MNN Vac a dist", "MNN Vac aT dist", "NNCB Vac a dist", "NNCB Vac aT dist", "NNCB Vac b dist", "NNCB Vac bT dist", and "BNN Vac dist", which give the distances from the vacancy site to the positions listed.
		
		"CNN Vac a sep", "CNN Vac b sep", "MNN Vac a sep", "NNCB Vac a sep", "NNCB Vac b sep", and "BNN Vac sep", which give the distances between the atoms in the listed positions. For example, the "MNN Vac a sep" is the distance between the two MNN atoms surrounding the vacancy site.
		
		"MNN Mig X a", "MNN Mig X aT", "NNCB Mig X a", "NNCB Mig X aT", "NNCB Mig X b", "NNCB Mig X bT", and "BNN Mig X", for each element type X. This follows a similar format as the "CNN Vac X a" as above, but this time it is in relation to the migrating atom.
		
		"CNN Mig a dist", "CNN Mig aT dist", "CNN Mig b dist", "CNN Mig bT dist", "MNN Mig a dist", "MNN Mig aT dist", "NNCB Mig a dist", "NNCB Mig aT dist", "NNCB Mig b dist", "NNCB Mig bT dist", and "BNN Mig dist", which give the distances from the migrating atom to the positions listed.
		
		"CNN Mig a sep", "CNN Mig b sep", "MNN Mig a sep", "NNCB Mig a sep", "NNCB Mig b sep", and "BNN Mig sep", which give the distances between the atoms in the listed positions. For example, the "MNN Vac a sep" is the distance between the two MNN atoms surrounding the migrating atom.
		
			
	Target:
		"EBF Migration barier" is the migration barrier energy in eV for the atom specified in the first set of descriptors

