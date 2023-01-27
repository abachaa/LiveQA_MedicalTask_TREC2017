--------------------------------------------------
TREC-2017 LiveQA: Medical Question Answering Task
--------------------------------------------------

The LiveQA'17 medical task focuses on consumer health question answering. We use consumer health questions received by the U.S. National Library of Medicine (NLM). 
We constructed medical question-answer pairs for training and testing, with additional annotations that can be used to develop question analysis and question answering systems.  

Please refer to our overview paper for more information about the constructed datasets and the LiveQA Track: 

	- Asma Ben Abacha, Eugene Agichtein, Yuval Pinter & Dina Demner-Fushman. Overview of the Medical Question Answering Task at TREC 2017 LiveQA. TREC, Gaithersburg, MD, 2017 (https://trec.nist.gov/pubs/trec26/papers/Overview-QA.pdf). 

A summary of the constructed medical datasets is below.   

If you use these datasets, please cite our paper: 

	@inproceedings{LiveMedQA2017,
	  author    = {Asma {Ben Abacha} and Eugene Agichtein and Yuval Pinter and Dina Demner{-}Fushman}, 
	  title     = {Overview of the Medical Question Answering Task at TREC 2017 LiveQA}, 
	  booktitle = {TREC 2017},
	  year      = {2017}
	} 

=========================
Medical Training Data
========================= 

We provide 634 question-answer pairs for training: 

	1) TREC-2017-LiveQA-Medical-Train-1.xml => 388 question-answer pairs corresponding to 200 NLM questions. 
	Each question is divided into one or more subquestion(s). Each subquestion has one or more answer(s). 
	These question-answer pairs were constructed automatically and validated manually.

	2) TREC-2017-LiveQA-Medical-Train-2.xml => 246 question-answer pairs corresponding to 246 NLM questions.
	Answers were retrieved manually by librarians. 

The datasets are not exhaustive with regards to subquestions, i.e., some subquestions might not be annotated. We also provide additional annotations for both (i) the Focus and (ii) the Question Type used to define each subquestion. 23 question types were considered (e.g. Treatment, Cause, Diagnosis, Indication, Susceptibility, Dosage) related to four focus categories: Disease, Drug, Treatment and Exam. 

=====================
Medical Test Data
=====================

Test questions cover 26 question types associated with five focus categories. Each question includes one or more subquestion(s) and at least one focus and one question type. Reference answers were selected from trusted resources and validated by medical experts. We provide at least one reference answer for each test question, its URL and relevant comments. Question paraphrases were created by assessors and used with the reference answers to judge the participants' answers.  


---------------------------------
Question Summaries & Annotations
---------------------------------

We also created summaries of the LiveQA test questions in the context of our work on Consumer Health Question Summarization, as described and used in the following paper: "On the Role of Question Summarization and Information Source Restriction in Consumer Health Question Answering". Asma Ben Abacha & Dina Demner-Fushman. AMIA 2019 Informatics Summit (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6568117/). 

Additional annotations for each test question are provided, including: 

  1) List of Foci and their categories:   
	Example: <FOCUS fid="F1" fcategory="Problem">Beckwith-Wieddeman Syndrome</FOCUS>
  2) List of relevant keywords and their categories: 
	Example: <KEYWORD kid="K1" kcategory="Anatomy">ear</KEYWORD> 
  3) List of question types and associated focus/foci and keyword(s):
	Example: <TYPE tid="T1" hasFocus="F1,F2">INTERACTION</TYPE>  
 	

---------------Simplified annotation of a test question-----------
<NLM-QUESTION qid=""> 
 <Original-Question qfile="">
	<SUBJECT></SUBJECT>
	<MESSAGE></MESSAGE>
 </Original-Question>
 <NIST-PARAPHRASE></NIST-PARAPHRASE>
 <NLM-Summary></NLM-Summary>

 <ANNOTATIONS>
	<FOCUS fid="F1" fcategory=""></FOCUS>
	<TYPE tid="T1" hasFocus="F1" hasKeyword="K1"></TYPE>
	<KEYWORD kid="K1" kcategory=""></KEYWORD>
 </ANNOTATIONS>	 
 <ReferenceAnswers> 
	<ReferenceAnswer aid="">
		<ANSWER></ANSWER>
		<AnswerURL></AnswerURL>
		<COMMENT></COMMENT>
	</ReferenceAnswer>	
 </ReferenceAnswers>   
</NLM-QUESTION> 
---------------------------------------------------------------------

------------------------------------
MedQuAD & Additional Judged Answers
------------------------------------

TestDataset (https://github.com/abachaa/LiveQA_MedicalTask_TREC2017/tree/master/TestDataset) contains the annotations of the test questions, the reference summaries, and the judgments of the participants' answers (qrels_NIST). 

In our BMC Bioinformatics paper "A question-entailment approach to question answering" (https://bmcbioinformatics.biomedcentral.com/articles/10.1186/s12859-019-3119-4), we have manually judged 2,479 additional answers retrieved from the MedQuAD collection to TREC-2017 LiveQA-Med questions. 

The MedQuAD collection and the 2,479 judged answers are available at https://github.com/abachaa/MedQuAD. 
 
