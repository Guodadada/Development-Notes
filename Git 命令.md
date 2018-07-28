# Git 命令


## 1. 基础

```

1. git init
2. git add <file>
3. git commit -m "xxxx"

--

1. git status
2. git diff
3. git log
4. git log --pretty=oneline

```

## 2. 日志和回退

/15322381752193 2.jpg

```

1. git reset --hard commit_id
2. git log
3. git relog

```

## 3. 三个回退版本的场景

1. 未提交到暂存区
    
    ```
    git checkout -- <file>
    ```
    
2. 已提交到暂存区

    ```
    1. git reset HEAD <file>
    2. git checkout -- <file>
    
    ```
    
3. 已 commit 到本地库

    ```

    git reset --hard commit_id
    
    回退上个版本：
    git reset --hard HEAD^
    
    ```

## 4. 移除文件

1. 移除本地文件：  

    ```
    rm <file>
    ```
2. 移除本地库文件：

    ```
    git rm <file>
    git commit -m "xxxx"
    ```
    
    
---

# 远程库操作

## 1. 关联远程库

```
git remote add origin git@server-name:path/repo-name.git
```

## 2. 第一次推送master分支的所有内容

```
-u 参数的作用：
1. 把本地的master分支内容推送到远程新的master分支
2. 把本地的master分支和远程的master分支关联起来

git push -u origin master
```


## 3. 克隆库

```
git clone git@github.com:xxxx
```


---

# 分支

## 1. 基础命令

1. 查看分支：`git branch`
2. 创建分支：`git branch <name>`
3. 切换分支：`git checkout <name>`
4. 创建 + 切换分支：`git checkout -b <name>`
5. 合并某分支到当前分支：`git merge <name>`
    
    ```
    git merge --no-ff -m "xxx" <branch name>
    
    --no-ff：会在merge时生成一个新的commit，这样，
    从分支历史上就可以看出分支信息。
    ```
    
6. 删除分支：`git branch -d <name>`
7. 查看分支合并图：`git log --graph --pretty=oneline --abbrev-commit`


## 2. 情景：正在写新需求，现要求更改 master 的一个 bug。

1. dev 分支上保存工作区内容（未添加到暂存区及本地库的内容）
2. 在 master 上新建一个 bug 分支
3. 在 bug 分支修复 bug 代码
4. 回到 master 分支，merge bug 分支
5. 删除 bug 分支
6. 回到 dev 分支
7. 恢复保存的工作区内容，完成


```
1. git stash（保存工作区内容）
2. git stash list（查看保存的工作区）

```

## 3. 丢弃一个没有被合并过的分支

```
git branch -D <name>
```


# 合作开发相关命令

1. 查看远程库信息，使用 `git remote -v`；
2. 本地新建的分支如果不推送到远程，对其他人就是不可见的；
3. 从本地推送分支，使用 `git push origin branch-name`，如果推送失败，先用 `git pull` 抓取远程的新提交；
4. 在本地创建和远程分支对应的分支，使用 `git checkout -b branch-name origin/branch-name`，本地和远程分支的名称最好一致；
5. 建立本地分支和远程分支的关联，使用 `git branch --set-upstream branch-name origin/branch-name`；
6. 从远程抓取分支，使用 `git pull`，如果有冲突，要先处理冲突。


# 相关拓展

1. 去掉 ssh 密码：`ssh-keygen -p` 
    
    ```
   ~ » ssh-keygen -p                                                                   qitmac000466@1aa
Enter file in which the key is (/Users/qitmac000466/.ssh/id_rsa):
Enter old passphrase:
Enter new passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved with the new passphrase.
    ```


2. 拉去远程分支：`git pull origin FLIGHT-72150:FLIGHT-72150`

