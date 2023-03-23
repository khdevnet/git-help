
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
[Add submodule](https://github.com/khdevnet/git-help/blob/master/submodules.md)
