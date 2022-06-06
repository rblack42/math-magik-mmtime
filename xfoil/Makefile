FC      = gfortran
FCFLAGS =  -J mod_files
FLFLAGS = -static-libgfortran -static-libgcc -dynamiclib -gfull


FSRCS = src/i_pindex.f90 \
		src/i_xfoil.f90 \
		src/i_blpar.f90 \
		src/i_circle.f90 \
		src/i_xbl.f90 \
		src/m_spline.f90 \
		src/m_xsolve.f90 \
		src/m_xutils.f90 \
		src/m_xpanel.f90 \
		src/s_xbl.f90 \
		src/s_xfoil.f90 \
		src/m_xgeom.f90 \
		src/m_userio.f90 \
		src/m_xgdes.f90 \
		src/s_xoper.f90  \
		src/m_xpol.f90 \
		src/m_xoper.f90 \
		src/m_aread.f90 \
		src/m_iopol.f90 \
		src/m_naca.f90 \
		src/m_sort.f90 \
		src/m_xblsys.f90 \
		src/m_xbl.f90 \
		src/m_xqdes.f90 \
		src/m_xmdes.f90 \
		src/m_xfoil.f90 \
		src/api.f90

FOBJS = $(FSRCS:.f90=.o)

TARGET = xfoil.dylib
	
%.o:	%.f90
	$(FC) $^ -o $@ $(FCFLAGS)

xfoil.dylib:	$(FOBJS)
	$(FC) -c $^ -o $@ $(FLFLAGS)

.PHONY: clean
clean:
	rm -f mod_files/*
	rm -f src/*.o
