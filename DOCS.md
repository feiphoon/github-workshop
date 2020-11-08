# An introduction to Github

This page will give you:

- [A quick overview](#a-quick-overview): The Github collaboration process
- [A step-by-step walkthrough](#a-step-by-step-walkthrough): Your how-to questions answered! (hopefully)

To give feedback about this page, please see: ++++

If you have any questions about Github, any member of Tech will be happy to help.


## A quick overview

![Handdrawn Octocat](handdrawn-github-octocat.png)

Github is a platform that allows people to store and collaborate on a project.

Github works by allowing collaborators to keep a history of revisions. In Github,
a project is called a **repository**. For the purposes of this manual, all changes
or revisions in a repository are saved to what are called branches.

A **branch** is effectively a collection of changes. The "default" branch,
which is the version of the project that contains the all latest approved changes
and should match exactly what is in production (or live), is known as the **master**.

Because many people might be working on different tasks simultaneously,
**any new task to add changes to a repository must first start with the
creation of a new branch other than the master branch**. This is so that
reviews and amendments can be managed in an organised way before your work can
be added to the master.

----
#### :+1: Do this:
![A network diagram from Seedy](seedy_network_diagram.png)

#### :-1: Don't do this:
![Don't commit directly to master!](dont_commit_to_master.png)

There is a :doughnut::doughnut::doughnut: penalty for saving directly to master. It will be used to fuel the developer who needs to undo the change.

----

If someone else has already started on the task before you, it is likely that
they will already have made a branch. You can select the branch and carry on
working on the task.

When you save a change in a branch, it is called a **commit**. You (and your
team) can make any number of commits in a branch.

----
| :bulb: Using a branch to group your commits will allow you to:                        |
|---------------------------------------------------------------------------------------|
| - make changes without affecting other people's work                                  |
| - collaborate on your task with others                                                |
| - organise a neat review of your work                                                 |
| - avoid accidentally adding invalid or incomplete work to the live/production version |
----

You can have multiple branches at the same time.

When you have finished working on your branch, you will want to make your work
available for review. To do this, you want to first open a pull request on your
branch.

A **pull request** is a request to submit your contributions to the latest,
approved version of the repository. This also means that a pull request is a
request to **merge** your branch into the master branch.

After a pull request has been opened, it is perfectly fine to continue making
changes to your branch. These changes will automatically be included in the pull
request.

----
| :bulb: Opening a pull request will allow you to:                          |
|---------------------------------------------------------------------------|
| - see how your work will impact the repository                            |
| - open discussions and continue collaborating on your task with others    |
| - tag other people to review and sign off your work                       |
| - establish when your work is ready to add to the live/production version |
----

You can have multiple open pull requests at the same time.

Your next goal will be to **merge your pull request**.

To get your pull request into a ready-to-merge state, it needs to have:
- received sign-offs from your team. This means others have checked your work
  and are satisfied.
- passed all automated tests, eg. on Seedy we have Code Climate and Semaphore.
  When they have passed, you will see a green tick next to it. In the event that
  you see a red cross, it means that a test has failed and you should ask Tech
  for help.
- no warning messages about a **merge conflict**. In the event that you see this,
  please ask Tech for help.

Depending on which repository you are working on, you may or may not able to
merge without Tech assistance. For example, some pull requests on Seedy are
self-serviced, so a non-Tech user can simply merge it themselves and the new
changes will be automatically deployed to the live site. If you are unsure,
always ask Tech.

----

Congratulations! You now know how to use Github to collaborate and make a
contribution to a repository.

Here are some examples of Github being used to store and manage a non-code project:

- Someone's TiL (Today I Learned) diary of new knowledge: https://github.com/jbranchaud/til
- A crowdsourced travel itinerary: https://github.com/dylanegan/travel
- A novel: https://github.com/gregorygershwin/Benjamin-Buckingham-And-The-Nightmares-Nightmare-Novel
- A place to store cat images from the game Neko Atsume: https://github.com/meteormanaged/neko-atsume-slack-emojis

----


## A step-by-step walkthrough

This walkthrough is for Github's web interface. For Github Desktop instructions,
please refer to this manual: https://help.github.com/desktop/guides/contributing/

:zap: **Look out for this icon for nice keyboard shortcut tips. The Github web
interface supports these anywhere on their site, and you can access the shortcut
help by hitting the `?` key.**


### Topics

1. [Find your repository](#1-find-your-repository)
2. [Check your current branch](#2-check-your-current-branch)
3. [Create a new branch](#3-create-a-new-branch)
4. [Find an existing branch](#4-find-an-existing-branch)
5. [Find files and navigation](#5-find-files-and-navigation)
6. [Edit a file](#6-edit-a-file)
7. [Save a change](#7-save-a-change)
8. [Create a pull request](#8-create-a-pull-request)
9. [Review a pull request](#9-review-a-pull-request)
10. [Merge a pull request](#10-merge-a-pull-request)


#### 1. Find your repository

All our repositories are accessible at https://github.com/simplybusiness/. You
will see the ones you have permission to access. If you can't find what you are
looking for, ask a Tech team member for help.


#### 2. Check your current branch

Once you are on the repository index page, you can check what branch you are
currently on from the `branch` dropdown button at the top left. This button
persists in the same position wherever you are in the repository. Remember
that it may default to master, so always check it!

![Checking your current branch](https://guides.github.com/activities/contributing-to-open-source/docs-folder.png)


#### 3. Create a new branch

Click on the `branch` dropdown button, and a little box appears below it.

Type the name of your new branch (give it a sensible name that describes your task,
and use either hyphens or underscores in place of spaces) into the text field
and hit the `Enter` key. If a branch by that name does not exist, it will
create it for you and automatically switch you to it. If it already exists,
it will just switch you to it.

![Create a new branch](https://guides.github.com/activities/hello-world/readme-edits.gif)

:zap: **You can also hit the `w` key to open this box.**

----
##### :bulb: Still not sure if you need a new branch? Some examples:

- If I was just adding a single new page I would create a new branch called
`my-new-page-name`
- If I was adding a whole collection of pages I may do them all in a single
branch: `seo-builder-pages`
- Even small changes such as spelling corrections should be done this way:
`spelling-landlord-insurance` or `correct-sidebar-links`

----


#### 4. Find an existing branch

See [Create a new branch](#3-create-a-new-branch), or click on the `branches` tab
just above the `branch` dropdown button for a full list of branches in progress.

![Full list of branches](https://help.github.com/assets/images/help/branches/branches-link.png)


#### 5. Find files and navigation

Click on folders in the file browser you see to get to the files you want to
edit.

:zap: **You can also hit the `t` key to open Github's file finder. Start typing
your file name and it will suggest possible results. This is useful if you don't
remember where the file is located. You can do this from wherever you are in the
repository.**

![File finder](https://cloud.githubusercontent.com/assets/2567/6140360/82221784-b14b-11e4-9cba-318ad98ce5d1.png)

#### 6. Edit a file

First, check that you're on the right branch.

Click the Pencil icon on the top right corner of the file you want to edit:

![Click the edit button](https://help.github.com/assets/images/help/repository/edit-file-edit-button.png)

Make your changes to the file in the Edit pane:

![Make changes in the edit pane](https://help.github.com/assets/images/help/repository/edit-readme-light.png)

You can also preview your changes in the Preview pane:
![Preview changes in the preview pane](https://help.github.com/assets/images/help/repository/edit-readme-preview-changes.png)


#### 7. Save a change

Otherwise known as making a commit. When you are done editing the file, look at the pane at the bottom of the file.
This is where you provide information about your changes.

![Commit a change](https://guides.github.com/activities/hello-world/commit.png)

----
| :bulb: Make your commit awesome by:                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| - having a short, descriptive title. The title of your commit will automatically default to something like `Update file.txt`, but to help others understand your changes better, replace this with something like`Amend broken link to /insurance/ page`. |
| - use the optional description text area to say more about the commit if needed. |
| - checking that you are on the right branch - where it says `Commit directly to the [your-branch-name] branch`. |

----
Hit `Commit changes` to save.


#### 8. Create a pull request

Go to the front/index page of your repository, eg. `http://github.com/simplybusiness/your-repository`

If you recently committed some changes you will see a notification mentioning
your branch, with a big green `Compare & pull request` button:

![Compare & pull request](compare_and_pull_request.png)

Alternatively, you can switch to your branch and you will see a big green
`New pull request button`:

![New pull request](new_pull_request.png)

A third option is to click on the `branches` tab at the top, find your branch in
the list, and hit the `New pull request` button next to it.

![New pull request from branches list](new_pull_request2.png)

Clicking the button will bring you to another page where you can fill in the
details of your pull request.

![Open a pull request](https://help.github.com/assets/images/help/pull_requests/pullrequest-send.png)

----
| :bulb: Make your pull request awesome by having:                                                                    |
|---------------------------------------------------------------------------------------------------------------------|
| - a useful title                                                                                                    |
| - tags in the description for people who need to review -  (type `@personsname`)                                    |
| - a link to the related Trello card if there is one                                                                 |
| - a link to preview your work. Your branch will be reachable at: http://peep-show.aws:8080/?branch=your-branch-name |
----

Hit `Create pull request`.


#### 9. Review a pull request

You can view the list of commits by clicking on the Commits tab at the top.

:zap: **Hit the `c` key to open the list of commits in the pull request.**

You can view the files changed by clicking on the Files Changed tab at the top.

:zap: **Hit the `t` key to open the list of files changed in the pull request.**

You can also discuss the pull request, either by commenting in the Conversation
pane, or by going to the Files Changed pane and clicking the exact line you want
to talk about.

If you are signing off a pull request, there is no official format. The
etiquette is to comment with `Signed off by @your-name`. If there is a sign-off
checklist in the description containing your name, check the box next to your name.


#### 10. Merge a pull request

This part varies depending on the repository you are working on.

If there is a process and agreement in place for self-service pull requests
(ie. a pull request where the user does not require Tech assistance) such as in
Seedy, you can hit the `Merge pull request` button yourself. If you are unsure,
best to ask.

Otherwise, you will need to ask a Tech team member for assistance.

There is a :doughnut::doughnut::doughnut: penalty for merging a pull request
prematurely or on a non-self-service pull request. It will be used to fuel the
developer who needs to undo the change.