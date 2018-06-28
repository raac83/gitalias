# gitalias

[alias]
    gl = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative --all
    b = branch
    d = diff --patience
    dc = diff --cached --patience
    st = status -sb
    ci = commit
    ca = commit -a
    co = checkout
    up = checkout
    ff = merge --ff-only
    ap = add -p
    dl = diff --name-only
    st = stash
    sl = stash list
    sp = stash pop
    sa = stash apply
    sd = stash drop

[color]
    ui = auto

[color "branch"]
    current = green reverse
    local = green
    remote = red

[branch]
    autosetuprebase = always

[merge]
    tool = diffmerge

[mergetool "diffmerge"]
    trustExitCode = true
    cmd = /usr/local/bin/diffmerge --merge --result=\"$MERGED\" \"$LOCAL\" \"$BASE\" \"$REMOTE\"

[push]
    default = simple
[difftool "sourcetree"]
	cmd = /Applications/DiffMerge.app/Contents/MacOS/DiffMerge --nosplash \"$LOCAL\" \"$REMOTE\"
	path =
[mergetool "sourcetree"]
	cmd = /Applications/DiffMerge.app/Contents/MacOS/DiffMerge --merge --result=\"$MERGED\" \"$LOCAL\" \"$BASE\" \"$REMOTE\"
	trustExitCode = true
