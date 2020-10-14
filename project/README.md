# Group project

The objective of project work is to apply the knowledge gained in the course to an open research problem.  Students are expected to work in groups of 2-3 and work on a project of their choosing from the list of available projects.

**IMPORTANT** You'll need to sign up for the group project by filling out [this form](https://forms.gle/1uB4FARyGPJ6d4rt7) by 19 October at the latest. People failing to sign up will automatically receive 0 points on their project work.

On the sign up form, you'll need to specify a first and a second project preference. We'll do our best to grant you your first preference and the best way for you to make sure it happens is to form a team with 1 or 2 additional students. Otherwise, we'll need to team you up with others.


## Projects

You may choose one from the following projects:

  * [MS Marco Document re-ranking](https://microsoft.github.io/msmarco/)
    - Given a candidate top-100 document as retrieved by BM25, re-rank documents by relevance. This task has also run as part of the TREC 2019 Deep Learning track.
    - Document collection: MS MARCO document corpus (3.2M documents, 22GB)
    - Resources
      - [Task GitHub repo](https://github.com/microsoft/MSMARCO-Document-Ranking)
      - [TREC 2019 Deep Learning track overview](https://arxiv.org/abs/2003.07820)
  * [TREC 2019 Conversational Assistance](http://www.treccast.ai/)
    - Given a series of conversational utterances, identify relevant passages for each user utterance that satisfies the user's information need.
    - Document collection: MARCO Ranking passages, Wikipedia, and News (Washington Post)
    - Resources
      - [Task GitHub repo](https://github.com/daltonj/treccastweb)
      - [TREC 2019 Conversational Assistance track overview](https://arxiv.org/abs/2003.13624)
  * [Semantic Answer Type Prediction](https://smart-task.github.io/)
    - Given a question in natural language, the task is to predict type of the answer using a set of candidates from a target ontology (DBpedia).
    - Document collection: DBpedia ([dump 2016-10](https://wiki.dbpedia.org/downloads-2016-10)) and/or Wikidata
    - Resources
      - [Task GitHub repo](https://github.com/smart-task/smart-dataset)
      - Papers: [Balog & Neumayer (2012)](https://krisztianbalog.com/files/cikm2012-querytypes.pdf), [Garigliotti et al. (2017)](https://krisztianbalog.com/files/sigir2017-qt.pdf)


## Objectives

The overall objective of the group project is to develop and experimentally compare approaches for a given information retrieval problem. Specifically, you'll first need to establish a reasonable baseline, then develop one or multiple advanced methods aiming to improve over the baseline. Using a standard test collection, you'll need to experimentally compare the baseline and advanced solutions.


## Workflow and rules

  * You'll need to hand in a report using the specified project template. The page limit for the report is 4 A4 pages (in double column format).
  * You'll also need to submit your code and the generated output files so that we can verify your solution and results.
  * There are no restrictions on the programming language, toolkits/libraries used, etc. with the default choice being Python and the packages used in the exercises/assignments.
  * You are free to use any external data collections or resources (e.g., pre-trained embeddings) in addition to the 'official' problem datasets.
  * Some of the problems involve working with large datasets. If you need server access, you'll need to contact the Unix system administrator.
  * While you are expected to work individually, you'll have the possibility to get feedback on your ideas in a regular weekly basis. For each group, there will be a weekly dedicated 15mins slot to discuss the project with the lecturer. Also, there will be an internal intermediate deadline for getting feedback on the draft of your report.

## Timeline

While the following is merely a recommendation, it may help you to stay on course.

  * Week 1:
    - Understand the problem
    - Preprocess and index the document collection
    - Implement a baseline method
  * Week 2
    - Run and evaluate the baseline method
    - Implement an advanced method
    - Write up your progress so far and submit the report for feedback    
  * Week 3
    - Run and evaluate your advanced method
    - Experiment with additional methods or refinements of your advanced method
    - Finalize your report


## Evaluation

Project submissions will be graded with respect the following categories:

| Category | Points |
| -- | -- |
| Problem understanding | 5 |
| Baseline method | 10 |
| Advanced method(s) | 15 |
| Report | 15 |
| Code quality | 5 |
| **Total** | **50** |

*More details on each of the above criteria will follow.*
The evaluation will not be automated like in the assignments, and therefore it will primarily proceed based on qualitative categories, rather than operationalized criteria. On the one hand, this means less certainty for you regarding what level of quality is good enough for a certain grade. On the other hand, if your work is truly excellent in some aspects within a category, this can make up for more deficient aspects in the same category. In short, do your best and the evaluation will look out for opportunities to justify awarding points.

Nevertheless, keep in mind that these key aspects of each grading category are some of the ways your project submission may score points:


  * Problem understanding
    - Demonstrating your understanding of the chosen project and associated task.
	- Clearly explaining the problem at hand, and the challenges it may entail.
	- Identifying main families of approaches developed for the task at hand (a literature review).
  * Baseline method
    - Selecting a sensible baseline, implementing and evaluating it experimentally.
  * Advanced method(s)
    - Selecting an interesting or performant advanced method, implementing and evaluating it experimentally.
    - Motivating, designing and implementing one or multiple advanced approaches.
	    - Either extending the baseline,
		- Employing a completely different approach found in the literature, or
		- Designing a method of your own.
	- Clarity of argumentation
	- Creativity
	- Demonstrating understanding of the advanced methods
	- Extensiveness of the experiments
	- Overall performance (improvements over baseline).
  * Report
    - Clearly explaining the motivation or rationale behind the choices made.
	- Documenting key technical decisions to support future reproducibility.
	    - This requires details with accessible wording and structure in a way that your results are reproducible based on the provided description.
	- Producing insight into the process through analysis and discussion of results.
	- Effectively using visual tools, such as illustrations, plots and tables to support and communicate your findings.
  * Code quality
    - Clearly structured and readable code.
	- Readability includes sensible variable/method naming conventions and adding docstrings/comments where necessary.
