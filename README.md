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
working-1-main = our develop branch, working-1-develop = out feature branch
2 updates from "working-1-main"
2 local pushes in "working-1-develop"

Steps:
A) Working with the "working-1-main" branch
1. Switch to local "working-1-main"
2. Pull 2 updates without clicking any option

B) Working with the "working-1-develop" branch
1. Switch to local "working-1-develop"
2. Right click "working-1-main" on left panel
3. Rebase current changes onto "working-1-main"
4. Push to remote (depend) ***Force Push is required if there is [x]behind y[fast-forward]

C) Working with the "working-1-main" branch
1. Switch to local "working-1-main"
2. Right click "working-1-develop" on left panel
3. ~~Rebase current changes onto "working-1-develop"~~
4. **Merge** "working-1-develop" into "working-1-main"
5. Push to remote (depend)

