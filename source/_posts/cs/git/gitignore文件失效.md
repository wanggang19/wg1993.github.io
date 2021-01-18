title: gitignore文件失效
date: 2021-01-17 00:00:01
categories:
- [计算机科学, git命令]
tags:
- git
---
# 问题
.idea文件已经被添加到.gitignore文件中，git提交依然会涉及
# 原因
.gitignore只能忽略那些原来没有被track的文件，如果某些文件已经被纳入了版本管理中，则修改.gitignore是无效的
<br/>
# 解决方法
```bash
git rm -r --cached .
git add .
git commit -m 'update .gitignore'
```