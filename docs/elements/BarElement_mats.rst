Material properties for bar element
===
BarElement.Material does define a material for our bar element.
the type ```BaseBarMaterial``` is base class that is used for defining a material for bar element. This class is a general class which can give us every information needed for stiffness matrix. All other materials of bar section are inherited from this class

UniformParametricBarElementCrossSection
===
This class is inherited from ```BaseBarMaterial``` and defines a uniform material for the bar element. Uniform material means that material does not change along the length of bar.
Parametric means that properties are parametrically defined (like ```UniformParametricBarElementCrossSection.E``` and ```UniformParametricBarElementCrossSection.G```).
for example if we have a steel material, with E = 210 GPa, G = 80 GPa then:
```
var steelMaterial = new UniformParametricBarElementCrossSection();
steelMaterial.E = 210e9;//210 * 10^9 Pas
steelMaterial.G = 80e9;//80 * 10^9 Pas
```


