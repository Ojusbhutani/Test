# CSE-241: AI Course Spring 2021 Assignment and Lab Task Submission

README

Introductions to Lab Tasks

The purpose of Lab Tasks is to get some actual practice with using AI techniques. The idea is to have a sequence of tasks which are (most of them) directly and sequentially related to each other. Gradually, they make up the components of a system that will be assembled in the last lab task.

Till now, we had lab tasks closely dependent on the material taught in the course. This time we will do it differently. There may be separate practical assignments based on the topics covered in the class. They will not be given as part of the lab component.

In the lab task, we will have some practice of other techniques which are not covered in the class. These will include traditional machine learning as well as deep neural networks, which will not be taught in the class and you will have get familiar with them on your own. You need not study about them in details, but you should learn to 'implement' them using the libraries available for this purpose.

The overall objective of the lab tasks will be to build a prototype transfer-based Machine Translation engine. This will not be Neural Machine Translation as such, but it will have several components, which may or may not be implemented using deep neural networks. The point is that in this engine, it should be easy to replace the implementation of a component using some other technique, but the engine will still work, although differently.

Keeping this in mind, the following lab tasks are tentatively planned:

Lab Task-1: Tic-Tac-Toe (This will not be a part of the final system, of course)

Lab Task-2: Part-of-Speech (POS) Tagging, Chunking and Named Entity Recognition (NER) using the CRF++ tool.

Lab Task-3: Word embeddings (Word2Vec, GloVe) and spelling error detection using CNN (?)

Lab Task-4: Part-of-Speech (POS) Tagging, Chunking and Named Entity Recognition (NER) using RNN and Bi-LSTM.

Lab Task-5: Isolated Word Morphological Analysis using RNN and Bi-LSTM.

Lab Task-6: Isolated Word Morphological Generation using RNN and Bi-LSTM.

Lab Task-7: Context-sensitive Morphological Analysis and Generation using RNN and Bi-LSTM.

Lab Task-8: Transliteration with NMT

Lab Task-9: Implementing the 'engine' or 'pipepline' using the above components to build a prototype Transfer-based Machine Translation system

To be able to do the above, you will have learn about the basic of the following problems:

POS tagging
Chunking
Named Entity Recognition
Morphological analysis and generation
Transliteration
Transfer-based Machine Translation
Neural Machine Translation
And to be able to implement the components, you will need to get familiar with the following techniques:

CRF++
Word embeddings (Word2Vec and GloVe)
Convolutional Neural Network (CNN)
Recurrent Neural Network (RNN)
Gated Recurrent Unit (GRU)
Long Short Term Memory (LSTM)
Bidirectional LSTM
Neural Machine Translation
Again, note that you don't have study much of theory of these, you just need to learn to implement them. This will be helpful to you this semester (Exploratory Projects) and even more so later on.

Submission of Code on GitHub:

[We will most probably move to GitHub Education for this purpose later on, but right now I am organizing a team structure for the class till we do that. This should be completed by tomorrow afternoon. You won't be able to follow the step below till you join and I have given you the access.]

Register on GitHub (if you are not already registered).
Accept the invitation that I have sent. This will make you a member of the Student sub-team of the CSE-241: AI Course Spring 2021 team, which is part of the NLPRL organisation. You will have access to the NLPRL/CSE-241-AI-Course-Spring-2021---Students repository.
First go through this introduction if you are not familiar with GitHub: https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners
Skip the Step-1 in the introduction mentioned above. Step-0 will involve installing git on your system.
After you have installed git, go to the folder where you keep your AI course related data.
Go inside this folder and run this command:
https://github.com/NLPRL/CSE-241-AI-Course-Spring-2021---Students

This will clone the repository on your system so that you can upload (commit) your code to the repository.
Go inside the NLPRL/CSE-241-AI-Course-Spring-2021---Students folder.
Create a subdirectory with the name in this format: [ROLL NO]-[FIRST NAME]-[LAST NAME], which is the same as given the filename formatting instructions earlier, except that [SUBMISSION NAME] is to be left out of your main folder name [SUBMISSION NAME].
Go inside this submission folder and create the following files: (i) Readme.md (ii) Your Python code files (e.g. four files named solution-1, solution-2 etc. for the first Lab Task). (iii) The Jupyter nodebook. (iv) A PDF file if you have additional comments/opinions about the solutions and your code and if you have not done so in the Readme.md file or the Jupyter notebook.
Note that all this can be done on your system and then from your main submission folder, it can be committed to the repository, so that it will be uploaded/submitted.

You may need to go through these if you are having problems using GitHub:

https://dont-be-afraid-to-commit.readthedocs.io/en/latest/git/commandlinegit.html

https://stackoverflow.com/questions/2505096/cloning-a-private-github-repo

https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token

[If you notice any errors in the above description, let me know.]
