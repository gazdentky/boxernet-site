---
layout: default
title: 自販機横リサイクルボックス溢れ問題｜構造分析サマリー | 株式会社Boxernet
description: 東京都内30〜40万台の自販機横リサイクルボックスが常時溢れる構造的要因を8つに分解し、東京都にとっての6つの政策的課題と統合的に整理。Tokyo Social Innovation Tech Award 2026 応募関連資料。
keywords: リサイクルボックス,自販機,溢れ問題,異物混入,ゼロエミッション東京,スマートシティ,つぶすくん,Boxernet,プラスチック資源循環促進法
permalink: /insights/recycle-overflow/
---

<style>
/* =========================================================
   リサイクルボックス溢れ問題ページ専用スタイル
   既存 site CSS と干渉しないよう、クラス名は全て "ro-" プレフィックス
   ========================================================= */
.ro-hero{
  background:linear-gradient(135deg,#0a1430 0%,#0B5FFF 100%);
  color:#fff;padding:72px 28px 80px;border-radius:18px;
  position:relative;overflow:hidden;margin-bottom:48px;
}
.ro-hero::after{
  content:"";position:absolute;right:-120px;top:-120px;
  width:520px;height:520px;
  background:radial-gradient(circle,rgba(0,198,169,.22) 0%,rgba(0,198,169,0) 60%);
  pointer-events:none;
}
.ro-hero-inner{position:relative;z-index:2;max-width:920px;}
.ro-badge{
  display:inline-block;font-size:11px;letter-spacing:.18em;
  background:rgba(0,198,169,.18);color:#7ff0db;
  padding:6px 12px;border-radius:999px;border:1px solid rgba(0,198,169,.4);
  margin-bottom:18px;font-weight:600;
}
.ro-hero h1{
  font-size:clamp(22px,3.4vw,34px);font-weight:800;color:#fff;
  line-height:1.3;margin:0 0 18px;
}
.ro-hero h1 em{color:#00C6A9;font-style:normal;}
.ro-hero .ro-sub{font-size:clamp(14px,1.55vw,16px);color:#cfd8ee;line-height:1.8;margin-bottom:18px;}
.ro-meta{font-size:12px;color:#9fb1d6;letter-spacing:.04em;}

.ro-section{margin:64px 0;}
.ro-eyebrow{
  font-size:11px;letter-spacing:.2em;color:#0B5FFF;font-weight:700;
  text-transform:uppercase;margin-bottom:8px;
}
.ro-section h2{
  font-size:clamp(20px,2.6vw,28px);font-weight:800;color:#0a1430;
  line-height:1.3;margin:0 0 16px;border-left:5px solid #00C6A9;
  padding-left:14px;
}
.ro-section h3{
  font-size:clamp(17px,2.0vw,20px);font-weight:700;color:#0a1430;
  line-height:1.4;margin:28px 0 10px;
}
.ro-lead{
  font-size:15px;color:#3a4868;line-height:1.85;margin:0 0 24px;
}
.ro-callout{
  background:linear-gradient(135deg,#f5f8ff 0%,#e8f7f3 100%);
  border-left:4px solid #00C6A9;
  border-radius:10px;padding:20px 24px;margin:24px 0;
  font-size:14.5px;line-height:1.85;color:#0a1430;
}

.ro-table{
  width:100%;border-collapse:collapse;background:#fff;
  border-radius:12px;overflow:hidden;box-shadow:0 8px 24px rgba(11,95,255,.06);
  margin:24px 0;
}
.ro-table th,.ro-table td{
  padding:14px 16px;text-align:left;border-bottom:1px solid #e5ebf5;
  font-size:13.5px;line-height:1.7;vertical-align:top;
}
.ro-table th{background:#0B5FFF;color:#fff;font-weight:700;font-size:13px;letter-spacing:.04em;}
.ro-table td:first-child{font-weight:600;color:#0a1430;width:34%;}
.ro-table tr:last-child td{border-bottom:none;}
.ro-table tr:nth-child(even) td{background:#fafbff;}

.ro-factors{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;margin:24px 0;}
.ro-factor{
  background:#fff;border:1px solid #e5ebf5;border-radius:12px;
  padding:24px;box-shadow:0 8px 24px rgba(11,95,255,.06);
  position:relative;
}
.ro-factor-num{
  position:absolute;top:-12px;left:20px;
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);color:#fff;
  font-size:12px;font-weight:700;letter-spacing:.1em;
  padding:5px 12px;border-radius:999px;
}
.ro-factor h4{
  font-size:16px;font-weight:700;margin:8px 0 10px;color:#0a1430;line-height:1.45;
}
.ro-factor p{
  font-size:13.5px;color:#3a4868;line-height:1.85;margin:0;
}
.ro-factor .ro-implication{
  margin-top:12px;padding-top:12px;border-top:1px dashed #e5ebf5;
  font-size:12.5px;color:#0B5FFF;font-weight:600;
}

.ro-issues{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;margin:24px 0;}
.ro-issue{
  background:linear-gradient(180deg,#fff 0%,#f5f8ff 100%);
  border:1px solid #e5ebf5;border-radius:12px;
  padding:24px;
}
.ro-issue-head{
  display:flex;align-items:center;gap:12px;margin-bottom:12px;
}
.ro-issue-no{
  width:36px;height:36px;border-radius:50%;
  background:#0B5FFF;color:#fff;font-weight:800;font-size:14px;
  display:flex;align-items:center;justify-content:center;flex-shrink:0;
}
.ro-issue h4{font-size:15.5px;font-weight:700;margin:0;color:#0a1430;line-height:1.4;}
.ro-issue p{font-size:13.5px;color:#3a4868;line-height:1.85;margin:0;}

/* 悪循環の構造図 */
.ro-cycle{
  display:flex;flex-direction:column;align-items:stretch;
  max-width:760px;margin:32px auto;gap:0;
}
.ro-cycle-step{
  background:#fff;border:2px solid #0B5FFF;border-radius:12px;
  padding:18px 22px;display:flex;align-items:flex-start;gap:14px;
  box-shadow:0 6px 18px rgba(11,95,255,.08);
}
.ro-cycle-step:nth-child(even){border-color:#00C6A9;}
.ro-cycle-num{
  flex-shrink:0;width:48px;height:48px;border-radius:50%;
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);color:#fff;
  display:flex;align-items:center;justify-content:center;
  font-weight:800;font-size:13px;letter-spacing:.05em;
}
.ro-cycle-body h4{
  margin:0 0 6px;font-size:15px;font-weight:700;color:#0a1430;line-height:1.4;
}
.ro-cycle-body p{margin:0;font-size:13px;color:#3a4868;line-height:1.7;}
.ro-cycle-arrow{
  text-align:center;color:#0B5FFF;font-size:22px;line-height:1;
  padding:8px 0;font-weight:700;
}
.ro-cycle-loop{
  text-align:center;font-size:12.5px;color:#6b7a99;
  margin-top:12px;font-style:italic;
}

/* 介入レイヤー */
.ro-layers{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;margin:24px 0;}
.ro-layer{
  background:#fff;border-radius:12px;padding:24px;
  border-top:4px solid #0B5FFF;box-shadow:0 8px 24px rgba(11,95,255,.06);
}
.ro-layer:nth-child(2){border-top-color:#00C6A9;}
.ro-layer:nth-child(3){border-top-color:#7C3AED;}
.ro-layer-tag{
  font-size:11px;letter-spacing:.18em;color:#6b7a99;
  font-weight:700;text-transform:uppercase;margin-bottom:6px;
}
.ro-layer h4{
  font-size:16px;font-weight:700;color:#0a1430;margin:0 0 10px;
}
.ro-layer p{font-size:13px;color:#3a4868;line-height:1.8;margin:0;}

/* 価値リスト */
.ro-values{
  display:grid;grid-template-columns:repeat(2,1fr);gap:14px;margin:24px 0;
}
.ro-value{
  background:#fff;border:1px solid #e5ebf5;border-radius:10px;
  padding:16px 20px;display:flex;align-items:flex-start;gap:12px;
}
.ro-value-num{
  flex-shrink:0;font-size:13px;font-weight:800;color:#0B5FFF;
  background:#f5f8ff;border-radius:6px;padding:4px 9px;letter-spacing:.04em;
}
.ro-value p{margin:0;font-size:13.5px;color:#0a1430;line-height:1.7;}

/* 参考文献 */
.ro-refs{
  background:#f5f8ff;border-radius:12px;padding:24px 28px;margin:24px 0;
}
.ro-refs ol{margin:0;padding-left:22px;}
.ro-refs li{
  font-size:13px;color:#3a4868;line-height:1.85;margin-bottom:8px;
}

/* CTA */
.ro-cta{
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);
  color:#fff;border-radius:18px;padding:48px 32px;text-align:center;margin-top:56px;
}
.ro-cta h3{font-size:24px;margin:0 0 12px;font-weight:800;color:#fff;}
.ro-cta p{font-size:14.5px;margin-bottom:24px;opacity:.95;line-height:1.8;}
.ro-cta-btn{
  display:inline-block;background:#fff;color:#0B5FFF;
  padding:13px 28px;border-radius:10px;font-weight:700;font-size:14px;
  text-decoration:none;letter-spacing:.04em;margin:4px 6px;
}
.ro-cta-btn.ro-cta-btn-outline{
  background:transparent;color:#fff;border:2px solid #fff;
}
.ro-cta-btn:hover{opacity:.9;}

@media (max-width:768px){
  .ro-factors,.ro-issues,.ro-layers,.ro-values{grid-template-columns:1fr;}
  .ro-hero{padding:52px 22px 60px;}
  .ro-table th,.ro-table td{padding:10px 12px;font-size:12.5px;}
  .ro-cta{padding:36px 22px;}
}
</style>

<section class="ro-hero">
  <div class="ro-hero-inner">
    <span class="ro-badge">STRUCTURAL ANALYSIS / 構造分析サマリー</span>
    <h1>自販機横リサイクルボックス<br><em>溢れ問題</em>の構造分析</h1>
    <p class="ro-sub">
      常時溢れる<strong>8つの構造的要因</strong>と、東京都にとっての<strong>6つの政策的課題</strong>。
      『回収オペレーターが怠慢だから』ではない。情報啓発だけでは断ち切れない悪循環の全体像を、一次情報・公的データに基づいて整理します。
    </p>
    <p class="ro-meta">
      Tokyo Social Innovation Tech Award 2026 応募関連資料／作成：株式会社Boxernet（令和8年5月）
    </p>
  </div>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">Executive Summary</div>
  <h2>エグゼクティブサマリー</h2>
  <p class="ro-lead">
    東京都内に推定 <strong>30〜40 万台</strong> が設置される自販機の隣のリサイクルボックスは、なぜ常時溢れているのか――。この問いに対する答えは「回収オペレーターが怠慢だから」ではありません。本問題は、(1) 業界のビジネスモデルに組み込まれた構造的弱点、(2) 異物混入 30% の負のループ、(3) 業界の人手不足、(4) 責任主体の曖昧さ、(5) 物理的制約、(6) 業界対応の限界、(7) 情報啓発の限界、(8) 法制度とデータの空白――の <strong>8 つの要因が複合的に絡み合った構造的問題</strong>です。
  </p>
  <p class="ro-lead">
    そしてこの問題は、東京都にとって単なる「街角のゴミの問題」ではなく、<strong>国際観光・景観政策、ゼロエミッション東京戦略、行政コスト、物流 2024 年問題、スマートシティ・都市 OS 戦略、災害時レジリエンス</strong>――の 6 つの主要政策軸が交差する戦略的ハブです。
  </p>
  <div class="ro-callout">
    本サマリーは、Tokyo Social Innovation Tech Award 2026 応募の補強資料、および二次審査・三次審査のプレゼン資料として活用することを想定して構成しています。
  </div>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">Key Data</div>
  <h2>主要データ一覧（一次情報・公的データ）</h2>
  <table class="ro-table">
    <thead>
      <tr>
        <th>指標</th>
        <th>数値・出典</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>国内自販機台数（清涼飲料）</td>
        <td>約 198 万台（うち屋外・リサイクルボックス併設 約 168 万台）。2013 年比で 2 割減少（日経新聞 2025 年 8 月）</td>
      </tr>
      <tr>
        <td>東京都内の自販機台数</td>
        <td>推定 30〜40 万台</td>
      </tr>
      <tr>
        <td>異物混入率</td>
        <td>回収物の約 30% が飲料容器以外（環境省実証事業 2022 年）</td>
      </tr>
      <tr>
        <td>リサイクルボックス認知率</td>
        <td>71.8%（2020 年比 +14pt、全国清涼飲料連合会 2025 年 9 月調査）</td>
      </tr>
      <tr>
        <td>異物投入経験</td>
        <td>21.1% が経験あり（トップはプラカップ 55.7%、全清飲 2025 年調査）</td>
      </tr>
      <tr>
        <td>飲み残し混入率</td>
        <td>約 11%（リサイクル品質を著しく毀損する要因）</td>
      </tr>
      <tr>
        <td>法的背景</td>
        <td>プラスチックに係る資源循環の促進等に関する法律（2022 年 4 月施行）</td>
      </tr>
      <tr>
        <td>業界の最新対応</td>
        <td>新機能リサイクルボックス（下向き投入口・オレンジ色・上面傾斜）を業界統一仕様として順次展開中</td>
      </tr>
    </tbody>
  </table>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">Part 1</div>
  <h2>常時溢れる 8 つの構造的要因</h2>
  <p class="ro-lead">
    一見「単なるオペレーション不足」に見える問題の背後には、業界構造・行動原理・物理制約・法制度の空白が重なり合った 8 つの要因が存在します。それぞれが他の要因を強化し合うため、単一の対策では断ち切れません。
  </p>

  <div class="ro-factors">
    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 01</span>
      <h4>回収オペレーション設計の根本問題</h4>
      <p>自販機オペレーターによる回収は、商品補充のついでに行われます。これは業界のビジネスモデル上の合理性ですが、補充サイクル（売上回転率最適化）と容器投入量（イベント・気候・観光客で変動）が異なる時間軸で動くため、構造的に追従できません。</p>
      <div class="ro-implication">怠慢ではなくモデルそのものの限界</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 02</span>
      <h4>異物混入 30% の負のループ</h4>
      <p>満杯状態のボックスが「もうゴミ箱」と認知され、本来の容器以外（プラカップ 55.7%、食品包装、リチウムイオン電池等）が連鎖的に投入されます。割れ窓理論的な負のループ。リチウムイオン電池混入は、リサイクル施設での発火事故という重大リスクも生みます。</p>
      <div class="ro-implication">満杯 → 異物 → 品質低下の連鎖</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 03</span>
      <h4>認知向上が行動を変えない非対称性</h4>
      <p>2020 年→2025 年で認知率は 58%→71.8%（+14pt）に上昇しましたが、異物混入率は劇的には下がっていません。「知っていても満杯を見たら捨てる」という行動原理は、情報啓発では覆りません。</p>
      <div class="ro-implication">情報的アプローチは既に限界。物理的・構造的アプローチが必要なフェーズへ</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 04</span>
      <h4>自販機オペレーター業界の構造的人手不足</h4>
      <p>国内自販機台数は 2013 年比で 2 割減少（日経新聞 2025 年 8 月）。背景は補充要員の慢性的な不足。連続勤務・休日出勤の常態化、燃料費・人件費の高騰下では、臨時回収のコストは見合わない。</p>
      <div class="ro-implication">回収頻度を増やす経済合理性が存在しない</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 05</span>
      <h4>責任主体の曖昧さ ― 4 者構造の問題</h4>
      <p>飲料メーカー（製造者責任を持つが現場回収は委託先頼み）／自販機オペレーター（回収の実行主体だが本業ではない）／地権者・店舗（設置場所を提供するが責任を負わない契約）／自治体（私有地のものは原則対象外）。</p>
      <div class="ro-implication">全員が当事者だが、誰も主担当ではない</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 06</span>
      <h4>物理的制約 ― 都市部のスペース不足</h4>
      <p>東京都心部は歩道狭小・自販機横 30〜40cm という極めて限定的なスペース。大型のリサイクルボックスは置けません。海外製スマートボックス（米国 Bigbelly 等、幅約 700mm）が日本市場に展開できないのも、この物理的制約によります。</p>
      <div class="ro-implication">海外ソリューションが直接移植できない構造</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 07</span>
      <h4>業界対応（新機能ボックス）の限界</h4>
      <p>全国清涼飲料連合会と日本自動販売協会は、業界統一仕様の「新機能リサイクルボックス」（下向き投入口・上面傾斜・オレンジ色）を展開中。これは異物混入対策としては評価できますが、満杯化・回収頻度の追従不足という根本問題には踏み込んでいません。</p>
      <div class="ro-implication">物理改良で異物を防いでも、容器自体が満杯になれば結局溢れる</div>
    </div>

    <div class="ro-factor">
      <span class="ro-factor-num">FACTOR 08</span>
      <h4>法制度の追い風と現場のデータ空白</h4>
      <p>プラスチック資源循環促進法（2022 年 4 月施行）は責任を明示しましたが、定量的な KPI 監視の仕組みを提供していません。ESG 投資家・TCFD／TNFD 開示の要請で定量データ証明の必要性は急増していますが、データを取得する手段が現場にありません。</p>
      <div class="ro-implication">「法律と現場のあいだに、データの空白がある」</div>
    </div>
  </div>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">Part 2</div>
  <h2>東京都にとっての複合的課題</h2>
  <p class="ro-lead">
    このリサイクルボックス問題は、東京都の <strong>6 つの主要政策軸</strong>と直接的に衝突します。単なるゴミ問題ではなく、観光・環境・行政コスト・物流・都市 OS・防災が交差する戦略的ハブとして捉える必要があります。
  </p>

  <div class="ro-issues">
    <div class="ro-issue">
      <div class="ro-issue-head">
        <div class="ro-issue-no">1</div>
        <h4>国際観光・景観政策との競合</h4>
      </div>
      <p>「国際的な観光・金融都市の実現」を主要政策として掲げる東京にとって、観光地（浅草・銀座・原宿・新宿等）の自販機横の溢れは、観光体験の質を直接的に損ないます。インバウンドの SNS 拡散で「日本＝清潔」のブランドが毀損され、都の景観条例とも競合する構造です。</p>
    </div>

    <div class="ro-issue">
      <div class="ro-issue-head">
        <div class="ro-issue-no">2</div>
        <h4>ゼロエミッション東京戦略との非整合</h4>
      </div>
      <p>2025 年 3 月改定の「ゼロエミッション東京戦略 Beyond カーボンハーフ」（2035 年までに温室効果ガス 60% 削減）に、2 つの面で抵触します。<strong>(a) CO2 排出</strong>：オペレーターの回収車両走行距離が、満杯予測の不在で最適化されていない。<strong>(b) サーキュラーエコノミー阻害</strong>：異物混入 30% によりリサイクル品質が低下し、ボトル to ボトル等の水平リサイクル目標を阻害。</p>
    </div>

    <div class="ro-issue">
      <div class="ro-issue-head">
        <div class="ro-issue-no">3</div>
        <h4>行政コストの増加</h4>
      </div>
      <p>都内自治体は、清掃職員の追加投入、市民苦情対応の行政事務、不法投棄対応、景観美化施策との連動コストを直接的に負担しています。豊島区など複数の自治体担当者からは「現在のオペレーションでは根本的な問題解決の見込みがない」との認識が共有されています（2026 年 3 月ヒアリング）。</p>
    </div>

    <div class="ro-issue">
      <div class="ro-issue-head">
        <div class="ro-issue-no">4</div>
        <h4>物流 2024 年問題との連動</h4>
      </div>
      <p>リサイクルボックスの非効率な回収は、物流 2024 年問題と同じ構造的問題を抱えます。自販機オペレーター業界の労働力ひっ迫、燃料費高騰下での走行距離最適化要請、再配達削減・ラストワンマイル効率化と同じ「街中物流の最適化」課題。飲料業界単独の問題ではなく、都市物流全体の最適化問題です。</p>
    </div>

    <div class="ro-issue">
      <div class="ro-issue-head">
        <div class="ro-issue-no">5</div>
        <h4>スマートシティ・都市 OS 戦略のブラックボックス</h4>
      </div>
      <p>東京都が推進する都市 OS 整備において、街中の物理レイヤー（自販機・リサイクルボックス）はデータ化されていません。容器循環データ・人流データ・廃棄物データが取得できず、政策評価が不可能。大手 SIer（NEC・富士通・NTT・日立）は街中の物理レイヤーにアクセスできない。<strong>このデータの空白は、都市 OS 戦略のアキレス腱になっています。</strong></p>
    </div>

    <div class="ro-issue">
      <div class="ro-issue-head">
        <div class="ro-issue-no">6</div>
        <h4>災害時レジリエンス資源の機会損失</h4>
      </div>
      <p>街中に分散配置された自販機・リサイクルボックスは、本来であれば災害時の街中拠点として活用できる潜在的インフラ。しかし現状の「溢れた状態」では、その物理レイヤーをスマート化・データ化する基盤がありません。</p>
    </div>
  </div>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">Part 3</div>
  <h2>悪循環の構造図</h2>
  <p class="ro-lead">
    8 要因と 6 課題を統合すると、次のような <strong>4 段の悪循環</strong>が見えてきます。
  </p>

  <div class="ro-cycle">
    <div class="ro-cycle-step">
      <div class="ro-cycle-num">STAGE 1</div>
      <div class="ro-cycle-body">
        <h4>オペレーション設計の構造的弱点</h4>
        <p>補充のついで／人手不足／コスト圧</p>
      </div>
    </div>
    <div class="ro-cycle-arrow">↓</div>
    <div class="ro-cycle-step">
      <div class="ro-cycle-num">STAGE 2</div>
      <div class="ro-cycle-body">
        <h4>物理的な満杯・溢れの発生</h4>
        <p>容量不足／回収頻度の不足</p>
      </div>
    </div>
    <div class="ro-cycle-arrow">↓</div>
    <div class="ro-cycle-step">
      <div class="ro-cycle-num">STAGE 3</div>
      <div class="ro-cycle-body">
        <h4>「もうゴミ箱」認知の伝播</h4>
        <p>異物混入 30%（プラカップ・食品・電池）</p>
      </div>
    </div>
    <div class="ro-cycle-arrow">↓</div>
    <div class="ro-cycle-step">
      <div class="ro-cycle-num">STAGE 4</div>
      <div class="ro-cycle-body">
        <h4>リサイクル品質低下</h4>
        <p>業界投資低迷 → 人手さらに不足（STAGE 1 へ戻る）</p>
      </div>
    </div>
    <div class="ro-cycle-loop">↻ STAGE 1 へ循環</div>
  </div>

  <div class="ro-callout">
    <strong>この悪循環は、情報啓発（認知向上）だけでは断ち切れません。</strong>2025 年に認知率 71.8% まで上がったにもかかわらず、現場が改善していないのが何よりの証拠です。断ち切るには <strong>物理層・データ層・オペレーション層の 3 点同時介入</strong>が必要です。
  </div>

  <h3>悪循環を断ち切る 3 つの介入レイヤー</h3>
  <div class="ro-layers">
    <div class="ro-layer">
      <div class="ro-layer-tag">LAYER 01</div>
      <h4>物理層</h4>
      <p>満杯化を構造的に解消（容量拡大・圧縮機構の導入）</p>
    </div>
    <div class="ro-layer">
      <div class="ro-layer-tag">LAYER 02</div>
      <h4>データ層</h4>
      <p>満杯率・異物混入率を定量計測（IoT センシング）</p>
    </div>
    <div class="ro-layer">
      <div class="ro-layer-tag">LAYER 03</div>
      <h4>オペレーション層</h4>
      <p>回収頻度・経路の最適化（AI 予測・ダッシュボード）</p>
    </div>
  </div>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">Part 4</div>
  <h2>政策的示唆と「つぶすくん」の位置づけ</h2>
  <p class="ro-lead">
    この問題を 6 つの政策軸と整合させて解決することができれば、東京都には次の戦略的価値がもたらされます。
  </p>

  <div class="ro-values">
    <div class="ro-value">
      <span class="ro-value-num">VALUE 01</span>
      <p>観光立国・景観政策における国際ブランド価値の向上</p>
    </div>
    <div class="ro-value">
      <span class="ro-value-num">VALUE 02</span>
      <p>ゼロエミッション東京戦略の定量的実装パートナー獲得</p>
    </div>
    <div class="ro-value">
      <span class="ro-value-num">VALUE 03</span>
      <p>行政コスト削減と市民満足の同時向上</p>
    </div>
    <div class="ro-value">
      <span class="ro-value-num">VALUE 04</span>
      <p>物流 2024 年問題への先行対応（Stage 2 連動）</p>
    </div>
    <div class="ro-value">
      <span class="ro-value-num">VALUE 05</span>
      <p>都市 OS 戦略の物理レイヤー整備（SIer が触れない領域）</p>
    </div>
    <div class="ro-value">
      <span class="ro-value-num">VALUE 06</span>
      <p>災害時レジリエンス強化の素地形成</p>
    </div>
  </div>

  <div class="ro-callout">
    「つぶすくん」が <strong>物理層・データ層・オペレーション層の 3 点に同時介入する設計</strong>になっているのは、この悪循環を構造的に断ち切るための必然です。リサイクルボックス問題は「ゴミの問題」ではなく、東京都の 6 つの主要政策が交差する <strong>戦略的ハブ</strong>です。
  </div>
</section>

<section class="ro-section">
  <div class="ro-eyebrow">References</div>
  <h2>主要データソース（参考文献）</h2>
  <div class="ro-refs">
    <ol>
      <li>環境省『自動販売機横リサイクルボックスへの効果的な異物混入防止に関する実証事業の結果について』</li>
      <li>全国清涼飲料連合会『清涼飲料水容器のリサイクルに関する消費者意識調査 2025』</li>
      <li>全国清涼飲料連合会『観光地等における自販機横「新機能リサイクルボックス」の新たな形での導入促進に向けた実証事業』</li>
      <li>食品産業新聞社『自販機横のリサイクルボックス 下向き投入口とオレンジ色で「ゴミ箱感」払しょくへ』</li>
      <li>日本経済新聞『自販機使ってる？ 飲料用 50 年に半減も』（2025 年 8 月）</li>
      <li>東京都環境局『ゼロエミッション東京戦略 Beyond カーボンハーフ』（2025 年 3 月改定）</li>
      <li>内閣府『スマートシティリファレンスアーキテクチャ』（2020 年 3 月）</li>
      <li>豊島区 公共施設管理担当部門ヒアリング（2026 年 3 月、自社実施）</li>
    </ol>
  </div>
</section>

<section class="ro-cta">
  <h3>「つぶすくん」が、悪循環を構造的に断ち切ります。</h3>
  <p>
    物理層・データ層・オペレーション層の 3 点同時介入。<br>
    東京都の 6 つの政策軸と整合する、スマートリサイクルボックスの設計思想をご紹介します。
  </p>
  <a href="{{ '/business/' | relative_url }}" class="ro-cta-btn">事業内容を見る</a>
  <a href="{{ '/contact/' | relative_url }}" class="ro-cta-btn ro-cta-btn-outline">お問い合わせ</a>
  <p style="margin-top:24px;font-size:.95em;">
    <a href="{{ '/products/tsubusukun/safety/' | relative_url }}" style="color:#fff;text-decoration:underline;">Li-ion 混入対策の設計思想 →</a>
  </p>
</section>
