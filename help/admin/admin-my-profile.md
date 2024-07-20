---
description: Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。
seo-description: Edit the details of your Audience Manager Admin tool profile or change your password.
seo-title: My Profile
title: マイプロファイル
uuid: ccaa611d-c855-484e-9696-081d9b4e0935
exl-id: d213f734-af52-4f43-8733-af67ce6f4e98
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 100%

---

# マイプロファイル {#my-profile}

Audience Manager の Admin ツールプロファイルの詳細情報の編集や、パスワードの変更をおこないます。

<!-- c_my_profile.xml -->

## プロファイルの編集 {#edit-profile}

Audience Manager の Admin ツールプロファイル（氏名、ユーザー名、電子メールアドレス、電話番号、[!UICONTROL IMS ID]、ユーザーの役割、ステータスなど）の表示と編集をおこないます。

<!-- t_edit_profile.xml -->

1. 「**[!UICONTROL My Profile]**」をクリックします。

   ![手順の結果](assets/profile.png)

2. 以下のフィールドを設定します。
   * **[!UICONTROL First Name]：**（必須）名を指定します。
   * **[!UICONTROL Last Name]：**（必須）姓を指定します。
   * **[!UICONTROL Username]：**（必須）ユーザー名を指定します。
   * **[!UICONTROL Email Address]：**（必須）電子メールアドレスを指定します。
   * **[!UICONTROL Phone Number]：**&#x200B;電話番号を指定します。
   * **[!UICONTROL IMS ID]：**&#x200B;インターネットメッセージサービス ID を指定します。
   * **[!UICONTROL User Roles]：**&#x200B;目的のユーザーの役割を選択します。
      * **[!UICONTROL DEXADMIN]：** Audience Manager の Admin ツールでタスクを実行するための管理者アクセス権を付与します。このオプションを選択しない場合、個別の役割を選択できます。これらの役割を使用すると、ユーザーは [!DNL API] 呼び出しを使用してタスクをおこなえますが、Admin ツールではおこなえません。
      * **[!UICONTROL CREATE_USERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して新しいユーザーを作成できます。
      * **[!UICONTROL DELETE_USERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して既存のユーザーを削除できます。
      * **[!UICONTROL EDIT_USERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して既存のユーザーを削除できます。
      * **[!UICONTROL VIEW_USERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して、Audience Manager 構成内の他のユーザーを表示できます。
      * **[!UICONTROL CREATE_PARTNERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを作成できます。
      * **[!UICONTROL DELETE_PARTNERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを削除できます。
      * **[!UICONTROL EDIT_PARTNERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを編集できます。
      * **[!UICONTROL VIEW_PARNTERS]：**&#x200B;ユーザーは [!DNL API] 呼び出しを使用して Audience Manager パートナーを表示できます。
   * **[!UICONTROL Status]：**&#x200B;目的のステータスを選択します。
      * **[!UICONTROL Active]：**&#x200B;このユーザーがアクティブな Audience Manager ユーザーであることを表します。
      * **[!UICONTROL Deactivated]：**&#x200B;このユーザーが非アクティブな Audience Management ユーザーであることを表します。
      * **[!UICONTROL Expired]：**&#x200B;このユーザーの Audience Manager アカウントが期限切れになっていることを表します。
      * **[!UICONTROL Locked Out]：**&#x200B;このユーザーの Audience Manager アカウントがロックされていることを表します。
3. 「**[!UICONTROL Submit]**」をクリックします。

## パスワードの変更 {#change-password}

Audience Manager の Admin ツールのパスワードを変更します。

<!-- t_change_password.xml -->

1. 「**[!UICONTROL My Profile]**」をクリックします。
1. 「**[!UICONTROL Change Password]**」をクリックします。

   ![](assets/change_password.png)

   Audience Manager のパスワードは次の条件を満たしている必要があります。

   * 8 文字以上である;
   * 少なくとも 1 文字の大文字を含める。
   * 少なくとも 1 文字の小文字を含める。
   * 少なくとも 1 文字の数字を含める。
   * 少なくとも 1 文字の特殊文字を含める。
   * 先頭および末尾には英数字を使用する。
   * 先頭および末尾には英数字を使用する。

1. 元のパスワードを指定します。
1. 新しいパスワードを指定し、新しいパスワードをもう一度確認します。
1. 「**[!UICONTROL OK]**」をクリックします。
