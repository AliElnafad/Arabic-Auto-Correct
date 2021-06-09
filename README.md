# Arabic-Auto-Correct
In this work, we address the problem
of spelling correction in the Arabic lan-
guage utilizing the new corpus provided
by QALB (Qatar Arabic Language Bank)
project which is an annotated corpus of
sentences with errors and their corrections.
The corpus contains edit, add before, split,
merge, add after, move and other error
types. We are concerned with the first four
error types as they contribute more than
90% of the spelling errors in the corpus.
The proposed system has many models to
address each error type on its own and then
integrating all the models to provide an
efficient and robust system to correct arabic words


## Our Approach
Our approach is spell detection and correction using dictionary-based and regular expression 

Dictionary: Arabic wordlist for spell checking 1
is a free dictionary containing 9 million Ara-
bic words. The words are automatically generated
from the AraComLex 2 open-source finite state
transducer.
The dictionary is used in the generation
of candidates and using a special version of
MADAMIRA 3 (Pasha et al., 2014) created for the
QALB shared task using a morphological database
based on BAMA 1.2.1 4 (Buckwalter, 2002). Fea-
tures are extracted for each word of the dictionary
to help in the proposed system in order that each
candidate has features just like the words in the
corpus.

## Our pipline
This project is divided into two parts (Spell-Checker Using Dictionary , Corrector )

Firstly : Spell-Checker Using Dictionary 

in this part user enter his sentence then our system find all words in this sentence from dictionary if word not contian in dictionary , our system detect it as Misspelled

1- We preprocess our dataset by clean it 

2- Getting targets from "QALB-Train2014.m2" to build our dictionary

3- Merge our unique dictionary with AraComLex dictionary  

4- User enter his sentence

Secondely : Corrector
in this part we build some functions to find all suggestions for Misspelled words then we get optimal suggestion word by its probability 









