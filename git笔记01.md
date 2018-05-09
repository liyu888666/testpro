# git
## git介绍
  1. git(https://github.com/)是分布式版本控制技术
  2. SVN是集中式管理版本控制技术
  3. 代码托管平台：github,码云，gitlab等

## 第一步注册github及创建仓库

##  第二步 生成公钥和密钥
  命令：   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
  
   执行完上述代码会在C:\Users\Dell\.ssh生成两个文件


## 第三步本地添加邮箱和用户名
      git config --global user.email "you@example.com"
      git config --global user.name "Your Name"


##第四步 克隆仓库

    git clone 仓库地址
    例如：git clone  git@github.com:liyu888666/testpro.git
     ssh:   git@github.com:liyu888666/testpro.git
    https:  https://github.com/liyu888666/testpro.git


## git 常用命令

   克隆：git clone 
   添加：git add 文件名
   查看文件状态：git status
   提交：git commit -m "说明"
   推送：git push
   历史回退:
```
    一、放弃工作区修改: git checkout -- 文件
	
	二、由暂存区返回到工作区 :  git reset HEAD 文件名
	
	三、撤消版本库: git reset --hard commit_id
	
	四、推送出错：先git pull 再git push
```

   git log 查看日志
   git log --pretty=oneline   
   git reflog

查看区别:
    1.查看工作区的修改的差异: git diff 文件名
    2.查看工作区和暂存区区别:git diff --cached 文件名
    3.工作区与版本库的区别: git diff   HEAD 文件名
    4.查看两次版本库之间的差异：git diff    commit_id     commit_id
    
     例如： git diff   bb6a1a8 6111f25

   5.查看两个分支之间的差异:????


   分支:git 重要内容
   
      查看分支： git branch
      创建分支： git branch 分支名
      切换分支：git checkout 分支名
  
      即创建也切换：git checkout -b 新分支

      合并分支：git merge --no-ff 要合并的分支

        删除分支： 
              git branch -d 要删除分支   //删除已合并的分支
              git branch -D 要删除分支    //删除未合并的分支

        解决冲突：手动解决

      git打版本
   
        查看版本：git tag
        创建版本： 
                1.git tag 版本号
                2.git tag 版本号 commit_id
        删除本地版本：git tag -d 要删除的版本号
        删除远程版本：git push origin :refs/tags/要删除的远程版本号


# ES6

    参考资料：
        1.http://es6.ruanyifeng.com/#docs/function   
        2.https://www.cnblogs.com/Wayou/p/es6_new_features.html

    JS:ES(EcmaScript),DOM,BOM
    
     ES1.0   1997
     ES2.0   1998
     ES3.0   1999
     ES4.0    XXXX   2005-2006
     ES5.0   2009
     ES5.1   2011
     ES6     2015
     ES7     2016
     ES8    2017
     ES9    2018
     .....

   ES6新增特性：
   
    1. let,const
       特点：
       （1）没有变量提升
        (2)  块级作用域
        （3）不能重复定义
   2.模板字符串
          适用场景：解决字符串拼接问题
         用反引号实现：``     获取值：${ }

    3.箭头函数：  =>
 匿名函数：
function(item,index,arr) {

   console.log(arr)

}


 用   =>来取代匿名函数
  (形参1,形参2,.....) =>  {

      //代码块

 }

  arr.forEach((item,index,arr)=> {

   console.log(item)

});


#VUE