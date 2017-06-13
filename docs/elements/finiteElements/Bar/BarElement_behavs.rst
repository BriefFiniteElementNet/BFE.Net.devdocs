Behaviours
==========
``BarElement.Behaviour`` property is an enum flag (enum flag  means an enum that can have several values at same time). It can be set to frame, beam, truss, shaft etc. 
The possible behaviours for the BarElement is:

- ``BarElementBehaviour.EulerBernoulyBeamY`` : Beam in Y direction based on Euler-Bernouly theory. DoFs are shown in below image:
.. image:: ../images/bar-b1.png
- ``BarElementBehaviour.EulerBernoulyBeamZ`` : Beam in Z direction based on Euler-Bernouly theory. DoFs are shown in below image:
.. image:: ../images/bar-b2.png
- ``BarElementBehaviour.TimoshenkoBeamY`` : Beam in Y direction based on Timoshenko's theory (shear deformation). DoFs are shown in below image:
.. image:: ../images/bar-b1.png
- ``BarElementBehaviour.TimoshenkoBeamZ`` : Beam in Z direction based on Timoshenko's theory (shear deformation). DoFs are shown in below image:
.. image:: ../images/bar-b2.png
- ``BarElementBehaviour.Truss`` : Only axial load carrying. DoFs are shown in below image:
.. image:: ../images/bar-truss.png
- ``BarElementBehaviour.Shaft`` : Only torsional moment carrying. DoFs are shown in below image:
.. image:: ../images/bar-shaft.png

These behaviours can be combined, for example a truss member should only have a Truss behaviour, but a 3d frame member does have two beam behaviour in Y and Z directions, a truss behaviour and a shaft behaviour, (all these behaviours at the same time).
 
This is an example which makes a BarElement with truss behaviour which in real acts as a truss member that only can carry axial load:

.. code-block:: cs
   
   var bar = new BarElement();
   bar.Behaviour = BarElementBehaviour.Truss;

There is another utility static class named ``BarElementBehaviours`` which contains predefined combination behaviours for BarElement which is more user (developer) friendly than original enum flag.
This is example usage of ``BarElementBehaviours`` class:

.. code-block:: cs
   
   var bar = new BarElement();
   bar.Behaviour = BarElementBehaviours.FullFrame;

If we did not want use BarElementBehaviours utility, then we had to write like this (in this example both are same):

.. code-block:: cs
   
   var bar = new BarElement();
   bar.Behaviour = BarElementBehaviour.Truss | BarElementBehaviour.BeamYEulerBernoulli | BarElementBehaviour.BeamZEulerBernoulli | BarElementBehaviour.Shaft;

So better to use ``BarElementBehaviours`` unless needed manually define combination of behaviours.

``BarElementBehaviours.FullBeam`` and ``BarElementBehaviours.FullBeamWithShearDefomation``: 

.. image:: ../images/bar-fullB.png
``BarElementBehaviours.FullFrame`` and ``BarElementBehaviours.FullFrameWithShearDeformation``: 

.. image:: ../images/bar-fullframe.png