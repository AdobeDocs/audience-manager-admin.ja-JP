---
description: Audience Manager の宛先を作成、編集および削除します。
seo-description: Create, edit, and delete Audience Manager destinations.
seo-title: Manage Company Destinations
title: 会社宛先の管理
uuid: d9a6bfb1-7629-44e0-b7d7-ece44f65ea2b
exl-id: a2e73613-07cd-4ab8-8c6e-be451ed50bfc
TQID: https://experienceleague.adobe.com/-MWpMACN0bFPIRAWejD0-VV5nG8BGAukmV1QXxXal-E
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
feature_v2:
  - id: c814092e-2730-45e8-a12d-e084529f52cb
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 100%

---

# 会社宛先の管理 {#manage-company-destinations}

Audience Manager の宛先を作成、編集および削除します。

<!-- t_company_destinations.xml -->

詳しくは、*Audience Manager ユーザーガイド*&#x200B;の「[宛先](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html?lang=ja)」を参照してください。

## 会社宛先の作成または編集 {#create-edit-company-destinations}

各セクションにスクロールして、[!DNL Audience Manager] の宛先の新規作成、または既存の宛先の編集手順を参照してください。

<!-- create-edit-company-destinations.xml -->

宛先を設定する前に、[Experience Cloud のパートナー統合のページ](https://wiki.corp.adobe.com/x/mPIMPw)を参照してください。 このページには、[!DNL Audience Manager] パートナー統合のそれぞれについて入力する必要がある個別の情報について記載されています。

クライアントが [!DNL Audience Manager] で [!DNL Adobe Media Optimizer] を宛先として使用したい場合は、[!DNL Adobe Media Optimizer] で設定する必要があります。

## 「宛先」タブに移動 {#navigate-destinations}

1. **[!UICONTROL Companies]**&#x200B;をクリックし、目的の会社を検索してからクリックして、[!UICONTROL Profile] ページを表示します。 「[!UICONTROL Search]」ボックス、またはリストの最下部にあるページネーションコントロールを使用すると、目的の会社を検索できます。 目的の列のヘッダーをクリックすると、その列を昇順または降順に並べ替えることができます。
1. 「**[!UICONTROL Destinations]**」タブをクリックします。
1. 新しい宛先を作成するには、「**[!UICONTROL Add Destination]**」をクリックします。 既存の宛先を編集するには、「**[!UICONTROL Name]**」列で宛先の名前をクリックします。

## 基本設定 {#basic-settings}

**[!UICONTROL Basic Settings]** ウィンドウの各フィールドに入力します。

* **[!UICONTROL Name]：**（必須）この宛先の名前を指定します。
* **[!UICONTROL Description]：**&#x200B;この宛先に関する説明を指定します。
* **[!UICONTROL Type]：**（必須）目的の宛先タイプを選択します。
   * **[!UICONTROL Bulk ID]**：プラットフォーム間での同期 ID。
   * **[!UICONTROL Bulk Trait]**：特性情報を一括で複数のプラットフォームに送信します。
   * **[!UICONTROL Bulk Segment]**：セグメント情報を一括で複数のプラットフォームに送信します。
   * **[!UICONTROL S2S]**：サーバー間宛先を使用して、リアルタイムデータとバッチデータを複数のプラットフォームに送信します。
* **[!UICONTROL Auto-Fill Destination Mapping]：**（[!UICONTROL S2S] のみ）オプションを選択します。
   * **[!UICONTROL Segment ID]：**&#x200B;この設定を選択した場合、宛先の値のマッピングとして [!DNL Audience Manager] のセグメント ID が入力されます。
   * **[!UICONTROL Integration Code Value]：**&#x200B;この設定を選択した場合、宛先の値のマッピングとして [!DNL Audience Manager] の統合コードが入力されます。
* **[!UICONTROL User ID Key]：**（必須）この宛先で使用するユーザー ID キーをドロップダウンリストから選択します。

この ID はマスターデータソース ID として使用します。 これにより、ファイルに送信されるユーザー ID が決定されます。

>[!NOTE]
>
>[!UICONTROL Bulk ID] 宛先タイプの場合、[!DNL Audience Manager]、[!UICONTROL User ID]、または [!DNL Adobe Experience Cloud] ID を使用することはできません。

データソース ID（[!UICONTROL DPID]）がドロップダウンリストに表示されない場合、[データソースの設定](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/manage-datasources.html?lang=ja)ページで、データソースレベルの「**[!UICONTROL Outbound]**」チェックボックスをオンにする必要があります。

* **[!UICONTROL Target Data Source]：**（必須）この宛先で使用するデータソースをドロップダウンリストから選択します。 この設定により、送信データのラベル付けができるようになり、クライアント側で別々のシステムへの取り込みが可能になります。
* **[!UICONTROL Foreign Account ID]：**&#x200B;この宛先で使用する外部アカウント ID を指定します。 これは、受信者側のシステムでこの送信データの識別値となります。
* **[!UICONTROL Outbound Sample Rate Denominator]：**&#x200B;返されるデータの総量が不明な場合、この設定を使用して、全量ではなく、サンプル量のデータのみを返すようにします。 この数値を調整して、データの比率を指定します（例えば、100 と指定すると標準のデータ量の 100 分の 1 が返され、10 と指定すると標準のデータ量の 10 分の 1 が返されます）。 デフォルト値は 1 です。この場合、すべてのデータが返されます。

## リアルタイムデータ（S2S の宛先の場合） {#realtime-s2s}

[!UICONTROL S2S] の宛先を作成する場合、以下の各フィールドに入力します。

**[!UICONTROL Servers]**：この宛先で使用する `HTTP` サーバーを選択します。
**[!UICONTROL Format]**：この宛先で使用する形式を [!UICONTROL HTTP only] ドロップダウンリストから選択します。

>[!NOTE]
>
>[!DNL S2S] の場合に限り、画面上の「Off」／「On」スライダーを使用して、「[!UICONTROL Realtime]」と「[!UICONTROL Batch]」のいずれかの宛先を有効にできます。 両方のオプションを無効にすることはできません。

## バッチデータ {#batch-data}

[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]、または [!UICONTROL Bulk Segment] の宛先の場合は、以下のフィールドを入力します。

* **[!UICONTROL Protocol]**：（必須）この宛先で使用するプロトコルをドロップダウンリストから選択します。
   * **[!UICONTROL FTP]**
   * **[!UICONTROL HTTP]**
   * **[!UICONTROL S3]**
* **[!UICONTROL Servers]**：（必須）この宛先で使用するサーバーをドロップダウンリストから選択します。
* **[!UICONTROL Format]**：（必須）この宛先で使用する形式をドロップダウンリストから選択します。形式は上で選択したプロトコルによって、[!DNL HTTP] 形式またはファイル形式のいずれかとなります。
* **[!UICONTROL Sync Type]**：（必須）この宛先で使用する同期タイプを選択します。 これは、クライアントが送信オーダーに含めるユーザーアクティビティのレベルを表します。 クライアントがプロパティからセグメントの選定のみを行う場合は、「**[!UICONTROL Customer]**」を選択します。 すべての **[!UICONTROL Platform]** ユーザーにまたがるオフサイトアクティビティからセグメントの選定を含める場合は、「[!DNL Audience Manager]」を選択します。
* **[!UICONTROL Customer]**：選択した期間について、クライアントのプロパティのみで（クライアントの [!UICONTROL PID] に関連付けられている）特性認識が少なくとも 1 件あるアクティブユーザーがファイルに含まれます。 *リアルタイム*&#x200B;のセグメントの選定を宛先に送信する場合、クライアントはこのオプションを使用する必要があります。
* **[!UICONTROL Platform]**：選択した期間について、すべての [!DNL Audience Manager] クライアントのプロパティの任意の箇所で（すべてのクライアント PID に関連付けられている）リアルタイムインタラクションが、ID 同期か特性認識かを問わず、少なくとも 1 件あるアクティブユーザーがファイルに含まれます。 *すべての*&#x200B;セグメントの選定を宛先に送信する場合、クライアントはこのオプションを使用する必要があります。
* **[!UICONTROL Lifetime]**：宛先が作成された後の、すべての [!DNL Audience Manager] クライアントプロパティの任意の箇所で見られるアクティブユーザーがファイルに含まれます。
* **[!UICONTROL Sync Type Lookback Period]**：「[!UICONTROL Customer]」または「[!UICONTROL Platform]」を選択した場合は、期間を選択します。 ファイルには選択した期間のアクティブユーザーが含まれます。
次に、オーダータイプを選択します。 これは、パートナーとの各送信統合の頻度と範囲を表します。 差分オーダーと完全オーダーのいずれかを選択します。
* **[!UICONTROL Incremental Scheduled Run]**：実行するたびに、[!DNL Audience Manager] は前回の送信オーダー以降に認定された新しいユーザーのみを送信します。 [!DNL Audience Manager] で差分同期処理を実行する間隔を選択します。 例えば、24 時間ごと、7 日ごと、30 日ごとを選択できます。また、実行しないようにすることもできます。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>最初の差分オーダーでは、それより前に宛先に送信されたユーザーがいないので、完全オーダーと同じになります。

* **[!UICONTROL Full Sync Scheduled Run]**：実行するたびに、[!DNL Audience Manager] は宛先が最初に設定された時点より後のすべてのアクティブユーザーを送信します。 [!DNL Audience Manager] が完全同期処理の実行に使用するスケジュールを選択します。 例えば、24 時間ごと、7 日ごと、30 日ごとを選択できます。また、実行しないようにすることもできます。

<!--
I removed {importance="high"} from note for Exp League rendering. -Bob
-->

>[!NOTE]
>
>完全同期より差分同期の方をより頻繁に使用することをお勧めします。 差分同期では、新しい特性認識または ID の同期を含むファイルしか送信されません。 完全同期では、新しい認識や ID の同期の有無にかかわらず、すべてのファイルが送信されます。 [!UICONTROL Full Sync Scheduled Run] 設定の使用は、クライアントが送信データ量を抑えるためにすべてのユーザーの完全コピーを必要とする場合のみにしてください。

## データソースの設定 {#configure-data-sources}

[!UICONTROL Bulk ID]、[!UICONTROL Bulk Trait]、または [!UICONTROL Bulk Segment] の宛先の場合は、以下のフィールドを入力します。 これらの設定により、データソースに関連付けられているすべてのデータ（選択したタイプにより、特性、セグメント、ID のいずれか）を送信できます。

* **[!UICONTROL All Unrestricted First Party Data]**：すべてのファーストパーティデータソースを使用する場合に選択します。 このオプションを選択すると、「[!UICONTROL Available Data Sources]」の各オプションは無効になります。
* **[!UICONTROL Available Data Sources]**：矢印を使用して、データソースを「**[!UICONTROL Available Data Sources]**」ボックスと「**[!UICONTROL In File Data Sources]**」ボックスの間で移動します。

## 保存とファイナライズ {#save-and-finalize}

すべての必須フィールドに入力すると、「**[!UICONTROL Save]**」がアクティブ化されます。 「**[!UICONTROL Save]**」をクリックすると、宛先の作成処理がファイナライズされます。

## 会社宛先の削除 {#delete-company-destinations}

<!-- delete-company-destinations.xml -->

宛先を削除するには：

1. 「**[!UICONTROL Companies]**」をクリックし、目的の会社を特定してからクリックして、その後「**[!UICONTROL Destinations]**」タブをクリックします。
1. 目的の宛先の「![](assets/icon_delete.png)」列で「**[!UICONTROL Actions]**」をクリックします。
1. 「**[!UICONTROL OK]**」をクリックして削除を確定します。

>[!NOTE]
>
>宛先にセグメントがマッピングされている場合、その宛先は削除できません。
