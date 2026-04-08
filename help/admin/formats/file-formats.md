---
description: FTP ベースのデータファイルの作成に使用できるマクロのリストを表示します。 一部のマクロは、データファイルのすべてのフィールドと行に使用できます。 その他のマクロは、ヘッダーとデータ行にしか使用できません。
seo-description: Lists the macros you can use to create FTP-based data files. Some macros can be used for all data file fields and rows. Other macros are specific to header and data rows only.
seo-title: File Format Macros
title: ファイル形式マクロ
uuid: f91c91b6-6581-4ed7-8d7f-f8532bd41df9
exl-id: e686bc33-da3e-49a9-8c71-2bc6ca399bfb
TQID: https://experienceleague.adobe.com/ATzqYmfRIVDeQ3DZpbcZkCP4Jjsapw9Nfyli1QFR8-o
product_v2:
  - id: df80eeb1-8d72-467e-b0df-9d51c7d3a0a1
source-git-commit: d2bed13a6ac7d38ae79b65d492b6de0ca6b6d488
workflow-type: tm+mt
source-wordcount: 686
ht-degree: 100%

---

# ファイル形式マクロ {#file-format-macros}

[!DNL FTP] ベースのデータファイルの作成に使用できるマクロのリストを表示します。 一部のマクロは、データファイルのすべてのフィールドと行に使用できます。 その他のマクロは、ヘッダーとデータ行にしか使用できません。

## 一般的なマクロ {#common-macros}

これらのマクロはどの形式フィールドでも使用できます。 例については、 [File Format Macro Examplesを参照してください](../formats/file-format-examples.md)。

<table id="table_A3309E175ABF4651BD11CE3632B3C553"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> マクロ </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>ASCII_SOH</code> </p> </td> 
   <td colname="col2"> <p>非表示の ASCII 文字。 コンテンツの行またはセクションの開始を表します。 ファイル内のデータ列を区切る場合にも使用できます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPID</code> </p> </td> 
   <td colname="col2"> <p>ターゲットデータプロバイダー ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MASTER_DPID</code> </p> </td> 
   <td colname="col2"> <p>ユーザー ID キーデータプロバイダー ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>ORDER_ID</code> </p> </td> 
   <td colname="col2"> <p>オーダー／宛先 ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PIDALIAS</code> </p> </td> 
   <td colname="col2"> <p>オーダー／宛先 ID のエイリアス。 </p> <p>このエイリアスの値は、宛先の「<span class="wintitle">Foreign Account ID</span>」フィールド（「<span class="wintitle">Basic Settings</span>」セクション内）で設定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_MODE</code> </p> </td> 
   <td colname="col2"> <p>同期タイプを表します。 次のオプションの変数を使用できます。 </p> 
    <ul id="ul_87E8E3CE6565447A9810B5119298CC7B"> 
     <li id="li_66F4889FB84E40AC92F69F3FF6B0042C"> <code>full</code>：完全同期。 </li> 
     <li id="li_BFE2C2D9A33A44FB9A840A7232ECCFFF"> <code>iter</code>：増分同期。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SYNC_TYPE</code> </p> </td> 
   <td colname="col2"> <p>データ転送方式を表します。 次のオプションの変数を使用できます。 </p> 
    <ul id="ul_13BE35BBBF7C4C67AEFC514C5D192902"> 
     <li id="li_195FE9B4C5494600BD17D7172A8FB630"> <code>ftp</code> </li> 
     <li id="li_751AD59C4C934D66BC530D9806B500AF"> <code>http</code> </li> 
     <li id="li_4638AF7D1FB54E2C890045048B85309C"> <code>s3</code> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TIMESTAMP</code> </p> </td> 
   <td colname="col2"> <p>10 桁の UTC を示す Unix タイムスタンプ。 </p> <p>Java の日付／タイムスタンプ形式ルールに従って <code>YYYYMMDDhhmmss</code> という形式にすることもできます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ヘッダーフィールドマクロ {#header-field-macros}

ヘッダーフィールドのみで使用されるマクロ。 例については、 [File Format Macro Examplesを参照してください](../formats/file-format-examples.md)。

<table id="table_1A8BD1750F4940B3A34E3F80371A447A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> マクロ </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>このマクロはフィールド間の区切り記号としてタブを挿入します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## データ行マクロ {#data-row-macros}

データ行でのみ使用するマクロ。 例については、 [File Format Macro Examplesを参照してください](../formats/file-format-examples.md)。

<table id="table_E378F94A3907407AA8110C8EE6C10909"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> マクロ </th> 
   <th colname="col2" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>CLOSE_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>閉じ中括弧（<code>}</code>）を挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>COMMA</code> </p> </td> 
   <td colname="col2"> <p>コンマを挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="term"> データパートナー一意のユーザー ID</span>。 ユーザー／サイト訪問者に割り当てた ID が <span class="keyword">Audience Manager</span> デバイス ID と既に同期されている場合、その ID を返します。 </p> <p>DPID が 0 の場合、このマクロはユーザーの ID ではなく <span class="keyword">Audience Manager</span> ID を返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DP_UUID_LIST</code> </p> </td> 
   <td colname="col2"> <p>1 件のデータパートナーに対する複数の ID が含まれるリストを返します。 複数の下位部門や、その他の組織グループがある大規模な組織でデータ共有が可能な場合に便利です。 このマクロは、これらの下位グループの ID のリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>DPUUIDS</code> </p> </td> 
   <td colname="col2"> <p>このマクロの出力では、データプロバイダー ID（DPID）が関連する一意のユーザー ID（DPUUID）にマッピングされます。 このマクロには、出力を制御するための書式設定文字列が必要です。 出力例として次のようなものが挙げられます。 </p> <p> <code>"dpids=dpid1,dpid2,...dpid n|maxMappings= n|format=json"</code> </p> <p><code>maxMappings</code> 設定により、マクロが返すマッピングの数が決定されます。 <code>maxMappings=0</code> の場合、このマクロは指定された各 DPID のすべてのマッピングを返します。 データはタイムスタンプを基準に並べ替えられ（最新のものが最初となります）、最も値が大きいタイムスタンプの結果が最初に返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>endif</code> </p> </td> 
   <td colname="col2"> <p>条件付き <code>if</code> と <code>SEGMENT_LIST</code> および <code>REMOVED_SEGMENT_LIST</code> マクロを使用する場合に必要です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>if(SEGMENT_LIST &amp;&amp; REMOVED_SEGMENT_LIST)endif</code> </p> </td> 
   <td colname="col2"> <p>マクロを組み合わせると、ユーザーが属し、<i>かつ</i>ユーザーが削除されたセグメントのリストを表示する条件文が作成されます。 いずれかの条件が満たされない場合、またはデータがない場合、空の文字列が返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>MCID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Adobe Experience Cloud</span> ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPEN_CURLY_BRACKET</code> </p> </td> 
   <td colname="col2"> <p>開き波括弧（<code>{</code>）を挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OPT_OUT</code> </p> </td> 
   <td colname="col2"> <p>廃止されました。 使用しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_TYPE</code> </p> </td> 
   <td colname="col2"> <p>廃止されました。 使用しないでください。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>OUTPUT_ATTRIBUTE_VALUE</code> </p> </td> 
   <td colname="col2"> <p><code>1</code> を静的な、ハードコーディングされた値として返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>PID</code> </p> </td> 
   <td colname="col2"> <p>パートナー ID（PID）。 PID は Admin UI の「<span class="wintitle">Profile</span>」タブに表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>REMOVED_SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>削除されたセグメントがあれば、そのリストを返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SEGMENT_LIST</code> </p> </td> 
   <td colname="col2"> <p>セグメントのリストを返します。 次のオプションの変数を使用できます。 </p> 
    <ul id="ul_B111AA0D6C18445598A1444B8B7E9325"> 
     <li id="li_8603B40229624856AF1FBC434DB8F16A"> <code>segmentId</code>：レガシー ID。 廃止されました。 <code>sid</code>（小文字のみ）を使用します。 </li> 
     <li id="li_1EF40DDCA3C5447586904CF021D8F912"> <code>csegid</code>：レガシー ID。 廃止されました。 <code>sid</code>（小文字のみ）を使用します。 </li> 
     <li id="li_D85F0A5D16AE4DAFB55C17DBB35EA66E"> <code>sid</code>：セグメント ID。 </li> 
     <li id="li_9BE103EFD8384464B46FAC00422431DB"> <code>type</code>：<code>5</code> を静的なハードコーディングされた値として返します。これはデータをセグメントデータとして識別する値です。 </li> 
     <li id="li_FE5049089F2944FA9DB9F9D546DBA167"> <code>alias</code>：セグメントのマッピング。 廃止されました。 <code>sid</code>（小文字のみ）を使用します。 </li> 
     <li id="li_DD778AA2D1DB4D409CF5026B5D9DBD27"> <code>lastUpdateTime</code>：セグメントが最後に認識された時点を示す Unix タイムスタンプ。 </li> 
    </ul> <p>この変数は、マクロの後に配置して波括弧で囲みます。 例えば、<code>&lt;SEGMENT_LIST:{seg|&lt;seg.type&gt;,&lt;seg.sid&gt;}; separator="|"&gt;</code> のように、このコードは結果をパイプ（ | ）で区切ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>SET_ATTRIBUTES</code> </p> </td> 
   <td colname="col2"> <p><code>1</code> を静的な、ハードコーディングされた値として返します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TAB</code> </p> </td> 
   <td colname="col2"> <p>区切り記号としてタブを挿入します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>TRAIT_LIST</code> </p> </td> 
   <td colname="col2"> <p>特性のリストを返します。 次のオプションの引数を使用できます。 </p> 
    <ul id="ul_757DEB56E4F849768468F3C166B0D171"> 
     <li id="li_859E1F4F21D645519F150DC512B3EB1A"> <code>type</code>：数値 ID で識別される特性タイプ。 この変数は次の値を返します。 
      <ul id="ul_C9839266783D42CCADAAC3FEA33BE4D7"> 
       <li id="li_6996A218E3F04EC3BC70032559DD87FC"> <code>10</code>：DPM 特性（オフライン、インバウンドジョブで転送されたジョブ）を表します。 </li> 
       <li id="li_831FF929BF50434C8804C13E5786DF79"> <code>3</code>：ルールベースの特性（リアルタイム、<span class="wintitle">DCS</span> から転送）を表します。 </li> 
      </ul> </li> 
     <li id="li_E84D6BC80AEE4F10963C9882C4151ED4"> <code>traitId</code>：特性 ID。 </li> 
     <li id="li_D30A849BA35248E6B9110FA3ADEFC332"> <code>lastRealized</code>：特性が最後に認識された時点。 Unix タイムスタンプ。 </li> 
    </ul> <p>この変数は、マクロの後に配置して波括弧で囲みます。 例えば、<code>TRAIT_LIST{type|traitId};separator="|"</code> のように、このコードは結果をパイプ（ | ）で区切ります。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>UUID</code> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> ユーザー ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>
