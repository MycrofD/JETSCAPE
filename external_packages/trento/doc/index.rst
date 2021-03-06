T\ :sub:`R`\ ENTo
=================
*Reduced Thickness Event-by-event Nuclear Topology*

T\ :sub:`R`\ ENTo is a simple, fast model for the initial conditions of high-energy nuclear collisions (pp, pA, AA).
`PRC 92 011901 <http://journals.aps.org/prc/abstract/10.1103/PhysRevC.92.011901>`_ / `arXiv:1412.4708 [nucl-th] <http://inspirehep.net/record/1334386>`_ formally presents the model and preliminary results.
The code is `publicly available on github <https://github.com/Duke-QCD/trento>`_.

.. figure:: _static/event.png
   :alt: Pb+Pb event

   Pb+Pb event generated by the model

Quickstart
----------
First, install the dependencies: a C++11 compiler, Boost, and optionally HDF5.
Then download the trento source and compile with CMake::

   mkdir build && cd build
   cmake ..
   make install

See :doc:`installation` for details.

Generate ten lead-lead events using default settings::

   trento Pb Pb 10

``trento`` prints the following event properties to stdout: event number, impact parameter, number of participants, total entropy, and eccentricity harmonics 2--5.
To additionally save the event profiles to an HDF5 file::

   trento Pb Pb 10 -o events.hdf

See :doc:`usage` and :doc:`examples` for complete documentation.

User guide
----------
.. toctree::
   :maxdepth: 2

   installation
   usage
   examples

Technical details
-----------------
.. toctree::
   :maxdepth: 2

   internals

Attribution
-----------
If you make use of this software in your research, please `cite it <http://inspirehep.net/record/1334386>`_.
The BibTeX entry is::

   @article{Moreland:2014oya,
         author         = "Moreland, J. Scott and Bernhard, Jonah E. and Bass,
                           Steffen A.",
         title          = "{Alternative ansatz to wounded nucleon and binary
                           collision scaling in high-energy nuclear collisions}",
         journal        = "Phys.Rev.",
         number         = "1",
         volume         = "C92",
         pages          = "011901",
         doi            = "10.1103/PhysRevC.92.011901",
         year           = "2015",
         eprint         = "1412.4708",
         archivePrefix  = "arXiv",
         primaryClass   = "nucl-th",
         SLACcitation   = "%%CITATION = ARXIV:1412.4708;%%",
   }

Running ``trento --bibtex`` will also print this entry.
