---
layout: default
title: つぶすくん｜ペットボトル自動圧縮 IoT デバイス
description: 「つぶすくん」はペットボトルを自動で圧縮し、回収効率を最大化する IoT デバイス。製品紹介動画でその動作をご覧ください。
permalink: /products/tsubusu-kun/
---

<style>
/* =========================================================
   つぶすくん 製品紹介ページ専用スタイル
   既存サイト CSS と干渉しないよう全クラスに "tk-" プレフィックス
   ========================================================= */
.tk-hero{
  background:linear-gradient(135deg,#0B5FFF 0%,#0a1430 100%);
  color:#fff;padding:64px 28px 72px;border-radius:18px;
  position:relative;overflow:hidden;margin-bottom:48px;
}
.tk-hero::after{
  content:"";position:absolute;right:-100px;bottom:-100px;
  width:520px;height:520px;
  background:radial-gradient(circle,rgba(0,198,169,.25) 0%,rgba(0,198,169,0) 60%);
  pointer-events:none;
}
.tk-hero-inner{position:relative;z-index:2;max-width:880px;}
.tk-badge{
  display:inline-block;font-size:11px;letter-spacing:.18em;
  background:rgba(0,198,169,.18);color:#7ff0db;
  padding:6px 12px;border-radius:999px;border:1px solid rgba(0,198,169,.4);
  margin-bottom:18px;font-weight:600;
}
.tk-hero h2{
  font-size:clamp(28px,4.8vw,44px);font-weight:800;color:#fff;
  line-height:1.25;margin:0 0 16px;
}
.tk-hero h2 em{color:#00C6A9;font-style:normal;}
.tk-hero p.tk-lead{
  font-size:clamp(14px,1.6vw,17px);color:#cfd8ee;line-height:1.7;
  margin:0;
}

/* 動画セクション */
.tk-video-section{margin:48px 0 64px;}
.tk-eyebrow{
  font-size:11px;letter-spacing:.2em;color:#0B5FFF;font-weight:700;
  text-transform:uppercase;margin-bottom:8px;
}
.tk-video-section h3{
  font-size:clamp(22px,2.8vw,30px);font-weight:800;color:#0a1430;
  line-height:1.3;margin:0 0 12px;
}
.tk-video-section p.tk-section-lead{
  font-size:15px;color:#3a4868;max-width:780px;margin:0 0 28px;line-height:1.7;
}

/* レスポンシブ動画埋め込み（16:9） */
.tk-video-wrap{
  position:relative;width:100%;padding-top:56.25%;
  border-radius:14px;overflow:hidden;
  box-shadow:0 16px 48px rgba(11,95,255,.18);
  background:#0a1430;
}
.tk-video-wrap iframe{
  position:absolute;top:0;left:0;width:100%;height:100%;
  border:0;
}

.tk-video-caption{
  margin-top:16px;font-size:13px;color:#6a7794;text-align:center;
}
.tk-video-caption a{color:#0B5FFF;text-decoration:none;}
.tk-video-caption a:hover{text-decoration:underline;}

/* CTA */
.tk-cta{
  background:#f5f8ff;border-radius:14px;padding:40px 28px;
  text-align:center;margin-top:48px;border:1px solid #e5ebf5;
}
.tk-cta h3{
  font-size:clamp(18px,2.2vw,24px);font-weight:800;color:#0a1430;
  margin:0 0 10px;
}
.tk-cta p{font-size:14px;color:#3a4868;margin:0 0 22px;}
.tk-cta-btn{
  display:inline-block;background:#0B5FFF;color:#fff;font-weight:700;
  padding:13px 28px;border-radius:8px;text-decoration:none;
  font-size:14px;letter-spacing:.02em;
  box-shadow:0 8px 20px rgba(11,95,255,.28);
  transition:transform .2s,box-shadow .2s;
}
.tk-cta-btn:hover{
  transform:translateY(-2px);
  box-shadow:0 12px 28px rgba(11,95,255,.36);
}

@media (max-width:680px){
  .tk-hero{padding:48px 22px 56px;}
}
</style>

<section class="tk-hero">
  <div class="tk-hero-inner">
    <span class="tk-badge">NEW PRODUCT</span>
    <h2>ペットボトルを、<em>その場で圧縮。</em><br>回収効率を変える IoT デバイス。</h2>
    <p class="tk-lead">
      「つぶすくん」は、捨てた瞬間にペットボトルを自動で圧縮する次世代スマートリサイクルデバイス。
      ボリュームを最大 80% 削減し、回収頻度と運搬コストを劇的に下げます。
    </p>
  </div>
</section>

<section class="tk-video-section">
  <div class="tk-eyebrow">Product Demo</div>
  <h3>製品紹介動画</h3>
  <p class="tk-section-lead">
    実機による動作の様子をご覧いただけます。投入から圧縮までの一連の流れを 1 分でご確認ください。
  </p>

  <div class="tk-video-wrap">
    <iframe
      src="https://www.youtube-nocookie.com/embed/fdW1WNHF1Co?rel=0"
      title="つぶすくん 製品紹介動画"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
      loading="lazy"
      referrerpolicy="strict-origin-when-cross-origin"></iframe>
  </div>

  <p class="tk-video-caption">
    動画が表示されない場合は <a href="https://www.youtube.com/watch?v=fdW1WNHF1Co" target="_blank" rel="noopener">YouTube で直接視聴</a> してください。
  </p>
</section>

<section class="tk-cta">
  <h3>「つぶすくん」の導入・パートナー連携をご検討の方へ</h3>
  <p>製品仕様書・デモ機の貸出・パイロット導入のご相談を承っております。</p>
  <a href="mailto:info@pickup-st.com?subject=%E3%80%8C%E3%81%A4%E3%81%B6%E3%81%99%E3%81%8F%E3%82%93%E3%80%8D%E3%81%AB%E9%96%A2%E3%81%99%E3%82%8B%E3%81%8A%E5%95%8F%E3%81%84%E5%90%88%E3%82%8F%E3%81%9B" class="tk-cta-btn">
    info@pickup-st.com に問い合わせる
  </a>
</section>
