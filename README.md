# studyNotes


## git配置核心步骤及遇到的问题
- 配置用户名和邮箱，参考:[git安装教程及环境配置](https://www.cnblogs.com/qkq505/p/15316884.html)  
  ```
  git config --global user.name "自己的用户名"
  git config --global user.emal "自己的邮箱"
  ```
- 生成ssh公钥(id_rsa_github为自定义的名字)，参考:[git本地仓库连接到多个远程仓库](https://www.cnblogs.com/tgkjy/p/15184043.html)  
  `ssh-keygen -t rsa -f id_rsa_github -C "yourmail@xxx.com"`
- 将生成的公钥配置到[Settings - Access - SSH and GPG keys - SSH keys](https://github.com/settings/keys)  
- 在~/.ssh文件夹下创建一个名字为config的文件，无后缀名，参考:[解决 git 上传:  Failed to connect to github.com port 443: Timed out](https://www.cnblogs.com/greentomlee/p/14613993.html)  
  ```
  Host github.com
  User git
  Hostname github.com
  PreferredAuthentications publickey
  IdentityFile ~\.ssh\id_rsa_github
  Port 443
  ```
- 生成Personal access tokens，参考:[git报错：remote: Support for password authentication was removed on August 13, 2021.](https://www.cnblogs.com/yutian-blogs/p/15548819.html)
- 从git下载的代码库都需要更改remote url  
  `git remote set-url origin https://<你的令牌>@github.com/<你的git用户名>/<要修改的仓库名>.git`  
  对于此库: `git remote set-url origin https://<令牌>@github.com/leiyupuya/studyNotes.git`