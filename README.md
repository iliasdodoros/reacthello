# GitHub Guidelines

## Branches

- The main branch contains the last stable version of the code and this is the version that is deployed.
- For every update that we want to develop we create a new branch with a appropriate name

We can also create an issue or choose an existing one and then [create a branch to work for this issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-a-branch-for-an-issue "create a branch to work for this issue").

### Pull Requests

Whenever we want to change something in the main branch (for example fixing a bug) the only way we can do this is with a pull request (simply pushing to main is disabled).
Each pull request should be approved by designated users (senior developers) and to be able to merge all the chosen test must be passed. Also a to reduce conflicts each branch should be up to date with main before the pull request.

## Issues

Issues should be created for every change that we want to do to the code. Each issue should have a title that is easy to understand and an appropriate label. Like mentioned above we can also create a new branch that is assosiated with an issue to work on the issue and when it is resolved we can create a pull request to the main branch.           

# Pipeline (Actions)
Our pipeline looks like this 

### BUILD -> TEST -> PACKAGE -> DEPLOY 

The pipeline is implemented with GitHub Actions. We use tvo actions, one for the main branch which is the whole pipeline and one for all the other branches.

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
 package:
   name: Package
   runs-on: ubuntu-latest
   steps:
     - name: Docker Login
       uses: docker/login-action@v1.8.0
       with:
         username: ${{secrets.DOCKERHUB_USERNAME}}
         password: ${{secrets.DOCKERHUB_TOKEN}}
         logout: true
     - name: Build Server image
       run: docker build -t iliasdodoros/reacthello .
     - name: Push to dockerhub
       run: docker push iliasdodoros/reacthello
```

