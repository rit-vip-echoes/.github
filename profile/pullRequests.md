# Pull Requests

## When to make them
Make a pull request when you’ve finished a feature to the point that it’s ready to be added to the game/shown off in a build demo. (It doesn’t necessarily have to be finished, just working well enough that it doesn’t break the game. Leads should be clear about when a pull request is needed vs. not!)

##  [How To Make Them](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
1. Build the game. Make sure you have a working WebGL build in the branches `docs` folder. [WebGL Instructions](https://docs.unity3d.com/2020.1/Documentation/Manual/webgl-building.html).
2. By default, all *echoes* repos use [pull_request_template.md](../.github/pull_request_template.md) as the pull request information template.
4. Ensure the pull request is merging from the feature branch into `dev`.
5. Document the pull request within the games project documents (not the pull request template)
6. The pull request itself should also have documentation of what the feature is and how to test it, along with a link to the additions within the project documentation. This can be brief overview tailored to testing if the feature works. It also should link to the proper spots in the project regarding more in-depth information.
7. Optionally link the pull requestion to its issues (#issueName). This is optional.
8. Request a review from the team lead and up to one other member.
   
10. Update the task board. Move the relevant tasks/issues to `under review` or similar column in the project board.
   
   

## Approval
- Approval standards should be set by each team, its reccomended that the lead and one other team member approve the pull request.
- If not approved, make sure to have detailed reasons why so the issues can be fixed.

## On Approval
- Once approved, someone should merge the branch into `dev`. Before doing so ensure it is up to date with `dev` to avoid potential merge conflicts.
- Make sure to update the taskboard, moving the task/issue to `done` if not already there. 





