---
description: 次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。 アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。 このフィルターを増分同期で使用することはできません。
seo-description: Follow these instructions to generate a full synchronization file that includes recently active users only. You may want to filter for active users to push relevant data to an on-site targeting system or to limit the size of the files sent to a DSP. You cannot use this filter with incremental synchronization.
seo-title: Filter Outbound Data by Active Users Only
title: 発信データをアクティブユーザーのみにフィルタリング
uuid: a2b4a385-eee3-458c-b978-09509cacb397
exl-id: d501cfd1-64dd-448e-92c5-180c0081d3e5
TQID: https://experienceleague.adobe.com/rr6ABB4pgrhkWG88VenqIcbyAaPQfbg258M6SVdE28k
product_v2: id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2: id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 100%

---

# 発信データをアクティブユーザーのみにフィルタリング {#filter-outbound-data-by-active-users-only}

次の手順に従って、最近アクティブなユーザーのみが含まれる、完全な同期ファイルを生成します。 アクティブユーザーをフィルタリングして、関連するデータをオンサイトのターゲット設定システムにプッシュしたり、DSP に送信するファイルのサイズを制限することが必要となる場合があります。 このフィルターを増分同期で使用することはできません。

>[!NOTE]
>
>訪問者が「アクティブ」と認定されるには、訪問者が選択した顧客サイトや広告トラフィックで認識される必要はありません。 任意の [!DNL Audience Manager] ユーザーまたはパートナーに認識されれば、「アクティブ」と認定されます。

アクティブなユーザーのみをフィルタリングするには、次の手順に従います。

1. 「**[!UICONTROL Companies]**」をクリックします。
1. 目的の会社を選択して、「**[!UICONTROL Destinations]**」をクリックします。
1. 「[!UICONTROL Batch Data]」セクションで、次の各オプションを設定します。

   * **[!UICONTROL Sync Type]**：**[!UICONTROL Customer]** または **[!UICONTROL Platform]** を選択します。
   * **[!UICONTROL Sync Type Lookback Period]**：この期間により、データファイルの範囲が設定されます。 選択肢には、**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]** などがあります。
   * **[!UICONTROL Incremental Sync Scheduled Run]**： **[!UICONTROL Never]** を選択します。 このフィルターは完全同期ファイルに対してのみ適用されます。
   * **[!UICONTROL Full Sync Scheduled Run]**：このファイルを受け取る頻度を決定します。 選択肢には、**[!UICONTROL 24 hours]**、**[!UICONTROL 7 days]**、**[!UICONTROL 30 days]**、または **[!UICONTROL Never]**（無効化する場合）などがあります。

1. 「**[!UICONTROL Save]**」をクリックします。
