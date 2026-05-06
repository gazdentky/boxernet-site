---
layout: default
title: 資料請求フォーム｜株式会社Boxernet
description: 株式会社Boxernet のピッチデック・追加資料をご請求いただけます。投資家・パートナー候補の皆様、必要事項をご記入のうえご送信ください。
permalink: /pitch-request/
---

<style>
/* =========================================================
   資料請求フォーム専用スタイル（pr- プレフィックス）
   ========================================================= */
.pr-hero{
  background:linear-gradient(135deg,#0B5FFF 0%,#083FA8 100%);
  color:#fff;padding:56px 32px 64px;border-radius:18px;
  position:relative;overflow:hidden;margin-bottom:40px;
}
.pr-hero::after{
  content:"";position:absolute;right:-100px;top:-60px;
  width:380px;height:380px;
  background:radial-gradient(circle,rgba(0,198,169,.25) 0%,rgba(0,198,169,0) 60%);
  pointer-events:none;
}
.pr-hero-inner{position:relative;z-index:2;max-width:880px;}
.pr-hero h2{
  font-size:clamp(24px,3.4vw,36px);font-weight:800;color:#fff;
  line-height:1.3;margin:0 0 14px;
}
.pr-hero p{font-size:15px;color:#cfd8ee;line-height:1.8;margin:0;}

.pr-card{
  background:#ffffff;border:1px solid #e5ebf5;border-radius:16px;
  padding:40px 36px;box-shadow:0 8px 24px rgba(11,95,255,.08);
  margin-bottom:32px;
}
.pr-section-title{
  font-size:13px;letter-spacing:.18em;color:#0B5FFF;
  font-weight:700;text-transform:uppercase;margin-bottom:18px;
  padding-bottom:10px;border-bottom:2px solid #0B5FFF;
}

.pr-row{display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-bottom:18px;}
.pr-field{display:flex;flex-direction:column;gap:6px;}
.pr-field.pr-full{grid-column:1 / -1;}
.pr-label{
  font-size:13px;font-weight:700;color:#0a1430;
  display:flex;align-items:center;gap:8px;
}
.pr-required{
  display:inline-block;font-size:10px;font-weight:700;
  background:#0B5FFF;color:#fff;padding:2px 8px;border-radius:4px;letter-spacing:.04em;
}
.pr-optional{
  display:inline-block;font-size:10px;font-weight:600;
  background:#f5f8ff;color:#6b7a99;padding:2px 8px;border-radius:4px;letter-spacing:.04em;
  border:1px solid #e5ebf5;
}
.pr-input,.pr-textarea,.pr-select{
  font-family:inherit;font-size:14px;color:#0a1430;
  padding:12px 14px;border:1px solid #d4dcec;border-radius:8px;
  background:#fff;transition:border-color .15s,box-shadow .15s;
  width:100%;box-sizing:border-box;
}
.pr-input:focus,.pr-textarea:focus,.pr-select:focus{
  outline:none;border-color:#0B5FFF;box-shadow:0 0 0 3px rgba(11,95,255,.12);
}
.pr-textarea{resize:vertical;min-height:110px;line-height:1.7;}
.pr-help{font-size:11px;color:#6b7a99;margin-top:2px;}

.pr-submit-row{
  margin-top:24px;display:flex;flex-direction:column;align-items:center;gap:14px;
}
.pr-btn-submit{
  background:linear-gradient(135deg,#0B5FFF,#00C6A9);
  color:#fff;font-size:15px;font-weight:700;letter-spacing:.04em;
  padding:16px 44px;border:none;border-radius:10px;cursor:pointer;
  transition:all .2s;box-shadow:0 8px 20px rgba(11,95,255,.25);
}
.pr-btn-submit:hover:not(:disabled){
  transform:translateY(-1px);box-shadow:0 12px 24px rgba(11,95,255,.35);
}
.pr-btn-submit:disabled{opacity:.6;cursor:not-allowed;}

.pr-privacy{
  font-size:11px;color:#6b7a99;text-align:center;
  line-height:1.7;max-width:560px;
}

.pr-status{
  display:none;padding:14px 18px;border-radius:10px;
  font-size:13px;font-weight:600;margin-top:16px;
}
.pr-status.pr-status-error{
  display:block;background:#fff0f0;color:#c8302a;border:1px solid #f4c1be;
}
.pr-status.pr-status-loading{
  display:block;background:#f5f8ff;color:#0B5FFF;border:1px solid #c8d8ff;
}

.pr-info{
  background:#f5f8ff;border:1px solid #e5ebf5;border-radius:10px;
  padding:18px 22px;font-size:13px;color:#3a4868;line-height:1.8;
}
.pr-info strong{color:#0a1430;}

@media (max-width:768px){
  .pr-row{grid-template-columns:1fr;}
  .pr-card{padding:28px 22px;}
  .pr-hero{padding:40px 22px 48px;}
}
</style>

<section class="pr-hero">
  <div class="pr-hero-inner">
    <h2>資料請求フォーム</h2>
    <p>
      ピッチデック（PDF）および関連資料をご希望の方は、以下のフォームに必要事項をご記入のうえ送信してください。<br>
      送信後にダウンロードページへ自動的に切り替わります。担当より個別にもご連絡いたします。
    </p>
  </div>
</section>

<form id="pr-form" class="pr-card" novalidate>
  <div class="pr-section-title">ご記入事項</div>

  <div class="pr-row">
    <div class="pr-field">
      <label class="pr-label" for="pr-company">会社名 <span class="pr-required">必須</span></label>
      <input class="pr-input" id="pr-company" name="company" type="text" required autocomplete="organization">
    </div>
    <div class="pr-field">
      <label class="pr-label" for="pr-name">ご担当者名 <span class="pr-required">必須</span></label>
      <input class="pr-input" id="pr-name" name="name" type="text" required autocomplete="name">
    </div>
  </div>

  <div class="pr-row">
    <div class="pr-field">
      <label class="pr-label" for="pr-email">メールアドレス <span class="pr-required">必須</span></label>
      <input class="pr-input" id="pr-email" name="email" type="email" required autocomplete="email">
    </div>
    <div class="pr-field">
      <label class="pr-label" for="pr-phone">電話番号 <span class="pr-optional">任意</span></label>
      <input class="pr-input" id="pr-phone" name="phone" type="tel" autocomplete="tel">
    </div>
  </div>

  <div class="pr-row">
    <div class="pr-field pr-full">
      <label class="pr-label" for="pr-address">ご住所 <span class="pr-required">必須</span></label>
      <input class="pr-input" id="pr-address" name="address" type="text" required autocomplete="street-address" placeholder="例：東京都豊島区○○1-2-3">
    </div>
  </div>

  <div class="pr-row">
    <div class="pr-field">
      <label class="pr-label" for="pr-position">ご職位 <span class="pr-optional">任意</span></label>
      <input class="pr-input" id="pr-position" name="position" type="text" placeholder="例：代表取締役、投資部マネージャー">
    </div>
    <div class="pr-field">
      <label class="pr-label" for="pr-round">ご関心のあるラウンド・金額 <span class="pr-optional">任意</span></label>
      <select class="pr-select" id="pr-round" name="round">
        <option value="">選択してください</option>
        <option value="seed_under_50m">シード・〜5,000万円</option>
        <option value="seed_50_100m">シード・5,000万〜1億円</option>
        <option value="seed_100_300m">シード・1億〜3億円</option>
        <option value="series_a">プレシリーズA / シリーズA 検討</option>
        <option value="strategic">事業会社・戦略パートナーとして検討</option>
        <option value="other">その他・未定</option>
      </select>
    </div>
  </div>

  <div class="pr-row">
    <div class="pr-field pr-full">
      <label class="pr-label" for="pr-message">メッセージ <span class="pr-optional">任意</span></label>
      <textarea class="pr-textarea" id="pr-message" name="message" placeholder="ご質問、関心領域、奉じておられるファンド名などご自由にご記入ください"></textarea>
    </div>
  </div>

  <input type="hidden" name="_subject" value="[Boxernet] ピッチデック資料請求">
  <input type="hidden" name="_format" value="plain">

  <div class="pr-submit-row">
    <button type="submit" class="pr-btn-submit" id="pr-submit-btn">送信して資料を取得する</button>
    <p class="pr-privacy">
      ご記入いただいた情報は、当社（株式会社Boxernet）からの資料提供および投資家対応のためにのみ使用し、第三者への開示は行いません。
    </p>
    <div id="pr-status-loading" class="pr-status pr-status-loading">送信中です。しばらくお待ちください…</div>
    <div id="pr-status-error" class="pr-status pr-status-error">送信に失敗しました。お手数ですが時間をおいて再度お試しいただくか、info@pickup-st.com まで直接ご連絡ください。</div>
  </div>
</form>

<div class="pr-info">
  フォームでの送信が難しい場合は、お手数ですが <strong>info@pickup-st.com</strong> 宛にメールでお問い合わせください。<br>
  通常 1〜3 営業日以内に担当より資料をお送りいたします。
</div>

<script>
  // === Formspree エンドポイント設定 ===
  // formspree.io でアカウント作成後、付与されたエンドポイント URL を以下に設定してください
  // 例: https://formspree.io/f/abcdwxyz
  var FORMSPREE_ENDPOINT = "https://formspree.io/f/xjglrrlb";

  (function () {
    var form = document.getElementById("pr-form");
    var submitBtn = document.getElementById("pr-submit-btn");
    var loading = document.getElementById("pr-status-loading");
    var errorBox = document.getElementById("pr-status-error");

    form.addEventListener("submit", function (e) {
      e.preventDefault();
      errorBox.style.display = "none";

      // ネイティブのバリデーション
      if (!form.checkValidity()) {
        form.reportValidity();
        return;
      }

      submitBtn.disabled = true;
      loading.style.display = "block";

      var formData = new FormData(form);

      fetch(FORMSPREE_ENDPOINT, {
        method: "POST",
        body: formData,
        headers: { Accept: "application/json" }
      })
        .then(function (res) {
          if (res.ok) {
            window.location.href = "/pitch-request/thanks/";
          } else {
            return res.json().then(function (data) {
              throw new Error((data && data.error) || "Submit failed");
            });
          }
        })
        .catch(function () {
          loading.style.display = "none";
          errorBox.style.display = "block";
          submitBtn.disabled = false;
        });
    });
  })();
</script>
