```
tyler@tyler-XPS-15-9560:~/Documents/Astro/lib/FLASH4.5$ source activate python2
(python2) tyler@tyler-XPS-15-9560:~/Documents/Astro/lib/FLASH4.5$ conda env list# conda environments:
#
                         /home/tyler/Downloads/yt-conda
base                     /home/tyler/anaconda3
python2               *  /home/tyler/anaconda3/envs/python2
untitled                 /home/tyler/anaconda3/envs/untitled
(python2) tyler@tyler-XPS-15-9560:~/Documents/Astro/lib/FLASH4.5$ ./setup Sedov -auto
Processing Shortcut file:
/home/tyler/Documents/Astro/lib/FLASH4.5/bin/setup_shortcuts.txt
checking for needed files and directories
    checking sites Aliases file
    site directory for site tyler-XPS-15-9560 not found;
    using prototype Linux
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
scanning /home/tyler/Documents/Astro/lib/FLASH4.5/object/Units file for included
units
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
Using Makefile.h: /home/tyler/Documents/Astro/lib/FLASH4.5/sites/Prototypes/Linux/Makefile.h
generating Makefile
Copying data files: 3 copied
SUCCESS
(python2) tyler@tyler-XPS-15-9560:~/Documents/Astro/lib/FLASH4.5$ cd object
(python2) tyler@tyler-XPS-15-9560:~/Documents/Astro/lib/FLASH4.5/object$ make
Calculating dependencies
./setup_depends.py --generateINTERMEDIATElines -ggdb -c -O2 -fdefault-real-8 -fdefault-double-8 -Wuninitialized  -I/home/Documents/Astro/lib/hdf5/include -DH5_USE_16_API -ggdb -c -O2 -Wuninitialized -D_FORTIFY_SOURCE=2 *.f *.f90 *.F90 *.F 
./setup_addcdepends.py -I/home/Documents/Astro/lib/hdf5/include -DH5_USE_16_API -ggdb -c -O2 -Wuninitialized -D_FORTIFY_SOURCE=2 *.c
rm -f reorder.sh
/home/Documents/Astro/lib/mpich-3.2.1/bin/mpif90 -ggdb -c -O2 -fdefault-real-8 -fdefault-double-8 -Wuninitialized  -DMAXBLOCKS=1000 -DNXB=8 -DNYB=8 -DNZB=1 -DN_DIM=2 Burn_interface.F90
make: /home/Documents/Astro/lib/mpich-3.2.1/bin/mpif90: Command not found
Makefile:115: recipe for target 'Burn_interface.o' failed
make: *** [Burn_interface.o] Error 127
(python2) tyler@tyler-XPS-15-9560:~/Documents/Astro/lib/FLASH4.5/object$
```