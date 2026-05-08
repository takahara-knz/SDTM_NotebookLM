# SDTM_NotebookLM

NotebookLMを使ってSDTMチャットボットを構築するためのレポジトリです。

## 📁 構成

- SDTMやSDTMIGなどのドキュメントは、[CDISC.org](https://www.cdisc.org/)から各自でダウンロードしてください。
- 読み込み用データは `Data/` フォルダに格納されています。
- NotebookLM用の初期命令サンプルは `初期命令sample.txt` にあります。

---

## 🛠️ 環境構築手順

### ① CDISC.orgからドキュメントを取得

1. [CDISC.org](https://www.cdisc.org/) にアクセスし、右上「Sign in」→「Sign up now」で無料ユーザ登録
2. ログイン後、以下の手順でPDFをダウンロード  
   `Standards → SDTM → Versions → ドキュメント名 → Files & Links`
3. 推奨ファイル（PDF）：
   - SDTM v1.7
   - SDTMIG v3.3
   - SDTMIG for Medical Devices v1.1
   - SDTMIG-AP v1.0（SDTM v1.4の横にあります）

### ② GitHubからデータと初期命令を取得

- [Dataフォルダ](https://github.com/takahara-knz/SDTM_NotebookLM/tree/main/Data)から以下をダウンロード：
  - `00.` で始まるファイル
  - `02.` で始まるファイル
- 左メニューの `初期命令sample.txt` もダウンロード
- Terminologyは20260327版が出ていますが、下位互換なしにSDTM4.0にない用語が削除されており、SDTM3.3では使い物にならなくなっています。そのため、ここで提供するTerminologyは20250926版のままとしています。

### ③ Googleアカウントの準備

- Chromeで事前にログインしておくとスムーズ
- NotebookLM起動時にログインを求められる場合あり

---

## 🚀 NotebookLMのセットアップ

1. [NotebookLM](https://notebooklm.google.com/) にアクセスし、Googleアカウントでログイン
2. 新規ノートブックを作成
3. 左側「ソース」→「＋追加」から以下をアップロード：
   - CDISC.orgから取得したPDF
   - GitHubから取得したテキストファイル（00.～、02.～）
4. 真ん中の「入力を開始します」に `初期命令sample.txt` の内容をコピー＆修正して入力

※ファイル追加後、表示が変わらなくても気長に待ってください

---

## 💬 使い方

- 「入力を開始します」にSDTM関連の質問を入力
- 回答まで約30秒かかることがあります
- ログは保存されないため、必要に応じてコピペ等で記録してください

---

## 🔁 再起動時の注意

- 作成済みのノートブックを開けば、再設定は不要です
- そのまま質問を入力して利用可能です

---

## 📌 ライセンス・注意事項

- CDISC関連ドキュメントは各自で取得してください（再配布不可）
- 本レポジトリは教育・研究目的での利用を想定しています
- 一般的な生成AIよりは精度が高いですが、100%正確ではありません。
- このリポジトリで使用しているTerminologyのテキストデータは、米国国立がん研究所（NCI）が以下のページで公開しているCDISC Terminology（SDTM）を加工し、Google翻訳結果を付加したものです。
  - 出典：https://www.cancer.gov/about-nci/organization/cbiit/vocabulary/cdisc
  - The National Cancer Institute (NCI) does not endorse this translation and no endorsement by NCI should be inferred.
  - 国立がん研究所 (NCI) はこの翻訳を承認しておらず、NCI による承認を推測すべきではありません


