---
title: "ワールドへの導入"
description: "VCCで追加してPrefabを配置する手順"
nav_order: 2
permalink: /install/
---

# ワールドへの導入

ご利用前に[利用規約（ライセンス）](https://github.com/aramaa-vr/player-carry-and-throw/blob/master/LICENSE.md)をご確認ください。

ワールド制作者向けの手順です。**VCCでパッケージを追加し、Unityで主要3モードのうち1つを配置する**のが基本です。遊ぶ人のアバターへの導入は必要ありません。

追加・更新前にプロジェクトをバックアップしてください。Unity 2022.3のVRChat Worldsプロジェクトを使用します。必要なパッケージはWorlds SDK（3.10.5以上・4.0.0未満）、TextMesh Pro 3.0.6、uGUI 1.0.0です。

## VCCでパッケージを追加する

**配布リポジトリの登録はVCC全体で1回、パッケージの追加はワールドのプロジェクトごとに必要です。** すでにリポジトリを登録している方は手順2へ、対象プロジェクトにパッケージを追加済みの方は[Unityでの配置](#unity-setup)へ進んでください。

<p class="step-hint">画面の表記はVCC・ブラウザーの言語やバージョンによって異なります。画像はクリックすると拡大できます（追加済みメッセージの画像を除く）。</p>

<ol class="steps">
  <li><strong>配布リポジトリをVCCに登録する（初回のみ）</strong><br><a href="https://aramaa-vr.github.io/vpm-repos/redirect.html">VCCへ登録</a>を開き、ブラウザーで確認が出たら <strong>CreatorCompanion を開く</strong> を選びます。
    <figure class="install-menu-shot install-vcc-shot">
      <a href="{{ '/assets/img/vcc-add-repo.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="ブラウザーからVCCを開く確認画面を拡大表示">
        <img src="{{ '/assets/img/vcc-add-repo.webp' | relative_url }}" alt="ブラウザーの確認画面。CreatorCompanion を開くボタンからVCCを起動する。" loading="lazy" decoding="async" width="1094" height="330">
      </a>
      <figcaption>「CreatorCompanion を開く」を選ぶと、VCCに移動します。</figcaption>
    </figure>
    <p>VCCの <strong>Add Repository</strong> で、配布元が <strong>あらまあ素敵なショップ</strong>、URLが <code>https://aramaa-vr.github.io/vpm-repos/vpm.json</code> であることを確認します。注意事項を読んで、<strong>I Understand, Add Repository</strong> を押してください。</p>
    <figure class="install-menu-shot install-vcc-shot">
      <a href="{{ '/assets/img/vcc-add-repository-confirm.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="VCCのリポジトリ登録確認画面を拡大表示">
        <img src="{{ '/assets/img/vcc-add-repository-confirm.webp' | relative_url }}" alt="VCCのAdd Repository画面。あらまあ素敵なショップのURLと、Included Packagesにだこちてギミック【ワールド版】があることを確認し、I Understand, Add Repositoryを押す。" loading="lazy" decoding="async" width="1177" height="601">
      </a>
      <figcaption>ここでは配布元を登録します。ワールドのプロジェクトへの追加は手順3で行います。</figcaption>
    </figure>
    <details class="install-repo-status">
      <summary>「You have already added this repository.」と表示された場合</summary>
      <p><strong>配布リポジトリは登録済みです。</strong> 再登録は不要なので、入力欄の <strong>Cancel</strong> で閉じ、手順2へ進んでください。このメッセージだけでは、対象プロジェクトにパッケージが入っているかは分かりません。</p>
      <figure class="install-menu-shot">
        <div class="install-repo-status-window">
          <img src="{{ '/assets/img/vcc-settings-repo-added-q75.webp' | relative_url }}" alt="VCCのリポジトリ登録欄に、You have already added this repository. You can't add it again. と表示されている。" loading="lazy" decoding="async" width="969" height="603">
        </div>
        <figcaption>「このリポジトリは追加済みで、再追加できません」という意味です。登録済みの配布元を削除し直す必要はありません。</figcaption>
      </figure>
    </details>
    <p class="step-hint">VCCが開かない場合は、VCCの <strong>Settings → Packages → Add Repository</strong> に上記URLを貼り付け、<strong>Add</strong> を押して登録できます。</p>
  </li>
  <li><strong>配布リポジトリにチェックが入っていることを確認する</strong><br>VCCの <strong>Settings → Packages → Installed Repositories</strong> で、<strong>あらまあ素敵なショップ</strong> にチェックを入れます。登録済みでも、チェックが外れているとパッケージの一覧に表示されません。
    <figure class="install-menu-shot install-vcc-shot">
      <a href="{{ '/assets/img/vcc-repository-enabled.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="VCCの配布リポジトリのチェック状態を拡大表示">
        <img src="{{ '/assets/img/vcc-repository-enabled.webp' | relative_url }}" alt="VCCのInstalled Repositories一覧。あらまあ素敵なショップの左側にチェックが入っている。" loading="lazy" decoding="async" width="1174" height="602">
      </a>
      <figcaption>「あらまあ素敵なショップ」の左側にチェックがあれば、配布元の準備は完了です。</figcaption>
    </figure>
  </li>
  <li><strong>ワールドのプロジェクトを選び、パッケージを追加する</strong><br>VCCの <strong>Projects</strong> に戻り、導入するワールドの <strong>Manage Project</strong> を開きます。<strong>Manage Packages</strong> の検索欄に <strong>「だこちてギミック【ワールド版】」</strong> と入力し、同名のパッケージを探してください。<strong>Installed Version</strong> が <strong>Not Installed</strong> の場合は、<strong>右端の「＋」ボタン</strong>を押して追加します。追加確認が表示されたら、内容を確認して進めてください。
    <figure class="install-menu-shot install-vcc-shot">
      <a href="{{ '/assets/img/vcc-manage-packages.webp' | relative_url }}" target="_blank" rel="noopener noreferrer" aria-label="VCCの検索と追加ボタンの画像を拡大表示">
        <img src="{{ '/assets/img/vcc-manage-packages.webp' | relative_url }}" alt="VCCのManage Packages画面。だこちてギミック【ワールド版】のInstalled VersionはNot Installedと表示され、右端に追加用の＋ボタンがある。" loading="lazy" decoding="async" width="1146" height="263">
      </a>
      <figcaption>「Not Installed」は、このプロジェクトには未導入という意味です。右端の「＋」から追加します。画像はクリックすると拡大できます。</figcaption>
    </figure>
    <p><strong>すでにインストール済みの場合：</strong> <strong>Installed Version</strong> にバージョン番号が表示されていれば、そのプロジェクトへの追加は完了しています。Unityでの配置へ進んでください。更新したい場合は、先に<a href="#package-update">更新・削除するとき</a>を確認します。</p>
    <span class="step-hint">見つからない場合は、手順2のチェックと、Manage Packagesの <strong>Selected Repos</strong> に配布元が含まれているかを確認してください。別のプロジェクトに導入済みでも、今回のプロジェクトには追加が必要です。</span>
  </li>
</ol>

<h2 id="unity-setup">Unityでギミックを配置する</h2>

すでにシーンにギミックを配置している場合は、本体を追加せず、既存の配置と動作を確認してください。更新する場合は[更新・削除するとき](#package-update)へ進みます。

<ol class="steps">
  <li><strong>Unityにギミックを配置する</strong><br>追加が完了したらVCCの <strong>Open Project</strong> からUnityを開きます。<br>Unity上部の <code>Tools → Aramaa → だこちてギミック【ワールド版】</code> を開き、目的のモードの「〜モードをワールドに配置」を選びます。<strong>配置するモードは1つだけ</strong>です。
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
  <li><strong>ワールドで確認する</strong><br>常設UIを使いやすい場所に置き、ワールドの <code>EventSystem</code> が1つあることを確認します。UdonSharpをコンパイルし、VRChat SDKでビルドして、UI操作・抱っこ・解除を確認してください。複数人での動作と、利用する端末での操作も確認します。</li>
</ol>

## どのモードを配置する？

| モード | 遊び方 |
|---|---|
| **だこちて** | 抱っこ → 離すと固定 |
| **組体操** | 抱っこをつなげる → 離すと固定 |
| **投げ合い** | 抱っこ → 離すと投げる |
| **カスタム** | ワールド制作者が動作を調整する |

<div class="note"><strong>配置は1 Sceneにつき1つだけ。</strong> 主要3モードは初期設定済みです。ワールドに既存の <code>EventSystem</code> がない場合は1つ用意してください。</div>

### 常設UIを配置・複製する

選んだモードのPrefab直下にある `DakoUI`／`GymnasticsUI`／`BattleUI` を移動して、利用者が操作しやすい場所に置きます。Desktopの利用者はこの常設UIで許可を設定します。

複数箇所に置く場合は、同じシステム内の上記UIルートを複製してください。`Panel` だけや、ギミックの本体Prefab全体は複製しません。元と同じシステムへの参照を保つと、どの常設UIからでも本人の同じ許可設定を変更できます。

### カスタムモードを使う場合

カスタムモードは、抱っこ・投げ・固定などの動作を調整する制作者向けです。ルートのInspectorで初期設定を調整し、常設の `CustomUI` と、ワールド設定・管理権限のUIを配置します。常設UIを増やす場合は `CustomUI` だけを複製します。

実行中の共有設定を変更できるのは、管理権限UIで選ばれた管理者です。「離した位置・姿勢に固定する」がONの場合は、「投げを許可」もONであっても、離すと固定されます。

主要3モードの操作説明は初期設定に合わせた内容です。制作者が動作を変更する場合は、利用者向けの案内も合わせて調整してください。

### Prefabから直接配置する場合

<code>Packages/jp.aramaa.player-carry-and-throw/Runtime/Prefabs/</code> にある以下のPrefabを1つ選びます。

- だこちて：<code>PlayerCarryAndThrow_Dako.prefab</code>
- 組体操：<code>PlayerCarryAndThrow_Gymnastics.prefab</code>
- 投げ合い：<code>PlayerCarryAndThrow_Battle.prefab</code>
- カスタム：<code>PlayerCarryAndThrow_Custom.prefab</code>

共通ベースの `PlayerCarryAndThrow_Base.prefab` やUI部品を、導入用の本体として直接配置しないでください。

<h2 id="package-update">更新・削除するとき</h2>

更新前に、配置位置・Inspectorで変更した設定・外部スクリプトからの参照を控え、プロジェクトをバックアップします。VCCで対象プロジェクトの **Manage Project → Manage Packages** を開き、本パッケージに更新が表示されている場合は更新操作を行います。更新がなければ、そのまま使えます。更新後は、ワールド内の表示と操作を再確認してください。

旧構造のPrefabから更新する場合は、参照や独自設定が自動で引き継がれないことがあります。配置メニューは、シーンに本体があると新しい本体を追加できません。バックアップと設定・参照の記録を済ませてから、次の順に移行してください。

1. 旧本体と、別途配置した旧UIをシーンから取り除きます。
2. 配置メニューから、新しいモードPrefabを1つ配置します。
3. 控えておいた配置位置・設定を反映し、外部スクリプトなどの参照を新しい本体へ設定し直します。
4. 本体が1つだけであることと、UI・抱っこ・解除などの動作を確認します。

削除するときは、先にシーン内の本体・UIと外部スクリプトからの参照を取り除き、その後VCCからパッケージを削除します。ほかのUdonも使用するため、`Assets/SerializedUdonPrograms` フォルダー全体は削除しないでください。

同梱フォントは現行UI向けです。独自の説明文やプレイヤー名を追加する場合は、必要な文字を含むフォントを用意してください。同梱音源を使う場合は、[第三者素材の通知とクレジット](https://github.com/aramaa-vr/player-carry-and-throw/blob/master/Third%20Party%20Notices.md)も確認してください。

<div class="action-row" id="contact"><a class="primary" href="{{ '/play/' | relative_url }}">遊び方へ進む</a><a href="{{ '/contact/' | relative_url }}">不具合・不明点のお問い合わせ</a></div>
