---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new HTTP server or to edit an existing server.
seo-title: Create or Edit an HTTP Server
title: HTTP サーバーの作成または編集
uuid: 1ef0e751-e239-4dc6-a4f6-73cc05686807
exl-id: 8b3dfb1e-2dee-4a05-835e-3c32643336bc
TQID: https://experienceleague.adobe.com/vcybBl222PvpcEeMFtPZyqbP-YWHCNKF9luqmTZ1C7Y
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: a8b0238e-1d43-4679-a3b4-5ba1bad83baa
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 315
ht-degree: 100%

---

# HTTP サーバーの作成または編集 {#create-or-edit-an-http-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい HTTP サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>新しいサーバーの作成や既存のサーバーの編集をおこなうには、[!UICONTROL DEXADMIN] の役割が必要です。

1. 新しいサーバーを作成するには、**[!UICONTROL Servers]**／**[!UICONTROL Create Server]** に移動します。 既存のサーバーを編集するには、「**[!UICONTROL Label]**」列で目的のサーバーをクリックします。
1. このサーバーで使用するラベルを指定します。
1. **[!UICONTROL Protocol]**&#x200B;ドロップダウンリストで、目的のプロトコル（[!DNL HTTP]）を選択します。
1. 以下のフィールドを設定します。

   * **[!UICONTROL Domain]：**&#x200B;このサーバーで使用するドメイン（ホスト）を指定します。
   * **[!UICONTROL Port]：**&#x200B;このサーバーで使用するポートを指定します。 デフォルトのポートは、暗号化タイプごとに表示されます。 必要があればデフォルトのポートを変更できます。
   * **[!UICONTROL Maximum Users Per Request]：**&#x200B;このサーバーで許可する、リクエストごとの最大ユーザー数を指定します。
   * **[!UICONTROL URL Prefix]：**&#x200B;このサーバーで使用する [!DNL URL] 接頭辞を指定します。
   * **[!UICONTROL Authentication URL]：**&#x200B;この [!UICONTROL Authentication URL] サーバーの `HTTP` を指定します。
   * **[!UICONTROL Authentication]：**&#x200B;目的の認証方法（**[!UICONTROL None]**、**[!UICONTROL Username/Password]**、または **[!UICONTROL SSH Key]**）を指定します。
   * **[!UICONTROL HTTP Signature Header]：**[!DNL HTTP] 署名キーを含む [!DNL HTTP] ヘッダーの名前。顧客が指定します。 デフォルト値は、次の例のように [!UICONTROL X-Signature] です。

     ```
     * Connected to partner.website.com (127.0.0.1) port 80 (#0)
     > POST /webpage HTTP/1.1
     > Host: partner.host.com
     > Accept: */*
     > Content-Type: application/json
     > Content-Length: 20
     > X-Signature: wxa2ByMWhhP328EvHQsVlOD5jTc=
     POST message content
     ```

   * **[!UICONTROL HTTP Signature Key]：**[!DNL HTTP] リクエストの署名に使用するキー。顧客が指定します。
   * **[!UICONTROL Show Signature Key]：**&#x200B;ブラウザーでの署名の表示と非表示を切り替えます。
   * **[!UICONTROL HTTP Signature Encryption Method]：**&#x200B;署名の暗号化に使用する方式を指定します。 顧客が別途指定しない限り、「[!UICONTROL SHA1]」を使用します。

   >[!NOTE]
   >
   >パートナーの[リアルタイムデータ転送の OAuth 2.0 認証](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/real-time-outbound-transfers/oauth-in-outbound-transfers.html?lang=ja)を有効にするには、以下のテーブルのように、フィールドに入力します。 *斜体*&#x200B;のフィールドは、正確に表のとおりに入力する必要があります。

   | 名前 | 値 |
   |---|---|
   | [!UICONTROL Label] | [!UICONTROL Server with OAuth 2.0 enabled] |
   | [!UICONTROL Protocol] | [!UICONTROL HTTP] |
   | [!UICONTROL Domain] | [!UICONTROL api.partner.com] |
   | [!UICONTROL Port] | [!UICONTROL 443] |
   | [!UICONTROL Maximum Users per Request] | [!UICONTROL 10] |
   | [!UICONTROL URL Prefix] | [!UICONTROL /segments/aam] |
   | [!UICONTROL Authentication URL] | [!UICONTROL api.partner.com/oauth2/token] |
   | [!UICONTROL Authentication] | [!UICONTROL Username/Password] |
   | [!UICONTROL Username] | [!UICONTROL *Authorization*] |
   | [!UICONTROL Password] | （パスワードをここに入力） |
   | [!UICONTROL HTTP Signature Header] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Key] | [!UICONTROL Leave this field blank] |
   | [!UICONTROL HTTP Signature Encryption Method] | [!UICONTROL None] |

1. 新しいサーバーを作成する場合は「**[!UICONTROL Create]**」をクリックし、既存のサーバーを編集する場合は「**[!UICONTROL Update]**」をクリックします。
