

<img src="https://miro.medium.com/max/1920/1*cKaYfzjtBxmJDp6xWnvHTQ.jpeg" alt="drawing" height="312" width="711">

[https://wall.alphacoders.com/](https://wall.alphacoders.com/)

Hello peeps!!  
If you haven't read  [Part-1](https://medium.com/@hrishabh01sharma/git-and-github-a-laymans-guide-be27d4ba5907)  of the series, then take a look over it for better understanding.

In the Part-1, most of the jargons related to Git and Github and basic commands have already been discussed. Still, there is much more to learn like how to revert back the changes, what is branching, merging, etc.

<img src="https://media.giphy.com/media/3OqqNQtYNc52lI17PT/source.gif" alt="drawing" height="312" width="711">

Giphy GIFs

So hold your coffee and let’s begin & try to understand them one by one in simplest form and don’t worry we are not going to deal with any PPT, Lol!!

We have used the term master branch in the previous article several times.  
So Let’s discuss it first..

## Branching :

We will try to relate this with a real-life scenario at first and then we will move on to the technical explanation.  
Imagine you are working on a team project. In such a project, there are often bugs to be fixed and sometimes a new feature has to be added. In a small project, it is easy to work directly on the main version, technically ‘master branch’ but in case of big projects, if you do so there is a high probability that you and other teammates may make changes which are conflicting. So the solution for this is ‘branching’ in git.

For proper understanding, you can think of the main git chain as a tree trunk which is technically called ‘master branch’.So whenever you want to work on a new feature, you can make a separate branch from the main tree trunk or master branch and start committing changes in your new branch and once you think that your feature is ready you can again merge that branch in the master branch.

Let’s understand this in a more robust way and also discuss the basic commands related to branching.

<!-- ![](https://miro.medium.com/max/60/1*fmTOvzFMX6H-M3Cloi6pVQ.png) -->
<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/a.png" alt="drawing" height="312" width="711">

Branch in git is a special pointer to one of the commit. Every time you make a commit, it moves forward to the latest commit.

<!-- ![](https://miro.medium.com/max/60/1*sMGBn52UQhVwajwYE1kXuQ.png?q=20)
 -->
<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/b.png" alt="drawing" height="312" width="711">

After adding one more commit in the master branch

Another important point to mention is that git has a special pointer called  
**HEAD** to keep track of the branch you are currently working on.

Let’s create a new branch with the name ‘new-feature’.

> git branch new-feature

This will create a new branch(a pointer) on the same commit you were working on.

<!-- ![](https://miro.medium.com/max/60/1*92FeGS5svhwSa9y8p_8DzQ.png?q=20)-->

<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/c.png" alt="drawing" height="312" width="711">

After adding a new branch ‘new-feature’

Note that HEAD is still on the master branch. You need to checkout to switch to the new branch.

> git checkout new-feature

<!-- ![](https://miro.medium.com/max/60/1*iL3vrOWyhUQ_T3qu5DwP_A.png?q=20) -->
<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/c.png" alt="drawing" height="312" width="711">


NOTE-You can create new branch and immediately checkout to the new branch by:

> git checkout -b new-feature

Let’s start working on the new-feature and make a new commit.

<!-- ![](https://miro.medium.com/max/60/1*cBI9pZd4ZXh423a_Q42MTw.png?q=20)
 -->
<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/d.png" alt="drawing" height="312" width="711">

Now if we checkout to the main branch again and make a new commit,the new-feature branch will not be affected at all.Let’s do this:

git checkout master

After some changes,and commiting the new changes:

<!-- ![](https://miro.medium.com/max/60/1*7NPv0h7WTj-eIP03ee-aVQ.png?q=20)
 -->
<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/e.png" alt="drawing" height="312" width="711">

So , you can see how you can work on a new-feature without disturbing the master branch and once you complete your task on the new-feature you can “merge” that branch into the main branch.  
Isn’t it amazing that you and your team can work on different features by creating multiple branches and later merging them into master?Hell Yeah!!!

Now Let’s discuss little bit about merging and basic commands related to it.

# Merging :

Whenever you make a separate branch for working on a feature, you can commit your changes in that branch. But when you task related to the feature for which you make a branch completes, you need to merge that branch into the main codebase/master branch and this process is called ‘Merging’.

Suppose your task on new-feature branch is now complete and you want to merge that branch into the master branch.Then firstly checkout to the master branch.

> git checkout master

And use the following command:

> git merge branchname

*Here in our case branchname is new-feature.

This command merge the changes you made in new-feature branch with the master branch by squashing them into a new commit that has information related to the two parent commits.See the picture..

<!-- ![](https://miro.medium.com/max/60/1*wHuXhRXPFFAvasWtGEjuyw.png?q=20)
 -->
<img src="https://www.cevgroup.org/wp-content/uploads/2019/05/f.png" alt="drawing" height="312" width="711">

Merging new-feature branch with master branch

And here comes the bad part….

<!-- ![](https://miro.medium.com/max/60/1*D4__S_vTcRm341pRLv6Afg.jpeg?q=20)
 -->
<img src="http://www.cevgroup.org/wp-content/uploads/2019/05/download-2.jpeg" alt="drawing" height="312" width="711">
pando.com

## Merge Conflicts :

When you merge a branch with the master branch, then there are chances you run into  
‘Merge -conflicts’.  
Basically,‘merge-conflicts’ arise when you changed the line of code that someone  
else also changed.

In such a situation, you manually have to decide which version of the code you want to keep that is you need to resolve the merge conflicts.

That’s All!!! Thanks for reading the article.  
The next blog in the series will focus more on using GitHub.  
Stay Tuned.

Happy Learning :)

References:  [https://git-scm.com/](https://git-scm.com/)

-   [Git](https://medium.com/tag/git)
-   [Github](https://medium.com/tag/github)
-   [Vcs](https://medium.com/tag/vc)
