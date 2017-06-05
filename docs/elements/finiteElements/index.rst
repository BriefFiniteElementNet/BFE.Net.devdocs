There are several finite elements in BFE. Each finite element in BFE does provide stiffness, mass and damp matrices. 
Their difference with special elements is that normal elements does provide stiffness, mass and damp matrices and usually have material, geometrial properties (like section on thickness) but special elements does not so and just binds several DoFs together and reduces the overall independent DoFs.
Elements Are:
	- BarElement: A 1D, 2 noded element
	- TriangleElement: A 2D, 3 noded element
	- TetrahedronElement: A 3D, 4 noded element