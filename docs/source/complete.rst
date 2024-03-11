``gougleai.complete()``
=======================

.. warning::
	*Not to be confused with :meth:`gougleai.chat.complete() <chat/complete>`.*

.. code-block::

	gougleai.complete(model, prompt: str, maxTokenNumber: int = 100) -> { choices[str] }

``gougleai.complete()`` is a fu
*Not to be confused with *:doc:```gougleai.complete()`` <complete>`*.*nction to get an API response from a prompt to a model with a max token number.
It interacts with the Gougle AI API to generate text completions.

.. note::
	Because of some technical issues with the Gougle AI API services, this use temporarly the `OpenAI API <https://platform.openai.com>`_.

Parameters
----------

* ``model``: The name of the :ref:`model <usage:models>` to use.
.. note::
	Only :guilabel:`Text Completion` models allowed for ``gougleai.complete()``.
* ``prompt: str``: The text prompt for the model.
* ``maxTokenNumber: int = 100``: The maximum number of tokens (words) to generate in the response (defaults to 100).

Returned value
--------------

The function returns a dictionary with the list ``choices`` containing the generated text completions.

Usage Examples
--------------

Here is an example of an AI that try to generate Python code about a given idea:

.. code-block:: python

	import gougleai

	gougleai.apiKey = "YOUR_API_KEY"

	while True:
		usr_inp = input("Idea of Python program: ")

		if usr_inp == "exit":
			print("Exiting...")
			break
		elif usr_inp != ("" or null):
			response = gougleai.complete(model=gougleai.models.glt.glt1, prompt="Make a Python program following this idea: " + usr_inp, maxTokenNumber=200)
			print("Generated code: \n```\n" + response.choices[0] + "\n```")
