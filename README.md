# GitHub Tutorial

As you have done with the previous extended project, you will be using Scala and Play. This time we'll be using the GitHub API to make your own version of GitHub!

The GitHub API is documented here: https://docs.github.com/en/rest?apiVersion=2022-11-28
Spend some time getting familiar with it prior to starting. 

You should clone this repo (ssh link: git@github.com:AprilGar/ExtendedProject2Template.git).
We want to track changes to the project using git. Since we cloned this repo we are going to change the remote origin.

* Go to your GitHub account → Your repositories → Create new repository
    * Give it the same name as your local project
    * Ensure it is public
    * Ensure 'Initialise with README' is unticked
* Go to the command line/terminal:
    * We need to tell git where the remote GitHub repository is, so that we can push up changes. Run the following, substituting with your GitHub username and newly created project name
    * `git remote rename origin upstream` (The old origin is now renamed to upstream)
    * `git remote add origin git@github.com:<username>/<repo-name>.git` (A new origin is added, your github!)
    * e.g. `git remote add origin git@github.com:MercatorDigital/gitHubExProject2.git`

* Run `git remote -v` to check the remote is correct

* Run `git status`, and you can now see there are various files git has picked up but is not yet tracking any changes and only recognises a bunch of new folders and files.

* Run `git add .` to add all files in red to a 'staging area' in preparation for a final commit

* To make a commit, run `git commit -m "example message"` (Think of an appropriate message for the changes you've made)

* Push your new commit up to main `git push origin main` (Note: there are two places we 'can' push to, the old location, upstream, and your new one, origin. Ensure you commit to "origin main"!)

* Go to your new project on GitHub to check everything pushed up okay.

* In terminal type `sbt run`, in your browser on localhost:9000 you should see a page with the title "Welcome to your version of GitHub".

When writing your code only have working code on your main branch and for each new task create a branch to create this.

This is great practice as if we push directly to main we could potentially be breaking the code or cause merge conflicts.
We can make commits in an isolated branch that will not affect the code in main which should only ever be working code.

When the task is completed, you have written the corresponding tests, and they are passing create a pull request to merge your branch into main.

Make sure you are practicing test driven development by writing integration and unit tests for all your methods after you have written them.

There is less information in these instructions, you might need to do a bit of research and ask questions but this is great practice as a large part of the job as a developer is research.
