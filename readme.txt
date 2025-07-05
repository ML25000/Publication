==================================================================
DATA AND CODE FOR: "Climate-Responsive Urban Morphogenesis: Real-Time Thermal Comfort Optimization by Synchronizing Wind and Solar Simulation in Grasshopper and Ansys Discovery Live "
==================================================================

Version: 1.0
Date: July 05, 2025
Authors: BOUNNAH Amel, BOURBIA Fatiha
Contact: amel.bounnah@univ-constantine.dz

This repository contains the data, code, and simulation models that support the findings of the aforementioned manuscript. This material is provided 'as-is' for research, verification, and educational purposes.

--------------------------
1. SOFTWARE REQUIREMENTS
--------------------------

To run the simulations and use the provided files, the following software and versions are required:

- Rhinoceros 3D: Version 7
- Grasshopper: Version 1.0.0007 (standard with Rhino 7)
- Ansys Discovery Live: Version 2019 R3
- Ladybug Tools for Grasshopper: Version [e.g., 1.5.0]
- Grasshopper plugins: Opossum, Human, Fennec, Wizard, Ladybug tools
- The Ansys plugin

--------------------------
2. FOLDER STRUCTURE
--------------------------

The repository is organized into the following folders:

- /Code:
  - AnsysGH.ghpy: The custom-built plugin connecting Grasshopper to Ansys.
  - Urban_Morphogenesis_Main.gh: The main Grasshopper script for the optimization process.
  - Optimisation.scdoc: the Ansys Discovery Live file

- /Data_Input:
  - Batna_Site_Base_Model.3dm: The initial Rhino 3D model of the urban site (embeded in the grasshopper file with the "internalise data" feature)
  - DZA_Batna.082010_IWEC.epw: The EPW weather file for Batna, Algeria used for the simulations.

- /Data_Output:
  - Optimization_Results: A  file containing the final set of optimized solutions, including building heights, rotations, and corresponding UTCI values.

--------------------------
3. HOW TO RUN THE SIMULATION WORKFLOW
--------------------------

Please follow these steps to reproduce the optimization workflow:

1. **Setup:**
   - Ensure all software listed in Section 1 is correctly installed.
   - Place the `AnsysGH.ghpy` file in your Grasshopper Components folder. (Typically found at: C:\Users\[YourUsername]\AppData\Roaming\Grasshopper\Libraries)
   

2. **Running the Script:**
   - Open the Grasshopper script `Urban_Morphogenesis_Main.gh` from the `/Code` folder.
   - **Important:** Inside the Grasshopper script, locate the "File Path" component for the weather data and ensure it correctly points to the `DZA_Batna.082010_IWEC.epw` file in your `/Data_Input` folder.
   - The entire optimization process is managed through Grasshopper's Remote Control Panel (RCP) for a user-friendly experience.
   - Activate the RCP. This will open a floating window where you can you can click on the key parameters, and start the optimization.
   - Activate the optimization solver Opossum to start the simulation process. The workflow will begin generating, simulating, and evaluating urban forms in real-time.

--------------------------
4. CITATION
--------------------------

If you use this code, data, or methodology in your research, please cite the following paper:

 BOUNAH Amel et al. (2025). "Climate-Responsive Urban Morphogenesis: Real-Time Thermal Comfort Optimization by Synchronizing Wind and Solar Simulation in Grasshopper and Ansys Discovery Live". Building and Environment (under review).

--------------------------
5. LICENSE
--------------------------

This work is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.
