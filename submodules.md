### Add submodule to folder

add submodules
```
git submodule add https://git@dev.azure.com/sss/_git/Common submodules/Common
load specific branch for submodule
```

update .gitmodules, add at the end
```
[submodule "submodules/Common"]
	path = submodules/Common
	url = https://git@dev.azure.com/sss/_git/Common
	branch = feature/test
```

pull submodules
```
git submodule update --init
git submodule update --recursive --remote
```

### Git remove submodule
```
git rm <path-to-submodule>
```

#### Other

sync all submodules
```
git submodule foreach --recursive 'git submodule sync'
```
