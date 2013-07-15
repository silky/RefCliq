RefCliq
====
This is a Python program that uses a network clustering algorthym to anlayze
 Web of Knowledge records in BibTeX format. The results are helpful for constructing
 literature reviews.
 
Requires Python 2.7 and the following dependencies:
* [NLTK](http://nltk.org)
* [Pybtex](http://pybtex.sourceforge.net)
* [NetworkX](http://networkx.github.io)
* [Community](http://perso.crans.org/aynaud/communities/)

Note: This should work with Python 2.6 if you have [Counter class](http://code.activestate.com/recipes/576611-counter-class/). 

Sample Usage:
--------
This program works exlusively with articles downloaded from Web of Knowledge that include the "Full Record" including "Cited References".

If you had all the articles from the journal Mobilization stored as `moby.bib` 
and you wanted the analysis to be stored in a folder called `moby`:

    $ python refcliq.py moby.bib -d moby

The contents of the output directory include:
* a
* b
    
To run a standard analysis of the files, `us_2012_a.bib`,  `us_2012_b.bib`,  
and , `us_2012_c.bib` and save the results in a folder called `us_sociology`.

    $ python refcliq.py us_2012.bib -d us_sociology

Using the same files and destintation, but include all references with at least
two citations.

    $ python refcliq.py us_2012*.bib -d us_sociology -n 2

Using the same files and destintation, but include all edges with at least two 
occurences.

    $ python refcliq.py us_2012*.bib -d us_sociology -e 2
    



    