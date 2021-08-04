# free-code-camp-git-tutorial

Based on Gwendolyn Faraday's github tutorial on Free Code Camp's YouTube channel:  https://www.youtube.com/watch?v=RGOj5yH7evk&t=1689s

Notes for Windows OS:

A. Obtain git software  
   1. Instructions:  
      i.  https://aadamich.wordpress.com/articles/git/git-ssh-with-visual-studio/  
     ii.  https://www.atlassian.com/git/tutorials/install-git  
    iii.  During install process, select "Use Git from Git Bash Only".  
          a.  Add git program's bin path to the Path in the System Variables list from System Properties->Environmental Variables  
          b.  Or add GitHub extension in Visual Studio Code?  I haven't done this (8/1/2021).  
    
B. Create and use SSH key to pull git repo from GitHub to VS Code  
   1. Intro and links to SSH key creation and use:  https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh  
      i. In Git Bash, search for existing SSH key  
     ii. If none, open Git Bash. Create new SSH key (add to SSH agent to avoid retyping password)  
    iii. Add new SSH key to GitHub account:  https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account  
     iv. In VS Code:  
         a. Open folder where git repository will be pulled from GitHob.  
         b. Open VS Code terminal:  
            *  ***Next to "TERMINAL" ensure "bash" ("Git Bash") is selected for data type.  If default "PowerShell" is selected, different commands are used for listing files - refer to C. 1. regarding ls -la command to list all files in a folder.  If using PowerShell anyway, use dir -force to list all files (thanks for Youtube Bony's comment to GitHub tutorial, July 2021)  ***  
            *  In folder directory (should be there already), type  
            *  git clone  
            *  then from GitHib repo, in the Download/Clone options (click the green button), copy the link in "Clone with SSH" and paste it into the VS Code terminal to get:  
            *  git clone git@github.com:myGithubUsername/repositoryName.git  
            *  type git password if not using SSH agent.  
  
C. Now GitHub repo is in the designated VS Code folder  
   1. Check that the folder is a repo directory.  
       i. In terminal, change directory:  
          a.    cd repositoryName  
      ii. Then show all folders in directory (to confirm repo folder):  
          a.  ls -la  
     iii. Or, list everything in directory, including hidden folders. 
      iv. Update a file in the repo and create new files.
       v. Check git's status regarding the files:  e.g. 1 modified, 1 untracked.
          a.  git status
      vi. *  *** DO NOT USE THE
          *  git add
          *  command in the Git Bash terminal, or the following error occurs:
          *  "fatal: Unable to create 'C:/ ...path... /.git/index.lock': No such file or *  directory" BUT 
          *  git add 
          *  DOES WORK in the PowerShell terminal.
        
            
