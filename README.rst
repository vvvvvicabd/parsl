Parsl - Parallel Scripting Library
==================================
|licence| |build-status| |docs|

Parsl is a parallel programming library for Python. Parsl augments Python with simple, scalable, and flexible constructs for encoding parallelism. Developers annotate Python functions to specify opportunities for concurrent execution. These annotated functions, called apps, may represent pure Python functions or calls to external applications, whether sequential, multicore (e.g., CPU, GPU, accelerator), or multi-node MPI. Parsl further allows these calls to these apps, called tasks, to be connected by shared input/output data (e.g., Python objects or files) via which Parsl can construct a dynamic dependency graph of tasks.

Parsl includes a flexible and scalable runtime that allows it to efficiently execute Python programs in parallel. Parsl scripts are portable and can be easily moved between different execution resources: from laptops to supercomputers to clouds. When executing a Parsl program, developers first define a simple Python-based configuration that outlines where and how to execute tasks. Parsl supports various target resources including clouds (e.g., Amazon Web Services and Google Cloud), clusters (e.g., using Slurm, Torque/PBS, HTCondor, Cobalt), and container orchestration systems (e.g., Kubernetes). Parsl scripts can scale from a single core on a single computer through to hundreds of thousands of cores across many thousands of nodes on a supercomputer.

Parsl can be used to implement various parallel computing paradigms:

* Concurrent execution of a set of tasks in a bag-of-tasks program
* Procedural workflows in which tasks are executed following control logic
* Parallel dataflow in which tasks are executed when their data dependencies are met
* Heterogeneous many-task applications in which many different computing resources are used together to execute different types of computational tasks
* Dynamic workflows in which the workflow is determined during execution
* Interactive parallel programming through notebooks or another interactive mechanism

The latest Parsl version available on PyPi is v0.9.0.

.. |licence| image:: https://img.shields.io/badge/License-Apache%202.0-blue.svg
   :target: https://github.com/Parsl/parsl/blob/master/LICENSE
   :alt: Apache Licence V2.0
.. |build-status| image:: https://travis-ci.com/Parsl/parsl.svg?branch=master
   :target: https://travis-ci.com/Parsl/parsl
   :alt: Build status
.. |docs| image:: https://readthedocs.org/projects/parsl/badge/?version=stable
   :target: http://parsl.readthedocs.io/en/stable/?badge=stable
   :alt: Documentation Status

QuickStart
==========

Parsl is now available on PyPI, but first make sure you have Python3.5+ ::

    $ python3 --version

Install Parsl using pip::

    $ pip3 install parsl

To run the Parsl tutorial notebooks you will need to install Jupyter::

    $ pip3 install jupyter

Detailed information about setting up Jupyter with Python3.5 is available `here <https://jupyter.readthedocs.io/en/latest/install.html>`_

Note: Parsl uses an opt-in model to collect anonymous usage statistics for reporting and improvement purposes. To understand what stats are collected and enable collection please refer to the `usage tracking guide <http://parsl.readthedocs.io/en/stable/userguide/usage_tracking.html>`__

Documentation
=============

The complete parsl documentation is hosted `here <http://parsl.readthedocs.io/en/stable/>`_.

The Parsl tutorial is hosted on live Jupyter notebooks `here <https://mybinder.org/v2/gh/Parsl/parsl-tutorial/master>`_


For Developers
--------------

1. Download Parsl::

    $ git clone https://github.com/Parsl/parsl

2. Install::

    $ cd parsl
    $ python3 setup.py install

3. Use Parsl!

Requirements
============

Parsl is supported in Python 3.5+. Requirements can be found `here <requirements.txt>`_. Requirements for running tests can be found `here <test-requirements.txt>`_.

Code of Conduct
============

Parsl seeks to foster an open and welcoming environment - Please see the `Parsl Code of Conduct <https://github.com/Parsl/parsl/blob/master/CoC.md>`_ for more details.

Contributing
============

We welcome contributions from the community. Please see our `contributing guide <CONTRIBUTING.rst>`_.
