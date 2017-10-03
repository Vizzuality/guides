Task Management
===========

At Vizzuality we use different task management systems across our projects.
In this guide you can find information about the purpose of each of the standard
way to use them, as well as some tips to keep on top of your tasks.

Bottom line the key to success of task managing is to make sure that you setup
your tools to inform you about your tasks the best way possible, be it via email,
Slack or messages inside bottles. Knowing the tool that is being used in each
project it is then each others' responsibility to not miss messages, comments
and not forget to reply to anyone.


Tools
-----

- [Basecamp](https://github.com/Vizzuality/guides/tree/master/task-management#basecamp)
  - [Tips and best practices](#tips-and-best-practices)
- [Pivotal Tracker](https://github.com/Vizzuality/guides/tree/master/task-management#pivotal-tracker)
  - [Pivotal Tracker stages in real life](#pivotal-tracker-stages-in-real-life)
  - [Planning sprints](#planning-sprints)
  - [Tips and best practices](#tips-and-best-practices-1)
  - [Epics, stories, backlog, icebox, and points](#epics-stories-backlog-icebox-and-points)


Basecamp
--------

We use it to communicate with our clients' teams. In Basecamp is where most of
our conceptual discussions take place and where high level tasks are maintained.

### Tips and Best practices

- When using basecamp you can tweak the list of who will receive email
notifications for your messages, it's a good practice to pick the correct list of
recipients so that people aren't flooded by all messages.
- When ToDo lists are being used in a Basecamp project it's important to use the
assignment functionality. This should be set to the person you're expecting an
answer from, so that conversations don't get lost without response.
- It is **your responsibility** to keep an eye on tasks assigned to you and to answer
to discussions when you are mentioned on them. So make sure to tweak Basecamp's
settings so that they suit your way of working. If you like emails, get emails,
if you don't, visit the website.
- If you are assigned to new tasks or brought in to some discussion but you are
busy with other more urgent tasks, it is a good practice to acknowledge the
assignment or message anyway, so that no one is left hanging. [e.g.: Thanks for
your message, I'm currently in the middle of something, but will look back at
this as soon as I can].
- If you feel that a task or message is better suited to be dealt with by
someone else make sure to assign them or let them know, as they might not have
been notified.


Pivotal Tracker
---------------

Our default tool to manage internal tasks for each of our projects.
The UI and functionality might be overwhelming, but if we all use it the
same way then confusion should go down and usefulness should go up.

One key thing to keep in mind is that this is an internal tool, we are the ones
driving it and so it's our responsibility to ensure that it is useful for us.

### Pivotal Tracker stages in real life

|STATE  |REQUIREMENTS FOR ENTERING STATE|REAL LIFE ACTIONS|
|------ |-------------------------------|------------------|
|STARTED|The task has been assigned to you or you have picked it from top of priority list and you are now available to start working on it. You understand what needs to be done and you have all the data / assets / copy required to complete the task.|You created a new branch.|
|FINISHED|You have completed the task and it is now ready for review, which means you have written the code, tested the code, written automated tests, seen the automated test build pass, run a codestyle check and fixed any violations before passing it on to a reviewer.|You have created a pull request, written a description of what this is for and how to test this, waited for any automated build tools to pass and assigned 2 reviewers (please refer to [code review guide](https://github.com/Vizzuality/guides/tree/master/code-review)). Please ensure the PR contains the minimum set of changes needed to satisfy the requirements of the PT task, keep it small.|
|DELIVERED|The reviewer has checked the code for smells, inconsistencies, violations of project-wide conventions as well as tested the code. Testing the code is not required in case of a reviewer who is not on the project team.|The reviewer approved the pull request (please refer to [code review guide](https://github.com/Vizzuality/guides/tree/master/code-review)).|
||Code is merged into the integration branch.|2 scenarios for this:|
|||1. as the code author you merge the code. It is your responsibility to resolve any conflicts, wait for automated builds to pass on the integration branch & resolve any unexpected issues.|
|||2. the reviewer merges the code. This is a quicker flow which does not require a round-trip to the author, and is probably more appropriate for small changes on non-conflicted branches with small potential for regressions.|
||Task is ready to test in a non-local environment. Most typically this will be a staging environment.|An automated deploy hook is recommended for deploys from integration branch (develop -> staging). If the automated deploy is not enabled, whoever merged the code should deploy it and verify it is actually ready for testing on the dedicated environment.|
|ACCEPTED|Task has been verified to work in the testing environment and meet acceptance criteria. Acceptance can be done on the Retrospective/Planning meeting or when the Project Manager reviews the status of Pivotal Tracker|Once all tasks in a release have been accepted, changes from the integration branch can be merged into the production branch. It helps to keep releases small. Here's a useful [branching workflow](http://nvie.com/posts/a-successful-git-branching-model/).|

For designers, data folks and others the `Pull Request` might not be the delivery
system, but Pivotal Tracker can still be used.

### Planning sprints

Best way to ensure that Pivotal Tracker is up to date is to ensure that everyone
is using it and that it reflects the state of the project.

It is recommended that each project team meets at least once a week to plan their
project sprints. Recommended agenda for such a meeting is:

1. Retrospective on previous sprint [if no specific meeting for it], goal is
to check where the project is and if there were any issues;
2. Discussion of priorities, the Project Manager should make sure to communicate
any priorities discussed with the client;
3. Identification of tasks to work on the new sprint;
4. Ensure that all tasks have been estimated;
5. Create a release on Pivotal Tracker with the date of the end of the sprint
and describe the goals of the sprint on the description.

After the planning meeting everyone should know what they are working on and
what are the goals for the sprint.


### Tips and Best practices

- Stories and epics have more than a title, you should make sure to read their
descriptions when picking up new tasks, to make sure you know as much as possible
when starting to work on something;
- You can click in your name or in `My Work` to get a list of the things that are
assigned to you;
- If you find something that needs doing and you can't find an associated story
on Pivotal Tracker, make sure to add it and to explain why it is needed the best
you can;
- Tags help organize work and can be useful to decide on what to work next, if
you're adding new stories make sure to tag them consistently;
- Sprint planning is a team job, everyone should be involved and participate
actively in it, that is the only way that an accurate list of tasks can be set
for a given sprint;
- Don't forget to update your stories when you finish some stage;
- When creating a Pull Request you can add a link to a Pivotal Tracker story
to make it easier for the reviewers to understand what they are reviewing;
- Most of our Pivotal Tracker projects are connected to a channel on Slack, if
you add your Pivotal Tracker handle to your notification list on Slack you will
never miss a relevant message;


### Epics, stories, backlog, icebox, and points

We all know that Pivotal Tracker is a bit complex, below is information on how
the key components could be used successfuly.

#### Epics

These are the highest level units on Pivotal Tracker. Epics work well to organize
smaller tasks in terms of a User Story (high level functionality that the application
should support) or a specific website page (when separation in pages makes sense).

The best way to make use of Epics is to add them at the start of a project and
then use them to tag specific stories. This will allow everyone in the project
to have a sense of what's left to do in regards to each user story.

The Epic's description can hold the full user story or a link to a document that
clearly describes the epic for further information.

#### Stories

Each story represents a feature on the application. Each story
should be clearly labelled with the epic that it's related with and any other
tags that make sense. Stories should also be estimated and if a story doesn't fit
in the points range being used, it should probably be split into smaller tasks.

For further clarity make sure to use the story description to add any detail
or advice that might be relevant. If there are clear sub-tasks on a story
you can also use them to better communicate what's happening with it.

#### Backlog

Usage varies but it seems to work well if we keep only the stories that we are
aiming to tackle in a given sprint, this way there's less clutter and
it's easier to check the pulse of an sprint.

#### Icebox

Here we keep the tasks that are not part of the current sprint but that should
be considered next. It's recommended that the icebox be filled as soon as there's
information about specific user stories, so that there's a pool of stories to work
from.

#### Points

It's recommended to use points as number of hours. A custom range can be set, and
at team Rosling we have been using `0,1,2,3,4,6,8,10,12,14,16`. Points should be
set by the team on each sprint planning or after any estimation effort, they
will help define each sprint.
