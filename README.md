# oni-remind-config

鬼リマインド用configファイル

https://github.com/gpioblink/oni-remind を使用するための設定用ファイルの例です。

※ webhookのURL等が含まれるため、必ずプライベートリポジトリとして作成してください。

# notification methods.yml

現在、providerはslack-webhookのみ対応しています。

methods以下に重複しないキーで次のように書けば、何件でも通知先を追加できます。

```
methods:
  lab-slack-random:
    provider: slack-webhook
    url: "https://hooks.slack.com/services/***"
  circle-slack-z-channel:
    provider: slack-webhook
    url: "https://hooks.slack.com/services/***"
```

# reminders.yml

reminders以下に重複しないキーで次のように書けば、何件でも通知先を追加できます。

```
reminders:
  zli-todo-remind:
    repo: my_user_name/repo1
    method: lab-slack-random
  lab-slack:
    repo: my_user_name/repo2
    method: circle-slack-z-channel
```