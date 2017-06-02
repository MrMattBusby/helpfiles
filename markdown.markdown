This is _Italics_

This is *AltItalics*

>> This is a note

This is __Bold__

This is **Bold**

This is ~~Crossed out~~

This is <u>underlined</u>

This is <a name="test">reference link</a>

This is a hyperlink: [Link](http://www.google.com/ "This is a title")

This is a hyperlink: <https://www.google.com>

This is an email: <asdf@google.com>

This is a `code block`

This is a python code block:

```python
# Larger python code block
import sys, os
def main():
  pass
```

Long sentance auto-moved to
one line.

Long sentance not moved  
to one line b/c of double spaces.

Long sentance not moved<br>
to one line b/c of br html.

    This is 4 space codeblock
      This is 4 space codeblock
    This is 4 space codeblock

#Header1

##Header2

###Header3

#### Header4

##### Header5

###### Header6

AltHeader1
======

AltHeader2
------

####Separators:

---

***

- - -

___

####Tables:

|Col1|Col2|Col3 |
|----|----|----:|
|Item|Item|Item |
|Doesnt|even|maaaaaaaater|

>Indented comment

> Block quote
Still on same line
> Still on same line  
> Now on a new line
>
> 1. list
> 1. list
>
> > Now embedded
> > Now embedded
> >
> > > Now more embedded
> > > Now more embedded
>
> End

####Bullets:

* Good
* Good
 
  * Good
  * Good
    * Good
    * Good
  * Good

- Good
  + Doesn't work in pandoc.
  + Doesn't work in pandoc.
    * 3rd indent
- Good
  - Doesn't work in pandoc.
  - Doesn't work in pandoc.

####Numbered lists:

1. Good
1. Goood
   Still good
1. Goood
   Still good
   Still good

1. Good
  1. Doesn't work in pandoc.

  1. Good
  1. Good
    1. Good
    1. Good
  1. Good

####Links/References:

  [1]: ./template.markdown "Title goes here"

  This [1]() links to open file just defined (hidden in html).

  [Link to 'reference link' above](#test)

  ![This would be a link to an image](/path/to/image.jpg)

####Items that only work in pandoc

Long sentance not moved\
to one line b/c of backslash. Only works in pandoc.

Table also works in github:

Col1|Col2|Col3
----|----|----
Item|Item|Item

#. Works in pandoc but shouldn't
#. Works in pandoc but shouldn't
  #. Bad
