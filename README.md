
This project presents LFG grammar developed within XLE Software and it encodes basics of information structure and word order phenomenon in Russian.

**Phenomenon description**

The phenomenon of word order in Russian can be seen in the way that the language allows a relatively free constituency order. In fact, word order is controlled by discourse information and intonation. More detailed description of the phenomenon is submitted as the final paper for LFG class in SoSe 2024. 

I chose this phenomenon since Russian is my native language and there is no publicly available XLE code that covers any of its phenomenons. I find the particular topic of information structure important to study and develop in code because it is fundamental for encoding word order rules and can be further extended and used for more complex grammar codes.

**Implementation**

Initially, 'utf-8' type of encoding is specified in the Configuration section since the software requires its specification to work with certain language groups.

In order to encode various options of constituency order we use Either-Or '{ | }' syntax and state all the possible options both within sentence rules and NP/VP rules. OT-Marks (with the use of a template) +TOPIC and FOCUS are used to prefer/disprefer respectfully particular parses that are more/less preferable to be initial. With the use of OT-Marks the grammar generates first c- and f-structures of sentences with the most common information structure and intonation pattern (topic followed by focus). 

Punctuation signs COMMA and PERIOD are added. While period at the end of a sentence is optional, comma is required for an optional case of external topic.

Lexical entries were made for sample nouns, a pronoun, verbs and punctuation. In comparison to English, more grammatical functions need to be stated, such as case, number and person. Additionally, these GFs can change endings of words, hence more of lexical entries need to be done. An OT-Mark +pl is used for word _kosti_ to prefer plural form over singular.

**Remaining challenges**

 1. Introduction of possibility to assign TOPIC and FOCUS functions to multiple words and constituents in a sentence, since Russian language allows for that.
 2. Creation of templates or morphological transducer in order to facilitate and optimize adding more lexical entries.
 3. Adding further important aspects of the language like Wh-questions and clitics. 

**Additional files**

This core files of this project are 'code.lfg' containing XLE code and 'testsuite.lfg' containing both correct and incorrect sentence examples for parsing with the code. Explanation of each sentence is available within the file. 

Additional files for the project include:

 1. 'xlerc' file used for more convenient work with the grammar code. It allows to call current code file and parse the testsuite file every time XLE is called within Terminal.
 2. '.gitignore' file that includes functional and hidden files generated from running the software and code.

_Link to the Github repository:_ https://github.com/Arsenia-Denisova/GD-Russian
