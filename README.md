
# Two-Stage Differential Amplifier Layout  – Cadence Virtuoso Flow
### Technology: UMC 180nm 
### Tool: Cadence Virtuoso
A two-stage differential amplifier layout typically consists of a differential input stage, a gain stage, and an output stage, often with a current mirror for biasing and compensation for stability
### Schematic Design (From the designer) 
o Designed a two-stage differential amplifier in the Schematic Editor.
o Devices include differential pair, current mirror with appropriate sizing.     
o Verified schematic connectivity and saved for simulation and layout.
# Implementation Steps of Layout
### 1. Floor planning
o	Created floorplan to allocate placement regions for the blocks (input pair, current mirror, output stage).        
o	Ensured symmetry and optimal routing paths were considered.    
o	Defined boundary and reserved area for routing and supply rails.
### 	2. Device Placement 
o	Placed transistors and matched devices (M1, M2) symmetrically.        
o	Grouped current mirrors and biasing transistors.    
o	Ensured minimal parasitic mismatch using common-centroid and interdigitated placement where needed. 

### 3. Routing
o	Connected all devices manually with metal layers (M1-M3) ensuring minimal crossovers.    
o	Inserted vias, pins, and contacts with proper DRC-safe spacing.
### 4. DRC (Design Rule Check)
o	Performed DRC verification using Cadence Assura    
o	Result:  No DRC Errors Found
### 5.LVS (Layout Versus Schematic) 
o	Run LVS to ensure layout matches schematic     
o	0 Net/Pin/Device Mismatches; Schematic and Layout match completely.
### 6.Parasitic Extraction (PEX) 
o	Extracted layout parasitics including capacitances and resistances.       
o	Generated extracted view and netlist with parasitic elements.    
o	This data is used for post-layout simulation to evaluate real-world performance degradation due to layout parasitics.
### 5.LVS (Layout Versus Schematic) 
o	Run LVS to ensure layout matches schematic     
o	0 Net/Pin/Device Mismatches; Schematic and Layout match completely.
### 7.Post-Layout Simulation 
o	Used the extracted view generated after LVS and PEX for post-layout simulation.     
o	Imported parasitic netlist into ADE (Analog Design Environment) and ran transient, DC, and AC simulations        
o	Compared pre-layout vs post-layout performance metrics.

## Outcome
•	Achieved a DRC/LVS-clean layout of a two-stage differential amplifier.       
•	Applied key layout techniques such as symmetry, matching, and common-centroid placement.
#### Differential Amplifier Schematic

![App Screenshot](https://via.placeholder.com/468x300?text=App+Screenshot+Here)

