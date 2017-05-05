一 环境安装
===
nodejs安装
---
    官网下载对应版本

选装cnpm
---
        npm install cnpm -g --registry=https://registry.npm.taobao.org
二 配置gulp
===

安装gulp包(全局安装)
---
    cnpm install gulp -g
pack.json配置依赖关系(重要)
---
    npm init
插件安装
---
    cnpm install gulp --save-dev
    cnpm install gulp-concate --save-dev
配置脚本
---
编写gulpfile.js脚本文件:

    var gp = require('gulp');
    var concat = require('gulp-concat');
    gp.task("jsConcat", function () {
        // 把1.js和2.js合并为main.js，输出到dest/js目录下
        gp.src(["js/ktw.user.js","js/ktw.db.js"])
            .pipe(concat('ktw.cps.js')).pipe(gp.dest('dist'));
    });

执行脚本
---
    - 示例:cmd-> gulp taskName
