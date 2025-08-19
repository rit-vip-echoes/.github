# Merge Conflicts
## How to Resolve
1. When in doubt about what to do, ask others for help. Merge conflicts can't hurt you. 
2. Merge coflicts are often the result of auto-generated files. If the files are not an important Unity or C# file (`.cs`, `.binary`, `.prefab` etc), you can often utilize the version from `origin` or `local` with little problem. Once again, ask for help if unsure.
4. If the merge conflict is contained within a code file and you wish to not overwrite entire files, files can be parsed line by line. Within almost any IDE or text editor such as [Visual Studio](https://code.visualstudio.com/), you can accept changes from one branch, combine, or accept neither.
5. If a scene has a merge conflict, duplicate the  conflicted scene before merging and accept the incoming scene change. Otherwise scene data could get permanently lost. 
### Resources
- [Github Desktop](https://www.youtube.com/watch?v=Q5AT8926fLI)
- [Visual Studio Code](https://code.visualstudio.com/docs/sourcecontrol/overview)
- [Visual Studio](https://learn.microsoft.com/en-us/visualstudio/version-control/git-resolve-conflicts?view=vs-2022)
- [Github](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github)
- [Command Line](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line)

## How to Prevent
- Follow best branch practices: [Branch Managment](./branches.md).
- Communicate well with the team, if everyone knows who is working on what, merge conflicts are less likely to occur.
- Consistently merge `dev` branch into  working branches, ensuring local work is up to date with the remote.
- Work in separate test scenes, only add to the main scenes of the game when a PR is created. This will protect scenes from being lost.
- Commit often, a bunch of smaller commits will lead to potentially less loss of work if a merge goes wrong. 
        
