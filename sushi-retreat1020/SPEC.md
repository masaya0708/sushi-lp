# 鮨リトリート 2026.10.20 LP（/sushi-retreat1020/）

## 決定 2026-10-08
- status: draft（ローカル作成のみ。公開・push未承認）
- input: new_artifact / objective_or_scope_change
- outcome: change / cause: objective_change
- 目的: 10/20開催の鮨リトリート（主催者経由の依頼）に、Googleフォームと併せて掲載する1枚LPを用意する。
- 読者: 主催者の紹介で来る、鮨リトリートを初めて知る人。申込フォームの前に内容・費用・流れを確認したい。
- source: ユーザー依頼（フォーム概要の貼付、LINEでの主催者コメント）。
  - 構成は /sushi-retreat0428/ の前半（ゲスト紹介より上）をベースにする。
  - 後藤将哉のプロフィールを入れる。
  - 鈴木亜佐子さんの回は「開催レポート」ではなく「過去の開催実績」として紹介。
- 費用表: sushi-experience-20261020/SPEC.md EXP-005（10円単位切り上げ）と一致。キャンセル規定はEXP-002。
- CTA: 申し込みフォームへ（FORM_URL_PLACEHOLDER を本番URLに差し替え）。

## 公開前の確認
- FORM_URL_PLACEHOLDER（2箇所）の差し替え。
- `<meta name="robots" content="noindex">` を公開時に外すか判断。
- 主催者（依頼元）の確認。ゲスト回の実績掲載、参加者の声（過去の交流会のもの）の流用。
- 匠さんの講師紹介は今回の参加が未確認のため掲載せず。写真キャプションのみ旧LPのまま（要確認）。

## 改訂 2026-10-08（1回目）
- input: new_evidence / explicit_instruction（ユーザー指示）
- outcome: change / cause: new_evidence
- ジン: ボトル写真（gin.png）と、2024年8月シンガポール酒類品評会で最高金賞、4月米・7月英・8月シンガポールの3品評会すべてで最高評価、の実績を追加（情報源: ユーザー提供文）。
- 主催者紹介: 鮨まさや大将（後藤将哉）と会場オーナー（和田優喜子）の2名。写真はユーザー添付（masaya.jpg / yukiko.jpg）。小野匠の掲載と集合写真（profile.jpeg）は削除。
- 文言: 「目利きのプロから仕入れる予定」に修正。
- 未確認: ボトルのラベル表記（Water Dragon Spirits）は画像alt内のみ。商品名として本文に出す場合は確認が必要。

## 改訂 2026-10-08（2回目: デザイン全面見直し）
- input: preference_or_objection（「AI臭い・余白・一辺倒・詰めが甘い」）
- outcome: change / cause: reasoning_correction（0428の流用CSSを均一に当てていたのが原因。目的・価格・オファー・導線は不変）
- 対象レイヤー: visual design / copy の微修正のみ。offer・funnel・価格は変更なし。
- 基準: デジタル庁デザインシステム（design.digital.go.jp, 2026-10-08閲覧、要約経由）。本文16px以上・行間175%・字間2%、8px基準の余白、テキスト4.5:1・境界3:1、ボタン高56px・角丸8px、リンク下線、FAQはアコーディオン。
- 変更: 余白スケール統一（8/16/24/40/64/96）、見出しを左揃え+短い金線へ、2カラム化（コンセプト・ジン・実績・主催者）、冒頭に要点4行、キャンセル規定を隠さず表で表示（FAQから分離）、旧#a33（コントラスト不足）を廃止、フェードイン廃止。
- コピー: 結びを僕の言葉に書き換え（「午後の頭の中がだいぶ軽くなります」）。「ゲストの回ではなく」の説明的な一文を簡素化。

## 改訂 2026-10-08（3回目: 行間・余白・写真サイズ）
- input: preference_or_objection（スクショ4枚の指摘）/ outcome: change / cause: reasoning_correction
- 原因: 和文約物を詰める font-feature "palt" が句点後を窮屈にしていた。文節折り返し指定がなく「す。」等が孤立。ジン写真の列幅が過大。鈴木亜佐子さんの写真が88pxで小さい。
- 修正: palt削除、word-break:auto-phrase と text-wrap:pretty、段落間24px、ジンは240px+1fr、鈴木さんは112px(SP)/160px(PC)で名前と肩書きを分離。
- 確認: 幅375pxと1100pxで該当4箇所を目視、横スクロールなし、本文16px。実機・Safari・Firefoxは未確認。
