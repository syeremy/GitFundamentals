git init
ren .gitignore.txt .gitignore
git add .
git status
git remote add origin https://syeremy1@bitbucket.org/syeremy1/website.git
git commit -m "initial Load"
git status
git remote -v
git push origin master
========================================================================

--Undo changes
git checkout

--undo commits
git reset --soft Head~1
git reset --hard head~1

-Remove files from tracking
-- list files to be removed
git clean -n
-- perform delete
git clean -f

echo "" > .gitignore

-- See commit logs (press q to exit)
git log --oneline --graph

--list remote branches
git branch -r

--link between local master with remote (origin)
git branch --set-upstream-to origin/master
git branch --track origin/master
	origin 		-> local branch
	origin/master	-> remote branch
	
-- add and commmit at the same time
git commit -am "commit message"


--remove origin
gitremote rm origin

--add origin with ssh instead of http(s)
git remote add origing git@github.com:syeremy/GitFundamentals.git

--add tags
git tag "[tag]"

--add tag with message (will prompt an editor to add the annotation [message]))
git tag -a "[tag]"

--add a signed tag (will prompt an editor to add the message and passphrase))
git tag -s "[tag]"

--verify tag
git tag -V "[signed_tag]"

--push tags to remote
git push --tags