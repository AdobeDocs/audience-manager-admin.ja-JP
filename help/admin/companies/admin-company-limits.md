---
description: 会社のアルゴリズムモデル、セグメント、宛先、特性の各制限を管理します。
seo-description: Manage the following limits for the company  algorithmic models, segments, destinations, and traits.
seo-title: Manage Company Limits
title: 会社制限の管理
uuid: 67a19fb2-8322-47ce-afa4-f6b78c52f814
exl-id: dd6d04ef-895a-4bd7-bf9d-851e2fdcb594
source-git-commit: f5d74995f0664cf63e68b46f1f3c608f34df0e80
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 100%

---

# 会社制限の管理 {#manage-company-limits}

会社について、アルゴリズムモデル、セグメント、宛先、特性の各制限を管理します。

<!-- t_company_limits.xml -->

1. **[!UICONTROL Companies]**&#x200B;をクリックし、目的の会社を検索してからクリックして、[!UICONTROL Profile] ページを表示します。「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用して、目的の会社を検索します。目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。
1. 「**[!UICONTROL Limits]**」タブをクリックします。
1. 以下のフィールドを設定します。

   >[!NOTE]
   >
   >いずれかのフィールドが空の場合、現在のデフォルトは無制限となります。すべてのフィールドは独立しています。例えば、「[!UICONTROL Trait Limits]」セクションで、「[!UICONTROL Total Traits]」に 100、他の特性タイプに 100 を指定できます。[!UICONTROL Max Number of Algorithmic Traits]、[!UICONTROL Max Number or Rule Based Traits]、および [!UICONTROL Max Number of Onboarded Traits] の合計は [!UICONTROL Total Number] とは等しくありません。

   * **[!UICONTROL Trait Folder Limits]**：この会社の[!UICONTROL Trait Folder]の制限を指定します。
      * **[!UICONTROL Max number of Trait Folders]**：この会社が保有できる[!UICONTROL Trait Folders]の最大数を指定します。
      * **[!UICONTROL Max depth of Trait Folders]**：会社 [!UICONTROL Trait Folder] の構造で使用できる最大の深さを指定します。
   * **[!UICONTROL AlgoModel Limits]**：この会社のアルゴリズムの制限を指定します。
      * **[!UICONTROL Total Number]**：この会社が保有できるアルゴリズム特性の合計数を指定します。
   * **[!UICONTROL Segment Limits]**：この会社のセグメントの制限を指定します。
      * **[!UICONTROL Total Number]**：この会社が保有できるセグメントの合計数を指定します。
   * **[!UICONTROL Destinations Limits]**：この会社の宛先の制限を指定します。
      * **[!UICONTROL Total Number]**：この会社が保有できる宛先の合計数を指定します。
      * **[!UICONTROL Max Number of URL Destinations]**：この会社が保有できる URL 宛先の最大数を指定します。
      * **[!UICONTROL Max Number of AdServer Destinations]**：この会社が保有できる [!UICONTROL AdServer] 宛先の最大数を指定します。
      * **[!UICONTROL Max Number of S2S Destinations]**：この会社が保有できる S2S 宛先の最大数を指定します。
   * **[!UICONTROL Trait Limits]**：この会社の特性の制限を指定します。
      * **[!UICONTROL Total Number]**：この会社が保有できる特性の合計数を指定します。
      * **[!UICONTROL Max Number of Algorithmic Traits]**：この会社が保有できるアルゴリズム特性の最大数を指定します。
      * **[!UICONTROL Max Number of Rule Based Traits]**：この会社が保有できるルールベースの特性の最大数を指定します。
      * **[!UICONTROL Max Number of Onboarded Traits]**：この会社が保有できるオンボードの特性の最大数を指定します。
1. 「**[!UICONTROL Save]**」をクリックします。
