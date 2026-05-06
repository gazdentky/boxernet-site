---
layout: default
title: Boxernet Lite｜TinyML 搭載スマートリサイクルボックス
description: Boxernet Lite は通信レス・TinyML 搭載のマンション設置型スマートゴミ箱。ESP32-S3 とエッジ AI で分別判定・満杯予測・異常検知をデバイス単体で完結。クラウド費 0 円、管理コスト 35% 削減。
permalink: /products/lite/
---

<style>
/* =========================================================
   Boxernet Lite ページ専用スタイル
   既存 site CSS と干渉しないよう、クラス名は全て "bl-" プレフィックス
   ========================================================= */
.bl-hero{
  background:linear-gradient(135deg,#0B5FFF 0%,#0a1430 100%);
  color:#fff;padding:72px 28px 88px;border-radius:18px;
  position:relative;overflow:hidden;margin-bottom:48px;
}
.bl-hero::after{
  content:"";position:absolute;right:-100px;bottom:-100px;
  width:520px;height:520px;
  background:radial-gradient(circle,rgba(0,198,169,.25) 0%,rgba(0,198,169,0) 60%);
  pointer-events:none;
}
.bl-hero-inner{position:relative;z-index:2;max-width:880px;}
.bl-edition{
  display:inline-block;font-size:11px;letter-spacing:.18em;
  background:rgba(0,198,169,.18);color:#7ff0db;
  padding:6px 12px;border-radius:999px;border:1px solid rgba(0,198,169,.4);
  margin-bottom:18px;font-weight:600;
}
.bl-hero h2{
  font-size:clamp(22px,3.6vw,36px);font-weight:800;color:#fff;
  line-height:1.25;margin:0 0 16px;
}
.bl-hero h2 em{color:#00C6A9;font-style:normal;}
.bl-hero p.bl-lead{font-size:clamp(14px,1.6vw,17px);color:#cfd8ee;line-height:1.7;}

.bl-stats{
  display:grid;grid-template-columns:repeat(3,1fr);gap:16px;
  margin-top:36px;max-width:680px;
}
.bl-stat{
  background:rgba(255,255,255,.06);border:1px solid rgba(255,255,255,.12);
  border-radius:12px;padding:16px;
}
.bl-stat-num{font-size:26px;font-weight:800;color:#00C6A9;line-height:1.1;}
.bl-stat-label{font-size:12px;color:#cfd8ee;margin-top:4px;letter-spacing:.04em;}

.bl-section{margin:64px 0;}
.bl-eyebrow{
  font-size:11px;letter-spacing:.2em;color:#0B5FFF;font-weight:700;
  text-transform:uppercase;margin-bottom:8px;
}
.bl-section h3{
  font-size:clamp(20px,2.6vw,28px);font-weight:800;color:#0a1430;
  line-height:1.3;margin:0 0 12px;
}
.bl-section p.bl-section-lead{
  font-size:15px;color:#3a4868;max-width:780px;margin:0 0 32px;
}

.bl-issues{display:grid;grid-template-columns:repeat(3,1fr);gap:20px;}
.bl-issue{
  background:#fff;border-radius:12px;padding:24px 22px;
  border:1px solid #e5ebf5;box-shadow:0 8px 24px rgba(11,95,255,.06);
}
.bl-issue-num{font-size:11px;color:#0B5FFF;font-weight:700;letter-spacing:.2em;margin-bottom:6px;}
.bl-issue-title{font-size:16px;font-weight:700;margin-bottom:8px;color:#0a1430;}
.bl-issue-desc{font-size:13px;color:#3a4868;margin-bottom:12px;line-height:1.7;}
.bl-issue-metric{
  display:inline-block;background:#f5f8ff;color:#0B5FFF;
  font-weight:700;padding:5px 11px;border-radius:6px;font-size:12px;
}

.bl-features{display:grid;grid-template-columns:repeat(2,1fr);gap:20px;}
.bl-feature{
  background:#fff;border:1px solid #e5ebf5;border-radius:12px;
  padding:24px;box-shadow:0 8px 24px rgba(11,95,255,.06);
}
.bl-feature-ico{
  width:44px;height:44px;border-radius:10px;
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);
  display:flex;align-items:center;justify-content:center;color:#fff;
  font-size:18px;font-weight:700;margin-bottom:14px;
}
.bl-feature h4{font-size:16px;margin:0 0 8px;color:#0a1430;}
.bl-feature p{color:#3a4868;font-size:13.5px;line-height:1.7;}

.bl-table{
  width:100%;border-collapse:collapse;background:#fff;
  border-radius:12px;overflow:hidden;box-shadow:0 8px 24px rgba(11,95,255,.06);
}
.bl-table th,.bl-table td{
  padding:12px 14px;text-align:left;border-bottom:1px solid #e5ebf5;
  font-size:13.5px;
}
.bl-table th{background:#f5f8ff;font-weight:700;color:#0a1430;}
.bl-table th.bl-hl{background:#0B5FFF;color:#fff;}
.bl-table td.bl-hl{background:rgba(11,95,255,.04);font-weight:600;color:#0B5FFF;}
.bl-table tr:last-child td{border-bottom:none;}

.bl-ai{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;}
.bl-ai-card{
  background:linear-gradient(180deg,#fff 0%,#f5f8ff 100%);
  border:1px solid #e5ebf5;border-radius:12px;padding:22px;
}
.bl-ai-task{font-size:11px;letter-spacing:.18em;color:#00C6A9;font-weight:700;margin-bottom:6px;}
.bl-ai-model{font-size:16px;font-weight:700;color:#0a1430;margin-bottom:4px;font-family:Menlo,Consolas,monospace;}
.bl-ai-size{font-size:12px;color:#6b7a99;margin-bottom:14px;}
.bl-ai-output{
  background:#fff;border:1px solid #e5ebf5;border-radius:8px;
  padding:8px 12px;font-size:12.5px;color:#3a4868;margin-bottom:10px;
}
.bl-ai-acc{font-size:13px;color:#0B5FFF;font-weight:700;}

.bl-spec{display:grid;grid-template-columns:repeat(2,1fr);gap:28px;}
.bl-spec-block h4{
  font-size:14px;color:#0B5FFF;margin:0 0 12px;
  padding-bottom:6px;border-bottom:2px solid #0B5FFF;
}
.bl-spec-list{list-style:none;padding:0;margin:0;}
.bl-spec-list li{
  display:flex;justify-content:space-between;gap:14px;
  padding:9px 0;border-bottom:1px dashed #e5ebf5;font-size:13px;
}
.bl-spec-k{color:#6b7a99;}
.bl-spec-v{color:#0a1430;font-weight:600;text-align:right;}

.bl-cta{
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);
  color:#fff;border-radius:18px;padding:48px 32px;text-align:center;margin-top:48px;
}
.bl-cta h3{font-size:26px;margin:0 0 12px;font-weight:800;color:#fff;}
.bl-cta p{font-size:14px;margin-bottom:24px;opacity:.92;}
.bl-cta-btn{
  display:inline-block;background:#fff;color:#0B5FFF;
  padding:13px 28px;border-radius:10px;font-weight:700;font-size:14px;
  text-decoration:none;letter-spacing:.04em;
}
.bl-cta-btn:hover{background:#f5f8ff;}

@media (max-width:768px){
  .bl-stats,.bl-issues,.bl-features,.bl-ai,.bl-spec{grid-template-columns:1fr;}
  .bl-table th,.bl-table td{padding:10px;font-size:12.5px;}
  .bl-cta{padding:36px 22px;}
  .bl-hero{padding:52px 22px 64px;}
}
</style>

<section class="bl-hero">
  <div class="bl-hero-inner">
    <span class="bl-edition">No Cloud · No Cellular · No Wi-Fi Edition</span>
    <h2>Boxernet Lite<br><em>通信レス・TinyML</em><br>スマートリサイクルボックス</h2>
    <p class="bl-lead">
      マンション分譲・賃貸運営のために設計された、エッジ AI 単体で完結するスマートゴミ箱。
      ESP32-S3 上の TinyML が「分別判定」「満杯予測」「異常検知」をデバイス内で処理。
      SIM 不要・配線工事不要・組合決議の長期化も不要です。
    </p>
    <div class="bl-stats">
      <div class="bl-stat">
        <div class="bl-stat-num">¥0</div>
        <div class="bl-stat-label">クラウド費用 / 月</div>
      </div>
      <div class="bl-stat">
        <div class="bl-stat-num">▲45%</div>
        <div class="bl-stat-label">Standard 比 価格</div>
      </div>
      <div class="bl-stat">
        <div class="bl-stat-num">35%</div>
        <div class="bl-stat-label">管理コスト削減見込み</div>
      </div>
    </div>
  </div>
</section>

<section class="bl-section">
  <div class="bl-eyebrow">Background</div>
  <h3>なぜ「通信レス」が求められるのか</h3>
  <p class="bl-section-lead">
    マンション共用部のごみステーション運営には、頻度ミスマッチ・分別品質・導入ハードルという 3 つの構造課題があります。Boxernet Lite はこれらを通信を使わずに解決します。
  </p>
  <div class="bl-issues">
    <div class="bl-issue">
      <div class="bl-issue-num">ISSUE 01</div>
      <div class="bl-issue-title">頻度ミスマッチ</div>
      <p class="bl-issue-desc">曜日固定収集では繁忙期は溢れ、閑散期は空回り。景観・衛生クレームの原因に。</p>
      <span class="bl-issue-metric">空車率 約 31%（業界平均）</span>
    </div>
    <div class="bl-issue">
      <div class="bl-issue-num">ISSUE 02</div>
      <div class="bl-issue-title">分別品質の低下</div>
      <p class="bl-issue-desc">PET キャップ・ラベル・液残・混入による差戻しで、清掃員の手作業負担が増大。</p>
      <span class="bl-issue-metric">資源化率低下 18%（首都圏）</span>
    </div>
    <div class="bl-issue">
      <div class="bl-issue-num">ISSUE 03</div>
      <div class="bl-issue-title">導入ハードル</div>
      <p class="bl-issue-desc">Wi-Fi/SIM の導入には組合決議・配線工事・セキュリティ対策が必須。</p>
      <span class="bl-issue-metric">合意形成 6〜12 ヶ月</span>
    </div>
  </div>
</section>

<section class="bl-section">
  <div class="bl-eyebrow">Features</div>
  <h3>完全オフライン × TinyML で<br>「捨てる」を、その場で賢く。</h3>
  <p class="bl-section-lead">
    ESP32-S3 上で複数の AI モデルが並列実行。撮影画像はメモリ上で処理されたあと即破棄され、ネットワーク経由で外部に送られることはありません。プライバシーとセキュリティを構造的に担保します。
  </p>
  <div class="bl-features">
    <div class="bl-feature">
      <div class="bl-feature-ico">AI</div>
      <h4>瞬時分別判定</h4>
      <p>カメラ＋ToF＋重量センサで、缶・ビン・ペット・紙・その他を 200ms 以内に判定。LED と音声で投入者へ即時案内。</p>
    </div>
    <div class="bl-feature">
      <div class="bl-feature-ico">%</div>
      <h4>満杯予測</h4>
      <p>過去の充填パターンを学習する 1D-CNN/LSTM が「あと ◯%」を LCD 表示。回収のムダを最適化。</p>
    </div>
    <div class="bl-feature">
      <div class="bl-feature-ico">!</div>
      <h4>異常物検知</h4>
      <p>Autoencoder による異常検知で、不適切物・残液混入時にアラート。住民スマホ通知ではなく筐体上で完結。</p>
    </div>
    <div class="bl-feature">
      <div class="bl-feature-ico">SD</div>
      <h4>SD カード持ち出し運用</h4>
      <p>ログは 32GB microSD に AES 暗号化保存。月 1 回の物理回収で十分。クラウド契約・通信費は発生しません。</p>
    </div>
    <div class="bl-feature">
      <div class="bl-feature-ico">P</div>
      <h4>プライバシー by Design</h4>
      <p>通信モジュール非搭載。撮影画像は推論直後に破棄され、外部に出る情報はゼロ。組合説明もシンプル。</p>
    </div>
    <div class="bl-feature">
      <div class="bl-feature-ico">⚡</div>
      <h4>電源 1 本のみ</h4>
      <p>AC100V を 1 本接続するだけで稼働。スーパーキャパシタで停電時もシャッタを安全に閉鎖。</p>
    </div>
  </div>
</section>

<section class="bl-section">
  <div class="bl-eyebrow">Why Lite</div>
  <h3>Standard モデルとの違い</h3>
  <p class="bl-section-lead">
    集合住宅のバックヤード設置に最適化されています。「マンション優先」のための割り切りが、コストと導入スピードを劇的に改善します。
  </p>
  <table class="bl-table">
    <thead>
      <tr>
        <th>項目</th>
        <th>Boxernet Standard</th>
        <th class="bl-hl">Boxernet Lite</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>通信</td><td>Wi-Fi / SIM 必須</td><td class="bl-hl">通信レス</td></tr>
      <tr><td>導入工事</td><td>配線・LAN 工事 ¥150K/棟〜</td><td class="bl-hl">電源 1 本のみ ¥0</td></tr>
      <tr><td>クラウド費用</td><td>¥3K / 台 / 月〜</td><td class="bl-hl">¥0 / 月</td></tr>
      <tr><td>セキュリティ対応</td><td>脆弱性管理・暗号化通信・監査が必要</td><td class="bl-hl">外部攻撃面ゼロ</td></tr>
      <tr><td>組合合意の取りやすさ</td><td>セキュリティ・電波問題で難航しがち</td><td class="bl-hl">基地局非依存・短期合意</td></tr>
      <tr><td>停電時挙動</td><td>稼働停止</td><td class="bl-hl">スーパーキャパで安全停止</td></tr>
    </tbody>
  </table>
</section>

<section class="bl-section">
  <div class="bl-eyebrow">On-device AI</div>
  <h3>ESP32-S3 上で並列稼働する 3 つの TinyML モデル</h3>
  <p class="bl-section-lead">
    合計 133KB の超小型モデル群が、PSRAM 8MB のうちわずか 1.6% で動作。すべてエッジで完結し、クラウド推論を必要としません。
  </p>
  <div class="bl-ai">
    <div class="bl-ai-card">
      <div class="bl-ai-task">TASK 01 / 分別判定</div>
      <div class="bl-ai-model">MobileNetV2-tiny</div>
      <div class="bl-ai-size">INT8 量子化 / 67KB</div>
      <div class="bl-ai-output">出力: 缶 / ビン / ペット / 紙 / その他</div>
      <div class="bl-ai-acc">標準精度 95% 以上</div>
    </div>
    <div class="bl-ai-card">
      <div class="bl-ai-task">TASK 02 / 満杯予測</div>
      <div class="bl-ai-model">1D-CNN + LSTM</div>
      <div class="bl-ai-size">回帰 / 24KB</div>
      <div class="bl-ai-output">出力: 充填率 0–100%</div>
      <div class="bl-ai-acc">予測誤差 ±5%</div>
    </div>
    <div class="bl-ai-card">
      <div class="bl-ai-task">TASK 03 / 異常検知</div>
      <div class="bl-ai-model">Autoencoder</div>
      <div class="bl-ai-size">42KB / 閾値判定</div>
      <div class="bl-ai-output">出力: 異常スコア / アラート</div>
      <div class="bl-ai-acc">検知率 90%</div>
    </div>
  </div>
</section>

<section class="bl-section">
  <div class="bl-eyebrow">Specifications</div>
  <h3>ハードウェア仕様</h3>
  <p class="bl-section-lead">
    市販部材で構成された堅実な BOM。1,000 ロット時の製造原価は ¥38,500（筐体・組立・梱包込）。量産・保守の安定性を最優先しています。
  </p>
  <div class="bl-spec">
    <div class="bl-spec-block">
      <h4>センサ・処理系</h4>
      <ul class="bl-spec-list">
        <li><span class="bl-spec-k">MCU</span><span class="bl-spec-v">ESP32-S3-WROOM-1 (N16R8)</span></li>
        <li><span class="bl-spec-k">カメラ</span><span class="bl-spec-v">OmniVision OV2640 / 200 万画素</span></li>
        <li><span class="bl-spec-k">ToF 距離</span><span class="bl-spec-v">ST VL53L1X / 0–3m</span></li>
        <li><span class="bl-spec-k">重量センサ</span><span class="bl-spec-v">HX711 / 0–3kg</span></li>
        <li><span class="bl-spec-k">人感センサ</span><span class="bl-spec-v">AM312 PIR</span></li>
        <li><span class="bl-spec-k">ストレージ</span><span class="bl-spec-v">microSD 32GB Class10 (AES)</span></li>
        <li><span class="bl-spec-k">RTC</span><span class="bl-spec-v">DS3231</span></li>
      </ul>
    </div>
    <div class="bl-spec-block">
      <h4>UI・電源・筐体</h4>
      <ul class="bl-spec-list">
        <li><span class="bl-spec-k">表示</span><span class="bl-spec-v">1.3" OLED + WS2812B LED ×24</span></li>
        <li><span class="bl-spec-k">音声</span><span class="bl-spec-v">DFPlayer Mini (MP3)</span></li>
        <li><span class="bl-spec-k">電源</span><span class="bl-spec-v">AC100V → DC5V/3A</span></li>
        <li><span class="bl-spec-k">バックアップ</span><span class="bl-spec-v">スーパーキャパ 10F</span></li>
        <li><span class="bl-spec-k">筐体</span><span class="bl-spec-v">PE 樹脂 240L / IP44</span></li>
        <li><span class="bl-spec-k">寸法</span><span class="bl-spec-v">W490 × D450 × H1100 mm</span></li>
        <li><span class="bl-spec-k">動作温度</span><span class="bl-spec-v">−10 〜 +40℃</span></li>
      </ul>
    </div>
    <div class="bl-spec-block">
      <h4>性能</h4>
      <ul class="bl-spec-list">
        <li><span class="bl-spec-k">推論応答時間</span><span class="bl-spec-v">180–220 ms</span></li>
        <li><span class="bl-spec-k">消費電力（平均）</span><span class="bl-spec-v">1.8 W</span></li>
        <li><span class="bl-spec-k">消費電力（Peak）</span><span class="bl-spec-v">6 W</span></li>
        <li><span class="bl-spec-k">通信</span><span class="bl-spec-v">なし（USB-C 保守用 I/F のみ）</span></li>
        <li><span class="bl-spec-k">推論モデル合計</span><span class="bl-spec-v">133 KB / PSRAM 1.6% 使用</span></li>
      </ul>
    </div>
    <div class="bl-spec-block">
      <h4>製造・展開</h4>
      <ul class="bl-spec-list">
        <li><span class="bl-spec-k">想定原価</span><span class="bl-spec-v">¥38,500（1,000 ロット）</span></li>
        <li><span class="bl-spec-k">価格帯</span><span class="bl-spec-v">Standard 比 ▲45%</span></li>
        <li><span class="bl-spec-k">主要設置先</span><span class="bl-spec-v">マンション共用部 / バックヤード</span></li>
        <li><span class="bl-spec-k">電波認証</span><span class="bl-spec-v">技適審査 不要</span></li>
        <li><span class="bl-spec-k">設置工事</span><span class="bl-spec-v">電源接続のみ</span></li>
      </ul>
    </div>
  </div>
</section>

<section class="bl-cta">
  <h3>Boxernet Lite の導入をご検討中の方へ</h3>
  <p>マンション共用部・PM 業務の改善ポテンシャルを試算します。資料・デモ動画もご提供可能です。</p>
  <a href="mailto:info@pickup-st.com?subject=Boxernet%20Lite%20%E8%B3%87%E6%96%99%E8%AB%8B%E6%B1%82" class="bl-cta-btn">
    info@pickup-st.com に問い合わせる
  </a>
</section>
