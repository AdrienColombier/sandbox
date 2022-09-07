# WITCO CLI

#### 1. How to install
##### 2. How to use

## 1. Installer:

To install the `witco cli` on your machine, you have to clone the dev-toolbox repository using (with ssh): `git clone git@github.com:MonBuilding-Co/dev-toolbox.git`

Then go to the witco_cli folder in the repository and run the install script: `cd dev-toolbox && ./install`

This is just gonna copy the witco bash script into your binary folder:
- Ubuntu: `/bin`
- Mac: `/usr/local/bin`

To check if the witco CLI is install you can run the following command: `witco --version`

## 2. Commands:

| COMMAND | ARGUMENTS | OPTIONS | DESCRIPTION | EXAMPLE |
|:-------:|:---------:|:-------:|:-----------:|:-------:|
| --help | NONE | NONE | Display the available commands | `witco --help` |
| --version | NONE | NONE | Display your witco cli version | `witco --version` |
| create-fix-branch | Branch number, branch description | NONE | Create a branch starting with `fix/` and containing the Jira ticket number and a name, the branch created is set as your current local branch | `witco create-fix-branch 12787 Incorrect_scroll_behavior_in_policy_settings` |
| create-feat-branch | Branch number, branch description | NONE | Create a branch starting with `featx/` and containing the Jira ticket number and a name, the branch created is set as your current local branch | `witco create-feat-branch 12787 Incorrect_scroll_behavior_in_policy_settings` |
| delete-branches | Jira ticket number | NONE | Delete all the local branches matching with the given Jira ticket number | `witco delete-branches 12787` |
| create-pr | NONE | `-b` (branch) branch to rebase / `-r` (reviewer) assign a reviewer | Create a pull request on github | `witco create-pr` / `witco create-pr -b env/groot` / `witco create-pr -r Ayoub -b env/cyberpunk` |
| update-work-on-branch | Module name, commit message | NONE | Add all local changes, commit with the given module name and commit message then push all the diff to the remote branch | `witco update-work-on-branch MyOrganization 'Fixing background color using css var'` |
| go-to-dev | NONE | NONE | Change your current local branch to develop and update the submodules | `witco go-to-dev` |
| go-to-last-branch | NONE | NONE | Change your current local branch to your previous one and update the submodules | `witco go-to-last-branch` |
| change-to-branch | Jira ticket number | NONE | Change your current local branch to the first matching with the given Jira ticket number | `witco change-to-branch 12787` |