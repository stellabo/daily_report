---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/stellabo/daily_report/issues/6/comments
created_at: '2023-08-14T13:58:45Z'
events_url: https://api.github.com/repos/stellabo/daily_report/issues/6/events
html_url: https://github.com/stellabo/daily_report/issues/6
id: 1849832386
labels: []
labels_url: https://api.github.com/repos/stellabo/daily_report/issues/6/labels{/name}
locked: false
milestone: 
node_id: I_kwDOKDBFSs5uQjPC
number: 6
performed_via_github_app: 
reactions:
  "+1": 0
  "-1": 0
  confused: 0
  eyes: 0
  heart: 0
  hooray: 0
  laugh: 0
  rocket: 0
  total_count: 0
  url: https://api.github.com/repos/stellabo/daily_report/issues/6/reactions
repository_url: https://api.github.com/repos/stellabo/daily_report
state: open
state_reason: 
timeline_url: https://api.github.com/repos/stellabo/daily_report/issues/6/timeline
title: このブログの運用について
updated_at: '2023-08-15T05:37:50Z'
url: https://api.github.com/repos/stellabo/daily_report/issues/6
user:
  avatar_url: https://avatars.githubusercontent.com/u/46933816?v=4
  events_url: https://api.github.com/users/stellabo/events{/privacy}
  followers_url: https://api.github.com/users/stellabo/followers
  following_url: https://api.github.com/users/stellabo/following{/other_user}
  gists_url: https://api.github.com/users/stellabo/gists{/gist_id}
  gravatar_id: ''
  html_url: https://github.com/stellabo
  id: 46933816
  login: stellabo
  node_id: MDQ6VXNlcjQ2OTMzODE2
  organizations_url: https://api.github.com/users/stellabo/orgs
  received_events_url: https://api.github.com/users/stellabo/received_events
  repos_url: https://api.github.com/users/stellabo/repos
  site_admin: false
  starred_url: https://api.github.com/users/stellabo/starred{/owner}{/repo}
  subscriptions_url: https://api.github.com/users/stellabo/subscriptions
  type: User
  url: https://api.github.com/users/stellabo

---
このブログ(日報?)はr7kamuraさんのブログ記事『[GitHub Issuesでブログを書く](https://r7kamura.com/articles/2022-05-03-github-issues-as-blog)』より、gialogという機能を使って書いている。
通常のブログサービス(はてなブログとか)を使わない理由は、今後のためにGithubに慣れておきたいというのと、自分好みにカスタマイズできるブログ環境が欲しかったからだ。

https://r7kamura.com/articles/2022-05-03-github-issues-as-blog
でも以下のように書かれている。

>そこで「ボタンを押すだけでブログが出来上がり、使っている内に徐々に最近のウェブの技術を読み解いていけるようなものがあると良いのでは」と考え、今回こういうものをつくってみることにした。GitHubの使い方は学んでおいて損はないし、GitHub Issues、GitHub Actions、GitHub Pagesで完結するように実装すれば、GitHubのアカウントを用意してもらうだけで済む。

また、
>見た目を変更したいときは、リポジトリのソースコードを直接編集する。このブログは[Next.js](https://nextjs.org/)でつくられていて、ソースコードもチュートリアルに出てくるような簡単なものになっている。デフォルトだとブログタイトルが「My blog」になっているので、まずはここを変更することから始めるのが良いと思う。

とのことなので、基本的にはnext.jsとtypescriptについて学びつつ、少しずつ(**本当に少しずつ。数年ぐらい。**)自分の好みのサイトにカスタマイズしていくスタイルになると思う。
要するに盆栽。

今のところ考えている機能
- issue(日報)を書く際は、テンプレートを用意してそれを埋めていくスタイル 
- チェックボックスで達成できたタスクをチェックする(デイリーミッション)
    - ただし、基本的にタスクはissueに追加したくない




