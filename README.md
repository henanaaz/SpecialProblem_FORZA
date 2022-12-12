# SpecialProblem_FORZA
ECE8903 for Special Problem with Professor A Daglis

This documents lists the steps involved to get to going on the project.

Step A:
Let's get you started on setting up SST Simulator.
1. On your system, create a directory structure "scratch/src" for all your set up files
2. Download the simulator core, element and macro using the page "https://sst-simulator.org/SSTPages/SSTMainDownloads/" inside the src directory
3. Make sure OpenMPI is installed
                  # OPENMPI SET UP
                  export MPIHOME=$HOME/local/packages/OpenMPI-4.0.5
                  export PATH=$MPIHOME/bin:$PATH
                  export MPICC=mpicc
                  export MPICXX=mpicxx

                  export PMIX_MCA_gds=hash

                  export LD_LIBRARY_PATH=$MPIHOME/lib:$LD_LIBRARY_PATH
                  export DYLD_LIBRARY_PATH=$MPIHOME/lib:$DYLD_LIBRARY_PATH
                  export MANPATH=$MPIHOME/share/man:$DYLD_LIBRARY_PATH

4. Let's set you up for SST core now:
                  #SSTCORE SET UP
                  export SST_CORE_HOME=$HOME/local/sstcore-11.1.0
                  export SST_CORE_ROOT=$HOME/scratch/src/sstcore-11.1.0
                  export PATH=$SST_CORE_HOME/bin:$PATH
                  
5. Let's configure the SST core. An example of the command line is 
                  "./configure --prefix=$HOME/scratch/src/sstcore-11.1.0 CC=\`which gcc\` CXX=\`which g++\` MPICC=`which mpicc` MPICXX=`which mpicxx`"                  

When the configuration is done successfully , it prompts the following:
![image](https://user-images.githubusercontent.com/93614048/206943147-f1f1649d-7b98-4e28-834d-520e30732cd3.png)

6. Inside the sstcore-11.1.0 directory (make use of the relevant directory structure), perform following steps to build the sst-core
                  make
                  make install
                  
7. Let's repeat steps 4-6 for sst elements as well
                  export SST_ELEMENTS_HOME=$HOME/local/sstelements-11.1.0
                  export SST_ELEMENTS_ROOT=$HOME/scratch/src/sst-elements-library-11.1.0                  

Step B:
Let's get you set up for using rev cores by Tactical Computing Labs!
