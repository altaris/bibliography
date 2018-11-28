# **何それ**:question::exclamation:

This repo stores by main bibliography `.bib` file. If you read this, you probably are collaborating with me (sorry about that) on writing a TeX document.

# Contributing 

The preferred way to edit the bibliography is by using [Jabref](http://www.jabref.org/). Regardless, here is a couple guidelines :pray:

## 1. The BibTeX key

It should be the name of the first author (first letter capitalized, all accents and spaces removed), followed by the year. If that key is aleady used, add a lowercase letter. Here are some examples:
```
@Book{Adamek1994a,
  title     = {Locally presentable and accessible categories},
  publisher = {Cambridge University Press, Cambridge},
  year      = {1994},
  author    = {Ad\'amek, {Ji\v{r}\'\i} and Rosick\'y, {Ji\v{r}\'\i}},
  volume    = {189},
  series    = {London Mathematical Society Lecture Note Series},
  isbn      = {0-521-42261-2},
  doi       = {10.1017/CBO9780511600579},
  groups    = {algebraic-theories, Type-theory},
  keywords  = {18Axx (18-02)},
  mrnumber  = {1294136},
  pages     = {xiv+316},
}
```

## 2. Names

The `author` field is list of names (of the authors), and should satisfy the following grammar:
```
AUTHOR_FIELD_VALUE ::= {AUTHOR_LIST}
AUTHOR_LIST        ::= ε
                    |  AUTHOR_NAME
                    |  AUTHOR_NAME and AUTHOR_LIST
AUTHOR_NAME        ::= first_name, last_name
```
(it is not LL1 but i'm sure you can manage)

## 3. Special characters

Do not assume unicode is supported, so use LaTeX macros instead of special characters directly. [Here is a usefule cheatsheet for accents](https://en.wikibooks.org/wiki/LaTeX/Special_Characters#Escaped_codes).

# Testing

A test TeX file is present in directory (test)[test/]. You can compile it by running
```sh
cd test
make
```
The output pdf should display the whole bibliography. 

# References

* [BibTeX guide, including a table of mandatory fields](https://en.wikibooks.org/wiki/LaTeX/Bibliography_Management#BibTeX)