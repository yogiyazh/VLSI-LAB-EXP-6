 # 6.SCHEMATIC ENTRY AND SIMULATION OF CMOS INVERTER, CMOS NAND and CMOS NOR USING CADENCE TOOL

# AIM:
To design and simulate the CMOS inverter and observe the DC and transient responses using cadence tool.

# APPARATUS REQUIRED:
 
1.	Laptop with MobaXterm
2.	Cadence tool

# PROCEDURE
SCHEMATIC ENTRY:
Creating a new library:
1.	In the library manager, execute File - New library. The new library form appears.
2.	In the new library form, type ‘my design lib’ in the name section.
3.	In the field of directory section, verify that the path to the library is set to ~/Database / Cadence- analog – lab –bl3 and click ok.
4.	In the next ‘technology file for new library form select option attach to an existing tech file and click ok.
5.	In the ‘attach design library to technology file’ form, select gpdk045 form the cyclic field and click ok.
6.	After creating a new library you can verify it from the library manager.
7.	If you right click on the ‘my design lib’ and select properties, you will find that gpdk045 library is attached as techlib to ‘my design lib’.

Creating a schematic cell view:
1.	In the CIW or library manager, execute file – new – cell viw.
2.	Setup the new file form as follows, Do not edit the library path file and the above might be different from the path shown in your form.
3.	Click ok when done the above setting. A black schematic window for the inverter design appears.

Adding components to schematic:
1.	In the inverter schematic window, click the instance fixed menu icon to display the add instance form.
2.	Click on the browse button. This opens up a library browser from which you can select components and the symbol view.
3.	After you complete the add instance form move your cursor to the schematic window and click left to place a component.
LIBRARY NAME	CELL NAME
gpdk045	PMOS
gpdk045	NMOS
4.	This is a table of components for building the inverter schematic.
5.	After entering components, click cancel in the add instance form or press ESC with your cursor in the schematic window.
 
![329846201-a2133400-912a-4560-844a-63dad142edba](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/f2943d16-3e2b-43a0-b202-62a7ea620092)

Adding pins to schematic:
1.	Click the pin fixed menu icon in the schematic window. You can execute create pin or press ‘p’.
2.	Add pin form appears. Type the following in the ADD pin form in the next order leaving space between the pin.
PIN NAMES	DIRECTION
Vin,Vdd,Vss	Input
Vout	Output
3.	Select cancel and then the schematic window enter window file or press the f bind key.
Adding wires to schematic:
1.	Click the wire (narrow) icon in the schematic window.
2.	In the schematic window click on a pin of one of your components as the first point for your wiring. A diamond shape appears over the starting point of this wire.
3.	Follow the prompts at the bottom of design window and click left on the destination point for your wire. A wire is routed between the source and destination points.
4.	Complete the wiring as shown in the figure and when done wiring press ECS key in the schematic window to cancel wiring.

Saving the design:
	Click the check and save icon in the schematic editor window observe CIW output for any errors.

# BUILDING THE INVERTER TEST DESIGN:
Creating the inverter test cell view:
1.	In the CIW or library manager, execute file – new – cell view.
2.	Setup the newfile as shown below.
3.	Click ok when done. A blank schematic window for the inverter test design appears.
4.	Using the components list and properties/ comments in this table build the inverter test schematic.
LIBRARY NAME	CELL VIEW NAME	PROPERTIES/COMMENTS
My design lib	Inverter	Symbol
Analog lib	Vpulse	Voltage1 = 0, Voltage2 = 1.8, delay Time = 0,
Rise time=Fall time=1ns
Period=20ns
Analog lib	Vdc, gnd	Vdc = 1.8v
5.	Add the above components using create – instance or by pressing I.
6.	Click the wire (narrow) icon and wire your schematic.
7.	Click create wire name or press c to name the i/p (vsin) and output wires as in below schematic.
8.	Click on the check and save icon to save the design.
 
![329846222-600d6e29-68ad-483b-ab55-41f38b3f10e8](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/582ec2f8-183f-41db-9e49-2bddf1222e53)


# ANALOG SIMULATION WITH SPECTRA:
Starting the simulation environment:
1.	In the Inverter-test schematic window execute launch – ADEL. The variable virtuoso analog design environment (ADE) simulation window appears.
Choosing a simulator:
1.	In the simulation window (ADE) execute setup – simulator / directory / host.
2.	In the choosing simulator form, set the simulator field to specra and click ok.
3.	In the simulation window (ADE) execute the setup model libraries.
To complete, move the cursor and click ok.
Choosing Analysis:
1.	Click the choose- Analysis icon in the simulation window (ADE).
2.	The choosing analysis form appears.
3.	To Setup the transient analysis.
a.	In the analysis section select tron.
b.	Set the stop time as 100ns
c.	Click at the moderate or enabled button and the bottom and then click apply.
4.	To set for DC analysis
a.	In the analysis section select DC.
b.	Turn on save DC operating point.
c.	Turn on the component parameters.
d.	Double click the select Vpulse source or Type V0 (capital V zero).
e.	Select the DC voltage in the select window parameter and click in the form start and stop voltages are 0 to 1.8.
f.	Select the enable button and click apply and then click ok.

Selecting output for plotting:
1.	Execute the o/p’s to be plotted  -select on sschematic in the simulation window.
2.	Follow the prompt at the bottom. Click on the o/p net vout input vin of the inverter. Press esc with the cursor after selecting.

Running the simulation:
1.	Execute the simulation Netlist and run in the simulation window to start the simulation on the icon. This will create the netlist as well as run the simulation.
2.	When the simulation finishes the transient and DC plots automatically will be popped up along with netlist.
 ![329846236-876d3164-cd85-49f3-80fa-23764b6cb3c3](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/5017d6a0-c664-451b-b83b-f00adbb4ad0c)
![329846242-25cba053-8830-463e-846a-3b4ef3b8306a](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/896a10cb-27ef-4390-af38-caf8b4a41bec)



# CMOS NAND GATE
NAND SCHEMATIC
![329846255-5c51bffd-e5ae-4004-af0d-46200931eadb](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/c85c06bf-af07-4ace-afb1-ea931511e80f)

NAND TEST CELL VIEW
![329846258-e29c6825-fa7e-4b55-9751-7f16ca01b1a8](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/3bc4aea8-8259-4a29-bbcc-5c77c57f30f5)

NAND SIMULATION WITH SPECTRA
![329846261-48db1573-0e9b-411e-8e50-7be9eda5a53e](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/f72b5b54-ea38-4b23-b3d0-a89b5ae7505d)



# CMOS NOR GATE
NOR SCHEMATIC
![329846399-536a1620-85d2-4b6a-958c-8fe8ce18f5ef](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/de47bbca-8317-4970-8693-f540ba61dfcd)

NOR TEST CELL VIEW

![329846407-79ef06ef-a3ef-41b1-87a9-c0feeb5e7a3e](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/79b7f7a3-b8a2-482d-a606-bea906b1575c)

NOR SIMULATION WITH SPECTRA
![329846431-2e1ccaef-1a37-403f-b200-8b6b248db6a9](https://github.com/yogiyazh/VLSI-LAB-EXP-6/assets/159939338/ed3d9510-0def-47c2-82ee-b49535bd29d3)

# Result:
Thus the schematic entry and simulation OF CMOS INVERTER, CMOS NAND and CMOS NOR using cadence tool is done and verified.
