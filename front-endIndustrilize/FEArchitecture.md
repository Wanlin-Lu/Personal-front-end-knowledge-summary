﻿# 六、产品前端架构

标签（空格分隔）： 模块 框架 库 流程 选型

---
## 目录
* 6.1 [协作流程][6.1]
* 6.2 [接口设计][6.2]
* 6.3 [版本控制][6.3]
* 6.4 [技术选型][6.4]
* 6.5 [一般开发过程][6.5]
---
### 6.1 协作流程
#### 6.1.1 web系统
web系统就是`服务器`，`浏览器`及两者之间的`交互关系`构成的系统。<br>
![web系统](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.1.1.png)<br>
web系统在服务器中的部分有三层：`Controller:控制层`,`Model:数据层`,`View:视图层`,三者关系如下：<br>
![web系统分层](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.1.2.png)<br>
一般前端的技术栈：<br>
![前端技术栈](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.1.3.png)<br>
大前端技术栈（包括了本来后端负责的控制层）：<br>
![大前端技术栈](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.1.4.png)<br>
#### 6.1.2 角色定位
* 一般web系统工程人员包括
    * `视觉工程师`
    * `前端工程师`
    * `后端工程师`

其中`前端工程师`又可以分为`页面工程师`和`前端工程师`；
<br>页面工程师技术栈：<br>
![页面工程师技术栈](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.2.1.png)<br>

* `页面工程师`技术栈:
    - 精通切图技术（Photoshop）
    - 精通页面制作技术（css、HTML）
    - 熟悉前端开发技术（JavaScript、template）
    - 了解后端开发技术（Java、node、···）

<br>
前端工程师技术栈：<br>
![前端工程师技术栈](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.2.2.png)<br>

* `前端工程师`技术栈:
    - 精通页面技术（css、HTML）
    - 精通页面开发技术（JavaScript、template）
    - 熟悉切图技术（Photoshop）
    - 熟悉后端开发技术（Java、node、···）

* 项目的开发时间：
    - 页面制作：3天
    - 前端逻辑：7天
    - 后端逻辑：10天

因此如果单角色开发的话，就需要20天的时间；而如果多人协作的话，就只需要10天时间；
![web工程开发时间](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.2.3.png)
        
#### 6.1.3 协作流程
`前端工程师`,`后端工程师`,`页面工程师`在一个web系统工程的开发过程中的分工协作流程如下图：
![前端工程协作流程](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.3.1.png)

* 在协作过程中必需的三个规范：
    - 页面入口规范
    - 同步数据规范
    - 异步数据规范

web系统开发完成，进入后续的维护时期，这时的协作流程如下图：
![维护期协作流程](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.1.3.2.png)
    
#### 6.1.4 web系统开发职责说明
* `页面工程师`
    - 切图、优化图片
    - 页面制作、优化页面效果与结构
    - 完成简单的前端业务逻辑开发
* `前端工程师`
    - 主导制定前后端分离规范
    - 主导前后端联调对接测试
    - 系统前端设计架构、满足一定的非功能需求（可扩展性、？）
    - 完成系统前端的业务逻辑实现、优化实现逻辑
* `后端工程师`
    - 协助制定前后端分析规范
    - 协助前后端联调对接测试
    - 完成后端系统架构及业务逻辑实现

### 6.2 接口设计
#### 6.2.1 概述
在web系统的交互过程中，`url`,`template`,`API`,`model`之间的规则需要确定下来；<br>
![web交互规则](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.1.1.png)
#### 6.2.2 接口规范
我们需要制定三个规范：`页面入口规范`,`同步数据规范`,`异步接口规范`;
![三个规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.1.png)
##### a 页面入口规范
![页面入口规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.a-1.png)<br>
页面入口规范文本样本：<br>
![页面入口规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.a-2.png)
##### b 同步数据规范
![同步数据规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.b-1.png)<br>
同步数据规范文本样本：<br>
![同步数据规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.b-2.png)
##### c 异步接口规范
![异步接口规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.c-1.png)<br>
异步接口规范文本样本：<br>
![异步接口规范](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.2.c-2.png)

#### 6.2.3 规范的应用
应用页面入口规范可以建构出项目的前端整体结构：<br>
![建构项目结构](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.3.1.png)<br>
应用页面入口规范可以建构出后端的template结构：<br>
![建构template结构](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.3.2.png)<br>
应用同步数据规范可以建构模拟同步数据结构：（有自动化工具）<br>
![建构模拟同步数据](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.3.3.png)<br>
应用异步数据规范可以建构模拟异步数据结构：（有自动化工具）<br>
![建构模拟异步数据](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.3.4.png)<br>

#### 6.2.4 本地开发
搭建前端开发的本地环境-->本地服务器和本地代理：<br>
![本地服务器和本地代理](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.4.1.png)<br>
本地模拟服务器（处理本地请求->模板+模拟数据）：<br>
![本地模拟服务器](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.4.2.png)<br>
本地代理（处理异步请求->模拟数据）：<br>
![本地代理](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.4.3.png)<br>
![本地代理](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.4.4.png)<br>
联调（去掉本地环境）：<br>
![联调](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.2.4.5.png)<br>

### 6.3 版本控制
#### 6.3.1 版本控制系统
* 版本控制系统即VCS（version control system）是一种记录若干文件的修订记录的系统，它帮助我们查阅或回到某个历史版本
    - “人肉”VCS
        - 人工管理文件的版本修改记录；
        - ![人肉VCS](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.1.1.png)
        - 缺点：工作量大，无法管理复杂项目
    - LVCS本地
        - 比如：RCS（Revision Control System）
        - ![RCS](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.1.2.png)
        - 缺点：无法多人协调开发
    - CVCS集中式
        - 比如：CVS（Concurrent Versions System）、SVN（Subversion）、Perforce；
        - ![CVS](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.1.3.png)
        - 缺点：每次操作都需要经过网络
    - DVCS分布式
        - 比如： Git、Mercurial
        - ![DVCS](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.1.4.png)

#### 6.3.2 分支模型
##### 6.3.2.1 分支和分支模型
* 分支：
    - 从目标仓库获得一份项目拷贝，每条拷贝都有和原仓库功能一样的开发线；
- 分支模型（branching model）/工作流（workflow）
    - 一个围绕项目（开发/部署/测试）等工作流程的分支操作（创建、合并等）规范集合；

##### 6.3.2.2 产品级的分支模型
* 常驻分支
    - development
        - 从master创建
    - production（master）
        - 默认分支
* 活动分支
    - feature
        - 从development创建
    - hotfix（bug修复）：如hotfix-36
        - 从master创建
    - release：如release-110
        - 从development分支创建

##### 6.3.2.3 分支模型——特性开发
![特性开发](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.2.3.png)
##### 6.3.2.4 分支模型——发布线
![发布线](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.2.4.png)
##### 6.3.2.5 四种开发环境
![开发环境](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.2.5.png)
#### 6.3.3 Git
##### 6.3.3.1 简介
* Git是什么
    - Git是一个免费开源的分布式版本控制系统（DVCS）
    - Git是一个基于内容寻址的存储系统
- Git历史
    - Git的出现离不开Linux
        - 1991-2002：几乎无版本控制（patch包）
        - 2002-2005：BitKeeper
        - 2005-至今：Git
- 和`BitKeeper`相比`Git`的优势
    - 快
    - 完全的分布式
    - 轻量级的分支操作
    - Git已经成为现实意义上的标准
        - Android
        - Apache
        - Eclipse
        - Gnome
        - The Linux KernelPerl
        - 几乎所有优秀前端的开源项目
    - 社区成熟活跃
- Git的安装
    - Windows： msysgit http://msysgit.github.io
    - Mac: brew install git
    - Ubuntu: apt-get install git

##### 6.3.3.2 命令详解
###### 帮助
```html
/* 打开帮助文档 */
git help <command>
/* 打开窗口帮助 */
git <command> -h
/* 打开帮助文档 */
git <command> --help
/* ??????? */
man git-<command>
```
###### 基本操作
* 配置git
```html
git config

用户配置：
    - git config --global user.name "Wanlin-Lu"
    - git config --global user.email test@example.com
配置级别：
    - --local【默认，高优先级】：只影响本仓库  .git/config
    - --global 【中优先级】 ：影响到所有当前用户的Git仓库  ~/.gitconfig
    - --system 【低优先级】 ：影响到全系统的Git仓库  /etc/gitvonfig
```
* 初始化仓库
```html
/* 初始化仓库 */
git init
    - git init [path]
    - git init [path] --bare
```
![git仓库](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-1.png)<br>

* 状态查询
```html
/* 对状态的跟踪 */
git status
- 未跟踪<->跟踪
- 工作目录<->暂存区
- 暂存区<->最新提交
```
* 添加文件内容到暂存区（同时文件被跟踪）
```html
/* 添加和跟踪文件到暂存区 */
git add
    - 如： git add README.md

/* 批量添加 */
git add .

/* 忽略文件 */
.gitignore
    - 在添加时忽略匹配的文件
    - 仅仅作用于未追踪的文件
```
* 从暂存区删除
```html
/* 从暂存区删除 */
git rm
    - git rm --cached :仅从暂存区删除
    - git rm :从暂存区和工作目录删除
    - git rm $(git ls-files --deleted) :删除所有被跟踪，但是在工作目录被删除的文件
```
* 工作目录与暂存区
    - 文件：货架上的物品
    - 工作目录：货架
    - 暂存区：购物车
    - 提交内容：购买
<br>

* 提交到提交区
```html
/* 根据暂存区内容创建一个提交记录 */
git commit -m 'a commont'

/* 直接从工作区提交 */
git commit -a -m 'a commont'
```
* 显示提交历史纪录
```html
/* 提交记录 */
git log

/* 单行显示提交记录 */
git log --oneline

/* 自定义显示样式 */
git log --color --graph --pretty=format:...
```
* git 组合短命令
```html
/* 组合命令 */
git config alias.shortname <fullcommand>

git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(boldblue)<%an>%Creset' --abbrev-commit"

git lg
```
* 显示不同版本差异
```html
/* 工作目录与暂存区的差异 */
git diff

/* 工作目录与某次提交之间的差异 */
git diff <reference>

/* 暂存区与某次提交的差异，默认为HEAD */
git diff -cached [<reference>]
```
显示不同图解：![git diff 图解](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-2.png)<br>

* 撤销本地修改
```html
/* 将文件内容从暂存区复制到工作目录 */
git checkout -- <file>
```
* 撤销暂存区内容
```html
/* 将文件内容从上次提交复制到暂存区 */
git reset HEAD <file>
```
* 撤销全部改动
```html
/* 将内容从上次提交复制到工作目录 */
git checkout HEAD -- <file>
git checkout HEAD -- README.md
```
* 基本操作总结
    - 三区操作：![三区操作总结](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-3.png)
    - 文件夹和工作区：![文件夹和工作区](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-4.png)

##### 6.3.3.3 分支操作
* 分支的增删查改
```html
/* 列出所有的分支 */
git branch

/* 创建新分支 */
git branch <branchName>

/* 删除分支 */
git branch -d <branchName>

/* 显示当前的分支信息，带*为当前分支 */
git branch -v
```
* 通过移动HEAD检出版本，可用于切换分支
```html
/* 切换到某分支,并更新工作空间 */
git checkout <branchName>

/* 创建并切换到一个分支 */
git checkout -b <branchName>

/* commit id ，version id */
git checkout <reference>
```
* 将当前分支回退到历史某个版本
```html
git reset --mixed <commit>(默认)
git reset --soft <commit>
git reset --hard <commit>

如：git reset --mixed e390b3
```
git reset:![git reset](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-5.png)<br>

* 回退历史记录
![git reflog](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-6.png)<br>
* 使用捷径
![git shortpass](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-7.png)<br>

* reset VS checkout
![reset VS checkout](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-8.png)<br>

* 保存目前的工作目录和暂存区状态，并返回到干净的工作空间
```html
/* 创建并保存到stash区，并清空工作空间 */
git stash save 'a-stash-name'

/* 列出所有的stash区 */
git stash list

/* 把某stash区的内容返回到工作空间 */
git stash apply stash@{0}

/* 删除某stash */
git stash drop stash@{0}

/* stash apply + stash drop */
git stash pop stash@{0}
```
stash:![stash](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-9.png)<br>

* 合并分支
```html
/* 合并分支到新的节点 */
git merge [next]

/* 单线合并，移动head到新的提交 */
git merge fast-forward

/* 合并的过程查询 */
git cat-file -p HEAD

/* 如果合并中有冲突，就要解决冲突，然后重新合并 */
```
git merge next:![merge](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-10.png)<br>

* 修剪提交历史基线，俗成“变基”
    - git rebase:![rebase](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-11.png)
    - git rebase --onto:![rebase](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-12.png)
    - 但是不要在共有的分支使用rebase

* 对某个提交设置一个不变的别名
    - git tag v0.1 e39d0b2
    - ![git tag](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.3.3.2-13.png)
    - git checkout v0.1
    


##### 6.3.3.4 远程操作
* git 支持本地协议，所以我们可以初始化一个本地的远程服务器（裸服务器，没有工作目录）
    - git init ~/git-server --bare
* 提交本地历史到远程
    - git push /Users/Wanlin-lu/git-server master（第一次提交）
    - git push origin master（以后的提交）
* 远程仓库相关配置操作（配置别名）
    - git remote add origin ~/git-server
    - git remote -v
* 获取远程仓库的提交历史
    - git fetch + merge
    - git pull = git fetch + git merge
* 完整获取远程仓库
    - git init + git remote + git pull
    - git clone

##### 6.3.3.5 其他参考资料
- git 简明指南
    - http://rogerdudler.github.io/git-guide/index.zh.html
- Pro git
    - http://git-scm.com/book/zh/v1/


### 6.4 技术选型
#### 6.4.1 JS模块和模块组织
##### 6.4.1-1 JS的模块组织
要建立一个大的web系统，最好的方法是把这个大型的应用分解成一个个小的功能块儿，分别实现之后，进行整合，就完成了这个宏大系统的建设。在Java中有`import`;在C#中有`using`;在css中有`@import`;但是JavaScript中的语言级别的模块支持还没有成熟。
##### 6.4.1-2 模块的作用
* 封装实现
* 暴露接口
* 声明依赖

##### 6.4.1-3 反模式（没有应用任何模块系统技术）
建立一个可以进行简单算术运算的JS模块，并在其基础上建立一个计算器模块；
```javascript
/* math.js */
function add(a,b){
    return a + b;
}
function sub(a,b){
    return a - b;
}
/* 封装性无；接口结构不明显 */

/* caculator.js */
var action = "add";
function compute(a,b){
    switch (action){
        case "add": return add(a,b);
        case "sub": return sub(a,b);
    }
}
/* 没有声明依赖；使用全局状态； */
```
对上面的两个模块进行改进：
```javascript
/* math.js */
var math = {
    add: function add(a,b){
        return a + b;
    },
    sub: function mul(a,b){
        return a - b;
    }
}
/* 结构性好；访问控制； */

/* caculator.js */
var caculator = {
    action: 'add',
    compute: function compute(a,b){
        switch(action){
            case "add": return math.add(a,b);
            case "sub": return math.sub(a,b);
        }
    }
}
/* 同样没有声明依赖； */
```
IIFE(Immediately-invoked Function Expression)(自执行的函数表达式)
```javascript
/* caculator-1.js */
var caculator = (function({
    var action = "add"
    function compute(a,b){
        switch (action){
            case "add":return m.add(a,b);
            case "sub":return m.sub(a,b);
        }
    }
    return{
        compute: compute;
    }
})(math)
/* 显示依赖管理；仍然污染了全局变量；必须手动进行依赖管理； */
```
##### 6.4.1-4 命名空间
```javascript
// namespace
var namespace = (function(){
    var cache = {}
    function createModule(name,deps,definition){
        if(arguments.length === 1)return cache[name];
        deps = deps.map(function(depName){return na(depName)});
        cache[name] = definition.apply(null,deps);
        return cache[name];
    }
    return createModule;
})()

// math.js
namespace("math",[],function(){
    function add(a,b){return a+b;}
    function sub(a,b){return a-b;}
    return {
        add: add,
        sub: sub
    }
})

// caculator.js
namespace("caculator",["math"],function(m){
    var action = "add"
    function compute(a,b){
        return m{action}(a,b)
    }
    return{
        compute: compute
    }
})
```
##### 6.4.1-5 依赖管理
手动管理依赖是非常困难的：<br>
![依赖管理](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.1-5.png)
##### 6.4.1-6 模块系统
* 模块系统进行依赖的管理
    - 加载
    - **分析**
    - **注入**
    - 初始化
* 采用不同的模块系统就要有不同的模块写法
    - Commonjs
    - AMD(Asynchronous Module Dfinition)
    - ES6 module

###### 1. Commonjs/module (a module spec for javascript outside the browser)
```javascript
/* math.js */
function add (a,b){
    return a + b;
}
function sub (a,b){
    return a - b;
}
exports.add = add
exports.sub = sub

/* caculator.js */
// 声明依赖，运行时注入
var math = require("./math");
function Caculator (container){
    this.left = container.querySelector(".j-left");
    this.right = container.querySelector(".j-right");
    this.add = container.querySelctor(".j-add");
    this.result = container.querySelector(".j-result");
    
    this.add.addEventListener("click",this.compute.bind(this));
}
Caculator.prototype.compute = function(){
    this.result.textContent = math.add(+this.left.value,+this.right.value)
}
//暴露接口
exports.Caculator = Caculator;
```
* 优点：
    - 依赖管理成熟可靠
    - 社区活跃，规范接受度高
    - 运行时支持，模块定义非常简单
    - 文件级的模块作用域隔离
    - 可以处理循环依赖
* 缺点
    - 不是标准组织的规范
    - 同步的require，没有考虑浏览器环境
* 那么是不是意味着前端就无法使用commonjs了呢？不是的，通过以下工具就可以使用了：
    - Browserify
    - webpack
    - component
    

###### 2. AMD(Asynchronous Module Definition)
```javascript
/* math.js */
define([],function(){
    function add(a,b){
        return a + b;
    }
    function sub(a,b){
        return a - b;
    }
    //接口暴露
    return {    
        add: add,
        sub: sub
    }
})

/* caculator.js */
define(["./math"], function(math){
    function Caculator (container){
        this.left = container.querySelector(".j-left");
        this.right = container.querySelector(".j-right");
        this.add = container.querySelector(".j-add");
        this.result = container.querySelector(".j-result");
        
        this.add.addEventListener("click",this.compute.bind(this));
    }
    Caculator.prototype.compute = function(){
        this.result.textContent = math.add(+this.left.value,+this.right.value);
    }
    return{
        Caculator: Caculator
    }
})

/* Simplified CommonJS wrapping */
define(function(require,exports){
    var math = require("./math");
    
    function Caculator(container){
        this.left = container.querySelector(".j-left");
        this.right = container.querySelector(".j-right");
        this.add = container.querySelector(".j-add");
        this.result = container.querySelector(".j-result");
        
        this.add.addEventListener("click",this.compute.bind(this));
    }
    Caculator.prototype.compute = function(){
        this.result.textContent = math.add(+this.left.value,+this.right.value);
    }
    exports.Caculator = Caculator;
})

/* 完整组件 = 结构 + 逻辑 + 样式 */
define(["regularjs","text!path/to/foo.html","css!path/to/style.css"],function(Regular,template){
    //通过text插件，template是通过Ajax加载的纯文本
    Component = Regular.extend({
        template = template,
        show: function(){},
        hide: function(){}
    })
})
```
* 优点
    - 依赖管理成熟可靠
    - 社区活跃，规范接受度高
    - 专为`异步IO环境`打造，适合浏览器环境
    - 支持类似Commonjs的书写方式
    - 通过插件API可支持加载非JS资源
    - 成熟的打包建构工具，并可结合插件
* 缺点
    - 模块定义繁琐，需要额外嵌套
    - 只是库级别的支持，需要引入额外库
    - 无法处理循环依赖
    - 无法实现条件加载

###### 3. ES6 module（JavaScript module definition for future）
```javascript
/* math.js */
function add(a,b){
    return a + b;
}
function sub(a,b){
    return a - b;
}
//export关键字：接口暴露
export{add,sub}

/* caculator.js */
//import关键字：引入依赖
impotr{add} from'./math';
//es6有了关键字class
class Caculator{
    //略...
}
export{Caculator}
```
* 优点：
    - 是真正的规范，未来的模块标准
    - 语言级别的关键字支持
    - 适应所有JavaScript运行时，包括浏览器
    - 同样可处理循环依赖
* 缺点：
    - 规范未达到稳定级别
    - 基本还没有浏览器支持
    - 鲜有项目使用，即使有大量的6TO5的天然水平力他人


###### 4. 如何使用这些工具？Systemjs(universal dynamic module loader)
* 支持加载AMD
* 支持加载Commonjs
* 支持加载ES6
* 支持Transpiler,可支持任意资源

```javascript
/* systemjs */

```

#### 6.4.2 框架与库(解答框架与库的what、why、how)
* 库（library）
    - 针对特定问题的解答
    - 不控制应用程序
    - 被动的被调用
* 框架（framework）
    - inverse of control
        - ![控制反转](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-1.png)
    - 决定应用程序生命周期
    - 一般会集成大量的库
* 库和框架：都是解决方案：
    - DOM
    - Communication
    - Utility
    - Templating
    - Component
    - Routing
    - Architecture
* 为什么要使用外部的解决方案呢？
    - 开发效率
    - 可靠性：浏览器兼容性、测试覆盖
    - 更好的配套：文档、DEMO、工具
    - 设计的更好
    - 专业性
* 什么时候不使用外部解决方案？
    - 问题过于简单
    - 备选框架质量与可控性无法保证
    - 无法满足当前业务需求
    - 团队中已有相关积累
* 如何整合自己的解决方案？
    - 开放：基于一个外部模块系统，自由组合。
    - 半开放：基于一个定制过的模块系统，内部-外部的解决方案共存
    - 大教堂：深度定制的模块系统，很少需要引入外部模块

##### 6.4.2-1 关于DOM的解决方案
KEY-Words：`selector`,`manipulaion`,`event(dom)`,`animation`;

* 职责：
    - 提供便利的DOM查询、操作、移动等操作
    - 提供事件绑定、事件代理等支持
    - 提供浏览器特性检测、UA侦测
    - 提供节点属性、样式、类名等操作
    - 所有以上操作实现目标平台的跨浏览器支持


1.jQuery
```js
//jQuery对象，非原生DOM对象
$("button.j-submit")
    .addClass("disable")
    .attr("title","Waiting")
    .html("Waiting...")
    .on("click",showWarning)
    .appendTo(".j-form")
```
2.zepto.js
```js
$("button.j-submit")
    .addClass("disable")
    .attr("title","Waiting")
    .html("Waiting...")
    .on("click",showWarning)
    .appendTo('.j-form')
```
3.mootools
```js
$("button.j-submit")
    .addClass("disable")
    .setAttribute("title","Watting")
    .set("html","Waiting...")
    .addEvent("click",showWarning)
    .inject(".j-form")
    
/* 特点：获得的是原生的DOM对象；
 * Mootools直接扩展了dom对象原生
 * Element.prototype.inject = function(){}
 * Element.prototype.set = function(){}
 */
```
![控制反转](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-1-1.png)<br>

* 对比
    - mootools:最好的原码阅读学习资源
    - jQuery：最稳妥的方案
    - zepto.js：移动端的备选品
- 选择
    - Issue的总量与解决率比Star更关键
* 其他特殊方案
    - 手势：**Hammer.js**
    - 局部滚动： iscroll.js
    - 高级动画： **Velocity.js**
    - 视频播放： **video.js**


##### 6.4.2-2 关于通信的解决方案
KEY-word:`XmlHttpRequest`,`Form`,`JSONP`,`Socket`;

* 职责
    - 处理与服务器的请求与响应
    - 预处理请求数据、响应数据Error、success的判断封装
    - 多种类型请求，统一接口（XMLHTTPRequest1/2，JSONP，Iframe）
    - 处理浏览器兼容性


![communication](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-2-1.png)<br>
1.Reqwest
```javascript
/* Robust wrapper for asynchronous http requests */
reqwest({
    url:'http://www.filltext.com/',
    type:'jsonp',
    success:function(resp){
        var ret=[];
        resp.forEach(function(item){
            ret.push(item.fname + '<br />');
        });
        document.getElementById('results').innerHTML = ret.join('');
    }
})
```
* 优点：
    - JSONP支持
    - 稳定/IE6+support
    - CORS跨域
    - Promise/A支持

2.qwest
```javascript
/* Ajax library with promises and XHR2 support */
qwest.<method>(<url>,[data],[options])
    .then(function(response){
        //Run when the request is suc
    }
    .catch(function(e,url){
        //Process the eror
    })
    .complete(function(){
        //Always run
    });
```
* 优点：
    - 更小的代码量
    - XmlHttpRequest2
    - CORS跨域
    - 支持高级数据类型如ArrayBuffer，Blob和FormData

3.socket.io（the fastest and most reliable real-time engine)<br>
```javascript

```
* 特点：
    * 实时性
    * 支持二进制数据流
    * 智能自动回退支持（非二进制数据流）
    * 多种多种后端语言支持


##### 6.4.2-3 工具包的解决方案
KEY-word： `函数增强&shim`,`Flow Control`

* 职责：
    - 提供原生JS不提供的功能
    - 方法门面包装，使其更易于使用
    - 异步队列，流程控制等等

```javascript
/* 应用 */
var list = [1,4,3,2,5],list2 = [];
for(var i = 0,len = list.length; i<len;i++){
    if(list[i] < 4) list2.push(list[i]);
}
console.log(list2)//=>[1,3,2]

/* Extension(unscore.js) */
var list2 = _filter(list,function(item,index){
    return item < 4;
})//=>[1,3,2]

/* shim */
var list2 = list.filter(function(item,index){
    return item < 4;
})//=>[1,3,2]
var list2 = list.filter(item => item < 4 );
/* Shim需要保证实现与规范一致 */
```
![工具包对比](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-3-1.png)<br>    
##### 6.4.2-4 模板技术
KEY-word：`String-based`,`Dom-based`,`Living Template`;

1.String-based
```html
/* 模板 */
<h3>{title}</h3>
<ul>
{#list users as user}
    <li>{user}</li>
{/list}
</ul>

/* 数据 */
{
 title:"hello",
 users:["HanMeimei","LiLei","Jack"]
}

/* 展现 */
<h3>Hello</h3>
<ul>
    <li>HanMeimei</li>
    <li>LiLei</li>
    <li>Jack</li>
</ul>
```
特点：改换数据之后，展现不会改变：<br>
![string-based](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-4-1.png)

2.Dom-based
```html
/* 模板 */
<h3>{title}</h3>
<ul>
    <li repeat="user in users">
    {user}
    </li>
</ul>

/* 数据 */
{
 title:"hello",
 users:["HanMeimei","LiLei","Jack"]
}

/* 展现 */
<h3>Hello</h3>
<ul>
    <li>HanMeimei</li>
    <li>LiLei</li>
    <li>Jack</li>
</ul>
```
特点：改换数据之后，展现跟着改变：<br>
![Dom-based](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-4-2.png)

3.Living-template
```html
/* 模板 */
<h3>{title}</h3>
<ul>
{#list users as user}
    <li>{user}</li>
{/list}
</ul>

/* 数据 */
{
 title:"bye",
 users:["Tom","Jack"]
}

/* 展现 */
<h3>Bye</h3>
<ul>
    <li>Tom</li>
    <li>Jack</li>
</ul>
```
特点：改换数据之后，展现跟着改变：<br>
![living-template](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-4-3.png)
<br>三种模板技术对比：<br>
![模板技术方案对比](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-4-4.png)

##### 6.4.2-5 组件的解决方案
KEY-word：`Modal`,`Slider`,`DatePicker`,`Tabs`,`Editor`;

* 职责
    - 提供基础组件CSS支持
    - 提供常用组件如：Slider，Modal
    - 提供声明式的调用方式（Option）
* 选择
    - Bootstrap
        - jQuery 版本的 Bootstrap
        - Knockout-Bootstrap
        - React-Bootstrap
    - Foundation

<br>对比：<br>
![组建方案的对比](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-5-1.png)

##### 6.4.2-6 路由的解决方案
KEY-word：`Client Side`,`Server Side`;

* 职责：
    - 监听URL变化，并通知注册的模块
    - 通过JavaScript进行主动跳转
    - 历史管理
    - 对目标浏览器的兼容性支持
* routing库
    - page.js
        - 兼容IE8+
        - 类似Express.Router的路由规则的前端路由库
    - crossroad.js
        - 老牌库（两年未更新），API定义较为繁琐
    - Director.js
        - 兼容IE6+
        - 可以前后端使用一套规则来定义路由(其实不可以的呀！)
    - Stateman
        - 兼容IE6+
        - 用于处理深层复杂路由的独立路由库


##### 6.4.2-7 架构（解耦）
KEY-word：`MVC`,`MVVM`,`MV*`;

* 职责：
    - 提供一种范式帮助（强制）开发者进行模块解耦
    - 视图与模型分离
    - 更容易进行单元测试
    - 更容易实现应用程序的扩展

* MVVM：
    - Model：数据实体，比如Car/Person等等，他们用于记录应用程序的数据；
    - View：展示友好的界面，它是数据的定制反映，它包含样式结构定义以及与VM享有的声明式数据、事件绑定
    - ViewModel：View与Model的粘合剂，它通过绑定、事件与View交互，并可以调用Sevice处理数据持久化，当然也能通过数据绑定将Model的变动更新到View中

![MVVM](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.4.2-7-1.png)

* 学习网站：
    * http://todomvc.com/
    * https://www.javascripting.com/
    * https://www.javascriptoo.com/
    * http://microjs.com/

### 6.5 一般开发流程
#### 6.5.1 系统设计
##### 6.5.1-1 交互说明
阅读交互稿，理清交互稿中的`交互流程`,`交互行为`,`异常提示`;<br>
![交互稿阅读](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-1.png)
##### 6.5.1-2 系统分解
阅读设计稿(主要视觉稿)，清理出系统的主要`功能点`和`结构布局`；

* 功能点
    - 注册登录密码
* 系统主框架
    - 顶栏
    - 边栏
    - 底栏
    - 内容区


![系统分解](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-2.png)

##### 6.5.1-3 接口设计
从系统功能点中找出`数据交互点`，前后端一起确定:`数据类型`,`模板资源`,`异步or同步接口`,`开发说明文档`;
![接口设计1](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-3-1.png)<br>
![接口设计2](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-3-2.png)

##### 6.5.1-4 工程构建
建构前后端模板：<br>
前端实现<br>
![前端实现](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-4-1.png)
<br>后端模板<br>
![后端模板](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-4-2.png)
<br>生成初始代码<br>
![初始代码](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-4-3.png)
<br>生成模拟数据<br>
![模拟数据](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.1-4-4.png)

#### 6.5.2 系统实现
##### 6.5.2-1 静态页面的实现
1.Photoshop切图，提取原件，制作sprite；<br>
![切图](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-1-1.png)<br>
2.通用列表的开发；<br>
![列表开发](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-1-2.png)<br>
3.复合组件开发；<br>
![组件](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-1-3.png)<br>
4.浮层弹窗开发；<br>
![弹窗](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-1-4.png)<br>
5.完成静态页面的制作；

##### 6.5.2-2 组件封装
1.组件结构<br>
![组件结构](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-2-1.png)<br>
2.模板（slider.html）<br>
![模板](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-2-2.png)<br>
3.逻辑（slider.js）<br>
![逻辑](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-2-3.png)<br>
4.示例（demo.html）<br>
![示例](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-2-4.png)<br>

##### 6.5.2-3 逻辑实现
![逻辑实现](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-3-1.png)<br>
1.数据层实现——节目数据（program.js）<br>
![节目数据](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-3-2.png)<br>
2.页面模板实现——页面模板（rec.ftl）<br>
![页面模板](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-3-3.png)<br>
3.控制层实现——页面入口（rec.js)<br>
![页面入口](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.2-3-4.png)<br>

#### 6.5.3 测试发布
##### 6.5.3-1 本地测试
1.配置模拟数据<br>
2.使用同步模拟数据<br>
![同步模拟](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-1-1.png)<br>
3.使用异步模拟数据<br>
![异步模拟](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-1-2.png)<br>
##### 6.5.3-2 对接联调
1.去除同步模拟数据<br>
![同步模拟](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-2-1.png)<br>
2.去除异步模拟数据<br>
![异步模拟](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-2-2.png)<br>
##### 6.5.3-3 发布上线
1.打包发布<br>
![打包发布](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-1.png)<br>
2.最终内容<br>
![最终内容](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-2.png)<br>
3.打包配置：<br>
3.1输入配置<br>
![输入配置](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-3.png)<br>
3.2优化图片<br>
![优化图片](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-4.png)<br>
3.3CDN配置<br>
![CDN配置](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-5.png)<br>
3.4代码压缩<br>
![代码压缩](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-6.png)<br>
3.5代码合并<br>
![代码合并](https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/images/5.5.3-3-7.png)<br>

---
[6.1]:https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/HCJD/6.FE-architecture.md#61-协作流程
[6.2]:https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/HCJD/6.FE-architecture.md#62-接口设计
[6.3]:https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/HCJD/6.FE-architecture.md#63-版本控制
[6.4]:https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/HCJD/6.FE-architecture.md#64-技术选型
[6.5]:https://github.com/Wanlin-Lu/Front-end-knowledge-summary/blob/master/HCJD/6.FE-architecture.md#65-一般开发流程




