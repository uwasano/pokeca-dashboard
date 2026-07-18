# pokeca-dashboard(限定公開ビューア)

ポケカ利益検知システムのダッシュボード閲覧用ページ(**実データのスナップショット**)。

- `index.html` は **AES-256 で暗号化済み**(StatiCrypt)。ログインするまで中身は復号されない。
- ログインは **メールアドレス + パスワード**(両方一致で表示)。
- これは取得時点の**静的スナップショット**。最新に更新するには、PCで「ポケカ相場チェック.bat」を
  実行して生成された `dist/dashboard.html` を暗号化し直し、この `index.html` を差し替える
  (担当のClaudeセッションに依頼)。
- システム本体(pokeca-profit)は別の**非公開**リポジトリで管理する。**このリポジトリに本体コードを置かないこと。**

## GitHub Pages 公開手順(ブラウザだけ)

1. github.com/new → リポジトリ名 `pokeca-dashboard` → **Public** → Create
2. 「uploading an existing file」→ この `index.html` と `README.md` をドラッグ → Commit
3. Settings → Pages → Branch: main / (root) → Save
4. 数分後 `https://<ユーザー名>.github.io/pokeca-dashboard/` で公開
