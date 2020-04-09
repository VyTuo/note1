# git

## git 凭证

1.  查看凭证

    1.  `$ ~` : 查看全局配置文件文字

        1.  File: .gitconfig -> 配置信息

        2.  File: .git-credentials -> 存储账号密码

            1.  https://account:password@github.com

    2.  `$ git config --list` : 查看配置信息

    3.  `$ git config --list | grep credential` : 查看凭证（默认 `credential.helper=manager`）

    4.  `$ git config --global user.name [name]` : 无 name 获取全局名称，有 name 设置全局名称

    5.  `$ git config --local user.name [name]` : 无 name 获取本地名称，有 name 设置本地名称

    6.  `$ git config user.name [name]` : 无 name 获取当前使用的名称，有 name 设置本地名称

    7.  email : 同上，name 修改为 email

2.  添加凭证 - Git

    1.  `$ git config --global credential.helper store`

3.  添加凭证 - TortoiseGit

    1.  右键 TortoiseGit(T) -> setting(S)

    2.  选中 Git -> 编辑全局.git/config(O) -> File: .gitconfig 添加代码

        ```
        [credential]
            helper = store
        ```

    3.  拉代码第一次还是需要输入密码，但是接下来会保存在 File: .git-credentials 里面

4.  删除凭证

    1.  File: .git-credentials 暴力删除

## Git 本地凭证

1.  `$ git init`: 初始化

2.  设置本地名称和邮箱

3.  本地的账号密码也保存在 File: .git-credentials 里面，和全局的放在一起
