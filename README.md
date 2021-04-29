# MGMgettingstarted

### On neukum or some host with local home.
###   Setup your local config with the values used in your github account
###   This gets stored in ~/.gitconfig
git config --global user.name "micahgarlichmiller"
git config --global user.email "micahgarlichmiller@gmail.com"
git config --global push.default simple


### figure out where you want to manage your git repos from.  I use ~/git
mkdir git
cd git

### go to the github site and create a new repo
###   Click on cat in upper left to return to github home
###   Click on "New" to create a new repository.
###   I created mine as public and I didnt create a README
###   My remote repo is called micahgarlichmiller/MGMgettingstarted

### after you create a repo in github, it pretty much tells you what to
### do, but first we will create a local dir of the same name
mkdir MGMgettingstarted
cd MGMgettingstarted

### Now, using the instructions from github create a new repo from the 
### commandline
echo "# MGMgettingstarted" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/micahgarlichmiller/MGMgettingstarted.git
git push -u origin main
### You now should be able to see your file up in github

### next I add a file to the repo (this file)
vi MGMgettingstartedwithgithub.txt
git status
git add MGMgettingstartedwithgithub.txt
git commit -m "Added getting started instructions"
git push
