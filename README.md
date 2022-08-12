
#### Init hooks from CMD
```
$ git config core.hooksPath hooks    # Init git hooks by path [./hooks]
```

#### Init hooks using package.json scripts they will be configured durring $ npm install

```
  "scripts": {
    ...
    "preinstall": "git config core.hooksPath hooks"
  }
```

#### Add submodule to folder
```
add submodules
git submodule add https://git@dev.azure.com/sss/_git/Common submodules/Common
load specific branch for submodule
update .gitmodules, add at the end
[submodule "submodules/Common"]
	path = submodules/Common
	url = https://git@dev.azure.com/sss/_git/Common
	branch = feature/test
pull submodules
git submodule update --init
git submodule update --recursive --remote
```
### Change file ending
```
git add --renormalize
```

### Git remove submodule
```
git rm <path-to-submodule>
```

#### Other
```
sync all submodules
git submodule foreach --recursive 'git submodule sync'
```
