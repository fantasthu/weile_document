## 前端开发规范

###  代码提交规范

1,新增内容提交到各自的分支上
2,项目上线打 tag
3,修改线上 bug, 在 master 上切一个 bug 分支,然后修改合并提交

###  基础设施

1,环境安装
git , node 环境
2,代码管理工具(比如码云)
3,任务管理工具(如 teambition,个人觉得 tower 更加的好用)
4,bug 管理工具
5,接口管理工具

### 前端工具

1,vscode,以及其插件

> 1Auto close tag
> eslint
> file peak
> git lens
> local history
> npm
> npm intellisense
> path autocomplete
> vetur
> vscode-icons
> vue2 snippets
> vueHelper

2,vscode 配置

```
{
  // 将设置放入此文件中以覆盖默认设置
  "editor.fontSize": 14,
  "vsicons.presets.jsOfficial": true,
  "workbench.iconTheme": "file-icons",
  "window.zoomLevel": 0,
  "editor.snippetSuggestions": "top",
  "editor.tabCompletion": true,
  // 搜索除去
  "search.exclude": {
    "**/node_modules": true,
    "**/bower_components": true,
    "**/.history": true
  },
  // 隐藏文件夹中的文件
  "files.exclude": {
    // "**/.history": true
  },
  "workbench.sideBar.location": "left",
  "editor.tabSize": 2,
  "emmet.syntaxProfiles": {
    "javascript": "jsx",
    "vue-html": "html",
    "vue": "html",
    "wpy": "html"
  },
  "emmet.includeLanguages": {
    "vue-html": "html",
    "vue": "html",
    "wpy": "html",
    "javascript": "javascriptreact",
    "plaintext": "jade"
  },

  "editor.formatOnSave": true,
  // "eslint.validate": [
  //     "javascript",
  //     "javascriptreact",
  //     {
  //         "language": "html",
  //         "autoFix": true
  //     },
  //     {
  //         "language": "vue",
  //         "autoFix": true
  //     }
  // ],
  "eslint.options": {
    "plugins": ["html"]
  },
  "eslint.autoFixOnSave": true,
  "prettier.singleQuote": true,
  "prettier.semi": false,
  // rem和px转化
  "rempx.remEqual": 10,
  // 本地文件缓存时间
  "local-history.daysLimit": 300,
  "files.associations": {
    "*.wpy": "vue"
  },
  "git.enableSmartCommit": true
}
```

3,eslint 规范

```
module.exports = {
  root: true,
  parser: 'babel-eslint',
  parserOptions: {
    sourceType: 'module'
  },
  env: {
    browser: true
  },
  // https://github.com/feross/standard/blob/master/RULES.md#javascript-standard-style
  extends: 'standard',
  // required to lint *.wpy files
  plugins: ['html'],
  settings: {
    'html/html-extensions': ['.html', '.wpy']
  },
  // add your custom rules here
  rules: {
    // allow paren-less arrow functions
    'arrow-parens': 0,
    // allow async-await
    'generator-star-spacing': 0,
    // allow debugger during development
    'no-debugger': process.env.NODE_ENV === 'production' ? 2 : 0,
    'space-before-function-paren': 0,
    'no-undef': 0,
    'standard/computed-property-even-spacing': 0
  }
}
```
