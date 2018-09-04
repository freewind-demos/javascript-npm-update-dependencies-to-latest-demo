JavaScript Npm Update Dependencies to Latest Demo
=================================================

有时候打开一个年久失修的repo，发现里面的依赖版本都很旧，想直接升级到当前最新的版本。

遗憾的是，npm本身不支持这样的功能，不过我们可以通过一个工具`npm-check-updates`实现。

```
npm install
npx ncu -u
```

可以看到`package.json`中的`lodash`的版本被自动从一个极老的版本`^1.0.1`更新到了当前最新的版本。

```
Using /Users/freewind/workspace/javascript-npm-update-dependencies-to-latest-demo/package.json
⸨░░░░░░░░░░░░░░░░░░⸩ ⠇ :
 lodash  ^1.0.1  →  ^4.17.10
Upgraded /Users/freewind/workspace/javascript-npm-update-dependencies-to-latest-demo/package.json
```

然后再执行一次：

```
npm install
```

即可。

注：`npm-check-updates`一般安装为全局工具：`npm install -g npm-check-updates`