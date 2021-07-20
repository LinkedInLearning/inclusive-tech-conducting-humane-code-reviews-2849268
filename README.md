# Inclusive Tech: Conducting Humane Code Reviews
This is the repository for the LinkedIn Learning course Inclusive Tech: Conducting Humane Code Reviews. The full course is available from [LinkedIn Learning][lil-course-url].

Learn how to conduct fair, objective, and productive code reviews and still like your teammates afterward! Instructor Adrienne Braganza Tacke explains why we conduct code reviews, the main pain points teams experience, and what your team needs to make code reviews successful. She explores objectivity and how to write constructive feedback, covers why your team needs a working agreement and how to create one, and offers tools and automations to make the process faster and easier for your team. Successful code reviews have an inclusive mindset, so Adrienne also steps through how to master writing any kind of code review comment, even constructive feedback, and covers how to formalize an enforceable code review process. With buy-in from the whole team and a clear, detailed process laid out, process loopholes should be minimized and hopefully eradicated for good.

## Instructions
This repository has branches for each of the videos in the course. You can use the branch pop up menu in github to switch to a specific branch and take a look at the course at that stage, or you can add `/tree/BRANCH_NAME` to the URL to go to the branch you want to access.

## Branches
The branches are structured to correspond to the videos in the course. The naming convention is `CHAPTER#_MOVIE#`. As an example, the branch named `02_03` corresponds to the second chapter and the third video in that chapter. 
Some branches will have a beginning and an end state. These are marked with the letters `b` for "beginning" and `e` for "end". The `b` branch contains the code as it is at the beginning of the movie. The `e` branch contains the code as it is at the end of the movie. The `main` branch holds the final state of the code when in the course.

When switching from one exercise files branch to the next after making changes to the files, you will get a message like this:

    error: Your local changes to the following files would be overwritten by checkout:        [files]
    Please commit your changes or stash them before you switch branches.
    Aborting

To resolve this issue:
	
    Add changes to git using this command: git add .
	Commit changes using this command: git commit -m "some message"

## Installing
1. To use these exercise files, you must have the following installed:
	- git
	- IDE of your choice (VS Code, Sublime, Atom, etc.)
2. Clone this repository into your local machine using the terminal (Mac), CMD (Windows), or a GUI tool like SourceTree.
3. The code review challenge (Video 04-05) will rely on you and your teammates / another individual to go through the pull request system in GitHub to practice your code review comments! Check out this [helpful guide](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request) on how to open a pull request in GitHub.

### Instructor

**Adrienne Braganza Tacke**

_Author and engineer who enjoys teaching others about software development._

Check out my other courses on [LinkedIn Learning](https://www.linkedin.com/learning/instructors/adrienne-braganza-tacke?u=104).

[lil-course-url]: https://www.linkedin.com/learning/inclusive-tech-conducting-humane-code-reviews
