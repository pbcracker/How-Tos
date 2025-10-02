# <span style="color: cyan;"> **Interacting With Remote Repositories** <span>

## <span style="color: cyan;"> *Setup* <span>
Add SSH key to SSH Agent:
* >ssh-add < path to private key > 
    * Note: this does have to be done each time because the SSH Agent stores keys in memory.

User Info (required info will be associated with commits):
* >git config --global user.name "name" 
* >git config --global user.email "email"
* >git config --global color.ui auto 

Connecting to Already Established Remote Repo:
* >git remote add [alias] [url]
    * Note: [alias] is what you will use to reference the remote repo going forward.
    * Note: [url] can be found by going to the github repo you want to commit to > green code button > then copy either HTTPS or SSH depending on how you want to connect.

## <span style="color: cyan;"> *Working With The Local Repo* <span>
* >git branch 
    * Note: displays branches (* will be next to the active branch).
* >git add [file]
    * Note: ads file as it appears now to the next commit stage ('.' captures the entire directory).
* >git commit -m < "Comment">
    * Note: commit must be done before pushing. Make comment applicable to the chnages made.

## <span style="color: cyan;"> *Commit to Remote Repo* <span>
* >git push [alias] [local]:[remote]
    * Note: use this when local and remote branch are different.
* >git push [alias] [brnach]
    * Note: use this when local and remote branch are the same. 

## <span style="color: cyan;"> *Clean Up* <span>
Delete It All ():
* >ssh-add -D
    * Note: removes all keys loaded in agent.
* >rm ~/.gitconfig
    * Note: deletes all global git preferences. 

Delete Specific Entries:
* >ssh-add -d < path to key >
    * Note: removes specified key from agent.
* >git config --global --unset < setting >
    * Note: works well for user.name, user.email, and color.ui.
* >git remote remove [alias]
    * Note: using the delete all options above will not delete remote URLs configured locally. So run "git remote -v" and see which URLs you have configured and their cooresponding alias to remove with this command. 
