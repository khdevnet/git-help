
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
	branch = feature/4516_book-appointment
pull submodules
git submodule update --recursive --remote
```
