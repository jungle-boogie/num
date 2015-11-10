# Helpers: commands that work well with Num

There are many commands that work with with Num; here are our favorites.


## awk

The `awk` command typically processes text, fields, records, and data.

Example to select column 2 then sum:

    $ awk '{print $2}' data.txt
    2
    5
    8

Run <a href="http://linux.die.net/man/1/awk">`man awk`</a> to see options for scanning, processing, input, output, etc.


## cat

The `cat` command typically prints the contents of a file.

Example to print a file of data then sum:

    $ cat data.txt
    1 2 3
    4 5 6
    7 8 9

Run <a href="http://linux.die.net/man/1/cat">`man cat`</a> to see options for line numbering, blank line squeezing, etc.


## cut

Cut a field

Example:

    cat data.txt | cut -f 2 -d " "
    2
    5
    8

Run <a href="http://linux.die.net/man/1/cut">`man cut`</a> to see options for cutting by character, changing delimiters, suppressing lines, etc.


## head

Get the head of the text, meaning the first lines of data or a file.

Example:

    $ cat data.txt | head -1
    1 2 3

Run <a href="http://linux.die.net/man/1/cat">`man head`</a> to see options for line counts, using bytes, etc.


## seq (sequence)

Sequence: generate a sequence of numbers.

Example:

    $ seq 3
    1
    2
    3

Run <a href="http://linux.die.net/man/1/seq">`man seq`</a> to see options for number separators, zero padding, etc.


## shuf (shuffle)

Shuffle a list, a.k.a. randomize the order of list items.

Example:

    $ seq 3 | shuf
    3
    1
    2

Run <a href="http://linux.die.net/man/1/shuf">`man shuf`</a> to see options for input range, sample number, head count, etc.


## sort

Sort the items.

Example:

    $ echo "3\n2\n1" | sort --numeric-sort
    1
    2
    3

Run <a href="http://linux.die.net/man/1/sort">`man sort`</a> to see options for reverse, unique, field separator, etc.


## tail

Get the tail of the text, meaning the last lines of data or a file.

Example:

    $ cat data.txt | tail -1
    7 8 9

Run <a href="http://linux.die.net/man/1/tail">`man tail`</a> to see options for removing headers, reversing, etc.


## uniq (unique)

Unique: make the items unique by removing duplicates.

Example:

    $ echo "1\n1\n2\n2\n3\n3" | uniq
    1
    2
    3

Run <a href="http://linux.die.net/man/1/uniq">`man unique`</a> to see options for showing duplicates, skipping duplicates, ignoring fields, etc.


## wc (word count)

Word count: this typically counts lines, words, and characters.

Example:

    $ wc data.txt
    3 9 15

Run <a href="http://linux.die.net/man/1/wc">`man wc`</a> to see options, and how to use languages other than English or character encodings other than ASCII.


## parallel

GNU parallel provides multi-core processing that spreads work among your CPU cores.

Example:

    $ cat data.txt | parallel --pipe num sum | num sum
    45

Run <a href="http://linux.die.net/man/1/parallel">`man parallel`</a> to see options for jobs, loads, delays, etc.

<p><hr><nav>
* <b>[Prev Page: Functions: the complete list of all capabilities](functions.md)</b>
* <b>[Next Page: Aritcles & Blogs](articles.md)</b>
</nav>