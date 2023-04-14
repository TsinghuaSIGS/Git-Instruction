## 常用的一些Git以及VS code使用方法

### Github回退代码到历史指定版本

> ### 第一种 github网页回滚

第一步、找到需要滚到的版本号
找到需要回滚的项目和分支，点击History，查看历史记录。
找到需要回滚的版本，点开。

第二步、回滚操作
点击Options-Revert回滚按钮。
选择需要回滚的分支。

第三步、提交
ok

> ### 第二种 git客户端

第一步、找到需要滚到的版本号
使用git log命令查看所有的历史版本，获取你git的某个历史版本的id。

```
git log --pretty=oneline
或者git log 
备注：版本号为某次提交后的版本号
```

第二步、回滚操作
回滚操作。

```
git reset --hard fae6966548e3ae76cfa7f38a461c438cf75ba123
```


第三步、提交
将回滚的结果提交到需要的分支。

```
git push -f -u origin master/main
备注：master/main为需要push到的分支，如果直接简单"git push"会提示低版本不可push到高版本
```
