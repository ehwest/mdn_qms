The QMS system "source" code is in the "source/Quality_Manual" folder.
A build of this source should put finished products in the "build" folder.
In this directory, find a Makefile that supports making the products
and putting them in the build folder.

The complete Quality Manual is assembled from about 30 markdown files.
A make file is provided to automatically assemble the files.

In addition, there is a folder that contains actual quality records and
templates for quality records.  Authorized users may create new quality records,
although most quality records are created automatically by the github system.

The latest copy of all of these files may be determined by reading the document
hash code created by the github system.


To build the work products, do a 

$ make latexpdf 

The pdf that is built will be here:   /Users/ehwest/mdn_qms/build/latex/medicaldatanetworksqualitymanagementsystemdescription.pdf
(for users/ehwest)


