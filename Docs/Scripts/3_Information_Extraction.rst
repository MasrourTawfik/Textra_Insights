Information Extraction
=======================

The fist stone of our pipeline is extracting main entities from french invoices.
This can be done with three different methods :

1.Using a VLM :
----------------

VLM(Vision Language models) like **LLaVA-7b**, **Llama-Vision3.2** are multimodal models designed to process both visual and textual information. 
They can be fine-tuned or used out-of-the-box to extract structured data from documents like invoices by processing images directly and generating textual outputs.

.. figure:: /Docs/Images/3_Information_Extraction/Pipeline1.png
   :width: 100%
   :align: center
   :alt: Using a VLM
   :name: Pipeline

2.Using LLM :
----------------

An alternative approach involves a **Document Parser** to extract text and structure it into **Markdown** format.
Passing this structured text to an **LLM** for processing and extracting key information.

.. figure:: /Docs/Images/3_Information_Extraction/Pipeline2.png
   :width: 100%
   :align: center
   :alt: Using a Document Parser + LLM
   :name: Pipeline


























