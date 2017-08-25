## github 从本地仓库上传项目到远程仓库命令行

1. Command line instructions(命令指令行)
Git global setup(先设置git全局设置)    #如果以前设置过则可以忽略
git config --global user.name "张三"   #设置git用户名
git config --global user.email "collinswang@21cn.com"    #设置git用户邮箱

# 方法一:(从零开始新建本地仓库,将远程文件clone下来)
Create a new repository     #本地新建仓库

git clone git@github.com/genghongkai/HKNote.git  #将远程git仓库文件clone至本地新建仓库
cd front                                    #切换至新建的分支
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
# 方法二:
Existing folder     #已经存在文件夹(此目录之前未建立过远程git仓库连接)

cd existing_folder     #切到已存在的目录下
git init                      #初始化git
git remote add origin git@github.com/genghongkai/HKNote.git     #建立远成仓库连接
git add .                  #添加文件
git commit              #提交
git push -u origin master    #push到远程仓库

# 方法三:
Git repository    #已经存在的git仓库分支

cd existing_repository_folder     #切到已存在的git分支的目录下
rm -rf .git                          #删除该分支之前的git配置
git init                            #初始化git
git remote add origin git@github.com/genghongkai/HKNote.git     #建立新的远成仓库连接
git add .                  #添加文件
git commit              #提交
git push -u origin master    #push到远程仓库

### 提交时错误总结
1.$ git remote add origin git@github.com/genghongkai/HKNote.git 
错误提示：fatal: remote origin already exists.   //远程仓库已经存在
解决办法：$ git remote rm origin   //移除远程仓库
然后在执行：$ git remote add origin git@github.com/genghongkai/HKNote.git 就不会报错误了 
2. $ git push origin master   //提交
错误提示：error:failed to push som refs to 
解决办法：$ git pull origin master //先把远程服务器github上面的文件拉先来，再push 上去。 
3.强制提交提交
解决办法: $ git push -u origin master -f 

