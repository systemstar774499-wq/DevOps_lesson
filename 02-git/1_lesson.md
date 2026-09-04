# Для установки GIT
 PS D:\DevOps_lesson> git init
Initialized empty Git repository in D:/DevOps_lesson/.git/
# Добовляем целую в репазитори 
PS D:\DevOps_lesson> git add .
# Делаем cammit
PS D:\DevOps_lesson> git commit -m "first commit"
# Выходит такая ошибка
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'Admin@DESKTOP-TYIJH89Y.(none)')
# Для регистраци в github видем следуюшию команду
PS D:\DevOps_lesson> git config --global user.email "systemstar774499@gmail.com"
PS D:\DevOps_lesson> git config --global user.name "systemstar774499"
# Проверяем
PS D:\DevOps_lesson> git config --list                               
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=schannel
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=main
core.editor="C:\Users\Admin\AppData\Local\Programs\Microsoft VS Code\bin\code
" --wait
user.email=systemstar774499@gmail.com
user.name=systemstar774499
core.repositoryformatversion=0
core.filemode=false
core.bare=false
core.logallrefupdates=true
core.symlinks=false
core.ignorecase=true

# Делаем заново cammit

PS D:\DevOps_lesson> git commit -m "first commit"                            
[main (root-commit) e1d7efe] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 00-roadmap.md
# Прошло успешно
# Ввидем следуюшую команду

PS D:\DevOps_lesson> git remote add origin https://github.com/systemstar774499-wq/DevOps_lesson.git

PS D:\DevOps_lesson> git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 214 bytes | 214.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/systemstar774499-wq/DevOps_lesson.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

# Всё прошло успешно

# Потом изменяем в папке заново делаем cammit

PS D:\DevOps_lesson> git commit -m "second commit"                           
On branch main        
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        01-linux/
        06-my-lab.md

nothing added to commit but untracked files present (use "git add" to track)

# Выходит следушая ошибка.
# Мы забыли вести команду git add это надо нам что бы добавить не сушествуюшие файли и папки

# Ввидем следуюшую команду

PS D:\DevOps_lesson> git add .                                               

# Потом делаем cammit
PS D:\DevOps_lesson> git commit -m "second commit"
[main 652db27] second commit
 12 files changed, 375 insertions(+)
 create mode 100644 01-linux/01-wsl2.md
 create mode 100644 01-linux/02-linux-basics.md
 create mode 100644 01-linux/03-filesystem.md
 create mode 100644 01-linux/04-networking.md
 create mode 100644 01-linux/05-systemd.md
 create mode 100644 01-linux/SSH.md
 create mode 100644 01-linux/commands.md
 create mode 100644 01-linux/filesystem.md
 create mode 100644 01-linux/networking.md
 create mode 100644 01-linux/permissions.md
 create mode 100644 01-linux/processes.md
 create mode 100644 06-my-lab.md
PS D:\DevOps_lesson> git push -u origin main      
branch 'main' set up to track 'origin/main'.
Everything up-to-date
PS D:\DevOps_lesson> 