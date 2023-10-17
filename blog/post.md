---
title: Small tools -- the Swiss army knife of translation tools 
---


Somewhere along the line I learned to write code - starting with Excel, Visual basic, C#, and then Python. Now I can fiddle in Javascript when necessary and with lots of looking things up. 

Python and Javascript are so useful for translation because they provide simple ways to create small tools to interact with data. Nodejs and Python make writing command line tools simple and easy. 

Data... There's lots of data on the Bible. Some of it easy to access, some of it not. Thankfully James Tauber's [vocabulary-tools](https://github.com/jtauber/vocabulary-tools) contains a packages `gnt_data` that makes is easy to interact with the Greek New Testament.

Using that package, I clobbed together a script to find verses containing lemmas and then print them in a simple string format where each book is separated by `;` and references within a book are separated by `,` which gives something like `MRK 1:1,2:1;JHN 14:1;ACT 1:1,2:2,5:4"`.

I can then pipe this into a variety of other small tools. I have a bash script that takes this input and uses [diatheke](https://wiki.crosswire.org/Frontends:Diatheke) to display each of these references in the translation of my choice, current Lexham English Bible, found in freely available [Sword modules](https://www.crosswire.org/sword/modules/index.jsp). 

I have a nodejs script that can parse USFM files using [usfm-grammar](https://github.com/Bridgeconn/usfm-grammar) and display a list of references.

## Why do small tools matter?

**They can do things more quickly or easily than Bible study websites and software.** Looking up a list of verses usually requires looking at them one at a time. This is slow and tedious. 

**In some cases to do things that the software can't do.** I love Logos Bible Software, but to my knowledge it can't read USFM files.

**These small tools are also composable.** Once script finds a list of where lemmas occur. One script displays a list of verses in Sword modules (diatheke) and one displays them in USFM files. 

**They are easily modified and extended.** If I wanted my bash script to use diatheke to display multiple translations or to also display the Greek NT text, it would be as simple as copying bash script, copying the line that calls diatheke and changing what package diatheke displays. 

**They are sharable.** With blogs and sites like GitHub, it's easy to share scripts so they can be useful to others.

Learning to write scripts is a learning curve, but it's not impossible and is certainly easier than many of things we have to learn related to the Bible (Greek or Hebrew for example). Should you do so? Maybe? Maybe not? 
