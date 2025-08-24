---
active_lock_reason: 
assignee: 
assignees: []
author_association: OWNER
closed_at: 
comments: 0
comments_url: https://api.github.com/repos/stellabo/daily_report/issues/22/comments
created_at: '2024-06-10T11:36:58Z'
events_url: https://api.github.com/repos/stellabo/daily_report/issues/22/events
html_url: https://github.com/stellabo/daily_report/issues/22
id: 2343674294
labels: []
labels_url: https://api.github.com/repos/stellabo/daily_report/issues/22/labels{/name}
locked: false
milestone: 
node_id: I_kwDOKDBFSs6LsaG2
number: 22
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
  url: https://api.github.com/repos/stellabo/daily_report/issues/22/reactions
repository_url: https://api.github.com/repos/stellabo/daily_report
state: open
state_reason: 
timeline_url: https://api.github.com/repos/stellabo/daily_report/issues/22/timeline
title: 2024/06/10
updated_at: '2024-06-10T11:36:59Z'
url: https://api.github.com/repos/stellabo/daily_report/issues/22
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
- [ ] ロボット関係1時間以上 
- [ ] 腹筋ローラー50回以上 
- [ ] スクワットorダンベル
- [ ] 絵を描く
- [ ] 日報更新


# 作業内容(進捗の証拠)

前回は足にサーボを埋め込む難しさを述べたが、依然として問題は解決していない。
まず段階を踏んで、サーボに求められる最低限のスペックについて調べることにした。

![image](https://github.com/stellabo/daily_report/assets/46933816/7491f905-d216-4f17-9259-601fb798d187)

というわけで、ゲーム画面を参考に、見よう見まねモデリングを行った。
このモデルを参考に、全体のサイズ感や重量を決めていく。
まず、サイズ感であるが、モデリングが終了した段階で、
高さ250mm、幅316mm、奥行き500mmとなった。サイズとしてはかなり大きめになってしまったが、
後述するモータサイズの観点からすると、正直これでも足りないくらいである。

![image](https://github.com/stellabo/daily_report/assets/46933816/c1e629e1-5ed0-4ea5-a4ad-20bc9ce8f138)

重量は、全身鋼で20㎏である。勿論、全身鋼にしたらめっちゃ高くなるし加工も難しいわで非現実的なので、
3Dプリンタでの製作を想定して、ABS樹脂とする。
ABS樹脂の密度はおおよそ0.0013であることから、÷6をすると、おおよその重さが出てくる。
20/6=3.3kgとなるが、まだモデリングできていない武装があったり、モータやバッテリ等の重量も含んでいないため、
将来的な重量はおおよそ5kgとなる見通しである。

サーボモータの選定
市販のサーボモータには様々な種類があります。以下を基準に、採用するサーボモータを検討した。
・トルク
・価格

1.トルクはどれだけの力でモーターを動かせるかという値で、大きいほど動作の安定につながる。
一方で、高トルクのサーボモータは消費電力も重量も大きい傾向にある。

2.サーボモータの価格は種類によって様々で、一個あたり数百円から数千円である。
今回作成するラジコンでは、足だけでも軸数（3軸）×足数（4本）=12個と、多数のサーボモータが必要になる。
我が部もミレニアムの鬼会計によって予算が減少傾向にあるため、あまり高価なものは予算の都合上使用できない。


トルク計算について：

サーボモータの必要トルクは、以下の数式で算出できる。
必要トルク[kg-cm]=ロボット重量[kg]×リンク長[cm]×マージン[安全率]

安全率に関して：
サーボモータは常に最大トルクを出し続けてはいけないので、余裕を持たせて設計する必要がある。
安全率は1.5が理想だが、今回はそこまで激しい動きをさせるつもりもないため、1.2～1.3とする。

よって、
必要トルク=5[kg]×4[cm]×1.3=26[kg.cm]となる。

この条件にあてはまるサーボモーターだが、ざっと見た感じ、以下の２つとなる。
![image](https://github.com/stellabo/daily_report/assets/46933816/2ef7c1cb-477f-433f-90cd-1061c04f63f0)
![image](https://github.com/stellabo/daily_report/assets/46933816/5926df64-dba6-47af-a568-54c0583c7127)

特に、krs4033はトルクにも余力があり、サイズも大き目ではあるが、工夫すればギリギリ足に収まらなくもない。
![image](https://github.com/stellabo/daily_report/assets/46933816/5867cd82-2591-4281-ae3e-bbdf4befaeca)

しかしながら、値段が1個一万円と、異様に高い。(ちなみにkrs2572も同じくらいの値段)
これを使用したいのは山々であるが、どうしようもなくなった時の最終手段としておくべきだろう。

それ以外の対策となると、「歩き方を工夫する」が挙げられる。

モデルを見れば分かる通り、ゲブラには合計で4本の脚が存在する。
脚が複数あるということは、その分だけ荷重を分散して支えることができるはずである。
ここで、脚が地面に常に2本以上接するようモーションを作成すれば、脚1本あたりにかかる荷重は単純計算で
2.5kgとなるため、
必要トルクは単純計算で13[kg・cm]まで減少する。
これであれば、このサーボが使用できる。
![image](https://github.com/stellabo/daily_report/assets/46933816/4ef757b7-d77c-4288-b3d0-741c63c0d629)

このkrs2552は、前述したサーボと比べるとトルクこそ小さいが、特殊なルート(ブラックマーケットではない)を使用することで、1個あたり1000円で買える。そのため、たとえ壊したとしても罪悪感はないし、躊躇なく分解もできる。

実際にこのモータで本当にうまくいくかは分からないが、一度このモータを使うことを検討し、ダメそうなら最終手段として
1個1万円のモータを使うことを検討したいと思う。

# 明日の作業予定


# 日記(何かあれば)
