VirtualConstraint
============
``VirtualConstraint`` is an ``MpcElement``, that can fix any free dofs of model. 
Technically there is no difference between using Node.Constraint and VirtualConstraint element in these two version of code, both will have exactly same result after solve:

```

for(var i = 0;i < 10;i ++)
{
	model.Nodes[i].Constraint = Constraints.FixedDx;
	model.Nodes[i].Settlements = new Displacement(0.1,0,0,0,0,0);
}
```

```
var elm = new VirtualConstraint();
elm.Constraint = Constraints.FixedDx;
elm.Settlement = new Displacement(0.1,0,0,0,0,0);

for(var i = 0;i < 10;i ++)
	elm.Nodes.Add(model.Nodes[i]);

model.MpcElements.Add(elm);
	
```
but the second one will let user to define settlements for specific LoadCases.
