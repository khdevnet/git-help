 ### CRLF vs. LF: Normalizing Line Endings in Git
 [CRLF vs. LF: Normalizing Line Endings in Git](https://www.aleksandrhovhannisyan.com/blog/crlf-vs-lf-normalizing-line-endings-in-git/)
 [How autocrlf works](https://stackoverflow.com/questions/1967370/git-replacing-lf-with-crlf)
 
#### How autocrlf works:
```
core.autocrlf=true:      core.autocrlf=input:     core.autocrlf=false:

     repository               repository               repository
      ^      V                 ^      V                 ^      V
     /        \               /        \               /        \
crlf->lf    lf->crlf     crlf->lf       \             /          \
   /            \           /            \           /            \
```

Set autocrlf
```
git config --global core.autocrlf false
```
 
#### Add  Line Endings configuration file
 ```
# .gitattributes

* text=auto
*.cs eol=crlf
*.csproj eol=crlf
*.sln eol=crlf
*.targets eol=crlf
*.sh text eol=lf
*.bash text eol=lf
*.bat text eol=crlf
*.ps1 text eol=crlf
 ```
 
#### Verifying Line Endings in Git for Any File
```
git ls-files --eol # Line Endings in Git for Any File
git ls-files path/to/file --eol # Only for a particular file:
```

#### Update line endings in the working tree
```
git rm --cached -r .
git reset --hard
```

#### Add normilex line eding "lf" to index
```
git add --renormalize .
```
