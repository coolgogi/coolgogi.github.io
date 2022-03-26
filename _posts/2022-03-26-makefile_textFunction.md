---
title : "Makefile text function"
date : 2022-03-26 15:29 +0900
category : study
---

## This is from **[gnu.org](https://www.gnu.org/software/make/manual/html_node/Text-Functions.html#Text-Functions)**

### $(subst <em>from, to, text</em>)

Performs a textual replacement on the text <em>text</em>: each occurrence of <em>from</em> is replaced by <em>to</em>.

	$(subst ee, EE, feet on the street)
	
result : 'fEEt on the strEEt'


### $(patsubst <em>pattern, replacement, text</em>)

Finds whitespace-separated words in <em>text</em> that match <em>pattern</em> and replaces them with <em>replacement</em>.

	$(patsubst %.c, %.o x.c.c bar.c)

result : 'x.c.o bar.o'

	$(var:pattern=replacement)

is equivalent to

> $(patsubst pattern, replacement, $(var))


### $(strip <em>string</em>)

Removes leading and trailing whitespace from <em>string</em> and replaces eachi internal sequence of one or more

whitespace characters with a sing space.

	$(strip a b c )

result : 'a b c'


### $(findstring <em>find, in</em>)

Searches <em>in</em> for an occurrence of <em>find</em>. If it occurs, the value is <em>find</em>; otherwise, teh value is empty.

	$(findstring a,a b c)
	$(findstring a,b c)

result : 'a' ''(the empty string)

### $(filter <em>pattern..., text</em>)

Returns all whitespace-separated words in <em>text</em> that <em>do</em> match any of the <em>pattern</em> words, removing any

words that <em>do not</em> match.

	sources := foo.c bar.c baz.s ugh.h
	foo: $(sources)
		cc $(filter %.c %.s,$(sources)) -o foo

says that foo depends of foo.c bar 

### $(filter-out <em>pattern..., text</em>)

Returns all whitespace-separated words in <em>text</em> that <em>do not</em> match any of the <em>pattern</em> words, removing the words that <em>do</em> match one or more.

given:
	objects=main1.o foo.o main2.o bar.o
	mains=main1.o main2.o

	$(filter-out $(mains), $(objedts))


### $(sort <em>list</em>)

Sorts the words of <em>list</em> in lexical order, removing duplicate words.

	$(sort foo bar lose)

result : 'bar foo lose'

### $(word <em>n, text</em>)

Returns the <em>n</em>th word of <em>text</em>. The legitimate values of <em>n</em> start from 1.

	$(word 2, foo bar baz)

result : 'bar'

### $(wordlist <em>s, e, text</em>)

Returns the list of words in <em>text</em> starting with word <em>s</em> and ending with word <em>e</em> (inclusive)/

The legitimate values of <em>s</em> start from 1.

	$(wordlist 2, 3, foo bar baz)

return 'bar baz'

### $(words <em>text</em>)

Returns the number of words in <em>text</em>.

### $(firstword <em>names...</em>)

The argument <em>names</em> is regarded as a series of names, separated by whitespace.

	$(firstword foo bar)

result : 'foo'


### $(lastword <em>names...</em>)

The argument <em>names</em> is regarded as a series of names, separated by wthiespace.

	$(lastword foo bar)

result : 'bar'

