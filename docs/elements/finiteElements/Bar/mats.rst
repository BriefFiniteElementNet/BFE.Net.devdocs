.. _BarElement-Material:

Material
--------
``BarElement.Material`` property defines a material for this element.
the type ``BaseBarMaterial`` is base class that is used for defining a material for bar element. This class is a general class which can gives every information of section's materials at specific location of length of element.
 All other materials of bar section are inherited from ``BaseBarMaterial`` class.

UniformParametricBarElementCrossSection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
This class is inherited from ``BaseBarMaterial`` and defines a uniform material for the bar element. Uniform material means that material does not change along the length of bar.
Parametric means that properties are parametrically defined (like ```UniformParametricBarElementCrossSection.E``` and ```UniformParametricBarElementCrossSection.G```).
for example if we have a steel material, with E = 210 GPa, G = 80 GPa then:

.. code-block:: cs
   var steelMaterial = new UniformParametricBarElementCrossSection();
   steelMaterial.E = 210e9;//210 * 10^9 Pas
   steelMaterial.G = 80e9;//80 * 10^9 Pas