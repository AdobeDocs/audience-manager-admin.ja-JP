---
description: OAuth2 Clients ページを使用して、Audience Manager 構成内の OAuth2 クライアントのリストを表示します。所定のユーザーの役割があれば、既存のクライアントの編集や削除、新しいクライアントの作成ができます。
seo-description: OAuth2 Clients ページを使用して、Audience Manager 構成内の OAuth2 クライアントのリストを表示します。所定のユーザーの役割があれば、既存のクライアントの編集や削除、新しいクライアントの作成ができます。
seo-title: OAuth2 クライアント
title: OAuth2 クライアント
uuid: 3e654053- fb2f-4d8f- a53c- b5c3b8dbdayaa
translation-type: tm+mt
source-git-commit: be661580da839ce6332a0ad827dec08e854abe54

---


# OAuth2 クライアント {#oauth-clients}

Use the [!UICONTROL OAuth2 Clients] page to view a list of [!UICONTROL OAuth2] clients in your [!DNL Audience Manager] configuration. 所定のユーザーの役割があれば、既存のクライアントの編集や削除、新しいクライアントの作成ができます。

## 概要 {#overview}

<!-- c_oauth.xml -->

>[!NOTE]
>
>Ensure that your customer reads the [OAuth2](https://docs.adobe.com/content/help/en/audience-manager/user-guide/api-and-sdk-code/rest-apis/aam-api-getting-started.html#oauth) documentation in the [!DNL Audience Manager User Guide.

[!DNL OAuth2] は、リソース所有者に代わって [!DNL Audience Manager] リソースへの安全な委任アクセスに使用する認証のオープン規格です。

![](assets/oauth.png)

目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。

「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用して、目的のクライアントを検索します。

## OAuth2 クライアントの作成または編集 {#create-edit-client}

<!-- t_create_edit_auth.xml -->

Use the [!UICONTROL OAuth2 Clients] page in the Audience Manager [!UICONTROL Admin] tool to create a new [!UICONTROL Oauth2] client or to edit an existing client.

1. 新しい [!UICONTROL OAuth2] クライアントを作成するには、 **[!UICONTROL OAuth2 Clients]** / **[!UICONTROL Add OAuth2 Client]**&#x200B;をクリックします。To edit an existing [!UICONTROL OAuth2] client, click the desired client in the **[!UICONTROL Client ID]** column.
1. [!UICONTROL OAuth2] このクライアントの名前を指定します。これはそのレコードのみの名前です。
1. [!UICONTROL OAuth2] クライアントの電子メールアドレスを指定します。指定できる電子メールアドレスは 1 つだけです。
1. **[!UICONTROL Partner]** ドロップダウンリストから、目的のパートナーを選択します。
1. **[!UICONTROL Client ID]** ボックスに、目的のIDを指定します。This is the value used when submitting [!DNL API] requests. 前の手順で「[!UICONTROL Partner]」ドロップダウンリストから選択した後に入力を始めると、プレフィックスが自動入力されます。The correct format is &lt; *`partner subdomain`*&gt; - &lt; *`Audience Manager username`*&gt;.
1. Select or deselect the **[!UICONTROL Restrict to Partner Users]** check box, as desired. このチェックボックスをオンにした場合、ユーザーは選択したパートナーにリストされている [!DNL Audience Manager] ユーザーでなければなりません。ベストプラクティスとして、このオプションをオンにすることをお勧めします。
1. **[!UICONTROL Scope]** セクションで、必要に応じて、「 **[!UICONTROL Read]** および **[!UICONTROL Write]** 」チェックボックスを選択または選択解除します。
1. **[!UICONTROL Grant Type]** セクションで、承認に必要な方法を選択します。デフォルトの設定 [!UICONTROL Password] および [!UICONTROL Refresh-token] オプションを使用することをお勧めします。

   * **[!UICONTROL Implicit]**:このオプションを選択すると、ボックスが [!UICONTROL Redirect URI] 有効になります。The user is given an automatic access token after being authenticated and is immediately sent to the redirect [!DNL URI].
   * **[!UICONTROL Authorization Code]**:このオプションを選択すると、ボックスが [!UICONTROL Redirect URI] 有効になります。The user is returned to the client after being authenticated and is then sent to the redirect [!DNL URI].
   * **[!UICONTROL Password]**：ユーザーの認証は、認証サーバーによる自動検証ではなく、ユーザーが入力したパスワードによっておこなわれます。
   * **[!UICONTROL Refresh_token]**: 期限切れのアクセストークンを更新し、期限を延長します。

1. **[!UICONTROL Redirect URI]** ボックスで、必要 [!DNL URI]に応じて指定します。このオプションは、「Grant Type」で「**[!UICONTROL Implicit]**」と「**[!UICONTROL Authorization_code]」を選択した場合のみ有効です。****[!UICONTROL Redirect URI]** このボックスでは、指定可能 [!DNL URI] な値のコンマ区切り値を指定できます。This is the [!DNL URI] a user of a client is redirected to after approving the client for [!DNL API] access.
1. アクセスの有効期間（秒単位）を指定し、トークンの有効期間を更新します。

   * **[!UICONTROL Access Token Expiration Time]**:アクセストークンが発行された後に有効な秒数。null にすると、プラットフォームのデフォルト（12 時間）が使用されます。-1 にすると、アクセストークンの有効期間は無制限になります。
   * **[!UICONTROL Refresh Token Expiration Time]**:更新後に更新トークンが有効な秒数。null にすると、プラットフォームのデフォルト（30 日）が使用されます。

1. 「**[!UICONTROL Save]**」をクリックします。

To delete an [!UICONTROL OAuth2] client, click **[!UICONTROL OAuth2 Clients]**, then click  ![](assets/icon_delete.png) in the **[!UICONTROL Actions]** column for the desired client.

>[!MORE_LIKE_THIS]
>
>* [API の要件と推奨事項](../admin-oauth2/aam-admin-api-requirements.md)
