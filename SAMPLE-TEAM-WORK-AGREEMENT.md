# Mango Engineering Team Working Agreement

## Code Review Guidelines
At Mango Engineering, we use the the feature branch workflow to collaborate on our code bases. The following is our code contribution
guidelines.

### Before you start
- Make sure you are assigned to a JIRA ticket.
- All code changes must be linked to a JIRA ticket. 
  - Should no ticket exist, create one and assign yourself to it.

### Making changes
- Create a topic branch for each new feature or bugfix you'll be basing your work on.

**How to create a topic branch**
```
git checkout dev
git pull origin dev
git checkout -b las-101-a-brief-feature-summary
```

- Always commit logical units of work.
- Every commit should be buildable and functional if checked out directly.
- If you need to temporarily save your work, stash your changes or commit and rebase later.

### Branch Guidelines
- All branch names must be in the proper format

branch name format: {JIRA ticket number}-{feature/fix/update}-{some identifiable description of change}

- Branches must be written in lower case letters.
- Branches must start with a JIRA ticket number.
- Branches must include a brief summary of the ticket.
- Branches must follow Kebab Case.
- Branch names should be kept below 40 characters.

**Examples of valid branch names**
DEV101-feature-a-brief-feature-summary
ENG333-fix-misaligned-toast
IT129-update-platform-docs

### Commit message guidelines
- All commit messages must be in the proper format.
- Commits must start with a valid topic:

(feature) - a feature change

(fix) - a bug fix change

(test) - unit test changes only

(refactor) - code reorganizations and improvements that do not affect functionality

(docs) - documentation changes only

(lint) - anything style/code quality related that does not affect functionality

(setup) - build and compile process related changes only

- Commits must be in imperative form.
(Further Reading: Seven Rules)

- Commit messages should not exceed 50 characters including the topic.
- In most cases, a declarative, one-line commit message is all you need.
- For more complex commits, a description block may be added to clarify.
    - Description blocks may include up to 72 characters per line.
    - The following is an example of a properly formatted commit message

    ```
    (fix) Use cache groups to improve grid performance
    Fabric.js' performance suffers when too many ungrouped items are on the
    screen. This can be easily avoided by grouping a large number of elements
    into smaller fabric.js groups. This commit introduces this grouping.
    
    There is however a distinct disadvantage using groups for the background
    grid:
    - The background grid uses 1px lines which become blurred when grouped
    - Fabric.js (v1.7.8) does not currently support "non-scaling stroke". See
    kangax/fabric.js#3042
    
    A possible solution might be to create and render a workspace vector
    graphic without relying on fabric.js directly onto the HTML5 canvas.
    ```

    Reference:
    - https://www.w3.org/TR/SVGTiny12/painting.html#NonScalingStroke


### Before you push
- Make sure you have added the necessary tests for your changes.
- Run all tests to assure nothing else was accidentally broken.
- Run any linting to make sure the code passes our code quality standards.
- Once you are ready, push your branch to the remote repository: `git push origin remote DEV101-feature-a-brief-feature-summary`

### Getting your code reviewed
We strive to have every line of code reviewed by at least two other developers to make sure we did not forget something obvious, break
something unintentionally, or isolate information from other developers on the team. For this reason, we use GitHub code reviews. Code may not be merged until it passes acceptance by at least two other
developers.

**Our pull request process**
1. Open the repository on GitHub.
1. Go to Pull Requests > New pull request.
1. Select your branch to compare.
1. Click "Create pull request".
1. Assign yourself as Assignee to the PR.
1. Assign at least two other developers as Reviewers (if two developers aren't already auto-added)
  - At most, assign 2-3 developers to a PR.
  - Assign more if absolutely necessary.
7. Edit the PR title to include your ticket number in uppercase.
1. Add a JIRA ticket link to the PR description.
1. Add any other information you think is necessary for the reviewers.
1. Specify changes you made that clarify commits.
1. Once you are ready, click "Create pull request"

### The review process
Developers you assigned to your pull request will be notified. Give the reviewers some time to review your changes. Remember, they may be
working on a feature right now and cannot immediately review your code. All code reviews should be addressed within 24 hours.

### Accepting changes
Once your code is reviewed and passed all continuous integration checks, it is time to merge your work. For this, we use the "Squash and merge"
feature on GitHub. To accept your changes, open your PR and click "Squash and merge". An editor will open:

1. Make sure your commit message starts with a capital JIRA ticket number.
2. Make sure to clean up any work-in-progress commits from the commit description.
3. Properly format the message as described above.

When you are ready, accept the commit and delete your branch locally and from GitHub.

References
http://nvie.com/posts/a-successful-git-branching-model/
