About
===

.. autosummary::
   :toctree: generated

   NanoPolaris : A tool for rapid computational optimization of plasmonic nanoparticles for chemical and biological sensing applications

   This tool calculates the near-field response of the nanoparticles from electrostatic principles, considering the surface charge density of the nanoparticle to be a function of its local mean curvature. This path allows to calculate the E-field in all points in space by integrating over the continuous surface charge distribution applying Coulomb law.
   
   Fast calculations of the field decay of the selected nanoparticle geometries are achieved using an equation of the type:

.. math::

    E(r, [G_1, G_2, \ldots, G_n]) = \frac{A([G_1, G_2, \ldots, G_n])}{\left(r + r_0([G_1, G_2, \ldots, G_n])\right)^{n([G_1, G_2, \ldots, G_n])}}

   where r is the distance to nanoparticle surface, and ([G_1, G_2, ..., G_n]) are the n geometric parameters that define the nanoparticle shape.
   Each of the parameters A, r_0 and n functions are fitted using a set of pre-calculated data for each nanoparticle geometry. Therefore, only simple algebraic calculation are required.

   An arbitrary number of surface layers can be considered in the model, each one with its own dielectric function. The dielectric functions of the materials can be defined by the user or taken from a built-in database. For the case of non-homogeneous elements, such as aptamers, enzymes and proteins, a pdf file can be used. The software slices the pdf file in the z-axis and calculates the effective dielectric function for each slice using the Maxwell-Garnett or Bruggemman effective medium theory. These layers are then converted to a single effective refractive index, calculated from the above-metioned field decay profile, as:

.. math::

    n_\mathrm{eff} = \frac{\int n(z)\, |E(z)|^2\, dz}{\int |E(z)|^2\, dz}


   The basis of the optical response is calculated using an universal analytical formalism developed by Garcia de Abajo et al., (https://doi.org/10.1039/C6CS00919K), where a polarizability is returned for the specific nanoparticle. In this package additional corrections are added to account for size effects: (i) Surface dampening for small nanoparticles; (ii) retardation effects for large nanoparticles; (iii) substrate effects for supported or nearby substrates.


   this project is under active development.
   Developed by Paulo S. S. dos Santos