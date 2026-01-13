---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/stellabo/daily_report/issues/32/comments
created_at: '2026-01-13T14:28:54Z'
events_url: https://api.github.com/repos/stellabo/daily_report/issues/32/events
html_url: https://github.com/stellabo/daily_report/issues/32
id: 3809115961
issue_dependencies_summary:
  blocked_by: 0
  blocking: 0
  total_blocked_by: 0
  total_blocking: 0
labels: []
labels_url: https://api.github.com/repos/stellabo/daily_report/issues/32/labels{/name}
locked: false
milestone: 
node_id: I_kwDOKDBFSs7jCn85
number: 32
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
  url: https://api.github.com/repos/stellabo/daily_report/issues/32/reactions
repository_url: https://api.github.com/repos/stellabo/daily_report
state: open
state_reason: 
sub_issues_summary:
  completed: 0
  percent_completed: 0
  total: 0
timeline_url: https://api.github.com/repos/stellabo/daily_report/issues/32/timeline
title: 新しく買ったデスクトップPCでstable diffusionやってみた
updated_at: '2026-01-13T14:28:54Z'
url: https://api.github.com/repos/stellabo/daily_report/issues/32
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
  user_view_type: public

---

参考URL

WSL2での導入(venvで仮想環境作れば良かったかも?)
https://qiita.com/tadokuno/items/8812bc33d75afb9005af

LORAの導入
https://soroban.highreso.jp/article/article-051#6540c6770e4f0c1447c8c2e8-e4ba9fca8d11d19c0422afc6

GPUのバージョン上、上のURLでは動かなかったため、こちらのURLを参考にLORA環境を作り直した
https://elirlab.com/lora-cuda128-rtx50series/#google_vignette

なお、train.pyはsdxl_train_network.pyを指定した。