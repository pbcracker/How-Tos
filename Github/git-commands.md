# **Interacting With Remote Repositories**

## *Setup*
User Info (required info will be associated with commits):
* >git config --global user.name "name" 
* >git config --global user.email "email"
* >git config --global color.ui auto 

Connecting to Already Established Remote Repo:
* >git remote add [alias] [url]
    * Note: [alias] is what you will use to reference the remote repo going forward.
    * Note: [url] can be found by going to the github repo you want to commit to > green code button > then copy either HTTPS or SSH depending on how you want to connect.

## *Working With The Local Repo*
* >git branch 
    * Note: displays branches (* will be next to the active branch).
* >git add [file]
    * Note: ads file as it appears now to the next commit stage ('.' captures the entire directory).

## *Commit to Remote Repo*
* >git push [alias] [local]:[remote]
