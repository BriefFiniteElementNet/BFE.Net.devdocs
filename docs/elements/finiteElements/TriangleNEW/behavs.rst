.. _TrignaleElement-Behaviour:

Behaviours
----------
``TriangleElement.Behaviour`` property is an enum flag (enum flag  means an enum that can have several values at same time). It can be set to ThinShell, TODO etc. 
The possible behaviours for the TriangleElement is:

- ``BarElementBehaviour.EulerBernoulyBeamY`` : Beam in Y direction based on Euler-Bernouly theory. DoFs are shown in below image:
.. figure:: ../images/bar-b1.png
   :align: center
   
   DoFs of ``BarElementBehaviour.EulerBernoulyBeamY``
   
These behaviours can be combined , for example a Membrane member should only have a Membrane behaviour, but a thin shell member does have behaviour of platebending and a membrane behaviour (both at the same time).
 
This is an example which makes a TriangleElement with plate bending behaviour which in real acts as a plate bending member that only can carry normal loads and in plate bendings:

.. code-block:: cs
   
   var tri = new TriangleElement();
   tri.Behaviour = TriangleElementBehaviour.ThinPlate;

There is another utility static class named ``TriangleElementBehaviours`` which contains predefined combination behaviours for TriangleElement which is more user (developer) friendly than original enum flag.
This is example usage of ``TriangleElementBehaviours`` class:

.. code-block:: cs
   
   var tri = new TrignaleElement();
   tri.Behaviour = TriangleElementBehaviours.ThinShell;

Which is exactly equal to:

.. code-block:: cs
   
   var tri = new TrignaleElement();
   tri.Behaviour = TriangleElementBehaviour.ThinPlate | TriangleElementBehaviour.Membrane | TriangleElementBehaviour.DrillingDof;

So better to use ``TriangleElementBehaviours`` unless needed manually define combination of behaviours.

- ``TriangleElementBehaviours.ThinShell`` and ``TriangleElementBehaviours.ThickShell``: 

.. image:: ../images/bar-fullB.png
   :align: center

   TODO IMAGE, DoFs of ``BarElementBehaviours.FullBeam`` and ``BarElementBehaviours.FullBeamWithShearDefomation``
- ``BarElementBehaviours.FullFrame`` and ``BarElementBehaviours.FullFrameWithShearDeformation``: 

.. image:: ../images/bar-fullframe.png
   :align: center

   TODO IMAGE, DoFs of ``BarElementBehaviours.FullFrame`` and ``BarElementBehaviours.FullFrameWithShearDeformation``
