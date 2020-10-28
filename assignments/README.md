# Assignments

Three main assignments, with the first two divided into sub-assignments (A and B parts).

| Assignment | Announced | Deadline | Points | Status |
| -- | :--: | :--: | --: | -- |
| Assignment 1 (three parts) ||| 10 | |
|   A1.1 | 25/08 | 08/09 16:00 | 2 | Closed, graded |
|   A1.2 | 01/09 | 15/09 16:00 | 3 | Closed, graded |
|   A1.3 ([errata](A1_3_errata.md)) | 08/09 | 22/09 16:00 | 5 | Closed, graded |
| Assignment 2 (A2) | 22/09 | 06/10 16:00 | 10 | Closed, graded |
| Assignment 3 (A3) | 30/09 | 13/10 16:00 | 10 | Closed, graded |
| Assignment 4 (A4) ([errata](A4_errata.md)) | 07/10 | 22/10 16:00 | 10 | Closed, being graded |
| Assignment 5 (A5) ([errata](A5_errata.md)) | 14/10 | 27/10 16:00 | 10 | Closed, being graded |
| **Total** | | | **50** | |

## Workflow and rules

  * Each assignment is given as a Jupyter notebook and is pushed to your private GitHub repository.
  * You are given 2 weeks for each assignment. You need to submit and push the solution to GitHub before the indicated deadline.
  * Deadlines are strict, no extensions, no exceptions!
  * We have a zero tolerance policy for cheating. Copying someone else's solution, even in part, will be considered plagiarism and may result in failing the whole course.
  * Assignments and project work account for **40% of the final grade**.

## General instructions

### How to solve each assignment

  * Make sure to carefully read and follow the assignment-specific instructions in each assignment notebook.
  * Note that the assignments do not rely on `ipytest`. You are not expected to import that package in the assignments. As long as the test cells run without error, the test cells have passed, except in the case of hidden tests.
    - In the case of hidden tests, passing the visible tests is still the best available indication that your solution will also pass the hidden test.  Hidden tests, however, may contain corner cases, larger datasets or other inputs in order to test that you fully understood the methods and/or followed the instructions.
  * Cells:
    - Do not create extra cells in the notebook, at least not in the submitted version, and do not interfere with the test cells provided in the initial assignment notebook.
    - Never delete a cell that is part of the initial assignment notebook, because creating a new cell with the same code is not equivalent to the old cell. Doing this may result in the loss of points.
  * Code format requirements:
    - Only insert code in the sections inside functions or methods **under** the comment `# YOUR CODE HERE`, replacing the `raise NotImplementedError()` line with your solution code, consisting of however many lines of code are needed.
    - Always remove the `raise NotImplementedError()` once you have added solution code below `# YOUR CODE HERE`.
    - Do not delete the line `# YOUR CODE HERE`, it helps both give guidance and troubleshoot students' problems while solving the assignment, and it helps during grading.
    - In general, keep in mind that your code must both be able to run correctly on another computer (and also be understandable where manual troubleshooting becomes necessary). Keep your code neat and clear.
  * Environment:
    - Each assignment specifies which libraries may or may not be imported, but unless otherwise stated only libraries that are part of the standard Anaconda distribution (i.e., the `base` environment of Anaconda without additional libraries installed) may be imported.
    - You may **not** include any `pip install`, `conda install`, or any other commands that change the environment which the autograder is running in. If you do, you may lose all points for that assignment.
    - You may be expected to modify you environment outside of the provided notebook. Managing environments with Anaconda is helpful for this.
  * Time-out:
    - Unless an exception is explicitly stated, your entire notebook should complete within 1-2 hours. If your solution is more time-consuming than that, even if a test would pass eventually, your submission may lose marks.
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
