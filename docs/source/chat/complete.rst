``gougleai.chat.complete()``
=============================

.. warning::
	*Not to be confused with * :doc:```gougleai.complete()`` <complete>` *.*

.. code-block::

   gougleai.chat.complete(model, chatHistory: object, maxTokenNumber: int = 100) -> { choices[str] }

``gougleai.chat.complete()`` is a function designed for chat conversations. 
It interacts with the Gougle AI API to generate responses based on a chat history 
and a specified model with a maximum token number.

.. note::
	Because of some technical issues with the Gougle AI API services, this use temporarly the `OpenAI API <https://platform.openai.com>`_.

**Parameters**
----------

* ``model``: The name of the :ref:`model <usage:models>` to use.
.. note::
     Only :guilabel:`Chat Completion` models allowed for ``gougleai.chat.complete()``.
* ``chatHistory: object``: A dictionary containing the chat history information. This dictionary should have the following keys:
    * ``role: str``: The role of the message sender (``ai``, ``system``, or ``user``).
    * ``message: str``: The message content of the previous turn.
* ``maxTokenNumber: int = 100``: The maximum number of tokens (~words) to generate in the response (defaults to 100).

**Returned value**
-----------------

The function returns a dictionary with the list ``choices`` containing 
the generated text completions for the chat response.

**Usage Examples**
----------------

Here's an example of how ``gougleai.chat.complete()`` might be used to 
create a simple chatbot:

.. code-block:: python

   import gougleai

   gougleai.apiKey = "YOUR_API_KEY"

   chat_history = {"role": "user", "message": "Hello!"}

   while True:
       user_message = input("You: ")
       chat_history["role"] = "user"
       chat_history["message"] = user_message

       if user_message == "exit":
           break

       response = gougleai.chat.complete(model=gougleai.models.glt.glt1, chatHistory=chat_history)
       print("Chatbot: " + response.choices[0])

       chat_history["role"] = "ai"
       chat_history["message"] = response.choices[0]
