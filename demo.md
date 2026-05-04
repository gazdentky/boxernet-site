---
layout: default
title: つぶすくん デモ | 株式会社Boxernet
heading: つぶすくん インタラクティブデモ
description: PET 専用スマートリサイクルボックス「つぶすくん」の状態遷移マネジメントを、ブラウザ上で体験できるインタラクティブデモ。
permalink: /demo/
hero: true
hero_class: hero-yokohama
lead: 投入から回収完了までの 6 ステップを、IoT センサーとクラウドの動きとともに体験できます。
---

<style>
  .demo-frame-wrap{
    margin:24px 0 8px;
    border:1px solid var(--color-border);
    border-radius:var(--radius);
    overflow:hidden;
    background:#fff;
    box-shadow:var(--shadow);
  }
  .demo-frame{
    width:100%;
    height:880px;
    border:0;
    display:block;
  }
  .demo-caption{
    text-align:center;
    font-size:13px;
    color:var(--color-text-sub);
    margin:8px 0 32px;
  }
  .flow-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:16px;
    margin:24px 0 32px;
  }
  .flow-item{
    background:#fff;
    border:1px solid var(--color-border);
    border-radius:var(--radius);
    padding:20px;
    border-left:4px solid var(--color-primary);
  }
  .flow-item .flow-num{
    font-size:11px;
    color:var(--color-primary);
    font-weight:700;
    letter-spacing:0.1em;
    margin-bottom:6px;
  }
  .flow-item h4{
    margin:0 0 8px;
    font-size:15px;
    color:var(--color-text);
  }
  .flow-item p{
    margin:0;
    font-size:13px;
    color:var(--color-text-sub);
    line-height:1.7;
  }
  @media (max-width:720px){
    .demo-frame{ height:1280px; }
  }
</style>

## 体験の流れ

下のデモボックス内の「▶ デモを開始」ボタンをクリックすると、PET ボトル投入から回収完了までの状態遷移を順番に確認できます。BOX 本体・IoT センサー・クラウド・収集業者の連携が、ボックス側のアニメーションと右側のサービスフローに連動して可視化されます。

<div class="demo-frame-wrap">
  <iframe class="demo-frame" src="{{ '/assets/demo/tsubusukun-demo.html' | relative_url }}" title="つぶすくん インタラクティブデモ" loading="lazy"></iframe>
</div>
<p class="demo-caption">※ 本デモは動作イメージを示すものです。実機の仕様は導入環境に応じて調整します。</p>

## 6 つのステップで分かる、状態遷移マネジメント

<div class="flow-grid" markdown="0">
  <div class="flow-item">
    <div class="flow-num">STEP 01</div>
    <h4>待機（IDLE）</h4>
    <p>BOX はスタンバイ中。IoT センサーが満空・重量をリアルタイム監視。アプリで近隣の空き BOX を確認できます。</p>
  </div>
  <div class="flow-item">
    <div class="flow-num">STEP 02</div>
    <h4>投入（DEPOSIT）</h4>
    <p>リサイクル品を投入。重量センサーが種別・重量を検知しポイントを自動付与。データをクラウドへ即時送信します。</p>
  </div>
  <div class="flow-item">
    <div class="flow-num">STEP 03</div>
    <h4>圧縮（COMPRESS）</h4>
    <p>一定量蓄積で自動圧縮機構が起動。容量を最大 3 倍に拡張し回収頻度を削減します。</p>
  </div>
  <div class="flow-item">
    <div class="flow-num">STEP 04</div>
    <h4>回収指示発信（70%）</h4>
    <p>充填率 70% 到達でクラウドが収集業者へ自動発注。最適回収ルートを生成し、満杯前に計画的な回収を実現します。</p>
  </div>
  <div class="flow-item">
    <div class="flow-num">STEP 05</div>
    <h4>投入口シャットダウン（100%）</h4>
    <p>満杯到達で投入口を自動ロック。これ以上の投入を物理的に遮断し、溢れ・詰まりを防止します。</p>
  </div>
  <div class="flow-item">
    <div class="flow-num">STEP 06</div>
    <h4>回収完了（COLLECTED）</h4>
    <p>回収後、自動リセットで IDLE 状態へ復帰。稼働率・圧縮効率・リードタイムが運用最適化に活用されます。</p>
  </div>
</div>

## 投資家・パートナー様へのご紹介ポイント

### 1. 「満杯になってから回収」を「満杯になる前に最適タイミングで回収」へ

従来のリサイクルボックスは、回収業者が定期巡回するか、利用者の通報で初めて満杯が判明する運用でした。つぶすくんは充填率 70% で自動的に回収指示を発信し、計画的な回収ルートを生成。**回収頻度の最適化と溢れ事故の予防を同時に実現**します。

### 2. 自動圧縮で容量を最大 3 倍に拡張

PET ボトルは空気層が大半を占めるため、圧縮なしでは輸送・保管コストが嵩みます。つぶすくんの自動圧縮機構は **1 BOX あたりの実効容量を最大 3 倍に拡張**し、回収頻度・物流コストの大幅削減に貢献します。

### 3. 状態遷移データが運用最適化の資産になる

センサーが取得した「投入頻度」「混雑時間帯」「圧縮効率」「回収リードタイム」は、すべてクラウドに蓄積されます。エリアごとの最適配置・自動販売機事業者との連携・行政との実証など、**データ駆動の運用改善とアライアンス**を可能にします。

---

## 関連リンク

- [事業内容]({{ '/business/' | relative_url }}) — つぶすくんを含む事業全体のご紹介
- [会社概要]({{ '/company/' | relative_url }}) — 株式会社 Boxernet の会社情報
- [お問い合わせ]({{ '/contact/' | relative_url }}) — 導入検討・パートナーシップ・取材のご相談
