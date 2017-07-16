.. _TriangleElement-CrossSection:

Cross Section
-------------
``TriangleElement`` is modelled as a 2D element, and it needs to have thickness values of it's cross section. ``TriangleElement.CrossSection`` (TODO: is TriangleElement.CrossSection right?) does define a cross section for ``TriangleElement``.
The type ``BaseTriangleElementCrossSection`` is base class that is used for defining a cross section for triangle element. This class is a general class which can gives every information of section's geometric properties at specific location of surface of element.
All other cross sections of triangle element are inherited from ``BaseTriangleElementCrossSection`` class.

UniformParametricTriangleElementCrossSection
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Inherited from ``BaseTriangleElementCrossSection``, defines a uniform section for the ``TriangleElement``. Uniform section means that section does not change along the surface of trignale.
Parametric means that properties are parametrically defined one by one. for example if we have a section, with thickness = 1 cm then:

.. code-block:: cs

   var section = new UniformParametricTriangleElementCrossSection();
   section.Thickness = 0.01;
   
   var tri = new TriangleElement();
   tri.CrossSection = section;