RDIST=/ugi/home/shared/vincent/Software/R-2.12.2



INCLUDES= -I. -I$(RDIST)/include -I/usr/lib64/R/include -I/usr/share/R/include/ 
LIBS = -lg2c

PROF= #-pg
DEB=  -g
OPT = -O 

CFLAGS= -L/usr/local/lib -pthread -fPIC -Wall $(OPT) $(PROF) $(DEB) $(INCLUDES) -lgsl -lblas -static

CNV_estimate.so: CNV_estimate.cpp
	R CMD SHLIB hmm.cpp fdiv.c stream.c hypot.c error.c ldfrexp.c VP_infnan.c elementary.c invhyp.c log1p.c VP_log.c exp.c math.c VP_zeta.c VP_trig.c VP_psi.c VP_gamma.c beta.c CNV_estimate.cpp -o ExomeDepth.so 

clean:
	rm *.o ExomeDepth.so


