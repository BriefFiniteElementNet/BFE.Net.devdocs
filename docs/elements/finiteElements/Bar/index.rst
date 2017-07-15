BarElement
==========

Overview of ``BarElement``
----------
A bar element is referred to an 1D element, which only have dimension in one direction:

1. It can act as frame, beam, truss or shaft - see :ref:`BarElement-Behaviour` section.

.. figure:: ../images/bar-fullframe.png
   :align: center
   
   DoFs of ``BarElement`` acting as a Frame

2. It can have a cross section - see :ref:`BarElement-CrossSection` section.
3. It can have a material - see :ref:`BarElement-Material` section.
4. Several types of loads are possible to be apply on them - see :ref:`BarElement-ApplicableLoads` section.
5. It Does have a local coordination system, apart from global coordination system - see :ref:`BarElement-CoordinationSystems` section.
6. It is possible to find internal force of it - see :ref:`BarElement-InternalForce` section.

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