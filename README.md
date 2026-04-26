# 友達AI「だわん」GW配布版

> 親が作って、子どもが遊ぶ。ゴールデンウイークの小さなサプライズ。

犬のキャラクターをモチーフにした、小学生が友達感覚で話せるAIフレームです。
キーワードに応じてキャラクターの表情が自動で切り替わり、なぞなぞや名言など子ども向けのコンテンツが組み込まれています。

---

## デモ・関連リンク

- **ランディングページ**：https://chotbotlabo.net/dawan_ai/
- **AIエンジン（Google AI Studio）**：https://aistudio.google.com/

---

## 特徴

- **6種類の表情変化**：入力キーワードに応じてキャラクター画像が自動で切り替わる
- **まばたきアニメーション**：3〜6秒ごとにランダムでまばたき
- **タイプライター表示**：AIの返答が1文字ずつ表示される演出
- **コピーボタン**：AIの返答テキストをワンタップでクリップボードにコピー
- **定型メッセージ**：ハンバーガーメニューからよく使うメッセージをワンタップ送信
- **効果音**：送信音・タイプライター音のオン/オフ切り替え
- **子ども向けコンテンツ設定済み**：なぞなぞ・名言・ストレス解消法などを内蔵
- **プログラミング不要でカスタマイズ可能**：専用GUIツールでコード生成できる

> ⚠️ 本バージョンは**ローカル版専用**です。音声入力は含まれていません（ローカル環境では毎回マイク許可の確認が発生するため）。

---

## 必要なもの

- [Google AI Studio](https://aistudio.google.com/) のアカウント（無料）
- Gemini APIキー
- PC（Windows / Mac）
- ブラウザ（Chrome推奨）

---

## フォルダ構成

```
var_localGW/
├── index.html        # メイン画面
├── css/
│   └── style.css     # 見た目（色・フォントサイズなど）
├── js/
│   ├── api_id.js     # Gemini APIキーを記入するファイル
│   ├── prompt.js     # だわんの性格・口調の設定
│   ├── knowledge.js  # ナレッジデータ（なぞなぞ・名言など）
│   ├── greeting.js   # 起動時のあいさつメッセージ
│   ├── quick_reply.js # 定型メッセージ一覧
│   ├── sound.js      # 効果音設定
│   ├── keyword.js    # キーワード→表情の対応設定
│   └── script.js     # 動作全般
└── image/            # キャラクター画像
```

---

## セットアップ手順

1. このフォルダをダウンロード（ZIP展開 または `git clone`）
2. `js/api_id.js` を開き、Gemini APIキーを入力

```js
const GEMINI_API_KEY = "ここにAPIキーを入力";
```

3. `index.html` をブラウザで開く

以上で完成です。

---

## カスタマイズ

### 主なカスタマイズ項目

| ファイル | 内容 | 難易度 |
|---|---|---|
| `js/prompt.js` | だわんのキャラクター設定（性格・口調・ルール） | ★☆☆ |
| `js/knowledge.js` | ナレッジデータ（なぞなぞ・名言・ストレス解消法） | ★★☆ |
| `js/greeting.js` | 起動時のあいさつメッセージ | ★☆☆ |
| `js/quick_reply.js` | ハンバーガーメニューの定型メッセージ | ★☆☆ |
| `js/sound.js` | 効果音のオン/オフ | ★☆☆ |
| `js/keyword.js` | キーワード→表情の対応設定 | ★★☆ |
| `js/script.js` | タイプライター速度・まばたき間隔など | ★★☆ |
| `css/style.css` | 背景色・背景画像・フォントサイズなど | ★★☆ |
| `image/` | キャラクター画像の差し替え | ★★☆ |

### キャラクターを差し替える

`image/` フォルダの画像ファイルを自分のキャラクター画像に差し替えるだけで、
まったく別のAIフレームとして転用できます。
（ソースコードはMITライセンスのため商用利用も可能です）

---

## ライセンス

### ソースコード
[MIT License](LICENSE) — 無償利用・商用利用・改変・再配布すべて可能です。

```
MIT License

Copyright (c) 2025 オトーワン

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### キャラクター「だわん」
著作権は作者（オトーワン）に帰属します。

| 利用 | 可否 |
|---|---|
| 個人利用・雑談・癒しなど | ✅ OK |
| SNS・ブログでの紹介 | ✅ OK |
| カスタマイズして自分用AIとして利用 | ✅ OK |
| キャラクター画像の再配布・商品化 | ❌ NG |
| だわんキャラクターのままでの商用利用 | ❌ NG（要相談） |

> 自分のキャラクター画像に差し替えれば、商用利用を含めて自由に使えます。

---

## 免責事項

- 本プロジェクトは「現状有姿」で提供されます。動作保証は行いません。
- 不具合・サービス停止が発生する可能性があります。
- AIの応答内容の正確性は保証されません。
- 本プロジェクトの利用によって発生したいかなる損害についても、作者は責任を負いません。
- だわんはエンターテインメント・雑談を目的としたAIフレームです。医療・カウンセリング・福祉の代替にはなりません。
- AI機能にはGemini APIを使用しています。AIの挙動・データ取り扱いはGoogleの利用規約に準拠します。
- APIキーは利用者自身の責任で管理してください。
- **`api_id.js` にAPIキーを記載したままGitHubなどの公開リポジトリにアップロードすると、第三者にキーが盗まれ、無断利用・不正アクセス・意図しない課金が発生する危険があります。**
- このような情報漏洩によって生じたいかなる損害・不利益についても、作者（オトーワン）は一切の責任を負いません。
- 本プロジェクトに対するサポートは原則行いません。

---

## 制作者

**オトーワン**
X（Twitter）：[@otousan19](https://x.com/otousan19)
note：[oto_wan_ai](https://note.com/oto_wan_ai)
