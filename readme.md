# Vcs ? :
short for version control system, a software that tracks your code changes or files over time.
# Why GIT ? :
unlike other vcs GIT stores files and code changes as snapshots instead of a list of file based changes
## Cool details :
Nearly everything is local so no need for network, you can easily track your code changes offline no server reaching needed and reads it directly from your local database so you can see your backups at any given time.
# INTEGRITY Notion :
Everything is being checksummed before any changes using a mechanism called SHA-1 hash, mainly a 40 character hexadecimal hash calculated on the actual file or repo directory etc...  
it often looks like this  

```bash
24b9da6552252987aa493b52f8696cd6d3b00373
```
GIT is only used to add data it is hard to get the system to do anything that is undoable or erase data but genuinely safe once you commit all your changes.
# MAIN STATES :
```mermaid
flowchart LR
%% Colors %%
classDef red fill:red,stroke:red,stroke-width:20px,color:grey

classDef blue fill:blue,stroke:blue,stroke-width:30px,color:grey

classDef grey fill:grey,stroke:grey,stroke-width:15px,color:black

%% link 0 %%
WK(Working Directory):::red  ===> |Project Checkout|GD(.git directory/Repo)

%% link 1 %% 
WK ===> |Stage Fixes|SA(Stating Area):::blue

%% link 2 %%
SA ===> |Commit|GD:::grey

%% Styling %%
linkStyle 0,1,2 stroke:grey
```
# Crucial steps :
#### **Creating a GIT Repo :**
- method 1 : take a local directory that is currently under version control then turn it into a GIT repo.
- method 2 : clone an existing GIT repo on your local machine.
#### **Initializing a Repo in an Existing Directory :**
```bash
$ cd C:/Users/user/my_project
```
then type
```bash
$ git init
```

#### **Staging Files :**
```bash
git add .
```

#### **Committing Files :**
```bash
git commit -m "your message"
```

#### **Pushing Files :**
```bash
git push
```

#### **Ignoring Files :**
```bash
$ cat .gitignore
```
# GIT Branching Basics :
to create a branch you run this command
```bash
git branch "name of your branch wihtout quotes"
```
### Important Clarification ! :
- When creating a new branch you're still on your main one with the help of a pointer called Head, so in order to switch the header and work on your desired branch you should use this command below
```bash
git checkout "your branch"s name without quotes"
```
to show all your commit histroy run this command
```bash
git log --all
```
for the desired branch, same command but type your branch's name instead of the ---all decorator





