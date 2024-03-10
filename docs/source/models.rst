``gougleai.models``
===================

.. code-block::

	gougleai.models: class { list: str, glt: class, gic: class }

The ``gougleai.models`` class contains the models of the Gougle AI API, the snippets to easly get a model ID.

Categories
----------

There is three categories of models:

* :guilabel:`Text Completion`
* :guilabel:`Chat Completion`
* :guilabel:`Image Generation`

``gougleai.models.list``
------------------------

.. code-block::

	list: str

Contains the list of models, here is the value:

.. code-block::

	GLT-1: gougleai.models.glt.glt1 (gougleai.models.glt.versions[0])
	GLT-1.0.5 Beta: gougleai.models.glt.glt105 (gougleai.models.glt.versions[1])
	GIC-1: gougleai.models.gic.gic1 (gougleai.models.gic.versions[0])
	GIC-1.0.5 Beta: gougleai.models.gic.gic105 (gougleai.models.gic.versions[1])

Models families
---------------

``gougleai.models`` contains models families, such as GLT and GIC.

Here is the documentation about these things:

* :doc:`GLT`
* :doc:`GIC`

These are the models families, some classes containing all versions of the models, such as GLT-1 or GIC-1.0.5 Beta.