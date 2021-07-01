
# Remote Repositories
In order to collaborate on Git projects, you must interact with remote repositories, versions of a project residing online or on a network. You can work with multiple repositories, for which you can have read/write or read-only privileges. Teams can use remote repositories to push information to and pull data from.

* Cloned Repositories
As mentioned earlier, for cloned repositories, Git will automatically give the name “origin” to the server from which you cloned and the name “master” to your local branch.

* Seeing Your Remotes
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.

* Adding Remotes
To create a new remote Git repository with a short name, use the following format:

* Fetching
Fetching entails pulling data that you don’t have from a remote project.

Here is the command format:

git fetch [remote-name]


* Pushing
To push your changes “upstream” for sharing, you would use the following git push command format:

git push [remote-name][branch-name]
Example:

$ git push origin master
*This command pushes committed changes from your local “master” branch upstream to the “origin” server.

Note: You can only successfully push changes upstream if you have write access for the server from which you cloned, and if someone else has not pushed changes upstream that you haven’t pulled yet. If a collaborator pushed changes upstream after you had cloned, your push will not be successful. You will have to pull new changes and merge them with your branch before you can successfully push your changes upstream.

* Renaming/Removing Remotes
Rename

To rename a remote’s short name, use the git remote rename command.

Example:

$ git remote rename js jane

$ git remote

origin

jane
*In the example above, we can see that the remote’s short name has been changed from js to Jane. The command git remote lists our existing remotes, which jane is now one of. The rename action also alters names of remote branches: js/master would change to jane/master.

Remove

To remove a remote for whatever reason (e.g., a contributor has left the team, the server has moved), simply use the git remote rm command:

Example:

$ git remote rm jane

$ git remote

origin
NOTE: Reminder: “origin” is simply the default remote name when you use the git clone command.
