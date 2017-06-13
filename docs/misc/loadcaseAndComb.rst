A ```LoadCase``` defines the group of loads. For example, in structure below there is a "dead" load and a "live" load, alwo two "earthquake" loads, one in X and other in Y direction:
TODO IMAGE
A LoadCase have a nature (an enum type) and a title (string). LoadNature can be:
Dead, Live, TODO (ADD)

So there can be three LoadCases:
	- case 1: Nature = Dead, Title = "D1"
	- case 2: Nature = Live, Title = "L1"
	- case 3: Nature = Quake, Title = "Qx"
	- case 4: Nature = Quake, Title = "Qy"

To make the model:

```
TODO
```

all loads in BFE should inherit from NodalLoad or ElementLoad. Both of these loads have a property named LoadCase property of type ```LoadCase```. So every load in BFE will
have the LoadCase property. In other hand to get analysis result of model - like internal force on elements, or nodal displacements or support reactions - a parameter of type LoadCombination
should pass to the appropriated method.
For example to get internal force of bar element, this method should be called:

```BarElement.GetInternalForceAt(double x, LoadCombination combination);```

Or to get support reaction of a node, this method should be used:

```Node.GetSupportReaction(LoadCombination combination);```

A ```LoadCombination``` in a list of LoadCases with a multiplier for each one. Internally it does uses ```Dictionary<LoadCase,double>``` to keep the list. 
For example if want to find support reaction for node n3 with loadCombination D + 0.8 L:

``` TODO fix typos if any
var case1 = new LoadCase(LoadNature.Dead,"D1");
var case2 = new LoadCase(LoadNature.Live,"l1");
var case3 = new LoadCase(LoadNature.Quake,"Qx");
var case4 = new LoadCase(LoadNature.Quake,"Qy");

var combination1 = new LoadCombination();// for D + 0.8 L
combination1[case1] = 1.0;
combination1[case2] = 0.8;

var n3Force = model.Nodes["N3"].GetSupportReaction(combination1);
Console.Writeline (n3Force);
```