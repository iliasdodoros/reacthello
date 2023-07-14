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

You can find an dditional information one the differences of these roles [here](https://docs.github.com/en/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization).

### Teams 
After an Organization is created you can invite people ot your organization by going to your Organization Home Page -> People -> Invite member and searching by their GitHub username. Once you choose one you can send the invitation and an email will be sent to them. 

Once you have invited everyone that you want to be part of you organization you can start creating Teams to divide people in groups depending on their role in a project. To create a team you can go to your Organization Home Page -> Teams -> New team and then choose the details for each Team. Once you create a Team you can go to your Teams page form your Organization Home Page and select the Team and Add a member you want to be part of the team. 

### Repositories
After you have create all the teams you need and added all the members you can start Creating new repositories by going to your Organization Home Page -> Repositories -> New Repository and filling out the details for the new repository. When you create a new repository you can find it in the Repositories page adn by selecting you can all the information about it. 

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
You can download the correct version for your computer of Git from [here](https://git-scm.com/downloads) and then run the installation Wizard that you downloaded. Follow the steps in the Installation Wizard without changing anything (unless you know for sure what you are doing) and then press Install.

### TortoiseGit
You can download the correct version for your computer of TortoiseGit from [here](https://tortoisegit.org/download/) and then run the installation Wizard that you downloaded. Follow the steps in the Installation Wizard without changing anything (unless you know for sure what you are doing) and then press Install.

### Visual Studio Code





































