``gougleai.models.glt``
=======================

.. code-block::

    gougleai.models.glt: class { glt1, glt105, versions[] }

``gougleai.models.glt`` is the class of the models familiy of GLT. GLT (**G**ougle **L**anguage **T**ransformer) models are :guilabel:`Text Completion` and :guilabel:`Chat Completion` models, that means that these models can be used with both ``gougleai.complete()`` and ``gougleai.chat.complete()``.

.. warning::
	Class names are case sensitive: ``GLT`` ≠ ``glt``

Included models
---------------

In ``gougleai.models.glt``, there is two models:

* GLT-1 (``gougleai.models.glt.glt1``)
* GLT-1.0.5 Beta (``gougleai.models.glt.glt105``)

These models are diferent versions of GLT, GLT-1 the latest release and GLT-1.0.5 the latest beta.

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

	gougleai  .  models  .  glt  .  glt1
	    ↑          ↑         ↑       ↑
	  module    primary    model   model
	             class    family   name

So by this way, we can acces to GLT-1 by its name.

Using model's version code number
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To make it using this way, we need to have the version code number, this number is the number of the version, starting from 0 as the first model's version and increasing of 1 each version of the model.

So, to acces to GLT-1.0.5 Beta by this way, we can use this:

.. code-block::

	gougleai  .  models  .  glt  .  versions  [  1  ]
	    ↑          ↑         ↑         ↑         ↑   
	  module    primary    model     model    model's   
	             class    family    versions  version
	                                           code
	                                          number   

So by this way, we can acces to GLT-1.0.5 Beta by its version code number.