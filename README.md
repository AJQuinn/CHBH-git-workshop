# CHBH Git Contribution Workshop

This is the practical activity included in the CHBH Git session as part of the Code, Computing and Open Science sessions. We are going to learn how to contribute to an open github repository using a mix of github and git commands.

There are two ways to do this, by creating a local copy of the repository or by making changes directly on github. The first way is more complex but most likely the best for working with code that you want to run and test. The second is simpler but only really appropriate for smaller changes to text and documentation. Choose the path that best suits you and the work in hand.

## Contribute using a local copy of the repository

This is the most common workflow for making a contribution. You'll need to `fork` this repository to make a copy,  `clone` your new copy, make some changes and `push` these back to github. Finally, you can request that the repository owner merge your contribution by creating a `pull request`.

Let's go through that step-by-step

#### 1. Fork this repository to get a copy attached to your github profile. 

You can do this by clicking the `fork` button on the top right of the original repository. Once this is done, you should be able to see a copy of the repository attached to your profile - it will also include a reference link back to the original. Github keeps track of this link for you.

#### 2. Clone your fork of the repository from your github profile (not the original!)

You can run this on a terminal on your local computer. The code will look something like:

`git clone https://github.com/AJQuinn/CHBH-git-workshop.git`

Make sure that you clone your copy of the repo - not the original. It is possible to contribute directly to a repository without making a fork but it is likely that you won't have permission to do this.

#### 3.  Make some local changes to the files

You should now have a copy of these files on your local computer. Please add a fact to `facts.md` and a joke to `jokes.md`! These are [markdown files]( https://www.markdownguide.org/basic-syntax) so you can use some additional formatting in your contribution if you like.

Finally, add your github handle and name to `Contributors.md`.

#### 4. Add the changes to your local git.

You can see a summary of your changes using `git status` to show which files have changed and `git diff` to see the specific changes.

Next you, should next `stage` your changes ready to share. There are several ways to do this using the `git add` command - either add all files in one go
`git add -u`

or add specific files one at a time
`git add facts.md` 

If you run `git status` you should now see all the changed files listed under 'Changes to be committed'

#### 5. Commit the changes with a helpful message

You can fix your final set of changes by 'committing' them using `git commit`. This fixes a snapshot of the repository including all of the currently staged changes. Remember to include a helpful message saying what the changes are
`git commit -m "New facts and jokes from Andrew`

#### 6. Push the changes back to your github profile

Next you can share your changes. This involves `pushing` your current local copy of the repository back to the `remote`- in this case, the remote is your fork of the original repository on github.

Git should have kept track of the `remote` when you ran git clone, so you can simply run

`git push`

to upload the changes back to github. Have a look on github.com and you should be able to see the updates.

Note that this stage is where you might run into a `confict` error. This means that the code on your local machine and on the remote have diverged and git doesn't know how to resolve the difference. These conflicts are normally resolvable but can be tricky - I'd recommend that you find a local expert if you're running into these and don't know what to do... Best advice is to always make sure that you're using the latest version of the code before you start making changes and talk to other people who are using the repository so you aren't surprised by large changes. Worst case scenario - you can always reset your local repository to the most recent version and re-apply your local changes but this can be painful for big work.

#### 7. Create a 'Pull Request' on the original profile

Finally, we need to tell the original repository that we have some changes to share. We do this by creating a `pull request` on github. You can do this by clicking the 	`pull request` button above the list of files on github.com.

On the pull request page, sure the 'base' repository is the original and the 'head' repository is your fork. Finally, include a helpful summary of the changes in the pull-request message. 

Github.com provide more details on [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) in their documentation.

#### 8. Wait for your changes to be merged into the original repo! 

In a real example, it is possible that the original repository comes back with some changes or comments on your pull request before merging. This is a normal part of collaboration and hopefully results in some constructive improvements to the contribution. 

## Contribute directly on github

This workflow is less common than the first. It has the advantage of being quick and working directly in the browser but the disadvantage that you never actually get a working copy of the repository that you can test. As a result, this workflow is best suited to changes to documentation rather than code itself.

Let's go through that step-by-step

#### 1. Fork this repository to get a copy attached to your github profile. 

You can do this by clicking the `fork` button on the top right of the original repository. Once this is done, you should be able to see a copy of the repository attached to your profile - it will also include a reference link back to the original. Github keeps track of this link for you.

#### 2. Make some changes to the text files on your fork.

Open up the `facts.md` file in the github browser window. You can make changes directly in the browser by clicking on the `edit` icon (symbol of a pen) on the top-right above the file content. Make your changes directly on the page before adding a helpful summary message and committing the changes using the options at the bottom of the editor page. (note that you don't have to `add` changes when using this route, everything is committed directly).

Use this method to add a joke to `jokes.md`, a fact to `facts.md` and your name/github handle to `Contributors.md`.

#### 3. Create a 'Pull Request'

Finally, we need to tell the original repository that we have some changes to share. We do this by creating a `pull request` on github. You can do this by clicking the 	`pull request` button above the list of files on github.com.

On the pull request page, sure the 'base' repository is the original and the 'head' repository is your fork. Finally, include a helpful summary of the changes in the pull-request message. 

You can navigate back to the original repository on github and look at the `pull requests` tab to see what changes other people are proposing. This only shows open (unmerged) requests by default but you can toggle this to look at closed (merged) requests as well.

Github.com provide more details on [pull requests](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) in their documentation.

#### 4. Wait for your changes to be merged into the original repo! 

In a real example, it is possible that the original repository comes back with some changes or comments on your pull request before merging. This is a normal part of collaboration and hopefully results in some constructive improvements to the contribution. 


## Updates to these instructions

These instructions are likely not perfect... If you see any errors, typos or something that is just unclear then feel free to use either workflow above and propose a fix! This will make things easier for the next person.
