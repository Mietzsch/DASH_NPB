SHELL=/bin/sh
BENCHMARK=ft
BENCHMARKU=FT

include ../config/make.def

OBJS = ft.o ${COMMON}/c_${RAND}.o ${COMMON}/c_print_results.o \
       ${COMMON}/c_timers.o ${COMMON}/c_wtime.o #../omp-prof.o

include ../sys/make.common

${PROGRAM}: config ${OBJS}
	${CLINK} -o ${PROGRAM} ${OBJS} ${C_LIB} ${CLINKFLAGS} 

ft.o:             ft.cpp  global.hpp npbparams.hpp
	${CCOMPILE} ft.cpp

clean:
	- rm -f *.o *~ mputil*
	- rm -f ft npbparams.hpp core
