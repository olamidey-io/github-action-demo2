# Project 2
## Github ACtions Lab guide

### Step 1: Create a New GitHub Repository

* Go to GitHub and create a new repository.
* Clone the repository to your local machine:

![alt text](github-actions-lab/images/Capture9.PNG)

### Step 2: Create a Workflow Directory

* Create a directory for your GitHub Actions workflows: **mkdir -p .github/workflows**

![alt text](github-actions-lab/images/Capture10.PNG)

### Step 3: Create a Simple Workflow

* Create a new workflow file: touch .github/workflows/main.yml

![alt text](github-actions-lab/images/Capture11.PNG)

* Open main.yml in your favorite text editor and add the following content to define a simple workflow:

![alt text](github-actions-lab/images/Capture12.PNG)

* If i stage this workflow and push to remote repository just like that, i will get a build error under "actions" because package.json file is missing in my project directory. For **npm test** to work, GitHub expects that there is a package.json file in the root of your repo (where it is running the command). The package.json file tells Node.js what your app is about. So, if package.json is missing, then npm test has no idea what to run — and it fails!. Images shared below

![alt text](github-actions-lab/images/Capture13.PNG)

![alt text](github-actions-lab/images/Capture14.PNG)

* To fix this, go back to the directory where your project lives and run **npm init -y** to add the **package.json** file

![alt text](github-actions-lab/images/Capture15.PNG)

* Open the file and edit the script

![alt text](github-actions-lab/images/Capture16.PNG)

* Stage your changes and push to the remote repo

![alt text](github-actions-lab/images/Capture17.PNG)

* Go back to GitHub → Actions tab → Watch your CI/CD workflow run again, now successful.

![alt text](github-actions-lab/images/Capture18.PNG)


