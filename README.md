<img width="740" alt="スクリーンショット 2024-02-19 20 05 13" src="https://github.com/iwatanabee/Idea-memory/assets/83575309/e12862cc-cc28-4694-a7e6-33d628db8a1c">

## このサービスについて
<img src="https://github.com/iwatanabee/Idea-memory/assets/83575309/492b3cb2-7943-4305-9c91-2b4c836bc469" width="100" height="100">  

**「アイデア出しをもっとスムーズに」**  
という思いがあり、このサービスを製作しました。 
Idea Memory (Imemo)とは、アイデア出しをサポートするWebサービスです。
主な機能として、マンダラートを作成することができます(他の機能も随時追加して行きます)。
自分のマンダラートを作成・保存・pdfでPCに保存できます。
気軽に体験してもらえるために、トップページでもマンダラートを作成できるようにしました。ぜひ使ってみてください。

## 作成の背景
<img width="100" src="https://github.com/iwatanabee/Idea-memory/assets/83575309/243b3a3b-50ea-4241-bcce-21e17a6f5d6b" style="display: flex;justify-content: center;">

現在大学生で、インターンやハッカソンで、ゲームやWebサービスを作っているが、アイデアを出すのにすごく時間がかかってしまうため、スムーズにアイデアが出せるWebサービスを作りたかった。
また、インターンの研修で、マンダラートを用いたアイデア出しを行ったが、みんなが共通で思っていた不便な点がいくつかあった。

- 紙と鉛筆で書くのは、正直面倒
- 中央のマスに書いたことを、外側のマスに書かないといけない→めっちゃめんどくさい
- 全てのマスを埋められない泣
- 共同で作業をしたい

これらの問題をWebサービスで解決できたら、いいサービスになるのではないかと考え、まずはインターンで使用したマンダラートをWebで作成してみることにした。
ちょうど就活の時期なので、マンダラートで自己分析をして、面接官に「自分が作ったサービスで自己分析しました」と言えば、ウケるのではないかと考えた。
最終的には、他のアイデア出しの手法も導入できたらいいと考えています（ジョハリの窓やオズボーンのチェックリストなど）。

## 使い方
- 開発のアイデア出しが簡単にできる
- 就活の自己分析や目標決めに利用できる
- いろいろなアイデアだしの手法が一つのWebサービスで使用できる


## サービスの機能一覧

## 工夫した点
### pdf保存機能のデザイン設定  
<img width="50%" src="https://github.com/iwatanabee/Idea-memory/assets/83575309/7d763a56-04bb-494e-a97d-a18483586da4">
<!-- <img width="10%" src="https://github.com/iwatanabee/Idea-memory/assets/83575309/6a1e6161-5766-4edf-9adf-1ca3048655c3"> -->
→
<img width="40%" alt="スクリーンショット 2024-02-19 21 14 33" src="https://github.com/iwatanabee/Idea-memory/assets/83575309/a68eca54-9df2-40a3-83a2-0374a909edaa">  

作成したマンダラートをpdfで保存できるようにしました。  
また保存するときに、マンダラートとロゴのみをpdf保存できるように(右上の画像)Webサービス側とpdf保存する側でデザインを変えて実装しました。

## 課題
### ユーザー側の課題
- [x] 紙と鉛筆で書くのは、正直面倒  
      → Webサービスにしてデジタル化する。
- [x] 中央のマスに書いたことを、外側のマスに書かないといけない  
      → 自動入力機能を作成。同じことを書くマスを片方書くと、もう片方のマスに反映されるようにした。
- [x] マンダラートを紙で持っていきたい  
      → pdf保存機能を作成。PCにマンダラートのpdfを保存できるようなボタンを作った。
- [ ] 全てのマスを埋められない  
      → 周りのマスの情報から、AIを使って単語を埋めようと思う。
- [ ] 共同で作業をしたい  
      → 共同作業できるようにリアルタイムで通信できるようにする→具体的な方法はまだわからない
### 技術的な課題
- [ ] マンダラートを読み込むとき、変更を保存するときに重くなる  
      → チューニングをして、スムーズに値が取れるようにする
- [ ] なんかサイトが全体的に重い  
      → 
- [ ] SQL文の見直し  
      → N+1問題を起こす命令の確認  
      LB, APP, DBサーバー間のネットワーク環境の確認/nginxやApacheなどのサーバーソフトウェアの設定値等の確認/SQL文の見直し（N+1問題を引く起こすクエリはないかなど）

## ほかのサービスとの差別化
- マンダラートを作成できるWebサイトがあったが、全部入力しないときれいなマンダラートを作れないことやログイン機能がないことが問題だった。  
  → 最初から81個のマスを用意し、それを表示　＆　ログイン機能を作成
- そもそもマスが小さすぎて、スマホでの作業に向いていない  
  → スマホを横にして作業ができるようにデザインを工夫した。

