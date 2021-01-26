PartialNonUniformLoad
============
``PartialNonUniformLoad`` in namespace `` BriefFiniteElementNet.Loads``, is a varying distributed load which can apply on 1D (like ``BarElement``), 2D (like ``TriangleElement``) or 3D (like ``TetrahedronElement``) elements.

Here are examples illustrated in image:

.. figure:: images/tload-body-bar.png
   :align: center
   
   ``PartialNonUniformLoad`` applying on a BarElement


SeverityFunction
---------
Severity function which defines how much is the amount of load in each iso location. For example a linear varying load from xi = -0.5 to xi = +0.5 and start magnitude = `100 N/m` and end magnitude `50 N/m`, severity function in -0.5 equals 100 and severity function +0.5 equals 50

StartLocation
---------
Isoparametric coordination of start location of load on the element. all members of `TrapezoidalLoad.StartIsoLocations` must be in range `[-1,+1]`.

EndLocations
---------
Isoparametric coordination of end location of load on the element. all members of `TrapezoidalLoad.EndIsoLocations` must be in range `[-1,+1]`.

Coordination System
-------------------
``PartialNonUniformLoad.CoordinationSystem`` which is a enum typed property of ``PartialNonUniformLoad``, defines the coordination system of trapezoidal load. It can only have two different values of ``CoordinationSystem.Global`` or ``CoordinationSystem.Local``:

	- ``CoordinationSystem.Global``: The load is assumed in global coordination system
	- ``CoordinationSystem.Local``: The load is assumed in local coordination system of element that load is applied to (each element type have different local coordination system which is stated in appropriated section).
