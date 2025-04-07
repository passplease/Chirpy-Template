# 这是啥
这是我从[Chirpy](Chirpy-README.md) Fork的静态网站的模板，并针对我的需求进行了改造，仅供我自己使用
# 怎么用
使用发布的Action，不过仓库的文件结构必须为如下结构，否则无法工作
```
仓库
└─ Chirpy
    ├── _config.yml
    ├── _posts/
    ├── common/
    ├── data/
    ├── _tabs/
    └── assets/img/
```
代码形如：
```yml
jobs:
  call-workflow-passing-data:
    uses: passplease/Chirpy-Template/.github/workflows/Deployer.yml@master
    with:
      repository: "Repository"
      send_email: ${{vars.SEND_EMAIL}}
    secrets:
      email_username: ${{secrets.EMAIL_USERNAME}}
      email_password: ${{secrets.EMAIL_PASSWORD}}
      email_recipient: ${{secrets.RECIPIENT_EMAIL}}
```
