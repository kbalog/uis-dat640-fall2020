# Assignments

Three main assignments, with the first two divided into sub-assignments (A and B parts).

| Assignment | Announced | Deadline | Points | Status |
| -- | :--: | :--: | --: | -- |
| Assignment 1 (three parts) ||| 10 | |
|   A1.1 | 25/08 | 08/09 16:00 | 2 | Closed, graded |
|   A1.2 | 01/09 | 15/09 16:00 | 3 | Closed, graded |
|   A1.3 ([amendments](A1_3_amendments.md)) | 08/09 | 22/09 16:00 | 5 | Closed, grading in progress |
| Assignment 2 (A2) | 22/09 | 06/10 16:00 | 10 | Open |
| Assignment 3 (A3) | 29/09 | 13/10 16:00 | 10 | Not announced yet |
| Assignment 4 (A4) | 06/10 | 20/10 16:00 | 10 | Not announced yet |
| Assignment 5 (A5) | 13/10 | 27/10 16:00 | 10 | Not announced yet |
| **Total** | | | **50** | |

## Workflow and rules

  * Each assignment is given as a Jupyter notebook and is pushed to your private GitHub repository.
  * You are given 2 weeks for each assignment. You need to submit and push the solution to GitHub before the indicated deadline.
  * Deadlines are strict, no extensions, no exceptions!
  * We have a zero tolerance policy for cheating. Copying someone else's solution, even in part, will be considered plagiarism and may result in failing the whole course.
  * Assignments account for **40% of the final grade**.

## General instructions

### How to solve each assignment

  * Make sure to carefully read and follow the assignment-specific instructions in each assignment notebook.
  * Note that the assignments do not rely on `ipytest`. You are not expected to import that package in the assignments. As long as the test cells run without error, the test cells have passed, except in the case of hidden tests.
    - In the case of hidden tests, passing the visible tests is still the best available indication that your solution will also pass the hidden test.
  * Do not create extra cells in the notebook, at least not in the submitted version, and do not interfere with the test cells provided in the initial assignment notebook.
  * Only insert code under the sections with comment `# YOUR CODE HERE`, replacing the `raise NotImplementedError()` line with your solution code, consisting of however many lines of code are needed.
  * Do not change the name of the notebook file.
  * Make sure not to push data files to your assignment repository. This is mostly take care of by the initial code provided in the assignment notebooks, but you may wish to add additional lines to the `.gitignore` file in each assignment folder before making any commits that include large data files.

### How submissions are graded

  * The test cells provided with the assignment notebooks are exactly what the autograder expects. They are read-only and should not be possible to change with normal use of the jupyter notebook interface. Any tampering with the test cells will be recognized and the correct test cells will be automatically inserted.
  * Passing each test cell provides the number of points stated in the assignment notebook. If the number of points per test cell is not stated explicitly, passing the test cell will provide 1 point.
  * The points are granted in an all-or-nothing manner. In other words, if a single test cell is worth 2 points, it is possible to get either 2 or 0 points for that test cell, but not 1 point.

### How to ask for help

  * When you are unsure and have made a reasonable effort to solve a problem you are stuck on, the best option is to use the Lab period on Wednesdays to get help with the assignment. This will solve your issue much faster, especially if you get started on the assignment when it's published.
    - Troubleshooting over email is not only more time-consuming due to the time-lag between question and response, but also because communication bandwidth is reduced.
  * You may send questions to dat640help@gmail.com, but make sure to do the following:
    - First make a reasonable effort to solve your problem, reviewing the instructions.
    - Write an explanation of your understand of what you are trying to accomplish, referring to the specific part of the assignment notebook which you are stuck on.
    - Summarize what you have already tried.
    - Explain what you believe to be possible causes of the issues you are having.
  * If you request help via dat640help@gmail.com, do so early so that there may be time to respond.

### How to stay organized

  * Make sure that the directories for your local repositories `ir-course` and `{github_username}-assignments` are separate and that one does not contain the other.
