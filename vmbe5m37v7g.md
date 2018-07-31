```
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
[tyler@fend01 object]$ make clean
rm -f setup_flags *.o *.mod *.a *.unit *API.h *API.c *API-bridges.F90
```