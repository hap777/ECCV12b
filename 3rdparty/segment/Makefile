INCDIR = -I.
DBG    = -g
OPT    = -O3
CPP    = g++
CFLAGS = $(DBG) $(OPT) $(INCDIR)
LINK   = -lm 

.cpp.o:
	$(CPP) $(CFLAGS) -c $< -o $@

all: segment

segment: segment.cpp segment-image.h segment-graph.h disjoint-set.h
	$(CPP) $(CFLAGS) -o segment segment.cpp $(LINK)

clean:
	rm -f segment *.o

clean-all: clean
	rm -f *~ 

clean-release: clean-all
	rm -f *.mex*

