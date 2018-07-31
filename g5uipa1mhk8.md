```
[tyler@fend01 object]$ nano Makefile.h
  GNU nano 2.0.9                         File: Makefile.h

#----------------------------------------------------------------------------

MV = mv -f
AR = ar -r
RM = rm -f
CD = cd
RL = ranlib
ECHO = echo

# full optimization does not work on runtime_parameters.F90
#runtime_parameters.o : runtime_parameters.F90
#       ${FCOMP} ${FFLAGS_TEST}  $(F90FLAGS) $<

#amr_%.o : amr_%.F90
#       ${FCOMP} ${FFLAGS_OPT_NOIPA} ${F90FLAGS} ${FDEFINES} $<

```