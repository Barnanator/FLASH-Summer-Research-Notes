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

```