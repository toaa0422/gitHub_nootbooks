JIRA-1234 feat: support for async execution

^-------^ ^--^: ^-------------------------^
|         |     |
|         |     +--> Summary in present tense.
|         |
|         +--> Type: feat, fix, docs, style, refactor, perf, test or chore.
|
+--> Jira ticket number

Type 类型必须是下面之一，并且为小写:

    feat: 修改/增加新功能
    fix: 修改bug的变更
    docs: 文档相关变更
    style: 不影响代码含义的变更(空白、格式、缺少符号等)
    refactor: 代码重构变更
    perf: 改进性能的变更
    test: 添加/修改现有的测试
    chore: Build, .gitignore或辅助工具、库(如文档生成)等变更





```
## 提交格式：

    
          1. <type>(<scope>): <subject>
    
      2. // 空一行
    
      3. <body>
    
    
    

## 范例:
		1. fix #251: add DataValidation
      	2.  
      	3. 提交的具体情况

##  说明：

### type（必需）

用于说明 commit 的类别

  * br: 此项特别针对bug号，用于向测试反馈bug列表的bug修改情况
  * feat：新功能（feature）
  * fix：修补
  * docs：文档（documentation）
  * style： 格式（不影响代码运行的变动）
  * refactor：重构（即不是新增功能，也不是修改bug的代码变动）
  * test：增加测试
  * chore：其他的小改动. 一般为仅仅一两行的改动, 或者连续几次提交的小改动属于这种
  * revert：feat(pencil): add 'graphiteWidth' option (撤销之前的commit)
  * upgrade：升级改造
  * bugfix：修补bug
  * optimize：优化
  * perf: Performance的缩写, 提升代码性能
  * test：新增测试用例或是更新现有测试
  * ci:主要目的是修改项目继续完成集成流程(例如Travis，Jenkins，GitLab CI,Circle)的提交
  * build: 主要目的是修改项目构建系统(例如glup，webpack，rollup的配置等)的提交

### scope（可选）

scope用于说明 commit 影响的范围，比如数据层、控制层、视图层等等，视项目不同而不同。

### subject（必需）

subject是 commit 目的的简短描述，不超过50个字符。  
以动词开头，使用第一人称现在时，比如change，而不是changed或changes  
第一个字母小写  
结尾不加句号（.）

### <body>(可选)

部分是对本次 commit 的详细描述，可以分成多行



优化自：<https://www.jianshu.com/p/79454cf00945>

Git Commit message 编写指南: <https://gitee.com/help/articles/4231#article-
header0>
```