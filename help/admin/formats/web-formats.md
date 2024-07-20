---
description: HTTP データファイルの作成に使用できるマクロのリストを表示します。HTTP はデータを JSON 形式で送信します。
seo-description: Lists the macros you can use to create HTTP data files. HTTP sends data in a JSON format.
seo-title: HTTP Format Macros
title: HTTP 形式マクロ
uuid: 91021f60-75d0-4b1d-86ca-91c9dadafac1
exl-id: 80ed24ac-1b84-4c1b-966f-039b587ea899
source-git-commit: cfc3396843592d80b017471a0e88cf335a5f81e0
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 100%

---

# HTTP 形式マクロ {#http-format-macros}

[!DNL HTTP] データファイルの作成に使用できるマクロのリストを表示します。[!DNL HTTP] はデータを [!DNL JSON] 形式で送信します。

[HTTP 形式マクロの例](../formats/web-format-examples.md)で、一般的に使用されるマクロの組み合わせのリストと例を参照してください。

<table id="table_72A72EA63C3643FB84B47A76CD2CC1CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> マクロ </th> 
   <th colname="col2" class="entry"> メソッドのタイプ </th> 
   <th colname="col3" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>AAM_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p> <span class="keyword">Audience Manager</span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>データパートナーの一意のユーザー ID。このマクロは、ユーザーに割り当てた ID が <span class="keyword">Audience Manager</span> デバイス ID と既に同期されている場合、その ID を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>データプロバイダー ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ECID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>データプロバイダー ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>GENERATION_TIME</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>Unix UTC タイムスタンプ。<span class="wintitle">S2S </span>宛先をパートナーに公開するよう AAM が通知を受けた時間を表す内部タイムスタンプ。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>IP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーの IP アドレス。 </p> </td> 
  </tr>
    <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>Experience Cloud ID.（MCID は、Experience Cloud のレガシー名である Marketing Cloud を表します） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーが属していないセグメントの数（整数）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>NUM_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーが属しているセグメントの数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>オーダー／宛先 ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID_ALIAS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET, POST</code> </p> </td> 
   <td colname="col3"> <p>パートナー ID のエイリアス。外部アカウント ID とも呼ばれます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>RANDOM</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>乱数を生成します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REGION_ID_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>アクティビティが開始される <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/api-and-sdk-code/dcs/dcs-api-reference/dcs-regions.html?lang=ja">Audience Manager DCS 領域</a>。</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーが認定されないセグメントがある場合、そのセグメントの ID のリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーが認定されないセグメントのリスト。以下のような特定のセグメントフィールドを返すこともできます。 </p> <p> 
     <ul id="ul_29B83093A7624A908F0C06F2A248981A"> 
      <li id="li_57A60A54F5D44E38ACB4E2648095F246"> <code>traitAlias</code> </li> 
      <li id="li_4079F646493F40DBA0CE75D662A69454"> <code>legacySegmentId (formerly segmentId)</code> </li> 
      <li id="li_D3509A2D379E4C1FB3BC1B5E7D45A916"> <code>newSegmentId</code> </li> 
      <li id="li_EA901C20EEEB4CFAA39A5E0E822D2394"> <code>status</code> </li> 
      <li id="li_6310E21F88CC4691980DD3C9D551409F"> <code>dateTime</code> </li> 
     </ul> </p> <p>以下の例のように、これらのフィールドを配列で指定します。 </p> <p> <code>[&lt;REMOVED_SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapping":&lt;seg.traitAlias&gt;,"Status:"&lt;seg.status&gt;, "Time":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&gt;&lt;CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p><a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31">HTTP 形式マクロの例</a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> ユーザーが認定されなくなったセグメントの最後の認識に関するリスト。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーが認定されなくなったセグメントのエイリアス名のリスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>セグメント ID のリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENTS</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>ユーザーが認定されているセグメントのリスト。以下のような特定のセグメントフィールドを返すこともできます。 </p> <p> 
     <ul id="ul_9209683A8E0A4B8081E5EFA4602F743F"> 
      <li id="li_D796526C1C9E45BEA891D619539888C4"> <code>traitAlias</code> </li> 
      <li id="li_BF12E010E1AD432C84605B9817F209DD"> <code>legacySegmentId (formerly segmentId)</code> </li> 
      <li id="li_4A81E3B715254549B9EADB983A2FC32B"> <code>newSegmentId</code> </li> 
      <li id="li_1F01A60829DF4C87879D94299E1D589C"> <code>status</code> </li> 
      <li id="li_E52F10CD5A04487D81A4B1750B0DC4E3"> <code>dateTime</code> </li> 
     </ul> </p> <p>以下の例のように、これらのフィールドを配列で指定します。 </p> <p> <code>[&lt;SEGMENTS:{seg|&lt;OPEN_BRACKET&gt;"Mapping":&lt;seg.traitAlias&gt;,"Status:"&lt;seg.status&gt;, "Time":&lt;seg.dateTime&gt;,"LegacySegmentId":&lt;seg.LegacySegmentId&gt;, "NewSegmentId":&lt;seg.NewSegmentId&gt;&lt;CLOSE_BRACKET&gt;}; "separator=","&gt;]</code> </p> <p><a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31">HTTP 形式マクロの例</a>も参照してください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIME_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>最後の認識のリスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>UNIX の UTC タイムスタンプ。セグメントの最後の認識を表します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAITALIAS_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>特定のセグメントのエイリアス名のリスト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_AGENT</code> </p> </td> 
   <td colname="col2"> <p> <code>GET</code> </p> </td> 
   <td colname="col3"> <p>初期リクエストのユーザーエージェント。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>USER_LIST</code> </p> </td> 
   <td colname="col2"> <p> <code>POST</code> </p> </td> 
   <td colname="col3"> <p><span class="keyword">Audience Manager</span> ユーザー ID のリスト。以下のような特定のフィールドを返すこともできます。 </p> 
    <ul id="ul_B6857D809FDC46749B7E745BD8C45F8E"> 
     <li id="li_F31CD82D16ED41FD82518141D90B5B35"> <code>user.aamUuid</code> </li> 
     <li id="li_623FA758C84D4A2D9B25C7FBE90F62B7"> <code>user.dpUuid</code> </li> 
     <li id="li_976B941908EB494EB476B5FB68B8972D"> <code>user.segments</code> </li> 
     <li id="li_D7E129833D1E4D59A554FFCE353924EE"> <code>user.removedSegments</code> </li> 
     <li id="li_8B3DD69D3FE3493492FC9F162812FCD5"> <code>user.userAgent</code> </li> 
     <li id="li_8C7EA05585A64141876DF169C31322FE"> <code>user.ip</code> </li> 
     <li id="li_678076A31A7743C480F718C9E7A07E99"> <code>user.dpuuids</code> </li> 
     <li id="li_B598A5AED28C4304972E51DBD4E480D8"> <code>user.timestamp</code> </li> 
     <li id="li_8424D540282F449CA5AF6B3CC343DDCB"> <code>user.random</code> </li>
     <li><code>user.regionIds</code></li> 
    </ul> <p>これらのフィールドは以下の例のように指定します。 </p> <p> 
     <codeblock>
       "AAM_UUID": "&lt;user.aamUuid&gt;" 
"DataPartner_UUID": "&lt;user.dpUuid&gt;" 
     </codeblock> </p> <p>完全な例については、<a href="../formats/web-format-examples.md#reference_98828E32B0964FF9AAC7C5400E88BA31">HTTP 形式マクロの例</a>を参照してください。 </p> </td> 
  </tr>
 </tbody>
</table>
