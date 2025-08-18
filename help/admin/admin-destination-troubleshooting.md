---
description: Audience Manager での宛先の設定と一般的な問題の解決に関する情報。
seo-description: Information to help you set up destinations in Audience Manager and avoid common problems.
seo-title: Destination Setup Troubleshooting
title: 宛先の設定に関するトラブルシューティング
uuid: 04080fb9-6c7b-4de7-960e-54482be2de83
exl-id: 53c72b1a-f1a1-4266-a595-e4821c2640b2
source-git-commit: c7c5da62b32f6a56152e1c09a965facfc601cade
workflow-type: tm+mt
source-wordcount: '1300'
ht-degree: 96%

---

# 宛先の設定に関するトラブルシューティング {#destination-setup-troubleshooting}

Audience Manager での宛先の設定と一般的な問題の解決に関する情報。

## 宛先を設定しましたが、ファイルが表示されません。どこにありますか？   {#destination-no-files}

<!-- c_dest_tshooting.xml -->

宛先の設定に関する一般的な問題として、次のようなものがあります。

### 宛先の設定が誤っている

* **[!UICONTROL UserID] キーが誤っている：**&#x200B;[!UICONTROL UserID] キーは、この宛先の [!UICONTROL MasterDPID] で、送信される ID 値の基礎となります。[!UICONTROL UserID] キーはドロップダウンリストから選択できますが、この値にマッピングされている ID、特徴、セグメントがあるとは限りません。[!UICONTROL Outbound] プロセス（宛先の作成後に実行）でこの [!UICONTROL UserID] キーにマッピングされているユーザーが見つからない場合、データは送信されません。
* **ファイル内データソースが選択されていない：**&#x200B;[!UICONTROL S2S] 以外の宛先タイプを選択すると、画面の最下部に「[!UICONTROL Configure Data Sources]」というラベルのセクションが表示されます。このセクションが最初に表示される際には、値が選択されていません。「[!UICONTROL All First Party]」チェックボックスをクリックせず、[!UICONTROL Available Data Sources] ウィンドウでデータソースを個別に選択していない場合、データは送信されません。

### 形式の設定が誤っている

送信データの形式を選択する場合は、できれば既存の形式を再利用するのが最善です。実績のある形式を使用すると、発信データを正常に生成できます。既存の形式がどのようにフォーマットされているかを正確に確認するには、メニューバーの「[!UICONTROL Formats]」オプションをクリックして、名前または ID 番号を使用して形式を検索します。形式、または形式で使用されているマクロが正しく設定されていない場合、出力が正しくフォーマットされなくなるか、情報が完全には出力されなくなります。

形式の設定とマクロの使用について詳しくは、[ ファイル形式マクロ ](formats/file-formats.md#) および [HTTP 形式マクロ ](formats/web-formats.md) を参照してください。

### サーバーの設定が誤っている

* **[!DNL FTP]**
   * **[!UICONTROL Domain]**
      * ホスト名の接頭辞は入力しません。アカウントが [!DNL ftp://hello.com] の場合、このフィールドには [!DNL hello.com] とだけ入力します。
   * **[!UICONTROL Port/Type Combination]**
      * [!DNL FTP] 転送の場合、推奨される転送タイプは [!DNL SFTP] です。
      * [!DNL SFTP] タイプを選択すると、ポートはほぼすべての場合で 22 となります。
      * [!DNL FTPs/TLS] タイプを選択すると、ポートはほぼすべての場合で 21 となります。
      * [!DNL FTPs/TLS] タイプは通常の [!DNL FTP] 転送とは異なります。通常の（セキュリティで保護されていない）[!DNL FTP] 転送はサポートされていません。
   * **[!UICONTROL Remote Path]**
      * リモートサブパスを選択する場合、先頭にスラッシュを入力しないようにする必要があります。
      * 転送したファイルを [!DNL (root)/inbound] サブフォルダーに配置する場合、リモートパスには [!DNL /inbound] ではなく [!DNL inbound] を追加します。
      * パス上で複数階層下のディレクトリにあるファイルを送信する場合、各ディレクトリの間にスラッシュを入力します。[!DNL /inbound/subdirectory1/subdirectory2] の場所を指定する場合は、 このフィールドに「[!DNL inbound/subdirectory1/subdirectory2]」と入力してください。
      * このファイルを配置する場所が、外部サーバーにより自動的にルーティングされるディレクトリである場合は、このフィールドを空白にします。ピリオド（.）やスラッシュ（/）も含め、何も入力しないでください。

* **[!DNL S3]**
   * [!DNL S3] は（[!DNL FTP] や [!DNL HTTP] より）推奨される転送プロトコルです。
      * **[!UICONTROL Bucket]**
         * グループ名にはスラッシュ、接頭辞、サフィックスなどを付けません。アドレスが [!DNL s3://your-bucket] の場合、このフィールドには [!DNL your-bucket] と入力します。
      * **[!UICONTROL Directory]**
         * データを配置するサブディレクトリが指定されていない場合は、このフィールドを空白にします。アドレスが [!DNL s3://your-bucket/your-subdirectory] の場合、「[!DNL your-bucket]」フィールドには [!UICONTROL Bucket] と入力し、「[!DNL your-subdirectory]」フィールドには [!UICONTROL Directory] と入力します。先頭にはスラッシュを追加しないでください。
         * パス上で複数階層下のディレクトリを参照する場合のみ、スラッシュを区切り記号として使用します。場所が [!DNL s3://your-bucket/your-subdirectory1/your-subdirectory2] の場合、「[!DNL your-bucket]」フィールドには [!UICONTROL Bucket]、「[!DNL your-subdirectory1/your-subdirectory2]」フィールドには [!UICONTROL Directory] と入力します。
      * **[!UICONTROL Access / Secret Keys]**
         * [!DNL TechOps] がグループを作成し、コンサルタントに対してアクセス権／秘密鍵を設定すると、これらの資格情報は通常 `READ-ONLY` で、クライアントに渡されます。これらの資格情報は「[!UICONTROL Access / Secret Key]」フィールドには入力しないでください。入力すると転送が失敗します（これらの資格情報は読み取り専用で、書き込み可能ではないため）。[!DNL TechOps] がグループを作成し資格情報を設定する場合、コンサルタントはこのグループにファイルを書き込むための Adobe キーペア（クライアントには渡しません）も要求する必要があります。このキーはこれらのフィールドに入力する必要があります。

* **[!DNL HTTP]**
   * **[!UICONTROL Domain]**
      * [!DNL HTTP] エントリには接頭辞情報を入力しないでください。アカウントが [!DNL https://superduper.com] の場合、このフィールドには [!DNL https://superduper.com] と入力します。
      * **[!UICONTROL URL Prefix]**
         * [!DNL URL] 接頭辞を追加する場合、先頭のスラッシュは付けません。[!DNL https://hello.com/r/x/y/z] の住所には、[!UICONTROL Domain] フィールドで入力した [!DNL https://hello.com] と、[!UICONTROL URL Prefix] フィールドでここに入力した [!DNL r/x/y/z] があります。
         * [!UICONTROL URL Prefix] が必要でない場合、この値は空白にします。
      * **[!UICONTROL Authentication - SSH Key]**
         * 完全な `SSH PRIVATE` キーの値（ヘッダー、フッター、改行を含む）をこのボックスに入力し、暗号化やキーストレージが正確になるようにします。

### 送信生成の時間が足りない

アウトバウンディングプロセスは 1 日に 2 回実行されます。ファイルが最終的な宛先にプッシュされる前に、複数のプロセス（アウトバウンディング、公開、外部ロケーションへのプッシュなど）を実行する必要があります。 データを外部の場所にプッシュする予定の 24 時間以上前に宛先を完全に設定しておくことを推奨します。

### ファイルの分割サイズが大きすぎます

ファイルを宛先に出力する場合、大きい送信ファイルをファイルチャンクに分割できます。個々のファイルチャンクが 10GB を超えないようにしてください。[送信データファイル名：構文と例](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/receiving-audience-data/batch-outbound-data-transfers/outbound-file-name-contents.html?lang=ja)も参照してください。


## Experience Cloud ID、顧客 ID、Audience Manager ID を送信データファイルにエクスポートするための宛先を設定する方法 {#set-up-destinations-export}

このページでは、[!UICONTROL Outbound Data Files] で必要な ID タイプをキーとするデータを書き出すための宛先を設定する方法を説明します。

<!-- set-up-destinations-mcid-aamid.xml -->

ユーザーは宛先の設定により、自分のデータを任意の数のデジタルチャネルにわたって有効にすることができます。例えば、オーディエンスデータを別の ソリューション（[!DNL Adobe Experience Cloud]、[!DNL Target]、[!DNL Campaign] など）にエクスポートできます。または、[!UICONTROL DSP]、[!UICONTROL SSP]、および Audience Manager と統合されている任意のプラットフォームにデータを送信できます。提携パートナーのリストは [Integrations Wiki ページ](https://wiki.corp.adobe.com/display/MCPI)にあります。

>[!NOTE]
>
>Admin UI での宛先の作成に関する詳細なチュートリアルについては、「[会社の宛先を作成または編集](companies/admin-manage-company-destinations.md#create-edit-company-destinations)」の記事を参照してください。

ユーザーは宛先ごとに別の ID タイプをエクスポートします。以下の図は、各 ID タイプに関連するプロファイル情報をエクスポートするために選択するオプションを示しています。さらに、[Audience Manager の ID のインデックス](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html?lang=ja)も参照することをお勧めします。ここで重要な設定として「[!UICONTROL User ID Key]」、「[!UICONTROL Data Source Type]」、「[!UICONTROL Format]」の 3 つがあります。以下に詳細を示します。

* [!UICONTROL User ID Key]をインストールします。[!UICONTROL Admin UI] で、**[!UICONTROL Companies]** に進みます。顧客の会社を検索し、クリックします。「**[!UICONTROL Destinations]**」タブを探して「**[!UICONTROL Add Destination]**」を押します。**[!UICONTROL Add Destination]** ワークフローで、[!UICONTROL User ID Key] を選択します。この [!UICONTROL User ID Key] キーにより、ターゲットデータソースからの受信 ID がフィルタリングされ、渡す ID のみが許可されます。

  ![](assets/user_id_key.PNG)

* [!UICONTROL Data Source Type]をインストールします。Audience Manager UI で宛先を作成する場合に選択します。まず、「[!UICONTROL Inbound]」を選択し、その後、目的の ID を選択します。オプションは以下のとおりです。

  ![](assets/data_source_settings.PNG)

* [!UICONTROL Format]をインストールします。このオプションでは、エクスポートする形式を決定します。「**[!UICONTROL Add Destination]**」ワークフローの「**[!UICONTROL Batch Data]**」で、形式を選択します。

形式を調べるには、**[!UICONTROL Admin UI > Formats]** に移動して、[!UICONTROL Data Row] 要素を探します。この要素には、ファイル形式（以下の例では &lt;MCID>）のマクロがあります。

![](assets/data_row.PNG)

<table id="table_DAEE5BC75DCB4FC690C4BAE41F627DEC"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> 設定番号 </th> 
   <th colname="col1" class="entry"> <p>ユーザーキー </p> </th> 
   <th colname="col2" class="entry"> <p>Data Source Type </p> </th> 
   <th colname="col3" class="entry"> <p>書式設定 </p> </th> 
   <th colname="col4" class="entry"> <p>エクスポートする ID のタイプ </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> 1 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 2 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 3 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Experience Cloud ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 4 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 5 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 6 </td> 
   <td colname="col1"> <p>Adobe Audience Manager (0) </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 7 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>顧客 ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>顧客 ID（DPUUID） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 8 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>顧客 ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 9 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>顧客 ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 10 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>&lt;DP_UUID&gt; </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 11 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>MCID </p> </td> 
   <td colname="col4"> <p>Experience Cloud ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> 12 </td> 
   <td colname="col1"> <p>DPID（会社がアクセス可能な任意のデータソース） </p> </td> 
   <td colname="col2"> <p>Audience Manager ID </p> </td> 
   <td colname="col3"> <p>UUID </p> </td> 
   <td colname="col4"> <p>Audience Manager UUID </p> </td> 
  </tr> 
 </tbody> 
</table>

## ユースケース

Audience Manager と [!DNL Campaign] を使用しているとします。顧客データを [!DNL Campaign] で処理できるようにするには、[!UICONTROL Experience Cloud IDs] をエクスポートする必要があります。ここでは、設定番号 3 を使用します。
