# Day 3 - Computation of Discourse Structure

## Presentation

* pipeline model
* OPT parser

---

## Existing discourse parsers (for English)

This is an incomplete list of discourse parsers for English. I've included only parsers which are available online and can be installed and run with reasonable effort.
Parsers which, after downloading, are up and running **and** can parse regular text input are marked with (*).

### 2Taggers (*)

* http://www.cs.columbia.edu/~orb/code_data.html
* Or Biran and Kathleen McKeown. PDTB Discourse Parsing as a Tagging Task: The Two Taggers Approach. SIGDIAL 2015, Prague, Czech Republic

`java -Xmx8G -cp bin:lib/* discourse.tagger.app.DiscourseTaggingDirectoryRunner ../../Sample_Texts/ ../../Sample_Texts_parsed/2Taggers/`


### Lin Parser

* https://github.com/linziheng/pdtb-parser
* You can try out the parser at http://wing.comp.nus.edu.sg/~linzihen/parser/
* Ziheng Lin, Hwee Tou Ng and Min-Yen Kan (2014). A PDTB-Styled End-to-End Discourse Parser. Natural Language Engineering, 20, pp 151-184. Cambridge University Press.

* need to **FIX** Lin Parser first as to instructions here: https://github.com/linziheng/pdtb-parser/issues/1


### Lin Parser, JAVA version (*)

* https://github.com/WING-NUS/pdtb-parser

`java -jar parser.jar ../../Sample_Texts/`

Output is in *.pipe


### Discopy -- Lin Parser Reimplementation

* https://github.com/rknaebel/discopy
* very nice modular Python reimplemenation of the Lin parser
* runs on CONLL style input

### Wang/Lan

* needs CONLL style input
* https://github.com/lanmanok/conll2015_discourse
* https://aclanthology.coli.uni-saarland.de/pdf/K/K15/K15-2002.pdf


### OPT

* needs CONLL Shared Task style input
* https://hub.docker.com/r/oslopots/oslopots-conll-2016/
* https://aclweb.org/anthology/K/K16/K16-2002.pdf


### Frankfurt Shallow Discourse Parser

* needs CONLL Shared Task style input
* only implicit relation classification
* English and Chinese
* simple neural model
* https://github.com/acoli-repo/shallow-discourse-parser
* https://www.aclweb.org/anthology/K16-2005
* ported to Python3 and Keras: https://github.com/AtreyaSh/shallow-discourse-parser

### UNITN Shallow Discourse Parser

* https://github.com/esrel/DP
* CONLL 2016 Shared Task Uni Trento submission
* runs on CONLL input
* __This repository contains a script [txt2json.sh](https://github.com/esrel/DP/blob/master/txt2json.sh) which, given the installation of the Berkeley and Stanford syntactic parsers, can convert plain text input into the CONLL JSON format__

### ETS: RST (Deep) Discourse Parser

* https://github.com/EducationalTestingService/discourse-parsing
