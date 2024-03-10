API Access
==========

.. note::
	Due to technical issues with the Gougle AI services, the library currently relies on the `OpenAI API <https://platform.openai.com/>`_. This is a temporary solution, and future updates might switch to the official Gougle AI services upon resolution.

This section covers how to interact with the Gougle AI API through its provided functions. However, there are two important pieces of information required before using the library:

* ``gougleai.apiKey``: Your API Key
* ``gougleai.orgId`` (optional): Your organization ID

``gougleai.apiKey``
-------------------

The API Key is a secret credential that identifies your project and grants access to Gougle AI's services. It's essential to keep your API Key secure and not share it publicly.

To obtain an API Key, you'll need to go to your `Gougle AI account page <https://ai.withgougle.cf/account>`_ and click on the button :guilabel:`Get API Key`.

Then, you'll need to provide you email and your password, then you will have a verification code by email, and you'll be able to see your API Key for the unique time.

.. note::
	Due to the technical issues with the Gougle AI services, we temporarly switched to the OpenAI API so you need to get OpenAI API Key from `OpenAI Platform <https://platform.openai.com/api-keys>`_.

Using the API Key
~~~~~~~~~~~~~~~~~

The Gougle AI library utilizes your API Key for authentication purposes whenever you call functions that interact with the Gougle AI services. Internally, the library stores the API Key in the ``gougleai.apiKey`` variable. 

Here's how to set your API Key:

.. code-block::
	import gougleai

	gougleai.apiKey = "YOUR_API_KEY"

Replace ``YOUR_API_KEY`` with your actual API Key.

.. warning::
	Setting an empty string to ``gougleai.apiKey`` will raise an exception.

``gougleai.orgId``
------------------

.. note::
	The Organization ID is not like an API Key, it don't grant access for the same things.

.. warning::
	The Organization ID is not used for now due to the technical issues.

The Organization ID is a secret credential that identifies your organization and grants access to some Gougle AI's services for more than one people. It's essential to keep your Organization ID secure and not share it publicly.

To obtain an Organization ID, you'll need to go to your `Gougle AI account page <https://ai.withgougle.cf/account>`_, then click on you profile picture and then on :guilabel:`Manage Organization`, and click on the button :guilabel:`Get Organization ID`.

Then, you'll need to provide you email and your password, then you will have a verification code by email, and you'll be able to see your Organization ID for the unique time.

.. note::
	Due to the technical issues with the Gougle AI services, we temporarly switched to the OpenAI API so you need to get OpenAI Organization ID from `OpenAI Platform <https://platform.openai.com/account/organization>`_.

Using the Organization ID
~~~~~~~~~~~~~~~~~~~~~~~~~

The Gougle AI library utilizes your Organization ID for authentication purposes whenever you call some functions that interact with some Gougle AI services. Internally, the library stores the Organization ID in the ``gougleai.orgId`` variable. 

Here's how to set your Organization ID:

.. code-block::
	import gougleai

	gougleai.orgId = "YOUR_ORG_ID"

Replace ``YOUR_ORG_ID`` with your actual organization ID.