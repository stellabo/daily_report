---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/stellabo/daily_report/issues/31/comments
created_at: '2025-08-31T07:07:01Z'
events_url: https://api.github.com/repos/stellabo/daily_report/issues/31/events
html_url: https://github.com/stellabo/daily_report/issues/31
id: 3369920125
issue_dependencies_summary:
  blocked_by: 0
  blocking: 0
  total_blocked_by: 0
  total_blocking: 0
labels: []
labels_url: https://api.github.com/repos/stellabo/daily_report/issues/31/labels{/name}
locked: false
milestone: 
node_id: I_kwDOKDBFSs7I3OZ9
number: 31
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
  url: https://api.github.com/repos/stellabo/daily_report/issues/31/reactions
repository_url: https://api.github.com/repos/stellabo/daily_report
state: open
state_reason: 
sub_issues_summary:
  completed: 0
  percent_completed: 0
  total: 0
timeline_url: https://api.github.com/repos/stellabo/daily_report/issues/31/timeline
title: 進捗報告8月号
updated_at: '2025-08-31T09:03:26Z'
url: https://api.github.com/repos/stellabo/daily_report/issues/31
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
先日、自分が設計した回路を発注したので、この機会に進捗報告してみる。
7月末まで海外出張に行っており、8月は空いた分の仕事の埋め合わせ(?)をしたり、
お盆は予定が重なってずっと遊んでたりと、今月は思った以上に作業時間が確保できなかった。


そんなこんなで、空いている時間で何とか作業を継続している。
今回は久しぶりに、回路設計をした。
ロボット活動自体は細々ながら継続しているが、最近は既製品のキットを使っており、
回路を設計したのは大学3年生以来5年ぶりとなる。
久しぶりで回路製作に自信が無いこともあって、
大学のサークルに所属していた頃に動作した、実績のある回路を参考に作った。
本来であれば、自分で考えて設計するのが理想ではあるが、
時間があまり無いのと、「動いてくれたらいいや」という投げやりな方針もあり、
このようなかたちで進めることにした。

----
以下、回路の解説

まず、全体システムの概略図を示す。
![システム図](https://i.imgur.com/b39beHC.png)
やってることは単純で、
3セルの電源をDCDCコンバーターで5Vに変換した後、
マイコンやモーター・LED等の各モジュールに電圧を供給している。
コントローラーからの入力を受け、マイコンは各モジュールと通信を行い、
各モジュールが動作してロボットが動く。


そして、設計した回路はこちら
![回路図](https://i.imgur.com/wzrpEB6.png)

回路としては非常に初歩的で、特筆すべき点は無いが、
自分に理解の為に、各部について手短に解説する。



