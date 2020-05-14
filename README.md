# git-test

git在不同分支上创建的文件，需要先commit，这样在另外的分支上通过git status才能看不到未提交，不然分支上未提交的文件，在主分支上也能看到未提交

## git upstream
### 1.将项目B clone 到本地
```
git clone -b master 项目B的git地址
```
### 2.将项目A的git地址，添加至本地的remote
```
git remote add upstream 项目A的git地址
```
### 3.在本地新建一个分支，该分支的名称最好与项目A中新增的那个分支的名称相同以便区分
```
git checkout -b 新分支名称
```
### 4.从项目A中将新分支的内容 pull 到本地
```
git pull upstream 新分支名称
```
### 5.将 pull 下来的分支 push 到项目B 中去
```
git push origin 新分支名称
```
