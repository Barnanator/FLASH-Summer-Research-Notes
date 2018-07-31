```
Last login: Tue Jul 31 20:11:14 2018 from dynamic-oit-astroturf-d-3.princeton.edu
[tyler@fend01 ~]$ pwd
/groups/dark/tyler
[tyler@fend01 ~]$ ls -lh
total 32M
drwxr-xr-x  2 tyler dark 12K Jul 27 16:56 Archive
drwxr-xr-x  9 tyler dark 13K Jul 26 22:14 flash
-rw-r--r--  1 tyler dark 90M Jul 26 21:32 flash.tar
drwxr-xr-x 11 tyler dark 16K Jul 26 23:34 modules-3-2-10
[tyler@fend01 ~]$ cd flash
[tyler@fend01 flash]$ ls -lh
total 452K
drwxr-xr-x   2 tyler dark  16K Jul 26 22:14 bin
drwxr-xr-x   3 tyler dark  12K Dec  9  2017 docs
drwxr-xr-x  12 tyler dark  13K Dec  9  2017 lib
-rw-r--r--   1 tyler dark 5.5K Dec  9  2017 LICENSE
drwxr-xr-x   2 tyler dark 219K Jul 31 21:19 object
-rw-r--r--   1 tyler dark   24 Dec  9  2017 RELEASE
-rw-r--r--   1 tyler dark  37K Dec  9  2017 RELEASE-NOTES
-rwxr-xr-x   1 tyler dark  225 Dec  9  2017 setup
-rwxr-xr-x   1 tyler dark  978 Dec  9  2017 setup_alt
drwxr-xr-x 136 tyler dark  20K Dec  9  2017 sites
drwxr-xr-x  16 tyler dark  13K Dec  9  2017 source
drwxr-xr-x  19 tyler dark  13K Dec  9  2017 tools
[tyler@fend01 flash]$ ./setup Sedov -auto
Processing Shortcut file: /lustre/hpc/dark/tyler/flash/bin/setup_shortcuts.txt
checking for needed files and directories
    checking sites Aliases file
    using site directory for site fen.bluegene.bnl.gov
generating default Units file
    Driver/DriverMain/Unsplit
    Driver/localAPI
    Grid/GridBoundaryConditions
    Grid/GridMain/paramesh/interpolation/Paramesh4/prolong
    Grid/GridMain/paramesh/interpolation/prolong
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/headers
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/mpi_source
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/source
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/utilities/multigrid
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/flash_avoid_orrery
    Grid/localAPI
    IO/IOMain/hdf5/serial/PM
    IO/localAPI
    PhysicalConstants/PhysicalConstantsMain
    RuntimeParameters/RuntimeParametersMain
    Simulation/SimulationMain/Sedov
    flashUtilities/contiguousConversion
    flashUtilities/general
    flashUtilities/interpolation/oneDim
    flashUtilities/nameValueLL
    flashUtilities/sorting/quicksort
    flashUtilities/system/memoryUsage/legacy
    monitors/Logfile/LogfileMain
    monitors/Timers/TimersMain/MPINative
    physics/Eos/EosMain/Gamma
    physics/Eos/localAPI
    physics/Hydro/HydroMain/unsplit/Hydro_Unsplit
    physics/Hydro/localAPI
scanning /groups/dark/tyler/flash/object/Units file for included units
    Driver/DriverMain/Unsplit
    Driver/localAPI
    Grid/GridBoundaryConditions
    Grid/GridMain/paramesh/interpolation/Paramesh4/prolong
    Grid/GridMain/paramesh/interpolation/prolong
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/headers
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/mpi_source
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/source
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/PM4_package/utilities/multigrid
    Grid/GridMain/paramesh/paramesh4/Paramesh4dev/flash_avoid_orrery
    Grid/localAPI
    IO/IOMain/hdf5/serial/PM
    IO/localAPI
    PhysicalConstants/PhysicalConstantsMain
    RuntimeParameters/RuntimeParametersMain
    Simulation/SimulationMain/Sedov
    flashUtilities/contiguousConversion
    flashUtilities/general
    flashUtilities/interpolation/oneDim
    flashUtilities/nameValueLL
    flashUtilities/sorting/quicksort
    flashUtilities/system/memoryUsage/legacy
    monitors/Logfile/LogfileMain
    monitors/Timers/TimersMain/MPINative
    physics/Eos/EosMain/Gamma
    physics/Eos/localAPI
    physics/Hydro/HydroMain/unsplit/Hydro_Unsplit
    physics/Hydro/localAPI
Computing default values for options not specified on command line
Using Makefile.h: /groups/dark/tyler/flash/sites/fen.bluegene.bnl.gov/Makefile.h
generating Makefile
Copying data files: 3 copied
SUCCESS
[tyler@fend01 flash]$ cd object
[tyler@fend01 object]$ make
Calculating dependencies
./setup_depends.py --generateINTERMEDIATElines -O2 -qintsize=4 -qrealsize=8 -qdpc=e -qfixed -qnosave -c -qsuffix=cpp=F -qarch=440 -qtune=440 -qmaxmem=131072 -qsuffix=f=F90:cpp=F90 -qfree=f90 -I/gpfs/home2/ajackson/local/hdf5/current/bgl/serial/include -DH5_USE_16_API -O2 -DIBM -DNOUNDERSCORE -c -qarch=440 -qtune=440 -qmaxmem=131072 *.f *.f90 *.F90 *.F
./setup_addcdepends.py -I/gpfs/home2/ajackson/local/hdf5/current/bgl/serial/include -DH5_USE_16_API -O2 -DIBM -DNOUNDERSCORE -c -qarch=440 -qtune=440 -qmaxmem=131072 *.c
rm -f reorder.sh
/bgl/BlueLight/ppcfloor/bglsys/bin/mpixlf90 -O2 -qintsize=4 -qrealsize=8 -qdpc=e -qfixed -qnosave -c -qsuffix=cpp=F -qarch=440 -qtune=440 -qmaxmem=131072 -qsuffix=f=F90:cpp=F90 -qfree=f90 -WF,-DMAXBLOCKS=1000 -WF,-DNXB=8 -WF,-DNYB=8 -WF,-DNZB=1 -WF,-DN_DIM=2 Burn_interface.F90
make: /bgl/BlueLight/ppcfloor/bglsys/bin/mpixlf90: Command not found
make: *** [Burn_interface.o] Error 127
[tyler@fend01 object]$ make realclean
Sorry, I am unable to build realclean mentioned in
Related directory contents:
If you do not see an appropriate source file, realclean is probably mentioned in the
wrong Makefile and should probably go deeper inside the unit
make: *** [realclean] Error 1
[tyler@fend01 object]$ make clean
rm -f setup_flags *.o *.mod *.a *.unit *API.h *API.c *API-bridges.F90
[tyler@fend01 object]$

```