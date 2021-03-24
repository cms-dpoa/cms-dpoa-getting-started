# Categorisation

To ease the search of datasets of interest in the collection of simulated data, a search tag is added to each simulated dataset. These tags describe the physics process included in each simulated dataset and they can be used for [search](https://opendata.cern.ch/search?page=1&size=20&q=&ondemand=True&subcategory=Drell-Yan&category=Standard%20Model%20Physics).

The category tag is defined from the dataset name with [the categorisation script](https://github.com/cernopendata/data-curation/blob/master/cms-YYYY-simulated-datasets/code/categorisation.py).

It can be run stand-alone (without other steps of the metadata preparation and without access to CMS databases) with

```
git clone git@github.com:cernopendata/data-curation.git
cd data-curation/cms-YYYY-simulated-datasets
python3 ./code/interface.py --print-categorisation ./inputs/CMS-2015-mc-datasets.txt > categorisation-2015.md
```

This run the categorisation on the list of 2015 simulated datasets. The output file is in markdown format (and can be rendered e.g. by opening it in VS Code, by right-clicking on the editor tab and selecting `Open preview`.).
