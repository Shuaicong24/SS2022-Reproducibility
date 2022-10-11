# Seminar Report

* Name: Shuaicong Wu
* Lecturer: Dr.-Ing. Stefan Winter
* Course: Master-Seminar "Reproducibility of Software Engineering Research"
* Due Date: 28.07.2022

## Experience throughout the artifact evaluation process

This was a new experience for me, as I had not reproduced artifacts before, even had no idea about artifacts. My initial perception before phase two was that if an artifact had a relatively complete documentation and one or more badges, it would be relatively easy to reproduce the artifact. In practice, however, this was not the case.  

In the first phase we reviewed some of the literature. We talked about the different expectations of artifacts as reviewers and users, and about the factors that influence the dissemination and sharing of artifacts in the community. As users we cared about the reusability of the artifacts and whether the artifacts can run successfully and get the corresponding results according to the provided guidance. I have personally reproduced 2 of the 4 papers, so it is not good or bad. Since these papers were brand new to me, I would have finished the lab report with only a superficial or almost no understanding of them when I only reproduce the results according to the instructions. When some errors were reported in the process, I tried to find solutions and fix them, and if it worked, all was well. But it was a helpless and even frustrating process to keep reporting errors, even with different errors on multiple runs.

There are five in total, one of which is hardware unavailable, specifically insufficient memory for my PC. The artifact is provided in the form of a virtual machine and code. For the other four, three of them are provided in the form of virtual machines, and the other one is in the form of Docker. For the types of artifacts, two of them are code. Besides there is one proof, and one command line, respectively. Thus, in general, Linux-type virtual machines are the main form of artifact storage. The years of the two successfully reproduced artifacts are 2013 and 2020, and the years that could not be reproduced are 2016 and 2020. So the year is not a deciding factor for successful reproduction. If an artifact can be well documented and successfully configured, relatively old artifacts can still be reused.

Furthermore, if you compare the documentation for the five artifacts, honestly, they all seem to me to be relatively detailed and well-documented, as they all describe how to configure the artifacts and how to execute them step by step to achieve the target result. Therefore, the reason for the non-functionality of 2 of the artifacts may not be in the documentation, but in the artifacts themselves. When I followed the documentation in order, I got error reports at some steps. It was confusing that for both artifacts, one has the Artifacts Evaluated Functional badge and the other one has Artifact Evaluated badge.

From the experience of reproducing these five artifacts, the following are some personal thoughts.

For artifact creators:
- Detailed guidance documentation is essential, which should include a list of configurations needed to run the artifact successfully (prerequisites), a list of steps to run it (possible issues and their solutions), expected results (the directory they store), etc. A better solution for the prerequisites part is that the required configuration is already installed in the provided artifact and we just need to jump to the list of steps and start building. For the possible issues part, since I believe that it is impossible for a creator to construct an artifact and run it without problems arising, these problems can be attached to the documentation as an issue-solution list, so that users can look up the corresponding problems when reusing them. 
- Since there may be a long time gap between when the artifact is used by the user and when it is created, the version of tools installed in the artifact may need to be updated, so the creator needs to clearly indicate all possible versions of the tools needed for the artifact.

For artifact evaluators:
- Although I am sorry to say this, according to the percentage of non-reproducibility, it cannot be excluded that the artifacts are not reproducible due to the users own inability to find a solution to the error reports, and partly also because the artifacts themselves are not functional, but are issued with a badge. Therefore, we hope that the evaluators will be more strict and accurate in evaluating the artifacts and issuing the badges.

Overall, it was a pleasure to have this experience of reproducing the artifacts. There is no denying the recognition and respect for the efforts of each author, whose work enriches the assets of the community. For myself, the feeling of successfully reproducing an article is a real joy!