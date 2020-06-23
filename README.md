# SweetViz-Library
  ### It is a pandas-based library to visualize and compare datasets.
  
## Description:
     Sweetviz is an open source Python library that generates beautiful, high-density visualizations to 
  kickstart EDA (Exploratory Data Analysis) with a single line of code. Output is a fully self-contained HTML application.

    The system is built around quickly visualizing target values and comparing datasets. 
 Its goal is to help quick analysis of target characteristics,training vs testing data, and other such data characterization tasks.
  
## Installation

Sweetviz currently supports Python 3.6+ and Pandas 0.25.3+. Reports are output using the base "os" module, so custom environments such as Google Colab which require custom file operations are not yet supported, although I am looking into a solution.

   ### Using pip
The best way to install sweetviz (other than from source) is to use pip:

pip install sweetviz

## Basic Usage
Create a DataframeReport object, then use a show_xxx function to render the report.

Note: Currently the only rendering supported is to a standalone HTML file, using a "widescreen" aspect ratio (i.e. 1080p resolution or wider).

There are 3 main functions for creating reports:

analyze(...)
compare(...)
compare_intra(...)

## Analyzing a single dataframe (and its optional target feature)

To analyze a single dataframe, simply use the analyze(...) function, then the show_html(...) function:

import sweetviz as sv

my_report = sv.analyze(my_dataframe)
my_report.show_html() # Default arguments will generate to "SWEETVIZ_REPORT.html"
When run, this will output a 1080p widescreen html app in your default browser
