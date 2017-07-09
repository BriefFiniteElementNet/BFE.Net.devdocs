TelepathyLink
=============
``RigidElement`` is an ``MpcElement``, That partially connect Dofs of several nodes together. Best example can be a hing that binds displacement DoFs of two nodes in same location together but doest not bind their rotational DoFs so they can each rotate individually and connection will be a hing connection.

.. hint:: all types of partiall connection of elements to nodes are able to be modeled with ``TelepathyLink``.

Example:
partiall end release of a 5 meter beam.

``
var n1 = new Node(0,0,0);
var n2 = new Node(0,0,0);
var n3 = new Node(5,0,0);

var bar = new BarElement(n2,n3);
var link = new TelepathyLink();
link.UseForAllLoads = true;
link.Nodes.Add(n1, n2);
link.BindDx = link.BindDy = link.BindDz = true;
link.BindRx = link.BindRy = link.BindRz = false;
``