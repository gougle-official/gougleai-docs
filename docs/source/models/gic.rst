``gougleai.models.gic``
=======================

.. code-block::

    gougleai.models.gic: class { gic1, gic105, versions[] }

``gougleai.models.gic`` is the class of the models familiy of GIC. GIC (**G**ougle **I**mage **C**reator) models are :guilabel:`Image Generation` models, that means that these models can be used with no module's function right now.

.. warning::
	Class names are case sensitive: ``GIC`` ≠ ``gic``

Included models
---------------

In ``gougleai.models.gic``, there is two models:

* GIC-1 (``gougleai.models.gic.gic1``)
* GIC-1.0.5 Beta (``gougleai.models.gic.gic105``)

These models are diferent versions of GIC, GIC-1 the latest release and GIC-1.0.5 the latest beta.

Access to the models
--------------------

To access to the models variables, there is two way:

* Using the model's name
* Using the model's version code number

There is the steps for both:

Using model's name
~~~~~~~~~~~~~~~~~~

To make it by this way, we just need to follow the 'class path':

.. code-block::

	gougleai  .  models  .  gic  .  gic1
	    ↑          ↑         ↑       ↑
	  module    primary    model   model
	             class    family   name

So by this way, we can acces to GIC-1 by its name.

Using model's version code number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To make it using this way, we need to have the version code number, this number is the number of the version, starting from 0 as the first model's version and increasing of 1 each version of the model.

So, to acces to GIC-1.0.5 Beta by this way, we can use this:

.. code-block::

	gougleai  .  models  .  gic  .  versions  [  1  ]
	    ↑          ↑         ↑         ↑         ↑   
	  module    primary    model     model    model's   
	             class    family    versions  version
	                                           code
	                                          number   

So by this way, we can acces to GIC-1.0.5 Beta by its version code number.