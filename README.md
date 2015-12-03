This is a utility helping to search words from a docx file
A usecase could be, searching for specific skillset in resume.
e.g. GoFinder /tmp/sample.docx C++ Java

The first argument is the Utility name, GoFinder
The next is docx filename
The filename is followed by list of skillset, C++ and Jave in this case

The result is printed as
-------------------------------
C++ true
Java false

indicating, C++ word exists n sample.docx and Java does not.

docx is a compressed zip file, following Office Open XML specifcations.
It contains various xml files. It follows ECMA-376 specfication.
More details about ECMA are available here
http://www.ecma-international.org/publications/standards/Ecma-376.htm

All important data for a docx file is present in word/document.xml.
This utility looks through the document.xml for given words.

The utility does a case-senistive search
It uses mainly ioutil and zip package from golang
