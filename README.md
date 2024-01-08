# rebase-testing
Testing of rebase action between branches  



# Branch description
1. main - default branch for clone  
2. working-[number]-main - similar to main/master/develop branch  
3. working-[number]-develop - similar to feature branch  



# [number]
My testing count  
For example, i tried 3 times, the [number]=3  



# Scenario
`working-1-main` = `our develop branch`,  
`working-1-develop` = `our feature branch`  
1. 5 updates from `working-1-develop`  
2. rebased changes in `working-1-develop` to `working-1-main`  
3. 1 of the commit is required to remove from `working-1-develop` and `working-1-main`  
4. rebase `interactively` will be used  


Steps:  
1. Create new branch (e.g. working-1-develop-1-working) at the commit that will be removed  
2. Switch to branch (e.g. working-1-develop) that contains the "will be removed" commit  
3. Right click the initial commit (commit before "will be removed" commit)  
4. Select "rebase children of xxx interactively" (sourcetree) or "interactive rebase" -> "rebase interactively [your branch, e.g. working-1-develop] to here" (forkgit)  
select delete or drop the commit "target to remove"  
5. Click rebase  
6. [your branch (local), e.g. working-1-develop] will be updated and requires a force push to update the origin (remote)  
7. [your branch, e.g. working-1-develop] does not contain the "will be removed" commit anymore  

