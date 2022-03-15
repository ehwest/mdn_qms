The QMS system "source" code is in the "source/Quality_Manual" folder.

To build the work products, position your terminal in the repository base  ehwest/mdn_qms
and then do this:

$ make latexpdf 

The pdf that is built will be here:   ...mdn_qms/build/latex/medicaldatanetworksqualitymanagementsystemdescription.pdf
(for users/ehwest)

A build of this source should put finished products in the "build" folder.
In this directory, find a Makefile that supports making the products
and putting them in the build folder.

The complete Quality Manual is assembled from about 30 markdown files.
A make file is provided to automatically assemble the files.
The official list of files that are part of the QMS are located in this file:
...mdn_qns/source/index.rst

Quality Record Templates are also provided in the Templates folder of the repository  .../mdn_qms/source/Quality_Manual/templates
Quality Records are stored in the Google Docs folder which is shared with designated employees.

The latest copy of all of these files may be determined by reading the document
hash code created by the github system.



