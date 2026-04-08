---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい S3 サーバーを作成するか、既存のサーバーを編集します。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new S3 server or to edit an existing server.
seo-title: Create or Edit an S3 Server
title: S3 サーバーの作成または編集
uuid: 94fee787-eb26-45aa-b602-d61ab12969ea
exl-id: 89310de0-e24e-4d4b-8171-56faf0b441f6
TQID: https://experienceleague.adobe.com/rtXpkVovwbjCwLk3caZ7Ii-LLcr2n3eL73OADaLoul0
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 211
ht-degree: 100%

---

# S3 サーバーの作成または編集 {#create-or-edit-an-s-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい [!DNL S3] サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>新しいサーバーの作成や既存のサーバーの編集をおこなうには、[!UICONTROL DEXADMIN] の役割が必要です。

1. 新しいサーバーを作成するには、**[!UICONTROL Servers]**／**[!UICONTROL Create Server]** をクリックします。 既存のサーバーを編集するには、「**[!UICONTROL Label]**」列で目的のサーバーをクリックします。
1. このサーバーで使用するラベルを指定します。
1. **[!UICONTROL Protocol]**&#x200B;ドロップダウンリストで、目的のプロトコル（**[!UICONTROL S3]**）を選択します。

   >[!NOTE]
   >
   >パートナー間でのファイルのやり取りには、[!DNL Amazon S3] を使用する方法を推奨します。 [!DNL Amazon S3] が提供するシンプルな Web サービスのインターフェイスを使用することで、あらゆるサイズのデータの保存および取得が Web 上でいつ、どこでも可能になります。 詳細については、*Audience Manager 製品ドキュメント*&#x200B;の [Amazon S3 について](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html?lang=ja)を参照してください。

1. 以下のフィールドを設定します。

   * **[!UICONTROL Account]：**&#x200B;目的の [!DNL S3] アカウントを指定します。
   * **[!UICONTROL Bucket]：**&#x200B;目的の [!DNL S3] バケットを指定します。
   * **[!UICONTROL Directory]：**&#x200B;目的の [!DNL S3] ディレクトリを指定します。
   * **[!UICONTROL Access Key]：**&#x200B;目的の [!DNL S3] アクセスキーを指定します。
   * **[!UICONTROL Secret Key]：**&#x200B;目的の [!DNL S3] 秘密鍵を指定します。

1. 新しいサーバーを作成する場合は「**[!UICONTROL Create]**」をクリックし、既存のサーバーを編集する場合は「**[!UICONTROL Update]**」をクリックします。
