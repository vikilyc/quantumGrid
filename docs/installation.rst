.. highlight:: shell

============
Installation
============

Recommended
-----------
This is a forked repo of quantumGrid that fixes the issue with scipy version deprecation, there are also some cool features under construction.

Before going further using conda, you should always update your conda package system:

.. code-block:: console

    $ conda update -y conda

First, we always recommend to create a conda environment for using our package. This is the general recommended procedure so there are no dependency issues and systemic issues that could break other parts of your computer. To create a conda environment named "DVRenv" run this command in your terminal:

.. code-block:: console

    $ conda create -n DVRenv python=3.10.10

Now we want all the rest of the packages to only be installed into this environment so activate it before moving forward:

.. code-block:: console

    $ conda activate DVRenv

If you have Anaconda intergrated with your shell, you should see `(DVRenv)` in the front of your prompt, indicating you are now in the `DVRenv` environment. If you do not have Anaconda integrated with your shell, then run the following command and confirm you see `DVRenv` on the next line in your terminal:

.. code-block:: console

    $ echo $CONDA_DEFAULT_ENV
    $ DVRenv


The sources for quantumGrid can be downloaded from the `Github repo`_.

Clone the public repository:

.. code-block:: console

    $ git clone git://github.com/vikilyc/quantumGrid

Or download the `tarball`_:

.. code-block:: console

    $ curl -OJL https://github.com/vikilyc/quantumGrid/tarball/master

Once you have a copy of the source, you can install it with:

first go to the folder,

.. code-block:: console

    $ cd ./quantumGrid
    
and then

.. code-block:: console

    $ python setup.py install

You are all set with the installation!

.. highlight:: shell

============
   USAGE
============

To use the library in your own script, first import by:

.. code-block:: python

    from quantumgrid.femdvr import FEM_DVR
    from quantumgrid.potential import Potential

And then create a FEM_DVR instance by:

.. code-block:: python

    fem_dvr = FEM_DVR(n_order, FEM_boundaries, Mass=mu)
   
For more details, *vide* `example`_
    
.. _Github repo: https://github.com/vikilyc/quantumGrid
.. _tarball: https://github.com/vikilyc/quantumGrid/tarball/master
.. _example: https://github.com/vikilyc/quantumGrid/blob/master/quantumgrid_examples/ECS_FEMDVR_diatomic_time_indep_vibration_H2.py
