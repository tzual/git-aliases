# git-aliases

st=status -s
sw=switch
co=checkout
ci=commit
br=branch
cp=cherry-pick
fp=fetch -p
sl=stash list
sa=stash apply
ss=stash save
la=!git config -l | grep alias | cut -c 7-
unstage=reset HEAD --
last=log -1 HEAD
gone=! git fetch -p && git for-each-ref --format '%(refname:short) %(upstream:track)' | awk '$2 == "[gone]" {print $1}' | xargs -r git branch -D
