---
title: "Makefile"
date: 2022-03-26 12:30 +0900
category: study
---


# Makefile
This is from gnu.org


## Functions for File Names
**[gnu link](https://www.gnu.org/software/make/manual/html_node/File-Name-Functions.html)**.

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
	>(addsuffix .c, foo bor)
	result : 'foo.c bar.c'.

### $(addprefix <em>prefix, names...</em>)


### $(join <em>list, list2</em>


### $(wildcard <em>pattern</em>


### $(readpath <em>names...</em>)


### $(abspath <em>names...</em>)



