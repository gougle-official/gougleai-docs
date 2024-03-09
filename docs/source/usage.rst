Usages
======

Installation
------------

For ``python`` using ``pip`` in ``cmd``:

.. code-block:: shell
	
	pip install gougleai

Models
------

+------------------+--------------------------------+-------------------------------------------------------------+
| Model Name       | Model ID                       | Model Type                                                  |
+==================+================================+=============================================================+
| GLT-1            | ``gougleai.models.glt.glt1``   | :guilabel:`Chat Completion` and :guilabel:`Text Completion` |
+------------------+--------------------------------+-------------------------------------------------------------+
| GLT-1.0.5 Beta   | ``gougleai.models.glt.glt105`` | :guilabel:`Chat Completion` and :guilabel:`Text Completion` |
+------------------+--------------------------------+-------------------------------------------------------------+
| GIC-1            | ``gougleai.models.gic.gic1``   | :guilabel:`Image Generation`                                |
+------------------+--------------------------------+-------------------------------------------------------------+
| GIC-1.0.5 Beta   | ``gougleai.models.gic.gic105`` | :guilabel:`Image Generation`                                |
+------------------+--------------------------------+-------------------------------------------------------------+

Example
-------

.. code-block:: python
	
	import gougleai

	gougleai.apiKey = "YOUR_API_KEY_HERE"

	while True:
		userInput = input("User: ")

		response = gougleai.complete(model=gougleai.models.glt.glt1, prompt=userInput, maxTokenNumber=100)

		print("GLT-1: " + response.choices[0])
