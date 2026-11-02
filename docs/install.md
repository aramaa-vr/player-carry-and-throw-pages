---
title: "ワールドへの導入"
description: "VCCで追加してPrefabを配置する手順"
nav_order: 2
permalink: /install/
---

# ワールドへの導入

ご利用前に[利用規約（ライセンス）](https://github.com/aramaa-vr/player-carry-and-throw/blob/master/LICENSE.md)をご確認ください。

ワールド制作者向けの手順です。**VCCでパッケージを追加し、Unityでモードを1つ配置するだけ**で基本の設定ができます。

<ol class="steps">
  <li><strong>VCCでワールドのプロジェクトを選ぶ</strong><br>VRChat Creator Companion（VCC）を開き、ギミックを導入するワールドの <strong>Manage Project</strong> を選びます。<span class="step-hint">配布リポジトリをまだ登録していない場合は、先に<a href="https://aramaa-vr.github.io/vpm-repos/redirect.html">VCCへ登録</a>してください。</span></li>
  <li><strong>「だこちてギミック【ワールド版】」を追加する</strong><br><strong>Manage Packages</strong> の検索欄に <strong>「だこちてギミック【ワールド版】」</strong> と入力します。検索結果に表示された同名のパッケージの<strong>右端の「＋」ボタン</strong>を押して追加してください。
    <figure class="install-menu-shot install-vcc-shot">
      <a href="{{ '/assets/img/vcc-manage-packages.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="VCCの検索と追加ボタンの画像を拡大表示">
        <img src="{{ '/assets/img/vcc-manage-packages.webp' | relative_url }}" alt="VCCのManage Packages画面。検索欄にだこちてギミック【ワールド版】を入力し、検索結果の右端にある＋ボタンを押して追加する。" loading="lazy" decoding="async" width="1172" height="260">
      </a>
      <figcaption>パッケージ名で検索し、右端の「＋」から追加します（画像をクリックすると拡大できます）。</figcaption>
    </figure>
    <span class="step-hint">見つからない場合は、VCCへの配布リポジトリ登録と「Selected Repos」の選択を確認してください。</span>
  </li>
  <li><strong>Unityにギミックを配置する</strong><br>追加が完了したらVCCの <strong>Open Project</strong> からUnityを開きます。<br>Unity上部の <code>Tools → Aramaa → だこちてギミック[ワールド版]</code> を開き、目的のモードの「〜モードをワールドに配置」を選びます。<strong>配置するモードは1つだけ</strong>です。
    <figure class="install-menu-shot">
      <a href="{{ '/assets/img/unity-placement-menu.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="Unityの配置メニュー画像を拡大表示">
        <img src="{{ '/assets/img/unity-placement-menu.webp' | relative_url }}" alt="UnityのToolsからAramaa、だこちてギミック[ワールド版]を開き、だこちて・投げ合い・組体操・カスタムのモードを選んでワールドに配置するメニュー" loading="lazy" width="975" height="146">
      </a>
      <figcaption>Unityの配置メニュー（画像をクリックすると拡大できます）</figcaption>
    </figure>
  </li>
  <li><strong>「TMP Importer」が表示された場合は初期設定する</strong><br>これはエラーではありません。上段の <strong>Import TMP Essentials</strong> をクリックし、読み込みが終わったらウィンドウを閉じてください。下段の <strong>Import TMP Examples &amp; Extras</strong> は、このギミックを使うためには必要ありません。
    <figure class="install-menu-shot install-tmp-shot">
      <a href="{{ '/assets/img/tmp-importer.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="TMP Importerの画面を拡大表示">
        <img src="{{ '/assets/img/tmp-importer.webp' | relative_url }}" alt="TMP Importerの画面。上段のImport TMP Essentialsボタンをクリック。下段のImport TMP Examples &amp; Extrasは操作不要。" loading="lazy" width="649" height="247">
      </a>
      <figcaption>「Import TMP Essentials」を1回クリックします（画像をクリックすると拡大できます）。</figcaption>
    </figure>
    <span class="step-hint">この画面が出なければ、この手順は不要です。</span>
  </li>
  <li><strong>ワールドで確認する</strong><br>常設UIを使いやすい場所に置き、ビルドして抱っこ・解除などの動作を確認します。</li>
</ol>

## どのモードを配置する？

| モード | 遊び方 |
|---|---|
| **だこちて** | 抱っこ → 離すと固定 |
| **組体操** | 抱っこをつなげる → 離すと固定 |
| **投げ合い** | 抱っこ → 離すと投げる |
| **カスタム** | ワールド制作者が動作を調整する |

<div class="note"><strong>配置は1 Sceneにつき1つだけ。</strong> 主要3モードは初期設定済みです。ワールドに既存の <code>EventSystem</code> がない場合は1つ用意してください。</div>

### Prefabから直接配置する場合

<code>Packages/jp.aramaa.player-carry-and-throw/Runtime/Prefabs/</code> にある以下のPrefabを1つ選びます。

- だこちて：<code>PlayerCarryAndThrow_Dako.prefab</code>
- 組体操：<code>PlayerCarryAndThrow_Gymnastics.prefab</code>
- 投げ合い：<code>PlayerCarryAndThrow_Battle.prefab</code>
- カスタム：<code>PlayerCarryAndThrow.prefab</code>

<div class="action-row"><a class="primary" href="{{ '/play/' | relative_url }}">遊び方へ進む</a></div>
