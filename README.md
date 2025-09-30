# YOUR PROJECT TITLE HERE

This repository contains the experiments, data, analyses, and figures for the paper
"[YOUR PAPER HERE](https://google.com)" by Author 1 and Author 2 (Year, Venue).

__Contents__:
Describe the contents of the repository here, e.g.;
- [Introduction](#introduction)
- [Preregistrations](#preregistrations)
- [Repository structure](#repository-structure)
- [CRediT author statement](#credit-author-statement)

## Introduction
A summary abstract and (potentially) your key figure here.

## Preregistrations
Your preregistration links here

## General points

- for each project:
	+ create a private repo for project development (incl. sensitive files)
	+ create a public repo for project presentation
- for folder and file names: 
	+ don't use white space in either folder or filenames, use an underscore "_" instead
	+ use lower case only
    + in cases where files should be read sequentially - such as steps in an analysis pipeline with dependencies between them, or multiple submissions of a paper - start each filename with a number so that they're read out in the intended order. See "Repository structure," below for specific guidelines for different types of files. 
- always use relative paths in your code
	+ for example, to save a figure from an R script inside the `code` folder, the path should be "../../figures/figure_name.pdf"
- keep your folder structure organized
	+ we recommend adhering to the folder structure in this repository 
	+ more complex projects may have additional folders such as `videos/`, `tables/`, ...
- note: some of the folders are empty except for a `.keep` file
	+ the `.keep` file is just there to make sure that github includes the otherwise empty folder 
	+ feel free to delete the `.keep` file once you've added another file to that folder
- each code subfolder has a readme file that should be updated with information about the code scripts 
- use github issues to keep track of any larger decisions that we make along the way 
- make sure to create a slack channel for each project, link up the github repository with the slack channel, and add the people working on the project to the github repo and slack channel 

## Repository structure 

```
├── code
│   ├── experiment
│   ├── preprocessing
│   └── analysis
├── data
│   ├── raw
│   └── processed
├── figures
├── materials
├── presentation
├── writeup
```

### code 
Put all your code here. There are subfolders for experiment code, preprocessing code, and analysis code.

* **experiments**: The experiments folder is for the online (or in lab) experiments. Each experiment should be in its own subfolder. When you run another experiment, make sure to create a new folder (so that we always know what an experiment looked like when it was run). In readme file for the experiments folder, provide a brief summary of each experiment. Also note down any additional information that may not be saved within each experiment (e.g. how much the payment was for MTurk participants).
* **preprocessing**: The preprocessing folder is for converting raw data to "clean" data that is ready to share. Use these scripts to make changes like removing identifying information from data or wrangling data into a well-organized csv file.
* * **analysis**: All your analyses on cleaned data live here!
  * For multi-experiment projects with multiple analysis files per experiment, consider splitting this subfolder by experiment (e.g., `exp1/` `exp2/` `exp3/`).
  * For projects with complex data processing pipelines, consider splitting this folder into numbered subfolders based on steps in the processing pipeline (e.g., `01_demographics/` `02_maplog`/ etc.) and numbering scripts inside each subfolder in the order that they should be executed. This naming convention allows other researchers—including you, in the distant future—to reproduce your analyses by running the analysis scripts in the correct order. You can find an example of this folder organization at work [here](https://github.com/nataliavelez/OHOL_Tech).

### data 

* **raw**: Store raw data here. **NEVER alter raw data data.** Any changes that you make to the data should be saved in the "processed" folder, or done online in your analysis scripts.
* **processed**: Store data here after preprocessing. In the README for processed data, add a codebook summarizing the structure of the data (e.g., which column correspond to which measure). You can find an example codebook [here]().

For multi-experiment experiment projects, add subfolders within the "raw" and "processed" folders corresponding to different experiments. For experiments with complex data analysis pipelines and lots of intermediate outputs, you may want to add subfolders within the "processed" folder corresponding 

### figures 
Save all your figures and display elements here. You may want to include additional subfolder here such as `plots/`, `diagrams/`, `tables/` etc. 

### materials
Put experiment stimuli and other materials here that are relevant for your project.

### presentation
Put your project presentation here (e.g. your keynote, powerpoint, google slides, or pdf file). You may want to include an additional subfolder called `assets/` for any display elements used in the presentation, such as cute videos, illustrations, etc.

### writeup 
Put all your writing here. This folder structure is likely to expand for more complex projects. For example, you could add a subfolders like folders `journal/01_cognition/sub01/`, `conference/2025-01_cogsci/resubmission/` etc. Best practices: 

* Number each written work chronologically; in the examples above, the folders are numbered with the order in which the author submitted to journals (`01_cognition`) or with the deadline for conference proceedings (`2025-01_cogsci`). Whatever you choose, make sure it's consistent within a folder!
* Create separate subfolders for each submission to the same journal, e.g., `initial_submission`, `rev1`, `rev2`. Do _not_ alter files within a submission after they've been sent out.

## CRediT author statement 

Each public repository should have a [credit author statement](https://www.elsevier.com/authors/policies-and-guidelines/credit-author-statement) 

| Term                       | Definition                                                                                                                                                                                                    |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Conceptualization          | Ideas; formulation or evolution of overarching research goals and aims                                                                                                                                        |
| Methodology                | Development or design of methodology; creation of models                                                                                                                                                      |
| Software                   | Programming, software development; designing computer programs; implementation of the computer code and supporting algorithms; testing of existing code components                                            |
| Validation                 | Verification, whether as a part of the activity or separate, of the overall replication/ reproducibility of results/experiments and other research outputs                                                    |
| Formal analysis            | Application of statistical, mathematical, computational, or other formal techniques to analyze or synthesize study data                                                                                       |
| Investigation              | Conducting a research and investigation process, specifically performing the experiments, or data/evidence collection                                                                                         |
| Resources                  | Provision of study materials, reagents, materials, patients, laboratory samples, animals, instrumentation, computing resources, or other analysis tools                                                       |
| Data Curation              | Management activities to annotate (produce metadata), scrub data and maintain research data (including software code, where it is necessary for interpreting the data itself) for initial use and later reuse |
| Writing - Original Draft   | Preparation, creation and/or presentation of the published work, specifically writing the initial draft (including substantive translation)                                                                   |
| Writing - Review & Editing | Preparation, creation and/or presentation of the published work by those from the original research group, specifically critical review, commentary or revision – including pre-or postpublication stages     |
| Visualization              | Preparation, creation and/or presentation of the published work, specifically visualization/ data presentation                                                                                                |
| Supervision                | Oversight and leadership responsibility for the research activity planning and execution, including mentorship external to the core team                                                                      |
| Project administration     | Management and coordination responsibility for the research activity planning and execution                                                                                                                   |
| Funding acquisition        | Acquisition of the financial support for the project leading to this publication                                                                                                                              |

**Sample CRediT author statement**
- Zhang San: Conceptualization, Methodology, Software 
- Priya Singh: Data curation, Writing- Original draft preparation
- Wang Wu: Visualization, Investigation 
- Jan Jansen: Supervision 
- Ajay Kumar: Software, Validation
- Sun Qi: Writing-Reviewing and Editing


