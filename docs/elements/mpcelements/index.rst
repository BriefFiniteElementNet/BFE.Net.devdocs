MPC Elements
****************

.. toctree::
    :titlesonly:
    :hidden:
    :maxdepth: 2

    rigid/index
    telepathy/index
	
MPC elements or Multi-Point Constraint elements, are kind of virtual elements that binds several DoFs of a model together and reduces the overall number of independent DoFs using technique MPC (Multi-Point Constraints).
Best example is ```TelepathyLink``` that can bind DoFs of several nodes together. For example this model have 8 DoFs:

TODO Picture

So K and Delta matrices will be 8x8 and 8x1.

TODO

Overview of special elements available:
	- ``TelepathyLink``
	- ``RigidElement``
	
for more info see: https://mashayekhi.iut.ac.ir/sites/mashayekhi.iut.ac.ir/files//files_course/lesson_16.pdf