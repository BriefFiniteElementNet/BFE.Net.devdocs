Geometrial Cross Section properties for bar element
===================================================
BarElement.CrossSection does define a cross section for our bar element.
the type ```BaseBarElementCrossSection``` is base class that is used for defining a cross section for bar element. This class is a general class which can give us every information needed for stiffness matrix.
All other geometric properties of bar section are inherited from this class

UniformParametricBarElementCrossSection
=======================================
This class is inherited from ``BaseBarElementCrossSection`` and defines a uniform section for the bar element. Uniform section means that geometry shape of section does not change along the length of bar.
Parametric means that properties are parametrically defined. for example if we have a H section, with Iy = Iz = J = 1e-6 m^4, A = 2e-6 m^4 then:

.. code-block:: cs
   var section = new UniformParametricBarElementCrossSection();
   section.A = 1e-4;
   section.Iy = section.Iz = section.J = 1e-6;

Note that two properties of Ay and Az, are about shear areas of section and they will not be used unless BarElement have behaviour of ```TimoshenkoBeam``` that takes the shear areas into consideration.
If bar element does not have this behaviour, then ```Ay``` and ```Az``` properties will not be used in core library calculations and it doesn't matter if they are ```0.0``` or any other value.