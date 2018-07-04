## HTTPS协议提交代码到GitHub (2018.07.03)
* 有时候在company只能以代理ip的方式上网，这个时候使用ssh协议的话，好多时候是提交不了代码到远程库的
* [解决failed to push some refs to git](https://www.jianshu.com/p/835e0a48c825)
```
* git pull --rebase origin master   // 拉取远程库代码下来
* git push -u origin master
```
* 使用https协议就可以实现和远程库的协作
1. `官网下载Git`
2. `设置用户名和邮箱`
* 右键打开 Git Bash Here
```
* git config --global user.name "Galen"
* git config --global user.email "827472476r@qq.com"
```
3. `查看一下设置好的用户名和邮箱`
```
* git config --global user.name
* git config --global user.email 
```
4. `提交代码`
```
* 提交到本地
echo "# android" >> README.md
git init                // 创建本地仓库
git add README.md       // git add . : 表示提交所有文件到本地
git commit -m "first commit"

* 提交到远程库
git remote add origin https://github.com/GalenDeng/android.git
git push -u origin master
```