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
- It is *your responsibility* to keep an eye on tasks assigned to you and to answer
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

1. `Start`: You should start a task when you start working on it [this one is easy];
2. `Finish`: Once you're done with a task and have created a Pull Request you can
click on the finish button;
3. `Deliver`: Once your Pull Request has been merged the task can be delivered,
and ideally it will be deployed to the staging environment;
4. `Acceptance`: Acceptance can be done on the Retrospective/Planning meeting or
when the Project Manager reviews the status of Pivotal Tracker.


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
- Iteration planning is a team job, everyone should be involved and participate
actively in it, that is the only way that an accurate list of tasks can be set
for a given iteration;
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
aiming to tackle in a given iteration/sprint, this way there's less clutter and
it's easier to check the pulse of an iteration.

#### Icebox

Here we keep the tasks that are not part of the current iteration but that should
be considered next. It's recommended that the icebox be filled as soon as there's
information about specific user stories, so that there's a pool of stories to work
from.

#### Points

It's recommended to use points as number of hours. A custom range can be set, and
at team Rosling we have been using `0,1,2,3,4,6,8,10,12,14,16`. Points should be
set by the team on each iteration planning or after any estimation effort, they
will help define each iteration.
