# Gitbomb

This repository is 61GB, but it takes only few megabytes on github.
If you try to clone it, you will download 61GB.

## How does it work

Use [hard links](https://en.wikipedia.org/wiki/Hard_link), Luke.

I created 1Mb file. Then I created about 61000 hard links.
Git doesn't know anything about hard links, thus it sees them as different files.
But git is clever enough to store them as one file in `.git`.

So... in general:

  1. Repository is only few megabytes before pushing to github.
  2. After pushing to github, repository is 61GB, but github stores it in few megabytes(github stores only `.git` directory, which is small)
  3. After cloning, repository will be 61GB.
