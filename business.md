---
layout: default
lang: ja
alt_url: /en/business/
title: 事業内容 | 株式会社Boxernet
heading: 事業内容
description: Boxernetの事業内容。つぶすくん、ピックアップステーション、状態遷移検知プラットフォームをご紹介します。
permalink: /business/
hero: true
hero_class: hero-shinjuku
lead: 物流・リサイクル・公共空間のIoT機器を、状態遷移で管理する都市インフラOS。
---

Boxernetは、物流・リサイクル・公共空間に置かれるIoT機器の状態を、**予約・占有・満杯・異常・回収**という"状態遷移"として管理する**都市インフラOS**を作っています。

## 事業の二本柱

<div class="card-grid" markdown="0">
  <div class="card">
    <h3>予約できるピックアップステーション</h3>
    <p>再配達・ラストワンマイルの非効率を解消する<strong>都市型インフラ</strong>。EC・配送事業者と連携し、駅前・商業施設・マンションエントランスなどに設置。予約 → 格納 → 受取の状態遷移をクラウドが管理します。</p>
  </div>
  <div class="card">
    <h3>スマートリサイクルボックス（つぶすくん）</h3>
    <p>自販機横・公共空間の回収オペレーションをIoT化する<strong>都市資源循環インフラ</strong>。PETボトル等の投入・圧縮・満杯・回収を状態遷移として検知し、回収頻度の最適化と溢れ事故の予防を同時に実現します。</p>
  </div>
</div>

## 共通基盤

両事業を支えるのは、Boxernetが独自開発する状態遷移マネジメントの共通基盤です。

**MQTT ／ センサー ／ 予約 ／ 通知 ／ 状態遷移 ／ 運用自動化**

軽量プロトコル（MQTT）と多様なセンサーで現場のイベントを取得し、予約・通知・状態遷移エンジン・運用自動化を一気通貫で提供。アプリケーションが変わっても、共通基盤の上に載せ替えるだけで新しい都市インフラサービスを立ち上げられる構造を目指しています。

<style>
  .biz-demo-wrap{
    margin:32px 0 8px;
    border:1px solid var(--color-border);
    border-radius:var(--radius);
    overflow:hidden;
    background:#fff;
    box-shadow:var(--shadow);
  }
  .biz-demo-frame{
    width:100%;
    height:1080px;
    border:0;
    display:block;
    transition:height 0.3s ease;
  }
  .biz-demo-cta{
    text-align:center;
    margin:8px 0 32px;
  }
  .biz-demo-cta .btn{
    background:var(--color-primary);
    color:#fff !important;
    padding:10px 24px;
    border-radius:999px;
    font-size:14px;
    font-weight:600;
    text-decoration:none;
    display:inline-block;
  }
  .biz-demo-cta .btn:hover{
    background:var(--color-primary-dark);
    text-decoration:none;
  }
  .biz-demo-note{
    font-size:12px;
    color:var(--color-text-sub);
    margin-top:8px;
  }
  @media (max-width:720px){
    .biz-demo-frame{ height:1700px; }
  }
</style>

<script>
  // iframe 内のデモから高さ通知を受信して自動リサイズ
  // ※ つぶすくんデモのみ対象（pickup-station-demo は別）
  window.addEventListener('message', function(e){
    var d = e.data;
    if(d && d.source === 'tsubusukun-demo' && d.type === 'resize' && typeof d.height === 'number'){
      var iframes = document.querySelectorAll('iframe.biz-demo-frame');
      iframes.forEach(function(f){
        // pickup-station 用 iframe はスキップ
        if(f.classList.contains('biz-demo-frame--pickup')) return;
        f.style.height = Math.max(d.height + 20, 600) + 'px';
      });
    }
  });
</script>

## つぶすくん インタラクティブデモ

実際の動作イメージを、ブラウザ上で体験いただけます。「▶ デモを開始」ボタンをクリックすると、投入 → 圧縮 → 回収指示 → 満杯シャットダウン → 回収完了までの 6 ステップが順番に再生されます。

<div class="biz-demo-wrap">
  <iframe class="biz-demo-frame" src="{{ '/assets/demo/tsubusukun-demo.html' | relative_url }}" title="つぶすくん インタラクティブデモ（簡易版）" loading="lazy"></iframe>
</div>
<div class="biz-demo-cta">
  <a href="{{ '/demo/' | relative_url }}" class="btn">フルスクリーンでデモを見る →</a>
  <div class="biz-demo-note">投資家・パートナー様向けの解説付き専用ページへ移動します。</div>
</div>

## ピックアップステーション インタラクティブデモ

駅前・商業施設に設置する **予約型スマート受取拠点** の動作イメージです。EC サイトでの購入時にステーションを指定し、配達業者が QR コードで開錠して格納、受取人が QR コードで受け取るまでの 3 ステップを再現します。

<div class="biz-demo-wrap">
  <iframe class="biz-demo-frame biz-demo-frame--pickup" src="{{ '/assets/demo/pickup-station-demo.html' | relative_url }}" title="ピックアップステーション インタラクティブデモ" loading="lazy"></iframe>
</div>
<div class="biz-demo-cta">
  <div class="biz-demo-note">状態遷移: <strong>EMPTY</strong>（空き）→ <strong>RESERVED</strong>（予約済み）→ <strong>OCCUPIED</strong>（格納中）→ <strong>EMPTY</strong>（空きへ復帰）</div>
</div>

<style>
  .biz-demo-frame--pickup{ height:840px; }
  @media (max-width:720px){
    .biz-demo-frame--pickup{ height:1320px; }
  }
</style>

## 技術的アプローチ

### 1. マルチセンサーによる状態検知

重量・距離・加速度・開閉など、対象物の特性に合わせた最適なセンサーを組み合わせ、必要十分な粒度で状態変化を取得します。

### 2. HMMによる現況推定

観測値の単純なしきい値判定ではなく、隠れマルコフモデル（HMM）を用いて「現在どの状態にあるか」を確率的に推定。センサーノイズや欠損にも頑健な運用判断を実現します。

### 3. 遠隔管理の最適化

推定された状態と運用コスト・優先度を組み合わせ、回収・補充・点検の最適タイミングをアルゴリズムが自動判断します。

---

## 導入事例・お問い合わせ

導入検討・パートナーシップに関するご相談は、[お問い合わせページ]({{ '/contact/' | relative_url }})よりご連絡ください。
