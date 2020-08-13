## 前端自动化测试

#### 为什么要进行自动化测试

1.功能越多越复杂，出现bug的风险越高；

2.bug发现的越晚，修复bug的成本越高；

3.手动测试繁琐，容易出错

### 两种基本的自动化测试

#### 1. 单测

直接测试代码的逻辑，一个函数或一个模块都可以是一个单元。站在开发角度，白盒测试

单元测试两种形态：

a. ***TDD（Test-Driven Development 测试驱动开发）\***：在开发功能代码之前，先编写测试代码。可以帮助客户和程序员明确需求，

优点：在任意一个开发节点都可以拿出一个可以使用，含少量bug并具一定功能和能够发布的产品。
缺点：增加代码量。测试代码是系统代码的两倍或更多，但是同时节省了调试程序及挑错时间。

b. ***BDD（Behavior Driven Development 行为驱动开发）\***：通过自然语言书写不是程序员也可以看懂的测试语言。能让开发者集中精力在开发项目上，而不是写测试代码，也能减少沟通客户、产品、开发之间的沟通成本。

常用工具，jest/mocha

#### 2. E2E（端到端测试/验收测试）

用脚本控制浏览器来触发web程序的功能，测试程序界面和功能。

工具：cypress

站在测试人员角度，类似黑盒测试

#### 测试框架大概有以下几种：

#### Mocha

Mocha是一款特性丰富的，运行在浏览器和nodejs 环境的测试框架（framework），它让异步测试更加简单有趣（官方给它的定义是：简单、灵活、有趣）。
mocha + chai + karma        安装 npm i --save mocha should  

#### Jest

Jest是一个令人愉快的 JavaScript 测试框架，专注于简洁明快。

mocha + chai + 【karma / supertest】   /   jest + jest-extended + jest-html-reporters

tag: 自动化测试脱离不开的一个概念：持续集成，不停的跑测试，每一次提交都需要跑测试。保证任何一次提交都通过测试代码测试

### 常用的测试工具

###### karma

​	把我们测试过程中编写的测试用例，通过它调用浏览器来运行这些测试用例，然后再汇集测试结果，生成测试报告

###### supertest

​	提供HTML请求与链式写法

###### chai

​	断言库

###### should

​	npm官方的解释是一款富有表现力、可读、框架无关的断言库。它的主要目的是让测试断言更富表现力，并对你的测试更有帮助。shouldjs有助于你的测试代码保持整洁，并且让错误信息提供更准确的提示。

### node环境  两种测试框架Mocha  Jest

#### Mocha

需要安装mocha、should、mochawesome、supertest

- mocha测试框架

- should断言库

- mochawesome 测试报告

- supertest 提供HTML请求与链式写法

mocha + should：npm i --save mocha should  

mochawesome：npm install --save-de mochawesome

supertest：npm i --save supertest

tag: npm install onchange --save

#### JEST

- jest：测试框架
- jest-etended：jest断言扩展
- jest-html-reporters：测试报告



jest安装：npm install --save-dev jest

jest-extended： npm i jest-extended-snapshot

jest-html-reporters： npm i jest-html-reporter  (注意，这个工具安装后需要修改源码，工具默认根目录下有temp文件，会自动搜索temp下文件进行数据分析。如果 没有会报错，中止生成报告)

#### Vue环境 测试

- 创建vue项目，vue create [项目名称]。选择测试

- 安装Vue Test Utils （cnpm i @vue/test-utils --save）

  Vue Test Utils是Vue.js官方的单元测试实用工具库
  https://vue-test-utils.vuejs.org/zh/

- Vue e2e测试使用cypress【官网：docs.cypress.io】， 

- unit测试使用jest【官网：jestjs.io】

 



### JEST

###### Jest单元测试的几个指标

![image-20200728152143260](C:\Users\G-JUN\AppData\Roaming\Typora\typora-user-images\image-20200728152143260.png)

- %stmts是语句覆盖率（statement coverage）：是不是每个语句都执行了？

- %Branch分支覆盖率（branch coverage）：是不是每个if代码块都执行了？

- %Funcs函数覆盖率（function coverage）：是不是每个函数都调用了？

- %Lines行覆盖率（line coverage）：是不是每一行都执行了？

### Jest WatchAll

当我们使用`jest --watchAll`之后，jest 提供了多种命令行工具，在 watchAll 模式下按`w`

![image-20200729153447027](C:\Users\G-JUN\AppData\Roaming\Typora\typora-user-images\image-20200729153447027.png)



`f`只测试失败的用例

`o`只测试有代码变更的用例**需要配合git使用**，这样 jest 才能检测到变更

`p`匹配测试文件名

`t`匹配测试名

`q`退出代码监控

`a`测试所有用例

`jest --watchAll`进入`a`模式

`jest --watch`进入`o`模式



####    彩蛋：

一张图说明BDD与ＴＤＤ的关系

![image-20200723165951090](C:\Users\G-JUN\AppData\Roaming\Typora\typora-user-images\image-20200723165951090.png)




