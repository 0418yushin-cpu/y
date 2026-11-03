# 補完調査：4銘柄のポートフォリオ指標（ベータ・ボラティリティ・相関・指数採用）と相場環境ノートの空白埋め

- **作成日時: 2026-11-03**（火・文化の日、東証休場。直近の取引日は 2026-11-02（月））
- **使った検索回数: 16回**（持ち分16回を全部使用。standard 15回、extended 1回。内訳は末尾の検索ログ）
- **未解決事項（要点）**
  1. 4銘柄のベータ値は提供元ごとに 0.1〜2.25 とばらつきが大きく、「基準指数（TOPIX か日経平均か、米国指数か）」「期間（1年か5年か）」「リターン頻度（日次か月次か）」が明示されたものはごく一部。TradingView の「ベータ（1年）」のみ期間が明示されているが基準指数は未確認。みんかぶ・Yahoo!ファイナンス（日本版）・日経のスニペットからはベータ値は取れなかった。
  2. 4銘柄間の相関係数を示す資料は見つからなかった（同日連動の事例で代替）。
  3. 指数採用：古河機械金属の日経225除外（2018-10-01）と三菱重工業のTOPIX Core30組入れ（2024-10-31付）は確認。双日・三菱重工業の日経225採用、三井海洋開発・古河機械金属のTOPIXサイズ区分、JPX日経400の2026年8月入替後の4銘柄の採否は、検索では一次ソースを確認できず【未確認】（一般知識にもとづく見立てを併記）。
  4. ドル円の2026年10月の**ザラ場ベース**の高値・安値は未確認（日銀17時時点の終値ベースのレンジのみ）。
  5. TOPIX が 8/14（4,197.20）以降に終値で最高値を更新したかは、8/15〜10/2 の日次が未確認。10/5 の終値 4,145.22 は 8/14 を下回っていた。
  6. 日銀12月会合（12/17〜18）と FOMC（12/8〜9）は、日銀・FRB の公式カレンダー本文は検索で直接確認できず、第三者サイト（公式日程を転記）での確認にとどまる。
  7. 古河機械金属の決算発表日（11/12）は株探・TradingView・Yahoo!ファイナンス・松井証券の表示で確認。会社IRカレンダーでの直接確認はできていない。

> **調査方法の制約**：株価サイト・証券会社・各社IR・ニュースサイトへの直接アクセスは全て拒否されるため、数値は Web検索結果の抜粋・要約のみに基づく。各数値には出所URLと基準日を併記した。推定・計算は【試算】、確認できなかったものは【未確認】。矛盾する数値は両方を記録した。他の調査員のノート（modec_6269.md、sojitz_2768.md、mhi_7011.md、furukawa_5715.md、market_environment.md、gapfill_prices.md など）の記述は「既存ノート」として引用し、書き換えていない。

---

## 1. ベータ値とヒストリカル・ボラティリティ（4銘柄）

### 1.1 一覧表（検索で取れた全数値。提供元・定義が異なるので横並び比較は注意）

| 銘柄 | 指標 | 値 | 期間・基準 | 基準日 | 出所 |
|---|---|---|---|---|---|
| 6269 三井海洋開発 | ベータ | 0.453 | 基準指数・期間の記載なし | 日付なし（ページ掲載値） | [Snowball Analytics](https://snowball-analytics.com/public/asset/6269.TSE) |
| 6269 | ベータ | 0.71 | 記載なし | 2026-01-03 時点 | [Disfold](https://disfold.com/stock/jpx-6269/) |
| 6269 | 週間平均変動率（ボラティリティ） | 11.2%／週（エネルギーサービス業界 5.7%、日本市場 3.7%） | 直近1年で「安定」だが日本株の75%より高い | 検索時点（日付記載なし） | [Simply Wall St](https://www.simplywall.st/stocks/jp/energy/tse-6269/modec-shares) |
| 6269 | 年率ボラティリティ予測（GARCH） | 41.97% | モデル推計値（1日先予測） | 2026-02-12 向け予測 | [NYU Stern V-Lab GARCH](https://vlab.stern.nyu.edu/volatility/VOL.6269%3AJP-R.GARCH) |
| 6269 | 年率ボラティリティ予測（MEM／非対称MEM） | 89.20%／79.51% | 高値安値ベースのモデル推計 | 2026-02-20 向け予測 | [V-Lab MEM](https://vlab.stern.nyu.edu/volatility/VOL.6269%3AJP-HL.MEM)、[V-Lab AMEM](https://vlab.stern.nyu.edu/volatility/VOL.6269%3AJP-HL.AMEM) |
| 6269 | 52週レンジ／1年騰落 | 6,370.0〜16,720.0円／56.8%（符号は要約に明記なし。株価約10,100円と下限6,370円の関係から＋とみられる【試算】） | 52週 | 2026年8月上旬で終わる期間 | [Investing.com（vn）](https://vn.investing.com/equities/modec-inc-historical-data) |
| 2768 双日 | ベータ（5年・月次） | 0.62 | 5Y Monthly（基準は米Yahoo!の標準＝S&P500 とみられる【未確認】） | ページのデータが **2024年4月ごろ**で古い | [Yahoo Finance 2768.T](https://finance.yahoo.com/quote/2768.T/) |
| 2768 | ベータ（5年） | 1.04 | 米ドル建て換算の数値 | 検索時点 | [getquin](https://app.getquin.com/database/JP3663900003) |
| 2768 | ベータ | 約0.67〜0.72 | 期間記載なし | 検索時点 | [Parqet](https://app.parqet.com/en/stocks/sojitz-JP3663900003) |
| 2768 | ベータ | 0.675 | 記載なし | 日付なし | [Snowball Analytics](https://snowball-analytics.com/public/asset/2768.TSE) |
| 2768 | ベータ | 0.00（プレースホルダーとみられる。採用しない） | — | — | [Motley Fool](https://www.fool.com/quote/tyo/2768/) |
| 2768 | ヒストリカル・ボラティリティ | 【未確認】（検索で数値が出なかった） | — | — | — |
| 7011 三菱重工業 | ベータ | 0.360 | 記載なし | 日付なし | [Snowball Analytics](https://snowball-analytics.com/public/asset/7011.TSE) |
| 7011 | ベータ | 0.36／0.37 | 記載なし | 検索時点 | [Rendement Bourse](https://rendementbourse.com/7011-mitsubishi-heavy-industries) |
| 7011 | ベータ（1年）／ボラティリティ | **1.52**／4.17%（TradingView の「ボラティリティ」は1日の値幅ベースの指標） | 1年。基準指数は未確認 | 検索時点（日付なし） | [TradingView（名証 7011）](https://tw.tradingview.com/symbols/NAG-7011/forecast-price-target/) |
| 7011（ADR） | ベータ（5年・月次） | 0.38 | 米OTC の MHVYF（東証7011ではない） | 検索時点 | [Yahoo Finance MHVYF](https://finance.yahoo.com/quote/MHVYF) |
| 5715 古河機械金属 | ベータ／ボラティリティ（1年）／シャープレシオ（1年） | **0.57／0.53（＝53%）／1.62** | 1年 | 株価 4,145円＝**2026-06-18** 時点 | [Fintel](https://fintel.io/s/jp/5715) |
| 5715 | ベータ（1年）／ボラティリティ | **2.25**／2.67%（1日） | 1年。基準指数は未確認 | 検索時点（日付なし） | [TradingView（独）](https://de.tradingview.com/symbols/TSE-5715/) |
| 5715 | ベータ／3年ボラティリティ | 0.8919（シュトゥットガルト）・0.8858／**58.2%**（フランクフルト） | 3年 | 検索時点 | [GuruFocus FRA:FUR](https://www.gurufocus.com/stock/FRA:FUR/summary)、[GuruFocus STU:FUR](https://www.gurufocus.com/stock/STU:FUR/summary) |
| 5715 | ベータ | 0.098（2025年の株価データ。信頼性が低い） | — | 2025年 | [Snowball Analytics](https://snowball-analytics.com/public/asset/5715.TSE.JPY) |
| 5715 | 週間平均変動率 | 7.3%／週（日本株の75%より高い、直近1年で安定） | 1年 | 検索時点 | [Simply Wall St](https://simplywall.st/stocks/jp/capital-goods/tse-5715/furukawaltd-shares) |
| 5715 | 年率ボラティリティ予測（GARCH ほか） | 51.23%（GARCH）。モデルにより 46〜97% | モデル推計 | 2026-02-06 向け予測 | [V-Lab GARCH](https://vlab.stern.nyu.edu/volatility/VOL.5715%3AJP-R.GARCH)、[V-Lab MEM](https://vlab.stern.nyu.edu/volatility/VOL.5715%3AJP-HL.MEM) |

### 1.2 銘柄別の読み方

**6269 三井海洋開発**
- ベータは 0.45〜0.71 と「市場より低い」値しか見つからなかったが、どちらも基準指数・期間が不明で、2026年の値動き（既存ノート：年初来高値 16,615円（2/12）→年初来安値 8,378円（10/9）、約−50%）と整合しない。海外のデータ提供元は米国指数を基準にすることが多く、日本株のベータが低く出やすい点に注意。
- ボラティリティは、Simply Wall St の週間 11.2%（市場 3.7% の約3倍）、V-Lab の GARCH 42%／MEM 80〜89%（2月時点）と、いずれも「極めて高い」水準で一致している。
- 【試算】週間 11.2% を年率換算（×√52）すると約 81%。V-Lab の MEM 系の予測（80〜89%）と近い。

**2768 双日**
- 5年・月次ベータは Yahoo Finance の 0.62 が唯一の期間明示値だが、ページのデータが2024年4月ごろで古い。Parqet・Snowball の 0.67〜0.72 と大差はない。米ドル建てで計算した getquin の 1.04 は為替の影響を含むため、円建てとは比較できない。
- ヒストリカル・ボラティリティの数値は取れなかった【未確認】。既存ノート（sojitz_2768.md）の事例では、10/30 の決算日に −6.28%、2026-01-13 に +6.84% と、商社株としては値動きが大きい日がある。

**7011 三菱重工業**
- Snowball／Rendement Bourse の 0.36〜0.37 と、TradingView の「ベータ（1年）1.52」が大きく食い違う。前者は期間・基準の記載がなく、ADR（MHVYF）の5年月次ベータ 0.38 と近いことから、米国指数を基準にした長期ベータの可能性が高い。日本株の分散を考える目的（対TOPIX・対日経平均の感応度）には、1年ベータ 1.52 の方が実感（既存ノート：52週高値から約−27%、10/2→11/2 で −11.8%）に合う。
- TradingView の「ボラティリティ 4.17%」は1日の値幅を終値で割った指標で、標準偏差ベースのヒストリカル・ボラティリティとは定義が異なる。【試算】仮に日次変動率として年率換算（×√250）すると約 66% だが、定義が違うので参考値にとどめる。

**5715 古河機械金属**
- ベータは 0.098（Snowball）〜2.25（TradingView 1年）まで幅がある。期間と日付がはっきりしているのは Fintel（ベータ 0.57、1年ボラティリティ 53%、2026-06-18 時点）と TradingView（1年ベータ 2.25）。GuruFocus の3年ボラティリティ 58.2% は Fintel の1年 53% と近い。
- Simply Wall St の週間 7.3% を年率換算すると約 53%【試算】で、Fintel の 53%、V-Lab GARCH の 51% とほぼ一致する。ヒストリカル・ボラティリティとしては「年率 50%台前半」が複数ソースで整合的。

### 1.3 【試算】4銘柄の相対比較（ボラティリティの目安）

| 銘柄 | 年率ボラティリティの目安（複数ソースの整合値） | 根拠 | 日本市場全体との比 |
|---|---|---|---|
| 6269 三井海洋開発 | **約 80%**（GARCH 42%〜MEM 89% のレンジ） | Simply Wall St 週間 11.2%×√52＝81%、V-Lab MEM 80〜89% | 市場（週間3.7%＝年率約27%【試算】）の約3倍 |
| 5715 古河機械金属 | **約 50〜58%** | Fintel 1年 53%、V-Lab GARCH 51%、GuruFocus 3年 58%、Simply Wall St 7.3%×√52＝53% | 約2倍 |
| 7011 三菱重工業 | 【未確認】（TradingView の値幅指標 4.17%/日のみ） | 定義の違いから年率換算は参考値（約66%【試算】） | — |
| 2768 双日 | 【未確認】 | 数値なし | — |

- ベータについては、「1年・対国内指数」とみられる TradingView の値（7011: 1.52、5715: 2.25）と、「長期・米国指数基準」とみられる値（0.36〜0.7）が混在しており、**同じ定義で4銘柄をそろえた数値は得られなかった**。証券会社のツール（SBI・楽天・マネックスの銘柄分析）や Bloomberg／QUICK での確認を推奨する。
- 既存ノート market_environment.md 第9節の「少なくとも三井海洋開発と三菱重工は指数より大きく動いている」という推論は、本調査のボラティリティ数値（6269 約80%、5715 約50%台、市場約27%【試算】）と整合する。

---

## 2. 4銘柄間の相関と、同じ材料で同日に大きく動いた事例

### 2.1 相関係数
- 4銘柄間の相関係数（日次・週次リターン）を示す資料は、検索では見つからなかった【未確認】。以下は代替として、同じ材料で同日に動いた事例を日付付きで整理したもの。

### 2.2 同日連動の事例（レアアース・経済安保・地政学）

| 日付 | 材料 | 6269 | 2768 | 7011 | 5715 | 出所 |
|---|---|---|---|---|---|---|
| 2026-01-06〜07 | 中国が日本向けデュアルユース品目の輸出管理強化を発表（1/6）。翌1/7、日経平均・TOPIXは最高値更新から一転して反落 | — | — | — | 一時 **+7.9%**（「レアアース採鉱の関連最右翼」として窓を開けて急伸、昨年来高値更新） | [PayPay証券 2026-01-28](https://media.paypay-sec.co.jp/cat5/f260128)、[Bloomberg 2026-01-07](https://www.bloomberg.com/jp/news/articles/2026-01-07/T8H100KJH6V500)、[みんかぶ 2026-01-07](https://minkabu.jp/news/4412644)（既存ノート furukawa_5715.md・market_environment.md 経由） |
| 2026-01-13 | 中国の規制強化＋南鳥島沖レアアース泥の試掘（探査船「ちきゅう」出航）期待、衆院解散 | **+3.2%** | **+6.84%**（6日続伸、上場来高値） | 記載なし | **+11.2%** | [X投稿まとめ 2026-01-13](https://x.com/t_ryoma1985/status/2010986397751222520)（一次情報ではない）、[LIMO](https://limo.media/articles/-/108304)（既存ノート経由） |
| 2026-10-26 | 時事通信（10/24）が「日独首脳会談で中国が輸出規制するレアアースなど重要鉱物が主要テーマになる」と報道 → レアアース関連銘柄の一角が買われた（思惑買いとされ、継続性には疑問との指摘） | 【未確認】 | 【未確認】 | 【未確認】 | 【未確認】 | [SBI証券 国内株式ウィークリー 2026-10-28](https://go.sbisec.co.jp/media/report/dom_em_weekly/dom_em_weekly_261028.html)（個別銘柄名は要約に出ず） |
| 2026-10-15 | AI需要懸念で日経平均 −3,318円（−4.9%、下げ幅歴代3位） | 【未確認】 | 【未確認】 | 【未確認】 | 【未確認】 | [熊本日日新聞（共同）2026-10-15](https://kumanichi.com/articles/2046867)（既存ノート market_environment.md 経由）。4銘柄の当日騰落は未取得 |
| 2026-10-30 | 双日の上期決算（昼発表） | — | **−6.28%**（5,130円） | — | — | 既存ノート sojitz_2768.md・gapfill_prices.md（[株探ニュース](https://s.kabutan.jp/news/n202611020864)）。個別材料で、他3銘柄との連動ではない |

### 2.3 読み方
- 確認できた「同日・同方向」の事例は、**レアアース・経済安保**の材料で古河機械金属・双日・三井海洋開発が同時に買われた 2026-01-13 と、古河機械金属が急伸した 2026-01-07。三菱重工業がこのテーマで同日に大きく動いた記録は見つからなかった（防衛・ガスタービンが主材料）。
- したがって、相関の構造は「5715・2768（＋6269）はレアアース・米中・中国規制のニュースで正の相関が強まりやすい」「7011 は防衛・電力設備で別の材料」「原油（6269）とドル円（4銘柄共通）は別軸」と整理できる【推論】。定量的な相関係数は未取得。
- 11/10（中国レアアース規制停止措置の期限、三井海洋開発の決算）や 11/18〜19（APEC 米中）など、既存ノートが挙げるイベントでは 5715・2768・6269 が同時に反応しうる。

---

## 3. 指数採用状況（日経225・TOPIX Core30/Large70・JPX日経400）

| 銘柄 | 日経225 | TOPIXサイズ区分（Core30／Large70／Mid400／Small） | JPX日経400（2026-08-31 付の定期入替後） | 根拠・出所 |
|---|---|---|---|---|
| 6269 三井海洋開発 | **非採用とみられる**【検索では採用・除外の記録なし。一般知識】 | 【未確認】（時価総額から Mid400 の可能性が高い【推定】） | 【未確認】 | 日経225・JPX400 の検索結果に銘柄名が出なかった |
| 2768 双日 | **採用（卸売業・商社グループ）とみられる**【一次ソース未確認。一般知識】 | 【未確認】（Large70 ではなく Mid400 の可能性が高い【推定】） | 【未確認】 | 既存ノート sojitz_2768.md も「一次ソースで未確認」と記載 |
| 7011 三菱重工業 | **採用（機械）とみられる**【一次ソース未確認。一般知識】 | **TOPIX Core30**（2024-10-31 付の定期入替で追加） | 【未確認】（時価総額・ROE から継続採用の可能性が高い【推定】） | [Weblio「TOPIX Core30」](https://www.weblio.jp/content/TOPIX_Core30)（Wikipedia由来の解説）、[kabu.com 用語集](https://kabu.com/glossary/kabu2248.html) |
| 5715 古河機械金属 | **非採用**（2018-10-01 の定期入れ替えでサイバーエージェント（4751）の採用と引き換えに**除外**。以後の再採用の記録なし） | 【未確認】（時価総額から Small の可能性が高い【推定】） | 【未確認】（2026-08 追加45銘柄のスニペットに名前なし） | [日経平均プロフィル 2018年9月 定期入れ替え](https://indexes.nikkei.co.jp/atoz/2018/09/9w4.html) |

**補足（指数の仕組みと直近の入替）**
- TOPIX Core30 は「TOPIX100 のうち Large70 に含まれない30銘柄（時価総額・流動性が最上位）」、Large70 は「Core30 に次ぐ70銘柄」。定期入替は毎年1回（10月）— [Weblio「TOPIX Large70」](https://www.weblio.jp/content/TOPIX+Large+70)、[JPX TOPIX Large70 ファクトシート](https://www.jpx.co.jp/markets/indices/factsheets/files/002_1_02_fac2_size_TOPIX%20Large70.pdf)、[大和証券 用語集](https://www.daiwa.jp/glossary/YST3503.html)。2026年10月の定期入替結果は検索で見つからず、確認できた一覧は 2025-10-31 時点のものまで（[JPX cal2_12_size.pdf](https://www.jpx.co.jp/corporate/news/news-releases/0060/t13vrt000000cg4e-att/cal2_12_size.pdf) は本文未取得）。
- JPX日経インデックス400：JPX総研と日経は 2026-08-07 に定期入替を発表、**45銘柄を追加・39銘柄を除外**（効力は 2026-08-31 算出分から）。スニペットで見えた追加銘柄はサイバーエージェント（4751）、上村工業（4966）、UACJ（5741）、京阪HD（9045）、大栄環境（9336）、中国電力（9504）、日本冶金工業（5480）など。除外一覧は未取得 — [JPX 2026-08-07 公表資料 data_j.pdf](https://www.jpx.co.jp/news/6030/t13vrt000001om22-att/data_j.pdf)、[同 data1_j.pdf](https://www.jpx.co.jp/news/6030/t13vrt000001om22-att/data1_j.pdf)、[サンゲツ 継続選定のお知らせ 2026-08-24](https://www.bridge-salon.jp/upload/tekiji_pdf/T~~81300~000000~1402~0~20260824~1000~20260820523690G.pdf)。MCJ（6670）は整理銘柄指定で 2026-06-02 算出分から期中除外 — [JPX](https://www.jpx.co.jp/news/1044/nlsgeu000004hy72-att/deta-j.pdf)。
- 日経225：2026-04-01 算出分からの定期見直しでキオクシアHD、パン・パシフィックHD が新規採用 — [PayPay証券 2026-03-09](https://media.paypay-sec.co.jp/cat5/jisha260309)。入替は通常年2回（4月・10月）。4銘柄の現行の採用一覧での確認は未了。

**ポートフォリオへの含意（推論）**
- 日経225 採用銘柄（7011、2768 とみられる）は日経平均連動 ETF・先物の売買に伴う需給（指数イベント、裁定）を受けやすく、非採用の 6269・5715 は個別要因の比重が高い。三菱重工業は Core30 でもあり、海外投資家のパッシブ資金の影響を最も受ける。
- 単元未満株での少額投資では指数採用の有無は売買手続きに影響しないが、「指数の値動きとの連動度（ベータ）」の見立てには関係する。

---

## 4. 相場環境ノートの空白埋め

### 4.1 新発10年国債利回り（2026-11-02）

| 項目 | 値 | 基準日 | 出所 | 備考 |
|---|---|---|---|---|
| 新発10年国債利回り（長期金利） | **2.77%**（前日比変わらず。日中は一時 2.785%） | 2026-11-02 | [Trading Economics 日本10年債](https://tradingeconomics.com/japan/government-bond-yield)、[市況記事「JGB yields edge up ahead of series of auctions」](https://rallies.ai/news/jgb-yields-edge-up-ahead-of-series-of-auctions-e4d7d4b52ea359ec) | 「最終の引値（日本相互証券）」は未確認 |
| 同（別ソース） | 2.774%（前日比 −0.07%） | 2026-11-02 終値 | [Investing.com 日本10年債 時系列](https://www.investing.com/rates-bonds/japan-10-year-bond-yield-historical-data) | 2.77% とほぼ一致 |
| MUFG の予想レンジ | 2.650〜3.000%（米中間選挙後、高市政権の財政政策をめぐる投機が材料） | 2026-11-02 付ウィークリー | [MUFG Research Japan Weekly 2026-11-02](https://www.mufgresearch.com/rates/japan-economic-financial-weekly-2-november-2026) | — |
| 今後の入札 | 10年債（11/5・木）、30年債（11/10）、5年債（11/12） | 2026-11 | 上記市況記事 | 6269 の決算（11/10）、5715 の決算（11/12）と同日 |

**過去の節目（文脈）**
- 2026-01-19：終値 2.270%（前週末比 +0.090%）、一時 2.275%（26年11カ月ぶり高水準） — [秋田魁新報（共同）2026-01-19](https://www.sakigake.jp/news/article/20260119CO0102/)
- 2026-08-31：一時 2.950%（1996年以来の高水準） — [熊本日日新聞（共同）](https://kumanichi.com/articles/2030791)
- 2026-09-01：約30年ぶりに 3% を突破。9/25 に一時 3.115% — [熊本日日新聞（共同）](https://kumanichi.com/articles/2043510)。9/11 に再び 3.000%（3%台は 9/2 以来） — [熊本日日新聞（共同）](https://kumanichi.com/articles/2034805)
- 2026-10-06：財務省が10年債の表面利率を年 3.1% に設定（1996年8月以来、約30年ぶりの高水準） — 同上（kumanichi 2043510）
- **整合性の注意**：10月初めの新発債の利率 3.1% に対し、11/2 の 2.77% は約30bp低い。10月の株式市場のリスクオフ（日経平均 −5.2%）と整合はするが、1カ月での低下幅が大きいため、日本相互証券または財務省「国債金利情報」で引値を再確認すること【要確認】。

### 4.2 ドル円の2026年10月レンジ

| 項目 | 値 | 基準 | 出所 | 備考 |
|---|---|---|---|---|
| 10月の最高終値 | **158円37〜40銭**（10/1） | 日銀公表 17時時点の終値ベース | [松井証券 日銀為替市況](https://finance.matsui.co.jp/news/631057/index)、[同](https://finance.matsui.co.jp/news/631507/index) | ページに年の表記がないが、10/30 の値が OANDA の 10/30 NY終値 157.487（既存ノート）と整合するため 2026年と判断【試算に近い判断】 |
| 10月の最安終値 | **156円95〜97銭**（10/23、前日比 ▼0.27） | 同上 | 同上 | — |
| 10/27 終値 | 157円86〜87銭 | 同上 | 同上 | — |
| 10/30 終値 | 157円55〜56銭（▼0.27） | 同上 | 同上 | 10/31 は土曜で東京市場休場（NY終値 157.487 — 既存ノート OANDA） |
| 10月の終値ベースのレンジ【試算】 | **約 156.95〜158.40円（値幅約1.4円）** | 上記の最高・最安終値 | — | **ザラ場ベースの高値・安値は未確認** |
| 11/2 の水準（参考） | 7時時点 157円35〜67銭、日中は157円台半ばで小動き | 2026-11-02 | 既存ノート（[中日新聞](https://www.chunichi.co.jp/article/1333673)、[OANDA 2026-11-02](https://www.oanda.jp/lab-education/market_news/report_usdjpy_20261102/)） | — |

**直前の月の文脈（GMOあおぞら 月次レポート）**
- 2026年7月：高値 163.981、安値 157.569、7月末 157.578（月間 −3.08%）。財務省は 8/3 に「7/31（米東部時間）に米財務省と協調して円買い介入を実施」と公表。8月の基本シナリオレンジは 152〜160円 — [GMOあおぞらネット銀行 USD/JPY 2026年8月号](https://gmo-aozora.com/fx/report/pdf/USD_JPY_202608.pdf)、[同 7月号](https://gmo-aozora.com/fx/report/pdf/USD_JPY_202607.pdf)。**10月号は検索で見つからず**【未確認】。
- 読み方：7月の協調介入後、8〜10月は157〜158円台で膠着しており、10月は終値ベースで約1.4円幅の極端に狭いレンジ。日銀の12月利上げ観測（既存ノート）で円高方向のバイアスがかかりつつ、米利上げ観測が相殺している構図【推論】。

### 4.3 TOPIX は 8/14（4,197.20）以降に最高値を更新したか

| 項目 | 値 | 基準日 | 出所 |
|---|---|---|---|
| 既存ノートの確認済み最高値（終値） | 4,197.20 | 2026-08-14 | 既存ノート market_environment.md（[時事通信 2026-08-14](https://news.yahoo.co.jp/articles/e1f2ce8394777d095a34e33d91b2d85a9f777bfe)） |
| 10/5 の TOPIX 現物終値 | **4,145.22** | 2026-10-05 | [松井証券 2026-10-05](https://finance.matsui.co.jp/news/624416/index) |
| 10/6 の推定終値【試算】 | 約 4,181（1305 ETF の 10/5 4,409円 → 10/6 4,447円、+0.86% を 4,145.22 に適用） | 2026-10-06 | [iFreeETF TOPIX（1305）時系列](https://www.traders.co.jp/stocks/00_1305/historical) |
| 10/9 以降の推定レンジ【試算】 | 約 3,950〜4,110（ETF 4,200〜4,370円台 × 0.940） | 2026-10-09〜 | 同上。既存ノートの 10/30 3,965.07、11/2 3,930.28 と整合 |
| 11/2 終値 | 3,930.28（8/14 比 **−6.36%**【試算】） | 2026-11-02 | 既存ノート |

**結論**：10月上旬の TOPIX（10/5 4,145.22、10/6 約4,181【試算】）は 8/14 の 4,197.20 を**下回っており**、10月に最高値を更新した形跡はない。**8/15〜10/2 の日次終値は未確認**のため「8/14 以降に一度も更新していない」とは断定できない【未確認】。6/17 に初めて終値 4,000台（4,013.23）に乗せた経緯は [Adnkronos 2026-06-17](https://english.adnkronos.com/2026/06/17/nikkei-topix-hit-all-time-closing-highs/) でも確認できる。なお ETF（1305）の価格を指数値そのものとして扱うのは不適切（10/5 の ETF 4,409円 vs 指数 4,145.22）。

### 4.4 日銀の次回金融政策決定会合

| 項目 | 値 | 出所 | 確度 |
|---|---|---|---|
| 次回会合 | **2026-12-17（木）〜12-18（金）**（2026年の第8回会合） | [moocota 金融政策決定会合 日程](https://www.moocota.com/mpm-nittei/)、[invest-concierge](https://www.invest-concierge.com/posts/boj-policy-meeting-guide) | 第三者サイト。**日銀公式ページでの12月の行は検索結果に含まれず**【公式未確認】 |
| 公式ページ | 「金融政策決定会合の運営」（2026年の一覧あり。スニペットは 4/27〜28 まで） | [日本銀行](https://www.boj.or.jp/mopo/mpmsche_minu/index.htm) | — |
| 裏付け | 日銀の2027年日程の公表文に「2026年12月会合の議事要旨は 2027-01-27（水）公表」と記載 → 12月会合の存在を裏付け | [日本銀行 2027年日程 mref260731a.pdf](https://www.boj.or.jp/mopo/mpmsche_minu/m_ref/mref260731a.pdf) | 公式 |
| 注意 | 2027年の12月会合は 12/16（木）〜17（金）。2026年と混同しないこと | 同上 | — |
| 既存ノートとの整合 | market_environment.md は MogWatch の表記から 12/17〜18 と判断していた。本調査の第三者サイト2件も同じ日付 | — | 整合 |

### 4.5 FOMC の次回日程

| 項目 | 値 | 出所 | 確度 |
|---|---|---|---|
| 次回 FOMC | **2026-12-08（火）〜12-09（水）**。声明は 12/9 14:00 ET（19:00 UTC ＝ 日本時間 12/10 4:00） | [fedratecalc（FOMC schedule December 2026）](https://fedratecalc.com/fomc-meeting-schedule/december-2026/)、[calendarx](https://www.calendarx.com/events/fomc-meeting-december-2026)、[thriveinmarkets](https://thriveinmarkets.com/calendar/dates/fomc-2026/)、[financecalendar.com（FRB公式カレンダー転記と明記）](https://www.financecalendar.com/fomc-meetings/) | 複数の第三者サイトが一致。**federalreserve.gov 本文は検索結果に出ず**【公式未確認】 |
| 会合の性質 | 年4回の経済見通し（SEP・ドットチャート）公表回 | 同上 | — |
| 食い違い | stockhub.kr は 12/16（水）と記載（他と矛盾、採用しない）。既存ノートの Kiplinger は 12/7〜8 と記載 | [stockhub.kr](https://stockhub.kr/en/fomc-schedule) | 12/8〜9 が最も妥当（多数のソースが FRB カレンダーを引用） |
| 参考 | シカゴ連銀の「Federal Reserve calendars」ページ | [Chicago Fed](https://www.chicagofed.org/utilities/about-us/federal-reserve-calendars) | 本文未取得 |

---

## 5. 4銘柄の決算発表日（確認状況）

本項目には検索回数を割かず、既存ノートで確認済みの一次ソース記述を整理した。

| 銘柄 | 発表日時 | 内容 | 根拠（既存ノート経由） | 確認状況 |
|---|---|---|---|---|
| 6269 三井海洋開発（12月決算） | **2026-11-10（火）12:30 JST** | 2026年12月期 第3四半期決算 | [MODEC IR Calendar](https://www.modec.com/ir/calendar/)（modec_6269.md）、[Yahoo!ファイナンス](https://finance.yahoo.co.jp/quote/6269.T)、[松井証券](https://finance.matsui.co.jp/stock/6269/index)、[stockanalysis](https://stockanalysis.com/quote/tyo/6269/) | **会社IRカレンダーで確認済み**。取引時間中の発表のため当日後場に大きく動きやすい（過去：2025/11 ストップ高、2026/2・2026/5 後場急落） |
| 7011 三菱重工業 | **2026-11-06（金）13:30** | 2026年度 第2四半期決算 | [三菱重工 IR情報](https://www.mhi.com/jp/finance/)（mhi_7011.md）、[Yahoo!ファイナンス](https://finance.yahoo.co.jp/quote/7011.T)（gapfill_prices.md） | **会社IRで確認済み**。取引時間中（13:30）の発表 |
| 5715 古河機械金属 | **2026-11-12（木）**（時刻未確認。前年 2025/11/7 は 15:30 大引け後） | 2027年3月期 第2四半期決算 | [株探](https://kabutan.jp/stock/?code=5715)、[TradingView](https://www.tradingview.com/symbols/TSE-5715/)、[Yahoo!ファイナンス](https://finance.yahoo.co.jp/quote/5715.T)、松井証券（furukawa_5715.md、gapfill_furukawa_extra.md、gapfill_prices.md） | 情報サイト4件で一致。**会社IRカレンダーでは未確認**。JapanIR に「11月9日」の記述があるが年度違いの可能性（既存ノート） |
| 2768 双日 | **2026-10-30（金）昼・発表済み** | 2027年3月期 上期決算：連結純利益 635億円（前年同期比 +40.4%）、通期計画 1,300億円に対する進捗率 48.9%。株価は当日 −6.28%（5,130円）、株探の「決算マイナス・インパクト」で −6.10% | [株探ニュース 2026-11-02](https://s.kabutan.jp/news/n202611020864)、[Yahoo!ファイナンス](https://finance.yahoo.co.jp/quote/2768.T)（sojitz_2768.md、gapfill_prices.md） | 発表済み。次回は第3四半期（2027年2月初めの予定 — [双日 IR](https://www.sojitz.com/jp/ir/)） |

**イベントの重なり（本調査で判明した追加点）**
- 11/10 は 6269 の決算と同時に、30年国債入札、中国レアアース規制停止措置の期限（既存ノート）が重なる。11/12 は 5715 の決算と5年国債入札が同日。11/6 は 7011 の決算と米雇用統計（既存ノート）が同日。

---

## 6. 検索ログ（16回）

| # | mode | クエリ（要旨） | 得られたもの |
|---|---|---|---|
| 1 | standard | MODEC 6269.T beta volatility stock statistics | Snowball β0.453、Disfold β0.71（2026-01-03）、Simply Wall St 週間11.2%、V-Lab GARCH 41.97%／MEM 89.20%、Investing 52週レンジ |
| 2 | standard | Sojitz 2768.T beta 5Y monthly | Yahoo 5Y月次 β0.62（2024年4月ごろのデータ）、getquin 1.04（USD）、Parqet 0.67〜0.72、Snowball 0.675 |
| 3 | standard | Mitsubishi Heavy Industries 7011.T beta 5Y monthly | Snowball 0.36、Rendement Bourse 0.36/0.37、TradingView 1年β1.52・ボラ4.17%、ADR MHVYF β0.38 |
| 4 | standard | Furukawa Co 5715.T beta volatility | Fintel β0.57・1年ボラ53%・シャープ1.62（2026-06-18）、TradingView 1年β2.25・2.67%、GuruFocus β0.89・3年ボラ58.2%、Simply Wall St 週間7.3%、V-Lab GARCH 51.23% |
| 5 | standard | 新発10年国債利回り 11月2日 2026 終値 | 11/2 の値は出ず。9月の3%台、1/19 終値2.270% の文脈のみ |
| 6 | standard | ドル円 2026年10月 月間 高値 安値 | GMOあおぞら月次は8月号まで（7月：163.981／157.569／末157.578）。松井「日銀為替市況」に10月終値（年表記なし） |
| 7 | standard | 日経225 構成銘柄 双日 三菱重工業 古河機械金属 三井海洋開発 | 古河機械金属の 2018-10-01 除外を確認。他3社の採否は出ず。2026-04 の新規採用はキオクシア・パンパシ |
| 8 | standard | TOPIX Core30 Large70 構成銘柄 2026 … JPX日経400 | 三菱重工業の Core30 追加（2024-10-31付）。2026-10 の入替結果は未取得 |
| 9 | standard | 2日の国債市場 新発10年債 利回り 11月2日 2026 | 11/2 は出ず。8/31 一時2.950%、9/1 3%突破、9/25 一時3.115%、10/6 10年債利率3.1% |
| 10 | standard | ドル円 10月の振り返り 2026年10月 … 10月31日 終値 | 松井 日銀為替市況：10/1 158.37〜40（月内最高終値）、10/23 156.95〜97（最安終値）、10/27 157.86〜87、10/30 157.55〜56 |
| 11 | standard | TOPIX 史上最高値 更新 終値 2026年10月 | 10/5 TOPIX 終値 4,145.22（松井）、1305 ETF 時系列、6/17 初の4,000台（4,013.23） |
| 12 | standard | 日本銀行 金融政策決定会合 2026年 開催予定日 12月 | 第三者サイト：12/17〜18。日銀公式の2027年日程文書に「2026年12月会合の議事要旨は 2027-01-27 公表」 |
| 13 | standard | federalreserve.gov FOMC meeting calendar 2026 December | 12/8〜9（決定は12/9 14:00 ET）。stockhub.kr のみ 12/16 |
| 14 | **extended** | Japan 10-year government bond yield November 2 2026 | **11/2 2.77%（変わらず、一時2.785%）**、Investing 終値2.774、MUFG 予想レンジ 2.650〜3.000% |
| 15 | standard | JPX日経インデックス400 構成銘柄 定期入替 2026年 … | 2026-08-07 発表：45追加・39除外（8/31 算出分から）。4銘柄の採否は不明 |
| 16 | standard | レアアース関連株 2026年10月 急騰 急落 同日 … | 10/26 レアアース関連の一角が買われた（SBI、時事報道が材料）。1/6〜7 の中国輸出管理強化と1/7 の反落（PayPay証券） |

---

## 7. 出所一覧（本ノートで新たに参照したURL）

- Snowball Analytics: https://snowball-analytics.com/public/asset/6269.TSE ／ https://snowball-analytics.com/public/asset/2768.TSE ／ https://snowball-analytics.com/public/asset/7011.TSE ／ https://snowball-analytics.com/public/asset/5715.TSE.JPY
- Disfold 6269: https://disfold.com/stock/jpx-6269/
- Simply Wall St: https://www.simplywall.st/stocks/jp/energy/tse-6269/modec-shares ／ https://simplywall.st/stocks/jp/capital-goods/tse-5715/furukawaltd-shares
- NYU Stern V-Lab: https://vlab.stern.nyu.edu/volatility/VOL.6269%3AJP-R.GARCH ／ https://vlab.stern.nyu.edu/volatility/VOL.6269%3AJP-HL.MEM ／ https://vlab.stern.nyu.edu/volatility/VOL.6269%3AJP-HL.AMEM ／ https://vlab.stern.nyu.edu/volatility/VOL.5715%3AJP-R.GARCH ／ https://vlab.stern.nyu.edu/volatility/VOL.5715%3AJP-HL.MEM
- Investing.com 6269 時系列: https://vn.investing.com/equities/modec-inc-historical-data
- Yahoo Finance: https://finance.yahoo.com/quote/2768.T/ ／ https://finance.yahoo.com/quote/MHVYF
- getquin / Parqet / Motley Fool: https://app.getquin.com/database/JP3663900003 ／ https://app.parqet.com/en/stocks/sojitz-JP3663900003 ／ https://www.fool.com/quote/tyo/2768/
- Rendement Bourse 7011: https://rendementbourse.com/7011-mitsubishi-heavy-industries
- TradingView: https://tw.tradingview.com/symbols/NAG-7011/forecast-price-target/ ／ https://de.tradingview.com/symbols/TSE-5715/
- Fintel 5715: https://fintel.io/s/jp/5715
- GuruFocus: https://www.gurufocus.com/stock/FRA:FUR/summary ／ https://www.gurufocus.com/stock/STU:FUR/summary
- 日経平均プロフィル（2018年9月 定期入れ替え）: https://indexes.nikkei.co.jp/atoz/2018/09/9w4.html
- PayPay証券（日経225 2026年4月入替）: https://media.paypay-sec.co.jp/cat5/jisha260309 ／（1月の中国輸出管理強化）: https://media.paypay-sec.co.jp/cat5/f260128
- TOPIX サイズ指数: https://www.weblio.jp/content/TOPIX_Core30 ／ https://www.weblio.jp/content/TOPIX+Large+70 ／ https://kabu.com/glossary/kabu2248.html ／ https://www.daiwa.jp/glossary/YST3503.html ／ https://www.jpx.co.jp/markets/indices/factsheets/files/002_1_02_fac2_size_TOPIX%20Large70.pdf ／ https://www.jpx.co.jp/corporate/news/news-releases/0060/t13vrt000000cg4e-att/cal2_12_size.pdf
- JPX日経400 2026年8月入替: https://www.jpx.co.jp/news/6030/t13vrt000001om22-att/data_j.pdf ／ https://www.jpx.co.jp/news/6030/t13vrt000001om22-att/data1_j.pdf ／ https://www.bridge-salon.jp/upload/tekiji_pdf/T~~81300~000000~1402~0~20260824~1000~20260820523690G.pdf ／ https://www.jpx.co.jp/news/1044/nlsgeu000004hy72-att/deta-j.pdf
- 長期金利: https://tradingeconomics.com/japan/government-bond-yield ／ https://www.investing.com/rates-bonds/japan-10-year-bond-yield-historical-data ／ https://rallies.ai/news/jgb-yields-edge-up-ahead-of-series-of-auctions-e4d7d4b52ea359ec ／ https://www.mufgresearch.com/rates/japan-economic-financial-weekly-2-november-2026 ／ https://kumanichi.com/articles/2043510 ／ https://kumanichi.com/articles/2030791 ／ https://kumanichi.com/articles/2034805 ／ https://www.sakigake.jp/news/article/20260119CO0102/
- ドル円: https://finance.matsui.co.jp/news/631057/index ／ https://finance.matsui.co.jp/news/631507/index ／ https://gmo-aozora.com/fx/report/pdf/USD_JPY_202608.pdf ／ https://gmo-aozora.com/fx/report/pdf/USD_JPY_202607.pdf
- TOPIX: https://finance.matsui.co.jp/news/624416/index ／ https://www.traders.co.jp/stocks/00_1305/historical ／ https://english.adnkronos.com/2026/06/17/nikkei-topix-hit-all-time-closing-highs/
- 日銀: https://www.boj.or.jp/mopo/mpmsche_minu/index.htm ／ https://www.boj.or.jp/mopo/mpmsche_minu/m_ref/mref260731a.pdf ／ https://www.moocota.com/mpm-nittei/ ／ https://www.invest-concierge.com/posts/boj-policy-meeting-guide
- FOMC: https://fedratecalc.com/fomc-meeting-schedule/december-2026/ ／ https://www.calendarx.com/events/fomc-meeting-december-2026 ／ https://thriveinmarkets.com/calendar/dates/fomc-2026/ ／ https://www.financecalendar.com/fomc-meetings/ ／ https://stockhub.kr/en/fomc-schedule ／ https://www.chicagofed.org/utilities/about-us/federal-reserve-calendars
- レアアース同日連動: https://go.sbisec.co.jp/media/report/dom_em_weekly/dom_em_weekly_261028.html
