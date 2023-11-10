# rgit (recursive git)
Program to run git commands in git repos recursively. This is just a convenience function for running git commands in multiple repos. I find it particularly useful in my ROS workspaces (espeicially if I don't want to change my .rosinstall to use wstool up)

# Common Usage
rgit takes one argument (the starting directory) and passes all other arguments to the git command. So really any git command should be possible, but some don't make a ton of sense to use recursively. There are a few examples below.

## Update all repos in the current directory and belwo with their current upstream branches
`rgit . pull`

## Get status of all repos in the home directory and below
`rgit ~ status`

## Get all commits in all repos from a specific user
`rgit . log --committer=<user@mail.com>`

# Installation
1. Install parallel (e.g. `sudo apt-get install parallel` 
2. Copy file `rgit` executable to `/usr/local/bin` and mark it executable `sudo chmod +x /usr/local/bin/rgit`

# TODO
Make release version that can be installed more easily on distributions
