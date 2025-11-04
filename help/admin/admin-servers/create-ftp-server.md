---
description: Audience Manager の Admin ツールの Servers ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。
seo-description: Use the Servers page in the Audience Manager Admin tool to create a new FTP server or to edit an existing server.
seo-title: Create or Edit an FTP Server
title: FTP サーバーの作成または編集
uuid: 9273abb2-963d-4d83-bf5a-b3817f0b90e6
exl-id: 9eae4ecf-ccde-483a-ae53-1cbac033d8d6
source-git-commit: 92bf9b281c71e38d1bd5e0229f550a2124080b21
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 97%

---

# FTP サーバーの作成または編集 {#create-or-edit-an-ftp-server}

Audience Manager の Admin ツールの [!UICONTROL Servers] ページを使用して、新しい FTP サーバーを作成するか、既存のサーバーを編集します。

>[!NOTE]
>
>新しいサーバーの作成や既存のサーバーの編集をおこなうには、[!UICONTROL DEXADMIN] の役割が必要です。

1. 新しいサーバーを作成するには、**[!UICONTROL Servers]**／**[!UICONTROL Create Server]** をクリックします。既存のサーバーを編集するには、「**[!UICONTROL Label]**」列で目的のサーバーをクリックします。
1. このサーバーで使用するラベルを指定します。
1. 「**[!UICONTROL Protocol]**」ドロップダウンリストで、目的のプロトコル **FTP** を選択します。

   >[!NOTE]
   >
   >ベストプラクティスとして、パートナー間でのファイルのやり取りには、[!DNL Amazon S3] を推奨します。[!DNL Amazon S3] が提供するシンプルな Web サービスのインターフェイスを使用することで、あらゆるサイズのデータの保存および取得が Web 上でいつ、どこでも可能になります。詳細については、*Audience Manager 製品ドキュメント*&#x200B;の [Amazon S3 について](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/amazon-s3.html?lang=ja)を参照してください。

1. 以下のフィールドを設定します。

   * **[!UICONTROL Type]：**&#x200B;目的の暗号化タイプ（**[!UICONTROL SFTP]** または **[!UICONTROL FTPs/TLS]**）を選択します。
   * **[!UICONTROL Domain]：**&#x200B;このサーバーで使用するドメイン（ホスト）を指定します。
   * **[!UICONTROL Port]：**&#x200B;このサーバーで使用するポートを指定します。デフォルトのポートは、暗号化タイプごとに表示されます。必要があればデフォルトのポートを変更できます。
   * **[!UICONTROL Remote Path]：**&#x200B;このサーバーで使用するリモートパスを指定します。このフィールドを空白にすると、Audience Manager はファイルをデフォルトのディレクトリに配置します。
   * **[!UICONTROL .tmp File Rename on Completion]：**&#x200B;このオプションを有効にすると、完了時に `.tmp` ファイルの名前を変更できます。
   * **[!UICONTROL Filename Suffix]：**&#x200B;転送ファイルに追加するテキストを指定します。
   * **[!UICONTROL Moved to When Finished]：**&#x200B;完了時に転送ファイルを移動する場所のパスを指定します。
   * **[!UICONTROL Authentication]：**&#x200B;目的のサーバー認証方式（**[!UICONTROL Username/Password]** または **[!UICONTROL SSH Key]**）を選択します。

   >[!NOTE]
   >
   >許可されている IP のリストにエグレス [!DNL FTP] [!DNL IP] を必ず追加してください：**54.204.116.43**。

1. **[!UICONTROL SSH Key]** 認証の場合：

   >[!NOTE]
   >
   >SSH キー認証を設定する場合は、常に OpenSSH 形式のみの公開鍵と秘密鍵を生成するようにしてください。

   1. 任意の [!DNL Linux]または [!DNL Mac] マシンから、公開鍵／秘密鍵のペアを生成します。
   1. **公開鍵**&#x200B;をクライアントに渡して、[!DNL SFTP] サーバーで更新します。これには、サーバー上にある公開鍵 （`-----BEGIN RSA PRIVATE KEY-----` や `-----END RSA PRIVATE KEY-----` を含む）のすべてのテキストを含める必要があります。一方、クライアントは鍵のインストールに使用するユーザー名を指定する必要があります。
   1. ユーザー名フィールドにクライアントが指定したユーザー名を入力し、鍵フィールドには&#x200B;**秘密鍵**&#x200B;を入力します。

1. 新しいサーバーを作成する場合は「**[!UICONTROL Create]**」をクリックし、既存のサーバーを編集する場合は「**[!UICONTROL Update]**」をクリックします。
