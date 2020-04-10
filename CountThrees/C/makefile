default : ServerCountThrees

test : ServerCountThrees
	mkdir ../build
	cp ServerCountThrees ../data/threesData.bin ../build
	cd ../build; \
	./ServerCountThrees

ServerCountThrees : ServerCountThrees.o readInt32BitLE.o
	gcc -o ServerCountThrees ServerCountThrees.o readInt32BitLE.o

ServerCountThrees.o : ServerCountThrees.c readInt32BitLE.h
	gcc -c ServerCountThrees.c

readInt32BitLE.o : readInt32BitLE.c readInt32BitLE.h
	gcc -c readInt32BitLE.c


clean : 
	rm ServerCountThrees ServerCountThrees.o readInt32BitLE.o 
	
cleantest : 
	rm ../build/*
	rmdir ../build
