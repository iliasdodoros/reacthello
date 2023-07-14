# GitHub Guidelines
## Teams 

We can create as many teams as we want. Each member of one team has the ;ermissions that we set for the whole team. One of the teams should be for those that should have admin access to the repository




## Branches

- The main branch contains the last stable version of the code and this is the version that is deployed. The main branch should be protected.
Setting -> Branches -> Add rule -> Branch name : main and make sure to check require a pull request before merging (check whichever is suited for the current project) and Do not allow bypassing the above settings

- For every update that we want to develop we create a new branch with a appropriate name

We can also create an issue or choose an existing one and then [create a branch to work for this issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-a-branch-for-an-issue "create a branch to work for this issue").

### Pull Requests

Whenever we want to change something in the main branch (for example fixing a bug) the only way we can do this is with a pull request (simply pushing to main is disabled).
Each pull request should be approved by designated users (senior developers) and to be able to merge all the chosen test must be passed. Also a to reduce conflicts each branch should be up to date with main before the pull request.

## Issues

Issues should be created for every change that we want to do to the code. Each issue should have a title that is easy to understand and an appropriate label. Like mentioned above we can also create a new branch that is assosiated with an issue to work on the issue and when it is resolved we can create a pull request to the main branch.           


## Secrets 
before explaining the pipeline we have to explain GitHub Secrets.Secrets are a safe way to store sensitive information that we can use in the pipeline. For example : passwords, tokens, RSA keys ,....
We can set secrets by going to Settings -> Secrets and Variables -> Actions -> New repository secret. We have to be careful what secrets we add and to make sure we have a buck up because once we set them we can not view them again.
Our pipeline looks like this 

# Pipeline 
### BUILD -> TEST -> PACKAGE -> DEPLOY 

The pipeline is implemented with GitHub Actions. We use tvo actions, one for the main branch which is the whole pipeline and one for all the other branches. Actions often need access to sensitive information, like passwords, and we store them with secrets so that we can easily access them in an Action with `secrets.<SECRET_NAME>`

The GitHub Action that implements the above pipeline is shown below while the one for all the other branches is just the build and test steps :

```YAML
name: Deploy Main Branch
on:
  push: 
    branches: main
jobs:
 build:
    name: Build
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2
      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: 20
      - name: Install Dependencies
        run: npm ci
      - name: Build Application
        run: npm run build
 test:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Repository
        uses: actions/checkout@v2
      - name: Set up Node.js
        uses: actions/setup-node@v2
        with:
          node-version: 20
      - name: Install Dependencies
        run: npm ci
      - name: Run Tests
        run: npm test
```
