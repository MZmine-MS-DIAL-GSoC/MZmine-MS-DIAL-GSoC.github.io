Visit the [MZmine](https://www.mzmine.org/) ([source](https://github.com/mzmine/mzmine3)) and [MS-DIAL](http://prime.psc.riken.jp/compms/msdial/main.html) websites.

# MZmine and MS-DIAL
The two software tools are fueling scientific data analysis of multidimensional mass spectrometry data. Working together on collaborative projects in the past, our teams are now joining together for Google Summer of Code. Previous collaborative publications include:

Schmid, Robin, Daniel Petras, Louis-Félix Nothias, Mingxun Wang, Allegra T. Aron, Annika Jagels, Hiroshi Tsugawa, et al. 2021. “Ion Identity Molecular Networking for Mass Spectrometry-Based Metabolomics in the GNPS Environment.” Nature Communications 12 (1): 3832.

Nothias, Louis-Félix, Daniel Petras, Robin Schmid, Kai Dührkop, Johannes Rainer, Abinesh Sarvepalli, Ivan Protsyuk, Ernst, Madeleine, Tsugawa, Hiroshi et al. 2020. “Feature-Based Molecular Networking in the GNPS Analysis Environment.” Nature Methods 17 (9): 905–8.

# About MS-DIAL 
Tsugawa, Hiroshi, Kazutaka Ikeda, Mikiko Takahashi, Aya Satoh, Yoshifumi Mori, Haruki Uchino, Nobuyuki Okahashi, et al. 2020. “A Lipidome Atlas in MS-DIAL 4.” Nature Biotechnology 38 (10): 1159–63.

Tsugawa, Hiroshi, Tomas Cajka, Tobias Kind, Yan Ma, Brendan Higgins, Kazutaka Ikeda, Mitsuhiro Kanazawa, Jean VanderGheynst, Oliver Fiehn, and Masanori Arita. 2015. “MS-DIAL: Data-Independent MS/MS Deconvolution for Comprehensive Metabolome Analysis.” Nature Methods 12 (6): 523–26.


# About MZmine
Mass spectrometry is an analytical technique that measures the mass of small molecules with high precision. The data coming from mass spectrometry instruments is complex and multi-dimensional. MZmine is an open-source graphical software for mass-spectrometry data processing. It is very popular among academic labs that work on metabolomics - the publication about MZmine 2 has received over 2500 citations to date. MZmine 3 is based on modern Java19 and JavaFX for its user interface.

Schmid, Robin, Heuckeroth, Steffen, Korf, Ansgar, et al. MZmine 3. in review. 2023

Pluskal, Tomás, Sandra Castillo, Alejandro Villar-Briones, and Matej Oresic. 2010. “MZmine 2: Modular Framework for Processing, Visualizing, and Analyzing Mass Spectrometry-Based Molecular Profile Data.” BMC Bioinformatics 11 (July): 395.


# History with GSoC
MZmine successfully participated in Google Summer of Code in the years 2017, 2018, and 2019 under the [OpenChemistry](https://www.openchemistry.org/) umbrella, and in 2020 and 2022 as its own organization.

# For GSoC contributors - How to apply?
Please check out Google's [FAQ](https://developers.google.com/open-source/gsoc/faq#what_are_the_eligibility_requirements_for_participation) and see if you’re eligible for the GSoC. Also, make careful note of the GSoC 2023 [timeline](https://developers.google.com/open-source/gsoc/timeline) in your calendar. We welcome applications from all contributors, but especially from those interested in chemistry, biology, and/or mass spectrometry. Please feel free to reach out to individual mentors if there is a specific project you are interested in. As part of the application process, we may ask you to work on simple, outstanding issues on our Github page, or to implement a small piece of code so we can get an idea about your coding skills. For more information and to apply, please contact the MZmine GSoC administrators by email: (mzmine.msdial.gsoc@gmail.com).


# Project ideas

## Projects mentored by MZmine

### Molecular networking support
Brief explanation: Molecular networking connects mass spectral fingerprints by various similarity metrics creating multi-layered graphs. This technology is changing how chemical compound discovery is done nowadays. MZmine supports various similarity metrics and interactive visualization. This project shall extend the network analysis and visualization options by options to filter and collopse based on graph topology.   

Expected project size: 175 or 350 hour
Expected outcome: Interactive visualization of thousands of chemical compounds and their fingerprint similarities, made digestable by topological filtering.
Difficulty: easy
Prerequisites: Java, JavaFX
Possible mentor: [Robin Schmid](https://github.com/robinschmid)

### Mass Spectrometry Query Language Integration
Brief explanation: Develop support for the Mass Spectrometry Query Language (MassQL) in MZmine. MassQL is a simplified way for users to query for signals and patterns in complex mass spectrometry data across millions of mass spectra. In the first step, the MassQL web API will parse queries into json representations to filter and visualize mass spectrometry data in MZmine. In a second step, a java library should implement a parser and engine to handle MassQL queries and drive further development in MZmine.

Expected project size: 175 or 350 hour
Expected outcome: Advanced query options for mass spectrometry data, JavaFX user interfaces
Difficulty: medium
Prerequisites: Java, JavaFX
Possible mentor: [Robin Schmid](https://github.com/robinschmid)

### New data visualization modules
Brief explanation: Implement new JavaFX-based visualization modules for MZmine such as Cloud Plot and Robust Volcano Plot. This project requires active use of JavaFX and chart plotting libraries - we mostly use JFreeChart.

Expected project size: 175 hour
Expected outcome: The contributer will get a deeper understanding of mass spectrometry data and data structures. The MZmine community will gain new data analysis tools readily integrated with other charts and views. 
Difficulty: easy
Prerequisites: Java, JavaFX
Possible mentor: [Tomas Pluskal](https://github.com/tomas-pluskal)


## Projects mentored by MS-DIAL

### Exporter migration from version 4 to 5
Brief explanation:  Development of exporter support for MS-DIAL version 5. The previous version 4 had exporters to connect to many other data formats and databases after processing the raw MS data, but the latest version 5 doesn't implement them yet.
The idea is to have 1) an export function for the MRMPROBS library 2) an mztab-M exporter 3) a format exporter for MassBank and MGF files.

Expected project size: 175 hour
Difficulty: easy
Prerequisites: C#, .Net
Possible mentor: [Yuki Matsuzawa](https://github.com/YukiMatsuzawa), [Hiroshi Tsugawa](https://github.com/htsugawa)

### Network visualization automation with MS-DIAL 5 and Cytoscape

Brief explanation: MS/MS similarity and metabolite profile correlations are calculated as the MS-DIAL output to be used in cytoscape.
The idea is to develop a visualisation workflow for MS-DIAL 5 that implements a function to generate data for such network visualisation and passes it to the network visualisation software [Cytoscape](https://cytoscape.org/).

Expected project size: 175 hour
Difficulty: easy
Prerequisites: C#, .Net
Possible mentor: [Kozo Nishida](https://github.com/kozo2), [Hiroshi Tsugawa](https://github.com/htsugawa)

### Predicting moleculer formula, metabolite class, and structure elucidation using MS-FINDER functions

Brief explanation: MS-FINDER is a partner program of MS-DIAL. MS-FINDER supports the molecular formula, the metabolite class, and the structure predictions for unknown mass spectra. Although MS-FINDER is currently available as an independent program, the functions are implemented in MS-DIAL at this project. The input is the mass spectrum query available in MS-DIAL, and the output is the formula, class, and structure descriptions predicted. [MS-FINDER](http://prime.psc.riken.jp/compms/msfinder/main.html).

Expected project size: 350 hour
Difficulty: medium
Prerequisites: C#, .Net
Possible mentor: [Yuki Matsuzawa](https://github.com/YukiMatsuzawa), [Hiroshi Tsugawa](https://github.com/htsugawa)

### A commandline application of MS-DIAL

Brief explantion: MS-DIAL is a graphical interface program. On the other hand, many users want to use it as a command line tool. The input is mass spectrometry raw data and the output is the metabolome table to be used for statistical analyses. Moreover, for users who want to visualize the data by MS-DIAL, the save format file is also generated from the command line tool as the option.

Expected project size: 350 hour
Difficulty: medium
Prerequisites: C#, .Net
Possible mentor: [Yuki Matsuzawa](https://github.com/YukiMatsuzawa), [Hiroshi Tsugawa](https://github.com/htsugawa)
