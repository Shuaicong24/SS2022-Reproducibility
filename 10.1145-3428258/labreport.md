# Lab Report on Research Artifact

* Date of examination: 17.07.22
* Start time: 13:00
* End time: 17:00

## Metadata

* Paper DOI (necessary): 10.1145/3428258
* Artifact DOI (optional): 10.5281/zenodo.4059797
* Badges achieved in regular artifact evaluation: Artifacts Available V1.1 & Artifacts Evaluated Functional V1.1
* Time (in minutes) needed to read the paper: 210

## Availability

* [x] Artifact is archived in a public archive with a long-term retention policy (which one(s)?) - zenodo
* [ ] Artifact is available on a different website (which one(s)?)
* [ ] Artifact is available in the version that was submitted to artifact evaluation
* [ ] Artifact is available in the version that passed artifact evaluation
* [ ] Artifact is available in a public version control system
* [ ] Artifact is available in a self-contained form (container, VM)
* Time (in minutes) needed for the check: 5

### Checks performed

1. Artifact is directly accessible from provided link
2. Artifact is provided in https://zenodo.org/record/4059797#.YtQTc-xBzaV.

### Observations

## Artifact Type

* [x] Code
* [ ] Dataset
* [ ] Automated proof
* [ ] Manual proof
* [ ] Other (please specify)
* Time (in minutes) needed for the check: 5

### Checks performed

1. Downloaded Docker Desktop Mac Version.
2. Followed the ```README.md``` and navigated to the directory ```/home/reviewer/gigahorse-toolchain```.
3. Checked the contents.

### Observations

## Functional

* [ ] Artifact is considered functional
* [x] Artifact is NOT considered functional
* Time (in minutes) needed for the check: 150

### Checks performed

First Try (in VM):
Same results as Second Try.  

Second Try (in Mac with Docker Desktop):
1. Navigated to ```/home/reviewer/gigahorse-toolchain``` folder and opened ```README.md```.
2. Followed the instructions.
3. Checked the Python version. But I found out no available solutions for updating the python version online.
4. Cloned ```souffle repo``` using HTTPS.
5. Navigated to the ```souffle``` directory and checked the contents using ```$ ls```.
6. Checked the contents in ```souffle-addon``` folder.
7. Cloned ```souffle-addon repo```.
7. First didn't consider the optional ones (```### For visualization part in README.md```).
8. Continued and couldn't find what to use to replace the contents of ```<contract>```.
9. Therefore, no further progress.

### Observations

1. In ```README.md```, it says that ```Python 3.8``` should be installed. The default python3 version is ```python 3.6.9```.
```
$ python3 -V
Python 3.6.9
```
2. In ```README.md```, it uses ```git clone git@github.com:souffle-lang/souffle.git``` (SSH), not HTTPS.
3. In ```souffle``` directory, there are no ```bootstrap``` or ```configure``` files.
```
$ ./bootstrap
/bin/sh: 30: ./bootstrap: not found
$ ./configure
/bin/sh: 31: ./configure: not found
$ ls
CMakeLists.txt	choco-packages.config  doxygen.in  sh	  utilities
LICENSE		    cmake		           licenses    src
README.md	    debian		           man	       tests
```
4. ```sudo``` is within docker unavailable.
```
$ sudo make install -j
/bin/sh: 32: sudo: not found
```
5. Nothing under ```souffle-addon``` folder (by default).
```
$ pwd
/home/reviewer/gigahorse-toolchain/souffle-addon
$ ls
```

## Reusable

* [ ] Artifact is considered reusable
* [x] Artifact is NOT considered reusable
* Time (in minutes) needed for the check: N/A

### Checks performed

Since the artifact is non-functional, therefore, it's not reusable.

### Observations

## Result reproducibility with the artifact

### To which degree *can* the artifact support claims from the paper?

* [ ] Results from the paper are fully supported by the artifact (i.e., it should in theory be possible to reproduce all results from the paper)
* [ ] Results from the paper are partially supported by the artifact
* [x] Results from the paper are not supported by the artifact

### To which degree *does* the artifact support the claims it *can* support?

* [ ] Results that are supported by the artifact could be fully reproduced
* [ ] Results that are supported by the artifact could be partially reproduced
* [x] Results from the paper could not be reproduced
* Time (in minutes) needed for the check: N/A

### Checks performed

Since the artifact cannot run, there is no result for artifact to support claims from the paper.

### Observations