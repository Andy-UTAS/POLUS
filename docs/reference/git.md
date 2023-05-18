# Version control (Git)

Have you ever been working on a project, and then realised that what was there previously was actually better? This may be due to making a mistake in your recent work, or you may have just been in the zone last time and only appreciated this after you had scrapped the work you did previously only to replace it with absolute junk and hit save. Or perhaps you are trying to work collaboratively with someone else, or many other people on complex projects which have many constituent parts - as is common in software development - and you are having difficulty knowing which files have been changed, and which parts of the file have been changed. Enter: version control.

![](git/header.gif){: .center}

---

## Introduction

The undertaking of complex projects has always demanded that one fastidiously keep track of progress, and the growth of collaborative projects which are increasingly undertaken non-locally, that is, they are not undertaken at the same place or on the same device, has seen the development of excellent ways of not only tracking progress, but also distributing the progress of one member of a team to all other members of the team. The most common way to accomplish this is by using _distributed version control_, which essentially boils down to all files which within a project - including the history of all files - being mirrored on any device which is used to contribute to the project. Beyond this, there are clever means and standard protocols to ensure problems such as conflicting changes to files arising from simultaneous editing are handled and don't break the whole system. These methods of working are standard across all industries and once you start using them, you will see why.

## Git

Perhaps unsurprisingly, there are quite a few options for distributed version control, but the largest by far is the free and open source software [git](https://git-scm.com/).

!!! Warning "git versus GitHub"
    You may have heard of one or both of [git](https://git-scm.com/) or [GitHub](https://github.com/), and it is important to know that these are distinct entities! We shall flesh out their relationship below, but do not make the mistake of thinking they are the same thing!

    `git`

    :   is a revision control system, a tool to manage your source code history

    `Github`

    :   is a hosting service for Git repositories

    In a crude sense, git is the _tool_ whilst GitHub is the _service_ for projects that use git.


Navigate to the directory to

``` git title="Initialise a directory"
git init
```

``` git title="Add all contents of the directory"
git add .
```

``` git title="Perform initial commit"
git commit -m "Initial commit"
```

## GitHub

https://github.com/

### Creating a remote repository

<figure markdown>
  ![mokugoconnect](git/github.gif)
  <figcaption>Creating a repository on GitHub</figcaption>
</figure>

### Adding a remote repository

``` git title="Add an existing remote repository"
git remote add origin <URL>
```

``` git title="Push content to remote repository"
git push -u origin master
```

``` git title="Change remote repository"
git remote set-url origin <url>
```

``` git title="Remove remote repository"
git remote remove origin
```



--8<-- "includes/abbreviations.md"
