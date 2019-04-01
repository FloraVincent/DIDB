[![Build Status](https://travis-ci.org/globalbioticinteractions/template-dataset.svg)](https://travis-ci.org/globalbioticinteractions/template-dataset)
[![DOI](https://zenodo.org/badge/178421754.svg)](https://zenodo.org/badge/latestdoi/178421754) [![GloBI](http://api.globalbioticinteractions.org/interaction.svg?accordingTo=globi:globalbioticinteractions/template-dataset)](http://globalbioticinteractions.org/?accordingTo=globi:globalbioticinteractions/template-dataset) 

## DIDB: Diatom Interaction DataBase
Available literature was automatically screened, and manually curated, to look for all ecological interactions involving diatoms to establish the current state of knowledge regarding the diatom interactome, both in marine and freshwater environments. 

Diatom ecological interactions as defined in this databse are a very large group of associations, characterized by (i) the nature of the association defined by the ecological interaction or the mechanism (predation, symbiosis, mutualism, competition, epibiosis), (ii) the diatom involved, and (iii) the partners of the interaction. 

The protocol to build the list of literature-based interactions was the following :
(i) collect publications involving diatom associations using (a) the Web of Science query TITLE: (diatom*) AND TOPIC : (symbio* OR competition OR parasit* OR predat* OR epiphyte OR allelopathy OR epibiont OR mutualism) ; (b) Eutils tools to mine Pubmed and extract ID of all publications with the search url http://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=diatom+symbiosis&usehistory=y and the same keywords; (c)  the get_interactions_by_taxa(sourcetaxon = “Bacillariophyta”) function from the RGlobi package (Poelen et al., 2014), the most recent and extensive automated database of biotic interactions; and (d) personal mining from other publication browsers and input from experts 
(ii) extract when relevant the partners of the interactions based on the title and on the abstract for Web of Science, Pubmed and personal references and normalize the label of the interaction based on Globi nomenclature 
(iii) display KRONA plot with Type of Interaction / Partner Class / Diatom genus / Partner genus_species. 

Cases of episammic (sand) and epipelon (mud) interactions were not considered as they involved association with non-living surfaces.

This repository provides an example on how to make your biotic interaction data available through Global Biotic Interactions (GloBI, http://globalbioticinteractions.org) published in 2014.

Note: This is DIDB V1.0 and is prone to improvement; if you want to contribute with last publications or publications that I forgot, drop me a message on Git, twitter (@vincentflora) and I'll make sure to add it and credit your contribution.
