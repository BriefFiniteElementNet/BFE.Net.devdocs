Finite Elements
***************

.. toctree::
    :titlesonly:
    :hidden:
    :maxdepth: 2

    Bar/BarElement
    Triangle/TriangleElement
    Tetrahedron/TetrahedronElement
	

There are several finite elements available in library. Each finite element does provide stiffness, mass and damp matrices. 
Their difference with special elements is that normal elements does provide stiffness, mass and damp matrices and usually have material, geometrical properties (like section on thickness) but special elements does not so and just binds several DoFs together and reduces the overall independent DoFs.
Elements Are:
	- BarElement: A 1D, 2 noded element
	- TriangleElement: A 2D, 3 noded element
	- TetrahedronElement: A 3D, 4 noded element
	
