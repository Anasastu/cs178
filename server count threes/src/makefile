all: dir ServerCountThrees cleanup

dir:
	mkdir temp

ServerCountThrees: readInt32BitLE.o main.o
	gcc temp/main.o temp/readInt32BitLE.o -o ../ServerCountThrees

readInt32BitLE.o: readInt32BitLE.c
	gcc -o temp/readInt32BitLE.o -c readInt32BitLE.c

main.o: ServerCountThrees.c
	gcc -o temp/main.o -c ServerCountThrees.c

cleanup:
	rm --recursive temp

test:
	mkdir ../build
	cp ../ServerCountThrees ../build/ServerCountThrees
	cp ../data/threesData.bin ../build/threesData.bin
	../build/ServerCountThrees