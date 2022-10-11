# Lab Report on Research Artifact

* Date of examination: 11.07.22
* Start time: 22:45
* End time: 03:30

* Date of examination: 15.07.22
* Start time: 14:00
* End time: 16:00

* Date of examination: 16.07.22
* Start time: 12:30
* End time: 16:00

## Metadata

* Paper DOI (necessary): 10.1145/2983990.2983998
* Artifact DOI (optional): N/A
* Badges achieved in regular artifact evaluation: Artifact Evaluated
* Time (in minutes) needed to read the paper: 60

## Availability

* [ ] Artifact is archived in a public archive with a long-term retention policy (which one(s)?)
* [x] Artifact is available on a different website (which one(s)?) - https://www.repository.cam.ac.uk/handle/1810/261804
* [ ] Artifact is available in the version that was submitted to artifact evaluation
* [ ] Artifact is available in the version that passed artifact evaluation
* [ ] Artifact is available in a public version control system
* [x] Artifact is available in a self-contained form (container, VM)
* Time (in minutes) needed for the check: 5

### Checks performed

1. Artifact is directly accessible from provided link.
2. But there are still other 2 github repositories which are relevant to this paper. https://github.com/stephenrkell/libcrunch and https://github.com/stephenrkell/liballocs.

### Observations

1. Artifact is provided in VM form.
2. Two github repositories seem different from the artifact.

## Artifact Type

* [ ] Code
* [ ] Dataset
* [ ] Automated proof
* [ ] Manual proof
* [x] Other (please specify) - Commands
* Time (in minutes) needed for the check: 2

### Checks performed

1. Log in using the username "user" and password "user".
2. Use cd command to navigate.

### Observations

1. Artifact is in Command-Line Interface(CLI) form. (Neutral)
2. But for us (as users), this is not convenient. The biggest problem is that the page cannot be pulled up, so the previous content is not visible. README cannot be displayed entirely. In order to display it, vim needs to be used instead of cat, however the vim command also has to be installed additionally. Also, the mouse is not visible, so copy and paste operations are not possible. (Negative)

## Functional

* [ ] Artifact is considered functional
* [x] Artifact is NOT considered functional
* Time (in minutes) needed for the check: 130

### Checks performed

1. Checked the README in the '/usr/local/src/oopsla-artifact' directory, and found out that I needed to check the README in the 'src/libcrunch/' directory.
2. For the two README files in two directories, I followed the steps.
3. Therefore, there is no way to reach the "using SPEC CPU2006 to reproduce the experimental results" part. And define this artifact as non-functional.
4. Besides, I tried the command in README in liballocs repo to run a smiple demo in a container in my VM. This also didn't work.
5. Tried running them all again and summarized the results.

------------------------------------------------------------------
Reinstallation and Rerun  
Hint: Because it took so many time to switch the keyboard to the US keyboard unsuccessfully, found out how to output ```\``` symbol under the UK keyboard (Macbook): ```Option```+```-```  
1. Followed the ```README``` in the ```/usr/local/src/oopsla-artifact``` directory.
2. Ran ```make -C contrib -j3```. There were some warning reports.
3. Ran ```./autogen.sh```. There were warning reports. ```aclocal: warning: couldn't open directory 'm4': No such file or directory```
4. Re-ran ```make -C contrib -j3```. The warnings before didn't show.
5. Re-ran ```./autogen.sh```. Seemed successful, no reports.
6. Continued the commands until.
7. Ran ```make -f "$LIBALLOCS"/tools/Makefile.allocsites \ /usr/lib/allocsites$( readlink -f /lib/x86_64-linux-gnu/libc.so.6 )-types.so```.  There were warning reports. 
```
make: /tools/Makefile.allocsites: No such file or directory
make: *** No rule to make target '/tools/Makefile.allocsites'. Stop.
```
8. Then checked the contents under folder ```/usr/local/src/oopsla-artifact/src/liballocs/tools``` using ```ls```, and found out that the file ```Makefile.allocsites``` exists.
9. Since I've spent too much time on it with no progress, there were no further actions about this artifact.

### Observations

1. For the instructions in two README, both could not continue because errors were reported. (Negative)
2. For the simple demo in a container for liballocs repo. The second command `$ docker build -t liballocs_built liballocs/buildtest/debian-stretch` failed (didn't work), and the VM stuck, so there was no further progress. (Negative)
Note: Related error reports are displayed in the error directory. ```rerun_no_rule_to_make_target.png``` is the report after reinstallation and rerun. ```rerun_no_rule_to_make_target.txt``` is its text form.

## Reusable

* [ ] Artifact is considered reusable
* [x] Artifact is NOT considered reusable
* Time (in minutes) needed for the check: 2

### Checks performed

1. Since the artifact is non-functional, therefore, it's not reusable.

### Observations

N/A

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

1. Since the artifact cannot run, there is no result for artifact to support claims from the paper.

### Observations

N/A
