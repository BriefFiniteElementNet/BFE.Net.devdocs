Internal forces for bar element
===
After solving the ``Model``, ``BarElements`` will have some internal forces. Internal force at each location of element can be different and it can be catched with method ```BarElement.GetInternalForce```.
with get the location that you need the internal force as input. Internal force means axial load, two shear loads, torque moment and two biaxial moments which are shown in picture:
TODO show with returned axis directions

Note that value returned from this method is in element's local coordination system.