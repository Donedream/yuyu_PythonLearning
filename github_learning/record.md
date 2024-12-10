# 关于git和github的基本使用方法介绍

## 1.如何给自己在github上创建的仓库建立新的文件夹和文件
    
### 从github上克隆仓库到本地
- 选定/新建一个文件夹用来存放要准备克隆的仓库
- 在这个文件夹下右键选择git bash打开终端
- 在终端中输入以下指令就可以在该文件夹内克隆目标仓库
```
git clone http://github.com/your_username/your_repository.git
```
*注：后面的网址可以在目标仓库界面点击code一键复制*
### 创建文件和文件夹
- 进入克隆到本地的仓库内
- 在这个文件夹下右键选择git bash打开终端
- 在终端中输入以下指令分别创建文件夹和文件
```
>mkdir new_folder // 创建文件夹
<br>touch new-folder/your_file // 创建文件
```
*注：这里可以自己新建文件夹或文件拖到仓库内；但是必须保证新建文件夹里至少有一个文件*
### 提交并推送更改到github/修改本地内容推送到github同理
- 增加新内容
- 提交修改声明
- 推送到github
```
git add .
git commit -m "Add new folder and file"
git push origin main // 这里需要根据默认分支来推送
```
*注：这里需要注意必须保证推送前没有文件缺失；否则需要先从github上更新补全本地文件，方法如下所示*
```
git pull origin main // 推拉指令都是在本地的仓库内打开git bash终端执行
```