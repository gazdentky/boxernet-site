---
layout: default
title: 投資家の皆様へ｜株式会社Boxernet
description: 株式会社Boxernet は、エッジ AI と HMM アルゴリズムで都市インフラの「状態」を可視化する IoT スタートアップです。2026 年シードラウンドを実施中。製品・市場・チームについて公開情報をご案内します。
permalink: /invest/
---

<style>
/* =========================================================
   投資家向け LP 専用スタイル（既存と干渉しないよう iv- プレフィックス）
   ========================================================= */
.iv-hero{
  background:linear-gradient(135deg,#0B5FFF 0%,#083FA8 50%,#0a1430 100%);
  color:#fff;padding:80px 32px 96px;border-radius:18px;
  position:relative;overflow:hidden;margin-bottom:56px;
}
.iv-hero::after{
  content:"";position:absolute;right:-120px;bottom:-120px;
  width:560px;height:560px;
  background:radial-gradient(circle,rgba(0,198,169,.28) 0%,rgba(0,198,169,0) 60%);
  pointer-events:none;
}
.iv-hero::before{
  content:"";position:absolute;left:-80px;top:-80px;
  width:340px;height:340px;
  background:radial-gradient(circle,rgba(11,95,255,.4) 0%,rgba(11,95,255,0) 60%);
  pointer-events:none;
}
.iv-hero-inner{position:relative;z-index:2;max-width:880px;}
.iv-round-badge{
  display:inline-flex;align-items:center;gap:10px;
  font-size:12px;letter-spacing:.16em;font-weight:700;
  background:rgba(0,198,169,.18);color:#7ff0db;
  padding:8px 16px;border-radius:999px;border:1px solid rgba(0,198,169,.45);
  margin-bottom:22px;
}
.iv-round-dot{
  width:8px;height:8px;border-radius:50%;background:#00C6A9;
  box-shadow:0 0 12px #00C6A9;animation:iv-pulse 2s infinite;
}
@keyframes iv-pulse{0%,100%{opacity:1;}50%{opacity:.4;}}
.iv-hero h2{
  font-size:clamp(26px,4.2vw,40px);font-weight:800;color:#fff;
  line-height:1.3;margin:0 0 18px;letter-spacing:.01em;
}
.iv-hero h2 em{color:#00C6A9;font-style:normal;}
.iv-hero p.iv-lead{font-size:clamp(14px,1.6vw,17px);color:#cfd8ee;line-height:1.8;margin-bottom:28px;}

.iv-hero-cta{display:flex;gap:14px;flex-wrap:wrap;}
.iv-btn{
  display:inline-flex;align-items:center;justify-content:center;gap:8px;
  padding:14px 26px;border-radius:10px;font-weight:700;font-size:14px;
  text-decoration:none;letter-spacing:.04em;transition:all .2s;
}
.iv-btn-primary{background:#00C6A9;color:#062b25;}
.iv-btn-primary:hover{background:#3ddabf;transform:translateY(-1px);text-decoration:none;color:#062b25;}
.iv-btn-ghost{background:transparent;color:#fff;border:1px solid rgba(255,255,255,.4);}
.iv-btn-ghost:hover{background:rgba(255,255,255,.1);text-decoration:none;color:#fff;}

.iv-section{margin:72px 0;}
.iv-eyebrow{
  font-size:11px;letter-spacing:.22em;color:#0B5FFF;font-weight:700;
  text-transform:uppercase;margin-bottom:10px;
}
.iv-section h3{
  font-size:clamp(22px,2.8vw,30px);font-weight:800;color:#0a1430;
  line-height:1.3;margin:0 0 14px;
}
.iv-section p.iv-section-lead{
  font-size:15px;color:#3a4868;max-width:820px;margin:0 0 36px;line-height:1.8;
}

/* Why Now */
.iv-trends{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;}
.iv-trend{
  background:#fff;border:1px solid #e5ebf5;border-radius:14px;
  padding:28px 24px;box-shadow:0 8px 24px rgba(11,95,255,.06);
}
.iv-trend-num{
  display:inline-block;width:34px;height:34px;border-radius:8px;
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);color:#fff;
  font-weight:800;text-align:center;line-height:34px;font-size:14px;margin-bottom:14px;
}
.iv-trend h4{font-size:16px;color:#0a1430;margin:0 0 10px;font-weight:700;}
.iv-trend p{font-size:13px;color:#3a4868;line-height:1.8;margin:0;}

/* Vision / Tech */
.iv-vision{
  background:linear-gradient(180deg,#f5f8ff 0%,#fff 100%);
  border:1px solid #e5ebf5;border-radius:18px;padding:40px 36px;
}
.iv-vision-grid{display:grid;grid-template-columns:1fr 1fr;gap:36px;align-items:center;}
.iv-vision h4{font-size:20px;color:#0B5FFF;margin:0 0 14px;font-weight:800;}
.iv-vision p{font-size:14px;color:#3a4868;line-height:1.9;margin:0 0 12px;}
.iv-vision-stack{
  background:#0a1430;color:#fff;border-radius:12px;padding:24px;
  font-family:Menlo,Consolas,monospace;font-size:12.5px;line-height:1.9;
}
.iv-vision-stack .iv-stack-layer{
  padding:8px 12px;margin-bottom:6px;border-radius:6px;
  background:rgba(0,198,169,.1);border-left:3px solid #00C6A9;
}
.iv-vision-stack .iv-stack-layer:last-child{margin-bottom:0;}
.iv-vision-stack .iv-stack-key{color:#7ff0db;}

/* Product roadmap */
.iv-roadmap{display:grid;grid-template-columns:repeat(3,1fr);gap:22px;}
.iv-product{
  background:#fff;border:1px solid #e5ebf5;border-radius:14px;
  padding:28px 24px;position:relative;
}
.iv-product.iv-live{border:2px solid #00C6A9;}
.iv-product-status{
  display:inline-block;font-size:10px;letter-spacing:.2em;font-weight:700;
  padding:4px 10px;border-radius:6px;margin-bottom:12px;
}
.iv-status-live{background:#e0fff8;color:#008f7a;}
.iv-status-dev{background:#e8efff;color:#0B5FFF;}
.iv-status-plan{background:#f5f8ff;color:#6b7a99;}
.iv-product h4{font-size:18px;color:#0a1430;margin:0 0 8px;}
.iv-product .iv-product-tag{font-size:11px;color:#6b7a99;letter-spacing:.12em;margin-bottom:10px;}
.iv-product p{font-size:13px;color:#3a4868;line-height:1.8;margin:0 0 12px;}
.iv-product a.iv-product-link{font-size:12px;color:#0B5FFF;font-weight:700;}

/* Market */
.iv-market{
  display:grid;grid-template-columns:repeat(3,1fr);gap:18px;
  margin-bottom:24px;
}
.iv-market-card{
  background:#fff;border:1px solid #e5ebf5;border-radius:14px;
  padding:26px 22px;text-align:center;
}
.iv-market-num{font-size:32px;font-weight:800;color:#0B5FFF;line-height:1.1;margin-bottom:6px;}
.iv-market-label{font-size:13px;color:#6b7a99;letter-spacing:.06em;}
.iv-market-note{font-size:11px;color:#9aa7c4;margin-top:8px;line-height:1.6;}

/* Team */
.iv-team-card{
  background:#fff;border:1px solid #e5ebf5;border-radius:14px;
  padding:34px 32px;display:flex;gap:28px;align-items:flex-start;
  box-shadow:0 8px 24px rgba(11,95,255,.06);
}
.iv-team-avatar{
  width:84px;height:84px;border-radius:50%;flex-shrink:0;
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);
  display:flex;align-items:center;justify-content:center;
  color:#fff;font-size:28px;font-weight:800;letter-spacing:.05em;
}
.iv-team-info{flex:1;}
.iv-team-name{font-size:18px;color:#0a1430;margin:0 0 4px;font-weight:800;}
.iv-team-role{font-size:13px;color:#0B5FFF;font-weight:600;letter-spacing:.06em;margin-bottom:14px;}
.iv-team-bio{font-size:13.5px;color:#3a4868;line-height:1.9;margin:0;}

/* Traction */
.iv-traction{display:grid;grid-template-columns:repeat(2,1fr);gap:18px;}
.iv-tract-card{
  background:#fff;border:1px solid #e5ebf5;border-radius:12px;
  padding:22px 24px;
}
.iv-tract-icon{
  display:inline-flex;width:36px;height:36px;border-radius:8px;
  background:rgba(0,198,169,.12);color:#008f7a;
  align-items:center;justify-content:center;font-weight:800;
  margin-bottom:12px;font-size:18px;
}
.iv-tract-card h4{font-size:15px;color:#0a1430;margin:0 0 6px;font-weight:700;}
.iv-tract-card p{font-size:13px;color:#3a4868;line-height:1.8;margin:0;}

/* Use of Funds */
.iv-funds{display:grid;grid-template-columns:repeat(2,1fr);gap:16px;}
.iv-fund-item{
  background:linear-gradient(180deg,#fff 0%,#f5f8ff 100%);
  border:1px solid #e5ebf5;border-radius:12px;padding:22px 24px;
  display:flex;gap:14px;align-items:flex-start;
}
.iv-fund-num{
  width:32px;height:32px;border-radius:8px;flex-shrink:0;
  background:#0B5FFF;color:#fff;font-weight:800;
  display:flex;align-items:center;justify-content:center;font-size:13px;
}
.iv-fund-content h4{font-size:14.5px;color:#0a1430;margin:0 0 4px;font-weight:700;}
.iv-fund-content p{font-size:12.5px;color:#3a4868;line-height:1.7;margin:0;}

/* CTA */
.iv-cta{
  background:linear-gradient(135deg,#0B5FFF 0%,#083FA8 50%,#00C6A9 100%);
  color:#fff;border-radius:20px;padding:60px 40px;text-align:center;margin-top:64px;
  box-shadow:0 20px 48px rgba(11,95,255,.18);
}
.iv-cta h3{font-size:28px;margin:0 0 14px;font-weight:800;color:#fff;}
.iv-cta p{font-size:15px;margin-bottom:32px;opacity:.94;line-height:1.8;}
.iv-cta-row{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;}
.iv-cta-primary{
  display:inline-flex;align-items:center;gap:10px;
  background:#fff;color:#0B5FFF;padding:14px 28px;
  border-radius:10px;font-weight:700;font-size:14px;text-decoration:none;
}
.iv-cta-primary:hover{background:#f5f8ff;text-decoration:none;color:#0B5FFF;}
.iv-cta-secondary{
  display:inline-flex;align-items:center;gap:10px;
  background:transparent;color:#fff;padding:13px 26px;
  border:1px solid rgba(255,255,255,.5);border-radius:10px;
  font-weight:700;font-size:14px;text-decoration:none;
}
.iv-cta-secondary:hover{background:rgba(255,255,255,.1);text-decoration:none;color:#fff;}

.iv-disclaimer{
  font-size:11px;color:#9aa7c4;text-align:center;
  margin-top:28px;line-height:1.7;max-width:680px;margin-left:auto;margin-right:auto;
}

@media (max-width:768px){
  .iv-trends,.iv-roadmap,.iv-market,.iv-traction,.iv-funds{grid-template-columns:1fr;}
  .iv-vision-grid{grid-template-columns:1fr;}
  .iv-team-card{flex-direction:column;align-items:center;text-align:center;}
  .iv-cta{padding:44px 24px;}
  .iv-hero{padding:54px 22px 68px;}
}
</style>

<section class="iv-hero">
  <div class="iv-hero-inner">
    <span class="iv-round-badge">
      <span class="iv-round-dot"></span>
      Seed Round 2026 · 調達中
    </span>
    <h2>
      都市インフラの「状態」を、<br>
      <em>エッジ AI と HMM</em> で可視化する。
    </h2>
    <p class="iv-lead">
      Boxernet は、各種センサー × HMM（Hidden Markov Model）アルゴリズム × TinyML を組み合わせ、
      ゴミ・水・電力といった都市インフラの状態遷移をデバイス単体で推定・可視化する IoT スタートアップです。
      第一弾プロダクト「Boxernet Lite」を起点に、マンション運営・自治体・公共インフラへ展開します。
      シードラウンドの調達を通じて、量産・初期顧客開拓・チーム拡大を加速します。
    </p>
    <div class="iv-hero-cta">
      <a href="/assets/pdf/boxernet-pitch-deck.pdf" class="iv-btn iv-btn-primary" download>
        ピッチデック（PDF）をダウンロード
      </a>
      <a href="mailto:info@pickup-st.com?subject=%5B%E6%8A%95%E8%B3%87%E5%AE%B6%E3%81%AE%E7%9A%86%E6%A7%98%5D%20Boxernet%20%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6" class="iv-btn iv-btn-ghost">
        メールで連絡
      </a>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Why Now</div>
  <h3>2026 年、IoT × エッジ AI 市場の潮目が変わった</h3>
  <p class="iv-section-lead">
    マンションストック数は過去最高、廃棄物管理の人手不足は深刻化、TinyML の実装コストは 1/10 以下に。
    クラウド前提だった IoT は、いま「通信レス・エッジ完結」のフェーズへ移行しつつあります。
  </p>
  <div class="iv-trends">
    <div class="iv-trend">
      <div class="iv-trend-num">01</div>
      <h4>ストック社会の到来</h4>
      <p>全国マンションストックは 700 万戸超。築 20 年以上が過半数を占め、共用部運営の効率化・自動化ニーズが高まっています。</p>
    </div>
    <div class="iv-trend">
      <div class="iv-trend-num">02</div>
      <h4>廃棄物管理の人手不足</h4>
      <p>清掃・回収業界は深刻な労働力不足。曜日固定収集や手作業の分別は、コストと環境負荷の両面で限界に近づいています。</p>
    </div>
    <div class="iv-trend">
      <div class="iv-trend-num">03</div>
      <h4>エッジ AI の民主化</h4>
      <p>ESP32-S3 など $5 級の MCU で TinyML が実装可能に。クラウドコスト・通信障壁を取り払う「通信レス IoT」が現実解となりました。</p>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Vision & Technology</div>
  <h3>HMM × TinyML で、状態遷移を「現場」で推定する</h3>
  <p class="iv-section-lead">
    私たちの強みは、隠れマルコフモデル（HMM）と軽量ニューラルネットワークを組み合わせ、
    ノイズの多い実環境センサーデータから「対象物の状態」を高い確度で推定できる点です。
    特許取得済みのコア技術を、複数プロダクトへ横展開していきます。
  </p>
  <div class="iv-vision">
    <div class="iv-vision-grid">
      <div>
        <h4>センサー × アルゴリズムで「状態」を見る</h4>
        <p>
          画像・距離・重量・人感・音響など複数のモダリティを統合。
          HMM が時系列の状態遷移を、TinyML が瞬間的な分類・回帰・異常検知を担います。
        </p>
        <p>
          すべての推論はデバイス内で完結。クラウド契約・通信契約・配線工事を必要とせず、
          プライバシー・セキュリティ・コストの 3 つを同時に解決します。
        </p>
      </div>
      <div class="iv-vision-stack">
        <div class="iv-stack-layer"><span class="iv-stack-key">Application</span> ＝ 製品ごとの UI / ログ / アラート</div>
        <div class="iv-stack-layer"><span class="iv-stack-key">State Engine</span> ＝ HMM による状態遷移推定（特許 第7534835号）</div>
        <div class="iv-stack-layer"><span class="iv-stack-key">TinyML</span> ＝ 分類・回帰・異常検知（合計 133KB / INT8）</div>
        <div class="iv-stack-layer"><span class="iv-stack-key">Edge MCU</span> ＝ ESP32-S3 + 各種センサー</div>
      </div>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Product Lineup</div>
  <h3>Boxernet Lite を起点とした製品ロードマップ</h3>
  <p class="iv-section-lead">
    マンション共用部に最適化した「Lite」を皮切りに、商業施設向け「Standard」、公共インフラ向け新カテゴリへ展開します。
    すべて共通の State Engine 上で開発するため、追加プロダクトの開発スピードは加速していきます。
  </p>
  <div class="iv-roadmap">
    <div class="iv-product iv-live">
      <span class="iv-product-status iv-status-live">● Available</span>
      <div class="iv-product-tag">PRODUCT 01</div>
      <h4>Boxernet Lite</h4>
      <p>通信レス TinyML スマートリサイクルボックス。マンション共用部・バックヤード設置型。PoC 完了、初期出荷可能。</p>
      <a href="/products/lite/" class="iv-product-link">製品ページを見る →</a>
    </div>
    <div class="iv-product">
      <span class="iv-product-status iv-status-dev">▶ In Development</span>
      <div class="iv-product-tag">PRODUCT 02</div>
      <h4>Boxernet Standard</h4>
      <p>クラウド連携・遠隔監視対応モデル。商業施設・自治体・大規模物件向け。複数台統合管理ダッシュボード搭載予定。</p>
    </div>
    <div class="iv-product">
      <span class="iv-product-status iv-status-plan">○ Roadmap</span>
      <div class="iv-product-tag">PRODUCT 03+</div>
      <h4>State Engine 横展開</h4>
      <p>水道メーター、ストック型インフラ点検など、HMM × TinyML を活かせる別領域への展開を計画中。</p>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Market Opportunity</div>
  <h3>巨大ストック市場と、まだ着手されていないエッジ IoT 領域</h3>
  <p class="iv-section-lead">
    マンション運営・廃棄物管理・公共インフラの市場規模は合計で年間数兆円規模。
    そのうち「IoT による状態可視化」が未到達な領域が、私たちのターゲットです。
  </p>
  <div class="iv-market">
    <div class="iv-market-card">
      <div class="iv-market-num">700 万+</div>
      <div class="iv-market-label">マンションストック数（戸）</div>
      <div class="iv-market-note">国土交通省統計、Lite 直接想定先</div>
    </div>
    <div class="iv-market-card">
      <div class="iv-market-num">2.5 兆円</div>
      <div class="iv-market-label">国内廃棄物管理市場</div>
      <div class="iv-market-note">業界推計値、Lite/Standard 隣接市場</div>
    </div>
    <div class="iv-market-card">
      <div class="iv-market-num">$50B+</div>
      <div class="iv-market-label">グローバル Edge AI 市場（2030）</div>
      <div class="iv-market-note">複数調査機関平均、State Engine 横展開先</div>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Team</div>
  <h3>創業者紹介</h3>
  <p class="iv-section-lead">
    現場での課題発見力と、実装まで一気通貫で進められる小回りの効くチームです。
    シードラウンドの調達を通じて、ハードウェア量産パートナー・ML エンジニアの採用を加速します。
  </p>
  <div class="iv-team-card">
    <div class="iv-team-avatar">AT</div>
    <div class="iv-team-info">
      <div class="iv-team-name">高橋 明宏 — Akihiro Takahashi</div>
      <div class="iv-team-role">Founder &amp; CEO / 株式会社Boxernet</div>
      <p class="iv-team-bio">
        2023 年 2 月、株式会社Boxernet を東京都豊島区にて創業。
        IoT・エッジ AI 領域における新規事業開発をリードし、HMM ベースの状態遷移推定アルゴリズムを発明（特許 第7534835号）。
        マンション運営・廃棄物管理の現場ヒアリングに基づくプロダクト設計を強みとし、
        Boxernet Lite の構想〜試作〜製品化を主導している。
      </p>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Traction & Milestones</div>
  <h3>シードまでの主要マイルストーン</h3>
  <p class="iv-section-lead">
    技術的な堀（特許）と最初のプロダクト（Lite）を確立し、初期顧客との対話フェーズに入っています。
  </p>
  <div class="iv-traction">
    <div class="iv-tract-card">
      <div class="iv-tract-icon">特</div>
      <h4>HMM 状態遷移推定アルゴリズム特許 取得</h4>
      <p>特許 第7534835号。コア技術を複数プロダクトに横展開できる知財ポートフォリオの起点。</p>
    </div>
    <div class="iv-tract-card">
      <div class="iv-tract-icon">P</div>
      <h4>Boxernet Lite 試作機完成・PoC 完了</h4>
      <p>ESP32-S3 上で TinyML 3 モデルが並列稼働。推論応答 180–220ms / 平均消費電力 1.8W を実機で実証。</p>
    </div>
    <div class="iv-tract-card">
      <div class="iv-tract-icon">公</div>
      <h4>製品サイト・コーポレートサイト公開</h4>
      <p>pickup-st.com にて製品情報・会社概要を公開。投資家・パートナー候補への情報提供基盤を整備。</p>
    </div>
    <div class="iv-tract-card">
      <div class="iv-tract-icon">対</div>
      <h4>初期顧客・パートナー候補との対話開始</h4>
      <p>マンション管理会社・PM 事業者・廃棄物処理事業者との個別ディスカッションを実施中。</p>
    </div>
  </div>
</section>

<section class="iv-section">
  <div class="iv-eyebrow">Use of Funds</div>
  <h3>調達資金の使途</h3>
  <p class="iv-section-lead">
    シードラウンドで調達した資金は、量産化準備、初期顧客との実証導入、コアチーム拡大に重点配分します。
  </p>
  <div class="iv-funds">
    <div class="iv-fund-item">
      <div class="iv-fund-num">1</div>
      <div class="iv-fund-content">
        <h4>量産プロトタイプ製造</h4>
        <p>第 1 ロット 100〜300 台規模の試作。筐体金型・部材調達・組立委託先の確保。</p>
      </div>
    </div>
    <div class="iv-fund-item">
      <div class="iv-fund-num">2</div>
      <div class="iv-fund-content">
        <h4>初期顧客との実証導入</h4>
        <p>マンション 5〜10 棟での実証パイロット。データ収集・モデル改善・運用設計のフィードバックループ確立。</p>
      </div>
    </div>
    <div class="iv-fund-item">
      <div class="iv-fund-num">3</div>
      <div class="iv-fund-content">
        <h4>コアチーム拡大</h4>
        <p>ML エンジニア・ハードウェアエンジニア・事業開発の採用。特に組み込み TinyML 経験者を重点的に。</p>
      </div>
    </div>
    <div class="iv-fund-item">
      <div class="iv-fund-num">4</div>
      <div class="iv-fund-content">
        <h4>知財・標準化・認証取得</h4>
        <p>追加特許出願、業界標準への適合、量産品としての必要認証（PSE 等）取得。</p>
      </div>
    </div>
  </div>
</section>

<section class="iv-cta">
  <h3>詳細資料・面談のご案内</h3>
  <p>
    ピッチデック（PDF）には、本ページに掲載していない事業計画・財務見通し・ロードマップ詳細を含みます。<br>
    投資家の皆様、戦略パートナー候補の皆様からのお問い合わせを歓迎いたします。
  </p>
  <div class="iv-cta-row">
    <a href="/assets/pdf/boxernet-pitch-deck.pdf" class="iv-cta-primary" download>
      ピッチデック（PDF）をダウンロード
    </a>
    <a href="mailto:info@pickup-st.com?subject=%5B%E6%8A%95%E8%B3%87%E5%AE%B6%E3%81%AE%E7%9A%86%E6%A7%98%5D%20Boxernet%20%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6" class="iv-cta-secondary">
      info@pickup-st.com に問い合わせ
    </a>
  </div>
</section>

<p class="iv-disclaimer">
  本ページは公開可能な情報に基づくご案内であり、株式の募集または勧誘を構成するものではありません。
  具体的な投資検討にあたっては、別途ピッチデックおよび個別面談を通じて詳細情報をご提供します。
  記載の市場規模等は各種公開統計に基づく当社推計を含みます。
</p>
