# 高野直樹 自己紹介図解

## 公開URL

**https://diagram-self-intro.surge.sh**

- **ポータル（トップ）**: https://diagram-self-intro.surge.sh/  
  ここから各バージョンに切り替えできます。

## フォルダ内のHTML

| ファイル | 説明 | 直リンク |
|----------|------|-----------|
| `index.html` | **ポータル**（アイコンで各版へ） | / |
| `self-intro_base.html` | 図解ツールベース版 | /self-intro_base.html |
| `self-intro_gemini1.html` | Gemini版1（Professional Profile） | /self-intro_gemini1.html |
| `self-intro_gemini2.html` | Gemini版2（Portfolio・ダーク） | /self-intro_gemini2.html |

各HTMLのフッターに公開URLのリンクを記載済み。

## デプロイするとき（ポータル＋全HTMLを公開）

プロジェクトルートで実行し、**self-intro フォルダごと**デプロイすると、トップがポータルになり各HTMLに切り替え可能です。

```bash
cd "/Users/dezigozigmail.com/Dropbox/会社/仕事/マイドキュメント/Ｍ／G/生産性向上(働き方改革)/AI/■PB/AI School/creating-visual-explainers"
npx --yes surge self-intro diagram-self-intro.surge.sh
```

## サイトを削除するとき

```bash
npx surge teardown diagram-self-intro.surge.sh
```
