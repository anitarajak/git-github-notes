# git-github-notes
#git commands##
when you install git bash, the first thing you should be doing is setting up your user details for only one time

#git config --global user.name " Anita Rajak"
#git config --global user.mail "anitarajak123@gmail.com"

Now Check for seetings :

#git config -list (OR) #git config -global -list (OR) #git config user.name

Task 1 : create a new repositiory and publish it to github, how to do that ?

Step1 : Go to the directory where you want to create the git repository
Let's say i want to create on desktop, then go to desktop directory
# cd ~/desktop
#mkdir git-commmands  << creating one directory called git-commands >>
#cd git-commands      << go inside the directory >>
#git init             << Initializing one empty git repository so that we will be able to maintain the history of the project "git-commands" >>
#touch name.txt        << create some files >>
#git status            << This command will tell that some changes are made and it is untracked >>
#git add .            <<  Add all the untracked file in staging area >>
(OR) #git add name.txt  << this command will add name.txt file in staging area >>
#git commit -m "name.txt file created in git-command directory"
#git status
on branch master
nothing to commit, working tree clean

---> now open file name.txt and make some changes
#git status
#git commit -a -m "updated name.txt file in git-commands directory"   << if we use -a along with commit command, no need to execute git add command separately >>

---> CREATE A REPOSITORY IN GITHUB AS FOLLOWS
     ------------------------------------------
Login into github (http://github.com)
On the right side top corner click on "+" symbol and click on "New repository" and give the repository name and click on create repository.

---> Now we want URL of the remote repository to b attached with the local project so that we can push our codein the remote repo for that
#git remote add origin << remote repo URL>>

---> NOW WE HAVE TO PUSH THE CHANGES IN YOUR LOCAL REPOSITORY TO GIT HUB REMOTE REPOSITORY FOR THAT :
#git push origin master    << here push is a git commands, origin is the url name, and master is the branch name >>

-----------------------------------------------------------------------------------------------------------------------                                                  

#git log  --> this will give you all commit ID's
#git log -2 --> it will display only 2 commit ID's


---> GIT BRANCHING
    -----------------

#git branch      << it gives branch name in current repository >>
#git branch <branchname you want to create>     << creating new branch >>
example : git branch feature (here i am creating one new branch called feature)

#git branch -v    << it will display all the branches in your repo, and also tell you what branch you are currently in >>

#git checkout <branchname>    << switch to new branch and all the commits will be added in this branch now >>
example : git checkout feature

#git merge <branchname>       << you want to merge this to main/master branch now >>
example : git merge feature  (it will merge feature branch to main branch)
