# BugTracking
A software idea to include bug tracking in common packages.

# Concept
Many packages (e.g., Python, apt-get) rely on user feedback to alert of bug fixes, but provide no (little?) automatic bug submission features.

The idea behind this project would to include bug submission features in projects globally with an easy de-coupled implementation that could attach to any project in Python or apt-get, etc. (with the users permission).

# Fine-grained Details

## Errors to submit and not submit 

**SHOULD NOT** be submitted
* Errors related to users not following directions (e..g, a user has not installed a dependency)
* Errors that are the result of users modifying the program
* Errors that have already been submitted, although they should be tallied for metrics. Additionally, if the same error is caused by a different cause, it should be submitted as a separate bug. Furthermore, if a bug provides more data for the bug fixer, this data should be appended to the first bug report.

**SHOULD** be submitted
* If a broken dependency exists
* If an error exists in compilation or interpretation
* etc.

Furthermore, de-duplication of errors should also be avoided.

## The submission process
These errors should be sent somewhere, but where? Perhaps creating a [GitHub App](https://developer.github.com/apps/building-github-apps/creating-a-github-app/) and including the bug submissions as issues, but specifying their origin (i.e., from the automatic bug tracking software).

## What to build on?

# Pros and Cons
## Pros
Bug tracking in this way contains a lot of benefits.
* The number of users affected by the bugs can automatically be tallied (of those who opt-in to the bug tracking software)
* Bugs can be triaged more quickly

## Cons
* Users may not be able to interact with bug fixers if the process is annonymous
