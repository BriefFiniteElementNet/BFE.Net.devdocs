UniformIsotropicMaterial
========================

Overview
--------

inherited from ``BaseMaterial``, this represents a *unifrom* and *isotropic* material:

- **uniform** means material properties are not varying throught the element's body, or in every location of element material properties are identical.
- **isotropic** means having identical values of a property in all directions

YoungModulus
------------
``UniformIsotropicMaterial.YoungModulus`` represents a value defining the `Young's Modulus <https://en.wikipedia.org/wiki/Young%27s_modulus>`_ (aka. elastic modulus). The dimension is standard SI unit [Pas].

PoissonRatio
------------
``UniformIsotropicMaterial.PoissonRatio`` represents a value defining the `Poisson's ratio <https://en.wikipedia.org/wiki/Poisson%27s_ratio>`_. Poisson’s ratio is Dimensionless and has no SI unit.

static CreateFromYoungPoisson()
-------------------------------
Creates a new instance of ``UniformIsotropicMaterial`` using Young's Modulus and Poisson's Ratio.
Example:
  var e = 210e9;//210 gpa
  var nu = 0.2;

  var steelMat = UniformIsotropicMaterial.CreateFromYoungPoisson(e, nu);
  
static CreateFromYoungShear()
-----------------------------
Creates a new instance of ``UniformIsotropicMaterial`` using Young's Modulus and Shear Modulus.
Example:
  var e = 210e9;//210 gpa
  var g = 79e9;//79 gpa

  var steelMat = UniformIsotropicMaterial.CreateFromYoungShear(e, nu);
  
static CreateFromShearPoisson()
-------------------------------
Creates a new instance of ``UniformIsotropicMaterial`` using Shear Modulus and Poisson's Ratio.
Example:
  var g = 79e9;//79 gpa
  var nu = 0.2;

  var steelMat = UniformIsotropicMaterial.CreateFromShearPoisson(g, nu);