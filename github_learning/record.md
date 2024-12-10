# 关于git和github的基本使用方法介绍
本篇文章是学习使用git和github工具的简单记录，初步掌握通过git在github上管理自己的文件数据的使用技巧。随着对相关知识的
学习的逐步深入，本篇文章内容会逐渐丰富，不断完善
- [x] 四个基本指令的使用 `clone` `commit` `push` `pull`
- [ ] 更复杂的指令及概念 `conflict` `branch` `merge` `GitIgnore`
- [ ] 其他工具的使用方法 `Github Desktop` `VScode Git`
## 一、如何给自己在Github上创建的仓库建立新的文件夹和文件

### （一）从Github上克隆仓库到本地
1. 选定/新建一个文件夹用来存放要准备克隆的仓库
2. 在这个文件夹下右键选择git bash打开终端
3. 在终端中输入以下指令就可以在该文件夹内克隆目标仓库
```
git clone http://github.com/your_username/your_repository.git
```
>*后面的网址可以在目标仓库界面点击code一键复制*

### （二）创建文件和文件夹
1. 进入克隆到本地的仓库内
2. 在这个文件夹下右键选择git bash打开终端
3. 在终端中输入以下指令分别创建文件夹和文件
```
>mkdir new_folder // 创建文件夹
<br>touch new-folder/your_file // 创建文件
```
>*这里可以自己新建文件夹或文件拖到仓库内*
<br>*Git本身只会跟踪文件而不会跟踪空文件夹，因此必须确保文件夹至少有一个文件*

### （三）提交并推送更改到Github/从Github上更新补全本地文件
1. 增加新内容
2. 提交修改声明
3. 推送到github
```
git add .
git commit -m "Add new folder and file"
git push origin main // 这里需要根据默认分支来推送
```
>*这里需要注意必须保证推送前没有文件缺失；否则需要先从github上更新补全本地文件，方法如下所示*
```
git pull origin main // 推拉指令都是在本地的仓库内打开git bash终端执行
```
<br>

## 二、如何通过Git在本地修改/删除文件并推送更改到Github

### （一）通过Git在本地修改文件并推送更改到Github
1. 增加新内容
2. 提交修改声明
3. 推送到github
```
git add .
git commit -m "Add new folder and file"
git push origin main // 这里需要根据默认分支来推送
```
>*在本地修改了文件后再推送更改到Github上方式与上文中的新建文件部分同理*

### （二）通过Git在本地删除文件并推送更改到Github
1. 删除文件/文件夹部分
2. 提交修改声明
3. 推送到github
```
git rm example.txt // 删除单一文件
git rm file1.txt file2.txt // 删除多个文件
git rm -r folder_name // 删除某个文件夹及内容
git rm *.log // 删除所有.log文件

git commit -m "Add new folder and file"
git push origin main // 这里需要根据默认分支来推送
```
>*在这里就明了了为什么修改或新增文件上传到Github前都要保证本地文件没有缺失，因为删除文件需要专门的指令*

- [ ] uncheck
- [x] 成功安装posh-git并在终端成功展示