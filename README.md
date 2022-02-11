# hist.sh -- Draw histograms in your shell

Reads data from STDIN and draws a frequency histogram in your shell.

Usage: `hist [plot function] [plotchar]`

"plot function" is any valid perl expression, with "x" being the value.

## Examples

Simple usage:

```
$ echo 'lorem ipsum dolor sit amet' | fold -w1 | hist
	4	####
a	1	#
d	1	#
e	2	##
i	2	##
l	2	##
m	3	###
o	3	###
p	1	#
r	2	##
s	2	##
t	2	##
u	1	#
```

Squared values:

```
$ echo 'lorem ipsum dolor sit amet' | fold -w1 | hist 'x**2'
	4	################
a	1	#
d	1	#
e	2	####
i	2	####
l	2	####
m	3	#########
o	3	#########
p	1	#
r	2	####
s	2	####
t	2	####
u	1	#
```

Different plotting character:

```
$ echo 'lorem ipsum dolor sit amet' | fold -w1 | hist x o
	4	oooo
a	1	o
d	1	o
e	2	oo
i	2	oo
l	2	oo
m	3	ooo
o	3	ooo
p	1	o
r	2	oo
s	2	oo
t	2	oo
u	1	o
```
