# this makefile takes the source files |readInt32BitLE.c| and |countThrees.c|
# to build a final program that will read integers from binary |threesData.bin|

# main branch
Count3s: readInt32BitLE.o main.o
	# compile the final result
	gcc temp/main.o temp/readInt32BitLE.o -o Count3s

# auxillary branch
readInt32BitLE.o: readInt32BitLE.c
	gcc -o temp/readInt32BitLE.o -c readInt32BitLE.c

# auxillary branch
main.o: countThrees.c
	gcc -o temp/main.o -c countThrees.c

# command to run final result
runCount3s: ./Count3s