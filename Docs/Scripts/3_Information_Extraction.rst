Information Extraction
=======================

The first stone of our pipeline is extracting main entities from french invoices.
This can be done with three different methods :

1.Using a VLM :
----------------

VLM(Vision Language models) like **LLaVA-7b**, **Llama-Vision3.2** are multimodal models designed to process both visual and textual information. 
They can be fine-tuned or used out-of-the-box to extract structured data from documents like invoices by processing images directly and generating textual outputs.

.. figure:: /Docs/Images/3_Information_Extraction/Pipeline1.png
   :width: 60%
   :align: center
   :alt: Using a VLM
   :name: Pipeline

To test this approach we used Llama-Vision-11b with Langchain and Ollama, all the Code here in a colab notebook.

.. raw:: html

   <a href="https://colab.research.google.com/github/MasrourTawfik/Textra_Insights/blob/main/Notebooks/3_Information_Extraction.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

2.Using LLM :
----------------

2.1 With a Document Parser
+++++++++++++++++++++++++++++

An alternative approach involves a **Document Parser** to extract text and structure it into **Markdown** format.
Passing this structured text to an **LLM** for processing and extracting key information.

.. figure:: /Docs/Images/3_Information_Extraction/Pipeline2.png
   :width: 80%
   :align: center
   :alt: Using a Document Parser + LLM
   :name: Pipeline

A question should be asked here is *Why using a Document Parser ?*, because LLMs understand markdown text better. Besides to 
preserving the Invoice's layout and tabulated data in a proper format.

There are many options like : Upstage API, MegaParse, Docling... but keep in mind that 
we want our tool's inference to be 100% with local and limited resources. So we decided to countinue with **Docling** of IBM.

To understand better the benifit of a Document Parser, here is a video from MegaParse github repository :

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe src="https://www.youtube.com/embed/RhX_vsk7abg" frameborder="0" allowfullscreen style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe>
    </div>


.. note:: 

   - Visit the `Docling <https://ds4sd.github.io/docling/>`_ documentation for more details.
   - You can find `here <https://github.com/QuivrHQ/MegaParse>`_ the MegaParse repository
   - For Upstage API, you can find `here <https://www.upstage.ai/products/document-parse>`_ the official website.

A hands-on example of this pipeline can be found in colab notebook.

.. raw:: html

   <a href="https://colab.research.google.com/github/MasrourTawfik/Textra_Insights/blob/main/Notebooks/3_Information_Extraction.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

2.2 With an OCR
+++++++++++++++++

1. **OCR (Optical Character Recognition)** Converts the invoice into machine-readable plain text by extracting text data from the Invoice.  

2. **LLM (Large Language Model)**: The text is processed by an LLM.

3. 🎉 **Output**: The processed information is presented in a structered json format.

.. figure:: /Docs/Images/3_Information_Extraction/Pipeline3.png
   :width: 80%
   :align: center
   :alt: Using an OCR + LLM
   :name: Pipeline

For the OCR-Engine there are alot of options like **PaddleOCR**, **EasyOCR**, **Tesseract**, **docTR**, ...

- A Blog by `Roboflow <https://blog.roboflow.com/best-ocr-models-text-recognition/#ocr-testing-methodology>`_ countain a good bechamrking of 4 OCR models (docTR, EasyOCR, Tesseract, Surya) Show that EasyOCR has the best accuarcy/speed ratio.

- Another comparaison between EasyOCR and `Paddle <https://paddlepaddle.github.io/PaddleOCR/latest/en/index.html>`_ by **Christian Weiler** `here <https://www.bludelta.de/en/ocr-and-deepocr-in-comparison/>`_ on 400 real invoices, show that EasyOCR has the best metrics.

.. figure:: /Docs/Images/3_Information_Extraction/Roboflow.png
   :width: 100%
   :align: center
   :alt: Using an OCR + LLM
   :name: Pipeline

.. raw:: html

   <a href="https://colab.research.google.com/github/MasrourTawfik/Textra_Insights/blob/main/Notebooks/3_Information_Extraction.ipynb" target="_blank"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

















