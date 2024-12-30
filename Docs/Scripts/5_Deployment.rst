Deployment
===========

You can deploy the two built-in pilpelines (**Extraction, Categorization**) in a Cloud services like AWS, Azure, GCP, etc or even HuggingFace in form of a **REST API**.

With the help of **Flask,FastAPI**, then use this API in your application (Gradio, Streamlit, React-Frontend, etc).

Deploying Your FastAPI Applications on Huggingface Via Docker
-------------------------------------------------------------

Step 1: Create a new Docker Space
+++++++++++++++++++++++++++++++++

.. figure:: /Docs/Images/5_Deployment/Image1.png
   :width: 100%
   :align: center
   :alt: Image1
   :name: Create a new Docker Space

Next, you can choose any name you prefer for your project, select a license, and use Docker as the software development kit (SDK). There are many docker templates available which you can choose from. 
I'll start with a blank docker template. Then click on the Create Space button.

.. figure:: /Docs/Images/5_Deployment/Image2.png
   :width: 100%
   :align: center
   :alt: Image2
   :name: Create a new Docker Space

Step 2: Set Up Your FastAPI Application
++++++++++++++++++++++++++++++++++++++++

Refer to the FastAPI documentation `here <https://fastapi.tiangolo.com/tutorial/>`_ if you dont't have any previous experience with FastAPI.

in a file **router.py**, build your routes for example:

-  ``/extraction``:

   - Accept a POST request with *base64* encoding of the Invoice, that you should save it in file because PaddleOCR only accepts file image as input. 
   - Returns a json response with the extracted informations.

-  ``/categorization``:

   - Accept a POST request with *base64* encoding of the Invoice, that you should save it in file because PaddleOCR only accepts file image as input. 
   - Returns a json response with the appropriate Debit Account ID.


1. **requirements.txt**

   - Lists the dependencies of the Python project or application.
   - Used by the Dockerfile to install required libraries.

2. **Textra/router.py**

   - A Python script that contains the implementation of the FastAPI app.
   - Handles the routes and logic for the application.

3. **Textra/ConfigEnv.py**

   - A Python script for managing environment variables.
   - Ensures secure and configurable access to sensitive settings.

4. **Dockerfile**

   - Defines the steps to build the Docker container for the app.
   - Sets up the environment, installs dependencies from `requirements.txt`, and runs the `router.py` script.





















