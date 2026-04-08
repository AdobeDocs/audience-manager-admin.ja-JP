---
description: ベータ環境は Audience Manager の実装のテストに使用します。 ベータ環境でおこなった変更は実稼動データに影響しません。 Audience Manager ベータ環境は、実稼動環境の小規模なスタンドアロンバージョンです。 テストするデータはすべてこの環境で入力および収集する必要があります。
seo-description: The beta environment is for testing Audience Manager implementations. Changes made in beta do not affect production data. The Audience Manager beta environment is a smaller-scale, standalone version of the production environment. All the data that you want to test must be entered and collected in this environment.
seo-title: Beta Environment
solution: Audience Manager
title: Beta 環境
uuid: 6a253f4e-96e7-4395-a783-a8eb213b7daf
exl-id: 78d5a1ff-c016-4366-ba34-9814a0d92067
TQID: https://experienceleague.adobe.com/Y6hON41v53cSXtuTYMW8UMgimwyewWHvfcBvMYDnBa4
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: a8b0238e-1d43-4679-a3b4-5ba1bad83baa
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 93%

---

# Beta 環境 {#beta-environment}

ベータ環境は Audience Manager の実装のテストに使用します。 ベータ環境でおこなった変更は実稼動データに影響しません。 Audience Manager ベータ環境は、実稼動環境の小規模なスタンドアロンバージョンです。 テストするデータはすべてこの環境で入力および収集する必要があります。

## 概要 {#overview}

<!-- beta_environment_admin.xml -->

| サービス | URL／ホスト名 | プロビジョニングの手順 |
|--- |--- |--- |
| S3 | | [Amazon S3 バケットのプロビジョニング](admin-beta-environment.md#provision-s3-buckets)を参照してください。 |
| DCS | https&colon;//dcs-beta.demdex.net/... | 追加の手順は必要ありません。 [Beta 環境で DCS にアクセスする](admin-beta-environment.md#access-dcs-beta-environment)を参照してください。 |
| UI | https&colon;//bank-beta.demdex.com | データは、実稼動環境から Beta 環境に毎月コピーされます。 実稼動用の資格情報はベータ版で有効です。 |
| API | https&colon;//api-beta.demdex.com/... | データは、実稼動環境から Beta 環境に毎月コピーされます。 実稼動用の資格情報はベータ版で有効です。 |

## Amazon S3 バケットのプロビジョニング {#provision-s3-buckets}

>[!NOTE]
>
>現在は、[!DNL FTP/SFTP] の使用を停止しています。 また、送信データ転送は Beta 環境では動作しません。

受信データ用 [!DNL S3] のバケットをプロビジョニングするには：

1. [**SKMS リクエスト TechOps ヘルプ**](https://skms.adobe.com/)機能を使用します。
1. 左ナビゲーションレールの **[!UICONTROL Request TechOps Help]** に移動します。
1. **[!UICONTROL Request Search]**&#x200B;で、検索フィールドに「Audience Manager」と入力します。
1. 検索結果を下にスクロールして **Audience Manager - S3 受信 / 送信アカウントのプロビジョニング**&#x200B;をクリックします。
1. プロビジョニングウィンドウのフィールドに入力し、「**[!UICONTROL Environment]**」フィールドの **サンドボックス環境** を指定します。

>[!NOTE]
>
>[!DNL FTP/SFTP] の使用は推奨しませんが、[!UICONTROL Amazon S3] の使用をお勧めします。 [!UICONTROL Amazon S3]の使用を推奨する理由は、[Amazon S3:About](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html?lang=ja)に記載されています。

## Beta 環境で DCS にアクセスする {#access-dcs-beta-environment}

Beta 環境で [!UICONTROL DCS] にアクセスする方法

1. [!UICONTROL DCS] [!DNL curl]コマンド[を使用して &#x200B;](https://curl.haxx.se/docs/manpage.html) 呼び出しをおこないます。 [!DNL Curl] は、サポートされている様々なプロトコルの中から 1 つを使用して、サーバー間データ転送をおこなうためのツールです。

   例：`curl -v https://dcs-beta.demdex.net/event`

1. [!UICONTROL DCS] 応答ヘッダー内の「[!DNL sandbox]」を確認し、ベータ版 [!UICONTROL DCS] によって要求が処理されたことを確認します。

   例：

   ```
   curl -v http://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```

<!--
1. Determine the load balancer's endpoint IP addresses.

   Run the `dig` [command](https://en.wikipedia.org/wiki/Dig_(command)) to determine the IP address of the nearest load balancer. The `dig` command queries the Domain Name System and returns the name and IP addresses of the Audience Manager [!UICONTROL Data Collection Servers (DCS)].

   ```
   dig dcs-beta.demdex.net
   ...
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.87.15.51
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 50.16.150.8
   dcs-sandbox-1754093861.us-east-1.elb.amazonaws.com. 60 IN A 52.2.228.100
   ```

1. Using one of the addresses in the above table, add a static DNS entry in the [!DNL `/etc/hosts`] file.

   On Windows, modify [!DNL `c:\WINDOWS\system32\drivers\etc\hosts`].

   For example:

[!DNL `52.87.15.51 samplepartner.demdex.net`]

   >[!NOTE]
   >
   >The addresses change occasionally, so you must keep your [!DNL /etc/hosts] file up to date.

   Additionally, if you need to set up ID synchronization, you must add a similar entry for [!DNL dpm.demdex.net.]

[!DNL `52.87.15.51 dpm.demdex.net`] [!DNL]. 

1. Make a [!UICONTROL DCS] call, using the `curl` [command](https://curl.haxx.se/docs/manpage.html). Curl is a tool to transfer data from or to a server, using one of many supported protocols.

   For example:

[!DNL `https://<domain>/event?product=camera`] 

1. Verify that your request was served by the beta [!UICONTROL DCS] by looking for "sandbox" in the [!UICONTROL DCS] response header.

   For example:

   ```
   curl -v https://dcs-beta.demdex.net/?event
   [...]
   < DCS: va6-sandbox-dcs-3.sandbox.demdex.com <release_number>
   [...]
   ```
-->
