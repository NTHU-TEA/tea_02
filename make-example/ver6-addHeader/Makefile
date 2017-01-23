# -*- MakeFile -*-
#target: dependencies
#   action

all: geom tip

geom: geom.o gd.o
	gcc geom.o gd.o -o geom -l m

geom.o: geom.c gd.h
	gcc -c geom.c gd.h

gd.o: gd.c
	gcc -c gd.c

tip: tip.o gd.o
	gcc tip.o gd.o -o tip

tip.o: tip.c gd.h
	gcc -c tip.c gd.h

clean:
	rm *.o tip geom
