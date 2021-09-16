# update-notifier-analysis

update-notifier-analysis

## 前言

## 环境准备

## 源码

```js
'use strict';
const {spawn} = require('child_process');
const path = require('path');
const {format} = require('util');
const importLazy = require('import-lazy')(require);

const configstore = importLazy('configstore');
const chalk = importLazy('chalk');
const semver = importLazy('semver');
const semverDiff = importLazy('semver-diff');
const latestVersion = importLazy('latest-version');
const isNpm = importLazy('is-npm');
const isInstalledGlobally = importLazy('is-installed-globally');
const isYarnGlobal = importLazy('is-yarn-global');
const hasYarn = importLazy('has-yarn');
const boxen = importLazy('boxen');
const xdgBasedir = importLazy('xdg-basedir');
const isCi = importLazy('is-ci');
const pupa = importLazy('pupa');
```

### 源码概览

一个 `UpdateNotifier` 类构造函数
三个方法

- check
- fetchInfo
- notify

导出一个函数 `` 和 `UpdateNotifier` 类

```js
class UpdateNotifier {
    constructor(options = {}) {
    }
    check(){}
    async fetchInfo(){}
    notify(options){}
}

module.exports = options => {
    const updateNotifier = new UpdateNotifier(options);
    updateNotifier.check();
    return updateNotifier;
};

module.exports.UpdateNotifier = UpdateNotifier;
```

## 总结
