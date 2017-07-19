TriangleElementNEW
==================

Overview
--------
A triangle element is referred to a 2D element, which only have dimension in two direction. It's features in an quick overview:

1. It can act as thin shell, thick shell, plate bending or membrane - see :ref:`TrignaleElement-Behaviour` section.

.. |pic1| figure:: ../images/tri-full.png
   :align: center
   :width: 45%
   
   DoFs of ``TriangleElement`` acting as a Shell

.. |pic2| figure:: ../images/tri-membrane.png
   :align: center
   :width: 45%
   
   DoFs of ``TriangleElement`` acting as a Membrane
   
   
2. It can have a cross section - see :ref:`TrignaleElement-CrossSection` section.
3. It can have a material - see :ref:`TrignaleElement-Material` section.
4. Several types of loads are possible to be apply on them - see :ref:`TriangleElement-ApplicableLoads` section.
5. It Does have a local coordination system, apart from global coordination system - see :ref:`TriangleElement-CoordinationSystems` section.
6. It is possible to find internal force of it - see :ref:`TriangleElement-InternalForce` section.

.. toctree::
    :titlesonly:
    :hidden:
    :maxdepth: 2

    behavs
    geos
    mats
    loads
    coords
    internalforces