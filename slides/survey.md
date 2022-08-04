# Survey of _hep-lat_ in 2021

-

## Survey scope

* Every hep-lat arXiv submission from 2021
  * Including cross-lists
  * Skim-read plus keyword searches
* Series of questions: yes/no, categorisation, and free text
  * Answers based solely on text of paper
* Data and analysis code are available on [Zenodo](https://doi.org/10.5281/zenodo.6584001)

-

## What computations does an LFT paper do?

A very reductive view:

1. Generate field configurations
2. Measures observables on configurations
3. Analyses, plots, tabulates measured observables

Less focus on emerging techniques, e.g.

* tensor networks
* quantum simulation

-

## High level numbers

Out of 1,229 arXiv submissions in 2021:

![Bar charts breaking down arXiv submissions](plots/all_numerical.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

* Use of preprints is already decades ahead of many disciplines! <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## Why cite software?

Citing software:
* Gives credit to those who built it
  * Avoids paper-centric metrics
  * Justifies funding maintenance
* More precisely specifies what was done
  * Implementations vary in subtle details
  * Referring to an algorithm is not sufficient

-

## Setting the scene: Acknowledging HPC

![Bar chart breaking down arXiv submissions by whether they acknowledge HPC resources. The majority of hep-lat submissions do; most crosslists do not.](plots/acknowledges_compute_resources.svg)

-

## How many submissions specify _any_ software?

![Bar chart breaking down arXiv submissions by whether they acknowledge software. The majortity do not.](plots/specifies_any_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="1000px" -->

---

## Generating field configurations

* Usually extremely expensive
  * Hard to test automated workflows end-to-end
  * Hard for others to reproduce (wait for Moore's law?)
  * Open sharing of configurations is good
    * Needs infrastructure (more later)
* Reproducibility efforts include:
  * Seedable RNG, RNG checkpoints
  * Include run parameters in output, configurations files
  * Include code version/commit ID within output
* Around 44% of publications do this

-

## Do authors specify how configurations are generated?

![Bar chart breaking down whether publications specify what software was used for generating configurations; the majority do not.](plots/specifies_configuration_generation_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## What software is used to generate configurations?

![Bar chart showing the top ten software packages used for configuration generation. Out of 100 papers, 14 use openQCD, 9 CL2QCD, and 7 each MILC, HiRep, FGrid, Chroma, BQCD](plots/configuration_generation_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

* 11 indicate unreleased modifications <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
* More only name toolkits (e.g. Grid, Chroma) <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

---

## Sharing configurations

* International Lattice Data Grid
  * Defines protocols and standards
  * Local deployments (Regional Grids) in US, UK, Europe, Japan, Australia
* FAIR before FAIR
* Early-ish example of open science

-

## How many papers acknowledge ILDG/an RG?

![Bar chart breaking down whether papers acknowledge ILDG or a regional grid. Less than 5% do.](plots/acknowledges_data_grid.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="800px" -->

-

## Which services are acknowledged?

![Bar chart showing which lattice data sharing services are acknowledged. 14 of 14 use the JLDG; 10 also acknowledge ILDG.](plots/which_data_grids.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="700px"-->

* Japan has the most active(ly cited) LDG <!-- .element: class="fragment fade-in" data-fragment-index="2" -->
* Either the others aren't used, or aren't cited <!-- .element: class="fragment fade-in" data-fragment-index="2" -->

-

## Ongoing work on ILDG

* Perceived issues with ILDG:
  * DOIs, citability
  * Grid certificates
  * Rigidity of metadata
* ILDG committees recently resumed activity
  * Significant German government funding
  * Dedicated staff to address these problems
* Plenary update and lattice data lunch yesterday


-

## Performing measurements

![Bar chart breaking down whether publications specify what software was used for measurement. A significant majority internationally do not](plots/specifies_measurement_software.svg) <!-- .element width="700px" -->

-

## Do authors publish data?

![Bar chart breaking down how whether publications publish data. The overwhelming majority do not.](plots/publish_any_data.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="1300px" -->

-

## Where are data published?

![Bar chart showing where data are published. Out of 38 submissions, 12 publish data directly on the arXiv, 5 on GitLab, 3 each on Unibi and Zenodo.](plots/used_data_repositories.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="800px" -->

-

## Code development hosting services are fragile!

[![Screen shot of The Register article "GitLab plans to delete dormant projects in free accounts"](images/el-reg.png)](https://www.theregister.com/2022/08/04/gitlab_data_retention_policy/)

---

## Data analysis

* Experimental research:
  * Does not generate configurations
  * Does not perform computationally reproducible "measurements"
  * Still has a substantial reproducibility effort
  * $\Rightarrow$ Data analysis of measurement results is the key reproducibility question

-

## Do authors specify _any_ software used for analysis?

![Bar graph breaking down whether software used for data analysis is specified. The vast majority of publications do not specify any software.](plots/specifies_analysis_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="1100px" -->

-

## What software is specified?

![Bar graph showing the top 10 software packages acknowledged by hep-lat publications and crosslists. The top 5 in hep-lat are Mathematica, gvar, numpy, matplotlib, and lsqfit.](plots/acknowledged_analysis_software.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="1300px" -->

-

## Do authors publish a full analysis workflow?

![Bar graph breaking down whether authors publish a full or partial analysis workflow. The overwhelming majority do not; only single digit numbers out of a thousand publish in full.](plots/publish_analysis_workflow.svg) <!-- .element: class="fragment fade-in" data-fragment-index="2" width="900px" -->
