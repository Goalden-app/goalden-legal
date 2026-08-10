# Goalden — 利用規約とプライバシーポリシー

App Store と Google Play は、どちらも「**Web 上に公開された** 規約の URL」を要求する
（アプリ内に表示があるだけでは審査を通らない）。このリポジトリはそのための公開場所。

- プライバシーポリシー — https://goalden-app.github.io/goalden-legal/privacy.html
- 利用規約 — https://goalden-app.github.io/goalden-legal/terms.html

## 更新のしかた（重要）

**このリポジトリの HTML を直接編集しないこと。** 次の更新で上書きされ、
さらにアプリ内の表示と食い違って審査の差し戻し・法的リスクにつながる。

本文の原本はアプリ側にある:

- `Goalden/app/src/legal/privacy.ts`
- `Goalden/app/src/legal/terms.ts`

原本を直したあと、Goalden リポジトリで次を実行すると、ここの HTML が作り直される:

```
node scripts/build-legal-site.mjs
```

そのうえで、このリポジトリでコミットする（push は自動で行われる。
`scripts/git-hooks/post-commit` 参照）。数分後に上の URL へ反映される。

## なぜ公開リポジトリなのか

GitHub Pages（無料の Web 公開機能）を使うため。
置いてあるのは誰でも読める規約の文章だけで、アプリのコードや経営文書は
別の Private リポジトリ（`goalden`）にある。
