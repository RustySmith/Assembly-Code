# Assembly-Code
Template for Visual Studio Assembly Language Project
This project was created in order to make a Visual Studio template for MASM projects.
It includes a Main.asm file with some model code. This code does nothing, but can be assembled and run.
Additional code can be added to the model as desired.
To get Visual Studio to invoke the MASM macro-assembler, two things were done:
	1. The Build Customization for masm was selected. This can be changed by right-clicking on the project name in the Solution Explorer, selecting Build Dependencies->Build Customization, then selecting or de-selecting masm from the list.
	2. Under Debug->Properties->Linker->Advanced, the entry point was set to "main". This allows processing to begin at the first line of a routine named "main" The "main" routine is in the Main.asm file.
To get the model code to run, one additional change needs to be made:
In the menu bar, set the Solution Platforms field to x64, not x86.
In order to create a template in VS, open the project in VS, then select Project->Export Template.
When I create a project in VS using this template, I have to select "All Languages" and scroll to the bottom of the list to find the template.
