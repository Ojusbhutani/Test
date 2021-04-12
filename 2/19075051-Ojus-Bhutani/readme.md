Lab Task-7:- Bilingual Dictionary Induction Using Lexical Transfer and comparable Corpora. 
 
AIM:- To create Bilingual Dictionary from Comparable Corpora first using fast text embeddings and then word2vec embeddings 
 
### Procedure 
### FastText Embedding 
-	Create a new notebook on google colab. 
-	Download [this](https://github.com/artetxem/vecmap) repo. 
-	Download English FastText embedding from 
[here](http://corpus.leeds.ac.uk/serge/bucc/ukwac.vec.xz). 
-	Download German FastText embedding from [here] http://corpus.leeds.ac.uk/serge/bucc/dewac.vec.xz. 
-	Extract the embeddings using  
 	!unxz < ukwac.vec.xz > ukwac.txt 
 	!unxz < dewac.vec.xz > dewac.txt 
-	Now, use the following commands to generate English to German and German to English mappings respectively: 
 !python3 map_embeddings.py --unsupervised ukwac.txt dewac.txt ukwac1_MAPPED.EMB dewac1_MAPPED.EMB --cuda 
 
    !python3 map_embeddings.py --unsupervised dewac.txt ukwac.txt dewac2_MAPPED.EMB ukwac2_MAPPED.EMB  --cuda 
 
-	Download the required dictionary for evaluation from 
[here](https://comparable.limsi.fr/bucc2020/bucc2020-task.html). 
-	Evaluate the models using the following commands: 
 	! python3 eval_translation.py ukwac1_MAPPED.EMB dewac1_MAPPED.EMB -d en-de-1-
5000-training.txt 
 	! python3 eval_translation.py dewac2_MAPPED.EMB ukwac2_MAPPED.EMB -d de-en-1-
5000-training.txt 
 
### Word2Vec Embedding 
-	Download the corpora data present on BUCC 2020 shared task. 
-	Extract it using 
 	!unxz < ukwac.ol.xz > ukwac.txt 
     	!unxz < dewac.ol.xz > dewac.txt 
-	Now, we need to create word2vec embeddings by preprocessing te data. 
-	After that, follow the same procedure mentioned above to generate and evaluate mappings. 
 

# Drive link for mappings are: https://drive.google.com/drive/folders/1dAQyzK1T8REVShIpYAn9Xi0V5UIZxSaW?usp=sharing
 
# Folder Structure  bash 
├── README.md 
├── word2vec.ipynb 
└── fasttest.ipynb 
 
 
# Result 
### FastText: 
-	English to German:- Coverage: 99.55%  Accuracy: 63.99% - German to English:- Coverage: 99.40%  Accuracy: 62.22% ### Word2Vec: 
-	English to German:- Coverage: 15.81%  Accuracy: 11.89% 
-	German to English:- Coverage: 21.8%  Accuracy: 13.86% 
 
### Conclusion  
The accuracy of the dictionaries generated from using the Word2Vec embeddings are less than that we receive from using the Fasttext embeddings. 
The main reasons for this :  
 
> Word2vec -  treats each word in a corpus like an atomic entity and generates a vector for each word ,thus word2vec treats words as the smallest unit to train on. 
>FastText — Which is essentially an extension of the word2vec model — treats each word as composed of character n-grams. So the vector for a word is made of the sum of this character ngrams. 
 
>The key difference between FastText and Word2Vec is the use of n-grams. 
Word2Vec learns vectors only for complete words found in the training corpus. FastText, on the other hand, learns vectors for the n-grams that are found within each word, as well as each complete word.  N-gram feature is the most significant improvement in FastText, it somewhat even solves OOV(Out-of-Vocabulary) issue. 
