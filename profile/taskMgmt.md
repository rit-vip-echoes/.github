# Overview
Keeping track of progress, planning and managing deadlines, and documentation will be handled in 3 key areas.

- Projects handles the tracking of tasks, deadlines and sprint planning.
- A repository Wiki page will store technical documentation related to the architecture and execution of the game right in the repository for easy access.
- A GDD document will store information related to the actual design of the game, as well as meeting notes and playtest feedback.

High Level Timeline
    <br>`Sprint Plan adds feature` -> `Issue for feature added to taskboard` -> `Work on the feature` -> `Finished and tested feature` -> `Documentation added to Wiki and GDD Doc` -> `Create Pull Request` -> `Approved Pull Request closes issue and merges feature`


# Sprint Planning
Before each sprint, teams will plan out a set of features and tasks related to a sprint goal, based on a project backlog. The backlog is an accumulation of higher level tasks that are known to be needed. These broader tasks inform the additions/refinements to the task board each sprint.

Features/tasks added to the current sprint should be detailed and actionable. If a task is not yet actionable, not enough information is known and instead a task to research should be used. 

# Projects
Task managment will be undertaken through Github [Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects). 

These are project boards, where teams will keep track of their current, planned and completed tasks by organizing them into separate columns. Board organization differs slightly team by team, but generally all teams have columns for a Project Backlog, a Sprint Backlog, In Progress Tasks, Tasks Under Review, Completed Tasks, and a Task Graveyard.
 -    Project Backlog: used for tracking all tasks to be completed at some point over the project. When a task is created, this is where it first goes.
 -    Sprint Backlog: Tasks to be completed over the current sprint. Tasks are taken from the project backlog at the beginning of the sprint and placed here.
 -    In Progress: Tasks that are currently being worked on by someone. 
 -    Under Review: Completed tasks that are awaiting a PR or review from a lead.
 -    Completed: Tasks that have been finished. THIS INCLUDES DOCUMENTATION! Please document your code before considering it complete.
 -    Graveyard: Tasks that were created but for one reason or another the team decided were not necessary. Placed here for posterity's sake, in case there's ever a need to reference an abandoned task. 

It's important to regularly update the project board, not just for your team's sake but for the production team and other leads to be able to keep track of progress across teams. The producers and Erika should be able to open up the project board at any given time and have a comprehensive understanding of where the project is at and what every team member is working on at a given time.

## Setup
### Milestones
Milestones are effectively what GitHub calls Sprints, and we'll utilize them as Sprints within echoes. Milestones are how we separate out a semester into iterative 'chunks', in which teams set development goals to achieve during a Sprint before working for roughly two weeks on developing and implementing their planned features before testing and receiving feedback through public and private playtests. At the end of a Sprint, teams meet up and reflect on the concluded sprint; what worked, what didn't work, what they should start doing and what they should stop doing. This reflection period is important; its where teams will reevaluate their approach to development and allow for course correction should they encounter issues or roadblocks. Afterwards, based on feedback from testing, the team sets new goals for the next Sprint and they repeat the entire process. 

Agile Sprints are a common production methodology practiced throughout the games industry; they allow for quick iteration and rapid prototyping. If you're an underclassman, you'll likely encounter Agile Sprints in the coming semesters, and if you're an upperclassman you've probably already encountered Agile Sprints and should be getting more comfortable with them.

Milestones will need to be setup to allow for the proper per sprint views of tasks. These are setup externally to the project inside of the repository.

1. In the repository, navigate to the `Issues` tab.
   
   <img width="2877" height="1565" alt="Screenshot 2026-09-14 130845" src="https://github.com/user-attachments/assets/7b27ed38-e6eb-4047-962b-cfffd8adffd5" />
   
3. Select `Milestones` in the bottom left.
4. Select the green `New milestone` box in the upper right hand corner.
  

5. Add information
  <img width="1378" height="635" alt="image" src="https://github.com/user-attachments/assets/14c91b52-50ab-4c19-81d7-81067ca58227" />
6. If desired, repeat for every planned sprint (7 in total).


   - [Semester Sprint Schedule (MyCourses)](https://mycourses.rit.edu/d2l/le/content/1167946/viewContent/11038364/View)
### Issue Creation

1. Type issue name the bottom dialogue box on the project board, then hit `enter`.
   
   <img width="1891" height="155" alt="image" src="https://github.com/user-attachments/assets/ca4f2129-780e-4b3a-b860-cb92915f4724" />
3. Select a type of [issue](https://github.com/rit-vip-echoes/.github/edit/main/profile/taskMgmt.md#issue-types)
4. Then fill out the needed information. Information needed varies depending on issue type.
5. Add additional organizational information to each task.

   - Assignee : Person(s) working on the task.
   - Label(optional) : Additional label to assist with high level task understanding (ie. `enhancement`)
   - Milestone: Select the Milestone this task should go under. `None` is ok if the task is not yet ready for a sprint. 

<img width="790" height="763" alt="Screenshot 2025-08-19 160710" src="https://github.com/user-attachments/assets/82460d20-1cb3-4f08-8918-a67fd636eabc" />

### Status Deletion
1. Navigate to your project.
2. In the top-right, click  to open the menu.

<img width="454" height="468" alt="Screenshot 2025-09-07 185343" src="https://github.com/user-attachments/assets/563f291b-89d9-4eca-9f00-d7713f374630" />

4. In the menu, click  Settings to access the project settings.
5. Navigate to the status section. 
6. Remove any uneeded statuses.

<img width="1792" height="761" alt="Screenshot 2025-09-07 185407" src="https://github.com/user-attachments/assets/23ee85a4-aa2b-40ab-bd6b-2d42d4593b09" />



## Views
### By Status
<img width="1915" height="924" alt="image" src="https://github.com/user-attachments/assets/4cf0e5ed-2a60-4fdb-ab7e-ea1b4c0ac461" />


### Roadmap
<img width="1911" height="891" alt="Screenshot 2025-08-19 154823" src="https://github.com/user-attachments/assets/bf2720c8-8813-4918-93d3-8ab6ffbb0a74" />

### Milestone Planning
<img width="1915" height="903" alt="Screenshot 2025-08-19 154834" src="https://github.com/user-attachments/assets/763ba8e3-9ae6-47f5-8575-2734b5d29973" />

### Not Done
<img width="1915" height="872" alt="image" src="https://github.com/user-attachments/assets/3bc7804f-6a80-487d-a829-185ce0563239" />


# Issue Types
Each issue type has its own template information to fill out. These are not always required pieces of information, use as much or as little as needed.

### Tasks
Tasks are general non-dev project tasks, and smaller dev tasks that don't qualify as a full feature. Examples would be minor art assets and system overhauls, as well as process documentation. 

### Features
A feature that needs to be added or modified for the project. Any kind of new player interaction would fall under this category; this includes UI systems, mechanics, controls, major art assets, etc. 

### Bugs
A bug, use this to track issues and how they are reproduced. These should be added to the project board in the meeting after any playtest, in order to make sure any bugs are not forgotten about and persist throughout the project far longer than they should.

It's very important that bugs, upon completion, receive extensive testing to make sure the bug was fully fixed and that no new bugs were created in the process. Ideally, when fixing a bug you do not create new bugs. However, if a bugfix is essential enough that its better to have a buggy fix to a bugfix, then you'll need to add the new bugs to the board as well. This should be a conversation with the team, not an individual decision to create more issues than you've solved. 

## Completing a Task
As echoes consists of students of a variety of years and disciplines, it’s important to have a mutual understanding of what is considered “done” for a task. For our purposes, a task must meet these criteria before it can be considered done and categorized as such.

1. The original task’s description has been fully completed/realized. 
2. Of presentable quality, no major bugs or oversights related to the task.
3. Progress on the task has been properly documented in all proper places (GitHub taskboard, GitHub wiki, GDD, etc). 
4. Reviewed and approved by other team members. 

