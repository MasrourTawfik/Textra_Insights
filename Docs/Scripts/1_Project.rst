Introduction
===============
Tetxtra Insights is an evolution of the previous version (`Textra <https://textra.readthedocs.io/fr/latest/index.html>`_).
We aim to build a tool for financial summary generation.
for an easy comprehension of our tool here is a infernce pipeline :

.. image:: ../Images/1_Project/infernce_Pipeline.png
   :width: 600
   :align: center
   :alt: alternate Text
   :figclass: align-center

1.Input
==========
The process begins with one or multiple invoices (Images,Pdf files), which can be either client invoices or payment invoices.

2.Enhancement
===============
The first step is to enhance quality of the invoices. with python libraries like
**OpenCV**, **PILOW**,...

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
This ensures compliance with accounting standards and simplifies reporting. Below is a detailed breakdown of the categorization process:










































