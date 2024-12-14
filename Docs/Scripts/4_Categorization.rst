Categorization
===============
*PCG (Plan comptable général)*

Now let's implement the second step of our pipeline: **Categorization**. As explained in the **Introduction** section, we aim to categorize invoices into PCG accounts. 
This can be achieved by using an **Advanced RAG** pipeline, utilizing definitions extracted from a PCG PDF file, which can be found online.

You can find the PCG PDF file `here <https://github.com/MasrourTawfik/Textra_Insights/tree/main/Files>`_.


1.Digitalization :
----------------

If you consult the previous **PCG file**, you notice that is not editable, it's a bunch of scanned images.
To be able to use these definitions we need to **digitize** them.




























