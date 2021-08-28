## 実行準備
hosts
```
[target]
18.183.192.11

[target:vars]
ansible_ssh_port=22
ansible_ssh_user=ec2-user
ansible_ssh_private_key_file=~/.ssh/common_key.pem
```

group_vars/target
```
__working_user:       <実行ユーザ名>
__pj_name:            <プロジェクト名(アプリケーション名)>
__git_repo_url:       <githubのリポジトリURL>

```

## 実行
```
$ ansible-playbook -i hosts site.yml
```

## roles
### nginx
    nginxのインストール
    nginxのスタート、自動起動


### rails
    ~~nginxの実行ユーザを変更~~
    gitからプロジェクトファイルを取得
    ~~/etc/nginx/conf.d配下にrails.dを配置~~

### bundle
    bundle installの実行
    ~~asset:precompireの実行~~

