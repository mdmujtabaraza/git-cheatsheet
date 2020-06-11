`git config --global user.name USERNAME`\
`git config --global user.email EMAIL`

`cat ~/.gitconfig`
`git config --global --list`
`git config --global -e`



## Config P4Merge as Default Merge Tool and Diff Tool

In Windows Add P4Merge installation directory as path to environment variables

`git config --global merge.tool p4merge`\
`git config --global mergetool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"`\
`git config --global mergetool.prompt false`

`git config --global diff.tool p4merge`\
`git config --global difftool.p4merge.path "C:/Program Files/Perforce/p4merge.exe"`\
`git config --global difftool.prompt false`