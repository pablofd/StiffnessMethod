# StiffnessMethod

Estructuras.xlsx => 

You must enter the structure in that file, numbering nodes and bars and taking into account which is the initial node and which is the final node. You can enter stiffnesses, sections and lengths. There are two types of nodes: articulated and rigid (AA, AR, RA, RR). 

In the tab "Displacements" you must enter the allowed displacements in supports, but among the allowed ones, only those that are not free. For example, in an articulated node the rotation is free and would be entered as 0, but if vertical displacements are allowed in that same node, a 1 would be entered. The order is horizontal, vertical, rotation, from node 1. 

In the same file, you must enter the external forces applied on the bars, but calculating the effect on the node. For example, a distributed force on a biaxially braced member has two vertical components at each node. The order is Horizontal, Vertical, Moment, from node 1. The coordinates are those of the member (local reference system), as these calculations are tabulated.  

In the last tab you can include the reactions at the supports (global reference system (X,Y,Z). 


Estructuras.ipynb => 

The program. Just put the xlsx in the same file and run. 

It will calculate the direct stiffness method matrices in each bar, assemble them, pose the system, solve it, give you the displacements, draw you the deformation of the bar and calculate the forces (shear, normal and bending) in each bar, plus the reactions. 

You can use the isolated functions. You can also leave the forces = 0 if you only want the system. The most important step is to introduce the 1 correctly in the displacements and define the system properly. 
