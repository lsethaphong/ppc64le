# ppc64le

25 April 2020
L. Sethaphong, PhD

When attempting to install and rebuild largely opensourced biotools for a drug discovery pipeline, there are challenges
in porting to ppc64le architecture.  The vast majority of opensource biotools are written for compilation on x86 architectures.

The previous three weeks proved successful in compiling Rosetta v3.10 and its NCBI and other open source tool dependencies.  Unfortunately, for the new fragment maker, the sparks-x utility of a modest sized NN is only provided as a binary.  Therefore, that step of fragment generation needed to be run on an x86 system (VM or bare metal).  Its execution is very fast but short changes the researcher who is attempting to leverage what resources he has avaialble such as pp64le machines in excess.

The rough scope of work was the following:

Installing Rosetta
Installing NCBI DB
Installing Legacy BLAST and BLAST+
Installing Psipred
Installing Ambermini
Installing rdock 2013
References:
Software Tools and Data Stack:
NCBI Tools & Data
BlAST (legacy version 2.2.22)
BLAST+ (version 2.10.0)
Uniref90 DB
NR DB
Rosetta version 3.10: request a license
Ambermini: 
Ff14SB forcefield library https://ambermd.org/AmberModels.php
ff99SB: https://ambermd.org/downloads/ff99SBildn.tar
Ambertools 18: https://ambermd.org/downloads/
Psipred: 
Pfilt: 
rdock (version 2013):

Main Dependencies:
Rosetta: libsqlite3 libsqlite3-dev
Sparks-x: libswitch-perl
MPI dependencies: libmpich-dev libmpich12 mpich
gcc-5,6,7
g++-5,6,7
gfortran - build-essential
scons
python python3
libcppunit (for rdock)
Notes:
If make_fragements doesn’t work, be sure to check if the psipred file generated is in the vertical format and file paths are correct.  Always add the verbose flag when debugging.
Additional Programs:
Spicker from Zhanglab:
 https://zhanglab.ccmb.med.umich.edu/SPICKER/
