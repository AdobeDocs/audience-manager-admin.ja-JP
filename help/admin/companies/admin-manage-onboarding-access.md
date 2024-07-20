---
description: 他のパートナーや顧客が所有するターゲットデータソースへのファイルやデータの誤ったオンボーディングを防ぐため、Audience Manager では、パートナー ID（PID）と他のパートナーが所有するデータソースとのマッピング要件を追加しました。
title: セカンドパーティデータのオンボーディングアクセスの管理
exl-id: 03bec978-dd31-41cc-a3aa-d67fbb98963c
source-git-commit: cc04863272005964cfbf1bb2319cc0dd86863680
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 100%

---

# セカンドパーティデータのオンボーディングアクセスの管理 {#manage-onboarding-access-for-second-party-data}

>[!IMPORTANT]
>
> このページのオーディエンスは、アドビ社内の従業員です。Audience Manager のお客様で、このページに記載されているようなセカンドパーティのデータソースマッピングをリクエストされる場合は、カスタマーケアまたはテクニカルアカウントマネージャーにお問い合わせください。
> 既存のデータ共有関係については、マッピングをリクエストする必要はありません。また、PID に属するターゲットデータソースにデータをオンボードする場合も、マッピングは必要ありません。

他のパートナーが所有するターゲットデータソースに、誤ってファイルやデータをオンボーディングしてしまうのを防ぐために、Audience Manager では、他のパートナーが所有するパートナー ID（PID）とデータソース（DPID）の間にマッピング要件を追加しました。詳しくは、[Audience Manager ID のインデックス](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=ja)の PID および DPID を参照してください。

セカンドパーティのデータ共有の目的で、Audience Manager のパートナーまたはお客様が、所有していないターゲットデータソースにファイルを取り込む場合、自社のパートナー ID（PID）とその特定のデータソース（DPID）の間のマッピングをリクエストする必要があります。マッピングがない場合、ファイルは受信データジョブで処理されず、データは Audience Manager に転送されません。

そのマッピングを作成するには、Jira チケットを Audience Manager エンジニアリングチームに送信します。Jira チケットのサンプルは[ここ](https://jira.corp.adobe.com/browse/AAM-60353)で表示できます。既存のデータ共有関係に対してマッピング作成をリクエストする必要はありません。
