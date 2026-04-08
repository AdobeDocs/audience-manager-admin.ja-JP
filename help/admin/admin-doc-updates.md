---
description: Audience Manager Admin Guide のすべての更新（追加、削除、修正）を日付別に紹介。
seo-description: All updates (additions, deletions, and corrections) to the Audience Manager Admin Guide, by date.
seo-title: Documentation Updates
title: ドキュメントのアップデート
uuid: 1c02dff5-8e3f-42bf-a50c-03b75e121ac7
exl-id: 8221b4df-99c2-47d3-a2ea-186a701a2b20
TQID: https://experienceleague.adobe.com/QQHJ9VBxkF-pMFYIvgny6JJRS38Q-3nXD1kSzWdGJxQ
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: baaa0dd2-d27e-4921-aae3-7888623a5fa5
  - id: c814092e-2730-45e8-a12d-e084529f52cb
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 644
ht-degree: 100%

---

# ドキュメントのアップデート {#documentation-updates}

Audience Manager Admin Guide のすべての更新（追加、削除、修正）を日付別に紹介。

機能リリース、改良点、バグの修正の詳細については、[Experience Cloud リリースノート](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=ja)を参照してください。 [!DNL Audience Manager] ドキュメントの変更点については、[ドキュメントの更新](https://experienceleague.adobe.com/docs/audience-manager/user-guide/documentation-updates/docs-2019.html?lang=ja)を参照してください。

## AAM 2019 ドキュメントのアップデート {#aam-2019-docs-updates}

| トピック | 説明 |
|--- |--- |
| HTTP 形式マクロ | 新しいマクロ、`REGION_ID_LIST`、および 3 つの新しいフィールド（`sda`、`sda`、および `sda`）を `USER_LIST` マクロに追加しました。 |
| HTTP 形式マクロ | `ECID` と `MCID` の 2 つの新しいマクロを追加しました。 |

## AAM 2018 ドキュメントのアップデート {#aam-2018-docs-updates}

<!-- c_doc_updates.xml -->

<table id="table_AECF59E131F84E7791A5A421BFB203FA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> トピック </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> FTP サーバーの作成または編集</a> </p> </td> 
   <td colname="col2"> <p>SFTP サーバーの SSH キー認証（ステップ 5）に関する情報を追加しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-destination-troubleshooting.md#set-up-destinations-export"> Experience Cloud を書き出す宛先の設定方法</a> </p> </td> 
   <td colname="col2"> <p>このページでは、送信データファイルで必要な ID タイプをキーとするデータを書き出すための宛先を設定する方法を説明します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/admin-authorize-s3-cross-bucket.md#task_20B12994C5484A9D8CC40DF6F456CBE7"> 手順：バッチ保存先へのクロスアカウント Amazon S3 バケットアクセスを承認</a> </p> </td> 
   <td colname="col2"> <p>顧客が Amazon S3 のアクセスキーとシークレットキーを共有しない場合は、送信データファイルの配信に Amazon S3 のクロスアカウントのバケットのアクセス許可を使用できます。 このドキュメントでは、Audience Manager Admin UI でこの代替手段を設定する方法を説明します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2017 ドキュメントのアップデート {#aam-2017-docs-updates}

<table id="table_81D2DA9293A9417085C630D00A7C96E1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> トピック </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP 形式マクロ</a> </td> 
   <td colname="col2"><code>segmentId</code> マクロを <code>legacySegmentId</code> に置き換え、<code>newSegmentId</code> マクロを追加しました。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-company-limits.md#task_3004C10CB9A9430A8D25E25BB830B5D6"> 会社制限の管理</a> </td> 
   <td colname="col2"> 特性フォルダーの最大数と、特性構造の深度を、制限のドキュメントに追加しました。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="formats/enable-outbound-seq.md#concept_526744C9433F40BF8269E18245B2F0BD"> 送信用の Hadoop シーケンスファイル転送の有効化</a> </td> 
   <td colname="col2"> 顧客が送信 SEQ ファイルを自分の Hadoop インスタンスに送信できるようにする方法を説明します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-containers.md#task_61DB5CEECC5049DD8D059C642AC3F967"> コンテナの管理</a> </td> 
   <td colname="col2"> コンテナの作成方法について簡単な説明を追加しました。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><a href="companies/admin-manage-company-destinations.md#create-edit-company-destinations"> 会社宛先の作成または編集</a> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_527E0E75C03846B0AB39EEE544904BE2"> 
      <li id="li_FC276B34158D44E3A5450C6C8BAF3184">完全同期と差分同期の使用のバランスについて説明を追加しました。 </li> 
      <li id="li_3975DA78DE9E441D8F8CB80F752DD7B7"><span class="keyword">Adobe Media Manager</span> を <span class="keyword">Audience Manager</span> 宛先としてプロビジョニングする処理は、<span class="keyword">Adobe Media Manager</span> 内でおこなわれます。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 会社宛先の管理</a> </p> </td> 
   <td colname="col2"> <p>マイナーな改訂。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-amo-sync.md#concept_2B5537233DAA4860B3503B344F937D83"> Media Manager との ID 同期</a> </p> </td> 
   <td colname="col2"> <p>各会社コンテナの AMO 同期チェックボックスについて説明する新しいドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-device-graph-options.md#concept_563615F1018340C683E0EE075F8F639D"> 会社のデバイスグラフオプション</a> </p> </td> 
   <td colname="col2"> <p>デバイスグラフオプションの設定方法を説明する新しいドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-oauth2/aam-admin-api-requirements.md#concept_A7FAC9443CF34974A873E6B787616421"> API の要件とレコメンデーション</a> </p> </td> 
   <td colname="col2"> <p>注意が必要であり、顧客に伝える必要がある要件と推奨事項について説明する新しいドキュメント。 公開ドキュメントに同じタイトルのドキュメントがありますが、異なる読者層向けに変更されている箇所があります。 公開ドキュメントの <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html?lang=ja#api-requirements-recommendations" format="https" scope="external">API の要件とレコメンデーション</a>を参照してください。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2016 ドキュメントのアップデート {#aam-2016-docs-updates}

<table id="table_E9D9810EA8244B58A4F27D56CFE521FD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> トピック </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"><a href="admin-servers/create-ftp-server.md#task_BF1DD0E5ECA64AEC87EACABFCAEA2C6D"> FTP サーバーの作成または編集</a> </td> 
   <td colname="col2">エグレス FTP IP <b>52.44.29.204</b> を追加しました。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 会社宛先の管理</a> </p> </td> 
   <td colname="col2"> <p>マイナーな改訂。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-servers/create-http-server.md#task_5BF59581868E4144B965D644D36BEACD"> HTTP サーバーの作成または編集</a> </p> </td> 
   <td colname="col2"> <p>Create Server Configuration ウィザードに <b>HTTP 署名</b>を追加しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="admin-beta-environment.md#concept_4AA12E66F49A452C8BA4E91AA28060AA"> Beta 環境</a> </p> </td> 
   <td colname="col2"> <p>Beta 環境の URL とホスト名を更新しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="companies/outbound-active-user-filter.md#task_F5CF8BDDA5DB4D23837B59CADF7A623B"> 発信データをアクティブユーザーのみにフィルタリング</a> </p> </td> 
   <td colname="col2"> <p>最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成するための手順。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-formats.md#reference_C392124A5F3F42E49F8AADDBA601ADFE"> HTTP 形式マクロ</a> </p> </td> 
   <td colname="col2" morerows="1"> <p>HTTP マクロと一般的な例の一覧を示す新しいドキュメント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><a href="formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31"> HTTP 形式マクロの例</a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2015 ドキュメントのアップデート {#aam-2015-docs-updates}

<table id="table_90F524BAAED44A45A1F6BF8BBA9F26F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日付およびトピック </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2015 年 12 月 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 形式</a> </p> </td> 
   <td colname="col2"> <p>マクロの項を改訂し、例を追加しました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## AAM 2014 ドキュメントのアップデート {#aam-2014-docs-updates}

<table id="table_FA9962E19248418BA73D5A794A378C9D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 日付およびトピック </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>2014 年 11 月 12 日 </p> <p> <a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 形式</a> </p> </td> 
   <td colname="col2"> <p>&lt;MCID&gt; マクロに関する情報を追加しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 23 日 </p> <p><a href="formats/admin-create-format.md#task_1A51FC9189DB439FB218D91F3875FD67"> 形式の作成または編集</a> </p> </td> 
   <td colname="col2"> <p>「<span class="wintitle">.info Receipt</span>」オプションに関する情報を追加しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 23 日 </p> <p><a href="formats/formats.md#concept_66AA2E78A25C4973B3230D5F75B192A2"> 形式</a> </p> </td> 
   <td colname="col2"> <p>新規ページ。 このページは現在作成中で、近い将来更新されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 22 日 </p> <p><a href="admin-destination-troubleshooting.md#"> 宛先の設定に関するトラブルシューティング</a> </p> </td> 
   <td colname="col2"> <p>新規トピックです。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 10 月 21 日 </p> <p><a href="companies/admin-manage-company-destinations.md#manage-company-destinations"> 会社宛先の管理</a> </p> </td> 
   <td colname="col2"> <p>トピック全体を改訂しました。 情報と設定を追加しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 9 月 25 日 </p> <p><a href="companies/admin-manage-company-profiles.md"> 会社の作成</a> </p> </td> 
   <td colname="col2"> <p>「<span class="wintitle">ライフサイクル</span>」および「<span class="wintitle">アカウントタイプ</span>」の各項に情報を追加しました。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2014 年 9 月 25 日 </p> <p><a href="companies/admin-manage-company-profiles.md#edit-company-profile"> 会社プロファイルの編集</a> </p> </td> 
   <td colname="col2"> <p>「<span class="wintitle">ライフサイクル</span>」および「<span class="wintitle">アカウントタイプ</span>」の各項に情報を追加しました。 </p> </td> 
  </tr> 
 </tbody> 
</table>
