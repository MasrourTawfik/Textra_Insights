Introduction
===============
Tetxtra Insights is an evolution of the previous version (`Textra <https://textra.readthedocs.io/fr/latest/index.html>`_).
We aim to build a tool for financial summary generation.
for an easy comprehension of our tool here is a infernce pipeline :

.. figure:: /Docs/Images/1_Project/Inference_Pipeline.png
   :width: 100%
   :align: center
   :alt: Alternative text for the image
   :name: Pipeline

1.Input
==========
The process begins with one or multiple invoices (Images,Pdf files), which can be either client invoices or payment invoices.

2.Enhancement
===============
The first step is enhancing quality of the invoices. with python libraries like
**OpenCV**, **PILOW**,...
Preprocessing Images (For Scanned or Photographed Invoices) by : 
  - Convert images to grayscale for simpler processing.
  - Denoise the image to remove background noise.
  - Binarize the image (convert to black and white) for better OCR (Optical Character Recognition) results.
  

3.Information Extraction
=========================
Extracts key fields from invoices for further analysis like :
  - Total amount (Tax included)
  - Total amount (Tax excluded)
  - VAT rate
  - Date of invoice
  - Invoice number
  - Supplier Contacts (email, phone, address ...)

4.Categorization
===================
A critical step in the invoice processing pipeline, where extracted information is analyzed and assigned to the correct accounting categories based on the `Moroccan General Chart of Accounts`. 
This ensures compliance with accounting standards and simplifies reporting.

In general three types of accounts are used :
  - Debit Account
  - Credit Account
  - VAT Account










































