## git命令

想要让git对一个目录 进行版本控制需要以下步骤:

* 进行要管理的文件夹

* 执行初始化命令

  > git init 

* 管理目录下的文件状态

  > git status
  >
  > 注:新增的文件和修改过后的文件都是红色

* 管理指定文件(红变绿)

  > git add 文件名
  >
  > git add .

* 个人信息配置:用户名,邮箱[一次即可]

  > git config --global user.email "you@example.com"
  >
  > git config --global user.name "your name"

* 生成版本

  > git commit -m "描述信息"

* 查看版本记录

  > git log

* 回退至之前版本

  > git log
  >
  > git reset --hard 版本号

* 回退至之后版本

  > git reflog
  >
  > git reset --hard 版本号

### 命令总结

* 查看分支

  > git branch 

* 创建分支

  > git branch 分支名称

* 切换分支

  > git checkout 分支名称

* 分支合并(可能产生冲突)

  > git merge 要合并的分支
  >
  > 注意: 切换分支再合并

* 删除分支

  > git branch -d 分支名称

* ssh实现免密码登录

  ```
  1. 生成公钥和私钥(默认放在~/.ssh目录下,id_rsa.pub公钥,id_rsa私钥) ssh-keygen
  2. 拷贝公钥的内容,并设置到github中
  3. 在git本地中配置ssh地址
  	git remote add origin git@github.com:lovewqf/aiproject.git
  4, 以后使用
  	git push origin master
  	
  ```

  