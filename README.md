# Compound-Solutions
ML Engineer Trial Task

## Introduction
This repository contains the code for the trial task from the company Compound Solutions. To view the task more detailed please [click here](https://docs.google.com/document/d/19LhCqx-ARCoAo6JWeQlNEfa0iE2vdg7Gb7RC8mn5GN4/edit). WARNING! Do not forget to upload task files to the same directory in Google Drive where you upload your pre-trained vectors. More detailed in the section called Running below.

Short desctiption of the task: Develop a tool that analyses a given text and suggests improvements based on the similarity to a list of "standardised" phrases. These standardised phrases represent the ideal way certain concepts should be articulated, and the tool should recommend changes to align the input text closer to these standards.


## Technologies
While doing this task the following list of tools were used:
- [Google Drive](https://drive.google.com/drive/my-drive?hl=ru)
- [Google Colab](https://colab.research.google.com/?hl=ru)
- [Fasttext official documentation](https://fasttext.cc/docs/en/english-vectors.html)

## Running
In order to run the code you need to do the following steps:
1. Download pre-trained vectors for Word2Vec model
2. Upload them to your Google Drive
3. Create an account on Google Colab
4. Add your Google Drive storage to the Colab project
5. Install necessary libraries
6. Have a fun and run the code!

Now let's dive into each step and find out how to do it!

First, pre-trained vectors can be downloaded from the official website of the FastText library by [this link](https://fasttext.cc/docs/en/english-vectors.html). Secondly, open Google Drive account and create the folder named "colab". After that unzip the freshly downloaded vectors to your computer and upload them to that folder on your Google Drive. As a third step you need to create a Google Colab account and open the "ML_Engineer_Trial_Task.ipynb" file in your Colab project page. For the fourth step run each code cell starting from the top till the end where you will be asked to allow access to your Google Drive space. WARNING! Make sure that your path to the uploaded vectors are correct in order to run the code succcesfully. In the fifth step you will import all the necessary libraries and functions in the second code cell. As the last step simply run all the remaining code cells in order to get a result.


## Structure
As a first step I made a small research in order to decide which NLP model to use in this task. I stopped at the model called FastText which is developed by the FaceBook company. The reason why I finally used Word2Vec is that FastText caused too many errors and problems during the installation process. More specifically it was connected with uploading and using the ready vectors. Problem was in its format, the model was accepting only the vectors in binary formats but not vector. After spending too much time on debugging and solving the problem I decided to use Word2Vec as I was running out of time. 

My solution proposes simple technique by preprocessing the input text data reading it from the txt file, lowercasing and tokenizing it, after deleting the stop words and finally removing special characters. Then the same algorithm for preprocessing I applied to my terms.

Then I calculated the vectors for each word in input text as for term words. Finally made a similiarity score by using standart cosine similiarity function.

If you do not understand the short decription of the code structure never mind. [Here](https://drive.google.com/file/d/18A6qVGiXIFF5Nev8Esic3TZN9wQDWghe/view?usp=sharing) I attach my link to the video where I explain the code and algorihm itself.
