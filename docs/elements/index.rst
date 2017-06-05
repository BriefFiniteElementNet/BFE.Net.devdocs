Elements Available
==================

.. toctree::
    :titlesonly:
    :hidden:
    :maxdepth: 2

    BarElement
    TriangleElement
    TetrahedronElement

There are two types of elements available in BFE:
	- Normal Elements: Phisical elements that provide stiffness, mass and damp matrices.
	- Special Elements: Some kind of virtual elements that usually act as a rigid (infinite stiffness) connection (a connection that strictly binds two or more DoF together)

There are several elements available in `BriefFiniteElement` library:
	- BarElement: A 1D, 2 noded element
	- TriangleElement: A 2D, 3 noded element
	- TetrahedronElement: A 3D, 4 noded element
