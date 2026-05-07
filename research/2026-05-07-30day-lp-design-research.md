# 30 日チャレンジ LP 設計リサーチ

最終更新: 2026-05-07
担当: Engineer Agent (UX/Web リサーチ)
対象 LP: `yarushika-site/yarushika/30day-challenge.html`（現状版）

---

## TL;DR

- **採用すべき構成 Top 1**: 「**スティッキーな iPhone モックアップ + 縦スクロール・タイムライン**」のハイブリッド型。Pokémon Sleep / Headspace / Apple 製品ページが採用する「**スクロール = 進行**」のメンタルモデルを 30 日チャレンジに自然に重ねられる。固定された iPhone 内のスクショが Day 1 → Day 11 → Day 21 と切り替わる演出が最小コストで「段階解放」を可視化する。
- **参考にすべき LP Top 3**: ① Pokémon Sleep（キャラクター + 段階開示の最良見本）／② Headspace（イラスト主導 + コピーの簡潔さ）／③ Calm（ヒーローでムードを 1 秒で伝える美しさ）。
- **避けるべきパターン Top 3**: ① いきなりスクショを並べる「機能列挙型」（Day1 から全画面見せる＝ハントレ流に矛盾）／② カラフル多色＋エフェクト過多（中高生＝ Gen Z 文脈で「アニメ広告っぽい」と一蹴される）／③ Hero に CTA がない or スクロール後のみに CTA がある構成（Above the fold CTA は鉄則）。
- **シカDO の現状版**は読み物としては成立しているが、**ファーストビューでの「30 日で何が起きるか」の可視化が弱い**。コンセプトドキュメントの「30 日の地図」を LP の Hero にそのまま昇華すべき。

---

## 1. 優秀 LP 事例分析（カテゴリ別）

### 1.1 教育・学習系

#### Duolingo（duolingo.com）
- **強み**: ストリーク文化の中心。streak が 60% エンゲージ向上、7 日継続ユーザーは 3.6 倍長期定着というデータを LP/OS 両方で活用 ([Orizon](https://www.orizon.co/blog/duolingos-gamification-secrets), [StriveCloud](https://www.strivecloud.io/blog/gamification-examples-boost-user-retention-duolingo))。
- **構成**: 「言語選択カード → スタートボタン → 統計（ユーザー数）→ メソッド説明 → 教師/科学者の推薦 → CTA」と直線的。
- **ビジュアル**: フクロウ Duo は HERO ではなく「ボタン横」「セクション間」に挟まる小ぶり配置。色は意味付け済み（緑=成功・赤=ハート・橙=streak）。
- **シカDO 適用度**: ★★★☆☆。`streak` の概念設計（数値・カラー・配置）はそのまま流用可。ただし「言語選択カード」のような **大きなディシジョン要素** は 30 日チャレンジ LP には不要。

#### Studyplus（app.studyplus.jp）
- **強み**: 大学受験生の **2 人に 1 人**（62.3%）が利用、という社会的証明を強烈に打ち出す ([Studyplus IR](https://info.studyplus.co.jp/678))。
- **構成**: 「学習記録 → グラフ可視化 → 仲間と励まし合う → 進路サポート → DL CTA」。中高生視点の **シーン別ビジュアル**（教室、自室、塾）が多い。
- **ビジュアル**: 写真 + 実際のアプリ UI スクショ。イラストよりリアル写真寄り（受験生の "本気" モードに合わせる）。
- **シカDO 適用度**: ★★★☆☆。「ペアと比較する Before/After」「数字での社会的証明」は手堅い手法。ただしシカDO は買い切り ¥300 で受験ガチ勢ではないので、**写真リアル系よりキャラ系のままが正解**。

#### Drops（languagedrops.com）
- **強み**: 単語ごとの **個別イラスト** が世界観を作り、UI が語学学習でなく「絵本めくり」に見える ([DesignRush](https://www.designrush.com/best-designs/apps/drops))。
- **構成**: ヒーロー = 巨大な単語 + イラスト → 「5 分で集中」コピー → 言語数 → DL。
- **シカDO 適用度**: ★★★★☆。「**1 概念 = 1 イラスト**」の徹底はシカ先輩 7 表情を活かす設計の参考になる。Phase 1/2/3 ごとにシカの **表情を変える** だけで段階感が伝わる。

### 1.2 習慣化・ライフスタイル系

#### Headspace（headspace.com）
- **強み**: イラストがブランドそのもの。曲線的・色味温かめ・無害な形のキャラで、"瞑想＝怖くない" を視覚で言い切る ([Blush Blog](https://blush.design/blog/post/headspace-mindfulness-app), [Lapa Ninja](https://www.lapa.ninja/post/headspace/))。
- **構成（2026 現在）**: Hero「Stress less all with Headspace」+ "Try for $0" → **「どんな headspace を探してる？」6 経路カード**（stress / sleep / anxiety / processing / meditation / therapy）→ 社会的証明 → B2B → コンテンツ図書館 → FAQ。
- **特筆**: 「Need Assessment」セクションで **訪問者の気分にラベルを貼ってから** ソリューションに誘導する流れ。LP 全体が "ユーザーの内面" を起点に組まれている。
- **シカDO 適用度**: ★★★★★。「**最初から全機能を押し付けない**」というシカDO の核と、Headspace の「あなたが求めてる headspace は？」の **共感先行型構造** は完全一致。Hero 直下に「**今のあなた、こうじゃない？**」セクションを置くのが正解。

#### Calm（calm.com）
- **強み**: フルスクリーンの **山と湖の動画** が 1 秒で「落ち着き」を伝える。コピー "Calm your mind. Change your life." は 8 単語で完結 ([Lapa Ninja](https://www.lapa.ninja/post/calm/), [Designity](https://www.designity.com/blog/landing-page-examples))。
- **構成**: 環境ビデオ → 短文ヒーロー → "Try Calm for Free" → 機能セクション数枚 → ストア DL。
- **シカDO 適用度**: ★★★☆☆。Calm の「ムードで攻める」アプローチは 30 日チャレンジには冗長。ただし **Hero の文字数を絞る教訓** は強く参考にすべき（現状 LP は Hero テキスト多すぎ）。

#### Streaks（streaksapp.com）
- **強み**: 「巨大な円をタップして塗りつぶす」UI を **そのまま LP のヒーロービジュアルに流用** ([Schezy 2025](https://schezy.com/blog/best-habit-tracker-apps-2025))。アプリのコア体験 = LP の主役。
- **シカDO 適用度**: ★★★★☆。30 日チャレンジでも「**Day カウンター + シカ先輩**」のセットを LP の主役オブジェクトにできる。スクロールに応じて Day カウンターが進む演出で「30 日を体感」させる。

#### Finch（finchcare.com）
- **強み**: "Your New Self-Care Best Friend" の一言で **キャラ = 友達** を提示。マスコット（Finch という鳥 = "birb"）が UX の中心 ([Tubik Studio](https://blog.tubikstudio.com/design-me-live-the-power-of-mascots-in-ui-and-branding/))。
- **シカDO 適用度**: ★★★★★。「**シカ先輩 = 30 日伴走するツンデレ友達**」の打ち出しは Finch のフレーミングそのまま流用可能。Hero コピー候補:「**30 日、伴走するツンデレ鹿。**」。

### 1.3 ゲーム・キャラクター活用系

#### Pokémon Sleep（pokemonsleep.net/en/）
- **強み**: ヒーロー "This sleep app gives you something fun to look forward to when you wake up" — **ベネフィットを 1 文で要約**しつつ、ポケモンというキャラクター IP の力を活用 ([Pokemon Sleep](https://www.pokemonsleep.net/en/))。
- **構成**: ロゴ + ヒーロー + DL ボタン → 「Sleep Tracking: Rest your very best!」→ 「Pokémon: Research sleep styles!」→ ニュース → Twitter フィード（社会的活気）。
- **特筆**: **「Sleep Tracking」と「Pokémon」のセクションが交互に出る**こと。機能セクションだけだと退屈、キャラセクションだけだと中身が伝わらない、を **交互設計** で解決している。
- **シカDO 適用度**: ★★★★★。「機能（段階解放）」と「キャラ（シカ先輩）」を **交互レイヤード** にする構成は LP に直接反映可能。Phase 1 説明 → シカ先輩 Phase 1 のセリフ → Phase 2 説明 → Phase 2 セリフ……の流れ。

### 1.4 段階解放・コース系

#### MasterClass / Coursera コース紹介ページ
- **強み**: 各レッスン/モジュールが **積み上げ式に並ぶ縦リスト**。Progress bar、レッスン番号、所要時間で「ゴールまでの距離」を視覚化 ([Leadpages](https://leadpages.com/blog/course-landing-page-examples))。
- **特筆**: 「各モジュールは独立して成立しつつ、順序通り進めると最大効果」という **二層構造** を LP で表現する手法が確立されている。
- **シカDO 適用度**: ★★★★☆。Day 1〜10 / Day 11〜20 / Day 21〜30 を「**3 章のミニコース**」として並べる演出が成立する。ただし、シカDO の場合は **解放されるまで未来は見えない**（地図は最初に 1 度だけ見せる）演出のほうがツンデレ世界観に合う。

### 1.5 日本アプリ LP

#### Monoxer（corp.monoxer.com）
- **強み**: 中学生・高校生・小学生で **学年別ケーススタディページ** を分けて訴求軸をピンポイント化 ([Monoxer 中学生](https://corp.monoxer.com/case_cate/junior/))。
- **シカDO 適用度**: ★★☆☆☆。シカDO は対象学年内で UI 差別化していないので、ケース分けは過剰。ただし「**保護者向け FAQ**」という形で対象別セクションを 1 つ持つのは検討価値あり。

#### スタディサプリ
- **強み**: 「進学実績」「講師の実績」「生徒の成績向上率」など **数字での説得** を徹底 ([ZEROラボ](https://zero-s.jp/labo/?p=14969))。
- **シカDO 適用度**: ★★☆☆☆。シカDO はリリース直後で実績数字が薄い。代わりに **「30 日後にこうなる」という体験ストーリー** を実績の代用にする。

#### 日本 LP デザイントレンド 2025-2026
- 余白を **意図的に活用**（情報グルーピング、視線誘導）が標準化 ([CV Labo 2025](https://conversion-labo.jp/report/lp_design/13771/))。
- 手書き風イラスト・コラージュ・落書きフォントが「親しみ」のキーワード ([kisa illustration & design 2025](https://kisa.ne.jp/design/trend-2025/))。
- ポップなキャラクター + キャンディカラー + 軽量 3D 表現がトレンド ([fukuoka-creative 2025](https://fukuoka-creative.jp/20250306-design-trend))。

→ シカDO のウォームパレット（ベージュ + ピンク）は完全にトレンド軸上。手書き風シカは現存資産で対応済み。

---

## 2. 「段階解放ストーリー」のベスト構成 4 つの比較

### 2.1 タイムライン型
**構造**: 縦スクロールで Day 1 → 30 が時系列に流れる。各 Phase の節目に大きなマイルストーンマーカー。
**例**: Coursera のシラバス、Strava のトレーニングプラン LP。
**メリット**: 直感的。「30 日」という時間軸が体感できる。スクロール = 時間進行のメンタルモデルが強力。
**デメリット**: 縦に長くなりがち。途中離脱率が上がる。
**シカDO 推奨度**: ★★★★★。30 日 = 時間 = スクロール、の図式が完全に成立。

### 2.2 3 カードグリッド型
**構造**: Phase 1 / Phase 2 / Phase 3 を横並び 3 カードで並べる。
**例**: SaaS の料金プラン、Apple の "Choose your iPhone"。
**メリット**: 1 画面で全体像が見える。比較しやすい。
**デメリット**: 「順番に解放される」感が出ない。並列に見えると "好きなのを選んでいい" と誤解される。
**シカDO 推奨度**: ★★☆☆☆。「30 日の地図」セクションのみ 3 カード採用、本編はタイムラインに。

### 2.3 インタラクティブステップ型
**構造**: クリック/タップで各 Phase の詳細が展開される。アコーディオン or タブ。
**例**: Notion の機能紹介、Apple Watch の文字盤紹介。
**メリット**: 縦長を避けられる。ユーザー主導で深堀り。
**デメリット**: モバイルで操作が煩雑。スクロールだけで読みたい層を逃す。JS が必要。
**シカDO 推奨度**: ★★☆☆☆。FAQ には適するが本編には不要。

### 2.4 アニメ動画埋め込み型
**構造**: 30 秒〜90 秒のアニメ動画で Day 1 → 30 を一気に見せる。
**例**: Headspace の "Why mindfulness?"、Calm の Sleep Story 紹介動画。
**メリット**: 圧倒的没入感。1 度見れば全体像が頭に入る。
**デメリット**: 制作コスト高（15-30 万）。再生されないと無意味。モバイル通信に厳しい。
**シカDO 推奨度**: ★★★☆☆。Phase 2 で動画版に進化させる将来案。**初版は静的でいく**。

| 構成 | 直感性 | 制作工数 | リッチさ | モバイル | シカDO 推奨度 |
|---|---|---|---|---|---|
| 2.1 タイムライン型 | ★★★★★ | ★★★ | ★★★★ | ★★★★★ | **★★★★★** |
| 2.2 3 カードグリッド | ★★★ | ★★ | ★★★ | ★★★★ | ★★☆☆☆ |
| 2.3 インタラクティブ | ★★★ | ★★★★ | ★★★★ | ★★ | ★★☆☆☆ |
| 2.4 アニメ動画 | ★★★★★ | ★★★★★ | ★★★★★ | ★★★ | ★★★☆☆（将来） |

→ **採用案**: 「**Hero で 3 カード地図 → 本編はタイムライン**」のハイブリッド。最初に全体像を 1 画面で見せ、スクロールで詳細に降りていく。

---

## 3. 中高生向け「映える」デザイン要素

中高生 = 完全な Z 世代。マーケ調査複数結果と日本 LP トレンドから:

### フォント
- **丸ゴシック（M PLUS Rounded 1c）はそのまま正解**。Z 世代は「親しみやすさ + 手書き感」を好む ([COAX](https://medium.com/coax-software-blog/design-hacks-for-gen-z-fonts-captions-and-color-palette-5242ef6a8dd0))。
- **サイズはやや大きめ**（本文 16-18px、見出し 28-40px）。スマホ片手読みで指が画面の半分を遮るため。
- **Hero のメインコピーだけは "ぐっと太く"**（700-900 ウェイト）。Z 世代は「弱い書体 = ノイズ」と認識する。

### 余白
- **窮屈はダメ**。日本 LP トレンド 2025 では「**余白＝情報グルーピング装置**」が共通認識 ([CV Labo](https://conversion-labo.jp/report/lp_design/13771/))。
- セクション間に **80-120px の縦余白** を取る。狭い余白は「広告っぽい」と嫌われる。

### 色数
- **メイン 1 色 + アクセント 1 色 + 背景** に絞る。シカDO のパレットはこの規律をすでに守っている。
- **Z 世代に多色派は刺さらない**（疲れる、誠実さがない印象）。代わりに **同色のグラデーションで奥行き** を出す。

### アニメーション
- **CSS のみで完結する fade-in / slide-up が無難**。Lottie や GSAP はファイルサイズで離脱を生む。
- **scroll-driven animations**（CSS の `animation-timeline: view()`）は 2026 現在 Chromium + Safari 18+ でネイティブ対応 ([MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Scroll-driven_animations/Timelines)、[Josh W. Comeau](https://www.joshwcomeau.com/animation/scroll-driven-animations/))。Intersection Observer フォールバックで全カバー可能。

### 絵文字 / イラスト密度
- **絵文字は 1 セクション 1 個まで**。多用は LINE スタンプ感が出て幼くなる。
- **シカ先輩イラストは "セクションの主役" として大きく**。サムネ扱いは禁。Phase 1: 控えめ表情、Phase 2: ガッツポーズ、Phase 3: 目を細めて遠くを見る、卒業: 笑顔、と表情変化で進行を見せる。

---

## 4. アプリ LP 必須要素チェックリスト

NN/g、TyrAds、Webstacks、Adjust の 2025-2026 ベストプラクティスから ([TyrAds](https://tyrads.com/mobile-app-landing-page/), [Adjust](https://www.adjust.com/blog/app-landing-pages/)):

### Above the fold で必須
- [ ] **ヘッドライン**（10-15 文字、ベネフィット 1 文）
- [ ] **サブヘッドライン**（補足、20-30 文字）
- [ ] **キービジュアル**（シカ + Day メーター を想定）
- [ ] **CTA ボタン**（"App Store でダウンロード" 視認性 ★ 最大）
- [ ] **価格 / 対応 OS のミニ表記**（信頼性）

### スクリーンショット
- **3-5 枚** を縦スクロール内に分散配置（10 枚以上は離脱）。
- iPhone モックアップ枠で囲む（CSS で実装可、devices.css 等）。
- スクショの **横にキャプション 1 文** を置く。「これは何画面？」を即答させる。

### CTA
- **3 回配置**（Hero + 中盤 + 末尾）。スクロールしながら「今押せばダウンロード」を切らさない。
- 表現は CTA 1: 「無料で見てみる」/ CTA 2: 「ダウンロードは ¥300」/ CTA 3: 「30 日チャレンジを始める」と **言葉を変える**。同文 3 連発は鬱陶しい。

### 信頼性パーツ
- [ ] **価格の明記**（買い切り ¥300、サブスクなし）
- [ ] **対応 OS**（iOS 17.4+）
- [ ] **プライバシー宣言**（データ収集なし、を 1 行で）
- [ ] **開発者の顔 or note リンク**（個人開発であることを隠さない）
- [ ] **App Store レビュー数 / 星**（リリース後）

### アクセシビリティ
- 本文コントラスト比 **4.5:1 以上**（現状ベージュ背景 #F5E6D3 + テキスト #3a2f28 は OK、要計測）。
- フォントサイズ **16px 以上**。
- 全画像に **alt テキスト**（特にシカ表情）。
- インタラクティブ要素は **44×44px 以上**（Apple HIG）。

---

## 5. 静的 HTML/CSS でできるリッチネス Tips

### CSS-only iPhone モックアップ
- `border-radius` + `box-shadow` + ノッチ用 `::before` で iPhone 枠を再現可能 ([CSS Script](https://www.cssscript.com/realistic-ios-mockup/), [Free Frontend](https://freefrontend.com/iphones-in-css/))。
- スクショは中に WebP で配置、**ファイルサイズは 1 枚 30-50 KB** に圧縮。
- ライブラリ採用なら `devices.css`（MIT ライセンス、純 CSS）。

### スクロール進行アニメーション
```css
/* 例: Phase カードがビューに入るとフェードアップ */
@supports (animation-timeline: view()) {
  .phase-card {
    animation: fadeUp linear;
    animation-timeline: view();
    animation-range: entry 0% cover 30%;
  }
}
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}
/* フォールバック */
@supports not (animation-timeline: view()) {
  .phase-card { /* JS Intersection Observer で .visible class を付与 */ }
}
```
- compositor thread で動くので **60fps 維持**、メイン thread をブロックしない ([Chrome Developer Blog](https://developer.chrome.com/blog/scroll-triggered-animations))。
- 旧 Safari（17 以下）には Intersection Observer JS 50 行のフォールバック。

### スティッキー iPhone + スクロール画像切替
- `position: sticky` で iPhone モックを画面中央に固定。
- 横の縦長 Phase 説明エリアがスクロールするにつれ、IO で iPhone 内の画像を `Phase1.webp` → `Phase2.webp` → `Phase3.webp` に切替。
- これだけで Apple iPhone ページ風の "重い" 演出が実現。

### グラデーション + シャドウ
- 単色塗りより **30 度方向のグラデーション**（accent → accent-deep）でリッチ感。
- シャドウは **二重 box-shadow**（近距離薄 + 遠距離濃）で立体感が増す。
  ```css
  box-shadow:
    0 1px 2px rgba(0,0,0,0.04),
    0 8px 24px rgba(235, 145, 120, 0.18);
  ```

### フォーマット
- 写真・スクショ: **WebP**（PNG の 1/3、AVIF はまだ Safari 弱い）。
- アイコン・シカイラスト: **SVG**（拡大縮小自由、ファイルサイズ最小）。
- LCP（Largest Contentful Paint） < 2.5 秒のため Hero 画像は preload。

---

## 6. シカDO 30 日チャレンジ LP の推奨構成（提案）

### セクション構成案

| # | セクション | 内容 | 視覚要素 | スクショ |
|---|---|---|---|---|
| 1 | **Hero** | 「30 日で、タスク管理が、身につく。」+ DL CTA | 大きめのシカ + Day 1 / 30 メーター | 不要（Hero に画像を盛りすぎない） |
| 2 | **共感パート** | 「タスク管理アプリ、最初から全部見せられても疲れる」 | シカが疲れた表情 + 散らかった画面のメタファー | 不要 |
| 3 | **ソリューション = 30 日の地図** | 3 段階解放のしくみを 1 画面で | 横並び 3 カード or 縦タイムライン縮小版 | 各 Phase に 1 枚（小） |
| 4 | **Phase 1 (Day 1〜10): 思いついたことを書く練習** | できるようになること / シカのスタンス | スティッキー iPhone に Box 画面 / シカ表情 1 | ✓ Box 画面 |
| 5 | **Phase 2 (Day 11〜20): 今日に集中する練習** | 「今日のリスト」が解禁、解説 | iPhone に Today 画面切替 / シカ表情 2 | ✓ Today 画面 |
| 6 | **Phase 3 (Day 21〜30): 先のことも書ける練習** | カレンダー解禁、解説 | iPhone にカレンダー / シカ表情 3 | ✓ カレンダー画面 |
| 7 | **Day 30 達成セレモニー** | 「身についた状態」の宣言 | 卒業バッジ風カード + シカ笑顔 | 卒業画面（あれば） |
| 8 | **お守り（サボり保険）の解説** | 失敗を許す設計の意味付け | 🛡 アイコン + シカのセリフ | お守りカード UI |
| 9 | **シカ先輩について** | キャラ深掘り、ツンデレ性格、Phase 別距離感 | シカ 4 表情並び（Phase 1/2/3/卒業） | 不要 |
| 10 | **はじめ方** | 新規 / 既存ユーザー両方の動線 | 2 カード（新規 / 既存） | オンボ画面 / 設定画面 |
| 11 | **FAQ** | 5 問のアコーディオン | アコーディオン UI | 不要 |
| 12 | **保護者向けミニセクション** | 価格・プライバシー・通知の頻度 | 緑チェック 3 行 | 不要 |
| 13 | **CTA Final** | App Store ダウンロード（再） | 大きい CTA + 価格 | App Store バッジ |
| 14 | **Footer** | 開発者リンク、note、X、トップへ戻る | リンク 4 つ | 不要 |

### 各セクションの設計意図メモ

- **#1 Hero**: 現状版は「30 日チャレンジって何？」とタイトルから入っているが、これは **見出しが質問形式 = 答えを後回しにする** 構造。Z 世代は答えを 3 秒で渇望する。「30 日で、タスク管理が、身につく。」と **3 文節で結論** を先出しする。
- **#2 共感パート**: 「全機能ドカ提供だと使えない」を Hero 直後に置く。Headspace の "What kind of headspace are you looking for?" 構造のシカDO 版。読者が「あ、自分のことだ」と思った瞬間、続きを読む確率が跳ね上がる。
- **#3 ソリューション**: ここが LP の頂点。「**最初は 1 つの画面 → 慣れたら 2 つ → 全機能**」を 1 画面で示す。**3 つの iPhone モック** を縦に並べて、それぞれ Day 1 / Day 11 / Day 21 のスクショを入れる。**1 番目だけ大きく、3 番目は小さくフェード** で「未来は徐々に見える」表現。
- **#4-6 Phase 詳細**: スティッキー iPhone モックアップ + 横にスクロールテキスト方式。Apple iPhone ページの「カメラ機能を 1 つずつ見せていく」と同じ手法。
- **#9 シカ先輩について**: コンセプトドキュメントに書かれている **Phase 別キャラ距離感** をビジュアル化する重要セクション。これを置かないとシカが装飾扱いになる。
- **#12 保護者向け**: シカDO の二次ターゲット。「価格 ¥300 一回だけ」「広告なし」「データ収集なし」「通知 1 日 3 回まで」の 4 つを **緑チェック + 1 行コピー** で簡潔に。

---

## 7. 必要なアセット一覧

### 撮影すべき iOS スクリーンショット（iPhone 16 Pro 6.3" シミュレータ）
1. **オンボ「30 日でタスク管理を身につける」選択画面**
2. **30 日の地図（オンボ直後のサマリー画面）**
3. **なんでもボックス画面**（Day 5 想定、4-5 件のタスク投入済み）
4. **Box 画面下部のシカ Day カード**（「あと N 日で…」表示）
5. **Today 画面解放直後のセレモニーモーダル**
6. **Today 画面**（Day 12 想定、3 件タスク）
7. **カレンダー解放セレモニーモーダル**
8. **カレンダー画面**（Day 23 想定、来週まで表示）
9. **Day 30 卒業セレモニー画面**
10. **お守りバッジ表示**（Box 画面の隅）
11. **設定画面の「30 日チャレンジ」セクション**
12. **App Store の DL ボタン**（バッジ素材）

→ 全て **PNG → WebP 変換 + 横幅 720px に縮小**。1 枚あたり 30-50 KB 目標。

### イラスト
- **シカ先輩 4 表情**:（既存 7 種から流用）
  - 控えめ（Phase 1）
  - ガッツポーズ or 並走（Phase 2）
  - 遠くを見る（Phase 3）
  - 笑顔・送り出し（卒業）
- **🛡 お守りアイコン**（SVG）
- **App Store バッジ**（Apple 公式素材）
- **Day カウンター リング SVG**（CSS でも可）

### コピー（要新規執筆）
- Hero メインコピー（10-15 文字）
- Hero サブコピー（20-30 文字）
- 各 Phase の 1 行サマリー（30-40 文字）
- 各 Phase でのシカ先輩のセリフ 1 つずつ
- お守りキャッチ
- 保護者向けチェックリスト 4 行

---

## 8. 実装ロードマップ提案

### Phase 1: ワイヤフレーム（半日）
- 上記セクション構成を Figma or Pen の 720px 1 カラム枠で確定
- スクショ配置位置決定
- コピー全文ドラフト
- 岡田さんレビュー → ロック

### Phase 2: デザイン詳細（1 日）
- カラー、タイポ、余白の詳細決定（既存 30day-challenge.html の CSS 変数を踏襲）
- iPhone モックアップ枠 CSS 確定
- スクロール演出（fade-up、sticky iPhone、画像切替）の実装方針
- アクセシビリティ：コントラスト比、alt テキスト全網羅

### Phase 3: HTML 実装（1.5 日）
- セマンティック HTML（`<section>`, `<article>`, `<details>`）で意味付け
- CSS scroll-driven animations + Intersection Observer フォールバック
- WebP 化と preload 設定
- iOS Safari / Chrome / Firefox で実機チェック
- Lighthouse スコア: Performance 90+ / Accessibility 100 / Best Practices 100 / SEO 100 を目標

### Phase 4: 公開（半日）
- `yarushika-site/yarushika/30day-challenge.html` を更新（既存と差し替え）
- Vercel に push、本番動作確認
- index.md / 既存リンクの整合
- X 固定ツイートに新 LP リンクを差し替え（任意）

合計 **3.5 日**程度の実装ボリューム想定。

---

## 出典・参考リンク

### 教育・学習系 LP
- [Duolingo Gamification Secrets — Orizon](https://www.orizon.co/blog/duolingos-gamification-secrets)
- [Duolingo Gamification — StriveCloud](https://www.strivecloud.io/blog/gamification-examples-boost-user-retention-duolingo)
- [Studyplus 大学受験生 60% 利用 — info.studyplus](https://info.studyplus.co.jp/678)
- [Monoxer 中学生事例](https://corp.monoxer.com/case_cate/junior/)
- [Drops App Design — DesignRush](https://www.designrush.com/best-designs/apps/drops)

### 習慣化・ライフスタイル系 LP
- [Headspace Landing Page — Lapa Ninja](https://www.lapa.ninja/post/headspace/)
- [Headspace Illustrations — Blush Blog](https://blush.design/blog/post/headspace-mindfulness-app)
- [Calm Landing Page — Lapa Ninja](https://www.lapa.ninja/post/calm/)
- [Streaks 2025 — Schezy](https://schezy.com/blog/best-habit-tracker-apps-2025)
- [The Power of Mascots in UI and Branding — Tubik Studio](https://blog.tubikstudio.com/design-me-live-the-power-of-mascots-in-ui-and-branding/)

### キャラクター活用系
- [Pokémon Sleep Official](https://www.pokemonsleep.net/en/)

### 段階解放・コース系
- [Course Landing Page Examples — Leadpages](https://leadpages.com/blog/course-landing-page-examples)
- [Progressive Disclosure — UXPin](https://www.uxpin.com/studio/blog/what-is-progressive-disclosure/)

### 日本 LP デザイントレンド
- [LPデザイン余白の使い方 2025 — CV Labo](https://conversion-labo.jp/report/lp_design/13771/)
- [2025 デザイン・イラストトレンド — kisa](https://kisa.ne.jp/design/trend-2025/)
- [2025 デザイントレンド5選 — fukuoka-creative](https://fukuoka-creative.jp/20250306-design-trend)
- [塾・予備校 LP 重要ポイント — ZEROラボ](https://zero-s.jp/labo/?p=14969)

### Z 世代デザイン
- [Design Hacks for Gen Z — COAX](https://medium.com/coax-software-blog/design-hacks-for-gen-z-fonts-captions-and-color-palette-5242ef6a8dd0)
- [Designing for Gen Z 2025 — Adtakenseo](https://medium.com/@adtakenseo11/designing-for-gen-z-in-2025-the-psychology-of-color-and-typography-for-younger-audiences-e121836d29bb)

### アプリ LP ベストプラクティス
- [Mobile App Landing Page Best Practices 2025 — TyrAds](https://tyrads.com/mobile-app-landing-page/)
- [App Landing Pages 2026 — Unicorn Platform](https://unicornplatform.com/blog/app-landing-pages-for-mobile-products-in-2026/)
- [Mobile Landing Page Examples 2025 — Webstacks](https://www.webstacks.com/blog/mobile-landing-page)
- [Create Mobile App Landing Page — Adjust](https://www.adjust.com/blog/app-landing-pages/)

### 技術: CSS / モックアップ / アニメーション
- [Realistic iOS Mockup In Pure CSS — CSS Script](https://www.cssscript.com/realistic-ios-mockup/)
- [Pure CSS iPhone Examples — Free Frontend](https://freefrontend.com/iphones-in-css/)
- [Modern Device Mockups With Devices.css — Medium](https://medium.com/javascript-in-plain-english/modern-device-mockups-with-devices-css-63286ca32859)
- [Scroll-driven Animations — MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Scroll-driven_animations/Timelines)
- [Scroll-Driven Animations — Josh W. Comeau](https://www.joshwcomeau.com/animation/scroll-driven-animations/)
- [CSS Scroll-Triggered Animations — Chrome for Developers](https://developer.chrome.com/blog/scroll-triggered-animations)

### 内部資料
- 現状 LP: `yarushika-site/yarushika/30day-challenge.html`
- コンセプト: `.kiro/specs/v1.5-30day-beginner-mode/concept-narrative.md`
- LP MD 元: `yarushika-site/30day-challenge.md`
