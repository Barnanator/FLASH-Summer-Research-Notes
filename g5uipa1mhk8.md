```
#-------------------------------------------------------------------
# FLASH makefile definitions for the llnl bgl
#
#
# These modules set environment variables pointing to the
# proper library locations. Only python is essential.
#-------------------------------------------------------------------

#----------------------------------------------------------------------------
# Set the HDF/HDF5 library paths -- these need to be updated for your system
#----------------------------------------------------------------------------

# This is HDF5 1.8.x, so the necessary define for the 1.6 API is included in
# the HDF5 flags below.

HDF5_PATH = /gpfs/home2/ajackson/local/hdf5/current/bgl/serial
# HDF5_PATH = /gpfs/home2/ajackson/local/hdf5/current/bgl/parallel
# HDF5_PATH = /bgl/apps/hdf5

# NCMPI_PATH = /usr/local/tools/parallel-netcdf/parallel-netcdf-1.0.0
ZLIB_PATH =

HPM_PATH =
PNG_PATH = /usr

MPI_PATH = /bgl/BlueLight/ppcfloor/bglsys

#----------------------------------------------------------------------------
# Compiler and linker commands
#
#  We use the f90 compiler as the linker, so some C libraries may explicitly
#  need to be added into the link line.
#----------------------------------------------------------------------------

ifdef PDTDIR
OPT=-optPDBFile=merged.pdb -optTauSelectFile="select.tau" -optReset="" -optVerbose
else
# LIB_MPI = -L$(MPI_PATH)/lib -lmpich.rts -lmsglayer.rts -ldevices.rts -lrts.rts -ldevices.rts
LIB_MPI =
endif
# FCOMP   = /opt/ibmcmp/xlf/bg/10.1/bin/blrts_xlf90 -I/bgl/BlueLight/ppcfloor/bglsys/include
FCOMP   = /bgl/BlueLight/ppcfloor/bglsys/bin/mpixlf90
# CCOMP   = /opt/ibmcmp/vac/bg/8.0/bin/blrts_xlc -I/bgl/BlueLight/ppcfloor/bglsys/include
CCOMP   = /bgl/BlueLight/ppcfloor/bglsys/bin/mpixlc
# CPPCOMP = cpp
CPPCOMP = /bgl/BlueLight/ppcfloor/bglsys/bin/mpixlcxx
# LINK    = /opt/ibmcmp/xlf/bg/10.1/bin/blrts_xlf90
LINK    = /bgl/BlueLight/ppcfloor/bglsys/bin/mpixlf90

#CONFIG_LIB = -L/bgl/BlueLight/ppcfloor/bglsys/lib -lmpich.rts -lmsglayer.rts -ldevices.rts -lrts.rts -ldevices.r$
#-----------------------------------------------------------------------------
# Compilation flags
#
#  Three sets of compilation/linking flags are defined: one for optimized code
#  code ("-opt"), one for debugging ("-debug"), and one for testing ("-test").
#  Passing these flags to the setup script will cause the value associated with
#  the corresponding keys (i.e. those ending in "_OPT", "_DEBUG", or "_TEST") to
#  be incorporated into the final Makefile. For example, passing "-opt" to the
#  setup script will cause the flags following "FFLAGS_OPT" to be assigned to
#  "FFLAGS" in the final Makefile. If none of these flags are passed, the default

```