# Lab Report on Research Artifact

* Date of examination: 08.07.22
* Start time: 14:15
* End time: 15:30

* Date of examination: 09.07.22
* Start time: 14:45
* End time: 16:20

* Date of examination: 14.07.22
* Start time: 16:30
* End time: 17:00

Note: With help by Terence Stenvold via Discord. His contributions included mainly:  
1. Let me check the *.aux files for proof that the coq proofs did happen.
2. Some hints on what I can add to the report, e.g. the aux outputs in the results directory, explain that without a deep understanding of the problem, reuse of artifacts by users is difficult (which is the last sentence of the last point in ```Observations``` in ```Result reproducibility with the artifact```).

## Metadata

* Paper DOI (necessary): 10.1145/3371109
* Artifact DOI (optional): 10.5281/zenodo.3541779
* Badges achieved in regular artifact evaluation: Artifacts Evaluated & Reusable, Artifacts Available
* Time (in minutes) needed to read the paper: 80

## Availability

* [ ] Artifact is archived in a public archive with a long-term retention policy (which one(s)?)
* [ ] Artifact is available on a different website (which one(s)?)
* [ ] Artifact is available in the version that was submitted to artifact evaluation
* [ ] Artifact is available in the version that passed artifact evaluation
* [x] Artifact is available in a public version control system - Gitlab
* [x] Artifact is available in a self-contained form (container, VM)
* Time (in minutes) needed for the check: 5

### Checks performed

1. Artifact is directly accessible from provided link.
2. Artifact is mentioned in the paper in VM form. [https://zenodo.org/record/3541779#.YsiPTuxBw88]
3. There is also a gitlab project. [https://gitlab.mpi-sws.org/FP/stacked-borrows]

### Observations

1. The artifact was published at November 14, 2019. However, there were still some modifications in gitlab project 1 year ago. (Neutral)
2. The artifact provides appendix and README provides some examples. (Positive)

## Artifact Type

* [x] Code
* [ ] Dataset
* [x] Automated proof
* [ ] Manual proof
* [ ] Other (please specify)
* Time (in minutes) needed for the check: 10

### Checks performed

1. Based on the instructions/tutorials mentioned in README, I need to write some commands to build the artifact.
2. There are some example code.
3. Check the contents of relevant files (*.v) in gitlab.

### Observations

1. The artifact has a README, which contains 'How To Start', 'Structure' and other important information. (Positive)

## Functional

* [x] Artifact is considered functional
* [ ] Artifact is NOT considered functional
* Time (in minutes) needed for the check: 5

### Checks performed

1. Followed the instructions, installed the dependencies via opam, rebuilded and make the results successfully. 
2. Checked the _CoqProject file via command ```cat _CoqProject```. And compared it with the file in gitlab project.

### Observations

1. There are 3 examples in README about Rust Counterexamples and Miri, the second one needed to be modified. (Neutral)
2. Unlike paper, the use of the identifier 'retag' always resulted in an error. (Negative)
3. The content of the generated files are the same, e.g. _CoqProject, opt/ex1_down.v. (Positive)  
Note: The error report for the example code is in the file documentation.pdf.

## Reusable

* [x] Artifact is considered reusable
* [ ] Artifact is NOT considered reusable
* Time (in minutes) needed for the check: 10

### Checks performed

1. After build, check the content in ```theroies``` directory, which contains ```lang```, ```opt``` and ```sim``` directories.

### Observations

1. The documentation (README) was well-structured. (Positive)
2. In these three directories, there are already existing ```*.v```, ```*.vo``` and ```*.glob``` files. (Positive)
3. For the various example files mentioned by the authors in Structure and Simulation Framework parts, I could only view their contents and had no way of knowing how the authors arrived at the relevant conclusions/observations. There is no relevant instructions for those parts. (Negative)

## Result reproducibility with the artifact

### To which degree *can* the artifact support claims from the paper?

* [ ] Results from the paper are fully supported by the artifact (i.e., it should in theory be possible to reproduce all results from the paper)
* [x] Results from the paper are partially supported by the artifact
* [ ] Results from the paper are not supported by the artifact

### To which degree *does* the artifact support the claims it *can* support?

* [x] Results that are supported by the artifact could be fully reproduced
* [ ] Results that are supported by the artifact could be partially reproduced
* [ ] Results from the paper could not be reproduced
* Time (in minutes) needed for the check: 50

### Checks performed

1. Built the artifact and checked the results.
2. Checked the ```*.aux``` files to show that the proofs are actually conducted.  
Note: The detailed proof contents for the files mentioned in ```Structure``` and ```Simulation``` parts are in the results directory.

### Observations

1. From the point of view of compile and build, the files are constructed using this Stacked Borrows compiler proposed by the authors and no errors are reported, as well as the results, including __CoqProject and all other generated files, are consistent. (Positive)
2. In paper there are some code blocks, and they are executed on the website https://play.rust-lang.org/. From this perspective, 'retag' cannot work. (Negative)
3. Combine 1 and 2, the artifact actually only does the build function and view the generated files, and executing the code to observe its results is actually done on a different platform. However, how to handle the generated v-files and how to evaluate them is not explained in the guide. The proofs are complicated. It's easy to only check the results via ```cat```, but it would be difficult to reuse without very deep understanding of the problem or the methods. (Negative)