--------------------------------------------------
TREC-2017 LiveQA: Medical Question Answering Task
--------------------------------------------------

The LiveQA'17 medical task focuses on consumer health question answering. We use consumer health questions received by the U.S. National Library of Medicine (NLM). 
We constructed medical question-answer pairs for training and testing, with additional annotations that can be used to develop question analysis and question answering systems.  

Please refer to our overview papers for more information about the constructed datasets and the LiveQA Track: 

	- Asma Ben Abacha & Dina Demner-Fushman. Overview of the Medical Question Answering Task at TREC 2017 LiveQA. TREC, Gaithersburg, MD, 2017.  

	- Eugene Agichtein, Asma Ben Abacha, Eric Nyberg, Donna Harman & Yuval Pinter. Overview of the TREC 2017 LiveQA Track. TREC, Gaithersburg, MD, 2017. 


A summary of the constructed medical datasets is below.  

If you use these datasets, please cite our paper: 

	@inproceedings{LiveMedQA2017,
	  author    = {Asma {Ben Abacha} and Dina Demner{-}Fushman},
	  title     = {Overview of the Medical Question Answering Task at TREC 2017 LiveQA}, 
	  booktitle = {TREC 2017},
	  year      = {2017}
	} 

======================
Medical Training Data
====================== 

We provide 634 question-answer pairs for training: 

	1) TREC-2017-LiveQA-Medical-Train-1.xml => 388 question-answer pairs corresponding to 200 NLM questions. 
	Each question is divided into one or more subquestion(s). Each subquestion has one or more answer(s). 
	These question-answer pairs were constructed automatically and validated manually.

	2) TREC-2017-LiveQA-Medical-Train-2.xml => 246 question-answer pairs corresponding to 246 NLM questions.
	Answers were retrieved manually by librarians. 

The datasets are not exhaustive with regards to subquestions, i.e., some subquestions might not be annotated. We also provide additional annotations for both (i) the Focus and (ii) the Question Type used to define each subquestion. 23 question types were considered (e.g. Treatment, Cause, Diagnosis, Indication, Susceptibility, Dosage) related to four focus categories: Disease, Drug, Treatment and Exam. 

==================
Medical Test Data
==================

Test questions cover 26 question types associated with five focus categories. Each question includes one or more subquestion(s) and at least one focus and one question type. Reference answers are selected from trusted resources and validated by medical experts. Additional annotations for each test question are provided, including: 

  1) List of Foci and their categories:   
	Example: <Q-Focus fid="F1" fcategory="Problem">Beckwith-Wieddeman Syndrome</Q-Focus>
  2) List of relevant keywords and their categories: 
	Example: <Q-Keyword kid="K1" kcategory="Anatomy">ear</Q-Keyword> 
  3) List of question types and associated focus/foci and keyword(s):
	Example: <Q-Type tid="T1" hasFocus="F1,F2">INTERACTION</Q-Type> 

---------------Simplified annotation of a test question-----------
<NLM-QUESTION qid=""> 
 <Original-Question qfile="">
	<Subject></Subject>
	<Message></Message>
	 </Original-Question>
 <Paraphrase></Paraphrase>
 <Annotations>
	<Q-Focus fid="F1" fcategory=""></Q-Focus>
	<Q-Type tid="T1" hasFocus="F1" hasKeyword="K1"></Q-Type>
	<Q-Keyword kid="K1" kcategory=""></Q-Keyword>
 </Annotations>	
 <ReferenceAnswers> 
	<ReferenceAnswer aid="">
		<Answer></Answer>
		<AnswerURL></AnswerURL>
		<Comment></Comment>
	</ReferenceAnswer>	
</ReferenceAnswers>  
</NLM-QUESTION> 
---------------------------------------------------------------------

Contact Information
-------------------
- Asma Ben Abacha: asma.benabacha@nih.gov
- Dina Demner-Fushman: ddemner@mail.nih.gov
