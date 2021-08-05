# Information Retrieval and Text Mining course (DAT640), University of Stavanger, fall 2020

## Course format

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
| Aug 25 | L2: Text classification | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-classification), [video lecture](https://youtu.be/3LMjRlwZzSA) | [exercises](exercises/20200825/), [solutions](solutions/20200825/) |
| Aug 31 | L3: Text preprocessing | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-preprocessing), [video lecture](https://youtu.be/IuBvlOuD3js) | [exercises](exercises/20200831/), [solutions](solutions/20200831/) |
| Sep 1 | L4: Text classification evaluation | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-classification-evaluation), [video lecture](https://youtu.be/3LdPjTW3F6I) | [exercises](exercises/20200901/), [solutions](solutions/20200901/) |
| Sep 7 | L5: Text classification: Naive Bayes  | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-text-classification-naive-bayes), [video lecture](https://youtu.be/EIXxvno9hLU) | [exercises](exercises/20200907/) |
| | L6: Text clustering | (slides to be added) | [exercises](exercises/20200907/) |
| Sep 21 | L7: Search engine architecture | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-search-engine-architecture), [video lecture](https://youtu.be/ar_XNgaimys) | [exercises](exercises/20200922/), [solutions](solutions/20200922/) |
| | L8: Indexing and query processing | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-indexing-and-query-processing), [video lecture](https://youtu.be/JNXn6BV9lMM) | |
| | L9: Retrieval evaluation | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-retrieval-evaluation), [video lecture](https://youtu.be/b8KoTQYDjxA) | |
| Sep 28 | L10: Retrieval models | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-retrieval-models), [video lecture](https://youtu.be/EAqjKmSbIzk) | [exercises](exercises/20200929/), [solutions](solutions/20200929/) |
| | L11: Query modeling | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-query-modeling), [video lecture](https://youtu.be/2qBD5vbIgvc) | |
| | L12: Web search | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-web-search), [video lecture](https://youtu.be/hyrMVIM-h1I) | |
| Oct 5 | L13: Semantic search: Entity-oriented search | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-semantic-search-entity-oriented-search), &dagger; | [exercises](exercises/20201006/), [solutions](solutions/20201006/) |
|  | L14: Semantic search: Entity retrieval | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-semantic-search-entity-retrieval), &dagger; | |
|  | L15: Semantic search: Entity linking | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-semantic-search-entity-linking), &dagger; | |
| | Elasticsearch | [code](code/elasticsearch) | |
| Oct 12 | L16: Learning to rank | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-learning-to-rank), [video lecture](https://youtu.be/fU_uSS2KU8Y), [code](blob/master/code/LTR.ipynb) | [exercises](exercises/20201013/), [solutions](solutions/20201013/) |
|  | L17: Neural IR (invited) | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-neural-ir), [video lecture](https://youtu.be/U0G-83_7ntw) | |
|  | L18: Table retrieval (invited) | [slides](https://speakerdeck.com/kbalog/information-retrieval-and-text-mining-2020-table-retrieval), [video lecture](https://youtu.be/Bdw8UkLn2Ns) | |

<sup>&dagger;</sup>Lectures L13-15 closely follow book chapters 1, 2, 3 and 5 of the Entity-Oriented Search book (available [open access](https://rd.springer.com/content/pdf/10.1007%2F978-3-319-93935-3.pdf)), therefore, no video lectures are made for them. Check the chapters for a detailed narrative.

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
