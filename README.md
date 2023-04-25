# EBSysMLSec

EBSysMLSec is a translation tool that takes a SysML model as an input and generates the corresponding Event-B model.
The tool is used only in the context of networked control system (NCS) i.e., the input must agree with a specifc style of modeling adopted for specifing a NCS using SysML, details could be found in papers [1,2]. 

To develope EBSysMLSec, we use ATL- a model transformation language.  ATL provides a way to genrate several target models from a sorce model. An ATL transformation program consists of several rules that specify how source model elements are matched with target model elements. The implemenation of EBSysMLSec contains four programs (.atl files). Each program takes the input SysML model and generates an Event-B component (either a Machine or a Context). All generated Event-B components form the output of EBSysMLSec. 


Run:
1)	Install Eclipse modeling tool. 
2)	Install ATL plugin.
3)	Create an Atl project
4)	For each program, create an atl file. Creating the file, choose UML ecore as an input metamodel and eventbcore as an output metamodel. UML metamodel exists as a registered package, but eventbcore need to be downloaded from https://sourceforge.net/projects/rodin-b-sharp/files/.
5)	For each program, configure a run and specify the input SysMl model and an directory for the generated .xmb model. An example of input model is provided in the repository (MovingBlockSysml).
6)	Run the configurations and open the generated files with rose editor in Rodin. 
7)	Specify the refinemnt chain.
