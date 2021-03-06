Plugin Machine Intelligence
============================

The Plugin Machine Intelligence (PMI) project is a plugin for the Pentaho Kettle engine that (initially) provides access to supervised machine learning algorithms from various underlying "engines". Out of the box, PMI provides five engines: Weka, Python scikit-learn, R MLR, Spark MLlib and DL4j (deep learning). The following learning schemes are supported, and are available in most of the engines: decision tree classifier, decision tree regressor, gradient boosted trees, linear regression, logistic regression, naive Bayes, naive Bayes multinomial, naive Bayes incremental, random forest classifier, random forest regressor, support vector classifier, support vector regressor, multi-layer perceptrons and deep learning networks. PMI is designed to be extensible via the addition of new engines and algorithms.

Building
--------
The PMI Plugin is built with Maven.

    $ git clone https://github.com/pentaho-labs/pentaho-machine-intelligence.git
    $ cd pentaho-machine-intelligence
    $ mvn install

This will produce a plugin archive in target/plugin-machine-intelligence-${project.revision}.zip. This archive can then be extracted into your Pentaho Data Integration plugin directory.

Requirements
---------------
The Weka engine is bundled with PMI, so no further installation is required for this. The MLlib engine's requirements are taken care of automatically by a one-time download of a Weka Spark plugin. This download is done automatically (assuming there is an active internet connection) and will delay the startup of PDI while the download is occurring. The Python scikit-learn engine requires python to be installed on the machine that PDI will be executed on. Both python 2.7 and 3.x are supported. Within python, pandas, numpy, scipy and matplotlib are required. The Anaconda distribution of python is a simple way to get started (especially for Windows users) as it comes with hundreds of packages pre-installed. The python executable must be in the PDI user's PATH. The R MLR engine requires R to be installed and the rJava package installed within R. The R executable must be in the PDI user's path. Further R package requirements are detailed in the PMI installation documentation.

License
-------
Licensed under the GNU GENERAL PUBLIC LICENSE, Version 3.0. See LICENSE.txt for more information.
