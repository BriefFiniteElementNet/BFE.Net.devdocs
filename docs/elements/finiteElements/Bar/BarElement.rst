BarElement
==========
A bar element is referred to an 1D element, which only have dimension in one direction:
- It can act as frame, beam, truss or shaft by setting the ``BarElement.Behaviour`` property.
- It can have a cross section by setting the ``BarElement.CrossSection`` property.
- It can have a material by setting the ``BarElement.Material`` property.
- Several types of loads are possible to be apply on them.
- It Does have a local coordination system, apart from global coordination system.
- It is possible to find internal force of it.

.. toctree::
    :titlesonly:
    :hidden:
    :maxdepth: 2

    BarElement_behavs
    BarElement_geos
    BarElement_mats
    BarElement_loads
    BarElement_coords
    BarElement_internalforces