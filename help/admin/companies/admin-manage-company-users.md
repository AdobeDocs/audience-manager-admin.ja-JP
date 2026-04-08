---
description: Audience Manager の新規宛先を作成するか、既存の宛先を編集または削除します。
seo-description: Create new Audience Manager users or edit and delete existing users.
seo-title: Manage Company Users
title: 会社ユーザーの管理
uuid: 32c8a4e1-c29c-44d2-8cd4-f4f1be707492
exl-id: a2c5fd10-699f-4a0d-acec-f46811140e48
TQID: https://experienceleague.adobe.com/hr8y9o-ghVHBh-O-7w0MtTV2yoXIpqc0BvLf8CSzpN8
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 100%

---

# 会社ユーザーの管理 {#manage-company-users}

Audience Manager の新規宛先を作成するか、既存の宛先を編集または削除します。

<!-- t_manage_company_users.xml -->

1. **[!UICONTROL Companies]**&#x200B;をクリックし、目的の会社を検索してからクリックして、[!UICONTROL Profile] ページを表示します。

   「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用して、目的の会社を検索します。 目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。
1. 「**[!UICONTROL Users]**」タブをクリックします。
1. 新しいユーザーを作成するには、「**[!UICONTROL Create a New User]**」をクリックします。 既存のユーザーを編集するには、「**[!UICONTROL Username]**」列で目的のユーザーを特定してクリックします。

   ![](assets/users.png)

1. 以下のフィールドを設定します。

   * **[!UICONTROL First Name]**：（必須）ユーザーの名を指定します。
   * **[!UICONTROL Last Name]**：（必須）ユーザーの姓を指定します。
   * **[!UICONTROL Username]**：（必須）ユーザーの Audience Manager ユーザー名を指定します。 ユーザー名は一意でなければなりません。
   * **[!UICONTROL Email Address]**：（必須）ユーザーの電子メールアドレスを指定します。
   * **[!UICONTROL Phone Number]**：ユーザーの電話番号を指定します。
   * **[!UICONTROL IMS ID]**：ユーザーの [!UICONTROL Identity Management System ID]。 この ID により、ユーザーはアドビのソリューションを Adobe Experience Cloud にリンクすることができます。
   * **[!UICONTROL Is Admin]**：このユーザーを Audience Manager 管理ユーザーにします。 管理者はこのパートナーに対して Audience Manager のすべてのユーザー役割を持っています。
   * **[!UICONTROL Status]**：新しいユーザーの作成時、このフィールドには最初に「**[!UICONTROL Pending]**」と表示されます。この状態は、ユーザーがログインして臨時パスワードをリセットするまで続きます。 既存のユーザーを編集する場合、次のいずれかのステータスを選択できます。
      * **[!UICONTROL Active]**：このユーザーがアクティブな Audience Manager ユーザーであることを表します。
      * **[!UICONTROL Deactivated]**：このユーザーが非アクティブな Audience Manager ユーザーであることを表します。
      * **[!UICONTROL Expired]**：このユーザーが有効期限切れであることを表します。
      * **[!UICONTROL Locked Out]**：このユーザーがロックアウトされていることを表します。

1. 「**[!UICONTROL Submit]**」をクリックします。

## ユーザーの削除 {#delete-user}

ユーザーを削除するには：

1. 「**[!UICONTROL Companies]**」をクリックし、目的の会社を特定してからクリックして、その後「**[!UICONTROL Users]**」タブをクリックします。
1. 目的のユーザーの「![](assets/icon_delete.png)」列で **[!UICONTROL Actions]** をクリックします。
1. 「**[!UICONTROL OK]**」をクリックして削除を確定します。
