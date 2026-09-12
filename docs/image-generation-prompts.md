# 画像生成用プロンプト

event_furikaeriプロジェクトの仕様を可視化する1枚の左→右フロー図。

---

## UIガイドライン

**フォント・文字：**
- Noto Sans JP使用
- 本文15〜16px、行間1.6〜1.8
- 見出し行間1.2〜1.4
- 純黒禁止。テキストは#1a1a1a〜#333333

**色彩：**
- 背景：オフホワイト（#fafaf8、#f7f6f3）
- メインカラー：ネイビー系（#1e3a5f前後）、くすみカラー
- 60:30:10配分
- グラデーション・グロー・ネオン禁止

**造形：**
- 角丸2〜8px（12px超は不可）
- 1px淡いボーダー（#e5e5e5）で階層表現
- シャドウは `0 1px 3px rgba(0,0,0,0.06)` 程度

**情報密度：**
- 余白で誤魔化さない
- 必要な情報は隠さず提示
- 具体性を優先

---

## プロンプト：入力→出力内容→レポート（左→右フロー図）

```
Create a horizontal flow diagram showing the complete data processing pipeline for a Startup Weekend analysis tool. Left to right flow: Input → Output Data → Final Report. Design in Japanese UI style following these strict guidelines:

TYPOGRAPHY:
- Use Noto Sans JP font
- Body text: 15-16px, line-height 1.6-1.8
- Headings: line-height 1.2-1.4
- Text color: #1a1a1a to #333333 (never pure black #000000)
- Japanese language for all text

COLOR SCHEME:
- Background: Off-white (#fafaf8 or #f7f6f3)
- Main color: Navy (#1e3a5f) or muted traditional Japanese colors
- 60:30:10 color distribution
- NO gradients, glows, or neon effects
- Subtle 1px borders (#e5e5e5) for hierarchy

LAYOUT:
- Border-radius: 2-8px only (never 12px+)
- Box shadows: minimal (0 1px 3px rgba(0,0,0,0.06))
- Information-dense, don't hide details in excessive whitespace
- Horizontal layout: 3 columns (Left → Center → Right) with arrows between them

Overall title (top center):
"Startup Weekend 54時間の記録から就活資料へ"

---

LEFT COLUMN - 入力（Input）:

Column header: "入力"

Main box (white background, navy border):
Title: "音声のみ（確定）"
Subtitle: "ボイスレコーダー、スマホのボイスメモ等"

5 data type items stacked vertically (compact cards):

Item 1:
- Label: "1. 沈黙（間）"
- Detail: "音量のみ / 話者分離不要"
- Badge: "確実" (green)

Item 2:
- Label: "2. 笑い声"
- Detail: "音量パターン"
- Badge: "ほぼ確実" (light green)

Item 3:
- Label: "3. トーン"
- Detail: "音響分析 / 意味は不明"
- Badge: "確実" (green)

Item 4:
- Label: "4. 発話量"
- Detail: "話者分離が必要"
- Badge: "環境次第" (yellow)

Item 5:
- Label: "5. 内容"
- Detail: "文字起こし / 範囲未確定"
- Badge: "環境次第" (yellow)

Bottom section (light yellow/beige background, smaller text):
Title: "未確定事項"
Compact list:
• 何台どこに置くか
• 解析を自作するかHylableを使うか
• どこまで文字起こしするか
• 話者分離が通るか（録るまで不明）
• 本人の関与をどこまで求めるか

Large arrow pointing right → to center column

---

CENTER COLUMN - 出力内容（Output Data）:

Column header: "出力内容"

5-6 pattern detection cards stacked vertically:

Card 1:
- Pattern: "沈黙が長い + 笑いなし"
- Arrow → "谷" (red badge)

Card 2:
- Pattern: "発話の重なり + 笑いあり"
- Arrow → "白熱・盛り上がり" (green badge)

Card 3:
- Pattern: "発話の重なり + 笑いなし + 声量大"
- Arrow → "対立" (orange badge)

Card 4:
- Pattern: "沈黙が破れた直後 + 声量大"
- Arrow → "転換点" (blue badge)

Card 5:
- Pattern: "発話少ない + 笑いあり"
- Arrow → "雑談・休憩" (gray badge)

Card 6:
- Pattern: "自信度 + 行動データの突き合わせ"
- Arrow → "自信度最低時の行動量" (navy badge)

Bottom note (small, gray):
"データは記憶の補助線。本人の思考は本人にしか分からない"

Large arrow pointing right → to right column

---

RIGHT COLUMN - レポート（Final Report）:

Column header: "レポート"

Two sections stacked vertically:

Section 1 - A面（企業提出用）:
Tag: "A面" (navy badge)
Mock document preview with these items (compact list):
• 見出し（順位ではなく行動で記述）
• 曲線（自信度の推移 金19:00〜日17:00）
• 状況→課題→行動→結果
• 強み3つ（根拠必須）
• 実数4つ（睡眠時間除外）
• 引用（本人+メンバー）

Note: "事実と解釈を分離"

Section 2 - B面（本人用・提出しない）:
Tag: "B面" (orange/brown badge)
Mock document preview with these items (compact list):
• ESドラフト（400字版+30秒口頭版）
• やりがちな失敗（×と○）
• 想定される深掘り質問
• まだ埋まっていないところ

Note: "未確認は空欄で残す"

Bottom caption (across all columns, small text):
"本人が話していないことは書かない / 弱さを消さない / AIの補完を禁止"

---

OVERALL STYLE:
Clean, professional, trust-inducing Japanese business UI. Horizontal flow with clear left-to-right progression. Use arrows to show data transformation. Avoid playful or casual aesthetics. Use subtle borders and spacing to create hierarchy, not heavy shadows or gradients. Information-dense but readable. Each column should have similar visual weight.
```

---

## 使用方法

プロンプトをそのままClaude（claude.ai）やDALL-E、Midjourney等の画像生成AIに投入する。

**調整が必要な場合：**
- 色の調整：`#1e3a5f`を他のくすみカラーに変更可（えんじ、深緑など）
- レイアウトの密度：`information-dense`の度合いを指定（"very information-dense"/"moderate density"）
- サイズ：横長推奨（`1920x1080`または`2560x1440`）

**禁止事項：**
- Inter等の欧文フォントを日本語に当てない
- 紫→ピンクのグラデーション
- 角丸12px超
- 純黒#000000のテキスト
- 情報を隠して余白で誤魔化すレイアウト
