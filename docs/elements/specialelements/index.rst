Special Elements
****************

Special elements are kind of virtual elements that binds several DoFs of a model together and reduces the overall number of independent DoFs.
Best example is ```TelepathyLink``` that can bind DoFs of several nodes together. For example this model have 8 DoFs:

TODO Picture

So K and Delta matrices will be 8x8 and 8x1.

TODO