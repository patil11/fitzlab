fitzlab
=======

Gregson laboratory respository

# Introduction to the Protocols Branch

This branch contains the protocols that are more or less up-to-date and used in the laboratory.

To clone just this branch, do:

    git clone git://github.com/agregson/fitzlab.git --branch protocols --single-branch protocolsLocal


# General Pandoc Instructions

An example to convert to pdf.

``pandoc abstract_jove.md --biblio ~/Documents/jabref/JabRefdb/gnr-new.bib --csl journal-of-visualized-experiments.csl --latex-engine=xelatex -o abstract_jove.pdf``