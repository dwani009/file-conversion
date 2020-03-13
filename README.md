# file-conversion
A program that can be invoked from the command line to convert files in the source tree, to files in the destination tree. 

Consider following example,

Source/

 +- sub1/
 |   +- sub1.1/
 |   |  +- sub2.1/
 |   |  |    `- 001.txt
 |   |  `- sub2.2/
 |   |       `- 001.txt
 |   `- sub1.2/
 |      +- sub2.1/
 |      |    `- 001.txt
 |      ` sub2.2/
 |           `- 001.txt
 `- sub2/
     +- sub1.1/
     |  +- sub2.1/
     |  |    `- 001.txt
     |  `- sub2.2/
     |       `- 001.txt
     `- sub1.2/
        +- sub2.1/
        |    `- 001.txt
        ` sub2.2/
             `- 001.txt
 
/output would be in the following structure/

Dest/

 +- sub2.1/
 |   +- sub1_sub1.1_sub2.1.txt
 |   +- sub1_sub1.2_sub2.1.txt
 |   +- sub1_sub1.1_sub2.1.txt
 |   `- sub1_sub1.2_sub2.1.txt
 `- sub2.2/
     +- sub1_sub1.1_sub2.2.txt
     +- sub1_sub1.2_sub2.2.txt
     +- sub1_sub1.1_sub2.2.txt
     `- sub1_sub1.2_sub2.2.txt
