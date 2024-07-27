# git guide
1.0.3
2024-07-27



\my_project
├── .gitignore
└── .git
   ├── ...
   └── ...


## .gitignore

create file:
`./.gitignore´

```.gitignore
/`directory_name`/
```

`powershell git --version`  
`git -v`
-> git version

`--global`
-> any repository


## config

`git config ...`
-> settings for local repository
   p.e.: `git config user.name "`user_name`"`
   -> set user name, for local repository to `user_name`

`git config --global ...`
-> global settings for repositories
   p.e.: `git config --global user.email "`user_email`"`
-> set global user e-mail to `user_email`

`git config user.name`
-> current user name

`git config user.name "`user_name`"`
-> set user.name to `user_name`

`git config user.email "`user_email`"`
-> set user.email to `user_email`

`git config --global init.defaultBranch main`
-> name branch 'main' by default
   sence 2020 main branch named: 'main'; no longer 'master'

`git help `search_term``
p.e. `search_term` = `config`
-> show help for `search_term` in browser


## Download repository from GitHub

`git clone `remote_repository_url``
-> `git clone https://github.com/username/repository.git`
-> local copy of repository
`cd `repository_directory``

`git clone `remote_repository_url` `local_directory``
-> clone remote repository into `local_directory`


### Download and replace 

```powershell
   Remove-Item -Recurse -Force .\`local_repository`

   git clone `remote_repository_url`


## init

```powershell
   ./git init`
```
-> create .git directory with repository metadata in `project path`

`git status`
-> show status
`git status -s`
-> short version
`git diff`
-> detailed changes for all modified files
`git diff --cached`
-> detailed changes for all modified staged files

`git add `filename.extension``
-> add `filename.extension`; `staging`
`git add .`
-> add all files

git restore <filename.extensioin>
-> restore local file with file in stage, if local file has been changed since last git add

git rm --cached <filename.extension>
-> remove <filename.extension> from stage

git commit
-> 'check in';
   open text editor for writing <commit_message> into (-m)
   no commit without <commit_message> possible

git commit -m "<commit_message>"
-> 'check in'

git commit -a -m "<commit_message>"
-> add and commit
-a git add


## remote repository

echo "# <directory_name>" >> <file_name.extension>
git init
git add <filename.extension>
git commit -m "<commit message>"
git branch -M main
git remote add origin <remote_respository_url>
git push -u origin main


## push

git remote add origin <remote_respository_url>
git branch -M main
git push -u origin main

git config credential.helper 'cache --timeout=900'
-> push automaticaly after 900 sec