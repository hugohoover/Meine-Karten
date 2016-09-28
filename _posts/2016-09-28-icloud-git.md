# Setup a Git Repository in iCloud Drive

`November 27, 2014`

Mac OSX is your preferred operation system as a developer? Then chances are good that you already use iCloud. Apple introduced iCloud Drive with OSX 10.10 (Yosemite) which grants you direct access to your remote iCloud folder. Finally you can move files directly between your local harddrive and iCloud back and forth.

iCloud Drive can easily be used as remote storage for your private git repositories. You don't have to use third-party services like Dropbox anymore. Read further for a quick and simple 3 min tutorial.

Still there? Great! Open your terminal and proceed to the next 4 steps&#x2026;

## Step 1

iCloud Drive is hidden in a verbose library folder accessible from the users home directory. We first create a symlink to simplify access to this directory via terminal:

    $ cd ~
    $ ln -s Library/Mobile\ Documents/com~apple~CloudDocs/ icloud
    $ cd icloud

Now we can simply cd into ~/icloud. All changes to this directory will automatically be synchronized with your iCloud account.

## Step 2

Next we create a bare git repository in iCloud Drive which later serves as remote origin for our project:

    $ cd ~/icloud
    $ mkdir git-repos && cd $_
    $ git init --bare my-project.git

## Step 3

We're ready to create the actual git project. I'm using ~/projects as the root directory for all my dev projects. You might change this to fit your needs.

First we create a new project directory and add two files .gitignore and README:

    $ cd ~/projects
    $ mkdir my-project && cd $_
    $ echo ".DS_Store" > .gitignore
    $ echo "My Awesome Project" > README

Next we initialize a git repository for this project and add the bare repository created in step 2:

    $ git init
    $ git add .
    $ git commit -m "initial commit"
    $ git remote add origin ~/icloud/git-repos/my-project.git
    $ git push -u origin master

## Step 4

Finally we verify that the git repository has been successfully uploaded by checking the web ui of iCloud Drive:

    $ open https://www.icloud.com/#iclouddrive

That's it. Now we can simply use commands like git fetch, git pull and git push origin :branch to work with the iCloud Drive git repository.

# references

-   [winterbe](http://winterbe.com/posts/2014/11/27/setup-icloud-git-repository/)
