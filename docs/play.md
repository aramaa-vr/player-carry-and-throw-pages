---
title: "遊び方"
description: "許可設定・抱っこ・固定・投げ合いの操作"
nav_order: 3
permalink: /play/
---

# 遊び方

ギミックが設置されたワールドに入ったら、まず<strong>自分と相手の許可を確認</strong>してから遊びましょう。

## 1. 抱っこの許可を設定する

<div class="guide-grid two-columns">
  <div class="guide"><img src="{{ '/assets/img/stick.webp' | relative_url }}" alt="右スティックを下に倒すイラスト"><b>VR：右スティックを下へ約1秒長押し</b><small>本人用UIを開く。もう一度長押しすると閉じる</small></div>
  <div class="guide"><img src="{{ '/assets/img/permission.webp' | relative_url }}" alt="許可スイッチのイラスト"><b>UIのスイッチで許可を選択</b><small>「抱っこする」と「抱っこされる」をそれぞれ設定</small></div>
</div>

**Desktop：** ワールド内に置かれた常設UIで設定します。VRでも常設UIを操作できます。右スティック長押しはUIの開閉だけで、許可自体は切り替わりません。呼び出したUIは表示した場所に留まり、次に開くと現在の目の前へ移動します。「閉じる」から閉じることもできます。

- **「抱っこする」**：自分が相手を抱っこするかどうかを選びます。
- **「抱っこされる」**：相手が自分を抱っこしてよいかを選びます。

2つの設定は独立しています。「抱っこされる」をOFFにしても、「抱っこする」がONなら許可している相手を抱っこできます。**これらの選択は、次回のワールド訪問には保存されません。** ワールド側で「抱っこされる」が強制設定されている場合、そのスイッチは操作できません。

## 2. 抱っこする

<div class="guide-grid two-columns">
  <div class="guide"><img src="{{ '/assets/img/grab.webp' | relative_url }}" alt="腰付近をつかむイラスト"><b>相手の腰付近をつかむ</b><small>VRはGrab / Pickup、Desktopは腰付近を狙ってPickup</small></div>
  <div class="guide"><img src="{{ '/assets/img/release.webp' | relative_url }}" alt="手を離すイラスト"><b>手を離す</b><small>モードに応じて固定・投げ・通常の解除</small></div>
</div>

**VRでは両手で別々の相手を抱っこできます。Desktopは一度に1人です。** 腰の取っ手は見えないため、相手の腰付近を狙ってください。

## 3. モード別の遊び方

主要3モードの標準設定での操作です。ワールド制作者が設定を変更している場合は、そのワールドの案内に従ってください。各画像は**クリックすると拡大**できます。画像は配置時の表示例です。「準備中」の部分は、ワールド内では本人の許可状態に応じて更新されます。

<section class="mode-guide" id="mode-dako">
  <h3>だこちてモード</h3>
  <p>相手の腰をつかんで抱っこ。<strong>VRでは手首を回して相手の角度も調整</strong>できます。手を離すとその位置・姿勢で固定され、抱っこされた人は<strong>ジャンプ入力で解除</strong>できます。固定した相手を掴み直し、すぐ離して解除することもできます。</p>
  <figure>
    <a href="{{ '/assets/img/mode-dako.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="だこちてモードの操作説明画像を拡大">
      <img src="{{ '/assets/img/mode-dako.webp' | relative_url }}" width="1200" height="900" loading="lazy" decoding="async" alt="だこちてモードの操作画面。抱っこする・抱っこされるを準備し、腰をつかみ、VRでは手首を回して角度を調整。離すと固定、ジャンプで解除。VR右スティック下約1秒でメニューを開閉する。">
    </a>
    <figcaption>だこちてモードの遊び方（画像をクリックすると拡大）</figcaption>
  </figure>
</section>

<section class="mode-guide" id="mode-gymnastics">
  <h3>組体操モード</h3>
  <p>抱っこを<strong>連鎖</strong>させて、3人以上でもつながれます。手を離すと固定され、抱っこされた人は<strong>ジャンプ入力で解除</strong>できます。固定した相手を掴み直し、すぐ離して解除することもできます。</p>
  <figure>
    <a href="{{ '/assets/img/mode-gymnastics.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="組体操モードの操作説明画像を拡大">
      <img src="{{ '/assets/img/mode-gymnastics.webp' | relative_url }}" width="1200" height="900" loading="lazy" decoding="async" alt="組体操モードの操作画面。連鎖で抱っこ、離すと固定、ジャンプで解除。3人以上の連鎖が可能。">
    </a>
    <figcaption>組体操モードの遊び方（画像をクリックすると拡大）</figcaption>
  </figure>
</section>

<section class="mode-guide" id="mode-battle">
  <h3>投げ合いモード</h3>
  <p>相手の腰をつかんで抱っこし、手を離すと<strong>視線方向へ投げます</strong>。VRは手の動き、Desktopは<strong>Use長押し</strong>で投げる力をためます。<strong>このモードでは固定・ジャンプ解除は無効</strong>です。手を振った方向ではなく、<strong>離した瞬間に見ている方向</strong>へ投げます。</p>
  <figure>
    <a href="{{ '/assets/img/mode-battle.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="投げ合いモードの操作説明画像を拡大">
      <img src="{{ '/assets/img/mode-battle.webp' | relative_url }}" width="1200" height="900" loading="lazy" decoding="async" alt="投げ合いモードの操作画面。腰をつかみ、離して視線方向へ投げる。抱っこされる許可を切り替え可能。VRは手を動かして、DesktopはUse長押しで蓄積。ジャンプ解除と固定は無効。">
    </a>
    <figcaption>投げ合いモードの遊び方（画像をクリックすると拡大）</figcaption>
  </figure>
</section>

**カスタムモード：** 抱っこ・固定・投げなどの動きは、ワールド制作者の設定によって異なります。

## 困ったとき

- **相手を掴めない**：自分の「抱っこする」と相手の「抱っこされる」がONか確認します。ワールド側で機能や参加資格が制限されている場合もあります。
- **抱っこされたくない・解除したい**：「抱っこされる」をOFFにすると、抱っこや固定を解除できます。だこちて・組体操の標準設定ではジャンプ入力でも解除できます。
- **自分が抱っこするのをやめたい**：「抱っこする」をOFFにすると、現在抱っこしている相手を投げずに離します。すでに離して固定した相手の固定は、この操作では解除されません。

<div class="note"><strong>遊ぶときは相手の同意を大切に。</strong> 許可スイッチだけでなく、その場での相手の意思も確認してください。</div>

<div class="action-row" id="contact"><a href="{{ '/install/' | relative_url }}">ワールドへの導入方法</a><a href="{{ '/contact/' | relative_url }}">不具合・不明点のお問い合わせ</a><a href="{{ '/' | relative_url }}">トップへ戻る</a></div>
