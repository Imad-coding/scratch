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
classDef blue fill:blue,stroke:blue,stroke-width:5px,color:grey

classDef blue fill:blue,stroke:blue,stroke-width:5px,color:grey

classDef grey fill:grey,stroke:grey,stroke-width:5px,color:black

%% link 0 %%
WK(Working Directory)  ===> |Project Checkout|GD(.git directory/Repo):::blue

%% link 1 %% 
WK ===> |Stage Fixes|SA(Stating Area):::blue

%% link 2 %%
SA ===> |Commit|GD:::grey

%% Styling %%

``` 


