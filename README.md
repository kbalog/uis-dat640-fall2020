# Information Retrieval and Text Mining course (DAT640), University of Stavanger, fall 2020

## Updates

  * **Oct 26** Deadlines for the group project and further details on the report have been posted.
  * **Oct 23** Team and topic assignments have been sent out in email. Each group is allocated a [dedicated 15mins slot](project/) (during what would normally be lecture hours) to discuss their progress. It is expected that at least one member of the group is present in person.
  * **Oct 23** The answer key to the trial exam (which was last year's exam) has been shared on Canvas.
  * **Oct 21** Clarifications regarding Assignment 5 have been posted [here](assignments/A5_errata.md).
  * **Oct 21** The results for Assignment A3 have been published. The majority of the submissions lost points on the hidden tests, in part due to not accounting for the possibility of empty fields when taking lengths of lists/documents and then dividing by zero. We have also updated the results for Assignment A1.3, where we decided it was more fair to award points for passing the visible part of the final test cell, even if the hidden part of the tests failed.
  * **Oct 20** Given the issues that surfaced in this assignment, the deadline is extended by 48 hours. Clarification and guidance have been posted [here](assignments/A4_errata.md).
  * **Oct 20** There is an error in one of the tests of Assignment 4 (field mapping probabilities). This part of the exercise will be corrected manually. Also, getting less than 2500 items indexed will not be penalized.
  * **Oct 16** The trial exam will be available from Monday 19/10 09:00 until Tuesday 20/10 23:59 on Inspera. It should take 4 hours in total. The exam will not be corrected (apart from the auto-corrected exercises), but answer key will be shared afterwards.
  * **Oct 14** Information on the [group project](project/) has been posted. You need to sign up by filling out [this form](https://forms.gle/1uB4FARyGPJ6d4rt7) by 19/10.
  * **Oct 14** The last assignment (A5) for 10 points has been pushed to the personal GitHub repositories. The deadline is 27/10 16:00.
  * **Oct 13** An error has been discovered in the description of Assignment A4 concerning the value of the Dirichlet smoothing parameter. See the [erratum](assignments/A4_erratum.md).
  * **Oct 7** The results for Assignment A2 have been published on Canvas. Questions concerning assignment correction may be asked during the Wed labs or via email at dat640help@gmail.com.
  * **Oct 7** Assigment 4 has been announced. The Jupyter notebook you need to complete can be found in your personal GitHub repository. This assignment is worth 10 points. The deadline is Oct 20, 16:00.
  * **Oct 7** The results for Assignment A1.3 have been published on Canvas. Given that A1.3 was one of the earlier assignments, we decided to be lenient and manually grade A1.3 to give students as many points as reasonable, which took some time. Please keep in mind for future submissions that your notebook may need to run on a different machine with a different OS, so (i) use os.path to construct paths, and (ii) be mindful of iterable data structures that may not guarantee a specific ordering of elements unless sorted. **The [general instructions for assignments](assignments/) have been extended. Please carefully check them, as we will rely on fully automatic grading in subsequent assignments.**
  * **Oct 5** An error was discovered in assignment A3 in the description under ‘BM25 scoring’, where IDF is defined without the logarithmic function. Instead, IDF should be computed by taking the log of N/n_t.
  * **Sep 30** Assigment 3 has been announced. The Jupyter notebook you need to complete can be found in your personal GitHub repository. This assignment is worth 10 points. The deadline is Oct 13, 16:00.
  * **Sep 24** General information on assignment grading and delivery has been posted [here](assignments/).
  * **Sep 22** Assignment 2 has been announced. The Jupyter notebook you need to complete can be found in your personal GitHub repository. This assignment is worth 10 points. The deadline is Oct 6, 16:00.
  * **Sep 21** You may use the [Issues tab](../../issues/) for posting questions. That way other could also benefit from a clarification. That way other could also benefit from a clarification (and you can also help your fellow students). For example, multiple people raised the issue of "infected" files for A1.3, which has now been clarified [there](../../issues/1).
  * **Sep 21** New format for the next 4 weeks! As of this week, Mondays will be lectures exclusively (lecture videos will follow). The exercises will be posted and done on Tuesdays. People can join in person in the lecture room or work on them remotely and ask for help on the [dedicated slack channel](https://uis-iai.slack.com/archives/C01AW7CA38E). (Note: this slack channel is reserved for this time-slot, i.e., Tuesdays between 14.15 and 16.00).
  * **Sep 21** Results for assignments A1.1 and A1.2 have been posted on Canvas. If you have any questions, you can ask them during the Wednesday labs or send an email to dat640help@gmail.com.

## Course format

**DISCLAIMER: Everything is subject to change.**

The course follows a hybrid format, where lecture videos are provided online and classroom time is used for discussion, [exercises](exercises/), and working on [assignments](assignments/).

This course involves **self-study** (which can be completed online): You're expected to watch the lecture videos, read the corresponding book chapters/sections listed on the last slide of each lecture deck, as well as complete the exercises on GitHub.

There is also a **physical component** which is not obligatory, but highly recommended for an optimal learning experience. This involves discussion and exercises in a regular classroom setting.

There is a double lecture on Mondays, 14:15-16:00 (without dividing into A/B groups). The Tuesday 14:15-16:00 slot is kept for open office hours (in KE E-433). Note that open office hours are meant for questions regarding the lecture material and/or exercises. Issues related to the assignments should be addressed at lab sessions on Wednesdays.

The semester is divided into lecture and group project work periods, with an (optional) trial exam in between.

### Lecture period (weeks 35-42)

  * Mondays and Tuesdays are classes for discussion and exercises, led by Krisztian Balog (KB).
    - The respective video lectures are made available either before or after the class (depending on the topic). If the video is made available before the class, you are expected to watch it, in order to be able to meaningfully participate in the discussion and undertake the exercises.
  * Wednesdays are labs for getting help on the obligatory [assignments](assignments/), led by Trond Linjordet (TL).
    - Assignments are to be solved individually. They constitute 50% the project work.

### Trial exam (week 43)

A trial exam will be made available mirroring the same setup that will be used at the final exam. The exam will not be corrected, but the answer key will be shared.

### Group project work (weeks 44-46)

Students will need to complete a [project](project/) in groups of 2-3, and write a report that will be graded.

There will be a pool of options to select a project from. During the project period, each group can request a 15mins dedicated weekly discussion slot with the lecturer during the class hours (Mon/Tue), and can get feedback on the draft report from the teaching assistant during lab hours (Wed). Both in-person and remote (Zoom) options will be available.


## Lectures and material

| Date | Topic | Lectures | Exercises |
| -- | -- | -- | -- |
| Aug 24 | L1: Welcome and introduction | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-introduction) | [exercises](exercises/20200824/), [solutions](solutions/20200824/) |
| Aug 25 | L2: Text classification | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-classification) | [exercises](exercises/20200825/), [solutions](solutions/20200825/) |
| Aug 31 | L3: Text preprocessing | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-preprocessing), [video lecture](https://youtu.be/s7vvaCtJ7iU) | [exercises](exercises/20200831/), [solutions](solutions/20200831/) |
| Sep 1 | L4: Text classification evaluation | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-classification-evaluation), [video lecture](https://youtu.be/TFze1mbcEbY) | [exercises](exercises/20200901/), [solutions](solutions/20200901/) |
| Sep 7 | L5: Text classification: Naive Bayes  | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-classification-naive-bayes) | [exercises](exercises/20200907/) |
| | L6: Text clustering | (slides to be added) | [exercises](exercises/20200907/) |
| Sep 21 | L7: Search engine architecture | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-search-engine-architecture) | [exercises](exercises/20200922/), [solutions](solutions/20200922/) |
| | L8: Indexing and query processing | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-indexing-and-query-processing) | |
| | L9: Retrieval evaluation | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-retrieval-evaluation) | |
| Sep 28 | L10: Retrieval models | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-retrieval-models) | [exercises](exercises/20200929/), [solutions](solutions/20200929/) |
| | L11: Query modeling | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-query-modeling) | |
| | L12: Web search | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-web-search) | |
| Oct 5 | L13: Semantic search: Entity-oriented search | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-semantic-search-entity-oriented-search) | [exercises](exercises/20201006/), [solutions](solutions/20201006/) |
|  | L14: Semantic search: Entity retrieval | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-semantic-search-entity-retrieval) | |
|  | L15: Semantic search: Entity linking | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-semantic-search-entity-linking) | |
| | Elasticsearch | [code](code/elasticsearch) | |
| Oct 12 | L16: Learning to rank | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-learning-to-rank), [code](blob/master/code/LTR.ipynb) | [exercises](exercises/20201013/), [solutions](solutions/20201013/) |
|  | L17: Neural IR (invited) | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-neural-ir) | |
|  | L18: Table retrieval (invited) | | |

## Grading

The overall grade comes from two components:

  * Project work (40%), of which
    - 50% individual [assignments](assignments/)
    - 50% group project
  * Written exam (60%)

Note that the project grade needs to be >F in order to pass the course.

## Contact and getting help

  * For all course-related matters, the primary contact email is dat640help@gmail.com
  * Wednesday labs are for working on the assignments. This is *the* time to get help!
  * If you need to talk to the lecturer, make an appointment via email. No drop-ins unannounced!
