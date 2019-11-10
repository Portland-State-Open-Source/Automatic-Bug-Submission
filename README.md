# BugTracking
A software idea to include bug tracking in common packages.

# Concept
Many packages (e.g., Python, apt-get) rely on user feedback to alert of bug fixes, but provide no (little?) automatic bug submission features.

The idea behind this project would to include bug submission features in projects globally with an easy de-coupled implementation that could attach to any project in Python or apt-get, etc. (with the users permission).

# Fine-grained Details

## Errors to submit and not submit 
There needs to, however, be a way to **NOT** include errors related to users not following directions. For example, if a user has not installed a dependency, that should not be a submitted issue. But if a broken dependency exists, that **SHOULD** be automatically submitted.

Furthermore, de-duplication of errors should also be avoided.

## The submission process
These errors should be sent somewhere, but where? Perhaps creating a [GitHub App](https://developer.github.com/apps/building-github-apps/creating-a-github-app/) and including the bug submissions as issues, but specifying their origin (i.e., from the automatic bug tracking software).
