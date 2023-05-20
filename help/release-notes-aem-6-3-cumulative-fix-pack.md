---
title: AEM 6.3 累积修补程序包
description: AEM 6.3 累积修补程序包发行说明。
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
source-git-commit: e9031f819352f34248c6a458ef5a9101a660fbea
workflow-type: tm+mt
source-wordcount: '15909'
ht-degree: 57%

---

# AEM 6.3 累积修补程序包发行说明 {#release-notes-aem-cumulative-fix-pack}

## 发行版信息 {#release-information}

| **产品** | Adobe Experience Manager |
|---|---|
| **版本号** | 6.3 |
| **发行版本** | [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) 上的累积修补程序包 6.3.3.8 |
| **先决条件** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html) |
| **正式发布** | 2020 年 3 月 5 日 |

### 累积修补程序包 {#cumulative-fix-pack}

Adobe 引入了统一交付模式，用于发布修补程序。现在，Adobe 每月会发布一个累积修订包 (CFP)（需通过质量检查），而不是针对个别问题发布修补程序。CFP是多個修正的彙總內容套件。 CFP主要包含錯誤修正，但也可能包含Feature Pack。 比起發行個別Hotfix，這種方式的優點如下：

* 本質上為累積性質（例如，CFP包含透過舊版CFP提供的修正）
* 提升品質保證
* 簡化安裝（使用者以無相依性的單一套件安裝CFP，但最新版Service Pack除外）

有关 CFP 和其他发行版类型的更多信息，请参阅[维护版本发行方式定义](https://docs.adobe.com/content/docs/cn/aem/6-3/deploy/maintenance-release-vehicle-definitions.html)。

## 关于此发行版 {#about-the-release}

AEM 累积修补程序包 6.3.3.8 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.8 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.20。

>[!CAUTION]
>
>在没有验证已安装功能包之间的兼容性的情况下应用 CFP，可能会导致系统故障或自定义配置丢失，这些问题可能需要从备份还原才能解决。

>[!NOTE]
>
>对于版本低于 6.3.3.0 的 AEM 实例，如果客户的 AEM 实例中具有大量用户，则 Adobe 建议通过安装文件夹来部署 SP/CFP。

>[!NOTE]
>
>AEM 6.3.3.1版開始支援MongoDB Enterprise 3.6。

## 問題清單 {#changes}

此部分列出了当前 CFP 中包含的所有问题和修补程序。

此外，此 CFP 还包含[以前的累积修订包](#previous)交付的修补程序。

### 资产 {#assets}

* 向收藏集添加资产时，“添加到收藏集”页面不会在卡片视图中显示所有可用的收藏集 (NPR-32537)。

### 站点 {#sites}

* 选择一个 Parsys 及其中包含的某个组件后，如果使用键盘快捷键删除这两个选定项目，此操作会同时删除该组件及其父 Parsys (NPR-32071)。
* 保存页面属性时，会创建一个不正确的节点 (NPR-31774)。

### 集成 {#integrations}

* ReportSuitesServlet 容易遭受服务器端请求伪造 (SSRF) 攻击 (NPR-32162)。

### 营销活动定位 {#campaign-targeting}

* 在创作实例中更改并激活的组件内容在重新启动该组件之前不会显示在发布实例中 **com.day.cq.personalization.impl.TargetedContentManagerImpl**（NPR-32489 和 NPR-32232）。
* ContextHub 性能在发布时崩溃 (NPR-31170)。

### Brand Portal {#brand-portal}

* Adobe I/O 未与 Adobe Experience Manager 6.3 集成以用于 Brand Portal (NPR-32056)。

### 表单 {#forms}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

#### Forms 附加组件包 {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM Service Pack 和累积修补程序包保持一致。因此，请务必在安装任意 AEM Service Pack、累积修补程序包或功能包之后安装 AEM Forms 附加组件包。

* Designer：如果已启用标记选项，则生成的 PDF 输出文件中的子表单边框将消失（NPR-32324 和 NPR-32545）。
* Designer：如果表中存在合并的单元格，则对使用输出服务从 XDP 表单转换而来的输出 PDF 文件进行的可访问性测试将失败 (NPR-32068)。
* 文档安全：将 `DisableGlobalOfflineSynchronizationData` 选项设置为 `True` 后，无法在脱机状态下打开受保护的 PDF 文件 (NPR-32080)。

**6.3.0-0047 中修复的问题**

* （仅限 JEE）针对 Apache Log4j2 报告的严重安全漏洞（CVE-2021-44228 和 CVE-2021-45046）。

## 以前的累积修补程序包中包含的修补程序和功能包 {#previous}

### 累积修补程序包 6.3.3.7 {#cumulative-fix-pack-1}

AEM 累积修补程序包 6.3.3.7 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.7 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

### 资产 {#assets-1}

* 在从“仅限内容”下拉列表中选择筛选器选项，然后选择移动选项之前选定的资产（在触屏 UI 的列视图中）也会移动 (NPR-30693)。
* 处理工作流时，`${extension}` 变量未呈现在创作实例中 (NPR-31694)。
* 为 Dynamic Media 混合模式配置的到期时间（客户端缓存有效时间）值没有复制到 Dynamic Media 交付环境 (NPR-31114)。
* 即便使用默认筛选器后，资产也会从在 Dynamic Media - Scene7 部署上运行的创作实例复制到发布实例 (NPR-30856)。

### 站点 {#sites-1}

* 主版頁面的頁面屬性無法載入，並傳回NullPointerException。 新增cq：blueprint屬性即可解決問題(NPR-30901)。
* 未從根節點上的blueprintConfig正確擷取轉出設定。 藍圖和即時副本都會觸發停用。 應該只對藍圖觸發停用(NPR-30866)。
* 當使用者轉出頁面時，轉出設定對話方塊顯示重複的即時副本路徑(NPR-30438)。
* 現成的支架RTF編輯器(RTE)。 意外地将内嵌字体大小应用到元素（NPR-31283、NPR-30922）。
* 無法在包含現成設計匯入工具元件的Adobe促銷活動中同步促銷活動(NPR-30890)。
* 富文本编辑器 (RTE). 不允許將內嵌表格插入為清單專案(NPR-30878)。
* 如果用户的焦点位于左侧边栏字段并使用键盘快捷方式粘贴内容，则会粘贴页面编辑器剪贴板的内容，而不是从左侧边栏字段复制的内容 (NPR-31173)。
* 用户编辑内容片段时，会恢复内容片段的已删除变量 (NPR-31272)。
* AEM Site 没有创建语言副本的选项 (NPR-30690)。
* 页面编辑器的操作没有控件来转出 Live Copy (NPR-30613)。

### 社区 {#communities}

* 活动和通知标题不一致 (NPR-30940)。
* AEM製作環境中未填入Analytics報表，出現空白頁面(NPR-30905)。
* Communities部落格中的分頁功能無法正常運作(NPR-30827)。

### Foundation {#foundation}

* 基于 Jetty 的 HTTP 服务的缓冲区大小配置中的更新未保存 (NPR-30925)。

### 表单 {#forms-1}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM Service Pack 和累积修补程序包保持一致。因此，请务必在安装任意 AEM Service Pack、累积修补程序包或功能包之后安装 AEM Forms 附加组件包。

#### 自适应表单 {#adaptive-forms}

* 使用脚本计算的浮动值未正确显示在表单集的表单中 (NPR-30802)。

#### HTML5 表单 {#html-forms}

* 在添加子表单的实例时，生成 XDP 表单的 HTML5 预览时会出现闪烁 (NPR-30908)。

### Forms JEE 安装程序 {#forms-jee-installer}

#### 文档服务 {#document-services}

* 应用补丁以修复 HTML 转 PDF 的问题后，OutputService 显示错误的响应 (NPR-31504)。

#### PDFG 服务 {#pdfg-service}

* 对于 HTML2PDF 服务，不会显示 JMX 控制台的最大重复使用计数 (NPR-30305)。

#### Foundation JEE {#foundation-jee}

* 对于 HTML2PDF 服务，不会显示 JMX 控制台的最大重复使用计数 (NPR-30136)。

### 累积修补程序包 6.3.3.6 {#cumulative-fix-pack-2}

AEM 累积修补程序包 6.3.3.6 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.6 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

### 资产 {#assets-2}

* Dynamic Video的視訊彙總只傳回結果集中的前100個專案。 NPR-30441；CQ-4213561的Hotfix
* 透過DatapowerAdobe智慧標籤連線問題。 NPR-30026：适用于 CQ-4269457 的修补程序
* 封存檔的解壓縮如果檔案夾名稱具有百分比符號(%)，將無法使用Assets介面將其開啟。 NPR-29989：适用于 CQ-4270467 的修补程序
* 處理大型PDF檔案的子資產會造成OutOfMemoryError (OOME)例外狀況。 NPR-29851：适用于 CQ-4269574 的修补程序

### 站点 {#sites-2}

* AEM與Campaign整合期間出現ContextHub錯誤。 NPR-30624：适用于 CQ-4250790 的修补程序
* 如果AEM伺服器重新啟動，系統不會重新叫用資產上儲存的「onTime」或「offTime」中繼資料屬性。 NPR-30412：适用于 CQ-4272784 的修补程序
* 產生CSV匯出時，為清單檢視新增自訂欄會中斷報表。 NPR-30208：适用于 CQ-4273344 的修补程序
* /etc/reports/中的OOTB報表無法正常運作，且歷史資料圖表無法顯示。 NPR-30016：适用于 CQ-4220180 的修补程序
* resourceType要求引數的值會複製到HTML標籤屬性的值中，該屬性會以雙引號包圍。 NPR-29832：适用于 CQ-4255365 的修补程序

### 社区 {#communities-1}

* AEM Communities稽核控制檯出現重複內容問題。 NPR-30667：适用于 CQ-4276829 的修补程序

### 翻译 {#translation}

* 翻译问题 - 只有少数组件使用机器翻译进行了翻译。NPR-30079：适用于 CQ-4273764 的修补程序
* 使用翻譯架構時，將頁面新增至多個翻譯工作會觸發錯誤。 NPR-29746：适用于 CQ-4270953 的修补程序

### 表单 {#forms-2}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM Service Pack 和累积修补程序包保持一致。因此，请务必在安装任意 AEM Service Pack、累积修补程序包或功能包之后安装 AEM Forms 附加组件包。

#### HTML5 表单 {#html-forms-1}

* 在浏览模式下使用 NonVisual Desktop Access 读取 HTML5 表单时，Chrome 浏览器会读取表单设计中每个可缩放矢量图形 (SVG) 前的“图形”。NPR-30451：适用于 CQ-4274732 的修补程序

#### 表单 - 后端集成 {#forms-backend-integration}

* 建立表單資料模型(FDM)時無法檢視資料庫連線的服務/資料來源。 NPR-30108：适用于 CQ-4273359 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-1}

#### 表单 - 文档服务 {#forms-document-services}

* 對PDF服務的HTML執行負載測試時，失敗並出現錯誤，且檔案型別設定會從AEM表單伺服器中移除。 NPR-30111、NPR-30086：适用于 CQ-4271495 的修补程序

### 累积修补程序包 6.3.3.5 {#cumulative-fix-pack-3}

AEM 累积修补程序包 6.3.3.5 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.5 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.17。

### 资产 {#assets-3}

* 针对 S3 多部分支持更新了 DAM DMGateway 接口。NPR-29740：Q-4226303的Hotfix
* 無法從資產詳細資訊頁面中刪除視訊資產的影像轉譯。 NPR-29417：适用于 CQ-4268675 的修补程序
* 擁有者無法在私人資料夾中建立私人資料夾。 NPR-29397：适用于 CQ-4229830 的修补程序
* 上傳超過2 GB的Adobe Illustrator圖稿檔案會產生Java棧積空間錯誤。 NPR-29265：适用于 CQ-4226217 的修补程序
* DAM CQ Mime Type Service為m3u8套用文字後，資產變得無法使用。 NPR-29259：适用于 CQ-4264052 的修补程序
* 嘗試在Edge中建立集合時，建立選項無法運作。 NPR-29248：适用于 CQ-4265699 和 CQ-4265438 的修补程序
* 資產連結共用針對資料夾中某些資產顯示空白灰色卡片。 NPR-29831：适用于 CQ-4270187 的修补程序
* 添加到资产的新标记无法保存，且从属性中消失。适用于 CQ-4271931、CQ-4270476 的修补程序

### 站点 {#sites-3}

* 搭配多欄位使用時，CoralUI會在元件層級儲存fileReferenceParameter，而非多欄位層級。 NPR-29535：适用于 CQ-4266129 的修补程序
* 在AEM 6.3.3.3上嘗試比較最新和目前頁面版本時發生問題。NPR-29532：CQ-4269639的Hotfix
* 路徑欄位會在根路徑開啟，無論指定要搜尋的路徑為何。 NPR-29398：适用于 CQ-4268897 的修补程序
* （体验片段）FacebookApplication#setUpApp 使用已弃用的 API，该 API 不再可用。NPR-29213：适用于 CQ-4266630 的修补程序
* 在執行個體上啟用縮制後，將元件新增至WCM頁面時會產生錯誤警報。 NPR-29476：适用于 CQ-4266197 的修补程序
* 轉出期間沒有從Blueprint傳播空白屬性和多個屬性。 使用Blueprint重設Live Copy對元件無效。NPR-29252：CQ-4264928、CQ-4264926、CQ-4267722的Hotfix
* 處於來源編輯模式時若從全熒幕最小化RTF編輯器，會導致內容遺失。 NPR-28838：适用于 CQ-4260584 的修补程序

### 社区 {#communities-2}

* 沒有版主許可權的訪客和成員可以透過貼上URL檢視未核准和待核准的貼文。 NPR-29726：适用于 CQ-4271124 的修补程序
* 觀察到使用者登入Community時出現40-50秒的高回應時間。 NPR-29679：适用于 CQ-4269444 的修补程序
* 以不同使用者名稱登入時無法重設密碼，且作為金鑰的電子郵件似乎是透過已交換的使用者名稱和電子郵件產生的。 NPR-29281：适用于 CQ-4268694 的修补程序

### 体验片段 {#experience-fragments}

* 使用智慧型影像時無法將體驗片段匯出至目標。 适用于 CQ-4269606 的修补程序

### 复制 {#replication}

* 复制代理组件容易受到漏洞攻击，该漏洞会向未经授权的用户泄露敏感信息。NPR-29613：适用于 Granite-25070 的修补程序
* 用户提供的数据不会在 `cq/replication/components/agent` 组件的输出中进行转义，从而导致存储型跨站点脚本 (XSS) 漏洞。NPR-29452：适用于 CQ-4266263 的修补程序

### 表单 {#forms-3}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-3}

* Forms 附加组件包中没有新的 AEM Forms 修补程序。

### Forms JEE 安装程序 {#forms-jee-installer-2}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

### 6.3.3.5 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in}

AEM 6.3.3.5 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_5-bundle-list.txt)

AEM 6.3.3.5 中包含的内容包列表

[获取文件](assets/do-not-localize/content_packages6335.txt)

### 累积修补程序包 6.3.3.4 {#cumulative-fix-pack-4}

AEM 累积修补程序包 6.3.3.4 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.4 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.16。
* 在Brand Portal復寫代理中新增通訊端逾時和連線逾時。

### 资产 {#assets-4}

* 如果重新上传具有相同名称的存档文件，则不会为新处理的资产生成呈现版本。NPR-28643：适用于 CQ-4262286 的修补程序
* 工作流 CommandLineProcess 因文件名中含有单引号而失败。NPR-28805：适用于 CQ-4262287 的修补程序
* 集合頁面和使用篩選器的集合頁面之間的值不同。 NPR-28642：适用于 CQ-4261405 的修补程序
* 上傳大型zip封存資產時會觸發CommitFailedException。 NPR-28528：适用于 CQ-4260903 的修补程序
* 編輯包含特殊字元的資料夾時，無法儲存資料夾中繼資料。 NPR-28211：适用于 CQ-4260401 的修补程序
* 無法從資產詳細資訊頁面中刪除視訊資產的影像轉譯。 NPR-29149：适用于 CQ-4266073 的修补程序
* 使用DMComponent的DMS7案頭視訊傳送使用漸進式下載，以在發佈模式下播放視訊且不會串流。 NPR-28754：适用于 CQ-4263732 的修补程序
* 無法建立/編輯影像預設集，因為限制存取/etc/dam/video/dynamicmedia停用了影像管理員的功能。 NPR-28662：适用于 CQ-4263022 的修补程序
* 具有DMS7編碼視訊檔案的連結共用導致空白資料夾。 NPR-28851：适用于 CQ-4206743 的修补程序
* 從AEM復寫至Brand Portal的過程長時間卡住。 NPR-28913：适用于 CQ-4254932 的修补程序

### 社区 {#communities-3}

* 無法開啟Outlook寄件匣和收件匣資料夾中含有附件的郵件。 NPR-28559：适用于 CQ-4217072 的修补程序

### 站点 {#sites-4}

* SuggestionHandler for 6.3中有跨網站指令碼(XSS)。NPR-28692：CQ-4253821的Hotfix
* 深度轉出結束卻沒有包含個別LiveCopy中的所有分支。 NPR-29175：适用于 CQ-4239472 的修补程序
* (MSM) 使用 oak-index 实施 LiveCopyIndex。NPR-29198：适用于 CQ-4222472 的修补程序
* 「coral.js」檔案包含易受攻擊的「handlebars.js」程式庫版本。 NPR-26973：适用于 CQ-4255377 的修补程序
* 如果将 Target 组件与嵌套式布局容器和文本组件一起使用，则在编辑文本或单击容器时，会引发以下 JavaScript 错误：“无法读取值为 null 的属性 currentPos”。NPR-29077：适用于 CQ-4246594 的修补程序
* （触屏 UI）无法将标记批量更新到已使用其他标记进行标记的页面。NPR-28729：适用于 CQ-4262922 的修补程序
* 在卡片檢視中開啟變數會造成500錯誤。 NPR-28611：适用于 CQ-4263571 的修补程序
* 转出已在母版中移动的结构会导致错误的 cq:moveTarget。NPR-28968：适用于 CQ-4265280 的修补程序

### 集成 {#integration}

* （云服务配置）在根级别出现的“继承自”复选框应被删除。NPR-28771：适用于 CQ-4259676 的修补程序
* com.day.cq.personalization.impl.TeaserResourceEventHandler進入無限回圈，並造成發佈執行個體上的節點更新。 NPR-28561：适用于 CQ-4263096 的修补程序
* 使用Brightedge認證失敗，發生連線錯誤。 NPR-29167：适用于 CQ-4265872 的修补程序
* OfferproxyTandtProvider.java中出現編譯問題，因為遺失「Resource」類別的匯入陳述式：missing import statement： import org.apache.sling.api.resource.Resource。 NPR-28772

### 商务 {#commerce}

* 排序选项不适用于 Commerce 收藏集中的资产。NPR-28755：适用于 CQ-4213622 的修补程序

### Jetty {#jetty}

* 在 6.3.3 基础上安装 CFP2 后，每个 302 重定向的 error.log 中会出现 Jetty 异常。NPR-28606：适用于 CQ-4262844 的补丁包

### UI - Foundation {#ui-foundation}

* 单击标记将删除全局 mouseup 事件，并且对话框在“可拖动模式”下冻结。NPR-28641：适用于 CUI-7294 的修补程序

### WCM - MSM {#wcm-msm}

* PageManager 移动的 PushOnModify 转出从两个会话提交多次，从而导致出现争用情况。NPR-28880：适用于 CQ-4266191 的修补程序

### 漏洞 {#vulnerability}

* CSRF 保护框架不适用于 AEM Foundation 表单。NPR-28612：适用于 GRANITE-22231 的修补程序

### 表单 {#forms-4}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

AEM Forms的關鍵重點為：

* 啟用原則集檢視頁面上選取每頁專案的選項。
* 為所有瀏覽器新增共用佇列功能。

### Forms 附加组件包 {#forms-add-on-package-4}

#### 表单 - 工作流 {#forms-workflow}

* 共用佇列回應任務會在HTML5工作區中開啟Flash元素。 NPR-29161：适用于 CQ-4266498 的修补程序
* 如果按鈕包含Umlaut字元，則無法從工作區提交。 NPR-29014：适用于 CQ-4263172 的修补程序

#### 表单 - 文档安全 {#forms-document-security}

* 啟用原則集檢視頁面上選取每頁專案的選項。 NPR-29243：CQ-4268567和CQ-4265132的Hotfix

#### 表单 - 文档服务 {#forms-document-services-1}

* OSGi 表单汇编程序无法处理 Acrobat 文件。NPR-29049：适用于 CQ-4254426 的修补程序

#### HTML5 表单 {#html-forms-2}

* 在Designer中以PDF預覽XDP和以HTML預覽相同XDP時會遇到不同的行為。 NPR-28602：适用于 CQ-4260239 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-3}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

### 6.3.3.4 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-1}

AEM 6.3.3.4 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

AEM 6.3.3.4 中包含的内容包列表

[获取文件](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### 累积修补程序包 6.3.3.3 {#cumulative-fix-pack-5}

AEM 累积修补程序包 6.3.3.3 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.3 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.16。
* 原則設定清單分頁變更為每頁限制50筆記錄。
* 已将 rep: cache 添加到发布实例上 AEM Communities 用户同步侦听器中的可忽略节点。
* 为列表和卡片视图按钮添加了 aria 标签。
* 執行任何搜尋時都包含逗號的逸出字元。
* 啟用內容原則的綜合資源支援。

#### 资产 {#assets-5}

* 無法下載多個.jp2、.max、.oft、.msg型別的檔案。 NPR-28002：适用于 CQ-4210856 的修补程序
* ImageServer 发布设置不会复制到混合交付中。NPR-28329：适用于 CQ-4253030 的修补程序

#### 社区 {#communities-4}

* 在Publish上為AEM Communities Enablement元件啟用鍵盤導覽。 NPR-27739：适用于 CQ-4253856 的修补程序
* 啟用鍵盤導覽以觸發內容播放。 NPR-27738：适用于 CQ-4254026 的修补程序
* 为列表和卡片视图按钮添加了 aria 标签。NPR-27736：适用于 CQ-4254027 的修补程序
* （补丁包）已将 rep: cache 添加到发布实例上 AEM Communities 用户同步侦听器中的可忽略节点。NPR-27841：适用于 CQ-4247234 的修补程序
* 在 UI 级别的搜索框中，特殊字符带有转义字符 (\) 前缀。NPR-27839：适用于 CQ-4259757 的修补程序
* 在快速搜索中搜索诸如 (、+、? 之类的字符时出现错误。NPR-28212：适用于 CQ-4260969 的修补程序
* 無法使用API刪除使用者產生的內容中的註解。 NPR-28075：适用于 CQ-4260534 的修补程序
* 發表新評論時，發表在下一頁的評論以黃色醒目提示。 NPR-28148：适用于 CQ-4259681 的修补程序
* 無法開啟Outlook寄件匣和收件匣資料夾中含有附件的郵件。 NPR-28559：适用于 CQ-4217072 的修补程序

#### 站点 {#sites-5}

* 在 AEM 6.3 中运行版本清除，会导致日志中持续不断地反复出现警告。NPR-27750；CQ-4206870的Hotfix
* RTF編輯器全熒幕模式不支援樣式外掛程式。 NPR-27622：适用于 CQ-4258674 的修补程序
* 将内容框架加载到 editor.js 中后，未清除“loaderPromises”列表。NPR-27768：适用于 CQ-4205337 的修补程序
* 若未设置父组件，则无法在嵌套的 Parsys 上设置模板策略。NPR-27987：适用于 CQ-4246095 的修补程序
* 元件瀏覽器沒有清除使用者輸入，因此可能會擲回javascript錯誤。 NPR-27986：适用于 CQ-4247590 的修补程序
* 用户尝试编辑内容片段时，页面显示为空白。NPR-27669
* 當使用者按一下註解時，註解反白顯示會消失。 BPR-27196：CQ-4254423的Hotfix

#### 集成 {#integration-1}

* ResourceResolver未解析目標元件的多個網域。 NPR-28265：适用于 CQ-107847 的修补程序
* 由於未顯示任何動作，LiveCopy繼承取消無法在目標容器上正常運作。 NPR-28129：适用于 CQ-4259813 的修补程序

#### 复制 {#replication-1}

* DispatcherFlushRules中斷6.3.3.1中的復寫NPR-28150：CQ-4261401的Hotfix

#### Campaign — 目標定位 {#campaign-targeting-1}

* TargetedContentManager中的NullPointerException。 适用于 CQ-4263485 的修补程序

#### 社交 — SCORM {#social-scorm}

* 在播放器中删除对可共享内容对象引用模型 (SCORM) 云的引用。适用于 CQ-4260779 的修补程序

#### DAM - 常规 {#dam-general}

* 透過連結共用電子郵件下載傳回空白/損毀的zip。 适用于 CQ-4259686 的修补程序

#### Mac - Test&amp;Target整合 {#mac-test-target-integration}

* 无法对默认受众之外的受众配置“目标组件”选项。适用于 CQ-4261370 的修补程序

#### 翻译 {#translation-1}

* 将 MS Translator 升级到 API v3.0 后，在 AEM 6.3 中启用对 MS Translator 服务的支持。NPR-28365：适用于 CQ-4259096 的修补程序

### 表单 {#forms-5}

### Forms 附加组件包 {#forms-add-on-package-5}

#### 表单 - 工作流 {#forms-workflow-1}

* 無法在HTML5工作區上呈現PDF forms。 NPR-28059：适用于 CQ-4260373 的修补程序

#### 表单 - 文档服务 {#forms-document-services-2}

* 在管理控制台的“策略集”视图中，无法看到除列出的前 1000 项之外的任何其他策略集。NPR-28060、NPR-26047：适用于 CQ-4249865 的修补程序
* 引发名称为 java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE 的异常，导致短暂的进程无法完成。NPR-28652

#### Forms — 最適化Forms {#forms-adaptive-forms}

* 选中复选框项目时，下拉列表中的添加/删除条目不会更新。NPR-28224：适用于 CQ-4252834 的修补程序

### Forms - JEE 安装程序 {#forms-jee-installer-4}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

### 6.3.3.3 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-2}

AEM 6.3.3.3 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6333_bundle_list.txt)

AEM 6.3.3.3 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_list_6333.txt)

### 累积修补程序包 6.3.3.2 {#cumulative-fix-pack-6}

AEM 累积修补程序包 6.3.3.2 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.2 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 AEM 6.3 Service Pack 3 发行说明。

AEM 累积修补程序包的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.15。
* 在「資料夾中繼資料結構」中新增對「規則」標籤和其在「資產資料夾」上強制執行的支援。
* 啟用分頁支援以分組發佈時列出的頁面。
* 啟用可使用任何數字設定的unreadCount通知。 預設值設為20。
* 修正外部連結檢查程式。

#### 资产 {#assets-6}

* 動態下拉式清單不支援階層式下拉式清單。 NPR-27044；CQ-4252564的Hotfix
* 改善查詢以使用ExpiryNotification功能。 NPR-26999：适用于 CQ-4251188 的修补程序
* 規則從中繼資料結構移轉至資料夾中繼資料結構。 NPR-27771：CQ-4257737、CQ-4257735、CQ-4259822的反向移植
* 資產參考調整無法更新Sling ResourceCollections所屬資產的參考。 NPR-26759：适用于 CQ-4252605 的修补程序
* 透過連結共用電子郵件下載傳回空白/損毀的zip檔案。 NPR-27997：适用于 CQ-4259686 的修补程序
* 混合視訊編碼未完成，且未建立縮圖。 NPR-27122：适用于 CQ-4255080 的修补程序

#### 站点 {#sites-6}

* 暂停父页面会导致从缺失页面中删除 cq : LiveRelationship mixin 类型NPR-26996：适用于 CQ-4254113 的修补程序
* （外部链接检查器）内部链接在各个页面上显示为已损坏，但外部链接并非如此。NPR-27481：适用于 CQ-4257780 的修补程序
* 編輯其他頁面屬性時，Cloud Service設定繼承中斷。 NPR-27311：适用于 CQ-4256785 的修补程序
* 搭配Foundation表單使用核心元件時出現Null指標例外狀況。 NPR-27333：适用于 CQ-4249176 的修补程序
* RTF編輯器會移除空白的alt標籤。 NPR-26938：适用于 CQ-4253267 的修补程序
* （经典 UI）存在多个下拉列表时，selectionchanged 侦听器出现性能问题。NPR-27115：适用于 CQ-4237215 的修补程序
* RTF編輯器與多個欄位結合時，出現Uncaught TypeError： fieldAPI.getName不是foundation.js的函式錯誤。 NPR-27146：CQ-4253155、CQ-4259967的Hotfix
* 即使按一下Safari瀏覽器中的選項按鈕，焦點/游標仍停留在RTF編輯器上。 NPR-27144：适用于 CQ-4249635 的修补程序
* 使用者嘗試編輯內容片段時，頁面顯示為空白。 NPR-27669
* 無法為體驗片段建立版本。 NPR-27689：适用于 CQ-4259009 的修补程序

#### 集成 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever遊走整個樹狀結構以收集可用的品牌。 NPR-27060：适用于 CQ-4255790 的修补程序
* 目标组件不考虑 cq: 操作。NPR-27616：适用于 CQ-4257497 的修补程序

#### Sling {#sling}

* 搭配具有相同名稱的類別使用data-sly-use時，會產生不相容的程式碼。 NPR-27282：Sling-7581的Hotfix

#### 商务 {#commerce-1}

* 已更新到 Apache Felix Http Jetty 4.0.6。NPR-26472：适用于 Granite-22916 的修补程序

#### DAM - DM 客户端 {#dam-dm-client}

* 在Dynamic Media元件中指定中斷點後，影像未顯示。 适用于 CQ-4256168 的修补程序

#### DAM - DMServices {#dam-dmservices}

* 包含相关视频的 MixedMediaSet 无法正确同步。适用于 CQ-4251650 的修补程序
* 对于混合媒体集，无法在查看器预设编辑器中播放视频。适用于 CQ-4251442 的修补程序

#### DAM - 常规 {#dam-general-1}

* 套用SP3修補程式後遺失內容片段模型的連結。 适用于 CQ-4259029 的修补程序

#### DAM - UI {#dam-ui}

* 安裝SP3後，資料夾中繼資料結構UI損毀。 适用于 CQ-4257737 的修补程序

#### 社区 {#communities-5}

* 為發佈時列出的群組新增分頁支援。 NPR-26953：适用于 CQ-4246525 的修补程序
* 未讀取計數通知的設定不能超過21。 NPR-27496：适用于 CQ-4252829 的修补程序
* 使用者訂閱限制上限為1000。 NPR-27615：适用于 CQ-4254689 的修补程序
* 在論壇中上傳影像以外的附件（例如.pdf）時發現錯誤。 NPR-27375：适用于 CQ-4257753 的修补程序
* 用於回覆的連結對列點選無效。 NPR-24556：适用于 CQ-4256138 的修补程序
* 刪除UGC時不會刪除與UGC的關係。 NPR-27631：适用于 CQ-4258706 的修补程序
* 如果社群是透過資料庫儲存資源提供者(DSRP)設定，則無法在關鍵字搜尋中依位址值搜尋。 NPR-27652：适用于 CQ-4253261 的修补程序
* 確認刪除後若按一下影像上的垃圾桶圖示，會永久移除附件。 NPR-27340：适用于 CQ-4255150 的修补程序
* 論壇貼文和回覆會新增到第二頁頂端，而重新整理後，貼文就會移至第一頁頂端的正確位置。 NPR-27341：适用于 CQ-4247338 的修补程序
* 啟用Scorm資源完成狀態標籤在UI中顯示為空白。 NPR-27152：适用于 CQ-4249994 的修补程序
* 啟用「允許有特殊許可權者」時，有特殊許可權的成員應該只能為屬於社群成員的使用者撰寫。 NPR-27901：适用于 CQ-4251235 的修补程序

#### 留存 {#sustenance}

* 套件管理器活動記錄應擷取到單獨的記錄檔中。 NPR-27323：适用于 Granite-14866 的修补程序

#### 翻译 {#translation-2}

* 翻译预览不适用于 we.retail 示例内容。NPR-27170：适用于 CQ-4241179 的修补程序

* 主動式platform.login修正。 NPR-26961
* 在具有Tomcat的AEM WAR中，「儲存並關閉」頁面屬性沒有傳回正確的頁面。 NPR-27567：适用于 Granite-23671 的修补程序

* 保存后，通过 sourceEdit 功能输入的文本将丢失。适用于 CQ-4259273 的修补程序

### 表单 {#forms-6}

### Forms 附加组件包 {#forms-add-on-package-6}

#### 表单 - 文档安全 {#forms-document-security-1}

* JEE使用者端SDK出現並行問題。 NPR-27572：适用于 CQ-4247156 的修补程序

#### 表单 - 文档服务 {#forms-document-services-3}

* 在WebSphere上根據SOAP建立表單資料模型失敗。 NPR-27692：适用于 CQ-4253702 的修补程序

#### Forms — 調適型表單 {#forms-adaptive-forms-1}

* AEM Forms 存在 XML 注入漏洞。NPR-27863：适用于 CQ-4257315 的修补程序
* 一旦在網站頁面中設定了錯誤的表單，並選取「表單涵蓋整個頁面寬度」核取方塊，AEM Forms容器元件就會隱藏。 NPR-25972：CQ-4239287、CQ-4249133的Hotfix

### Forms JEE 安装程序 {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* 在WebSphere上根據SOAP建立表單資料模型失敗。 NPR-27692：适用于 CQ-4253702 的修补程序

#### 包含的OSGI套件組合和內容套件 {#osgi-bundles-and-content-packages-included}

AEM 6.3.3.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/63332bundle_list.txt)

AEM 6.3.3.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6332content_package.txt)

### 累积修补程序包 6.3.3.1 {#cumulative-fix-pack-7}

AEM 累积修补程序包 6.3.3.1 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.1 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.14。
* 述詞和搜尋的效能改善。
* 修正預設值的FormData處理問題。
* 將FormBuilder升級至最新的Handlebars版本。
* 新增設定servlet以在對話方塊模式中編輯RTE的設定。
* 新增對複合欄位的支援。
* 使用編輯對話方塊的內容原則啟用/停用RTF編輯器的工具列專案。

#### 资产 {#assets-7}

* 启用 IDS 分离后，DAM 更新资产工作流不再链接引用。NPR-26135：适用于 CQ-4250933 的修补程序
* 無法開啟解封存器步驟建立的封存檔解壓縮後檔名中有%的資料夾。 NPR-26275：适用于 CQ-4251482 的修补程序
* 單引號字元導致中繼資料無法更新。 NPR-26808：适用于 CQ-4254305 的修补程序
* (Omnisearch) 在收藏集中搜索时，出现性能问题。NPR-26714：适用于 CQ-4253408 的修补程序
* 使用GQLConverter進行全文檢索搜尋時，如果文字中包含「OR」字母，則會錯誤處理。 NPR-26564：适用于 CQ-4247362 的修补程序
* 來自多租使用者的共用資產連結會在租使用者ID前加上文字，形成無效的URL。 NPR-26482：适用于 CQ-4253540 的修补程序
* 在 Dynamic Media 云配置 UI 中，禁用“公司根文件夹路径”。NPR-26361：适用于 CQ-4249505 的修补程序
* .mos RAW檔案的擷取時間延長。 NPR-26296：适用于 CQ-4250661 的修补程序
* 资产链接共享不允许使用数字用户 ID 添加多个内部用户。NPR-26206：适用于 CQ-4251466 的修补程序
* 使用 deflate64 算法压缩的 ZIP 文件损坏。NPR-26793：适用于 CQ-4253995 的修补程序
* 缩略图生成过程无法正确用于复杂的 PDF 文件，从而导致缩略图中缺少图像的部分内容。NPR-26057：适用于 CQ-4250944 的修补程序
* 產生縮圖時出現棧積記憶體使用問題。 NPR-25545：适用于 CQ-4246960 的修补程序
* 在資產上建立大量關係會導致錯誤。 NPR-26309：适用于 CQ-4250708 的修补程序
* 「刪除轉譯」選項無法運作，且擲回「無專案可刪除」錯誤。 NPR-26007：适用于 CQ-4213414 的修补程序
* 無法刪除多值欄位的預設值。 NPR-25116：适用于 CQ-4247856 的修补程序
* （DM 混合模式）带有 Dynamic Media 的 AEM 6.3.2 的目录复制中断。NPR-26406：适用于 CQ-4251306 的修补程序

#### 站点 {#sites-7}

* Sites修正的主動式反向移植。 NPR-26963
* 「標題」和「名稱」案例型別不同時會建立兩次標籤。 NPR-26877：适用于 CQ-4254134 的修补程序
* 編輯對話方塊中的RTF編輯器功能不受原則控制。 NPR-27059、NPR-26750：适用于 CQ-4241130 的修补程序
* 使用者端內容segment.js快取與非快取問題。 NPR-26622：适用于 CQ-4253486 的修补程序
* 经典 UI 中子规则的区段规则 (/etc/segmentation) 激活导致发布下降。NPR-26601：适用于 CQ-4253588 的修补程序
* 新增「特殊字元」會將RTF編輯器對話方塊捲動到頂端。 NPR-26435：适用于 CQ-4249869 的修补程序
* （触屏 UI）从全屏切换到浮动对话框时，多个富文本编辑器的工具栏变得不可用。NPR-25652：适用于 CQ-4206008 的修补程序
* 提升多頁啟動會為每個頁面建立多個版本。 NPR-26810：适用于 CQ-4254663 的修补程序
* 標籤移動操作未反映在結構化內容片段模型標籤欄位中。 NPR-26801：适用于 CQ-4251805 的修补程序
* （触屏 UI）重命名 Blueprint 中的页面后，无法从页面编辑器取消发布子页面。NPR-26774：适用于 CQ-4254175 的修补程序
* 未发布的页面无法使用引用。NPR-26749：适用于 CQ-4254372 的修补程序
* 将变量创建为 Live Copy 需要用户刷新页面才能得以反映。NPR-26663：适用于 CQ-4254328 的修补程序
* （经典 UI）返回页面属性后，缩略图图像不再使用继承并从站点管理和 Sidekick 中消失，导致图像显示为空白。NPR-26562：适用于 CQ-4252346 的修补程序
* 建立頁面的版本並觸發比較時，/content/ versionshistory中的節點會列在Blueprint的即時副本清單中。 NPR-26506：适用于 CQ-4243957 的修补程序
* 體驗片段管理員編輯器中的URL不允許覆蓋。 NPR-26318：适用于 CQ-4252156 的修补程序

#### 平台 {#platform}

* 包含测试事件的 ReplicationEventListener 中出现会话泄漏。NPR-25937：适用于 CQ-4251090 的修补程序
* 復寫使用過期的OAuth代號，導致多個錯誤。 NPR-25894：适用于 GRANITE-22388 的修补程序

#### 集成 {#integration-3}

* 升級為Handlebars 4後，由於使用不相容的範本，透過AEM內嵌的TSDK中斷。 NPR-26699：适用于 CQ-4248974 的修补程序
* 發佈含有新資產的頁面時，會從發佈執行個體中停用子頁面，而不會發出通知。 NPR-24869：适用于 CQ-4247832 的修补程序
* 復寫使用過期的oauth代號。 NPR-25984：适用于 Granite-22388 的修补程序

#### 复制 {#replication-2}

* Http傳輸可能會洩漏開啟的工作階段。 Granite-17434的Hotfix
* 多個復寫代理同時存取存取存取權杖節點時，記錄中出現例外狀況。 NPR-26964：GRANITE-23276、Granite-23155的Hotfix

#### ContextHub {#contexthub}

* 「coral.js」檔案包含易受攻擊的「handlebars.js」程式庫版本。 适用于 CQ-4255377 的修补程序

#### DAM - DM 客户端 {#dam-dm-client-1}

* 刪除影像資產的復本會使原始影像資產無法使用。 适用于 CQ-4251648 的修补程序
* 從S7伺服器備援下載額外的影像內容。 适用于 CQ-4248770 的修补程序

#### Granite {#granite}

* AEM OAuth提供者沒有執行不區分大小寫的搜尋。 NPR-26133：适用于 GRANITE-22650 的修补程序
* 套件驗證器不會驗證CFP/SP中包含的套件。 NPR-26775：适用于 Granite-22825 的修补程序

#### 社区 {#communities-6}

* 搜尋結果出現分隔符號問題。 NPR-27051：适用于 CQ-4248939 的修补程序
* 在 Adobe 存储资源提供程序中，将下拉列表值从“达拉斯”更改为“弗吉尼亚”。NPR-26936：适用于 CQ-4254434 的修补程序
* 在 SocialTagManager 中启用对本地化标题搜索的支持。NPR-26932：适用于 CQ-4250276 的修补程序
* 建立論壇貼文時，附件影像未顯示縮圖。 NPR-26380：适用于 CQ-4253105 的修补程序
* 從Word外掛程式貼上時，無法載入一個以上的影像。 NPR-26728：适用于 CQ-4253638 的修补程序
* 無法篩選稽核頁面中的內容。 NPR-26697：适用于 CQ-4213766 的修补程序
* （安全漏洞）由于 JWT 配置错误，导致帐户接管。NPR-26440：适用于 CQ-4253314 的修补程序
* 從Adobe儲存資源提供者擷取資料的速度緩慢。 NPR-26237：适用于 NPR-24152 的修补程序
* 私人訊息撰寫頁面的行為不穩定且緩慢。 NPR-26120：适用于 CQ-4250923 的修补程序
* 「全部標籤為已讀」通知只將前10個轉譯為未讀，而不重新整理頁面。 NPR-27036：适用于 CQ-4254058 的修补程序
* Communities評論區段分頁點按和頁面載入行為。 NPR-27030：适用于 CQ-4251228 的修补程序
* （论坛搜索）“返回”按钮跳过页面，并返回到 forum.html。NPR-26949：适用于 CQ-4254804 的修补程序
* 未讀通知數增加不超過21。 NPR-26947：适用于 CQ-4251251 的修补程序
* （SearchScheduledPosts 作业）在 ConfigMgr 中添加启用/禁用切换开关。NPR-26924：适用于 CQ-4250463 的修补程序
* 在「工作總攬」頁面上捲動時，Tomcat Context(/aempublish)路徑會掉格。 NPR-26919：适用于 CQ-4254345 的修补程序
* 建立群組和成員時出現NullPointerException。 NPR-26778：适用于 CQ-4248095 的修补程序
* 版主取消釘選和取消精選內容無法搭配MySQL單一職責原則(SRP)使用。 NPR-26767：适用于 CQ-4251520 的修补程序
* 某些字元出現搜尋功能問題。 NPR-26726：适用于 CQ-4247744 的修补程序
* 啟用稽核UI和啟用資源的深層連結。 NPR-26705：适用于 CQ-4251381 的修补程序
* 論壇元件出現搜尋問題。 NPR-26577：适用于 CQ-4251303 的修补程序
* 在Communities訊息中同時搜尋名字和姓氏時沒有傳回預期的結果。 NPR-26377：适用于 CQ-4253150 的修补程序
* 移除回覆時分頁未更新。 NPR-26327
* 刪除貼文會生效，但控制檯會出現錯誤，且貼文仍可在UI上看到。 NPR-26292：适用于 CQ-4252803 的修补程序
* 分頁沒有動態更新，且回覆清單持續變長。 NPR-26145：适用于 CQ-4251586 的修补程序
* 若群組包含5萬到10萬名使用者，則群組設定不會載入。 NPR-25642：适用于 CQ-4238426 的修补程序
* 目錄資源播放器的內容路徑失敗。 NPR-25640：适用于 CQ-4238426 的修补程序
* （论坛搜索）- 包含大量帖子的线程的分页链接不适用于通知。适用于 CQ-4254202 的修补程序
* 使用Firefox時，稽核主控台只會顯示5個專案。 适用于 CQ-4254128 的修补程序
* 建立網站時群組不可見。 NPR-27148：适用于 CQ-4251788 的修补程序
* 将组和成员添加到“角色”设置中，并在博客功能中允许拥有权限的成员时，出现空指针异常。NPR-21732、NPR-27176：适用于 CQ-4255909 的修补程序
* 編輯網站並在角色設定中新增成員會擲回Null指標例外狀況。 NPR-27132：适用于 CQ-4255909 的修补程序

#### 用户界面 {#user-interface}

* 主動式平台登入修正。 NPR-26961
* （多字段）允许复合项目拥有自定义名称。NPR-26493：适用于 Granite-20568 的修补程序
* 貼上頁面後欄檢視沒有更新，直到重新整理後才更新。 NPR-26030：适用于 CQ-4236346 的修补程序
* 主動式granite.ui.commons修正。 NPR-26960
* 主動式granite.ui.content修正。 NPR-26959
* 主動式CQ/體驗記錄修正。 NPR-26943
* 主動式Foundation UI反向移植。 NPR-26942
* (IE 11) 键入负值时，数字字段中会显示“NaN”。NPR-26701：适用于 CQ-100826 的修补程序
* （Coral 多字段）嵌套的多字段使用错误模板来创建项目。NPR-25649：适用于 CUI-6743 的修补程序
* 更新 granite coralui2 和 coralui3 clientlib 以从内部版本中删除 Handlebars。NPR-25606：适用于 Granite-22116 的修补程序

### 表单 {#forms-7}

### Forms 附加组件包 {#forms-add-on-package-7}

#### 表单 - 文档安全 {#forms-document-security-2}

* 非作用中金鑰的伺服器記錄中出現主體金鑰變換例外狀況。 NPR-26748：适用于 CQ-4253705 的修补程序
* 無法建立或修改Document Security的水印設定。 NPR-26267、NPR-26129：适用于 CQ-4250234 的修补程序

#### 表单 - 文档服务 {#forms-document-services-4}

* 使用“验证 PDF/A”进行 PDF/A 验证时，未显示有效。NPR-25934：适用于 CQ-4248558 的修补程序

#### 表单 - 交互式通信 {#forms-interactive-communication}

* 編輯、儲存可編輯模組，然後開啟/關閉PDF預覽時，信函的PDF和HTML預覽可在相同視窗中顯示和運作。 NPR-26770：适用于 CQ-4253217 的修补程序

#### 表单 - 工作流 {#forms-workflow-2}

* 工作區會斷斷續續地停頓並重複顯示起始點。 NPR-26461：适用于 CQ-4253439 的修补程序
* 任務名稱中使用大括弧時，記錄中會擲回ESAPI例外狀況。 适用于 CQ-4256627 的修补程序
* 開啟與起點相關聯的非預填適用性表單/表單集時，會擲回Null指標例外狀況。 适用于 CQ-4256124 的修补程序
* 無法使用全域設定傳送電子郵件。 NPR-26163：适用于 CQ-111110 的修补程序
* 套用axis.jar檔案後無法開啟工作區。 NPR-26131：适用于 CQ-4251126 的修补程序
* “刷新”按钮无法将最新数据从服务器同步到自适应表单。适用于 CQ-4255670 的修补程序
* 从管理员 UI 设置搜索模板，然后使用该模板在 AEM Forms 工作区中搜索任务会引发异常。适用于 CQ-4255649 的修补程序
* 名称中带有圆括号符号的应用程序下的进程跟踪详细信息未显示在 HTML 工作区中。适用于 CQ-4242101 的修补程序
* 在HTML工作區的偏好設定畫面中儲存變更時，系統擲回例外狀況。 适用于 CQ-4241485 的修补程序
* 最新JEE設定的大量核准失效。 适用于 CQ-4241486 的修补程序
* 最新6.4 JEE伺服器上的任務/起始點草稿失敗。 适用于 CQ-4241484 的修补程序
* 設定Date()。getTime()。toString引數來初始化工作階段，而非Date.toString()。 适用于 CQ-4241483 的修补程序
* 打开 /lc/ws 时，发现 HTML 参数中存在易受攻击的字符异常。适用于 CQ-4241481 的修补程序

#### 漏洞 {#vulnerability-1}

* 表单管理器的注释选项卡中存在存储型跨站点脚本 (XSS) 漏洞。NPR-27157：适用于 CQ-4255556 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Enterprise Security API的程式碼審查。 适用于 CQ-4255638 的修补程序
* 無法將esapi.properties載入為WAS9中的類別載入器資源。 适用于 CQ-4255631 的修补程序
* 在網域設定期間按一下「新增驗證」會擲回錯誤。 适用于 CQ-4255634 的修补程序
* Forms JEE 支持 PKCS#11 双向身份验证。NPR-21372
* 修正Core靜態程式碼分析中報告的問題。 适用于 CQ-104446 的修补程序
* 运行 LCM 时，部署 adobe.livecycle.weblogic.ear 和 adobe.livecycle.websphere.ear 会失败。适用于 CQ-4255629、CQ-4255630 的修补程序
* 应用程序管理中出现无效的错误消息。NPR-23289：CQ-4233163、CQ-4255636的Hotfix
* 在網域設定期間按一下「新增驗證」會導致錯誤。 适用于 CQ-4255634 的修补程序

#### 表单 - JEE 连接器 {#forms-jee-connector}

* 修正Connector靜態程式碼分析中報告的問題。 NPR-22260

#### PDFG 服务 {#pdfg-service-1}

* 從LiveCycle升級為AEM 6.2表單後，記錄中出現org.jgroups.Message錯誤。 NPR-26795：适用于 CQ-4220415 的修补程序
* AEM forms — 移轉樣式時發生錯誤。 适用于 CQ-4251969 的修补程序
* 修正PDFG靜態程式碼分析報告中報告的問題。 NPR-23251：适用于 CQ-4213930 的修补程序

#### 6.3.3.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-3}

AEM 6.3.3.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/63sp3cfp1bundlelist.txt)

AEM 6.3.3.1 中包含的内容包列表

### 累积修补程序包 6.3.2.2 {#cumulative-fix-pack-8}

AEM 累积修补程序包 6.3.2.2 是一个重要更新，它包括自 2018 年 4 月 AEM 6.3 Service Pack 2 (6.3.2.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.2.2 依赖于 AEM 6.3 Service Pack 2。因此，您必须先安装 AEM 6.3 Service Pack 2，然后再安装 AEM 累积修补程序包 6.3.2.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 2 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp2-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.11。
* 在Brand Portal上啟用子資產和多頁資產檢視器。
* 將欄位型別的長度變更為255，以支援不同附件型別的所有可能mime型別。
* 設定了影像違反上傳條件時從伺服器傳出的錯誤訊息。
* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。
* 更新至cq-wcm-content和com.adobe.cq.launches.it.serverside的最新版本。
* 將com.adobe.granite.ui.coralui3-rte更新至最新發行版本。
* 当 expressionResolver 为 null 时，确定的呈现条件返回正常结果。
* Coral.ColumnView：添加了对“按住 Shift 键单击”的支持。

### 资产 {#assets-8}

* 資產資料夾封閉使用者群組(CUG)欄位未傳回「所有人」群組。 NPR-23163：适用于 CQ-4239377 的修补程序
* 搜尋智慧型系列儲存的搜尋不會傳回所有結果。 NPR-23243：适用于 CQ-4240355 的修补程序
* (ExpiryNotificationJobImpl) 优化了现有查询。NPR-23330：适用于 CQ-4205249 的修补程序
* （元数据配置文件）创建时设置的标准标记值在保存后不可用。NPR-23370：适用于 CQ-4235458 的修补程序
* （触屏 UI）由于 JS 错误，无法移动多个资产。NPR-23395：适用于 CQ-4241279 的修补程序
* 下載大小與顯示的資訊不相符不正確，導致使用者混淆。 NPR-23418：适用于 CQ-4242774 的修补程序
* 為副檔名LSR和SKETCH擷取的mimetype不正確，並導致無效的檔案下載。 NPR-23644：适用于 CQ-4243260 的修补程序
* (Firefox/Chrome) 无法在“资产共享”页面中下载资产。NPR-23963：适用于 CQ-4244391 的修补程序
* 預覽後搜尋面板中的資產管理員搜尋面向消失。 NPR-23964：适用于 CQ-4244410 的修补程序
* 取消發佈搜尋表單會完全移除預設的搜尋表單。 NPR-23291：适用于 CQ-4241382 的修补程序
* (Brand Portal) 应在复制时筛选出目录谓词中的搜索。NPR-23292：适用于 CQ-4241385 的修补程序
* 發佈至Brand Portal UI動作無法使用。 NPR-23293：适用于 CQ-4241161 的修补程序
* 發佈/取消發佈至Brand Portal按鈕不應適用於內容片段。 NPR-23318：适用于 CQ-4245086 的修补程序
* (Brand Portal) 发布资产后允许创建子资产。NPR-23331：适用于 CQ-4242018 的修补程序
* Dynamic Media請求不使用Proxy/HTTP通用使用者端。 NPR-10727：CQ-45695、CQ-88800的Hotfix
* 無法在Dynamic Media S7 (DMS7)中為單一轉譯MP4視訊資產加上註釋。 NPR-22046：适用于 CQ-4215912 的修补程序
* 对于 Ptiff 生成流程，EmbedXMP 数据始终设置为“活动”。NPR-22903：适用于 CQ-4234498 的修补程序
* 大量影像預設集出現動態轉譯顯示/選擇問題。 NPR-23151：适用于 CQ-4217511 的修补程序
* Dynamic Media編碼視訊 — 修改/重新上傳啟動器出現問題。 NPR-23237：适用于 CQ-4240260 的修补程序
* 修复了 Dynamic Media S7 中 HTTP 转发器的代理处理问题。NPR-24001：适用于 CQ-244140 的修补程序

### 站点 {#sites-8}

* 查询生成器差异导致 6.2 与 6.3 之间的 xPath 转换不同。NPR-23245：适用于 CQ-4240396 的修补程序
* 展开对话框时，页面属性中的“缩略图”选项卡不起作用。NPR-22844：适用于 CQ-4241474 的修补程序
* Parsys中斷了模擬器裝置框架寬度，並裁切掉其中新增的任何元件。 NPR-22926：适用于 CQ-4238224 的修补程序
* 執行多次啟動時，會在Author中提升該啟動，但由於缺少復寫許可權，因此不會在Publish伺服器上復寫變更。 NPR-22934：适用于 CQ-4234746 的修补程序
* 用户在第一个会话中锁定的页面，可以被另一个会话中的其他用户修改。NPR-23057：适用于 CQ-4199017 的修补程序
* 修正清單檢視中的可重新排序選項。 NPR-23065：适用于 CQ-4239321 的修补程序
* （页面编辑器）再次打开对话框时，图像组件上的图像消失。NPR-23156：适用于 CQ-4239978 的修补程序
* 範本編輯器僅顯示20個範本/資料夾，且捲動至頁面底部時未載入其他範本/資料夾。 NPR-23185：适用于 CQ-4238483 的修补程序
* （经典 UI）移动或重命名页面时产生错误。NPR-23213：适用于 CQ-4240971 的修补程序
* 無法編輯/建立ContextHub區段 NPR-23218：适用于 CQ-4226948 的修补程序
* （富文本编辑器）- 替换操作会更改单词的格式。NPR-23271：适用于 CQ-4239677 的修补程序
* XF變異的Blueprint索引標籤中缺少轉出按鈕。 NPR-23320：适用于 CQ-4240404 的修补程序
* 由於功能遭淘汰，傳統UI無法用於編輯CUG。 NPR-24122：适用于 4241823 的修补程序
* 主動式修正，可防止不想要的內容促銷活動。 NPR-24387：适用于 4244993 的修补程序
* 一旦約 在Assets的資料夾中新增80個片段，從時間軸主控台觸發工作流程時遇到錯誤。 NPR-23393；CQ-4211216的Hotfix
* 無法將影像從內容尋找器拖放至RTF編輯器對話方塊中。 NPR-23403：适用于 CQ-4242094 的修补程序
* 将组件从 AEM 6.0 迁移到 AEM 6.2 时出现“无效的递归选择器值”错误。NPR-23532：适用于 CQ-4241258 的修补程序
* （富文本编辑器）工具提示显示插件的变量名称，而不是可读的插件名称。NPR-23550：适用于 CQ-4243269 的修补程序
* 無法透過行動/平板電腦版本中必要的選取下拉式清單儲存對話方塊。 NPR-23904：适用于 CQ-4243096 的修补程序
* 樣式系統選項會出現在安裝6.3.2.1之後的所有頁面上。 NPR-23972：适用于 CQ-4244394 的修补程序
* 由於功能遭淘汰，傳統UI無法用於編輯CUG。 NPR-24122：适用于 4241823 的修补程序
* 主動式修正，可防止不想要的內容促銷活動。 NPR-24387：适用于 4244993 的修补程序
* 資產移動時不會更新資產參考。 NPR-23208：适用于 CQ-4239879 的修补程序

### 平台 {#platform-1}

* 如果在搜尋面向中使用標籤述詞，儲存後智慧型集合不會顯示結果。 NPR-23401：适用于 Granite-21278 的修补程序
* 修补 clientlib 中的 jQuery 1.12.4 以包含安全修补程序。NPR-24128：适用于 Granite-20058 的修补程序
* 除非重新啟動套件組合，否則國際化翻譯不會更新。 NPR-23193：Sling-7190的Hotfix
* ReplicationEventListener中無結尾標籤的資源解析器。 NPR-23240：适用于 CQ-4241350 的修补程序
* 「Day CQ Mail Service」支援STARTTLS。 NPR-23941：适用于 CQ-4240397 的修补程序
* JCR申訴標籤名稱應根據標籤標題自動填入。 NPR-24173：适用于 CQ-4199411 的修补程序

### 集成 {#integration-4}

* (Target) 将 API 类型用作 XML 时，不会激活营销活动。NPR-23199：适用于 CQ-4240936 的修补程序****
* 中繼資料夾結構導致設定參考復寫失敗。 NPR-23485：适用于 CQ-4242751 的修补程序

### 漏洞 {#vulnerability-2}

* Salesforce 集成容易遭受服务器端请求伪造 (SSRF) 攻击。NPR-24289：适用于 CQ-424527 的修补程序
* 管理員UI專案連結中有跨網站指令碼(XSS)。 NPR-23272：适用于 CQ-4241795 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components}

* Foundation表格容易受到儲存型跨網站指令碼攻擊。 NPR-23214：适用于 CQ-4240760 的修补程序

### 翻译 {#translation-3}

* 建立語言副本時沒有刪除即時副本屬性。 NPR-23123：适用于 CQ-4230641 的修补程序

### 用户界面 {#user-interface-1}

* DatePicker不支援手動設定隱藏欄位所設定的外部型別提示。 變更型別提示會出現轉換錯誤。 NPR-23371：适用于 Granite-21194 的修补程序
* Coral.ColumnView：新增對Shift +按一下操作的支援。 NPR-23404：适用于 Granite-13338 的修补程序
* 選取了具有空白值的專案時，選取RT不會驗證。 NPR-23405：适用于 Granite-21283 的修补程序
* (OMEGA) 仅以英语报告“功能”。NPR-23990：适用于 Granite-21231 的修补程序
* Coral.Autocomplete API的修正。 NPR-23516

### Granite {#granite-1}

* Apache Http使用者端追蹤連線和高棧積使用率導致AEM伺服器當機。 NPR-23906：适用于 Granite-21056 的修补程序

### 商务 {#commerce-2}

* Campaign json輸出不包含servlet內容根目錄。 NPR-23733：适用于 CQ-4243827 的修补程序

### 社区 {#communities-7}

* 對社群進行搜尋因幾個字而失敗。 NPR-23256：适用于 CQ-4240717 的修补程序
* 無法為社群管理員角色指派群組的問題。 NPR-23317：适用于 CQ-4241233/CQ-4221399 的修补程序
* 使用類似的資產名稱建立資源時出現問題。 NPR-23319：适用于 CQ-4240700 的修补程序
* (ContextPath) 在社区组成员列表中搜索组成员时，中断消息功能因 Jetty 配置和错误而中断。NPR-23336：CQ-4241519、CQ-4242080的Hotfix
* 上傳至Communities論壇的影像未出現在Adobe儲存資源提供者(ASRP)中。 NPR-23397：适用于 CQ-4242497 的修补程序
* 已刪除的創意會在活動中顯示為作用中連結。 NPR-23406
* imsmanifest.xml無法以使用內容根目錄執行的AEM載入。 NPR-23483：适用于 CQ-4242193 的修补程序
* 舊版Handlebars中存在安全性漏洞。 NPR-23518：适用于 CQ-4243055 的修补程序
* 通道服務無法運作。 NPR-23543：适用于 CQ-4242217 的修补程序
* 透過Dispatcher存取且對其啟用Sling動態包含時，Communities元件出現問題。 NPR-23586：CQ-4242360、CQ-4241522的Hotfix
* 當搜尋會透過搜尋產生許多結果的搜尋字詞，然後輸入新的搜尋字詞時，未重設分頁。 NPR-23739：适用于 CQ-4222593 的修补程序
* 對論壇元件執行搜尋時出現問題。 NPR-23838：适用于 CQ-4243770 的修补程序
* （社区审核标记）无法批量允许已标记的消息。NPR-23845：适用于 CQ-4243962 的修补程序
* 儘管選取了預設的排序順序，排序按鈕文字仍沒有顯示預設的選取值。 NPR-23881：适用于 CQ-4243375 的修补程序
* 由于向组发送消息失败，未触发 Web 和邮件通知。NPR-23934：适用于 CQ-4242880 的修补程序
* 使用DSRP設定時，標幟使用者和原因沒有詳細資訊。 NPR-23973：适用于 CQ-4243205 的修补程序
* 已取消標幟的使用者之標幟理由仍然可見/ NPR-23974：CQ-4243822的Hotfix
* 將具有相同名稱的兩個檔案附加至一個表單貼文兩次，會導致伺服器錯誤。 NPR-24166：适用于 CQ-4244367 的修补程序
* 無法使用資料庫儲存資源開發工具(DSRP)儲存mime型別超過15個字元的附件。 NPR-24174
* 將違反上傳准則的影像拖放至貼文的文字中時，系統會擲回伺服器錯誤，且會向使用者顯示一般錯誤訊息。 NPR-24243
* 多個AEM Communities伺服器端問題的修正。 NPR-23971：CQ-4243144、CQ-4242145、CQ-4243365、CQ-4244098的Hotfix
* 多個Adobe Social問題的修正。 NPR-24242：适用于 CQ-4245054、CQ-4245120、CQ-4245296 的修补程序

### 营销活动 {#campaign}

* Campaign json輸出不包含servlet內容根目錄。 NPR-23733：适用于 CQ-4243827 的修补程序

### MSM {#msm}

* 转出页面时，LiveCopy 不会显示从母版继承的打开/关闭时间属性。NPR-23873：适用于 CQ-4243431 的修补程序
* LiveCopy作業不會忽略已刪除元件的子節點。 NPR-23058：适用于 CQ-4211662 的修补程序

### 卸载 {#offloading}

* 请求机制在处理后或定期从工作线程实例中清理资产。NPR-23638：适用于 Granite-21337 的修补程序

## 表单 {#forms-8}

### Forms 附加组件包 {#forms-add-on-package-8}

#### 自适应表单 {#adaptive-forms-1}

* 將ReCaptchaConfigService移至內部套件。 适用于 CQ-4217459 的修补程序
* 數值欄位未遵循最小值。 NPR-23967：适用于 CQ-4244830 的修补程序
* 透過AdobeSign支援最適化Forms整合中的多重分片。 NPR-23383

#### 後端整合 {#backend-integration}

* (FDM)（Web 服务）在 WSDL 解析器中支持 WSDL 的扩展结构。NPR-23640，NPR:23236: 适用于 4205821 的修补程序
* 在Forms附加使用者端SDK中包含SDLInvokerParams。 NPR-23157

### Forms JEE 安装程序 {#forms-jee-installer-7}

#### 进程管理 {#process-management}

* 套用新的axis.jar檔案後無法開啟工作區。 NPR-23316
* LiveCycle容易在PMAdmin上遭受XSS攻擊。 NPR-23267
* 升级到 AEM 6.1 Forms 后，访问特定用户的任务列表时，HTML 工作区会冻结。NPR-23943

#### 核心 {#core}

* Forms JEE 支持 PKCS#11 双向身份验证。NPR-21372

#### PDFG 服务 {#pdfg-service-2}

* 同時處理TIFF檔案（大小約50 KB）時，紙張擷取服務當機。 NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms伺服器輸出 — 遺失註解的替代說明。 NPR-22207
* 將PDF/UA支援新增至透過設計工具和Output Service產生的XML表單。 NPR-23132

### 6.3.2.2 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-4}

AEM 6.3.2.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_3_2_2_bundle-list.txt)

AEM 6.3.2.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### 累积修补程序包 6.3.2.1 {#cumulative-fix-pack-9}

AEM 累积修补程序包 6.3.2.1 是一个重要更新，它包括自 2018 年 4 月 AEM 6.3 Service Pack 2 (6.3.2.0) 正式发布以来的若干内部修补程序和客户修补程序。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.10。
* 改善傳統UI中轉譯Parsys元件的功能。
* 更新Sling模型套件組合以包含字元集修正。
* 已針對所有資產型別非同步處理發佈至Brand Portal。
* 將coralui-component-richtexteditor.git從0.1.15更新至0.1.16
* 修复了下拉组件的显示/隐藏功能。
* 啟用核心影像元件的影像翻轉功能。
* 更新felix http套件組合以啟用工作階段屬性。

* 由于内存消耗问题，移除了 Sling 模型上的 cache=true。

### 资产 {#assets-9}

* 在“资产文件夹”设置中更改标题或缩略图图片时，文件夹的原始组和权限会被覆盖。NPR-22171：适用于 CQ-4216080 的修补程序
* UI擲回假錯誤「發佈至Brand Portal失敗」，但工作已新增至復寫佇列且資產已發佈至Brand Portal。 NPR-22179：适用于 CQ-4205273 的修补程序
* （触屏 UI）列视图中资产的默认上传位置。NPR-22465：适用于 CQ-4237057 的修补程序
* 嘗試將資產結構從/conf/global複製到/conf/ mytenant時，AEM擲回StackOverflow錯誤。 NPR-22489：适用于 CQ-4235875 的修补程序
* 由於資料夾名稱結尾有空格，因此嘗試解壓縮ZIP封存檔失敗。 NPR-22522：适用于 CQ-4238036 的修补程序
* 使用資產標題欄進行排序無法用於搜尋結果。 NPR-22908：适用于 CQ-4239076 的修补程序
* Youtube影片以完整路徑標籤，而非標籤名稱本身。 NPR-22976：适用于 CQ-4238669 的修补程序
* 在可重新排序的資料夾下重新排序資料夾不會持續存在。 NPR-23125：适用于 CQ-4231761 的修补程序
* HTTP 504：嘗試使用共用連結共用集合時，發生閘道逾時錯誤。 NPR-21928：适用于 CQ-4234507 的修补程序
* 當一個PDF資產有多個相關聯的關鍵字時，PDF關鍵字中繼資料無法正確擷取和錯誤修改。 為解決此問題，已移除PDF資產的「主旨」欄位中繼資料屬性。 不過，您可以編輯中繼資料結構，為「主旨」欄位新增多值文字欄位。 NPR-21972：适用于 4215741 的修补程序****
* 如果在2個快顯視窗顯示之間變更了選取的資料夾，系統會刪除錯誤的資產。 NPR-21980：适用于 CQ-4233675 的修补程序
* (DAM) 添加到收藏集向导时，出现多个跨站点脚本 (XSS) 漏洞。NPR-22432：适用于 CQ-4327086 的修补程序
* 在 Safari 上的资产中使用数字版权管理时，资产下载失败。用户无法下载包含免责声明和长文件名的资产。NPR-22747：适用于 CQ-4236460 和 CQ-4235274 的修补程序
* 將公開共用設為將資產發佈至Brand Portal時的預設選項。 NPR-21931：适用于 CQ-4218816 的修补程序

### 站点 {#sites-9}

* 工作流收件箱中的新项目显示页面路径而非页面标题。NPR-21634：适用于 CQ-4230672 的修补程序
* 可編輯的結構元件遺失編輯時回應式格線所需的CSS類別名稱。 NPR-21741：适用于 CQ-4232374 的修补程序
* （触屏 UI）HTL 组件存在多个跨站点脚本 (XSS) 漏洞。NPR-21899：适用于 CQ-4232511 的修补程序
* 無法變更內容片段混合媒體影像資源型別。 NPR-21907：适用于 CQ-4233401 的修补程序
* 觸控式UI對話方塊的RTE全熒幕隱藏了RTE外掛程式。 NPR-22034：适用于 CQ-4235457 的修补程序
* （触屏 UI）富文本编辑器会从 &lt;a> 标记中删除 id 以外的所有其他属性。NPR-22044：适用于 CQ-4234133 的修补程序
* 由於長時間執行的查詢（超過6個）出現多個棧疊，導致AEM變得緩慢。 NPR-22134：适用于 CQ-4233904 的修补程序
* 無法變更名稱中有冒號的節點的許可權。 NPR-22136：适用于 CQ-4236221 的修补程序
* （经典 UI）富文本编辑器输出 html 将“list-position-style: inside;”作为内嵌样式添加到 &lt;ul> 标记中。NPR-22145：适用于 CRTE-114 的修补程序
* 當文字為空白時，讓TreeNode遞補為name屬性。 NPR-22146：适用于 CQ-4234724/CQ-4236300 的修补程序
* RSS摘要問題，AEM 6.3的連線埠–1。NPR-22176：CQ-4233339的Hotfix
* （经典 UI）粘贴文本快捷键 (Ctrl+V) 对 OOTB 文本（富文本）组件不起作用。NPR-22224：适用于 CQ-4236224 的修补程序
* 在键入文本时，Tagfield 的筛选功能无法按预期发挥作用。NPR-22236：适用于 CQ-4236655 的修补程序
* （页面编辑器）在图像映射组件中粘贴文本数据时，也会粘贴文本组件。NPR-22264：适用于 CQ-4236230 的修补程序
* 必須填寫對話方塊FileUpload欄位會導致提交對話方塊時發生問題。 NPR-22464：适用于 CQ-4222192 的修补程序
* 如果移動的頁面或其反向連結無法啟動，移動w/o復寫許可權會啟動啟動工作流程請求。 NPR-22467：适用于 CQ-4211765 的修补程序
* 加载包含大量（2000 及以上）受众的页面时，出现性能问题。NPR-22478；CQ-4209567的Hotfix
* 在初始化过程中 ContextHub 存储覆盖默认持久层时出现持久性问题。NPR-22479：适用于 CQ-4218399 的修补程序
* 如果沒有在第一個內容根勾選「包含子頁面」，含有多個頁面的啟動就不會將子頁面發佈至發佈伺服器。 NPR-22482：适用于 CQ-4237818 的修补程序
* （触屏 UI）通过经典 UI 控制台删除启动项会使所有页面无法编辑。NPR-22491：适用于 CQ-4225074 的修补程序
* 對話方塊中的額外空間導致影像元件出現問題。 NPR-22528：适用于 CQ-4238183 的修补程序
* 使用inlide模式開啟元件時，先前載入的外掛程式第二次不可見。 NPR-22591：适用于 CQ-4236850 的修补程序
* 删除嵌套启动项中的启动项，会导致子启动项变得孤立。NPR-22621；CQ-4202639的Hotfix
* （经典 UI Sidekick）当页面处于工作流锁定阶段时，“工作流”选项卡被禁用。NPR-22722：适用于 CQ-4237557 的修补程序
* 將新增至頁面上影像元件中的影像翻轉後，變更不會儲存，而原始影像會顯示在頁面上。 呈现支持已通过 [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141) 添加到图像核心组件。NPR-22801：适用于 CQ-4221539 的修补程序
* 當使用者嘗試從錨點選單中刪除現有錨點時，RTF編輯器元件視窗會關閉，且變更保持未儲存狀態。 NPR-22802：适用于 CQ-4238167 的修补程序
* Omnisearch篩選器未顯示Sites主控台中的所有動作。 NPR-22804：适用于 CQ-4239007 的修补程序
* 操作系统剪贴板以及内部 AEM 剪贴板的触屏 UI 中存在复制/粘贴问题。NPR-22807：适用于 CQ-4220383 的修补程序
* Lucene搜尋傳回的摘要醒目提示不一致。 NPR-22879：适用于 CQ-4238513 的修补程序
* 在發佈執行個體關閉的情況下啟動頁面會導致綠色狀態而不是變成琥珀色。 NPR-22927：适用于 CQ-4236310 的修补程序
* (StyleSystem) 从弹出窗口中选择样式时，屏幕位置会跳转。NPR-23183：适用于 CQ-4238867 的修补程序
* （管理发布）需要多次点击，方可移至日历的下个月。NPR-23508：适用于 CQ-4242732 的修补程序

### 平台 {#platform-2}

* Sling Exporter servlet無法正確匯出日文字元。 NPR-22153：适用于 CQ-4228920 的修补程序
* 啟動期間排程器鎖死。 NPR-22440：Sling-7004的Hotfix
* 无法在两个发布实例之间同步组。NPR-21943：适用于 Granite-19564 的修补程序
* org.apache.sling.i18n共用工作階段/資源解析器出現效能問題。 NPR-23390：Sling-7543的Hotfix

### 集成 {#integration-5}

* com.day.cq.analytics.sitecatalyst中無結尾標籤的ResourceResolver。 NPR-22323：适用于 CQ-4236515 的修补程序
* 長時間執行查詢期間，TargetContentImpl導致AEM變得緩慢。 NPR-22361：适用于 CQ-4236907 的修补程序
* 目標引擎(mbox.js、at.js)不會使用損毀的URL，而是使用包含冒號的URL，這可能會導致某些部署失敗。 NPR-22366：适用于 CQ-4237854 的修补程序
* 提供自訂at.js或mbox.js時，系統將include指令碼當作文字寫入頁面，而非HTML標籤。 NPR-22441：适用于 CQ-4203691 的修补程序
* 在「目標」模式中，作者不需取消繼承即可修改從Blueprint繼承的元件。 NPR-22751：适用于 CQ-4237907 的修补程序
* 由於遺失jcr：content節點，PersonalizationDataSource擲回Null指標例外狀況。 NPR-22850：适用于 CQ-4222122 的修补程序
* 使用非英語時，AEM鎖定目標失敗。 NPR-22917：适用于 CQ-4218213 的修补程序
* 發佈具有目標內容的頁面遺失相關資源。 NPR-23064：适用于 CQ-4227119 的修补程序
* 用户在 mbox 调用中看不到测试静态参数值，而在云配置中使用 AT.js 作为客户端库进行测试时，则可以看到这些值。NPR-21930：适用于 CQ-4234520 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-1}

* 取消勾選取消/停用繼承核取方塊後，iParsys會建立位置位移。 NPR-21905：适用于 CQ-4230951 的修补程序
* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-22327：适用于 CQ-4222853 的修补程序
* 为了提高安全性，已弃用 CAPTCHA 组件。如果您使用的是 CAPTCHA 组件，则在安装 6.3.2.1 或更高版本后，将显示“Captcha 组件已弃用，不应再使用”消息。可以自定义 AEM 组件来包含 reCAPTCHA 以提高安全性。NPR-22151：适用于 CQ-4220052 的修补程序

### WCM - 页面编辑器 {#wcm-page-editor}

* 使用无效选择器时导致反射型跨站点脚本攻击 (XSS)。适用于 CQ-4270397 的修补程序

### 翻译 {#translation-4}

* 调查预览功能存在的问题。NPR-22114：适用于 CQ-4223753 的修补程序

### 用户界面 {#user-interface-2}

* 設定「下限」和「上限」日期範圍時，Coral Calendar月份選擇器出現問題。 NPR-22716：适用于 CUI-7187 的修补程序
* （经典 UI）即使关联的表单数据模型服务设置为空字段，组件也会显示默认值。NPR-22272：适用于 GRANITE-19744 的修补程序

### Granite {#granite-2}

* 内存泄漏导致资产共享 AEM 发布者实例出现稳定性问题。NPR-22205、NPR-23178：Sling-5668、Sling-7292和Sling-7470的Hotfix。
* 不穩定的服務ID不應該用於工作階段屬性名稱。 NPR-22821：适用于 Granite-21059 的修补程序
* 当 http 白板管理的会话失效时，如果容器会话不含其他会话属性，则容器会话也将失效。NPR-23059：FELIX-5819的Hotfix
* 啟動時LogbackManager可能會遺漏某些OSGi設定。 NPR-23060：适用于 Granite-19791 的修补程序

### 商务 {#commerce-3}

* 啟用在體驗片段功能表中建立工作流程。 NPR-22347：适用于 CQ-4221661 的修补程序
* 體驗片段錯誤可在WeRetail上重現。 NPR-21958：适用于 CQ-4220061 的修补程序
* 啟用包含已刪除體驗片段的頁面會擲回NullPointerException。 NPR-23179：适用于 CQ-4239939 的修补程序

### 项目 {#projects}

* （多语言项目）项目不会列出超过 19 种语言的翻译作业。NPR-22498：适用于 CQ-4229978 的修补程序

### 工作流 {#workflow}

* （经典 UI）启用或禁用工作流启动器会导致不良行为。NPR-22907：适用于 CQ-4239153 的修补程序

## 表单 {#forms-9}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

AEM Forms的關鍵重點為：

* 新增對HTML5輸入型別的支援。
* 修正基本SOAP標頭驗證。
* 新增對超連結標題屬性的支援。
* 啟用Forms Designer協助工具樹狀結構中的PDF/UA識別碼。
* 为 Workbench 用户启用了证书身份验证。
* 新增對產生PDF/A-2a或PDF/A-3a相容PDF檔案的支援。

### Forms 附加组件包 {#forms-add-on-package-9}

#### 表单 - 管理员 UI {#forms-admin-ui}

* 檢查ECM聯結器設定頁面的密碼欄位時，密碼以純文字顯示。 NPR-22508：适用于 CQ-4236065 的修补程序

#### 表单服务 {#forms-service}

* 启用 SSL 后，“提交”和“放弃”事件不适用于表单分析。NPR-22637：适用于 CQ-4237973 的修补程序

#### 用户管理 {#user-management}

* 無法同步LDAP，因為cglib-nodep版本不正確。 NPR-22493：适用于 CQ-4234099 的修补程序

#### 自适应表单 {#adaptive-forms-2}

* 在调用函数后，规则编辑器的自定义函数添加一个额外的 ;，即使自定义函数返回 true，验证也会失败。NPR-22481：适用于 CQ-4235499 的修补程序
* 顯示驗證訊息最小值和最大值時，無論選取的日期模式為何，日期選擇器元件都不會依照該模式。 NPR-22444：适用于 CQ-4236269 的修补程序
* 提交請求中傳送的日期格式應與日期選擇器元件中提供的模式一致。 NPR-22384
* Android 6.0 Samsung裝置不遵循為最適化表單文字方塊指定的字元數上限。 NPR-22363、NPR-22364：适用于 CQ-4235205 的修补程序
* (Microsoft Edge) (IE 11) 具有多行字段的自适应表单文本字段组件显示“Null”作为默认值，而不是空白。NPR-22284：适用于 CQ-69107 的修补程序
* 最適化Forms中的SOAP UTF-8輸入編碼傳回錯誤並出現亂碼頁面。 NPR-20105：适用于 CQ-4222669 的修补程序
* 一旦在網站頁面中設定了錯誤的表單，AEM Forms容器元件就無法用於編輯。 适用于 CQ-4237456 的修补程序
* 在JEE伺服器上執行開發測試時失敗。 适用于 CQ-4222082 的修补程序
* 由於Calvin框架中的縮制問題，JEE伺服器上的AF測試失敗。 适用于 CQ-4217220 的修补程序

#### 表单管理器 {#forms-manager}

* (Firefox) 无法更新自适应表单的 XML 架构属性，因为记录文档 (DOR) 中的选项未在属性页面中预先选择。NPR-22298：适用于 CQ-4237402 的修补程序
* 發佈網站時，發佈頁面後修改過的Forms不會再發佈。 NPR-23013：适用于 CQ-4236566 的修补程序

#### 後端整合 {#backend-integration-1}

* SOAP服務的OOTB基本驗證無法用於FDM整合中的基本驗證。 NPR-23238：适用于 CQ-4241308 的修补程序

#### 通信管理 {#correspondence-management}

* 在信件内部使用并预览 OOTB XDP 时，会显示内容与页脚重叠。适用于 CQ-4212414 的修补程序

#### 汇编程序服务 {#assembler-service}

* 关于 PDF/A-1b 合规检查错误的 Acrobat DC 报告和 AEM 报告存在差异。NPR-22051、NPR-22050：适用于 CQ-4226128、CQ-4227671 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-8}

#### Workbench {#workbench}

* 为 Workbench 用户启用了证书身份验证。NPR-20644：适用于 CQ-4214486 的修补程序
* 使用Workbench下載伺服器記錄只能用於一部伺服器，而無法用於另一部伺服器。 NPR-21079：适用于 CQ-4229842 的修补程序

#### 进程管理 {#process-management-1}

* （HTML 工作区）滚动条存在屏幕大小问题。NPR-23288
* （HTML 工作区）进程起点未按字母数字顺序排序。NPR-22841：适用于 CQ-4238944 的修补程序
* （HTML 工作区）关闭工作区中的表单时触发“准备数据”。NPR-21127：适用于 CQ-4224574 的修补程序
* （HTML 工作区）调用的进程需要较长说明的注释时，“注释”展开按钮不起作用。适用于 CQ-4241488 的修补程序

#### 核心 {#core-1}

* 啟動排程器時啟動時發生錯誤。 NPR-22990
* 防止瀏覽器儲存輸入到HTML表單中的認證。 NPR-21762：适用于 CQ-4206543 的修补程序
* 應修正核心靜態程式碼分析中報告的問題。 适用于 CQ-104446 的修补程序

#### PDFG 服务 {#pdfg-service-3}

* PDF 生成器无法生成具有指定书签级别的 PDF 文档。NPR-22921、NPR-22285：适用于 CQ-4230562 的修补程序
* 新增對產生PDF/A-2a或PDF/A-3a相容PDF檔案的支援。 NPR-23021：适用于 CQ-4214172 的修补程序

#### Forms Designer {#forms-designer-1}

* 從Designer另存為PDF時遺失PDF/UA識別碼。 NPR-23137
* 從Designer另存為PDF時，沒有標籤路徑物件，例如邊框、底線和超連結。 NPR-23136
* 從Designer另存為PDF時，影像物件沒有邊界方框。 NPR-23134
* 從Designer另存為PDF時，在Designer中定義的內嵌超連結沒有受到標籤，也沒有替代文字。 NPR-23133
* 使用AEM 6.3 Forms Designer開啟XML Data Package時，會移除XML來源中的XHTML格式設定。 NPR-21178：LC-3917046的Hotfix

#### 安装 LCM {#install-lcm}

* 在安装程序和 LCM 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21370

#### 签名服务 {#signatures-service}

* 嘗試透過HSM以數位方式簽署/認證PDF檔案時，發生例外狀況。 NPR-21154：适用于 CQ-4226978 的修补程序

### 6.3.2.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-5}

AEM 6.3.2.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list_002_.txt)

AEM 6.3.2.1 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_comparison.txt)

AEM Cumulative Fix Pack 6.3.1.2為重要更新，包含自2017年10月正式發行AEM 6.3 Service Pack 1 (6.3.1.0)以來累積的多項內部及客戶修正。

AEM 累积修补程序包的主要功能亮点包括：

* 修改UI以支援在AEM Assets中實作CUG功能。
* 修正授權檢查頁面的UI問題，以獲得更好的體驗。
* 啟用AEM Forms應用程式中的OSGi工作流程任務支援。

### 资产 {#assets-10}

* 修改UI以支援在AEM Assets中實作CUG功能。 NPR-19485
* 使用触屏 UI 将资产上传为其自身的直接子节点会导致出现问题。资产会作为先前选定的资产的直接子级上传。NPR-19736
* 加载已保存的搜索/智能收藏集时，“日期范围”谓词和“范围”谓词不起作用。NPR-19844：适用于 CQ-4220808 的修补程序
* 将多个资产（超过 4 个）发布到 Brand Portal 时，AEM 实例运行缓慢。NPR-20009：适用于 CQ-4213426 的修补程序
* 无法从许可证检查页面下载带有空格的资产。NPR-20067：适用于 CQ-4216557 的修补程序
* 上传具有多个 Alpha 层的 PSB 文件时出现处理问题。NPR-20250：适用于 CQ-4220869 的修补程序
* 用户无法下载定义了长文件名和免责声明的资产。NPR-20254
* ProductAssetsUploader 将 Java 缓存的临时文件放在 Java TEMP 文件夹中。NPR-20256：适用于 CQ-4221801 的修补程序
* 由于许可问题，使用 Adobe 专有代码替换版本比较代码。NPR-20272：适用于 CQ-4223758 的修补程序
* 字符串属性 documentNumber 的元数据显示为日期，然而它应该是数字。NPR-20291：适用于 CQ-4223991 的修补程序
* 受损 PDF 的文本提取卡住。NPR-20416：适用于 CTG-4150375 的修补程序
* 无法正常下载其中包含具有 UTF-8 不兼容名称的资源的压缩文件。NPR-20420：适用于 CQ-4219961 的修补程序
* OmniSearch 中的字符过多导致 AEM 服务器崩溃。NPR-20434：适用于 CQ-4223602 的修补程序
* DAM 资产 API 元数据缺陷导致 xmp 回写 API 受损。NPR-20607：适用于 CQ-4220455 的修补程序
* 將使用者新增至集合時出現效能問題。 NPR-20699：适用于 CQ-4225733 的修补程序
* 对于 Dynamic Media 集，不应允许从 AEM 发布到 Brand Portal。NPR-20320：适用于 CQ-4221147 的修补程序
* 含有空格和重音符号的视频不会在“呈现版本”页面上生成任何视频。NPR-19961：适用于 CQ-4221014 的修补程序
* 解決Assets API的多個資料夾處理問題。 NPR-20569
* 雲端服務設定中的目的地路徑指向根路徑中的子資料夾時，AEM Dynamic Media Classic (前身為Scene7)無法從AEM伺服器同步資產。 CQ-4228265
* 已添加 Apache Commons `{org.apache.commons/commons-email/1.5}` 的电子邮件包，用于替换 `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`。

### 站点 {#sites-10}

* 管理員許可權問題：無法從頁面屬性中移除「已關閉的使用者群組」成員。 NPR-20631
* 透過「管理發布」發佈頁面時，輸入的工作流程名稱應該可在「通知」方塊中使用。 NPR-20046：适用于 CQ-4221586 的修补程序
* 在富文本编辑器中的两行上应用样式化文本，然后将它们合并为一个段落，会删除样式化跨区。NPR-20110：适用于 CQ-4223051 的修补程序
* 在“属性”编辑对话框的多个选项卡中对字段属性所做的更改有时不会保存。NPR-20286
* 内容片段中粘贴内容的末尾出现意外标记。NPR-20413：适用于 CQ-4224014 的修补程序
* 在 Adobe Campaign 中实施了一种机制，用于从外部定位资源中获取内容资源的策略。NPR-20667
* 富文本插件不适用于多字段触屏 UI 中的内嵌和全屏栏。NPR-20973

### 营销活动 {#campaign-1}

* 占位符在包含多个 Parsys 组件的页面中不可见。NPR-20436；CQ-4215000的Hotfix

### 商务 {#commerce-4}

* 體驗片段在Internet Explorer 11中無法正確顯示。 NPR-20161：适用于 CQ-4223319 的修补程序
* 在商务工作流中，当基于具有多个图像的主要产品创建变量时，会自动插入空白图像。NPR-20068：适用于 CQ-4222048 的修补程序
* 在產品控制檯的集合頁面上依標籤篩選的功能無法運作。 NPR-20292：适用于 CQ-4224023 的修补程序

### 社区 {#communities-8}

* searchresult元件的搜尋結果不一致。 NPR-20070：适用于 CQ-4220913 的修补程序
* 已發佈元件上與版主相關的任何活動都不會觸發電子郵件通知。 NPR-20122
* 系統會為匿名社群使用者顯示沒有結果的空白分頁。 NPR-20136：适用于 CQ-4220738 的修补程序
* 設定偵測到UGC為垃圾訊息或使用者在經預先稽核的網站上張貼內容時的警報觸發條件。 NPR-20274：适用于 CQ-96850 的修补程序
* 解决了 AEM Communities 站点页面中的多个问题，包括错误的重定向和页面刷新问题。NPR-20344
* CommunityUserOperationExtension發生類別轉換例外狀況。 NPR-20532：适用于 CQ-4224385 的修补程序
* 创建社区站点后，用户无法从站点地图中打开它，因为上下文路径未添加到 URL 前面。NPR-20730

### 集成 {#integration-6}

* 将 Analytics 现有凭证迁移到 WSSE 身份验证。NPR-19962：适用于 CQ-4218071 的修补程序
* 進行任何修改後重新啟用區段會失敗並擲回錯誤。 NPR-20054：适用于 CQ-4218401 的修补程序
* Search&amp;Promote 云服务配置忽略表单检索方法，导致其在创作实例上不可用。NPR-20447：适用于 CQ-4206076 的修补程序
* 安装 Search&amp;Promote 功能后，内容包中模糊不清的筛选器定义导致路径被覆盖。NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* 每次显示属性时，TXT 类型资产的元数据属性会显示在不同的元数据编辑器中。NPR-20239

### 平台 {#platform-3}

* 解决了资源解析程序未关闭的异常。NPR-19749：适用于 Granite-19143 的修补程序
* 请求在操作功能板中显示自定义卡片，以及默认的运行状况检查。NPR-20145
* 页面编辑器的注释层在 Internet Explorer 11 中无法正常工作。NPR-20222：适用于 CQ-4222818 的修补程序
* 在复制代理中将用户代理设置为管理员时出现会话泄漏。NPR-20578
* 沒有為其他data-sly-resource陳述式取消設定requestAttributes。 NPR-20639：适用于 4226206 的修补程序
* 修复了 AEM 中 OOTB 资产的 curl Head 请求问题。NPR-20781：适用于 CQ-4221520 的修补程序

### 项目 {#projects-1}

* 從專案控制檯存取不同專案需要較長時間載入。 NPR-20314
* 安裝AEM 6.3.0.1會移除dam-update-service使用者的金鑰存放區。 NPR-20018
* 在某些自訂部署中，使用者若嘗試在addTask模組中選取受託人，會花較長的時間填入使用者選取器中的清單。 NPR-20283：适用于 CQ-4224193 的修补程序

### 用户界面 {#user-interface-3}

* 無論對話方塊中的屬性為何，Colorfield皆設為「永遠必要」。 NPR-19702
* 在Internet Explorer 11上不會以全熒幕為多欄位元件顯示卷軸。 NPR-20261：适用于 CQ-4219782 的修补程序
* 如果触发连续查询导致不正确的结果，之前的查询不会被中止。NPR-20398：适用于 GRANITE-19306 的修补程序

### 工作流 {#workflow-1}

* 用户在其收件箱中收到工作流任务时，不会发出相关通知。NPR-20213：适用于 CQ-4221639 的修补程序
* 在单击工作流模型的对话框参与者步骤中的下拉列表后，OOTB Granite 用户选取器未加载任何用户。NPR-20236

## 表单 {#forms-10}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-10}

#### 自适应表单 {#adaptive-forms-3}

* 缺少对重复面板的整合表达式的支持。NPR-20861
* 即使關聯的表單資料模型服務未傳回值，下拉式清單仍會顯示最後儲存的值。 NPR-20710
* 無法在規則編輯器中編輯具有布林值限制的現有規則。 NPR-21128

#### 表單入口網站 {#form-portal}

* 即使自适应表单的资产类型不是 XDP，也会为其显示 HTML 配置文件。NPR-20079

#### 後端整合 {#backend-integration-2}

* 無法將切換元件的值設定為true/false。 NPR-21111

#### OSGI工作流程 {#osgi-workflow}

* 管理工作流提交仅列出十个应用程序。CQ-4230193

#### HTML5 表单 {#html-forms-3}

* 如果在辅助功能配置中未定义，则 XDP 表单对象（例如子表单）的名称会显示为其工具提示。NPR-20523

### Forms JEE 安装程序 {#forms-jee-installer-9}

#### 进程管理 {#process-management-2}

* FormSetPrefillApp 起点未预填充 AEM Forms 应用程序中的表单集字段。NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* 安装最新的 CTJPEG2K 库，以解决关键安全漏洞。这会影响 XMLFM（AEM 和 IfBA）、RM、PDFG 模块。NPR-20625：NPR-21337。

### 包含的功能包 {#feature-packs-included}

#### AEM Forms 应用程序 {#aem-forms-app}

* 啟用AEM Forms應用程式中的OSGi工作流程任務支援。 CQ-4222638

### 6.3.1.2 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-6}

AEM 6.3.1.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_3_1_2-bundle-list.txt)

AEM 6.3.1.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM 累积修补程序包 6.3.1.1 是一个重要更新，它包括自 2017 年 10 月 AEM 6.3 Service Pack 1 (6.3.1.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包的主要功能亮点包括：

* 为默认的元数据架构表单启用了“发布到 Brand Portal”操作。
* 对于将 dc: title 属性设置为 String []（多字段）的图像，在图像卡片上显示标题时发生行为更改。
* 以基礎時間元件取代伺服器端的時間轉譯。
* 啟用從標籤管理員/標籤控制檯將標籤從AEM發佈到Brand Portal的功能。
* 發佈JSON API以使用內容片段。
* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.5。

### 资产 {#assets-11}

* 將具有相同屬性的兩個欄位對應到不同屬性欄位型別時，系統擲回內部錯誤。 NPR-19462：CQ-4216828的HF
* dc： title和dc： description不會變更為crx /de中的多欄位值。 NPR-19570：CQ-4209086的HF
* Dynamic Viewer載入畫質最低的視訊轉譯，用於以製作模式測試視訊播放體驗。 NPR-19004
* 无法为名称中包含空格的资产下载动态呈现版本。NPR-19433：适用于 CQ-4211738 的修补程序
* 无法使用 Chrome 在列视图中加载页面/资产的完整列表。NPR-19566：适用于 CQ-4214248 的修补程序
* 选择任何架构、搜索 Facet 或预设时，“发布到 Brand Portal”选项不可用。NPR-19550
* 在欄檢視中選取資產並按一下編輯時，頁面傳回錯誤。 NPR-20301：适用于 CQ-4224052 的修补程序
* 跨越正時區和負時區時，資產到期顯示會關閉。 NPR-20329：适用于 CQ-4219333 的修补程序

### 营销活动 {#campaign-2}

* 为营销活动选择默认体验后，营销活动滑块组件未显示。NPR-19213

### 集成 {#integration-7}

* 透過匿名使用者存取時，自訂at.js檔案不會發佈。 NPR-19542：适用于 CQ-4219592 的修补程序
* 設定精靈中的目標定位引擎欄位設為ContextHub (AEM)而非Adobe Target。 NPR-19320：CQ-4218465的HF
* 建立體驗時對象區段損毀。 NPR-19110
* 如果对定位模块进行编辑并保存超过一次，则定位模式下不显示定位对话框。NPR-19144：适用于 CQ-4216708 的修补程序
* 在经典 UI 上的 Adobe Digital Publishing Solution 中，文章的访问属性设置不正确。NPR-19367
* 如果用户可以访问多个区域，通过 Campaign 个性化选件时，会出现自动折叠的错误行为。NPR-19290：适用于 CQ-4218029 的修补程序

### 站点 {#sites-11}

* 將執行個體升級為AEM 6.1SP2-CFP3後，由於Sidekick.js中的程式碼變更，系統沒有重新填入多複合欄位下拉式清單值。 NPR-19450：CQ-4194771的HF
* 在製作模式下，WCMMode.EDIT無法用於目標元件。 NPR-19387
* 發佈JSON API以使用內容片段。 NPR-19500
* 在作者對話方塊中，粗體、斜體、底線功能無法用於RTF編輯器欄位。 NPR-19670、NPR-19718：适用于 CQ-4219088 的修补程序

### Mobile On-Demand {#mobile-on-demand-1}

* 由于使用全尺寸图像导致呈现过程缓慢，AEM 文章控制台出现呈现问题。NPR-19088

### 翻译 {#translation-5}

* 無法為翻譯專案產生預覽。 NPR-19289

### 安全 {#security}

* SSL 连接错误。无法与服务器建立安全连接。NPR-19628

### 社区 {#communities-9}

* 透過預先稽核的網站發佈內容時會觸發郵件。 NPR-20008
* 已發佈元件上與版主相關的任何活動都無法使用電子郵件通知。 NPR-19767：CQ-4218060的HF

### 平台 {#platform-4}

* AEM 生产服务器部署存在稳定性问题。NPR-19707
* 升级到 AEM 6.3 后，未找到引用作为脚本实施的标记的自定义 taglib。NPR-19087
* AEM 6.3.1 的 HTL 错误修复。NPR-19161
* 富文本字段在多字段组件中不可编辑。NPR-19604：适用于 Granite-16755 的修补程序
* Adobe 电子邮件模板服务会将标记添加到自定义用户模板。NPR-19190
* 适用于 Oak 1.6.5 的修补程序。NPR-19148

### 商务 {#commerce-5}

* 選取XF變數編輯器後，「開始工作流程」按鈕無效。 NPR-19642：适用于 CQ-4207796 的修补程序

### 项目 {#projects-2}

* 项目编辑者无法将资产复制/粘贴到项目资产文件夹中。NPR-19619: 适用于 CQ-4215321 的修补程序

### 网站内容管理 {#web-content-management}

* 在「轉出」畫面中，無法核取或取消核取與LiveCopy頁面對應的核取方塊。 NPR-19518
* 大量編輯頁面屬性無法正確使用，因為目前所有索引標籤和欄位都可供大量編輯。 NPR-19451
* 在傳統UI中編輯影像時，OOTB屬性和影像對齊方式屬性未出現。 NPR-19488：CQ-4217914的HF

### 用户界面 {#user-interface-4}

* 使用Google Chrome瀏覽器時，使用者無法在觸控式UI中使用欄檢視來載入頁面/資產的完整清單。 NPR-19566：适用于 CQ-4214248 的修补程序

### Brand Portal {#brand-portal-1}

* 無法從AEM發佈含有註解和附註的資產。 NPR-19590：适用于 CQ-4218386 的修补程序
* 启用通过 tagadmin/tagging 控制台将标记从 AEM 发布到 Brand Portal 的功能。NPR-20271：适用于 CQ-4223948 的修补程序
* 修正Brand Portal cloudservice設定UI上的「已啟用」欄位。 适用于 CQ-4211101 的修补程序
* 搜尋表單復寫失敗。 适用于 CQ-4220080 的修补程序

## 表单 {#forms-11}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-11}

#### 自适应表单 {#adaptive-forms-4}

* 提交至JEE工作流程沒有從JEE端傳回輸出引數至AEM，並擲回「因為值非原始值而忽略」錯誤。 NPR-20265
* 最適化Forms不允許PDF作為Safari中的附件。 NPR-19625
* RestoreGuideState會覆寫customcontextproperty對應。 CQ-4222877
* 使用Cloud Service設定Google reCaptcha時，在需要org.apache.http.proxyconfigurator設定以進行外部連線的環境中，POST呼叫似乎不會通過PROXY。 NPR-20454
* 安裝時以XSD結構描述為基礎的最適化Forms會針對數值欄位提交有問題的XML值，且語言環境有非「」的小數分隔符號。 从而导致出现错误。NPR-20444
* 向第三方服务器发出 HTTP 请求时，不接受为“Apache HTTP 组件代理配置”设置的代理设置。使用 HTTP GET 或 POST 调用时出现连接超时问题。NPR-20457、NPR-20456、NPR-20455、NPR-20451

#### 表单数据集成 {#forms-data-integration}

* 針對非英文地區設定，作為SOAP服務輸出的UTF-8字元未正確複製到最適化Forms欄位中。 NPR-20238：NPR-20103

#### 通信管理 {#correspondence-management-1}

* 在文字編輯器中，從Word檔案複製貼上內容會失去其內容顏色和字型。 NPR-19521

#### 組合器服務 {#assembler-services}

* 在對PDFA-1b格式的檔案進行合規性驗證期間，Acrobat和AEM的結果不一致。 NPR-19280

#### 工作流 {#workflow-2}

* 允許http呼叫透過Proxy連線的工作流程簽署步驟。 NPR-20529

#### HTML5 表单 {#html-forms-4}

* 新增對preSubmit事件的支援。 NPR-20604

### Forms JEE 安装程序 {#forms-jee-installer-10}

#### 进程管理 {#process-management-3}

* 将表单最大化/最小化并将其另存为草稿或转发后，工作流“附件”、“注释”和“详细信息”选项卡在工作区中无法使用。NPR-20243
* 在HTML工作區中提交資料後，多行文字欄位(TextArea)未保留文字中的新行字元或分行符號。 NPR-20085

#### 程式報告 {#process-reporting}

* 由於Null指標例外狀況，程式報告無法正確擷取資料。 NPR-19759

>[!NOTE]
>
>安裝中列出的LiveCycle內巢狀件 [AEM Forms發行版本](aem-forms-releases.md) 文章以修正此問題。

#### 標準服務 {#standard-services}

* docConvertor 不支持 PDF 中的拼合透明度，且无法生成 PDF/A。NPR-16228：适用于 CQ-4214488 的修补程序

#### 核心 {#core-2}

* 當JBoss應用程式上以叢集設定執行的AEM Forms伺服器停止時，應用程式伺服器會中斷與資料庫的連線。 這可能會導致資料損毀問題。 NPR-19724

### 包含的功能包 {#feature-packs-included-1}

* 下拉式中繼資料結構欄位無法設為必要，因為資產缺少必要欄位驗證。 NPR-17882：CQ-4208373的FP

### 6.3.1.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-7}

AEM CFP 6.3.1.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list.txt)

AEM CFP 6.3.1.1 中包含的内容包列表

[获取文件](assets/do-not-localize/content-package-list.txt)

AEM 累积修补程序包 6.3.0.2 是一个重要更新，它包括自 2017 年 4 月 AEM 6.3 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包的主要功能亮点包括：

* 使用者存取控制的可稽核性
* 包含內建存放庫1.6.2版(Apache Jackrabbit Oak)
* 解決無結尾標籤的資源解析器問題
* 簡化智慧內容服務的設定
* 解決內容片段驗證問題
* 改善混合裝置上中繼資料結構的可編輯性
* 解決即時副本中的元件層級同步問題
* 改善欄檢視中大量內容頁面的可用性
* 改善長標題頁面對頁面命名慣例的合規性
* 改善觸控式UI上的促銷活動個人化體驗
* 修正多項專案覆蓋問題

### 平台 {#platform-5}

* 适用于 Oak 1.6.2 的修补程序。NPR-16993
* 使用篩選器開啟Omnisearch時，路徑不再設定。 NPR-17398：适用于 CQ-4204870 的修补程序
* 要求AEM中使用者許可權變更具有可稽核性。 NPR-17061
* 延遲連線至DMCloud Services造成「開啟的檔案過多」例外狀況。 CQ-4211407

### 资产 {#assets-12}

* 使用不同選項設定智慧內容服務時出現可用性問題。 NPR-18200：适用于 CQ-4201557 的修补程序
* 二進位資料流中的資源洩漏至S3資料存放區。 NPR-18041：适用于 CQ-4209506 的修补程序
* 將ASCII/UTF-8編碼文字檔案上傳至AEM Assets時發生錯誤，且產生縮圖失敗。 NPR-18006：适用于 CQ-4209345 的 CFP
* 預設中繼資料結構導致內容片段驗證失敗。 NPR-17769：适用于 CQ-4211111 的修补程序
* com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner中無結尾標籤的資源解析器。 NPR-17598：适用于 CQ-4209018 的 CFP
* 請求建立多個復寫代理以用於將資產發佈到Brand Portal。 NPR-17189
* 日文語言資料夾下的資產稽核任務無法運作。 CQ-4204782
* 將資產從其屬性頁面移動時，會發生Null指標例外狀況。 CQ-4204251
* 如果連結至InDesign檔案多次，AEM就無法追蹤屬性頁面中資產的後續參照。 CQ-4204186
* 在混合裝置上使用Chrome編輯中繼資料結構表單時，在該表單中新增索引標籤時發生問題。 CQ-4201810
* 上傳重複資產時，（刪除/保留）選項會套用至所有資產，即使未在偵測到重複專案的對話方塊中選取該選項亦然。 CQ-4201673
* 當資產資料夾中有超過150傳入的參考移動時，會引發Null指標例外狀況。 CQ-4200981
* 對於已下載的資產資料夾，如果在解壓縮ZIP檔案的內容時發生衝突，預設選項會顯示為「建立版本」而不是「保留兩者」。 CQ-97800
* 擁有應用程式唯讀許可權的使用者無法從AEM Mobile內容管理預覽內容。 NPR-17486：适用于 CQ-4209690 的 CFP
* 「目錄」主控台的欄檢視中，「建立目錄」按鈕無法運作。 CQ-4209952

### 站点 {#sites-12}

* 透過data-sly-resource屬性內嵌影像/視訊元件時發生問題。 NPR-18182：适用于 CQ-4212100 的 CFP
* 在 LiveCopy 中重新应用继承时，修改后的本地化组件无法恢复为原始形式。NPR-18172：适用于 CQ-4211379 的修补程序
* 在觸控式UI中以欄檢視導覽含有大量內容的頁面時發生問題。 NPR-17799：适用于 CQ-4199611 的修补程序
* `com.day.cq.wcm.core.impl.VersionManagerImpl` 中的资源解析程序未关闭。NPR-17789：适用于 CQ-4211152 的 CFP
* 長頁面標題沒有依照慣例產生頁面名稱。 NPR-17633：适用于 CQ-4209056 的修补程序
* 在部署於Jboss EAP 6.4上的AEM 6.3中，在觸控式UI上建立頁面時出現問題。NPR-17589：CQ-4210137的Hotfix
* 巢狀群組存在時，工作流程狀態提供者會導致執行個體鎖定。 NPR-17556：CQ-4202056的CFP請求
* 以下对象中的资源解析程序未关闭：

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497：适用于 CQ-4208673 的 CFP
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495：适用于 CQ-4208668 的 CFP
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494：适用于 CQ-4208669 的 CFP
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493：适用于 GRANITE-17404 的 CFP

### 集成 {#integrations-1}

* 解决了在 AEM Day HTTP Client 3.1 OSGi 配置了需要摘要身份验证的代理时可能发生的 AEM 搜索组件错误。NPR-18128：适用于 NPR-18029 的修补程序
* 透過傳統UI個人化行銷活動和相關體驗時發生問題。 NPR-18127：适用于 CQ-4211559 的修补程序
* 將品牌/區域設定為網站的根頁面時，一旦取消繼承，就無法再為子頁面中的區域還原。 NPR-17753：适用于 CQ-4210139 的修补程序

### 工作流 {#workflow-3}

* 在非暫時性工作流程中，在外部程式步驟之前進行的程式歷史記錄和中繼資料變更不會持續存在。 NPR-17848：适用于 GRANITE-17757 的修补程序
* 工作流程對話方塊欄位的值未保留在工作專案節點中。 NPR-17734：适用于 CQ-4210369 的修补程序
* 從收件匣編輯任務時發生無法剖析的日期錯誤。 CQ-4208749

### 项目 {#projects-3}

* 修正多項專案覆蓋問題。 NPR-17733
* 重新建構專案模組中的Pod會降低其可設定性。 CQ-4209859
* 將頁面新增至翻譯工作時，資產路徑會變更為個別本地化網站。 CQ-4206007

### 安全 {#security-1}

* 上传 LDAP 用户的头像图像时出现问题。NPR-16561
* 请求使用 Apache Sling API 中的升级版 org.apache.sling.servlets.post servlet (2.3.22) 来预先制止 XSS 漏洞。NPR-18963

## 表单 {#forms-12}

AEM Forms 修补程序通过随发行版一起提供的 Forms 附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

AEM Forms的關鍵重點為：

* 通訊管理文字模組、信函預覽和以程式設計方式啟動建立通訊管理UI的修正。
* 修复了 PDF/A-1b 验证、将大型图像文件转换为 PDF，以及 PDF 生成器中的日语 PDF 文档的问题。
* 修复了通信管理、文档安全和论坛工作流的可用性问题。
* 添加了对捕获潦草签名字段的审核事件的支持。

### Forms 附加组件包 {#forms-add-on-package-12}

**通信管理**

* 在编辑通信管理片段时，文本编辑器显示内嵌条件以及已处理的文本。CQ-4211930
* 建立通訊管理信函時，信函的說明未儲存。 NPR-18089
* 專案符號清單上下方的額外邊界可在文字編輯器中看到，但在HTML和PDF轉譯中看不到。 NPR-18126
* 當HTML提交使用POST方法時，建立通訊UI無法啟動。 NPR-18202
* 當文字模組已儲存，且文字模組中的運算式不包含開頭或結尾運算式標籤時，未顯示錯誤訊息。 文字模組顯示錯誤訊息，且無法在信函中轉譯。 NPR-18535
* 新增內容或按下Enter鍵時，div標籤會新增至文字模組。 NPR-18240

**組合器**

* 驗證PDF檔案以符合PDF/A-1b規範時，AEM Forms傳回驗證錯誤：PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED。 使用PDF預檢和協力廠商軟體驗證時，Adobe檔案未傳回錯誤。 NPR-18011
* 驗證PDF檔案以符合PDF/A-1b規範時，AEM Forms傳回驗證錯誤：表單欄位有多個外觀。 PDF檔案符合PDF/A-1b標準。 NPR-18013

**監看資料夾**

* 選擇使用工作流程處理檔案時，在建立監看資料夾時，工作流程模型選擇下拉式清單顯示為被截斷。 NPR-17566

**HTML5 表单**

* AEM Forms不會擷取手寫簽名欄位的稽核事件。 NPR-15286

**Forms Manger**

* AEM Forms UI會以最舊的資產第一順序列出所有資產。 使用者無法以最新的順序將資產重新排序。 NPR-18450

**Java API參考**

为 com.adobe.livecycle.content 类添加了 JavaDocs。NPR-18468

### Forms JEE 安装程序 {#forms-jee-installer-11}

**PDF產生器**

* PDF產生器服務無法將大於100 MB的影像轉換為PDF檔案。 Ref# CQ-4208628
* 搭配日文OCR使用PDF產生器服務時，會產生反轉PDF。 NPR-17602

**进程管理**

* AEM Forms處理序未填入TaskContext變數。 NPR-18199

**文档安全**

* Microsoft Excel和Microsoft PowerPoint需要更長的時間來開啟受Microsoft Office適用的AEM Document Security Extension保護的檔案。 CQ-4212358
* 建立新原則且名稱與現有原則相同時，會發生內部伺服器錯誤。 NPR-18247

## 包含的功能包 {#feature-packs-included-2}

* 要求AEM中使用者許可權變更具有可稽核性。 NPR-17061

AEM 累积修补程序包 6.3.0.1 是一个重要更新，它包括自 2017 年 4 月 AEM 6.3 正式发布以来的若干内部修补程序和客户修补程序。AEM 累积修补程序包的主要功能亮点包括：

* 改进了以下方面：

   * 内容片段、站点编辑器、富文本编辑器、规则编辑器以及模板编辑器组件
   * 社交审核和 Facebook 社交登录
   * 配置和启动翻译作业
   * 在社交社区中访问通知的响应时间
   * 在 DAM 存储库中显示审核任务

* 在包管理器中提供验证选项，以检测叠加与 CFP 之间的冲突

## 通过 Software Distribution 下载 CFP 说明 {#download-instructions-for-cfp-via-package-share}

您可以直接从 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html) 下载 CFP 包，或者执行以下步骤：

1. 打开 [Software Distribution](https://experience.adobe.com/downloads)。您需要 Adobe ID 才能登录 Software Distribution。
1. 点按标题菜单中的 **[!UICONTROL Adobe Experience Manager]**。
1. 点按包名称，选择&#x200B;**[!UICONTROL 接受 EULA 条款]**，然后点按&#x200B;**[!UICONTROL 下载]**。

## 安装说明 {#installation-instructions}

此部分将向您介绍安装 CFP 的要求和步骤。

### 安装之前 {#before-you-install}

>[!NOTE]
>
>Adobe 提供的可选功能包依赖于发行版本和累积修订包。如果您已安装功能包，请联系 [AEM 客户关怀团队](https://helpx.adobe.com/cn/marketing-cloud/contact-support.html)以验证与 AEM 6.3 的累积修补程序包的兼容性。

>[!NOTE]
>
>我们建议您先对每个新的安装包运行验证，然后再尝试安装。预验证会分析并报告安装之前发现的任何错误，并主动向用户发出有关此类错误的警告。
>
>您可以访问相关文档以了解“验证”选项，网址为：[https://docs.adobe.com/content/docs/cn/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/cn/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* AEM 6.3.3.0 是安装 CFP 的先决条件。请访问[升级文档](https://docs.adobe.com/docs/cn/aem/6-3/deploy/upgrade.html)以了解关于将 AEM 安装升级至 AEM 6.3 的详细说明。
* 对于使用 RDBMK 或 MongoDB 的群集部署，可以在使用包管理器的任何创作实例上安装 CFP 包。
* 在安装累积修订包之前，请确保拍摄快照或备份您的 AEM 实例。
* 不支援解除安裝CFP。

### 新增記錄器 {#adding-new-loggers}

要配置调试级别日志记录并在 SP/CFP 安装期间检索活动日志，您可以按照以下步骤操作：

* 您可以在默认位置 [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) 添加新的日志记录器，该日志记录器具有以下属性：

   * 日志级别：调试
   * 加總： false
   * 記錄檔：logs/activity.log
   * 日志记录器：org.apache.jackrabbit.vault.packaging.impl.ActivityLog

将在 crx -quickstart /logs 文件夹中创建 activity.log。

### 通过 Software Distribution 安装累积修补程序包 {#install-the-cumulative-fix-pack-via-package-share}

执行以下步骤以在现有 AEM 6.3 实例上安装累积修补程序包：

1. 单击 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) 链接以下载包。

1. 打开[包管理器](http://localhost:4502/crx/packmgr/index.jsp)，并单击&#x200B;**[!UICONTROL 上传包]**&#x200B;以上传包。

1. 选择包名称，然后单击&#x200B;**[!UICONTROL 安装]**。

### 自动安装 {#automatic-installation}

可以通过以下方式将 CFP 自动安装到正在运行的实例中：

* 在服务器运行时，将包放入 `../crx-quickstart/install` 中。包会自动进行安装。
* 使用[包管理器中的 HTTP API](https://helpx.adobe.com/cn/experience-manager/6-3/sites/administering/using/package-manager.html) – 确保使用 `cmd=install&recursive=true` – 这会安装嵌套包。

### 验证安装 {#validate-installation}

1. “产品信息”页面 (`/system/console/  productinfo`) 此时应在“已安装的产品”下显示更新的版本字符串“Adobe Experience Manager，版本 6.3.3.8”。
1. 所有 OSGi 包在 OSGi 控制台中均为“活动”或“片段”（使用 Web 控制台：`/system/console/bundles`）。

>[!NOTE]
>
>成功安装包后，错误日志中会显示一条信息性消息，指示已成功安装内容包，例如“已成功安装内容包 **AEM-6.3.3-Cumulative-Fix-Pack-7**”。

>[!NOTE]
>
>自 AEM 6.3.3.1 起，对于大多数消息，Jackrabbit FileVault 中的日志级别已从“信息”更改为“调试”。要获取在 AEM 6.3.3.1 或更高版本上安装的内容包的安装日志，请为 org.apache.jackrabbit.vault.packaging.impl 启用“调试”日志级别。

### 安装 AEM Forms {#install-aem-forms}

>[!NOTE]
>
>如果您沒有使用AEM Forms，請略過本節。

#### 安裝AEM Forms附加元件 {#install-forms}

1. 确保您已安装 AEM 6.3.3.x CFP 包。
1. 下载适用于您的操作系统的 [AEM Forms 发行版](aem-forms-releases.md)中列出的相应 Forms 附加组件包。
1. 按照[安装 AEM Forms 附加组件包](https://helpx.adobe.com/cn/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html)中的所述安装 Forms 附加组件包。

#### 安装 AEM Forms JEE 包 {#install-aem-forms-jee-bundles-package}

AEM Forms JEE中的修正是透過單獨的安裝程式提供。 如需有關在JEE版AEM Forms上安裝CFP的資訊，請參閱 [在AEM Forms JEE上安裝CFP](install-cfp-aem-forms-jee.md).

#### Forms Designer安裝程式 {#designer-installer}

1. 要安装更新，请运行 Designer 6.2.0_&lt;语言>_Cumulative_QF.msp 文件。
1. 在歡迎畫面上，按一下 **更新**. 安裝隨即開始。
1. 安裝完成後，按一下 **完成**.

## AEM Forms JEE (JBoss EAP)的組態設定 {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>如果您要安裝6.3.3.0或更新版本，請執行以下程式來設定JBoss應用程式伺服器的設定。 如果您要在Oracle WebLogic或IBM WebSpehere應用程式伺服器上執行的AEM Forms伺服器上安裝6.3.3.0，則不需要進行額外設定。 有关更多详细信息，请参阅 [AEM 6.3.3.0 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

## Search&amp;Promote 集成的配置更新 {#configuration-updates-for-search-promote-integration}

如果安装的是 AEM 累积修补程序包 6.3.0.2 及更高版本，则用于 Search&amp;Promote 集成的 OSGi 配置是 **Apache HTTP 组件代理配置**。不再使用 Day Commons HTTP Client 3.1 中的代理配置。

## 已知问题 {#known-issues}

* 在 AEM CFP 6.3.3.x 的安装过程中可能会出现以下错误和警告，这些错误和警告可以安全忽略：

   * &#42;警告&#42; [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependencies.jar擲回執行階段例外狀況。
   * &#42;錯誤&#42; [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] 等待登入變更完成解除登入逾時。 CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver 服务缺失，无法发送服务请求，发送状态 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource：无法检查资源 [/bin/receive]，页面管理器不可用
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver：呼叫錯誤處理常式導致錯誤
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver原始錯誤null
   * org.apache.sling.engine.impl.DefaultErrorHandler錯誤處理常式失敗：java.io.IOException
   * &#42;錯誤&#42; [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent錯誤(org.osgi.framework.ServiceException：服務工廠傳回null。 （组件：com.day.cq.dam.handler.standard.ps.PostScriptHandler）)

**Brand Portal**

* 自6.3.1.2起，已移除智慧型集合的「發佈至Brand Portal」按鈕。

**用户界面**

>[!NOTE]
>
>若您受到這兩個問題其中任何一個的影響，請聯絡 [AEM客戶服務](https://helpx.adobe.com/cn/marketing-cloud/contact-support.html).

* 由于管理员搜索功能中存在大量请求，观察到 CPU 使用率很高。NPR-24229
* 重新開啟元件時，沒有在pathBrowser中選取PathField。 NPR-24177

## NPR-27692 所需的配置设置 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>此配置设置适用于 CFP 6.3.3.2 及更高版本。它将指导您更新 `sling` .properties 文件中的启动委托属性。

要手动更新 adobe- livecycle - cq -author.ear/ cq .war 中的更改，请按以下所述步骤操作：

* 停止AEM伺服器。
* 前往adobe-livecycle-cq-author.ear/cq.war
* 開啟adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml進行編輯：

   * 将 **sling.bootdelegation.ibm** 参数名称值更新为：

      * com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * 進行上述變更後，init-param看起來應該像這樣：

      * &lt;init-param>\
         &lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* 从 Websphere 应用程序服务器中卸载之前的企业存档 (EAR) 文件，并按照 [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf) 的第 10.2 节中的步骤来安装更新后的 EAR 文件
* 保存文件并重新启动服务器。[https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## NPR-23208 所需的配置设置 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>此配置设置适用于 6.3.2.2 及更高版本。它会指导您通过 CRX-DE 手动更新访问控制列表 (ACL) 策略，因为 ACL 由于“merge_preserve”acHandling 无法通过 CFP 安装进行更新。

**手動新增ACL原則的說明檔案**

若要更新ACL原則，請透過CRX-DE新增以下存取控制：

`1)` 路径：“/content”\
`a)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
Restrictions ： rep：glob=&quot;/&#42;/jcr：content&quot;\
`b)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
Restrictions ： rep：glob=&quot;/&#42;/jcr：content/&#42;&quot;

`2)` 路径：“/content/usergenerated”\
`a)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:write

`3)` 路径：“/etc”\
`a)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
Restrictions ： rep：glob=&quot;/&#42;/jcr：content&quot;\
`b)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
Restrictions ： rep：glob=&quot;/&#42;/jcr：content/&#42;&quot;

## NPR-19450 所需的配置设置 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>此配置设置适用于 CFP 6.3.1.1 及更高版本。

**配置属性 CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL。**

该属性可控制页面 ` /  jcr   :content` 节点下节点子树的最大深度，在达到该深度之前，存储库中存在的节点将用于获取页面属性。此屬性中位於指定深度以下的任何節點都會被忽略。

默认值为 1。此值可由覆蓋檔案constants.js (`/libs/cq/ui/widgets/source/constants.js`)取消註解CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL屬性並指派所需值（頁面/ jcr ：content底下的深度上限，系統會儲存到該深度為止的頁面屬性資料）。

**如果用户需要创建多个页面变量，以使页面 / jcr :content 节点下的节点数大于 1000，请使用以下步骤进行配置更改：**

* 配置 Apache Sling 的属性 JSON MaxResults
* 使用 `/system/console/  configMgr` 获取 Servlet
* 将其值设置为大于 > 1000（这是当前的默认值）的数字，以使该数字大于在达到上面配置的深度之前 / jcr :content 子树中存在的节点总数。

这使 Sling GET Servlet 能够返回所有必需的节点。

## Uber Jar {#uber-jar}

适用于 6.3.3.8 的 Uber Jar 可在 [Adobe 公共 Maven 存储库](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/)中获取。

要在 Maven 项目中使用 Uber Jar，请参阅[如何使用 Uber Jar](https://helpx.adobe.com/cn/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) 一文，并在项目 POM 中包含以下依赖项：

```TXT
<dependency>
      <groupId>com.adobe.aem</groupId>
      <artifactId>uber-jar</artifactId>
      <version>6.3.3.8</version>
      <classifier>apis</classifier>
      <scope>provided</scope>
</dependency>
```

## 已移除/已弃用功能 {#deprecated}

此部分列出了 AEM 6.3 中已移除或已弃用的功能和特性。

| 区域 | 专题 | 替换 | 版本号 |
|----|-----|-----|-----|
| Assets與Adobe Creative Cloud整合 | AEM 6.2 中引入了 [AEM 到 Creative Cloud 的文件夹共享](https://helpx.adobe.com/cn/experience-manager/6-3/sites/administering/using/creative-cloud.html)功能，以便创意用户可以从 AEM 访问资产。Creative Cloud應用程式推出的新功能Adobe Asset Link提供更優異的使用者體驗，以及更強大的存取功能，可直接從Photoshop、InDesign和Illustrator中存取AEM的資產。<br /> Adobe將不會對資料夾共用功能提供進一步的增強功能。 雖然此功能包含在AEM中，但強烈建議使用替代功能。 | Adobe資產連結或案頭應用程式。 如需詳細資訊，請參閱 [AEMCreative Cloud整合](https://helpx.adobe.com/cn/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html) 文章。 | AEM 6.3.3.x |

## 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-1}

以下文本文档列出了 CFP 中包含的 OSGi 包和内容包。

* [AEM 6.3.3.8 中包含的 OSGi 包列表](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [AEM 6.3.3.8 中包含的内容包列表](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM 发行版和更新](https://helpx.adobe.com/cn/experience-manager/aem-releases-updates.html)
>* [AEM 6.3 修补程序页面](https://helpx.adobe.com/cn/experience-manager/kb/aem63-available-hotfixes.html)
>* [AEM 6.3 发行说明](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [AEM 产品页面](http://www.adobe.com/cn/solutions/web-experience-management.html)
>* [AEM 6.3 文档](https://docs.adobe.com/content/docs/cn/aem/6-3.html)
>* 订阅 [Adobe 产品更新早知道](https://www.adobe.com/cn/subscription/priority-product-update.html)

