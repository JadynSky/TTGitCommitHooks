# 🔑 钩子使用说明

### 提交规则

Add Jid 描述

Fix Jid 描述

Mod Jid 描述

OCT 描述

举例：
Add ZZZDCP-58 通过APP扫码登录平台（后台）



### :a: 提交时注释填写规则钩子
  1. **获取脚本文件**
      将本库中的项目clone到本地。

  2. **安装**

      全局git仓库配置:
      将下载的脚本文件`commit-msg`配置全局设置，全局设置之后，重新clone代码，钩子就可生效。
      配置方式：

      ``` 
      [root@liweiguang ~]# git clone -b version3 http://git.komect.net/devops/hooks.git
      [root@liweiguang ~]# mkdir -p ~/.git_template/hooks
      [root@liweiguang ~]# cp ./hooks/commit-msg ~/.git_template/hooks
      [root@liweiguang ~]# chmod u+x ~/.git_template/hooks/commit-msg
      [root@liweiguang ~]# git config --global init.templatedir ~/.git_template
      ```

      某个git仓库配置：

      将下载的脚本文件`commit-msg`放入本地已克隆的需要改规则的代码库根目录的`.git/hooks/`目录下。并保证该脚本文件的root权限，钩子将立刻生效。
      配置方式：

      ```
      [root@liweiguang ~]# git clone http://git.komect.net/group/project.git
      [root@liweiguang ~]# git clone -b version3 http://git.komect.net/devops/hooks.git
      [root@liweiguang ~]# cp ./hooks/commit-msg ./project/.git/hooks/
      [root@liweiguang ~]# chmod u+x ./project/.git/hooks/commit-msg 
      ```

  3. **添加push二次校验**

  4. **警告**
      :zap: ```适用项目,如本地commit时不按规则填写，则Push时将无法通过服务端对commit注释的二次校验，导致Push失败！```