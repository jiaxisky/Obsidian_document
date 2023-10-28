<iframe src="https://www.liaoxuefeng.com/wiki/896043488029600/898732864121440" allow="fullscreen" allowfullscreen="" style="height:100%;width:100%; aspect-ratio: 16 / 9; "></iframe>
[[git]]
  ##  git 上传所有新文件
```
   git add -A
   git commit -a -m"上传所有文件"
```

 推送到远程仓库
```
   git push -u origin master
```
## 1.怎么看git是否连接了GitHub和Gitee
### 测试是否连接成功
github：
```
ssh -T git@github.com
```
gitee ：
```
ssh -T git@gitee.com
```
<iframe src="https://blog.csdn.net/apple_51931783/article/details/128387863" allow="fullscreen" allowfullscreen="" style="height: 100%; width: 100%; aspect-ratio: 1 / 1;"></iframe>

如果你clone下来一个别人的仓库，在此基础上完成你的代码，推送到自己的仓库可能遇到如下问题：
## error: remote origin already exists.表示远程仓库已存在。
因此你要进行以下操作：
1、先输入git remote rm origin 删除关联的origin的远程库
2、关联自己的仓库 git remote add origin https://gitee.com/xxxxxx.git
3、最后git push origin master，这样就推送到自己的仓库了。
## 添加远程仓库
```
$ git remote add origin git@github.com:jiaxisky/obsidianworkspace.git
```
# warning: in the working copy of ‘package-lock.json‘, LF will be replaced by CRLF the next time Git
换行符的问题，Windows下换行符和Unix下的换行符不一样，git会自动转换，但是这样有问题，所以解决方法如下：
使用命令，禁止自动转换：
git config --global core.autocrlf false
#  2.关于git完之后本地文件消失的解决方法
<iframe src="https://blog.csdn.net/LINJUN0423/article/details/127495704?spm=1001.2101.3001.6650.1&amp;utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-127495704-blog-113784621.235%5Ev38%5Epc_relevant_anti_vip_base&amp;depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1-127495704-blog-113784621.235%5Ev38%5Epc_relevant_anti_vip_base&amp;utm_relevant_index=2" allow="fullscreen" allowfullscreen="" style="height: 100%; width: 100%; aspect-ratio: 4 / 3;"></iframe>
# 三、删除远程仓库
1使用以下命令删除远程仓库：
1
git remote rm origin
2.确认已经删除：
git remote -v
