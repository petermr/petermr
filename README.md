# petermr repositories

Many of these repos are widely used in collaborative projects and include:
* code
* data
* projects

This special repo is to coordinate navigation and discussion

# discussion lists

The "Discussions" for this repo https://github.com/petermr/petermr/discussions include discussions for the other repos and are of indicated by their name. They may replace our (private) Slack for all public-facing material (private project management will remain on Slack). 

# active repos
* https://github.com/petermr/pygetpapers. automatic downloading of articles and preprints in bulk. Pioneered by Rik Smith-Unna and ported to Python by @ayush
garg. CLI. PyPi: https://pypi.org/project/pygetpapers/ 
* https://github.com/petermr/amilib. (Was https://github.com/petermr/pyami). Port of Java https://github.com/petermr/ami3 to Python (@petermr). CLI. Includes a prototype GUI in `tkinter`. PyPi: https://pypi.org/project/py4ami/ (Note there is already an unrelated `pyAMI` in `PyPi` so in that namespace we are `py4ami`, but on Github it's `pyami`)
* https://github.com/petermr/pyamiimage. Analysis of scientific duagrams (@petermr, @anuvc). No CLI, or PyPI yet. 
* https://github.com/petermr/docanalysis. Text-based analysis of scientific articles (@shweatahegde). [PyPI](https://pypi.org/project/docanalysis/) 
* https://github.com/petermr/cevopen. Projects, dictionaries and outreach for analysing articles in plant sciences.
* https://github.com/petermr/openvirus. Projects, dictionaries and outreach for analysing articles on viral epidemics.
* https://github.com/petermr/crops. NIPGR-intern projects on crops. Minicorpora and dictionaries for terpene synthases
* https://github.com/petermr/opendiagram. Adaptation of `pyamiimage` to extract data from diagrams, especially materials science/batteries
* https://github.com/petermr/dictionary. Software for distributed dictionaries and many dictionaries


# active Python projects:

For context:
We have 4 packages (if that's the right word).  They are largely standalone but can have useful library routines. They all share a common data structure on disk (simply named directories). This means that state is less important and often held on the filesystem. It also means that data can be further manipulated by Unix tools and other utilities. This is very fluid as we are constantly adding new data substructures. (I developed much of this in Java - https://github.com/petermr/ami3/blob/master/README.md) . The top directory is a `CProject` and its document children are called `CTree`s as they are useful split into many subdirectory trees.

Each package has a maintainer. These are all volunteers. Their Python is all self-taught . There are also interns - mixture of compsci/engineers/plant_sci who have a 3-month stay. They test the tools, develop resources, explore text-mining, NLP, image analysis, machine-learning, etc. They are encouraged to use the packages, link them into Python scripts or Notebooks but don't have time for serious development. (They might add readers or exporters).

* pygetpapers , Ayush Garg. https://github.com/petermr/pygetpapers . Searches and downloads articles from repositories. Standalone, but the results may be used by docanalysis or possibly imageanalysis. Can be called from other tools. 

* docanalysis. Shweata Hegde. https://github.com/petermr/docanalysis . Ingests CProjects and carries out text-analysis of documents, including sectioning, NLP/text-mining, vocabulary generation. Uses NLTK and other Python tools for many operations, and spaCy, scispaCy for annotation of entities. Outputs summary data, correlations, word-dictionaries. Links entities to Wikidata.

* pyamiimage, Anuv Chakroborty + PMR. https://github.com/petermr/pyamiimage . Ingests Figures/images,  applies many image processing techniques (erode-dilate, colour quantization, skeletons, etc.), extracts words (Tesseract) , extracts lines and symbols (uses sknw/NetworkX) and recreates semantic diagrams (not finished)

* py4ami . PMR. https://github.com/petermr/pyami . Translation of ami3(J) to Python. Processes CProjects to extract and combine primitives into semantic objects. Some functionality overlaps with docanalysis and imageanalysis. Includes libraries (e.g. for Wikimedia) and includes prototype GUI in tkinter, and a complex structure of word-dictionaries covering science and related disciplines. (Note the project is called pyami locally but there is already a PyAMI project so there it is called py4ami)

All packages aim to have a common commandline approach, use config files, generate and process CProjects (e.g. iterating over CTrees and applying filters, transformers, map/reduce, etc.).  All 4 packages have been uploaded to PyPI

# basicTest

Checks that the Python environment works (independently of the applications)
https://github.com/petermr/basicTest/blob/main/README.md

# presentations

Some presentations about the software, many from collaborators/interns

## pygetpapers

* https://youtu.be/pUjiNzLVHLY (@ayushGarg) 5 min

## notebook
* https://github.com/petermr/docanalysis/blob/main/resources/docanalysis_demo.ipynb

## docanalysis

* docanalysis slides (MADICES): https://github.com/petermr/CEVOpen/blob/master/outreach/docanalysis_demo_madices.pdf

## wikidata

* WikidataCon Presentation slides and recording: https://github.com/petermr/crops/tree/main/outreach/WikidataCon2021
