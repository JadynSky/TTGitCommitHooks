<p>提交规则</p>
<p>Add Jid 描述</p>
<p>
<p>Fix Jid 描述</p>
<p>
<p>Mod Jid 描述</p>
<p>
<p>OCT 描述</p>
<p>
<p>举例：</p>
<p>Add ZZZDCP-58 通过APP扫码登录平台（后台）</p>
# :key: 钩子使用说明
### :a: 提交时注释填写规则钩子
  1.  **获取**
      <p>获取钩子脚本 **【[commit-msg](commit-msg)】** ,  这个脚本在Git库 hooks 中: 【[http://git.komect.net/devops/hooks]()】，如果无法单个文件进行下载，可以克隆整个库到本地。</p>
  2.  **安装**
      <p>将下载的脚本 【[commit-msg](commit-msg)】 , 配置全局设置，全局设置之后，重新clone代码，钩子才可生效。**推荐此种配置方法**。详见第五节：示例一。</p>
      <p>或</p>
      <p>将下载的脚本 【[commit-msg](commit-msg)】 ,  放入本地已克隆的需要改规则的代码库根目录的**【.git/hooks/】**目录下。并保证该脚本文件具有可执行权限，钩子将立刻生效。详见第五节：示例二。</p>
  3.  **使用**
      <p>填写规则同Subversion已在用规则。使用中如有问题，可以随时联系GitLab管理员：**@zhangyifei**</p>
  4.  **警告**
      <p>:zap: ```适用项目,如本地commit时不按规则填写，则Push时将无法通过服务端对commit注释的二次校验，导致Push失败！```</p>
  5.  **示例**

      示例一
>     [root@liweiguang ~]# git clone -b version3 http://git.komect.net/devops/hooks.git
>     [root@liweiguang ~]# mkdir -p ~/.git_template/hooks
>     [root@liweiguang ~]# cp ./hooks/commit-msg ~/.git_template/hooks
>     [root@liweiguang ~]# chmod u+x ~/.git_template/hooks/commit-msg
>     [root@liweiguang ~]# git config --global init.templatedir ~/.git_template

      示例二
>     [root@liweiguang ~]# git clone http://git.komect.net/group/project.git
>     [root@liweiguang ~]# git clone -b version3 http://git.komect.net/devops/hooks.git
>     [root@liweiguang ~]# cp ./hooks/commit-msg ./project/.git/hooks/
>     [root@liweiguang ~]# chmod u+x ./project/.git/hooks/commit-msg  