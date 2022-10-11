# Lab Report on Research Artifact

* Date of examination: 12.07.22
* Start time: 12:30
* End time: 17:30

* Date of examination: 15.07.22
* Start time: 17:00
* End time: 19:30

## Metadata

* Paper DOI (necessary): 10.1145/2509136.2509531
* Artifact DOI (optional):
* Badges achieved in regular artifact evaluation: Artifact Evaluated
* Time (in minutes) needed to read the paper: 40

## Availability

* [ ] Artifact is archived in a public archive with a long-term retention policy (which one(s)?)
* [x] Artifact is available on a different website (which one(s)? - https://soft-dev.org/pubs/files/storage_strategies/
* [ ] Artifact is available in the version that was submitted to artifact evaluation
* [ ] Artifact is available in the version that passed artifact evaluation
* [x] Artifact is available in a public version control system - BitBucket
* [x] Artifact is available in a self-contained form (container, VM)
* Time (in minutes) needed for the check: 15

### Checks performed

1. The link is mentioned in the paper.
2. Artifact is directly accessible from provided link by clicking ```Virtual Image: 0.3 (2013-08-06)```. There is a VM file to download. 
3. There is a source code file by clicking ```BitBucket repo```.
4. There is a standard version by clicking ```Standard: 0.3 (2013-08-06)```.

### Observations

1. The provided link includes the paper,  the guide, Virtual Image, full source code. (Positive) 
2. In ```Getting Started (Step-by-step instructions)```, the selection of ```vboximg.ova``` is specified here, which is different from the alternative one, i.e. ```storage_strategy_benchmarks-0.3.ova```. (Neutral)

## Artifact Type

* [x] Code
* [ ] Dataset
* [ ] Automated proof
* [ ] Manual proof
* [ ] Other (please specify)
* Time (in minutes) needed for the check: 5

### Checks performed

1. Import the Virtual Image ```storage_strategy_benchmarks-0.3.ova``` file into the Virtualbox.
2. In BitBucket repo there are ```*.sh``` files.
3. After several attempts and even after reinstallation, the ```storage_strategy_benchmarks-0.3.ova``` can run and mouse is clickable. (Positive)

### Observations

1. After running the virtual image, there is a graphical interface, but the mouse cannot be displayed, based on the correct settings. Therefore no further progress is possible (e.g. follow instructions, open Terminal to make). (Negative)
2. ```BitBucket repo``` and ```Standard: 0.3 (2013-08-06)``` are the same. (Neutral)

## Functional

* [x] Artifact is considered functional
* [ ] Artifact is NOT considered functional
* Time (in minutes) needed for the check: 180

### Checks performed

1. Followed the instructions mentioned in https://soft-dev.org/pubs/files/storage_strategies/getting-started.html. At first, I only considered the ```standard``` folder. So it kept reporting errors, and I searched for solutions, and it reported new errors.
1.1. Before modifying the address in Makefile 
    1) ```storage_strategy_benchmarks-0.3.ova```:  
        1. Need to upgrade Ubuntu to version 14.04 first.
        2. Enter ```cd standards```, then ```make```.
    2) BitBucket repo:
        1. Cloned the ```storage_strategy_benchmarks BitBucket repo``` into my VM, simply ran ```$ make```.
        2. Checked the clone link, also the link mentioned in README later, i.e. https://bitbucket.org/pypy/pypy.
1.2. After modifying the address in Makefile 
    For all methods, first needed to modify the benchmarks address in the Makefile to ```hg clone https://foss.heptapod.net/pypy/benchmarks pypy-benchmarks```.

2. Because there were always different errors that occur, I tried to navigate to the ```prebuilt``` folder in ```storage_strategy_benchmarks-0.3.ova```, and ran ```make```.

### Observations

(Negative)  
Using ```$ make``` in ```standard/``` folder for ```storage_strategy_benchmarks-0.3.ova VM```:  
- Before modifying the address in Makefile 
```
$ make
hg clone https://bitbucket.org/pypy/benchmarks pypy-benchmarks
make: hg: No such file or directory
make: *** [Makefile:40: pypy-src] Error 127
```
- After modifying the address in Makefile 
```
$make
hg clone clone https://foss.heptapod.net/pypy/benchmarks pypy-benchmarks  
abort: error: _ssl.c:510: error:1409442E:SSL routines:SSL3_READ_BYTES:tlsv1 alert protocol version
make: *** [pypy-src] Error 255
```

(Positive)  
Using ```$ make``` in ```prebuilt/``` folder:
The main results showed in the folder ```tables/``` and ```diagrams/```.

Note: Because there is no  ```prebuilt/``` folder in ```BitBucket repo``` and ```Standard: 0.3 (2013-08-06)```, therefore, these two should be marked as non-functional and non-reusable. The following parts are around the artifact ```storage_strategy_benchmarks-0.3.ova```.

## Reusable

* [x] Artifact is considered reusable
* [ ] Artifact is NOT considered reusable
* Time (in minutes) needed for the check: 10

### Checks performed

1. For the certain case: ```storage_strategy_benchmarks-0.3.ova``` and ```cd prebuilt/```, we can find the results (the tables (in latex format) in the folder ```tables/``` and the diagrams (as pdf) in ```diagrams/```).

### Observations

1. It's easy to check the reusability for the case by running ```$ make```. (Positive)
2. The files in tables directory are .tex suffixed. (Neutral)

## Result reproducibility with the artifact

### To which degree *can* the artifact support claims from the paper?

* [ ] Results from the paper are fully supported by the artifact (i.e., it should in theory be possible to reproduce all results from the paper)
* [x] Results from the paper are partially supported by the artifact
* [ ] Results from the paper are not supported by the artifact

### To which degree *does* the artifact support the claims it *can* support?

* [x] Results that are supported by the artifact could be fully reproduced
* [ ] Results that are supported by the artifact could be partially reproduced
* [ ] Results from the paper could not be reproduced
* Time (in minutes) needed for the check: 20

### Checks performed

1. Compared the diagram (```transitions.pdf```) with Figure 6 mentioned in the paper. 
2. Since files in the folder ```tables/`` are .tex suffixed, they couldn't visually compare to the tables mentioned in the paper.

### Observations

1. There are some numerical differences for the ```transitions diagram```. (Neutral)
2. ```*.tex``` files cannot be transformed to tables correctly, which leads to no comparison between results and paper. (Negative)