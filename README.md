
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


```
add submodules
git submodule add https://git@dev.azure.com/sss/_git/Common submodules/Common
pull submodules
git submodule update --recursive --remote
```
