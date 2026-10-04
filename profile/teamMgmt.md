## Overview
Keeping track of progress, planning and managing deadlines, and documentation will be handled in 3 key areas.

- Projects handles the tracking of tasks, deadlines and sprint planning.
- A repository Wiki page will store technical documentation related to the architecture and execution of the game right in the repository for easy access.
- A GDD document will store information related to the actual design of the game, as well as meeting notes and playtest feedback.

Below is an index linking to different pages going more in-depth on setup and management of things such as milestones, sprints, and tasks. 

Below that is a section on project boards and setting them up. This will only need to be done when starting a new game/project, so likely only every 2-3 semesters.

## Index
 - [Sprint Management](./sprintMgmt.md)
 - [Task Management Pt.1: Issue Creation](./taskMgmt.md)
 - [Task Management Pt.2: Issue Updating](./taskMgmt2.md)

## Projects
Task management will be undertaken through GitHub [Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects). 

These are project boards, where teams will keep track of their current, planned and completed tasks by organizing them into separate columns. Board organization differs slightly team by team, but generally all teams have columns for a Project Backlog, a Sprint Backlog, In Progress Tasks, Tasks Under Review, Completed Tasks, and a Task Graveyard.
 -    Project Backlog: used for tracking all tasks to be completed at some point over the project. When a task is created, this is where it first goes.
 -    Sprint Backlog: Tasks to be completed over the current Sprint. Tasks are taken from the project backlog at the beginning of the Sprint and placed here.
 -    In Progress: Tasks that are currently being worked on by someone. 
 -    Under Review: Completed tasks that are awaiting a PR or review from a lead.
 -    Completed: Tasks that have been finished. THIS INCLUDES DOCUMENTATION! Please document your code before considering it complete.
 -    Blocked: Tasks that cannot be worked on due to reliance on other tasks or other external factors.
 -    Graveyard: Tasks that were created but for one reason or another the team decided were not necessary. Placed here for posterity's sake, in case there's ever a need to reference an abandoned task. 

It's important to regularly update the project board, not just for your team's sake but for the production team and other leads to be able to keep track of progress across teams. The producers and Erika should be able to open up the project board at any given time and have a comprehensive understanding of where the project is at and what every team member is working on at a given time.

### Project Board Creation

At the beginning of a new game project, it's appropriate to create a new project board to track tasks and development over the course of the project. To create a task board, navigate to the RIT echoes' projects page and click the big green button that says "New Project".

<img width="700" height="200" alt="Screenshot 2026-10-04 164647" src="https://github.com/user-attachments/assets/b4a65df5-f23e-486d-93e0-9790a37a5eb6" />

Afterwards, scroll down until you see the "Iterative Development" template, and select that.

<img width="700" height="300" alt="Screenshot 2026-10-04 165218" src="https://github.com/user-attachments/assets/e2d9886b-36cd-4d7f-8749-2dbc4f55cae9" />

Then, make sure to give the board a fitting name as well as making sure the box to "Import items from repository" is NOT CHECKED, as there should not be anything imported over from other boards/repos. Then, hit the green "Create Project" button.

<img width="600" height="400" alt="Screenshot 2026-10-04 165253" src="https://github.com/user-attachments/assets/2223df42-8b7e-4fc5-8c5a-d6935b154287" />

Once you're at the board, there's a little bit of cleanup you'll need to do. Mainly, renaming the "Ready" category to "Sprint Backlog" as well as adding a relevant description. After that, you'll want to add two new columns; one for the Blocked tasks and one for the Graveyard. You can find the spot for adding new columns all the way to the right with the `+` arrow button. Click that and select "new column".

<img width="700" height="300" alt="Screenshot 2026-10-04 165934" src="https://github.com/user-attachments/assets/c491485a-b1d0-46e2-b063-f0d1b2402be1" />

From there, you can start adding new tasks to the board! Issue creation will be continued in [Task Management Pt.1: Issue Creation](./taskMgmt.md).
