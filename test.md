## 关于git的总结
### 基础认知
Git，是一个**分布式**版本控制软件，用于敏捷高效地处理任何或小或大的项目。  
与常用的版本控制工具 CVS, Subversion 等不同，它采用了分布式版本库的方式，**不必服务器端软件支持**。
### Git与SVN区别
**1、Git 是分布式的，SVN 不是。**  
**2、Git 把内容按元数据方式存储**，而 SVN 是按文件。  
**3、Git 分支和 SVN 的分支不同**：分支在 SVN 中一点都不特别，其实它就是版本库中的另外一个目录。  
**4、Git 没有一个全局的版本号，而 SVN 有**：目前为止这是跟 SVN 相比 Git 缺少的最大的一个特征。  
**5、Git 的内容完整性要优于 SVN**：Git 的内容存储使用的是 SHA-1 哈希算法。  
### Git三区域
- **工作区：** 就是你在电脑里能看到的目录。  
- **暂存区：** 英文叫 stage 或 index。有时也叫作索引（index）。  
- **版本库：** 英文叫repository  
### 版本回退
1. 先用git log --pretty=oneline或git log查看
2. 回退git reset --hard bianhao
3. 要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本
### Git与Github链接
#### 先有本地库，后想线上库，并且同步：
1. 先在GitHub上建立一个远程仓库
2. 本地库右键Git Bash Here
3. 初始化git init
4. 本地一波操作（比如建了个test.md）
5. git add test.md
6. git commit -m "created test.md"
7. 和远程仓库链接git remote add origin git@github.com:username/repositoryname.git（使用的是SSH）
8. 提交修改git push -u origin main (main是主分支名，-u作用是之后提交修改可以只用写git push)
9. 再修改的话先add后commit最后push  
#### 先有线上库，后想克隆库：
0. 线上已经有仓库
1. 本地mkdir filename
2. cd filename
3. git init
4. git clone git@github.com:username/repositoryname.git（使用的是SSH）
5. success!
### 分支管理
- 查看分支git branch(* 表示当前分支)
- 创建git branch branchname
- 切换git checkout branchname  
  (上两项操作可合为git checkout -b name)
- 删除git branch -d branchname
- 合并git merge branchname
