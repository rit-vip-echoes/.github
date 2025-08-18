# Creating Branches
There are two ways to create branches:
- Through GitHub Desktop/other version control [HowTo](https://docs.github.com/en/desktop/making-changes-in-a-branch/managing-branches-in-github-desktop) 
- In GitHub [HowTo](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-and-deleting-branches-within-your-repository)

## Naming Conventions
Naming conventions don’t need to be the standard across all teams. It's important to maintain consistency within each team for naming conventions, so ensure a standard is created and met.
- `Feature-Feature_Name` for each new feature you are working on. 
- `BugFix-Bug_Name` for each new bugfix branch. 

# Branch Management
## Dev Branch Managment
- Each sprint, there will be multiple feature or bug-fix branches. 
  Once these are complete, (PR + Review) they will be merged into the `dev` branch. 
- Make sure to consistently merge `dev` into any active feature branches to avoid merge conflicts later on.
- `dev` will get merged into `main` generally once each sprint. 
## Main Branch Managment
- `main` should contain the most up to date stable build of the game.
- Do not merge or push directly to main.
- Main will be updated every sprint from the `dev` branch, if `dev` has no serious problems.
## Old Branches
Delete old branches when one of the right criteria are met (no deleting `main` or `dev`):
- Branch is a few weeks out of date with the `main` branch 
- Branch contains broken versions of the game and won't be revisited
