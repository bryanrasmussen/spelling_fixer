spelling_fixer
==============

The Purpose
===========

Spelling_Fixer is a collection of scripts in the Autohotkey language for doing autocorrection
of commonly misspelled words in a number of languages. 

The goal is to support all languages that have a unicode representation, although in such cases
one might still have support for those languages that do not have their alphabetic script 
supported but which can be written in another alphabetic script, for example Hmong which 
can be written in Latin 1. 

The goal is not to provide a comprehensive autocorrection, as such a solution would then
require user interaction whenever a possible misspelling was found, instead we will support
only those words that are obviously misspelled in their respective languages. 

As an example the word akvarie in Danish can be either a misspelling of akvarium or an adjective, 
since it has a possible correct usage it will not be corrected by the Danish spelling_fixer script;
on the other hand the word abonere is simply the word abonnere misspelled, and would be fixed 
automatically without asking the user if it is what they want. 

Requirements
============

Spelling_Fixer is implemented in Autohotkey and will only work on Windows (Windows 8 not checked as yet), as it uses Autohotkey's 
hotstrings functionality. 

Hotstrings are of course only possible on an OS that gives the level of control over the keyboard that
Windows does. 

The Unicode version of Autohotkey is needed. 

How the Autothotkey Scripts are written
===========

Currently I don't handwrite the scripts but generate them from screen-scraping various sources, 
for example Wikipedia sites for the respective languages listing common spelling errors. 

These screen-scraping tools are not generic enough to warrant putting in the repo.

The list of mis-spelled words and their corrections are used to generate an xml format,
and that xml format is used to generate the Autohotkey code. 
