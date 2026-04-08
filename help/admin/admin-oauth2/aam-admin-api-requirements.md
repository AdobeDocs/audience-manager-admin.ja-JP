---
description: Audience Manager API を使用しているクライアントへの注意事項。
seo-description: Things you should encourage your clients to be aware of when they're working with the Audience Manager APIs.
seo-title: API Requirements and Recommendations
title: API の要件とレコメンデーション
uuid: eba9cf92-f0c8-4394-8532-0de9a2e7b103
exl-id: 24f90732-31a6-436d-862b-e6871d279c7a
TQID: https://experienceleague.adobe.com/mm5-TOwj8WckXoG4-E4wzuEF-1oBbxbBUvRLOoA--As
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2: id: baaa0dd2-d27e-4921-aae3-7888623a5fa5
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 350
ht-degree: 94%

---

# API の要件とレコメンデーション {#api-requirements-and-recommendations}

Audience Manager [!DNL API] を使用しているクライアントへの注意事項。

## 要件 {#requirements}

[!DNL Audience Manager] [!DNL API] コードを操作する場合は、以下の点に注意してください。

* **リクエストパラメーター：**&#x200B;特に指定のない限り、すべてのリクエストパラメーターが必要となります。
* **[!DNL JSON]コンテンツタイプ：** コード内で、`content-type: application/json` *および* `accept: application/json` を指定してください。

* **要求と応答：**&#x200B;適切な形式の [!DNL JSON] オブジェクトとして要求を送信してください。 [!DNL Audience Manager] は [!DNL JSON] 形式のデータで応答します。 サーバーの応答には要求されたデータもしくはステータスコード、またはその両方を含めることができます。

* **アクセス：**&#x200B;担当の [!DNL Audience Manager] コンサルタントによって、[!DNL API] 要求をおこなうために必要なクライアント ID およびキーが提供されます。

* **ドキュメントおよびコードサンプル：** *斜体* のテキストは、[!DNL API] データを作成または受け取る際に指定または渡される変数を示します。 *斜体*&#x200B;のテキストを独自のコード、パラメーターまたは他の必要な情報に置き換えてください。

## レコメンデーション：汎用の API ユーザーを作成する {#recommendations}

Audience Manager [!DNL API]を使用する場合は、別のテクニカルユーザーアカウントを作成することをお勧めします。 これはクライアントの組織にいる特定のユーザーとは関係がない汎用アカウントです。 このような [!DNL API] ユーザーアカウントにより、以下の 2 つのことができます。

* [!DNL API] を呼び出しているサービスを特定する（[!DNL API] を使用しているクライアントアプリケーションからの呼び出しや、一括変更からの呼び出しなど）。
* [!DNL API]さんへの中断のないアクセスを提供します。 特定の従業員に結び付けられたアカウントは、その従業員が退職すると削除される可能性があります。 その場合、使用可能な [!DNL API] コードの操作ができなくなります。 特定の従業員に結び付けられていない汎用アカウントを使用すると、この問題を回避できます。

このようなアカウントのユースケースとして、顧客が多数のセグメントを[一括管理ツール](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/bulk-management-tools/bulk-management-intro.html?lang=ja)により一度に変更しようとしている場合を見てみましょう。 この処理をおこなうには、[!DNL API] アクセスが必要です。 特定のユーザーに対して権限を追加するのではなく、適切な資格情報、キー、および [!DNL API] 呼び出し用の暗号鍵を持つ汎用の [!DNL API] ユーザーアカウントを作成します。 また、クライアントが [!DNL Audience Manager] [!DNL API] を使用するアプリケーションを開発する場合にも便利です。
