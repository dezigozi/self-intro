# 高野直樹 自己紹介図解

## 公開URL

**https://diagram-self-intro.surge.sh**

- **ポータル（トップ）**: https://diagram-self-intro.surge.sh/  
  ここから各バージョンに切り替えできます。

## フォルダ内のHTML

| ファイル | 説明 | 直リンク |
|----------|------|-----------|
| `index.html` | **ポータル**（アイコンで各版へ） | / |
| `self-intro_base.html` | もと / normal design（Professional Profile） | /self-intro_base.html |
| `self-intro_simple.html` | simple（図解ツールベース版） | /self-intro_simple.html |
| `self-intro_solid.html` | Solid design（Portfolio・ダーク） | /self-intro_solid.html |

各HTMLのフッターに公開URLのリンクを記載済み。

## Surge にデプロイする手順

公開サイト（https://diagram-self-intro.surge.sh/）を更新するには、次のいずれかを実行する。

### パターン1: self-intro フォルダの中で実行（推奨）

```bash
cd self-intro   # このリポジトリを clone した場所
npx --yes surge . diagram-self-intro.surge.sh
```

### パターン2: 親フォルダから self-intro を指定して実行

```bash
cd 親フォルダ   # self-intro がサブフォルダになっている場所
npx --yes surge self-intro diagram-self-intro.surge.sh
```

- 初回のみ Surge のログインを求められることがある。
- 成功すると **https://diagram-self-intro.surge.sh/** で公開される。
- 詳細は `手順書.md` の「3. デプロイ手順」を参照。

### main に push すると自動デプロイ（GitHub Actions）

`.github/workflows/deploy-surge.yml` により、**main ブランチへ push するたびに** 自動で Surge にデプロイされる。  
初回のみ、GitHub の **Settings → Secrets and variables → Actions** で `SURGE_TOKEN` を登録する必要がある。トークンはローカルで `npx surge token` で取得できる。詳しくは `手順書.md` の「3-2. main に push したら自動で Surge にデプロイする」を参照。

## サイトを削除するとき

```bash
npx surge teardown diagram-self-intro.surge.sh
```
