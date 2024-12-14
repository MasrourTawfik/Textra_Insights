Categorization
===============
*PCG (Plan comptable général)*

Now let's implement the second step of our pipeline: **Categorization**. As explained in the **Introduction** section, we aim to categorize invoices into PCG accounts. 
This can be achieved by using an **Advanced RAG** pipeline, utilizing definitions extracted from a PCG PDF file, which can be found online.

You can find the PCG PDF file `here <https://github.com/MasrourTawfik/Textra_Insights/tree/main/Files>`_.


1.Data Preparation
----------------

If you consult the previous **PCG file**, you notice that is not editable, it's a bunch of scanned images.
To be able to use these definitions we need to **digitize** and **clean** them.

.. note::
   
   - From a quick search on the internet about **Payment Invoices** you find the most relevant Classes is the **PCG file** are :
    
     - *Classe 2  : Comptes d'actif immobilisé (page 18-27 in PCG file)*

        - *21 IMMOBILISATIONS EN NON-VALEURS*
        - *22 IMMOBILISATIONS INCORPORELLES*
        - *23 IMMOBILISATIONS CORPORELLES*
   
     - *Classe 6 : Comptes de charges (page 85-101 in PCG file)*

        - *61 CHARGES D'EXPLOITATION*
   
   - So we focused only on these two classes and their accounts.



























