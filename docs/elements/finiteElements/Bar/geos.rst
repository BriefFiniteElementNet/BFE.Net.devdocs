.. _BarElement-CrossSection:

Cross Section
-------------
``BarElement`` is modelled as a 1D element, and it needs to have geometrical values of it's cross section (like A, Iy, Iz, etc.). ``BarElement.CrossSection`` does define a cross section for ``BarElement``.
The type ``BaseBarElementCrossSection`` is base class that is used for defining a cross section for bar element. This class is a general class which can gives every information of section's geometric properties at specific location of length of element.
All other cross sections of bar element are inherited from ``BaseBarElementCrossSection`` class.

UniformParametricBarElementCrossSection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Inherited from ``BaseBarElementCrossSection``, defines a uniform section for the ``BarElement``. Uniform section means that section does not change along the length of bar.
Parametric means that properties are parametrically defined one by one. 
for example if we have a H section, with Iy = Iz = J = 1e-6 m^4, A = 2e-6 m^4 then:

.. code-block:: cs

   var section = new UniformParametricBarElementCrossSection();
   section.A = 1e-4;
   section.Iy = section.Iz = section.J = 1e-6;
   
   var bar = new BarElement();
   bar.CrossSection = section;

   .. hint::

   Note that two properties ``Ay`` and ``Az`` of ``BaseBarElementCrossSection``, are about shear areas of section and their value will not be used unless BarElement have one of  ```TimoshenkoBeam``` behaviours.