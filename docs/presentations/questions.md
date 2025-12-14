---
marp: true
theme: default
paginate: true
header: 'AI Challenge 2025'
---

<style>
blockquote {
  position: absolute !important;
  bottom: 20px !important;
  left: 40px !important;
  font-size: 0.5em !important;
  border-left: 3px solid #ccc !important;
  text-align: left !important;
  background: transparent !important;
  padding-left: 10px !important;
  margin: 0 !important;
  color: #666 !important;
  width: auto !important;
  max-width: 40% !important;
}
blockquote::before {
  content: none !important;
  display: none !important;
}
blockquote::after {
  content: none !important;
  display: none !important;
}
blockquote p {
  margin: 0 !important;
  padding: 0 !important;
  line-height: 1.4 !important;
}
</style>

<!-- _class: lead -->
# How to ask questions to collaborator

AI Challenge 2025

---

## 目次

1. We are collaborator
2. Not Teacher, But Collaborator
3. How to ask **concise** questions
4. 効果的な質問のTips
5. GitHub Issueの活用

---

<!-- _class: lead -->
# 1. We are collaborator

---

## We are **collaborator**

### Not teacher, Not TA

---

<!-- _class: lead -->
# 2. Not Teacher, But Collaborator

---

## Teacher の場合

### Teacherの特徴

- ✅ あなたが使っているシステムについて詳しい
- ✅ 時間のマネジメントはteacherの責任
- ✅ あなたの進捗状況を把握している

### 質問スタイル

- 詳細な説明なしでも理解してもらえる
- 時間をかけて質問できる

---

## collaborator の場合

### collaboratorの特徴

- あなたが**そもそも何をしたいのか知らない**
- あなたの**ゴールは何なのか知らない**
- あなたが**どこまでわかっているのか知らない**
- あなたのシステムについては**詳しくないかもしれない**

### 必要なこと

- 📝 簡潔な説明を添える必要がある
- 🎯 背景とゴールを明確に伝える

---

<!-- _class: lead -->
# 3. How to ask **concise** questions

---

## 質問はためらわず、でも**簡潔**に！

### なぜ簡潔にする必要があるのか？

1. **他の人への配慮**
   - 長く聞くと他の人が質問できない

2. **collaboratorへの配慮**
   - 長く聞くとcollaboratorの時間が奪われる

3. **自分自身のため**
   - まとめることで理解が深まる

---

## 質問をまとめるプロセス

### 1. まずは自分のためにまとめる

- **疑問点をまとめる**
- **やったこと、わかったこと**を整理

### 2. 次に相手のためにまとめる

- 自分のシステムをどう説明すれば、**相手にとって**わかりやすいか考える
- 自分のシステムについて、どう**抽象化**して伝えるか考える

---

<!-- _class: lead -->
# 4. 効果的な質問のTips

---

## 視覚化を活用する

### 図にしよう

- **draw.io** や **Mermaid** で図を作成
- システムの構成を視覚的に説明
- データフローを明確に示す

### 例

```mermaid
graph LR
    A[センサ] --> B[処理]
    B --> C[制御]
```

図があると、複雑なシステムも理解しやすい！

---

## 構造化された質問フォーマット

### Well Structured な形式にまとめる

1. **何をしたいか** (Goal)
   - 最終的に達成したいこと

2. **何が課題か** (Problem)
   - 現在直面している問題

3. **何を試したか、その結果どうなったか** (Attempted Solutions)
   - 試したアプローチと結果

4. **具体的な情報**
   - ROSBAG dataへのlink, スクリーンショット, エラーログ

---

## BackgroundとQuestionを分ける

### Background（背景情報）

- システムの概要
- 使用している技術スタック
- これまでの経緯

### Question（質問内容）

- 具体的に知りたいこと
- 期待する結果
- どんな助けが必要か

**明確に分けることで、相手が理解しやすくなる**

---

## LLMを活用する

### 質問文を短くする

長い質問文を書いた後：

1. ChatGPTやGemini等のLLMに入力
2. 「この質問を簡潔にまとめてください」「質問相手はこの点まで理解していると想定しています」と依頼
3. 重要なポイントだけを抽出して質問

---

<!-- _class: lead -->
# 5. GitHub Issueの活用

---

## GitHub Issueで質問を管理

### なぜGitHub Issue？

- 📝 履歴が残る
- 🔗 リンクで共有しやすい
- 💬 非同期でコミュニケーションできる
- 🏷️ ラベルで分類できる

### 基本ルール

**大きな質問一つごとに、GitHub issueを立てる**

小さな質問を一つのissueにまとめない

---

## GitHub Issueのテンプレート例

```markdown
## Goal（何をしたいか）
- TinyLiDARNetで周回タイムを10秒短縮したい

## Problem（何が課題か）
- カーブでの速度が遅すぎる
- LiDARデータが正しく取得できていない可能性

## Attempted Solutions（試したこと）
1. 学習データを2倍に増やした → 効果なし
2. 学習率を0.001→0.0001に変更 → わずかに改善

## Additional Information
- ROSbag: [link]
- スクリーンショット: [image]
- ログ: [error.log]

## Question
どのようにデバッグすれば良いでしょうか？
```

---

## 良い質問の例

### ✅ Good Example

```
【Goal】
TinyLiDARNetでOvertakeを実現したい

【Problem】
他車両を検知はできるが、回避軌道が生成されない

【Tried】
- データ量: 1万→2万サンプルに増加
- Result: 検知精度は向上、回避動作は未実装のまま

【Question】
回避軌道の生成にはどのようなアプローチが有効でしょうか？
```

---

## 悪い質問の例

### ❌ Bad Example

```
動きません。助けてください。
```

### 何が問題？

- ❌ 何をしたいのか不明
- ❌ 何が起きているのか不明
- ❌ 何を試したのか不明
- ❌ どんな助けが必要なのか不明

---

<!-- _class: lead -->
# まとめ

---

## まとめ

### Key Points

1. **We are collaborator** - 教師ではなく仲間として接する
2. **簡潔な質問** - LLMを活用
3. **視覚化する** - 図を使ってわかりやすく説明
4. **構造化する** - Goal, Problem, Solutions, Question
5. **GitHub Issueを活用** - 履歴を残して効率的に管理

### One Message

**LLMの手を借りて、簡潔かつ構造化された質問をしよう！**

---

<!-- _class: lead -->
# Thank you!

## Questions?

どんな小さな疑問でも、構造化して質問してみよう！
