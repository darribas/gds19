# Contributing

**IMPORTANT**: this document has been adapted from the excellent Contributing
guide of the [UofTCoders' `rcourse`](https://github.com/UofTCoders/rcourse/blob/master/CONTRIBUTING.md).

Geographic Data Science'18 is an open-source course,
aimed to introduce the use of Python for Geographic Data Science. 

## How to Contribute

Anyone can contribute to the course repository via [pull requests][pull-requests].

We use [GitHub flow][github-flow] to manage changes:

1. Create a [fork][fork-explanation] of this repository, and [clone][clone-explanation] it to your local computer.
2. In your local copy of this repository, create a new [branch][branch-explanation].
3. Commit your changes to that branch.
4. Push the edits on that branch to your fork on GitHub.
5. Submit a pull request to the master repository (`darribas/gds18`).
6. If you receive feedback on your pull request, 
make further commits to the new branch on your fork. These will automatically be added to 
your pull request. 

You may wish to look at [How to Contribute to an Open Source Project on GitHub][contribute]
for more detailed instructions. The [GitHub Glossary][glossary] is also a useful resource that explains
Git-related terminology. 

## Format

We follow a consistent format across all course materials. 

A **lesson**
is written in markdown and converted automatically into HTML and PDF through a
[`Makefile`][makefile]. See, for example, the `.md` file of the [first
lesson](https://github.com/darribas/gds18/blob/master/content/lectures/lecture_01.md) and the [HTML](https://github.com/darribas/gds18/blob/master/slides/lecture_01.html) and [PDF](https://github.com/darribas/gds18/blob/master/slides/lecture_01.pdf) versions. 

**Labs** are written as Jupyter Notebooks (`.ipynb`) and rendered also as HTML and PDF files. See an example of [Lab-1](https://github.com/darribas/gds18/blob/master/content/labs/lab_01.ipynb), and the [HTML](https://github.com/darribas/gds18/blob/master/content/labs/lab_01.ipynb) and [PDF](https://github.com/darribas/gds18/blob/master/content/labs/lab_01.pdf) files produced automatically through the [`Makefile`][makefile].


[branch-explanation]: https://help.github.com/articles/about-branches/
[clone-explanation]: https://help.github.com/articles/cloning-a-repository/
[contribute]: https://egghead.io/courses/how-to-contribute-to-an-open-source-project-on-github
[fork-explanation]: https://help.github.com/articles/fork-a-repo/
[github-flow]: https://guides.github.com/introduction/flow/
[glossary]: https://help.github.com/articles/github-glossary/
[makefile]: https://github.com/darribas/gds18/blob/master/Makefile

