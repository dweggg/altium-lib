Changelog: 
Date			   Author			Version					Changes
18-02-2026		AS				   1.0						Document Creation	


Rules for MasterLibrary
%----------------------%

1. Create a separate branch when new components need to be created.
   Name of the branch should be associated with the project.

2. Create a review sheet and carry out peer review before merging.

3. Things to review columns

   3.a To be filled by Schematic and Footprint Designer
       Design Item ID;
       Manufacturer;
       Manufacturer Part Number;
       Designators;
       Comment;
       Description;
       Footprint;

   3.b To be reviewed by Reviewer
       Footprint Link;
       Design Item;
       Footprint;
       Manufacturer;
       Manufacturer Part Number;
       Sch Sym.;
       Review Status;
       Reviewer;

4. Reviewer needs to verify:
       Naming convention follows MasterLibrary guidelines;
       Values and units are correct;
       No illegal characters;
       No underscore used;
       No R/C/L prefix in component name;
       Footprint matches datasheet;
       Pin mapping is correct;
       Designator type is correct;

5. Only after all checks are completed and Review Status is APPROVED,
   the symbol and footprint can be added to the MasterLibrary main branch.

6. Footprints must be reused.
   Do not create new footprints for identical packages.
   Duplicate footprints are not allowed.





Designator Assignment Convention
%--------------------------------%

| Component Type | Designator  | Example |
| -------------- | ----------  | ------- |
| Resistor       | R?          | R15     |
| Capacitor      | C?          | C7      |
| Inductor       | L?          | L3      |
| Diode          | D?          | D2      |
| MOSFET / BJT   | Q?          | Q4      |
| IC             | U?          | U1      |
| Connector      | J?          | J1      |
| Test Point     | TP?         | TP3     |
| Fuse           | F?          | F1      |
| Crystal        | Y?          | Y1      |
| Switch         | SW?         | SW1     |



Component Naming Convention: 
%----------------------------%

Resistor:
---------
*Syntax: 
	<Value> <Tolerance> <Power> <Package> 

*Sufix: 
	mOhms		-	XXXL 
	kiloOhms	- 	XXXK

*Examples:
	1L 0.1% 3W 3512 
	0R 0.25W 1206
	4R7 5% 0.25W 0402
	10K 1% 1/4W 1206
	1M 0.1% 1W 3512

Capacitor:
-----------
*Syntax: 
	<Value> <Tolerance> <Voltage> <Di-Electric> <Package> 

*Sufix: 
	pico farad 	- XXXpF 
	Nano Farad 	- XXXnF
	micro Farad	- XXXuF

*Examples: 
	47nF 10% 100V X7R 0805
	1uF 10% 100V X7R 1206
	1uF 10% 500V X7R RAD

Inductor:
---------
*Syntax
	<Value> <Tolerance> <Current Rating> <DC Resistance> <Package>

*Sufix: 
	nano Henry 	- 	XXXnH
	micro Henry - 	XXXuH
	milli Henry	- 	XXXmH
	
*Examples:
	10uH 10% 0.1A 360L 0805
	1mH 20% 10A 3L TH


Integrated Circuit : 
--------------------
*Syntax
	IC: <MPN> 

*Example: 
	IC: TJA1050T

Operational Amplifier: 

OPAM:
----- 
*Syntax
	OPAM: <MPN>

*Examples: 
	OPAM: TL081HIDR

Modules : 
---------
*Syntax
	MOD: <MPN>
	
*Examples: 
	MOD: TSR 1-2450E


Connector: 
----------
*Syntax
	CON<PIN_COUNT>: <MPN>

*Examples: 
	CON2: 282837-2


Diodes: 
-------
*Syntax
	<Type> <Vr Voltage> <If_Max/Power> <Package>

*Type: 
   ZD -  Zener Diode
   SD -  Schottky Diode
   D  -  General Diode

*Examples: 
	D 1kV 1A SOD-123-FL2
   ZD 10V 0.2W SOD-323F


	
	
	
Footprint Naming Convention
%---------------------------%

IPC7351B Needs to Followed