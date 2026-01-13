---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/stellabo/daily_report/issues/23/comments
created_at: '2024-06-11T13:28:10Z'
events_url: https://api.github.com/repos/stellabo/daily_report/issues/23/events
html_url: https://github.com/stellabo/daily_report/issues/23
id: 2346443490
labels: []
labels_url: https://api.github.com/repos/stellabo/daily_report/issues/23/labels{/name}
locked: false
milestone: 
node_id: I_kwDOKDBFSs6L2-Li
number: 23
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
  url: https://api.github.com/repos/stellabo/daily_report/issues/23/reactions
repository_url: https://api.github.com/repos/stellabo/daily_report
state: open
state_reason: 
timeline_url: https://api.github.com/repos/stellabo/daily_report/issues/23/timeline
title: 2024/06/11
updated_at: '2024-06-11T16:09:56Z'
url: https://api.github.com/repos/stellabo/daily_report/issues/23
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
# デイリーミッション
- [x] ロボット関係1時間以上 
- [ ] 腹筋ローラー50回以上 
- [ ] スクワットorダンベル
- [ ] 絵を描く
- [ ] 日報更新


# 作業内容(進捗の証拠)

KRS2552の改造について考える

2552に使用されている、中身のアルミギアのスペックは公開されていない。
よって、自作でケースを作る際は地道な調整が必要だと思われる。
4000番のファイナルギヤと2552のファイナルギヤはモジュールが同じとのこと
2500番のファイナルではアーム固定用のネジ穴を開けれない。2552+4000ファイナルで検討

懸念点：モータ・制御回路に流していい電流値は?
どれだけトルクが上がっても、サーボに負荷がかかり、定格以上の電流を流し続けると燃える。
2552の基板を流用するとして、4000番のファイナルを繋げたり、別モータを繋げて大丈夫なのか?
やってみるしかない。

ステップ１：とりあえずモデリング

・KRS4000番系のファイナルギヤを買ってみる(何でもいいのか?)
・とりあえずケース含めモデリングを行う
・実際に出力し、組み込む
・未加工状態の歯車を組付け、回るかどうか確かめる
・問題なく動くことが分かったら、4000番のファイナルギヤにタップ穴をあける

ステップ2：アーム固定用のネジ穴を空ける
順当に考えるとボール盤
固定治具も考えないといけない
CNC買う?あるいは外部サービス?(値段が高くなるので、本末転倒)

ステップ3：トルク計測装置(重量計で良い?)でどのくらいのトルクが出るか調べる

ステップ4:モーターの変更を検討

最終的には、マイコンでサーボとLED、音声ICを連動させたいが、ICS3.5でそれができるかは不明

# 明日の作業予定


# 日記(何かあれば)
