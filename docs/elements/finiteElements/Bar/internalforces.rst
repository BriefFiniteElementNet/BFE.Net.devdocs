.. _BarElement-InternalForce:

Internal Force And Displacement
--------------
After solving the ``Model``, ``BarElements`` will have some internal forces. Internal force at each location of element can be different and it can be catched with method ``BarElement.GetInternalForce`` and ``BarElement.GetExactInternalForce``. The difference between ``BarElement.GetInternalForce`` and ``BarElement.GetExactInternalForce`` is that Exact one also considers effect of elemental loads (like distributed loads) in element. Internal force means axial load, two shear loads, torque moment and two biaxial moments which are shown in picture:
TODO show with returned axis directions

Note that value returned from this method is in element's local coordination system.
