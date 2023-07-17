# Quick setup

### Admins
1. [Create GitHub account](https://github.com/iliasdodoros/reacthello#github-account)
2. [Create Organization](https://github.com/iliasdodoros/reacthello#creating-an-organization-administrators-only)
3. [Invite members to Organization](https://github.com/iliasdodoros/reacthello#teams)
4. [Create Teams](https://github.com/iliasdodoros/reacthello#teams)
5. [Create repositories](https://github.com/iliasdodoros/reacthello#repositories)
6. [Add Branch protection Rules]()
7. [Add Teams to Repositories](https://github.com/iliasdodoros/reacthello#repositories)
8. [Create Projects](https://github.com/iliasdodoros/reacthello#projects)
9. [Create pipeline]()
    - Build
    - Test
    - Package
    - Deploy

### Members
1. [Create Github account](https://github.com/iliasdodoros/reacthello#github-account)
2. [Accept invitation to Organization](https://github.com/iliasdodoros/reacthello#teams)
3. [Download the necessary software](https://github.com/iliasdodoros/reacthello#software-installation)
4. [Read the guidelines](https://github.com/iliasdodoros/reacthello#pipeline)

# Getting started 
This repository is a guideline for creating repositories to use in projects and this is a guide on how to create it and use it. This quide explains step-by-step creating an GitHub account,creating an organization to group many projects together, downloading and installing the necessary software for each member and finally creating a CI/CD pipeline to use when creating a new piece of software and deploying it on a server. 

## GitHub Account
Each member of the project must have a GitHub account you can create one [here](https://github.com/) by entering your information and your preferences.The next step is to create an Organiztion in GitHub to organize your projects and you members in teams for easier control (this is for administrators). 

### Creating an Organization (Administrators only)
To create an Organization you can Sign In on your GitHub account and then going into Settings -> Organizations -> New Organization. In the new page that opens you can choose your plan. The Free plan has almost all the functionality we will use in this case except you cannot use Code Owners (more on that later). Once you choose your plan then you have to choose a name for you Organization and who owns this Organization and then your Organization is Created. The person that created the organization is the Organization Owner. Generally inside a GitHub Organization everyone has one role from the following   
- Owner
- Member
- Moderator
- Billing Manager
- Security Manager (Beta)
- Outside Collaborator
- GitHub App Manager

You can find additional information one the differences of these roles [here](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization).

### Teams 
After an Organization is created you can invite people ot your organization by going to your Organization Home Page -> People -> Invite member and searching by their GitHub username. Once you choose one you can send the invitation and an email will be sent to them. 

Once you have invited everyone that you want to be part of you organization you can start creating Teams to divide people in groups depending on their role in a project. To create a team you can go to your Organization Home Page -> Teams -> New team and then choose the details for each Team. Once you create a Team you can go to your Teams page form your Organization Home Page and select the Team and Add a member you want to be part of the team. 

### Repositories
After you have create all the teams you need and added all the members you can start Creating new repositories by going to your Organization Home Page -> Repositories -> New Repository and filling out the details for the new repository. When you create a new repository you can find it in the Repositories page and by selecting you can see all the information about it. 

To select a team to work a repository you can go to the Teams Page and select a team. Then on the team's page you can go to Repositories and add a repository from those you have created. Additionally you can change the permissionsthat each team's members have on a repository by going to the team's Repository Pgae and choosing from the drop-down list one of the following: 
- **Read**: Recommended for non-code contributors who want to view or discuss your project
- **Triage**: Recommended for contributors who need to proactively manage issues, discussions, and pull requests without write access
- **Write**: Recommended for contributors who actively push to your project
- **Maintain**: Recommended for project managers who need to manage the repository without access to sensitive or destructive actions
- **Admin**: Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repositor

### Projects 
GitHub has a feature called Projects which is a way to manage tasks and has a direct connection with the repositories Issues. You can create a new Project by going to the Organization Home Page -> Porjects -> New Project and selecting the view you want the project to have. After creating a Project you can go to the projects Page select a project and then go to the settings from the three-dot man on the top right where you can manage who has access to this project and who can view it. 

## Software Installation
Once you have a GitHub account the next step is preping your computer. You will need two applications Git and TortoiseGit.

### Git
You can download the correct version for your computer of Git from [here](https://git-scm.com/downloads) and then run the installation Wizard you downloaded. Follow the steps in the Installation Wizard without changing anything (unless you know for sure what you are doing) and then press Install. You can use Git from the command line or by opening Git Bash but this is not necessary because everyone can use the application TortoiseGit that we will install below which is essentially a plugin for the Windows File Explorer. 

### Visual Studio Code
The developers of the project can download Visual Studio Code which has a very good integration with Git and is very easy to use with many extensions. If you dont want to use Visual Studio Code and the IDE of your choice does not have an integration with Git you can download TortoiseGit by following the guide below. You can download the correct version for your computer of Visual Studio Code from [here](https://tortoisegit.org/download/) and then run the installation Wizard you downloaded. Follow the steps in the Installation Wizard without changing anything (unless you know for sure what you are doing) and then press Install.

### TortoiseGit
If you don't want to use git or Visual Studio Code to make changes to the project, for example if you are not a developer, you can use TortoiseGit which is a plugin for Windows File Explorer and is really easy to install and use. You can download the correct version for your computer of TortoiseGit from [here](https://tortoisegit.org/download/) and then run the installation Wizard you downloaded. Follow the steps in the Installation Wizard without changing anything (unless you know for sure what you are doing) and then press Install. Once installed in File Explorer when you right click another optoin should appear called TortoiseGit and you can choose to clone a repository from GitHub by copying the URL of the repository and pasting in the dialog. Additionally you can check the box that says Branch and write the name of the branch that you want to download (in the Pipeline section of this guide you can see what branches are and how you can use them). Once you do that all the files from that branch will be downloaded and will appear in the folder.  

## Pipeline 
The pipeline is the procedure we follow to create new projects and change existing ones. The pipeline we use is made of four steps : Build -> Test -> Package -> Deploy.

### Build 


































