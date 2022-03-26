---
title: "Makefile"
date: 2022-03-26 12:30 +0900
category: study
---


This is from **[gnu.org](https://www.gnu.org/software/make/manual/html_node/File-Name-Functions.html)**.

## Functions for File Names

### $(dir <em>names...</em>)

	Extracts the directory-part of each file name in <em>names</em>.

		> $(dir src/foo.c hacks)
	
	result : 'src/ ./'

### $(notdir <em>names...</em>)

	Extracts all but the directory-part of each file name in <em>names</em>.

		> $(notdir src/foo.c hacks)
	
	result : 'foo.c hacks'

### $(suffix <em>names...</em>)

	Extracts the suffix of each file name in <em>names</em>.

		> $(suffix src/foo.c src-1.0/bar.c hacks)
	
	result : '.c .c'.

### $(basename <em>names...</em>)

	Extracts all but the suffix of each file name in <em>names>,

		> $(basename src/foo.c src-1.0/bar hacks)
	
	result : 'src/foo src-1.0/bar hacks)

### $(addsuffix <em>suffix, names...</em>)

	The argument <em>names</em> is regarded as a series of names, separated by whitespace;

		> $(addsuffix .c, foo bor)

	result : 'foo.c bar.c'.

### $(addprefix <em>prefix, names...</em>)

	The argument <em>naems</em> is regarded as a series of names, separated by whitespace;
	
		> $(addprefix src/, foo bar)

	result : 'src/foo src/bar'


### $(join <em>list, list2</em>)

	Concatenates the two arguments word by word: the two first words (one from each argument)

	concatednated form the first word of the result, the two seconde words from the second word of the result, and so on.

		> $(join a b,.c .o)

	result : 'a.c b.o'	


### $(wildcard <em>pattern</em>

	The argument <em>pattern</em> is a file name pattern, typically containing wildcard characters (as in shell file name patterns).
	example 1

		> clean :
		>		rm -f *.o
		
	example 2 

		> print: *.c
		>		lpr -p $?
		> 		touch print

	example 3
		
		> objects = *.0

	example 4
		
		> objects := $(wildcard *.o)


### $(realpath <em>names...</em>)
	
	For each file name in <em>names</em> return the canonical absolute name. A canonical name does not contain any

	. or .. components, nor any repeated path separators (/) or symlinks.


### $(abspath <em>names...</em>)

	For each file name in <em>names</em> return an absoulte name that does not contain any . or .. components, nor

	any repeated path separators (/).


