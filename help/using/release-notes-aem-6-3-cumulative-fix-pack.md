---
title: AEM 6.3 累积修订包
description: AEM 6.3 累积修订包发行说明。
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
source-git-commit: 53803f61394144ed81367a5c050814223fc6d565
workflow-type: tm+mt
source-wordcount: '17347'
ht-degree: 73%

---

# AEM 6.3 累积修订包发行说明 {#release-notes-aem-cumulative-fix-pack}

## 发行版信息 {#release-information}

| **产品** | Adobe Experience Manager |
|---|---|
| **版本号** | 6.3 |
| **发行版本** | [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) 上的累积修订包 6.3.3.8 |
| **先决条件** | [AEM 6.3 服务包 3 (6.3.3.0)](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **正式发布** | 2020 年 3 月 5 日 |

### 累积修订包 {#cumulative-fix-pack}

Adobe 引入了统一交付模式，用于发布修补程序。现在，Adobe 每月会发布一个累积修订包 (CFP)（需通过质量检查），而不是针对个别问题发布修补程序。CFP 是指多个修补程序的汇总内容包。CFP 主要包括错误修复，但也可能包括功能包。与单个修补程序发行版相比，CFP 具有以下优点：

* 本质上是累积的（例如，CFP 包含以前 CFP 已交付的修补程序）
* 提高了质量保证
* 简化了安装（用户将 CFP 安装为一个不含任何依赖关系的包，最新的服务包除外）

有关 CFP 和其他发行版类型的更多信息，请参阅[维护版本发行方式定义](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)。

## 关于此发行版 {#about-the-release}

AEM 累积修订包 6.3.3.8 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.8 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 的发行说明。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.20。

>[!CAUTION]
>
>在没有验证已安装功能包之间的兼容性的情况下应用CFP，可能会导致系统故障或自定义配置丢失，这些问题可能需要从备份还原才能解决。

>[!NOTE]
>
>对于版本低于 6.3.3.0 的 AEM 实例，如果客户的 AEM 实例中具有大量用户，则 Adobe 建议通过安装文件夹来部署 SP/CFP。

>[!NOTE]
>
>从 AEM 版本 6.3.3.1 开始，支持 MongoDB Enterprise 3.6。

## 问题列表 {#changes}

此部分列出了当前 CFP 中包含的所有问题和修补程序。

此外，此 CFP 还包含[以前的累积修订包](#previous)交付的修补程序。

### 资源 {#assets}

* 向收藏集添加资产时，“添加到收藏集”页面不会在卡片视图中显示所有可用的收藏集(NPR-32537)。

### Sites {#sites}

* 选择一个 Parsys 及其中包含的某个组件后，如果使用键盘快捷键删除这两个选定项目，此操作会同时删除该组件及其父 Parsys (NPR-32071)。
* 保存页面属性时，会创建一个不正确的节点 (NPR-31774)。

### 集成 {#integrations}

* ReportSuitesServlet 容易遭受服务器端请求伪造 (SSRF) 攻击 (NPR-32162)。

### 营销活动定位 {#campaign-targeting}

* 在创作实例中更改了某个组件的内容，但在重新启动该组件之前，激活的内容在Publish实例中不可见&#x200B;**com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489和NPR-32232)。
* Context Hub 性能在发布时崩溃 (NPR-31170)。

### Brand Portal {#brand-portal}

* Adobe Developer 未与 Adobe Experience Manager 6.3 集成以用于 Brand Portal (NPR-32056)。

### 表单 {#forms}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

#### Forms 附加组件包 {#forms-add-on-package}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM 服务包和累积修订包保持一致。因此，请务必在安装任意AEM Service Pack、累积修补程序包或功能包之后安装AEM Forms附加组件包。

* Designer：如果已启用标记选项，则生成的 PDF 输出文件中的子表单边框将消失（NPR-32324 和 NPR-32545）。
* Designer：如果表中存在合并的单元格，则对使用输出服务从 XDP 表单转换而来的输出 PDF 文件进行的可访问性测试将失败 (NPR-32068)。
* 文档安全：将 `DisableGlobalOfflineSynchronizationData` 选项设置为 `True` 后，无法在脱机状态下打开受保护的 PDF 文件 (NPR-32080)。

**6.3.0-0047 中修复的问题**

* （仅限 JEE）针对 Apache `Log4j2` 报告的严重安全漏洞（CVE-2021-44228 和 CVE-2021-45046）。

## 以前的累积修订包中包含的修补程序和功能包 {#previous}

### 累积修订包 6.3.3.7 {#cumulative-fix-pack-1}

AEM 累积修订包 6.3.3.7 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.7 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 的发行说明。

### 资源 {#assets-1}

* 在从“仅内容”下拉列表中选择筛选器选项，然后选择移动选项之前已选择Assets（在触屏UI的列视图中），也会移动(NPR-30693)。
* 处理工作流时，`${extension}` 变量未呈现在创作实例中 (NPR-31694)。
* 为 Dynamic Media 混合模式配置的到期时间（客户端缓存有效时间）值没有复制到 Dynamic Media 交付环境 (NPR-31114)。
* 即便使用默认筛选器后，资源也会从在 Dynamic Media - Scene7 部署上运行的创作实例复制到发布实例 (NPR-30856)。

### 站点 {#sites-1}

* 主要页面的页面属性无法加载，并返回 NullPointerException。该问题通过添加 `cq:blueprin`t 属性得以解决 (NPR-30901)。
* 无法从根节点上的 blueprintConfig 正确检索到转出配置。触发了 Blueprint 和 Live Copy 的停用。仅触发 Blueprint 的停用 (NPR-30866)。
* 用户转出页面时，转出配置对话框显示重复的Live Copy路径(NPR-30438)。
* 开箱即用的基架富文本编辑器 (RTE) 意外地将内嵌字体大小应用到元素（NPR-31283、NPR-30922）。
* 在包含开箱即用设计导入程序组件的 Adobe Campaign 中无法同步营销活动 (NPR-30890)。
* 富文本编辑器 (RTE) 不允许您将嵌入的表格作为列表项插入 (NPR-30878)。
* 用户聚焦于左边栏字段，并使用键盘快捷键粘贴内容。 在执行此操作时，它会粘贴页面编辑器剪贴板的内容，而不是从左边栏字段复制的内容(NPR-31173)。
* 用户编辑内容片段时，会恢复内容片段的已删除变量(NPR-31272)。
* AEM Site 不会创建语言副本 (NPR-30690)。
* 页面编辑器的操作没有控件来转出 Live Copy (NPR-30613)。

### 社区 {#communities}

* 活动和通知标题不一致 (NPR-30940)。
* Analytics报表不会填充到AEM创作环境中。 此时将显示一个空白页面(NPR-30905)。
* 在社区博客中无法正常分页 (NPR-30827)。

### Foundation {#foundation}

* 基于 Jetty 的 HTTP 服务的缓冲区大小配置中的更新未保存 (NPR-30925)。

### 表单 {#forms-1}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-1}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM 服务包和累积修订包保持一致。因此，请务必在安装任意AEM Service Pack、累积修补程序包或功能包之后安装AEM Forms附加组件包。

#### 自适应表单 {#adaptive-forms}

* 使用脚本计算的浮动值未正确显示在表单集的表单中 (NPR-30802)。

#### HTML5 表单 {#html-forms}

* 在添加子表单的实例时，生成 XDP 表单的 HTML5 预览时会出现闪烁 (NPR-30908)。

### Forms JEE 安装程序 {#forms-jee-installer}

#### Acrobat 服务 {#document-services}

* 应用补丁以修复 HTML 转 PDF 的问题后，OutputService 显示错误的响应 (NPR-31504)。

#### PDFG 服务 {#pdfg-service}

* 对于 HTML2PDF 服务，不会显示 JMX 控制台的最大重复使用计数 (NPR-30305)。

#### Foundation JEE {#foundation-jee}

* 对于 HTML2PDF 服务，不会显示 JMX 控制台的最大重复使用计数 (NPR-30136)。

### 累积修订包 6.3.3.6 {#cumulative-fix-pack-2}

AEM 累积修订包 6.3.3.6 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.6 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 的发行说明。

### 资源 {#assets-2}

* Dynamic Video的视频聚合仅返回结果集中的前100项。 NPR-30441：适用于 CQ-4213561 的修补程序
* 通过 DataPower 实施的 Adobe 智能标记存在连接问题。NPR-30026：适用于 CQ-4269457 的修补程序
* 无法使用Assets界面打开其名称具有百分比符号(%)的文件夹的存档解压缩。 NPR-29989：适用于 CQ-4270467 的修补程序
* 处理大型 PDF 文件的子资源会导致 OutOfMemoryError (OOME) 异常。NPR-29851：适用于 CQ-4269574 的修补程序

### 站点 {#sites-2}

* AEM 与 Campaign 集成过程中发生 ContextHub 错误。NPR-30624：适用于 CQ-4250790 的修补程序
* 如果 AEM 服务器重新启动，保存在资源上的“onTime”或“offTime”元数据属性不会被撤回。NPR-30412：适用于 CQ-4272784 的修补程序
* 在生成CSV导出时，为列表视图添加自定义列会中断报表。 NPR-30208：适用于 CQ-4273344 的修补程序
* /etc/reports/中的OOTB报告无法正常工作，并且未显示历史数据图。 NPR-30016：适用于 CQ-4220180 的修补程序
* resourceType请求参数的值将被复制到用双引号封装的HTML标记属性的值中。 NPR-29832：适用于 CQ-4255365 的修补程序

### 社区 {#communities-1}

* AEM Communities审核控制台存在重复内容问题。 NPR-30667：适用于 CQ-4276829 的修补程序

### 翻译 {#translation}

* 翻译问题 - 只有少数组件使用机器翻译进行了翻译。NPR-30079：适用于 CQ-4273764 的修补程序
* 使用翻译框架时，将页面添加到多个翻译作业会触发错误。NPR-29746：适用于 CQ-4270953 的修补程序

### 表单 {#forms-2}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM 服务包和累积修订包保持一致。因此，请务必在安装任意AEM Service Pack、累积修补程序包或功能包之后安装AEM Forms附加组件包。

#### HTML5 表单 {#html-forms-1}

* 在浏览模式下使用 NonVisual Desktop Access 读取 HTML5 表单时，Chrome 浏览器会读取表单设计中每个可缩放矢量图形 (SVG) 前的“图形”。NPR-30451：适用于 CQ-4274732 的修补程序

#### 表单 - 后端集成 {#forms-backend-integration}

* 创建表单数据模型 (FDM) 时，看不到数据库连接的服务/数据源。NPR-30108：适用于 CQ-4273359 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-1}

#### Forms - Acrobat Services {#forms-document-services}

* 对PDF服务的HTML执行负载测试时，该测试会因错误而失败，并且文件类型设置会从AEM Forms Server中删除。 NPR-30111、NPR-30086：适用于 CQ-4271495 的修补程序

### 累积修订包 6.3.3.5 {#cumulative-fix-pack-3}

AEM 累积修订包 6.3.3.5 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.5 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 的发行说明。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.17。

### 资源 {#assets-3}

* 针对 S3 多部分支持更新了 DAM DMGateway 接口。NPR-29740：适用于 Q-4226303 的修补程序
* 无法从资源详细信息页面中删除视频资源上的图像演绎版。 NPR-29417：适用于 CQ-4268675 的修补程序
* 所有者无法在私有文件夹内创建私有文件夹。NPR-29397：适用于 CQ-4229830 的修补程序
* 上传大于2 GB的Adobe Illustrator图稿文件会生成一个Java™栈空间错误。 NPR-29265：适用于 CQ-4226217 的修补程序
* DAM CQ Mime 类型服务为 m3u8 应用文本后，资源变得无法使用。NPR-29259：适用于 CQ-4264052 的修补程序
* 尝试在 Edge 中创建收藏集时，“创建”选项无法正常使用。NPR-29248：适用于 CQ-4265699 和 CQ-4265438 的修补程序
* 资源链接共享在文件夹中显示某些资源的空白灰色卡片。NPR-29831：适用于 CQ-4270187 的修补程序
* 添加到资源的新标记无法保存，且从属性中消失。适用于 CQ-4271931、CQ-4270476 的修补程序

### 站点 {#sites-3}

* 在多字段中使用时，CoralUI在组件级别存储fileReferenceParameter而不是多字段级别。 NPR-29535：适用于 CQ-4266129 的修补程序
* 尝试在 AEM 6.3.3.3 上比较最新与当前页面版本时出现问题。NPR-29532：适用于 CQ-4269639 的修补程序
* 路径字段将在根路径中打开，这与指定的搜索路径无关。 NPR-29398：适用于 CQ-4268897 的修补程序
* （体验片段）FacebookApplication#setUpApp使用已弃用的API，该API不再可用。 NPR-29213：适用于 CQ-4266630 的修补程序
* 在实例上启用缩小功能后，将组件添加到WCM页面时生成错误警报。 NPR-29476：适用于 CQ-4266197 的修补程序
* 转出期间不从Blueprint传播空属性和多个属性。 使用 Blueprint 重置 Live Copy 对组件不起作用。NPR-29252：适用于 CQ-4264928、CQ-4264926、CQ-4267722 的修补程序
* 在源代码编辑模式下，将富文本编辑器从全屏最小化会导致内容丢失。NPR-28838：适用于 CQ-4260584 的修补程序

### 社区 {#communities-2}

* 没有审查方权限的访客和成员可以通过粘贴 URL 查看未批准和待处理的帖子。NPR-29726：适用于 CQ-4271124 的修补程序
* 在社区登录时，出现长达 40-50 秒的高响应时间。NPR-29679：适用于 CQ-4269444 的修补程序
* 使用不同的用户名和电子邮件登录时无法重置密码，因为密钥似乎是使用交换的用户名和电子邮件生成的。NPR-29281：适用于 CQ-4268694 的修补程序

### 体验片段 {#experience-fragments}

* 使用智能图像时，无法将体验片段导出到目标。 适用于 CQ-4269606 的修补程序

### 复制 {#replication}

* 复制代理组件容易受到漏洞攻击，该漏洞会向未经授权的用户泄露敏感信息。 NPR-29613：适用于 Granite-25070 的修补程序
* 用户提供的数据未在`cq/replication/components/agent`组件的输出中进行转义，从而导致存储型跨站点脚本(XSS)漏洞。 NPR-29452：适用于 CQ-4266263 的修补程序

### 表单 {#forms-3}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-3}

* AEM Forms附加组件包中没有新的修复。

### Forms JEE 安装程序 {#forms-jee-installer-2}

* AEM Forms JEE 安装程序中没有新的修补程序。

### 6.3.3.5 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in}

AEM 6.3.3.5 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_5-bundle-list.txt)

AEM 6.3.3.5 中包含的内容包列表

[获取文件](assets/do-not-localize/content_packages6335.txt)

### 累积修订包 6.3.3.4 {#cumulative-fix-pack-4}

AEM 累积修订包 6.3.3.4 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.4 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 的发行说明。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.16。
* 在 Brand Portal 复制代理中添加了套接字超时和连接超时。

### 资源 {#assets-4}

* 如果重新上传具有相同名称的存档文件，则不会为新处理的资源生成呈现版本。NPR-28643：适用于 CQ-4262286 的修补程序
* 工作流CommandLineProcess因文件名中含有单引号而失败。 NPR-28805：适用于 CQ-4262287 的修补程序
* 使用过滤器时，收藏集页面和收藏集页面之间的值不同。 NPR-28642：适用于 CQ-4261405 的修补程序
* 上传较大的 ZIP 存档资源时会触发 CommitFailedException。NPR-28528：适用于 CQ-4260903 的修补程序
* 编辑包含特殊字符的文件夹时，文件夹元数据无法保存。NPR-28211：适用于 CQ-4260401 的修补程序
* 无法从资源详细信息页面中删除视频资源的图像演绎版。 NPR-29149：适用于 CQ-4266073 的修补程序
* 使用 DM 组件的 DMS7 桌面视频交付采用渐进式下载来以发布模式播放视频，并且不进行流式传输。NPR-28754：适用于 CQ-4263732 的修补程序
* 无法创建/编辑图像预设，因为限制对 /etc/dam/video/dynamicmedia 的访问会禁用图像管理器的功能。NPR-28662：适用于 CQ-4263022 的修补程序
* 与 DMS7 编码的视频文件的链接共享会导致空白文件夹。NPR-28851：适用于 CQ-4206743 的修补程序
* 从 AEM 到 Brand Portal 的复制操作会卡住较长时间。NPR-28913：适用于 CQ-4254932 的修补程序

### 社区 {#communities-3}

* 无法打开 Outlook 已发送邮件和收件箱文件夹中包含附件的邮件。NPR-28559：适用于 CQ-4217072 的修补程序

### 站点 {#sites-4}

* 6.3 的 SuggestionHandler 中存在跨站点脚本 (XSS) 漏洞。NPR-28692：适用于 CQ-4253821 的修补程序
* 深度转出结束，而不包含相应 Live Copy 中的所有分支。NPR-29175：适用于 CQ-4239472 的修补程序
* (MSM) 使用 oak-index 实施 Live CopyIndex。NPR-29198：适用于 CQ-4222472 的修补程序
* 文件`coral.js`包含易受攻击的库`handlebars.js`版本。 NPR-26973：适用于 CQ-4255377 的修补程序
* 如果将Target组件与嵌套式布局容器和文本组件一起使用，则在编辑文本或单击容器时，会引发以下JavaScript错误：“无法读取null的属性currentPos”。 NPR-29077：适用于 CQ-4246594 的修补程序
* （触屏UI）无法将标记批量更新到已使用其他标记进行标记的页面。 NPR-28729：适用于 CQ-4262922 的修补程序
* 在卡片视图中打开该变量会导致500错误。 NPR-28611：适用于 CQ-4263571 的修补程序
* 转出已在主节点中移动的结构会导致错误的`cq:moveTarget`。 NPR-28968：适用于 CQ-4265280 的修补程序

### 集成 {#integration}

* （云服务配置）在根级别出现的“继承自”复选框应被删除。NPR-28771：适用于 CQ-4259676 的修补程序
* com.day.cq.personalization.impl.TeaserResourceEventHandler 陷入无限循环，并导致对发布实例上的节点进行更新。NPR-28561：适用于 CQ-4263096 的修补程序
* 使用 BrightEdge 凭证失败并出现连接错误。NPR-29167：适用于 CQ-4265872 的修补程序
* 因缺少‘资源’类的导入语句而导致 OfferproxyTandtProvider.java 中出现编译问题：缺少导入语句：import org.apache.sling.api.resource.Resource。NPR-28772

### 商务 {#commerce}

* 排序选项不适用于 Commerce 收藏集中的资源。NPR-28755：适用于 CQ-4213622 的修补程序

### Jetty {#jetty}

* 在 6.3.3 基础上安装 CFP2 后，每个 302 重定向的 error.log 中会出现 Jetty 异常。NPR-28606：适用于 CQ-4262844 的补丁包

### UI - Foundation {#ui-foundation}

* 单击标记会移除全局鼠标上移事件，并且对话框在可拖动模式下冻结。 NPR-28641：适用于 CUI-7294 的修补程序

### WCM - MSM {#wcm-msm}

* PageManager 移动的 PushOnModify 转出从两个会话提交多次，从而导致出现争用情况。NPR-28880：适用于 CQ-4266191 的修补程序

### 漏洞 {#vulnerability}

* CSRF保护框架不适用于AEM Foundation表单。 NPR-28612：适用于 GRANITE-22231 的修补程序

### 表单 {#forms-4}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

AEM Forms 的主要功能亮点包括：

* 启用了在“策略集视图”页面上选择每页项目的选项。
* 为所有浏览器添加了共享队列功能。

### Forms 附加组件包 {#forms-add-on-package-4}

#### 表单 - 工作流 {#forms-workflow}

* 共享队列响应任务会在HTML5工作区中打开一个Flash元素。 NPR-29161：适用于 CQ-4266498 的修补程序
* 如果按钮包含umlaut字符，则无法从Workspace提交。 NPR-29014：适用于 CQ-4263172 的修补程序

#### 表单 - 文档安全 {#forms-document-security}

* 启用该选项，以便在策略集视图页面上选择每页的项目。 NPR-29243：适用于 CQ-4268567 和 CQ-4265132 的修补程序

#### Forms - Acrobat Services {#forms-document-services-1}

* OSGi 表单汇编程序无法处理 Acrobat 文件。NPR-29049：适用于 CQ-4254426 的修补程序

#### HTML5 表单 {#html-forms-2}

* 在Designer中将XDP作为PDF与同一XDP作为HTML进行预览时，会遇到不同的行为。 NPR-28602：适用于 CQ-4260239 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-3}

* AEM Forms JEE 安装程序中没有新的修补程序。

### 6.3.3.4 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-1}

AEM 6.3.3.4 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

AEM 6.3.3.4 中包含的内容包列表

[获取文件](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### 累积修订包 6.3.3.3 {#cumulative-fix-pack-5}

AEM 累积修订包 6.3.3.3 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.3 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 的发行说明。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.16。
* 策略集列表分页更改为每页限制 50 条记录。
* 已将 rep: cache 添加到发布实例上 AEM Communities 用户同步侦听器中的可忽略节点。
* 为列表和卡片视图按钮添加了aria标签。
* 执行任何搜索时，会包含逗号的转义字符。
* 启用了对内容策略的综合资源的支持。

#### 资源 {#assets-5}

* 无法下载类型为 `.jp2`、`.max`、`.oft`、`.msg` 的多个文件。NPR-28002：适用于 CQ-4210856 的修补程序
* ImageServer 发布设置不会复制到混合交付中。NPR-28329：适用于 CQ-4253030 的修补程序

#### 社区 {#communities-4}

* 发布时，为 AEM Communities 启用组件启用了键盘导航。NPR-27739：适用于 CQ-4253856 的修补程序
* 启用了键盘导航来触发内容播放。NPR-27738：适用于 CQ-4254026 的修补程序
* 为列表和卡片视图按钮添加了aria标签。 NPR-27736：适用于 CQ-4254027 的修补程序
* （补丁包）已将 rep: cache 添加到发布实例上 AEM Communities 用户同步侦听器中的可忽略节点。NPR-27841：适用于 CQ-4247234 的修补程序
* 在搜索框中，特殊字符带有转义字符(\)前缀。 NPR-27839：适用于 CQ-4259757 的修补程序
* 在快速搜索中搜索`(`、`+`和`?`等字符时出错。 NPR-28212：适用于 CQ-4260969 的修补程序
* 无法使用 API 删除用户生成的内容中的评论。NPR-28075：适用于 CQ-4260534 的修补程序
* 在发布新评论时，发布到下一页的评论以黄色突出显示。 NPR-28148：适用于 CQ-4259681 的修补程序
* 无法打开 Outlook 已发送邮件和收件箱文件夹中包含附件的邮件。NPR-28559：适用于 CQ-4217072 的修补程序

#### 站点 {#sites-5}

* 在 AEM 6.3 中运行版本清除，会导致日志中持续不断地反复出现警告。NPR-27750：适用于 CQ-4206870 的修补程序
* 富文本编辑器全屏模式不支持样式插件。 NPR-27622：适用于 CQ-4258674 的修补程序
* 将内容框架加载到editor.js中后未清除列表`loaderPromises`。NPR-27768：适用于CQ-4205337的修补程序
* 若未在父组件中设置模板策略，则无法在嵌套的Parsys上设置该策略。 NPR-27987：适用于 CQ-4246095 的修补程序
* 组件浏览器无法清除用户输入的内容，因此可能会引发 JavaScript 错误。NPR-27986：适用于 CQ-4247590 的修补程序
* 用户尝试编辑内容片段时页面显示为空白。 NPR-27669
* 用户单击注释后，注释的高亮显示立即消失。BPR-27196：适用于 CQ-4254423 的修补程序

#### 集成 {#integration-1}

* ResourceResolver未解析Target组件的多个域。 NPR-28265：适用于 CQ-107847 的修补程序
* 现在，当操作显示时，LiveCopy继承取消可在目标容器上正常使用。 NPR-28129：适用于 CQ-4259813 的修补程序

#### 复制 {#replication-1}

* DispatcherFlushRules中断了6.3.3.1中的复制。NPR-28150：适用于CQ-4261401的修补程序

#### 营销活动 - 定位 {#campaign-targeting-1}

* TargetedContentManager 中出现 NullPointerException。适用于 CQ-4263485 的修补程序

#### 社交 - SCORM {#social-scorm}

* 在播放器中删除对可共享内容对象引用模型 (SCORM) 云的引用。适用于 CQ-4260779 的修补程序

#### DAM - 常规 {#dam-general}

* 通过链接共享电子邮件下载，会返回空的/损坏的 Zip 文件。适用于 CQ-4259686 的修补程序

#### `MAC` - Test&amp;Target 集成 {#mac-test-target-integration}

* 无法对默认受众之外的受众配置Target组件选项。 适用于 CQ-4261370 的修补程序

#### 翻译 {#translation-1}

* 将 MS® Translator 升级到 API v3.0 后，在 AEM 6.3 中启用对 MS® Translator 服务的支持。NPR-28365：适用于 CQ-4259096 的修补程序

### 表单 {#forms-5}

### Forms 附加组件包 {#forms-add-on-package-5}

#### 表单 - 工作流 {#forms-workflow-1}

* 无法在 HTML5 工作区上呈现 PDF 表单。NPR-28059：适用于 CQ-4260373 的修补程序

#### Forms - Acrobat Services {#forms-document-services-2}

* 在 Admin Console 的“策略集”视图中，无法看到除列出的前 1000 项之外的任何其他策略集。NPR-28060、NPR-26047：适用于 CQ-4249865 的修补程序
* 引发了一个名为 `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` 的异常，导致短暂过程无法完成。NPR-28652

#### 表单 - 自适应表单 {#forms-adaptive-forms}

* 选中复选框项目时，下拉列表中的添加或删除项目不会更新。 NPR-28224：适用于 CQ-4252834 的修补程序

### Forms - JEE 安装程序 {#forms-jee-installer-4}

* AEM Forms JEE 安装程序中没有新的修补程序。

### 6.3.3.3 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-2}

AEM 6.3.3.3 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6333_bundle_list.txt)

AEM 6.3.3.3 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_list_6333.txt)

### 累积修订包 6.3.3.2 {#cumulative-fix-pack-6}

AEM 累积修订包 6.3.3.2 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.2 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 AEM 6.3 服务包 3 发行说明。

AEM 累积修订包的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.15。
* 在文件夹元数据架构中添加了对规则选项卡的支持，以及在资产文件夹中强制实施该选项卡的支持。
* 为发布时的组列表页面启用了分页支持。
* 启用的 unreadCount 通知可以配置为任意数量。默认值设置为20。
* 修复了外部链接检查程序。

#### 资源 {#assets-6}

* 动态下拉列表不支持级联下拉列表。NPR-27044：适用于 CQ-4252564 的修补程序
* 改进了查询，使其使用ExpiryNotification功能。 NPR-26999：适用于 CQ-4251188 的修补程序
* 规则从元数据架构迁移到文件夹元数据架构。NPR-27771：适用于 CQ-4257737、CQ-4257735 和 CQ-4259822 的补丁包
* 资产引用调整无法更新Sling ResourceCollections中资产的引用。 NPR-26759：适用于 CQ-4252605 的修补程序
* 通过链接共享电子邮件下载会返回空的或损坏的zip文件。 NPR-27997：适用于 CQ-4259686 的修补程序
* 混合视频编码未完成，且没有创建缩略图。NPR-27122：适用于 CQ-4255080 的修补程序

#### 站点 {#sites-6}

* 暂停父页面会从缺失页面中删除cq：LiveRelationship mixin类型。 NPR-26996：适用于 CQ-4254113 的修补程序
* （外部链接检查程序）内部链接在各个页面上显示为已损坏，但外部链接并非如此。NPR-27481：适用于 CQ-4257780 的修补程序
* 编辑其他页面属性时，云服务配置继承中断。NPR-27311：适用于 CQ-4256785 的修补程序
* 将核心组件表单与Foundation表单一起使用时出现空指针异常。 NPR-27333：适用于 CQ-4249176 的修补程序
* 富文本编辑器删除了空的 alt 标记。NPR-26938：适用于 CQ-4253267 的修补程序
* （经典 UI）如果存在多个下拉菜单，则选择操作可能会导致性能问题，并触发更改侦听器。NPR-27115：适用于 CQ-4237215 的修补程序
* 当富文本编辑器与多个字段组合时，出现“Uncaught TypeError： fieldAPI.getName is not a function at foundation.js”错误。 NPR-27146：适用于 CQ-4253155/CQ-4259967 的修补程序
* 即使单击Safari浏览器中的单选按钮，焦点/光标仍保留在富文本编辑器上。 NPR-27144：适用于 CQ-4249635 的修补程序
* 用户尝试编辑内容片段时页面显示为空白。 NPR-27669
* 无法创建体验片段版本。NPR-27689：适用于 CQ-4259009 的修补程序

#### 集成 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever 遍历整个树来收集可用品牌。NPR-27060：适用于 CQ-4255790 的修补程序
* `cq:actions` 未被视为目标组件。NPR-27616：适用于 CQ-4257497 的修补程序

#### Sling {#sling}

* 当 data-sly-use 与具有相同名称的类一起使用时，会生成不合规的代码。NPR-27282：适用于 Sling-7581 的修补程序

#### 商务 {#commerce-1}

* 已更新到 Apache Felix Http Jetty 4.0.6。NPR-26472：适用于 Granite-22916 的修补程序

#### DAM - DM 客户端 {#dam-dm-client}

* 在Dynamic Media组件中指定断点后，图像不显示。 适用于 CQ-4256168 的修补程序

#### DAM - DMServices {#dam-dmservices}

* 包含相关视频的 MixedMediaSet 无法正确同步。适用于 CQ-4251650 的修补程序
* 对于混合媒体集，无法在查看器预设编辑器中播放视频。 适用于 CQ-4251442 的修补程序

#### DAM - 常规 {#dam-general-1}

* 应用SP3补丁后缺少指向内容片段模型的链接。 适用于 CQ-4259029 的修补程序

#### DAM - UI {#dam-ui}

* 安装SP3后，文件夹元数据架构UI损坏。 适用于 CQ-4257737 的修补程序

#### 社区 {#communities-5}

* 添加分页支持，以在发布时对列表分组。NPR-26953：适用于 CQ-4246525 的修补程序
* 未读通知计数无法设置为大于 21。NPR-27496：适用于 CQ-4252829 的修补程序
* 用户订阅限制限制为1000。 NPR-27615：适用于 CQ-4254689 的修补程序
* 在论坛中上传图像以外的附件（例如 PDF）时出现错误。NPR-27375：适用于 CQ-4257753 的修补程序
* 用于回复的链接对行点击不起作用。 NPR-24556：适用于 CQ-4256138 的修补程序
* 删除 UGC 时，不会删除与 UGC 的关系。NPR-27631：适用于 CQ-4258706 的修补程序
* 如果社区是使用数据库存储资源提供程序 (DSRP) 设置的，则无法在关键字搜索中按地址值搜索。NPR-27652：适用于 CQ-4253261 的修补程序
* 确认删除后，单击图像上的垃圾桶图标将永久删除附件。NPR-27340：适用于 CQ-4255150 的修补程序
* 论坛帖子和回复会添加到第二页的顶部，刷新后，帖子将移至第一页顶部的正确位置。NPR-27341：适用于 CQ-4247338 的修补程序
* 启用Scorm资源完成状态标签在UI中显示为空。 NPR-27152：适用于 CQ-4249994 的修补程序
* 启用&#x200B;**允许拥有权限的**&#x200B;时，拥有权限的成员应只能为社区成员用户撰写。 NPR-27901：适用于 CQ-4251235 的修补程序

#### 留存 {#sustenance}

* 应将包管理器活动日志提取到单独的日志文件中。NPR-27323：适用于 Granite-14866 的修补程序

#### 翻译 {#translation-2}

* 翻译预览不适用于 we.retail 示例内容。NPR-27170：适用于 CQ-4241179 的修补程序

* 主动式 platform.login 修补程序。NPR-26961
* 在具有Tomcat的AEM WAR中，“保存并关闭”页面属性不会返回到正确的页面。 NPR-27567：适用于 Granite-23671 的修补程序

* 保存后，通过sourceEdit功能输入的文本将丢失。 适用于 CQ-4259273 的修补程序

### 表单 {#forms-6}

### Forms 附加组件包 {#forms-add-on-package-6}

#### 表单 - 文档安全 {#forms-document-security-1}

* JEE 客户端 SDK 出现并发性问题。NPR-27572：适用于 CQ-4247156 的修补程序

#### Forms - Acrobat Services {#forms-document-services-3}

* 在 WebSphere® 上创建基于 SOAP 的表单数据模型失败。NPR-27692：适用于 CQ-4253702 的修补程序

#### 表单 - 自适应表单 {#forms-adaptive-forms-1}

* AEM Forms 存在 XML 注入漏洞。NPR-27863：适用于 CQ-4257315 的修补程序
* 如果在AEM Forms页面中配置了错误的表单，并且选中了“表单覆盖整个页面宽度”复选框，则AEM Sites容器组件将不可见。 NPR-25972：适用于 CQ-4239287/CQ-4249133 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* 在 WebSphere® 上创建基于 SOAP 的表单数据模型失败。NPR-27692：适用于 CQ-4253702 的修补程序

#### 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included}

AEM 6.3.3.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/63332bundle_list.txt)

AEM 6.3.3.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6332content_package.txt)

### 累积修订包 6.3.3.1 {#cumulative-fix-pack-7}

AEM 累积修订包 6.3.3.1 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 服务包 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.3.1 依赖于 AEM 6.3 服务包 3。因此，您必须先安装 AEM 6.3 服务包 3，然后再安装 AEM 累积修订包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 服务包 3](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 中的发行说明。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.14。
* 改进了谓词和搜索的性能。
* 修复了 FormData 处理中的默认值问题。
* 已将表单生成器升级到最新的Handlebars版本。
* 在对话框模式下为RTE的编辑配置添加了配置servlet。
* 添加了对复合字段的支持。
* 为编辑对话框启用/禁用含内容策略的富文本编辑器工具栏项目。

#### 资源 {#assets-7}

* 启用IDS分离后，DAM更新资产工作流不再链接引用。 NPR-26135：适用于 CQ-4250933 的修补程序
* 无法对由取消存档器步骤创建的存档文件（其中包含名为%的文件夹）进行解压缩。 NPR-26275：适用于 CQ-4251482 的修补程序
* 单引号字符会阻止元数据更新。 NPR-26808：适用于 CQ-4254305 的修补程序
* (Omnisearch) 在收藏集中搜索时，出现性能问题。NPR-26714：适用于 CQ-4253408 的修补程序
* 将 GQLConverter 与全文搜索一起使用时，如果在文本中包含“OR”字母，则会被错误地处理。NPR-26564：适用于 CQ-4247362 的修补程序
* 从多租户共享资源链接，会在前面附加租户 ID，从而形成无效的 URL。NPR-26482：适用于 CQ-4253540 的修补程序
* 在 Dynamic Media 云配置 UI 中，禁用“公司根文件夹路径”。NPR-26361：适用于 CQ-4249505 的修补程序
* .mos RAW 文件的摄取时间延长。NPR-26296：适用于 CQ-4250661 的修补程序
* 资产链接共享不允许添加多个具有数字用户ID的内部用户。 NPR-26206：适用于 CQ-4251466 的修补程序
* 使用 deflate64 算法压缩的 ZIP 文件损坏。NPR-26793：适用于 CQ-4253995 的修补程序
* 缩略图生成过程无法正确用于复杂的PDF文件，从而导致缩略图缺少图像的部分内容。 NPR-26057：适用于 CQ-4250944 的修补程序
* 缩略图生成出现堆内存利用问题。NPR-25545：适用于 CQ-4246960 的修补程序
* 在资源上创建许多关系会导致错误。NPR-26309：适用于 CQ-4250708 的修补程序
* **删除演绎版**&#x200B;选项不起作用，并引发错误“没有可删除的内容”。 NPR-26007：适用于 CQ-4213414 的修补程序
* 无法删除多值字段的默认值。NPR-25116：适用于 CQ-4247856 的修补程序
* （DM 混合模式）带有 Dynamic Media 的 AEM 6.3.2 的目录复制中断。NPR-26406：适用于 CQ-4251306 的修补程序

#### 站点 {#sites-7}

* Sites 修补程序的主动式补丁包。NPR-26963
* 如果“标题”和“名称”的大小写类型不同，标记会创建两次。NPR-26877：适用于 CQ-4254134 的修补程序
* 策略不控制“编辑”对话框中的富文本编辑器功能。 NPR-27059、NPR-26750：适用于 CQ-4241130 的修补程序
* 客户端上下文 segment.js 缓存与非缓存问题。NPR-26622：适用于 CQ-4253486 的修补程序
* 经典版本中子规则的区段规则 (/etc/segmentation) 激活导致发布下降。NPR-26601：适用于 CQ-4253588 的修补程序
* 添加“特殊字符”会将“富文本编辑器”对话框滚动到顶部。 NPR-26435：适用于 CQ-4249869 的修补程序
* （触屏 UI）从全屏切换到浮动对话框时，多个富文本编辑器的工具栏变得不可用。NPR-25652：适用于 CQ-4206008 的修补程序
* 提升多页启动项会为每个页面创建多个版本。NPR-26810：适用于 CQ-4254663 的修补程序
* 结构化内容片段模型标记字段不反映标记移动操作。 NPR-26801：适用于 CQ-4251805 的修补程序
* （触屏 UI）重命名 Blueprint 中的页面后，无法从页面编辑器取消发布子页面。NPR-26774：适用于 CQ-4254175 的修补程序
* 未发布的页面无法使用引用。NPR-26749：适用于 CQ-4254372 的修补程序
* 将变体创建为Live Copy需要用户刷新页面才能反映。 NPR-26663：适用于 CQ-4254328 的修补程序
* （经典UI）返回页面属性后，缩略图图像不再使用继承并从站点管理员和Sidekick中消失，导致图像显示为空白。 NPR-26562：适用于 CQ-4252346 的修补程序
* 创建页面版本并触发比较时，/content/versionshistory 中的节点将列在 Blueprint 的实时副本列表中。NPR-26506：适用于 CQ-4243957 的修补程序
* 体验片段管理员编辑器中的 URL 不允许叠加。NPR-26318：适用于 CQ-4252156 的修补程序

#### 平台 {#platform}

* 包含测试事件的 ReplicationEventListener 中出现会话泄漏。NPR-25937：适用于 CQ-4251090 的修补程序
* 复制使用过期的OAuth令牌，从而导致多个错误。 NPR-25894：适用于 GRANITE-22388 的修补程序

#### 集成 {#integration-3}

* 由于使用不兼容的模板，嵌入了 AEM 的 TSDK 在升级到 Handlebars 4 时中断。NPR-26699：适用于 CQ-4248974 的修补程序
* 发布包含新资源的页面，会停用发布实例中的子页面，而不会发出通知。NPR-24869：适用于 CQ-4247832 的修补程序
* 复制操作使用已过期的令牌进行 OAauth。NPR-25984：适用于 Granite-22388 的修补程序

#### 复制 {#replication-2}

* Http 传输可能会泄漏处于打开状态的会话。适用于 Granite-17434 的修补程序
* 当访问访问访问令牌节点时，多个复制代理同时进行访问会导致日志中出现异常。 NPR-26964：适用于 GRANITE-23276 和 Granite-23155 的修补程序

#### ContextHub {#contexthub}

* 文件`coral.js`包含易受攻击的库`handlebars.js`版本。 适用于 CQ-4255377 的修补程序

#### DAM - DM 客户端 {#dam-dm-client-1}

* 删除图像资源的副本，会使原始图像资源无法使用。适用于 CQ-4251648 的修补程序
* 从 S7 服务器冗余下载额外的图像内容。适用于 CQ-4248770 的修补程序

#### Granite {#granite}

* AEM OAuth 提供程序无法执行不区分大小写的搜索。NPR-26133：适用于 GRANITE-22650 的修补程序
* 包验证程序无法验证 CFP/SP 中含有的包。NPR-26775：适用于 Granite-22825 的修补程序

#### 社区 {#communities-6}

* 搜索结果中存在分隔符问题。NPR-27051：适用于 CQ-4248939 的修补程序
* 在 Adobe 存储资源提供程序中，将下拉列表值从“达拉斯”更改为“弗吉尼亚”。NPR-26936：适用于 CQ-4254434 的修补程序
* 在 SocialTagManager 中启用对本地化标题搜索的支持。NPR-26932：适用于 CQ-4250276 的修补程序
* 创建论坛帖子时，附件图像不显示缩略图。 NPR-26380：适用于 CQ-4253105 的修补程序
* 从Word插件粘贴时，无法加载多个图像。 NPR-26728：适用于 CQ-4253638 的修补程序
* 无法筛选审核页面中的内容。NPR-26697：适用于 CQ-4213766 的修补程序
* （安全漏洞）由于 JWT 配置错误，导致帐户接管。NPR-26440：适用于 CQ-4253314 的修补程序
* 从Adobe存储资源提供程序检索数据时速度较慢。 NPR-26237：适用于 NPR-24152 的修补程序
* 私人留言合成页面不稳定且缓慢。 NPR-26120：适用于 CQ-4250923 的修补程序
* “全部标记为已读”通知仅将前 10 个呈现为未读，而不刷新页面。NPR-27036：适用于 CQ-4254058 的修补程序
* 社区评论部分分页单击和页面加载行为。NPR-27030：适用于 CQ-4251228 的修补程序
* （论坛搜索）“返回”按钮跳过页面，并返回到 forum.html。NPR-26949：适用于 CQ-4254804 的修补程序
* 未读通知不会增加超过 21。NPR-26947：适用于 CQ-4251251 的修补程序
* （SearchScheduledPosts 作业）在 ConfigMgr 中添加启用/禁用切换开关。NPR-26924：适用于 CQ-4250463 的修补程序
* 在“指定任务”页面上滚动时，Tomcat 上下文 (/aempublish) 路径中断。NPR-26919：适用于 CQ-4254345 的修补程序
* 创建组和成员时，出现 NullPointerException。NPR-26778：适用于 CQ-4248095 的修补程序
* 审查方取消固定和取消功能内容，不适用于 MySQL 单一职责原则 (SRP)。NPR-26767：适用于 CQ-4251520 的修补程序
* 某些字符存在搜索功能问题。NPR-26726：适用于 CQ-4247744 的修补程序
* 为审核 UI 和启用资源启用深层链接。NPR-26705：适用于 CQ-4251381 的修补程序
* 搜索论坛组件时出现问题。 NPR-26577：适用于 CQ-4251303 的修补程序
* 在社区消息中使用名称和姓氏一起搜索，不会返回预期结果。NPR-26377：适用于 CQ-4253150 的修补程序
* 删除回复后，分页不会更新。NPR-26327
* 删除帖子会起作用，但在控制台上出现错误，并且帖子在UI上仍然可见。 NPR-26292：适用于 CQ-4252803 的修补程序
* 分页不会动态更新，并且回复列表越来越长。NPR-26145：适用于 CQ-4251586 的修补程序
* 组设置不会加载到包含数千个用户的组上。NPR-25642：适用于 CQ-4238426 的修补程序
* 目录资源播放器无法使用上下文路径。NPR-25640：适用于 CQ-4238426 的修补程序
* （论坛搜索）- 包含大量帖子的线程的分页链接不适用于通知。适用于 CQ-4254202 的修补程序
* 审核控制台在 Firefox 中仅显示 5 个条目。适用于 CQ-4254128 的修补程序
* 创建站点时，组不可见。NPR-27148：适用于 CQ-4251788 的修补程序
* 将组和成员添加到“角色”设置中，并在博客功能中允许拥有权限的成员时，出现空指针异常。 NPR-21732、NPR-27176：适用于 CQ-4255909 的修补程序
* 编辑站点并在角色设置中添加成员会引发空指针异常。 NPR-27132：适用于 CQ-4255909 的修补程序

#### 用户界面 {#user-interface}

* 主动式平台登录修补程序。NPR-26961
* （多字段）允许复合项目拥有自定义名称。NPR-26493：适用于 Granite-20568 的修补程序
* 粘贴页面后，在刷新之前不会更新列视图。NPR-26030：适用于 CQ-4236346 的修补程序
* 主动式 granite.ui.commons 修补程序。NPR-26960
* 主动式 granite.ui.content 修补程序。NPR-26959
* 主动式 CQ/体验日志修补程序。NPR-26943
* 主动式 Foundation UI 补丁包。NPR-26942
* (IE 11) 键入负值时，数字字段中会显示“NaN”。NPR-26701：适用于 CQ-100826 的修补程序
* （Coral 多字段）嵌套的多字段使用错误模板来创建项目。NPR-25649：适用于 CUI-6743 的修补程序
* 更新 granite coralui2 和 coralui3 clientlib 以从内部版本中删除 Handlebars。NPR-25606：适用于 Granite-22116 的修补程序

### 表单 {#forms-7}

### Forms 附加组件包 {#forms-add-on-package-7}

#### 表单 - 文档安全 {#forms-document-security-2}

* 对于非活动密钥，服务器日志中出现“主体密钥滚动”异常。NPR-26748：适用于 CQ-4253705 的修补程序
* 无法创建或编辑Document Security的水印设置。 NPR-26267、NPR-26129：适用于 CQ-4250234 的修补程序

#### Forms - Acrobat Services {#forms-document-services-4}

* 使用“验证 PDF/A”进行 PDF/A 验证时，未显示有效。NPR-25934：适用于 CQ-4248558 的修补程序

#### 表单 - 交互式通信 {#forms-interactive-communication}

* 编辑并保存可编辑的模块，然后打开或关闭“PDF预览”，可保持信件的PDF和HTML预览可见。 两个预览在同一窗口中仍然可用。 NPR-26770：适用于 CQ-4253217 的修补程序

#### 表单 - 工作流 {#forms-workflow-2}

* 工作区间歇性挂起并重复显示起始点。 NPR-26461：适用于 CQ-4253439 的修补程序
* 如果在任务名称中使用大括号，则会在日志中引发 ESAPI 异常。适用于 CQ-4256627 的修补程序
* 打开与起点关联的非预填充自适应表单或表单集时，会引发空指针异常。 适用于 CQ-4256124 的修补程序
* 无法使用全局设置发送电子邮件。NPR-26163：适用于 CQ-111110 的修补程序
* 应用axis.jar文件后无法打开工作区。 NPR-26131：适用于 CQ-4251126 的修补程序
* “刷新”按钮无法将最新数据从服务器同步到自适应表单。适用于 CQ-4255670 的修补程序
* 从管理员UI设置搜索模板，然后使用模板在AEM Forms工作区中进行搜索时，会引发异常。 适用于 CQ-4255649 的修补程序
* HTMLWorkspace中不显示名称中带有圆括号符号的应用程序下的进程跟踪详细信息。 适用于 CQ-4242101 的修补程序
* 在HTMLWorkspace的首选项屏幕中保存更改会引发异常。 适用于 CQ-4241485 的修补程序
* 最新 JEE 设置中的批量批准功能已损坏。适用于 CQ-4241486 的修补程序
* 任务/起点的草稿在最新的 6.4 JEE 服务器上失败。适用于 CQ-4241484 的修补程序
* 设置Date()。getTime()。toString参数以初始化会话，而不是Date.toString()。 适用于 CQ-4241483 的修补程序
* 打开/lc/ws时，在HTML参数中发现易受攻击的字符异常。 适用于 CQ-4241481 的修补程序

#### 漏洞 {#vulnerability-1}

* Forms Manager 的注释选项卡中存在存储型跨站点脚本 (XSS) 漏洞。NPR-27157：适用于 CQ-4255556 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* 企业安全 API 的代码审核。适用于 CQ-4255638 的修补程序
* 未能在WAS9中将esapi.properties加载为类加载器资源。 适用于 CQ-4255631 的修补程序
* 在域配置过程中单击“添加身份验证”会引发错误。适用于 CQ-4255634 的修补程序
* Forms JEE 支持 PKCS#11 双向身份验证。NPR-21372
* 修复了 Core 静态代码分析中报告的问题。适用于 CQ-104446 的修补程序
* 运行 LCM 时，部署 adobe.livecycle.weblogic.ear 和 adobe.livecycle.websphere.ear 会失败。适用于 CQ-4255629、CQ-4255630 的修补程序
* 应用程序管理中出现无效的错误消息。NPR-23289：适用于 CQ-4233163/CQ-4255636 的修补程序
* 在域配置过程中单击“添加身份验证”会导致出现错误。适用于 CQ-4255634 的修补程序

#### 表单 - JEE 连接器 {#forms-jee-connector}

* 修复了连接器静态代码分析中报告的问题。NPR-22260

#### PDFG 服务 {#pdfg-service-1}

* 从 LiveCycle 升级到 AEM 6.2 Forms 后，日志中出现 org.jgroups.Message 错误。NPR-26795：适用于 CQ-4220415 的修补程序
* AEM Forms - 迁移样式时出错。适用于 CQ-4251969 的修补程序
* 修复了PDFG静态代码分析报表中报告的问题。 NPR-23251：适用于 CQ-4213930 的修补程序

#### 6.3.3.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-3}

AEM 6.3.3.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/63sp3cfp1bundlelist.txt)

AEM 6.3.3.1 中包含的内容包列表

### 累积修订包 6.3.2.2 {#cumulative-fix-pack-8}

AEM 累积修订包 6.3.2.2 是一个重要更新，它包括自 2018 年 4 月 AEM 6.3 服务包 2 (6.3.2.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包 6.3.2.2 依赖于 AEM 6.3 服务包 2。因此，您必须先安装 AEM 6.3 服务包 2，然后再安装 AEM 累积修订包 6.3.2.x。有关安装说明，请参阅 [AEM 6.3 服务包 2](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) 中的发行说明。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.11。
* 在 Brand Portal 上启用了子资源和多页资源查看器。
* 已将字段类型的长度更改为255，以支持不同类型附件的所有可能的mime类型。
* 配置了当图像违反上传条件时从服务器发出的错误消息。
* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。
* 更新至cq-wcm-content和com.adobe.cq.launches.it.serverside的最新版本。
* 将com.adobe.granite.ui.coralui3-rte更新至已发布的最新版本。
* 已确保当expressionResolver为null时，呈现条件返回正常结果。
* Coral.ColumnView：添加了对“按住 Shift 键单击”的支持。

### 资源 {#assets-8}

* 资源文件夹“已关闭的用户组”(CUG) 字段不会返回“每个人”组。NPR-23163：适用于 CQ-4239377 的修补程序
* 搜索所保存的智能收藏集搜索时，不会返回所有结果。NPR-23243：适用于 CQ-4240355 的修补程序
* (ExpiryNotificationJobImpl) 优化了现有查询。NPR-23330：适用于 CQ-4205249 的修补程序
* （元数据配置文件）创建时设置的标准标记值在保存后不可用。NPR-23370：适用于 CQ-4235458 的修补程序
* （触屏 UI）由于 JS 错误，无法移动多个资源。NPR-23395：适用于 CQ-4241279 的修补程序
* 与显示的信息相比，下载大小不匹配。 NPR-23418：适用于 CQ-4242774 的修补程序
* 提取的文件扩展 LSR 和 SKETCH 的 mime 类型不正确，导致无效的文件下载。NPR-23644：适用于 CQ-4243260 的修补程序
* (Firefox/Chrome) 无法在“资源共享”页面中下载资源。NPR-23963：适用于 CQ-4244391 的修补程序
* 预览后，搜索面板中的资产管理员搜索彩块化消失。 NPR-23964：适用于 CQ-4244410 的修补程序
* 取消发布搜索表单，会完全删除默认搜索表单。NPR-23291：适用于 CQ-4241382 的修补程序
* (Brand Portal) 应在复制时筛选出目录谓词中的搜索。NPR-23292：适用于 CQ-4241385 的修补程序
* “发布到 Brand Portal”UI 操作不可用。NPR-23293：适用于 CQ-4241161 的修补程序
* “Publish/取消发布到Brand Portal”按钮应该对内容片段不可用。 NPR-23318：适用于 CQ-4245086 的修补程序
* (Brand Portal) 发布资源后允许创建子资源。NPR-23331：适用于 CQ-4242018 的修补程序
* Dynamic Media请求不使用代理/HTTP公共客户端。 NPR-10727：适用于 CQ-45695/CQ-88800 的修补程序
* 无法在Dynamic Media S7 (DMS7)中为单个演绎版MP4视频资源添加批注。 NPR-22046：适用于 CQ-4215912 的修补程序
* 对于 Tiff、金字塔生成流程，EmbedXMP 数据始终设置为“活动”。NPR-22903：适用于 CQ-4234498 的修补程序
* 大量图像预设存在动态演绎版显示/选择问题。 NPR-23151：适用于 CQ-4217511 的修补程序
* Dynamic Media编码视频 — 修改/重新上传启动器出现问题。 NPR-23237：适用于 CQ-4240260 的修补程序
* 修复了 Dynamic Media S7 中 HTTP 转发器的代理处理问题。NPR-24001：适用于 CQ-244140 的修补程序

### 站点 {#sites-8}

* 由于6.2和6.3之间的xPath转换不同而导致查询生成器不一致。NPR-23245：适用于CQ-4240396的修补程序
* 在扩展对话框时，页面属性中的缩略图选项卡不起作用。 NPR-22844：适用于 CQ-4241474 的修补程序
* Parsys 会中断模拟器设备框架宽度，并裁剪掉添加到其中的任何组件。NPR-22926：适用于 CQ-4238224 的修补程序
* 执行多次启动时，会在Author中提升该启动，但是由于缺少复制权限，因此不会在Publishing Server上复制更改。 NPR-22934：适用于 CQ-4234746 的修补程序
* 不同会话中的另一个用户可以修改第一个会话中用户锁定的页面。 NPR-23057：适用于 CQ-4199017 的修补程序
* 修复了列表视图中的可重新排序选项。 NPR-23065：适用于 CQ-4239321 的修补程序
* （页面编辑器）再次打开对话框时，图像组件上的图像消失。 NPR-23156：适用于 CQ-4239978 的修补程序
* 滚动到页面底部时，模板编辑器仅显示 20 个模板/文件夹，而不会加载其他模板/文件夹。NPR-23185：适用于 CQ-4238483 的修补程序
* （经典 UI）移动或重命名页面时产生错误。NPR-23213：适用于 CQ-4240971 的修补程序
* 无法编辑/创建 ContextHub 区段。NPR-23218：适用于 CQ-4226948 的修补程序
* （富文本编辑器）- 替换操作会更改单词的格式。NPR-23271：适用于 CQ-4239677 的修补程序
* XF变体的Blueprint选项卡中缺少转出按钮。 NPR-23320：适用于 CQ-4240404 的修补程序
* 由于已弃用，经典 UI 无法用于编辑 CUG。NPR-24122：适用于 4241823 的修补程序
* 主动式修补程序，以防止不必要的内容促销。NPR-24387：适用于 4244993 的修补程序
* 在将大约 将80个片段添加到Assets中的文件夹中，从时间线控制台触发工作流时会遇到错误。 NPR-23393：适用于 CQ-4211216 的修补程序
* 无法将图像从内容查找器拖放到富文本编辑器对话框中。 NPR-23403：适用于 CQ-4242094 的修补程序
* 将组件从 AEM 6.0 迁移到 AEM 6.2 时出现“无效的递归选择器值”错误。NPR-23532：适用于 CQ-4241258 的修补程序
* （富文本编辑器）工具提示显示插件的变量名称，而不是可读的插件名称。 NPR-23550：适用于 CQ-4243269 的修补程序
* 在手机/平板电脑版本中，无法保存带有必需选择下拉列表的对话框。NPR-23904：适用于 CQ-4243096 的修补程序
* 安装 6.3.2.1 之后，所有页面上都显示样式系统选项。NPR-23972：适用于 CQ-4244394 的修补程序
* 由于已弃用，经典 UI 无法用于编辑 CUG。NPR-24122：适用于 4241823 的修补程序
* 主动式修补程序，以防止不必要的内容促销。NPR-24387：适用于 4244993 的修补程序
* 移动资源后，不会更新资源引用。NPR-23208：适用于 CQ-4239879 的修补程序

### 平台 {#platform-1}

* 如果在搜索Facet中使用标记谓词，则智能收藏集在保存后不显示结果。 NPR-23401：适用于 Granite-21278 的修补程序
* 修补 clientlib 中的 jQuery 1.12.4 以包含安全修补程序。NPR-24128：适用于 Granite-20058 的修补程序
* 现在，在重新启动捆绑包时，将更新国际化翻译。 NPR-23193：适用于 Sling-7190 的修补程序
* ReplicationEventListener 中的资源解析程序未关闭。NPR-23240：适用于 CQ-4241350 的修补程序
* 在“每日 CQ 邮件服务”中支持 STARTTLS。NPR-23941：适用于 CQ-4240397 的修补程序
* 应根据标记标题，自动填充符合 JCR 的标记名称。NPR-24173：适用于 CQ-4199411 的修补程序

### 集成 {#integration-4}

* (Target)使用API类型（如XML）时，不会激活营销活动。 NPR-23199：适用于 CQ-4240936 的修补程序****
* 对于中间文件夹结构，配置引用复制失败。 NPR-23485：适用于 CQ-4242751 的修补程序

### 漏洞 {#vulnerability-2}

* Salesforce 集成容易遭受服务器端请求伪造 (SSRF) 攻击。NPR-24289：适用于 CQ-424527 的修补程序
* 管理员 UI 项目链接中存在跨站点脚本 (XSS) 漏洞。NPR-23272：适用于 CQ-4241795 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components}

* Foundation 表容易遭受存储型跨站点脚本攻击。NPR-23214：适用于 CQ-4240760 的修补程序

### 翻译 {#translation-3}

* 创建语言副本时，不会删除Live Copy属性。 NPR-23123：适用于 CQ-4230641 的修补程序

### 用户界面 {#user-interface-1}

* DatePicker不支持手动设置隐藏字段设置的外部类型提示。 更改类型提示会导致转换错误。NPR-23371：适用于 Granite-21194 的修补程序
* Coral.ColumnView：添加了对“按住 Shift 键单击”的支持。NPR-23404：适用于 Granite-13338 的修补程序
* 选择具有空值的项时，选择RT不会进行验证。 NPR-23405：适用于 Granite-21283 的修补程序
* (OMEGA) 仅以英语报告“功能”。NPR-23990：适用于 Granite-21231 的修补程序
* 修复了 Coral.Autocomplete API。NPR-23516

### Granite {#granite-1}

* Apache HTTP 客户端跟踪连接和高堆利用率导致 AEM 服务器崩溃。NPR-23906：适用于 Granite-21056 的修补程序

### 商务 {#commerce-2}

* 营销活动 json 输出不包含 Servlet 上下文根。NPR-23733：适用于 CQ-4243827 的修补程序

### 社区 {#communities-7}

* 在社区中搜索因几个字而失败。 NPR-23256：适用于 CQ-4240717 的修补程序
* 无法为社区管理员角色分配组的问题。NPR-23317：适用于 CQ-4241233/CQ-4221399 的修补程序
* 使用相似资源名称创建资源时出现问题。NPR-23319：适用于 CQ-4240700 的修补程序
* (ContextPath)中断消息功能因Jetty配置而中断，且在社区组成员列表中搜索组成员时出错。 NPR-23336：适用于 CQ-4241519/CQ-4242080 的修补程序
* “正在将图像上传到社区论坛”未出现在 Adobe 存储资源提供程序 (ASRP) 中。NPR-23397：适用于 CQ-4242497 的修补程序
* 已删除的构思在“活动”中显示为活动链接。NPR-23406
* 在通过上下文根运行的 AEM 中，无法加载 imsmanifest.xml。NPR-23483：适用于 CQ-4242193 的修补程序
* 旧版本的 Handlebars 中存在安全漏洞。NPR-23518：适用于 CQ-4243055 的修补程序
* 通道服务无法正常工作。NPR-23543：适用于 CQ-4242217 的修补程序
* 通过 Dispatcher 访问并为其启用 Sling 动态包含时，社区组件出现问题。NPR-23586：适用于 CQ-4242360/CQ-4241522 的修补程序
* 当使用搜索词进行搜索而产生许多结果，然后输入新的搜索词时，分页不会重置。NPR-23739：适用于 CQ-4222593 的修补程序
* 对论坛组件执行搜索时出现问题。 NPR-23838：适用于 CQ-4243770 的修补程序
* （社区审核标记）无法批量允许已标记的消息。NPR-23845：适用于 CQ-4243962 的修补程序
* 尽管选择了默认排序顺序，但排序按钮文本未显示默认选择值。NPR-23881：适用于 CQ-4243375 的修补程序
* 由于向组发送消息失败，未触发 Web 和邮件通知。NPR-23934：适用于 CQ-4242880 的修补程序
* 使用 DSRP 配置，不会显示有关标记用户和原因的详细信息。NPR-23973：适用于 CQ-4243205 的修补程序
* 来自未标记用户的标记原因仍然可见。 NPR-23974：适用于 CQ-4243822 的修补程序
* 将两个具有相同名称的文件附加到表单帖子两次，会导致服务器错误。NPR-24166：适用于 CQ-4244367 的修补程序
* 使用数据库存储资源提供程序 (DSRP) 无法存储 MIME 类型超过 15 个字符的附件。NPR-24174
* 将违反上传条件的图像拖放到帖子文本中时，将引发服务器错误，并向用户显示通用错误消息。NPR-24243
* 修复了若干 AEM Communities 服务器端问题。NPR-23971：适用于 CQ-4243144、CQ-4242145、CQ-4243365 和 CQ-4244098 的修补程序
* 修复了多个 Adobe Social 问题。NPR-24242：适用于 CQ-4245054、CQ-4245120、CQ-4245296 的修补程序

### 营销活动 {#campaign}

* 营销活动 json 输出不包含 Servlet 上下文根。NPR-23733：适用于 CQ-4243827 的修补程序

### MSM {#msm}

* 转出页面时，Live Copy 不会显示从主版继承的打开/关闭时间属性。NPR-23873：适用于 CQ-4243431 的修补程序
* Live Copy 操作不会忽略已删除组件的子节点。NPR-23058：适用于 CQ-4211662 的修补程序

### 卸载 {#offloading}

* 请求机制在处理后或定期从工作线程实例中清理资产。 NPR-23638：适用于 Granite-21337 的修补程序

## 表单 {#forms-8}

### Forms 附加组件包 {#forms-add-on-package-8}

#### 自适应表单 {#adaptive-forms-1}

* 将 `ReCaptchaConfigService` 移动到内部包。适用于 CQ-4217459 的修补程序
* 数值字段不遵循最小值。 NPR-23967：适用于 CQ-4244830 的修补程序
* 在自适应表单与 Adobe Sign 的集成中支持多分片。NPR-23383

#### 后端集成 {#backend-integration}

* (FDM)（Web 服务）在 WSDL 解析器中支持 WSDL 的扩展结构。NPR-23640
* 将 SDLInvokerParams 包含在 Forms 附加组件客户端 SDK 中。NPR-23157

### Forms JEE 安装程序 {#forms-jee-installer-7}

#### 进程管理 {#process-management}

* 应用新的axis.jar文件后无法打开工作区。 NPR-23316
* LiveCycle 在 PMAdmin 上易遭受 XSS 攻击。NPR-23267
* 升级到 AEM 6.1 Forms 后，访问特定用户的任务列表时，HTML 工作区会冻结。NPR-23943

#### 核心 {#core}

* Forms JEE 支持 PKCS#11 双向身份验证。NPR-21372

#### PDFG 服务 {#pdfg-service-2}

* 同时处理TIFF文件（大小约50 KB）时，纸张捕获服务崩溃。 NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms 服务器输出 - 缺少注释的替代描述。NPR-22207
* 对通过 Designer 和输出服务生成的 XML 表单添加 PDF/UA 支持。NPR-23132

### 6.3.2.2 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-4}

AEM 6.3.2.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_3_2_2_bundle-list.txt)

AEM 6.3.2.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### 累积修订包 6.3.2.1 {#cumulative-fix-pack-9}

AEM 累积修订包 6.3.2.1 是一个重要更新，它包括自 2018 年 4 月 AEM 6.3 服务包 2 (6.3.2.0) 正式发布以来的若干内部修补程序和客户修补程序。

**AEM 累积修订包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.10。
* 改进了经典 UI 中 Parsys 组件的呈现。
* 更新了Sling模型包以包含字符集修复。
* 将所有资源类型异步发布到 Brand Portal。
* 已将 coralui-component-richtexteditor.git 从 0.1.15 更新到 0.1.16
* 修复了下拉组件的显示/隐藏功能。
* 为核心图像组件启用了图像翻转。
* 更新了 felix http 包，以启用会话属性。

* 由于内存消耗问题，移除了 Sling 模型上的 cache=true。

### 资源 {#assets-9}

* 在资产文件夹设置中更改标题或缩略图图片时，文件夹的原始组和权限将被覆盖。 NPR-22171：适用于 CQ-4216080 的修补程序
* 当作业添加到复制队列且资产发布到Brand Portal时，UI会引发虚假错误“Publish到Brand Portal失败”。 NPR-22179：适用于 CQ-4205273 的修补程序
* （触屏 UI）列视图中资源的默认上传位置。NPR-22465：适用于 CQ-4237057 的修补程序
* 尝试将资源架构从`/conf/global`复制到`/conf/mytenant`时，AEM会引发StackOverflow错误。 NPR-22489：适用于 CQ-4235875 的修补程序
* 尝试解压缩 ZIP 存档文件失败，因为文件夹名称末尾包含空格。NPR-22522：适用于 CQ-4238036 的修补程序
* 无法使用资源标题列对搜索结果进行排序。NPR-22908：适用于 CQ-4239076 的修补程序
* YouTube 视频使用完整路径进行标记，而不是使用标记名称本身进行标记。NPR-22976：适用于 CQ-4238669 的修补程序
* 在可重新排序的文件夹下重新排序文件夹不会持久保留。NPR-23125：适用于 CQ-4231761 的修补程序
* 尝试使用共享链接共享收藏集时，出现“HTTP 504：网关超时”错误。 NPR-21928：适用于 CQ-4234507 的修补程序
* 当有多个与 PDF 资源关联的关键字时，PDF 关键字元数据无法正确提取，并且会以错误方式修改。为解决该问题，已删除 PDF 资源的“主题”字段元数据属性。但是，您可以编辑元数据架构以为主题字段添加多值文本字段。 NPR-21972：适用于 4215741 的修补程序****
* 如果在显示两个弹出窗口的间隔时间内更改了选定的文件夹，则会删除错误的资源。NPR-21980：适用于 CQ-4233675 的修补程序
* (DAM)添加到收藏集向导时，出现多个跨站点脚本(XSS)漏洞。 NPR-22432：适用于 CQ-4327086 的修补程序
* 在 Safari 上的资源中使用数字版权管理时，资源下载失败。用户无法下载包含免责声明和长文件名的资产。 NPR-22747：适用于 CQ-4236460 和 CQ-4235274 的修补程序
* 将公共共享设置为将资产发布到Brand Portal时的默认选项。 NPR-21931：适用于 CQ-4218816 的修补程序

### 站点 {#sites-9}

* 工作流收件箱中的新项目显示页面路径而非页面标题。 NPR-21634：适用于 CQ-4230672 的修补程序
* 可编辑的结构组件在编辑时丢失了响应式网格所需的CSS类名称。 NPR-21741：适用于 CQ-4232374 的修补程序
* （触屏UI）HTL组件存在多个跨站点脚本(XSS)漏洞。 NPR-21899：适用于 CQ-4232511 的修补程序
* 无法更改内容片段混合媒体图像资源类型。 NPR-21907：适用于 CQ-4233401 的修补程序
* 触屏UI对话框的RTE全屏隐藏RTE插件。 NPR-22034：适用于 CQ-4235457 的修补程序
* （触屏 UI）富文本编辑器会从 &lt;a> 标记中删除 id 以外的所有其他属性。NPR-22044：适用于 CQ-4234133 的修补程序
* 由于长时间运行的查询（超过 6 个）而导致的多个堆叠式 Parsys 致使 AEM 运行缓慢。NPR-22134：适用于 CQ-4233904 的修补程序
* 无法更改名称中带有冒号的节点的权限。NPR-22136：适用于 CQ-4236221 的修补程序
* （经典UI）富文本编辑器输出html将“list-position-style： inside；”作为内联样式添加到&lt;ul>标记中。 NPR-22145：适用于 CRTE-114 的修补程序
* 当文本为空时，使TreeNode回退到name属性。 NPR-22146：适用于 CQ-4234724/CQ-4236300 的修补程序
* 从端口 -1 到 AEM 6.3 的 RSS 馈送问题。NPR-22176：适用于 CQ-4233339 的修补程序
* （经典 UI）粘贴文本快捷键 (Ctrl+V) 对 OOTB 文本（富文本）组件不起作用。NPR-22224：适用于 CQ-4236224 的修补程序
* 键入文本时，标记字段的筛选功能无法按预期发挥作用。 NPR-22236：适用于 CQ-4236655 的修补程序
* （页面编辑器）在图像映射组件中粘贴文本数据时，也会粘贴文本组件。NPR-22264：适用于 CQ-4236230 的修补程序
* 对话框 FileUpload 必填字段在提交对话框时导致出现问题。NPR-22464：适用于 CQ-4222192 的修补程序
* 如果无法激活移动的页面或其反向链接，则在具有或没有复制权限的情况下移动会启动激活工作流的请求。NPR-22467：适用于 CQ-4211765 的修补程序
* 加载包含大量（2000 及以上）受众的页面时，出现性能问题。NPR-22478：适用于 CQ-4209567 的修补程序
* 初始化期间ContextHub存储覆盖默认持久层时出现持久性问题。 NPR-22479：适用于 CQ-4218399 的修补程序
* 如果没有在第一个内容根上选中“包含子页面”，则包含多个页面的启动不会将子页面发布到发布服务器。 NPR-22482：适用于 CQ-4237818 的修补程序
* （触屏UI）通过经典UI控制台删除启动项会使所有页面无法编辑。 NPR-22491：适用于 CQ-4225074 的修补程序
* 由于对话框中有多余空间，图像组件出现问题。NPR-22528：适用于 CQ-4238183 的修补程序
* 使用内联模式打开组件时，之前加载的插件再次不可见。 NPR-22591：适用于 CQ-4236850 的修补程序
* 删除嵌套启动项中的启动项，会导致子启动项变得孤立。NPR-22621：适用于 CQ-4202639 的修补程序
* （经典 UI Sidekick）当页面处于工作流锁定阶段时，“工作流”选项卡被禁用。NPR-22722：适用于 CQ-4237557 的修补程序
* 在页面上翻转添加到图像组件中的图像后，更改未保存，并且原始图像显示在页面上。 渲染支持已通过 [https://github.com/adobe/aem-core-wcm-components/pull/141](https://github.com/adobe/aem-core-wcm-components/pull/141) 添加到图像核心组件。NPR-22801：适用于 CQ-4221539 的修补程序
* 当用户尝试从锚点菜单中删除现有锚点时，富文本编辑器组件窗口将关闭，并且更改保持未保存状态。 NPR-22802：适用于 CQ-4238167 的修补程序
* Omnisearch筛选器未显示站点控制台中的所有操作。 NPR-22804：适用于 CQ-4239007 的修补程序
* 操作系统剪贴板以及内部 AEM 剪贴板的触屏 UI 中存在复制/粘贴问题。NPR-22807：适用于 CQ-4220383 的修补程序
* Lucene 搜索返回的“摘录”高亮显示内容不一致。NPR-22879：适用于 CQ-4238513 的修补程序
* 激活具有发布实例的页面时，会导致处于绿色状态而不是变为琥珀色。 NPR-22927：适用于 CQ-4236310 的修补程序
* (StyleSystem) 从弹出窗口中选择样式时，屏幕位置会跳转。NPR-23183：适用于 CQ-4238867 的修补程序
* （管理发布）需要多次单击才能移至日历的下一个月。 NPR-23508：适用于 CQ-4242732 的修补程序

### 平台 {#platform-2}

* Sling导出程序servlet无法正确导出日语字符。 NPR-22153：适用于 CQ-4228920 的修补程序
* 启动过程中出现调度程序死锁。NPR-22440：适用于 Sling-7004 的修补程序
* 无法在两个发布实例之间同步组。NPR-21943：适用于 Granite-19564 的修补程序
* org.apache.sling.i18n 共享会话/资源解析程序存在性能问题。NPR-23390：适用于 Sling-7543 的修补程序

### 集成 {#integration-5}

* com.day.cq.analytics.sitecatalyst 中的资源解析程序未关闭。NPR-22323：适用于 CQ-4236515 的修补程序
* 在长时间运行的查询期间，TargetContentImpl 致使 AEM 运行缓慢。NPR-22361：适用于 CQ-4236907 的修补程序
* 目标引擎(mbox.js、at.js)不使用损坏的URL。 并且，使用的URL包含冒号，在某些部署中可能会失败。 NPR-22366：适用于 CQ-4237854 的修补程序
* 提供自定义at.js或mbox.js时，系统会将包含的脚本作为文本写入页面，而不是HTML标签。 NPR-22441：适用于 CQ-4203691 的修补程序
* 在 Target 模式中，作者可以修改从 Blueprint 继承的组件，而无需取消继承。NPR-22751：适用于 CQ-4237907 的修补程序
* 由于缺少`jcr:content`节点，PersonalizationDataSource引发空指针异常。 NPR-22850：适用于 CQ-4222122 的修补程序
* 使用非英语时，AEM定位失败。 NPR-22917：适用于 CQ-4218213 的修补程序
* 发布具有目标内容的页面会丢失相关资源。NPR-23064：适用于 CQ-4227119 的修补程序
* 用户在mbox调用中看不到测试静态参数值，而在云配置中使用AT.js作为客户端库进行测试时，则可以看到这些值。 NPR-21930：适用于 CQ-4234520 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-1}

* 取消选中“取消/禁用继承”复选框后，iParsys将创建位置偏移。 NPR-21905：适用于 CQ-4230951 的修补程序
* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-22327：适用于 CQ-4222853 的修补程序
* 为了提高安全性，已弃用CAPTCHA组件。 如果您使用的是CAPTCHA组件，则在安装6.3.2.1或更高版本后，将显示“Captcha组件已弃用，不应再使用”消息。 可以自定义 AEM 组件来包含 reCAPTCHA 以提高安全性。NPR-22151：适用于 CQ-4220052 的修补程序

### WCM - 页面编辑器 {#wcm-page-editor}

* 使用无效选择器时出现反射式跨站点脚本(XSS)。 适用于 CQ-4270397 的修补程序

### 翻译 {#translation-4}

* 调查预览功能存在的问题。NPR-22114：适用于 CQ-4223753 的修补程序

### 用户界面 {#user-interface-2}

* 设置“最小”和“最大”日期范围时，Coral 日历月份选取器出现问题。NPR-22716：适用于 CUI-7187 的修补程序
* （经典UI）即使关联的表单数据模型服务设置为空字段，组件也会显示默认值。 NPR-22272：适用于 GRANITE-19744 的修补程序

### Granite {#granite-2}

* 内存泄漏导致资源共享 AEM 发布者实例出现稳定性问题。NPR-22205、NPR-23178：适用于 Sling-5668、Sling-7292 和 Sling-7470 的修补程序。
* 不应使用会话属性名称的不稳定服务 ID。NPR-22821：适用于 Granite-21059 的修补程序
* 当 http 白板管理的会话失效时，如果容器会话不含其他会话属性，则容器会话也将失效。NPR-23059：适用于 FELIX-5819 的修补程序
* LogbackManager在启动时可能缺少某些OSGi配置。 NPR-23060：适用于 Granite-19791 的修补程序

### 商务 {#commerce-3}

* 支持在体验片段菜单中创建工作流。 NPR-22347：适用于 CQ-4221661 的修补程序
* 体验片段错误在 WeRetail 上可重复出现。NPR-21958：适用于 CQ-4220061 的修补程序
* 激活包含已删除体验片段的页面会引发 NullPointerException。NPR-23179：适用于 CQ-4239939 的修补程序

### 项目 {#projects}

* （多语言项目）项目不会列出超过 19 种语言的翻译作业。NPR-22498：适用于 CQ-4229978 的修补程序

### 工作流 {#workflow}

* （经典 UI）启用或禁用工作流启动器会导致不良行为。NPR-22907：适用于 CQ-4239153 的修补程序

## 表单 {#forms-9}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

AEM Forms 的主要功能亮点包括：

* 添加了对 HTML5 输入类型的支持。
* 修复了基本 SOAP 标头身份验证问题。
* 添加了对超链接的标题属性的支持。
* 在 Forms Designer 的辅助功能树中启用了 PDF/UA 标识符。
* 为 Workbench 用户启用了证书身份验证。
* 添加了对生成PDF/A-2a或PDF/A-3a兼容PDF文件的支持。

### Forms 附加组件包 {#forms-add-on-package-9}

#### 表单 - 管理员 UI {#forms-admin-ui}

* 当您在ECM Connectors的“配置”页面上检查“密码”字段时，密码以纯文本形式显示。 NPR-22508：适用于 CQ-4236065 的修补程序

#### 表单服务 {#forms-service}

* 启用 SSL 后，“提交”和“放弃”事件不适用于表单分析。NPR-22637：适用于 CQ-4237973 的修补程序

#### 用户管理 {#user-management}

* 由于 cglib-nodep 版本不正确，无法同步 LDAP。NPR-22493：适用于 CQ-4234099 的修补程序

#### 自适应表单 {#adaptive-forms-2}

* 规则编辑器的自定义函数在函数调用后添加一个额外的；。 因此，即使自定义函数返回true，它们也会导致验证失败。 NPR-22481：适用于 CQ-4235499 的修补程序
* 显示最小和最大验证消息时，无论选择的日期模式如何，日期选取器组件都不会遵循该模式。 NPR-22444：适用于 CQ-4236269 的修补程序
* 提交请求中发送的日期格式应与日期选取器组件中提供的模式一致。 NPR-22384
* 在 Android™ 6.0 Samsung 设备上不接受为自适应表单文本框指定的最大字符数。NPR-22363、NPR-22364：适用于 CQ-4235205 的修补程序
* (Microsoft® Edge) (IE 11)具有多行字段的自适应表单文本字段组件将`Null`显示为默认值，而不是空白。 NPR-22284：适用于 CQ-69107 的修补程序
* 自适应表单中的 SOAP UTF-8 输入编码会返回页面乱码错误。NPR-20105：适用于 CQ-4222669 的修补程序
* 一旦在AEM Forms页面中配置了错误的表单，AEM Sites容器组件便无法编辑。 适用于 CQ-4237456 的修补程序
* 在JEE服务器上运行开发测试时失败。 适用于 CQ-4222082 的修补程序
* 由于Calvin框架中的缩小问题，JEE服务器上的AF测试失败。 适用于 CQ-4217220 的修补程序

#### Forms Manager {#forms-manager}

* (Firefox) 无法更新自适应表单的 XML 架构属性，因为记录文档 (DOR) 中的选项未在属性页面中预先选择。NPR-22298：适用于 CQ-4237402 的修补程序
* 发布页面后修改的Forms不会再发布。 NPR-23013：适用于 CQ-4236566 的修补程序

#### 后端集成 {#backend-integration-1}

* SOAP 服务的 OOTB 基本身份验证不适用于 FDM 集成中的基本身份验证。NPR-23238：适用于 CQ-4241308 的修补程序

#### 通信管理 {#correspondence-management}

* 在信件内部使用并预览 OOTB XDP 时，会显示内容与页脚重叠。适用于 CQ-4212414 的修补程序

#### 汇编程序服务 {#assembler-service}

* 关于 PDF/A-1b 合规检查错误的 Acrobat DC 报告和 AEM 报告存在差异。NPR-22051、NPR-22050：适用于 CQ-4226128、CQ-4227671 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-8}

#### Workbench {#workbench}

* 为 Workbench 用户启用了证书身份验证。NPR-20644：适用于 CQ-4214486 的修补程序
* 使用 Workbench 下载服务器日志，仅适用于一台服务器，而不适用于另一台服务器。NPR-21079：适用于 CQ-4229842 的修补程序

#### 进程管理 {#process-management-1}

* （HTML 工作区）滚动条存在屏幕大小问题。NPR-23288
* （HTML 工作区）进程起点未按字母数字顺序排序。NPR-22841：适用于 CQ-4238944 的修补程序
* (HTMLWorkspace)关闭工作区中的表单时会触发准备数据。 NPR-21127：适用于 CQ-4224574 的修补程序
* （HTML 工作区）调用的进程需要较长说明的注释时，“注释”展开按钮不起作用。适用于 CQ-4241488 的修补程序

#### 核心 {#core-1}

* 在启动过程中启动调度程序时遇到错误。NPR-22990
* 阻止浏览器存储输入到HTML表单中的凭据。 NPR-21762：适用于 CQ-4206543 的修补程序
* 应修复 Core 静态代码分析中报告的问题。适用于 CQ-104446 的修补程序

#### PDFG 服务 {#pdfg-service-3}

* PDF Generator 无法生成具有指定书签级别的 PDF 文档。NPR-22921、NPR-22285：适用于 CQ-4230562 的修补程序
* 添加了对生成PDF/A-2a或PDF/A-3a兼容PDF文件的支持。 NPR-23021：适用于 CQ-4214172 的修补程序

#### Forms Designer {#forms-designer-1}

* 从Designer另存为PDF时缺少PDF/UA标识符。 NPR-23137
* 从 Designer 中另存为 PDF 时，不会标记路径对象（例如：边框，下划线和超链接）。NPR-23136
* 从 Designer 中另存为 PDF 时，图像对象没有边界框。NPR-23134
* 从Designer另存为PDF时，在Designer中定义的内联超链接不会进行标记，或者它们具有替换文本。 NPR-23133
* 使用 AEM 6.3 Forms Designer 打开 XML 数据包，会从 XML 源中移除 XHTML 格式。NPR-21178：适用于 LC-3917046 的修补程序

#### 安装 LCM {#install-lcm}

* 在安装程序和 LCM 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21370

#### 签名服务 {#signatures-service}

* 通过HSM对PDF文档进行数字签名时遇到异常。 NPR-21154：适用于 CQ-4226978 的修补程序

### 6.3.2.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-5}

AEM 6.3.2.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list_002_.txt)

AEM 6.3.2.1 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_comparison.txt)

AEM 累积修订包 6.3.1.2 是一个重要更新，它包括自 2017 年 10 月 AEM 6.3 服务包 1 (6.3.1.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包的主要功能亮点包括：

* 修改了 UI，以支持在 AEM Assets 中实施 CUG 功能。
* 修复了许可证检查页面上的 UI 问题，以优化体验。
* 在 AEM Forms 应用程序中启用了 OSGi 工作流任务支持。

### 资源 {#assets-10}

* 修改了 UI，以支持在 AEM Assets 中实施 CUG 功能。NPR-19485
* 使用触屏 UI 将资源上传为其自身的直接子节点会导致出现问题。资源会作为先前选定的资源的直接子级上传。NPR-19736
* 加载已保存的搜索/智能收藏集时，“日期范围”谓词和“范围”谓词不起作用。NPR-19844：适用于 CQ-4220808 的修补程序
* 将多个资源（超过 4 个）发布到 Brand Portal 时，AEM 实例运行缓慢。NPR-20009：适用于 CQ-4213426 的修补程序
* 无法从许可证检查页面下载带空格的资产。 NPR-20067：适用于 CQ-4216557 的修补程序
* 上传具有多个 Alpha 层的 PSB 文件时出现处理问题。NPR-20250：适用于 CQ-4220869 的修补程序
* 用户无法下载定义了长文件名和免责声明的资产。 NPR-20254
* ProductAssetsUploader将Java™缓存的临时文件放在Java™ TEMP文件夹中。 NPR-20256：适用于 CQ-4221801 的修补程序
* 由于许可问题，使用 Adobe 专有代码替换版本比较代码。NPR-20272：适用于 CQ-4223758 的修补程序
* 字符串属性 documentNumber 的元数据显示为日期，然而它应该是数字。NPR-20291：适用于 CQ-4223991 的修补程序
* 受损 PDF 的文本提取卡住。NPR-20416：适用于 CTG-4150375 的修补程序
* 无法正常下载其中包含具有 UTF-8 不兼容名称的资源的压缩文件。NPR-20420：适用于 CQ-4219961 的修补程序
* OmniSearch中的字符过多可能会导致AEM服务器崩溃。 NPR-20434：适用于 CQ-4223602 的修补程序
* DAM资产API元数据缺陷导致xmp回写API受损。 NPR-20607：适用于 CQ-4220455 的修补程序
* 将用户添加到收藏集时出现性能问题。NPR-20699：适用于 CQ-4225733 的修补程序
* 对于 Dynamic Media 集，不应允许从 AEM 发布到 Brand Portal。NPR-20320：适用于 CQ-4221147 的修补程序
* 含有空格和重音符号的视频不会在“呈现版本”页面上生成任何视频。NPR-19961：适用于 CQ-4221014 的修补程序
* 解决了资源 API 的多个文件夹处理问题。NPR-20569
* AEM Dynamic Media Classic(以前为Scene7)无法从AEM服务器同步资产。 当Cloud Service配置中的目标路径指向根路径子文件夹时，会发生此问题。 CQ-4228265
* 添加了 Apache Commons `{org.apache.commons/commons-email/1.5}` 的电子邮件包，用于替换 `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`。

### 站点 {#sites-10}

* 管理员权限问题：无法从页面属性中删除“已关闭的用户组”成员。NPR-20631
* 在通过“管理发布”发布页面时，键入的工作流名称应该可在“通知”框中使用。 NPR-20046：适用于 CQ-4221586 的修补程序
* 在富文本编辑器中的两行上应用样式化文本，然后将它们合并为一个段落，会删除样式化跨区。NPR-20110：适用于 CQ-4223051 的修补程序
* 在“属性”编辑对话框的多个选项卡中对字段属性所做的更改有时不会保存。NPR-20286
* 内容片段中粘贴内容的末尾出现意外标记。 NPR-20413：适用于 CQ-4224014 的修补程序
* 在 Adobe Campaign 中实施了一种机制，用于从外部定位资源中获取内容资源的策略。NPR-20667
* 富文本插件不适用于多字段触屏UI中的内嵌和全屏栏。 NPR-20973

### 营销活动 {#campaign-1}

* 占位符在包含多个 Parsys 组件的页面中不可见。NPR-20436：适用于 CQ-4215000 的修补程序

### 商务 {#commerce-4}

* 无法在 Internet Explorer 11 中正确显示体验片段。NPR-20161：适用于 CQ-4223319 的修补程序
* 在商务工作流中，当基于具有多个图像的主要产品创建变量时，会自动插入空白图像。NPR-20068：适用于 CQ-4222048 的修补程序
* 产品控制台中的“按收藏集页面上的标记筛选”不起作用。NPR-20292：适用于 CQ-4224023 的修补程序

### 社区 {#communities-8}

* 搜索结果与搜索结果组件不一致。NPR-20070：适用于 CQ-4220913 的修补程序
* 在已发布的组件上，与审查方相关的任何活动均不会触发电子邮件通知。NPR-20122
* 对于匿名社区用户，将显示无结果的空白分页。NPR-20136：适用于 CQ-4220738 的修补程序
* 配置警报触发器，当检测到 UGC 为垃圾邮件或用户在预先审核的站点上发帖时，触发警报。NPR-20274：适用于 CQ-96850 的修补程序
* 解决了 AEM Communities 站点页面中的多个问题，包括错误的重定向和页面刷新问题。NPR-20344
* CommunityUserOperationExtension 出现类强制转换异常。NPR-20532：适用于 CQ-4224385 的修补程序
* 创建社区站点后，用户无法从站点地图中打开它，因为上下文路径未添加到URL前面。 NPR-20730

### 集成 {#integration-6}

* 将 Analytics 现有凭证迁移到 WSSE 身份验证。NPR-19962：适用于 CQ-4218071 的修补程序
* 执行任何修改后重新激活区段失败，并引发错误。NPR-20054：适用于 CQ-4218401 的修补程序
* Search&amp;Promote云服务配置忽略表单检索方法，导致其在创作实例上不可用。 NPR-20447：适用于 CQ-4206076 的修补程序
* 安装Search&amp;Promote功能后，内容包中模糊不清的过滤器定义会导致路径被覆盖。 NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* 每次显示TXT类型资产的属性时，其元数据属性会显示在不同的元数据编辑器中。 NPR-20239

### 平台 {#platform-3}

* 解决了资源解析程序未关闭的异常。NPR-19749：适用于 Granite-19143 的修补程序
* 请求在操作功能板中显示自定义卡片，以及默认的运行状况检查。NPR-20145
* 页面编辑器的注释层在Internet Explorer 11中无法正常工作。 NPR-20222：适用于 CQ-4222818 的修补程序
* 在复制代理中将用户代理设置为管理员时出现会话泄漏。NPR-20578
* 对于其他data-sly-resource语句，现在未设置requestAttributes。 NPR-20639：适用于 4226206 的修补程序
* 修复了 AEM 中 OOTB 资源的 curl Head 请求问题。NPR-20781：适用于 CQ-4221520 的修补程序

### 项目 {#projects-1}

* 从项目控制台访问不同的项目时，需要较长时间才能加载。 NPR-20314
* 安装 AEM 6.3.0.1 会删除 `dam-update-service` 用户的密钥库。NPR-20018
* 在某些自定义部署中，用户尝试在addTask模块中选择被分配人时，需要较长时间才能填充用户选取器中的列表。 NPR-20283：适用于 CQ-4224193 的修补程序

### 用户界面 {#user-interface-3}

* 无论对话框中的属性如何，“颜色”字段均设置为“始终必需”。 NPR-19702
* 在 Internet Explorer 11 上，以全屏模式显示的组件多字段的滚动条不会显示。NPR-20261：适用于 CQ-4219782 的修补程序
* 如果触发连续查询导致不正确的结果，之前的查询不会被中止。NPR-20398：适用于 GRANITE-19306 的修补程序

### 工作流 {#workflow-1}

* 用户在其收件箱中收到工作流任务时，不会发出相关通知。NPR-20213：适用于 CQ-4221639 的修补程序
* 在单击工作流模型的对话框参与者步骤中的下拉列表后，OOTB Granite 用户选取器未加载任何用户。NPR-20236

## 表单 {#forms-10}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-10}

#### 自适应表单 {#adaptive-forms-3}

* 缺少对重复面板的整合表达式的支持。NPR-20861
* 即使关联的表单数据模型服务未返回值，下拉菜单仍显示上次存储的值。 NPR-20710
* 无法在规则编辑器中编辑具有布尔约束条件的现有规则。NPR-21128

#### 表单门户 {#form-portal}

* 即使自适应表单的资源类型不是 XDP，也会为其显示 HTML 配置文件。NPR-20079

#### 后端集成 {#backend-integration-2}

* 无法将Switch组件的值设置为true或false。 NPR-21111

#### OSGi 工作流 {#osgi-workflow}

* 管理工作流提交仅列出十个应用程序。CQ-4230193

#### HTML5 表单 {#html-forms-3}

* 如果在辅助功能配置中未定义，则XDP表单对象（例如子表单）的名称会显示为其工具提示。 NPR-20523

### Forms JEE 安装程序 {#forms-jee-installer-9}

#### 进程管理 {#process-management-2}

* FormSetPrefillApp起点未预填充AEM Forms应用程序中的表单集字段。 NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* 安装最新的 CTJPEG2K 库，以解决关键安全漏洞。这会影响 XMLFM（AEM 和 IfBA）、RM、PDFG 模块。NPR-20625：NPR-21337。

### 包含的功能包 {#feature-packs-included}

#### AEM Forms 应用程序 {#aem-forms-app}

* 在 AEM Forms 应用程序中启用了 OSGi 工作流任务支持。CQ-4222638

### 6.3.1.2 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-6}

AEM 6.3.1.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_3_1_2-bundle-list.txt)

AEM 6.3.1.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM 累积修订包 6.3.1.1 是一个重要更新，它包括自 2017 年 10 月 AEM 6.3 服务包 1 (6.3.1.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包的主要功能亮点包括：

* 为默认的元数据架构表单启用了“发布到Brand Portal”操作。
* 对于将dc： title属性设置为`String [] (multifield)`的图像，在图像卡片上显示标题时发生行为更改。
* 将服务器端的时间渲染替换为基础时间组件。
* 启用了从tagadmin/tagging控制台将标记从AEM发布到Brand Portal的功能。
* 发布了JSON API以使用内容片段。
* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.5。

### 资源 {#assets-11}

* 将具有相同属性的两个字段映射到不同类型的属性字段会引发内部错误。 NPR-19462：适用于 CQ-4216828 的修补程序
* dc: title 和 dc: description 在 CRXDE Lite 中不会更改为多字段值。NPR-19570：适用于 CQ-4209086 的修补程序
* 动态查看器会在创作模式下加载品质最低的视频呈现版本，用于测试视频播放体验。NPR-19004
* 无法为名称中包含空格的资源下载动态呈现版本。NPR-19433：适用于 CQ-4211738 的修补程序
* 无法使用Chrome在列视图中加载页面/资源的完整列表。 NPR-19566：适用于 CQ-4214248 的修补程序
* 选择任何架构、搜索 Facet 或预设时，“发布到 Brand Portal”选项不可用。NPR-19550
* 在列视图中选择资源并单击“编辑”时，页面会返回错误。NPR-20301：适用于 CQ-4224052 的修补程序
* 跨越正负时区时，会关闭“资源到期”显示。NPR-20329：适用于 CQ-4219333 的修补程序

### 营销活动 {#campaign-2}

* 为营销活动选择默认体验后，营销活动滑块组件未显示。NPR-19213

### 集成 {#integration-7}

* 使用匿名用户访问时，自定义 at.js 文件不会发布。NPR-19542：适用于 CQ-4219592 的修补程序
* 配置向导中的“定位引擎”字段设置为ContextHub (AEM)，而不是Adobe Target。 NPR-19320：适用于 CQ-4218465 的修补程序
* 创建体验时，受众部分损坏。 NPR-19110
* 如果编辑并保存目标模块多次，则定位模式下不会显示“定位”对话框。 NPR-19144：适用于 CQ-4216708 的修补程序
* 在经典 UI 上的 Adobe Digital Publishing Solution 中，文章的访问属性设置不正确。NPR-19367
* 如果用户可以访问多个区域，通过 Campaign 个性化选件时，会出现自动折叠的错误行为。NPR-19290：适用于 CQ-4218029 的修补程序

### 站点 {#sites-11}

* 将实例升级到 AEM 6.1SP2-CFP3 后，由于 Sidekick.js 中的变更代码，多复合字段下拉列表值不会重新填充。NPR-19450：适用于 CQ-4194771 的修补程序
* 在创作模式下，WCMMode.EDIT不适用于目标组件。 NPR-19387
* 发布了JSON API以使用内容片段。 NPR-19500
* 在创作对话框中，粗体、斜体、下划线功能不适用于富文本编辑器字段。 NPR-19670、NPR-19718：适用于 CQ-4219088 的修补程序

### Mobile On-Demand {#mobile-on-demand-1}

* AEM文章控制台存在呈现问题，因为使用全尺寸图像使其速度变得缓慢。 NPR-19088

### 翻译 {#translation-5}

* 无法生成翻译项目的预览。NPR-19289

### 安全 {#security}

* SSL 连接错误。无法与服务器建立安全连接。NPR-19628

### 社区 {#communities-9}

* 使用预先审核的站点发布内容时会触发邮件。NPR-20008
* 电子邮件通知不适用于已发布组件上与审查方相关的任何活动。NPR-19767：适用于 CQ-4218060 的修补程序

### 平台 {#platform-4}

* AEM 生产服务器部署存在稳定性问题。NPR-19707
* 升级到AEM 6.3后，未找到引用作为脚本实施的标记的自定义标记库。NPR-19087
* AEM 6.3.1 的 HTL 错误修复。NPR-19161
* 富文本字段在多字段组件中不可编辑。NPR-19604：适用于 Granite-16755 的修补程序
* Adobe 电子邮件模板服务会将标记添加到自定义用户模板。NPR-19190
* 适用于 Oak 1.6.5 的修补程序。NPR-19148

### 商务 {#commerce-5}

* 选择XF变体编辑器后，“启动工作流”按钮不起作用。 NPR-19642：适用于 CQ-4207796 的修补程序

### 项目 {#projects-2}

* 项目编辑者无法将资产复制并粘贴到项目资产文件夹中。 NPR-19619：适用于 CQ-4215321 的修补程序

### 网站内容管理 {#web-content-management}

* 在转出屏幕中，无法选中或取消选中与Live Copy页面对应的复选框。 NPR-19518
* 无法正确使用页面属性的批量编辑，因为当前所有选项卡和字段都可用于批量版本。NPR-19451
* 在经典UI中编辑图像时，OOTB属性和图像对齐方式属性未显示。 NPR-19488：适用于 CQ-4217914 的修补程序

### 用户界面 {#user-interface-4}

* 使用Google Chrome浏览器时，用户无法使用触屏UI中的列视图加载页面/资源的完整列表。 NPR-19566：适用于 CQ-4214248 的修补程序

### Brand Portal {#brand-portal-1}

* 无法通过 AEM 发布带有评论和注释的资源。NPR-19590：适用于 CQ-4218386 的修补程序
* 启用通过tagadmin/tagging控制台将标记从AEM发布到Brand Portal的功能。 NPR-20271：适用于 CQ-4223948 的修补程序
* 修复 Brand Portal 云服务配置 UI 上的“已启用”字段。适用于 CQ-4211101 的修补程序
* 搜索表单复制失败。适用于 CQ-4220080 的修补程序

## 表单 {#forms-11}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-11}

#### 自适应表单 {#adaptive-forms-4}

* 提交到JEE工作流未从JEE端将输出参数返回到AEM，并引发“由于值非原始值而忽略”错误。 NPR-20265
* 在 Safari 中，自适应表单不允许将 PDF 作为附件。NPR-19625
* RestoreGuideState将覆盖customcontextproperty映射。 CQ-4222877
* 使用Cloud Service配置Google `reCaptcha`时，在需要配置org.apache.http.proxyconfigurator以进行外部连接的环境中，POST调用似乎不会通过PROXY。 NPR-20454
* 安装时基于XSD架构的自适应Forms对数字字段提交有问题的XML值，这些字段的区域设置具有除句点(.)之外的小数分隔符 从而导致出现错误。NPR-20444
* 向第三方服务器发出HTTP请求时，不接受为“Apache HTTP组件代理配置”设置的代理设置。 使用 HTTP GET 或 POST 调用时出现连接超时问题。NPR-20457、NPR-20456、NPR-20455、NPR-20451

#### 表单数据集成 {#forms-data-integration}

* 对于非英语区域设置，UTF-8 字符作为 SOAP 服务的输出未正确复制到自适应表单字段中。NPR-20238：NPR-20103

#### 通信管理 {#correspondence-management-1}

* 从 Word 文件中复制粘贴的内容在文本编辑器中丢失其内容颜色和字体。NPR-19521

#### 汇编程序服务 {#assembler-services}

* 在验证文档是否符合 PDFA-1b 格式时，Acrobat 与 AEM 结果之间存在差异。NPR-19280

#### 工作流 {#workflow-2}

* 工作流签名步骤允许 HTTP 调用通过代理连接。NPR-20529

#### HTML5 表单 {#html-forms-4}

* 添加了对 preSubmit 事件的支持。NPR-20604

### Forms JEE 安装程序 {#forms-jee-installer-10}

#### 进程管理 {#process-management-3}

* 将表单最大化/最小化并将其另存为草稿或转发后，工作流“附件”、“注释”和“详细信息”选项卡在工作区中无法使用。 NPR-20243
* 在HTMLWorkspace中提交数据后，多行文本字段(TextArea)未保留文本中的新行字符或换行符。 NPR-20085

#### 进程报告 {#process-reporting}

* 由于空指针异常，进程报表无法正确获取数据。 NPR-19759

>[!NOTE]
>
>安装[AEM Forms发行版](aem-forms-releases.md)文章中列出的LiveCycle嵌入包以解决该问题。

#### 标准服务 {#standard-services}

* docConvertor 不支持 PDF 中的拼合透明度，且无法生成 PDF/A。NPR-16228：适用于 CQ-4214488 的修补程序

#### 核心 {#core-2}

* 当在 JBoss® 应用程序上的群集配置中运行的 AEM Forms 服务器停止时，应用程序服务器从数据库断开连接。这可能导致数据损坏问题。NPR-19724

### 包含的功能包 {#feature-packs-included-1}

* 无法将下拉元数据架构字段设为必填字段，因为资源缺少必填字段验证。 NPR-17882：适用于 CQ-4208373 的修订包

### 6.3.1.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-7}

AEM CFP 6.3.1.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list.txt)

AEM CFP 6.3.1.1 中包含的内容包列表

[获取文件](assets/do-not-localize/content-package-list.txt)

AEM 累积修订包 6.3.0.2 是一个重要更新，它包括自 2017 年 4 月 AEM 6.3 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修订包的主要功能亮点包括：

* 用户访问控制的可审核性
* 包含内置存储库 (Apache Jackrabbit Oak) 版本 1.6.2
* 解决了资源解析程序未关闭的问题
* 简化了智能内容服务的配置
* 解决了内容片段验证问题
* 改进了混合设备上元数据架构的可编辑性
* 解决了 Live Copy 中的组件级同步问题
* 改进了列视图中内容繁多的页面的可用性
* 改进了长标题页面的页面命名约定的合规性
* 改善了触屏 UI 上的营销活动个性化体验
* 修复了各种项目叠加问题

### 平台 {#platform-5}

* 适用于 Oak 1.6.2 的修补程序。NPR-16993
* 使用筛选器打开 OmniSearch 时，不再设置路径。NPR-17398：适用于 CQ-4204870 的修补程序
* AEM 中用户权限更改的可审核性要求。NPR-17061
* 延迟的 DM 云服务连接导致“打开的文件太多”异常。CQ-4211407

### 资源 {#assets-12}

* 使用不同选项配置智能内容服务时出现可用性问题。NPR-18200：适用于 CQ-4201557 的修补程序
* 在到 S3 数据存储的二进制流中出现资源泄漏。NPR-18041：适用于 CQ-4209506 的修补程序
* 将 ASCII/UTF-8 编码文本文件上传到 AEM Assets 时出现错误，并且缩略图生成失败。NPR-18006：适用于 CQ-4209345 的 CFP
* 默认元数据架构导致内容片段验证失败。 NPR-17769：适用于 CQ-4211111 的修补程序
* com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner 中的资源解析程序未关闭。NPR-17598：适用于 CQ-4209018 的 CFP
* 请求创建多个复制代理，以便将资源发布到 Brand Portal。NPR-17189
* 日语文件夹下资产的审核任务不起作用。 CQ-4204782
* 将资产从其属性页面移动时，会发生空指针异常。 CQ-4204251
* 如果资源多次链接到 InDesign 文档，则 AEM 无法在属性页面中跟踪对资源的后续引用。CQ-4204186
* 在混合设备上的Chrome中编辑元数据架构表单时，在该表单中添加新选项卡时出现问题。 CQ-4201810
* 上传了重复的资源时，即使未在“检测到的重复项”对话框中选择选项，（删除/保留）选项也将应用于所有资源。 CQ-4201673
* 移动具有超过 150 个传入引用的资源文件夹时，会引发空指针异常。CQ-4200981
* 对于已下载的资源文件夹，如果解压缩 ZIP 文件的内容时发生冲突，则默认选项会显示为“创建版本”，而不是“保留两者”。CQ-97800
* 对应用程序具有只读权限的用户无法从AEM Mobile内容管理预览内容。 NPR-17486：适用于 CQ-4209690 的 CFP
* “创建目录”按钮在“目录”控制台的列视图中不起作用。 CQ-4209952

### 站点 {#sites-12}

* 通过 data-sly-resource 属性嵌入图像/视频组件时出现问题。NPR-18182：适用于 CQ-4212100 的 CFP
* 在LiveCopy中重新应用继承时，修改的本地化组件不会恢复到其原始形式。 NPR-18172：适用于 CQ-4211379 的修补程序
* 在触屏 UI 的列视图中浏览内容繁多的页面时出现问题。NPR-17799：适用于 CQ-4199611 的修补程序
* `com.day.cq.wcm.core.impl.VersionManagerImpl` 中的资源解析程序未关闭。NPR-17789：适用于 CQ-4211152 的 CFP
* 长页面标题的页面名称不会按照惯例生成。 NPR-17633：适用于 CQ-4209056 的修补程序
* 在 JBoss® EAP 6.4 上部署的 AEM 6.3 中的触屏 UI 上创建页面时出现问题。NPR-17589：适用于 CQ-4210137 的修补程序
* 当存在嵌套组时，工作流状态提供程序会导致实例锁定。 NPR-17556：适用于 CQ-4202056 的 CFP 请求
* 以下对象中的资源解析程序未关闭：

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497：适用于 CQ-4208673 的 CFP
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495：适用于 CQ-4208668 的 CFP
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494：适用于 CQ-4208669 的 CFP
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493：适用于 GRANITE-17404 的 CFP

### 集成 {#integrations-1}

* 解决了在 AEM Day HTTP Client 3.1 OSGi 配置了需要摘要身份验证的代理时可能发生的 AEM 搜索组件错误。NPR-18128：适用于 NPR-18029 的修补程序
* 通过经典 UI 个性化营销活动和关联的体验时出现问题。NPR-18127：适用于 CQ-4211559 的修补程序
* 将品牌/区域设置为站点的根页面后，子页面中的“区域”继承一旦取消，将无法恢复。NPR-17753：适用于 CQ-4210139 的修补程序

### 工作流 {#workflow-3}

* 在非瞬态工作流中，在外部流程步骤之前所做的流程历史记录和元数据更改不会持久保留。NPR-17848：适用于 GRANITE-17757 的修补程序
* 工作流对话框字段中的值不会持久保留在工作项目节点中。NPR-17734：适用于 CQ-4210369 的修补程序
* 从收件箱编辑任务时出现无法分析的日期错误。 CQ-4208749

### 项目 {#projects-3}

* 修复了各种项目叠加问题。NPR-17733
* 重组项目模块中的面板会降低其可配置性。CQ-4209859
* 当页面添加到翻译作业时，资源路径会更改为相应的本地化站点。CQ-4206007

### 安全 {#security-1}

* 上传 LDAP 用户的头像图像时出现问题。NPR-16561
* 请求在Apache Sling API中使用org.apache.sling.servlets.post servlet的升级版本(2.3.22)来防御XSS漏洞。 NPR-18963

## 表单 {#forms-12}

AEM Forms 修补程序通过随发行版一起提供的 Forms 附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

AEM Forms 的主要功能亮点包括：

* 修复了通信管理文本模块、信件预览和编程启动以创建通信管理UI的问题。
* 修复了 PDF/A-1b 验证、将大型图像文件转换为 PDF，以及 PDF Generator 中的日语 PDF 文档的问题。
* 修复了通信管理、文档安全和Forms Workflow的可用性问题。
* 添加了对捕获潦草签名字段的审核事件的支持。

### Forms 附加组件包 {#forms-add-on-package-12}

**通信管理**

* 编辑通信管理片段时，文本编辑器显示内嵌条件以及处理的文本。 CQ-4211930
* 创建通信管理信件时，信件的描述未保存。 NPR-18089
* 项目符号列表上下方的额外边距在文本编辑器中可见，但在HTML和PDF呈现中不可见。 NPR-18126
* HTML 提交所使用的 POST 方法后，无法启动创建通信 UI 的操作。NPR-18202
* 当文本模块已保存且文本模块中的表达式不包含开放或闭合的表达式标记时，未显示错误消息。文本模块显示错误消息，并且无法在信件中呈现。NPR-18535
* 添加新内容或者按下 `Enter` 键后，div 标记会被添加到文本模块。NPR-18240

**汇编程序**

* 验证 PDF 文档是否符合 PDF/A-1b 标准时，AEM Forms 返回一则验证错误：PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED。使用 Adobe Preflight 和第三方软件进行验证时，PDF 文档未返回错误。NPR-18011
* 验证 PDF 文档是否符合 PDF/A-1b 标准时，AEM Forms 返回一则验证错误：表单字段具有多种外观。PDF 文档符合 PDF/A-1b 标准。NPR-18013

**监视文件夹**

* 如果在创建监视文件夹时，选择使用工作流来处理文件，则工作流模型选项下拉菜单会被截断。NPR-17566

**HTML5 表单**

* AEM Forms 不会捕获潦草签名字段的审核事件。NPR-15286

**Forms 管理器**

* AEM Forms UI 按照时间以升序（最早的排在最前面）列出所有资源。用户无法按照时间以降序（最新的排在最前面）重新排列资源。NPR-18450

**Java™ API 引用**

为 com.adobe.livecycle.content 类添加了 JavaDocs。NPR-18468

### Forms JEE 安装程序 {#forms-jee-installer-11}

**PDF Generator**

* PDF Generator服务无法将大于100 MB的图像转换为PDF文档。 CQ-4208628
* 在将PDF Generator服务与日语OCR一起使用时，生成反向PDF。 NPR-17602

**进程管理**

* 没有为 AEM Forms 进程填充 TaskContext 变量。NPR-18199

**文档安全**

* Microsoft® Excel 和 Microsoft® PowerPoint 需要花费更长的时间，才能打开受适用于 Microsoft® Office 的 AEM 文档安全扩展保护的文档。CQ-4212358
* 创建新策略且策略使用与现有名称相同的名称时，会发生内部服务器错误。NPR-18247

## 包含的功能包 {#feature-packs-included-2}

* AEM 中用户权限更改的可审核性要求。NPR-17061

AEM 累积修订包 6.3.0.1 是一个重要更新，它包括自 2017 年 4 月 AEM 6.3 正式发布以来的若干内部修补程序和客户修补程序。AEM 累积修订包的主要功能亮点包括：

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
>Adobe 提供的可选功能包依赖于发行版本和累积修订包。如果您已安装功能包，请联系 [AEM 客户关怀团队](https://experienceleague.adobe.com/?support-solution=General#support)，验证与 AEM 6.3 累积修订包的兼容性。

>[!NOTE]
>
>Adobe建议您在尝试安装每个新的安装包之前先运行验证。 预验证会分析并报告安装之前发现的任何错误，并主动向用户发出有关此类错误的警告。
>
>您可以在[https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)上访问有关验证选项的文档

* AEM 6.3.3.0 是安装 CFP 的先决条件。有关将AEM安装升级到AEM 6.3的详细说明，请参阅[升级文档](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)。
* 对于使用 RDBMK 或 MongoDB 的群集部署，可以在使用包管理器的任何创作实例上安装 CFP 包。
* 在安装累积修订包之前，请确保拍摄快照或备份AEM实例。
* 不支持卸载 CFP。

### 添加新日志记录器 {#adding-new-loggers}

要配置调试级别日志记录并在 SP/CFP 安装期间检索活动日志，您可以按照以下步骤操作：

* 您可以在默认位置 [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) 添加日志记录器，该日志记录器具有以下属性：

   * 日志级别：调试
   * 累加：false
   * 日志文件：logs/activity.log
   * 日志记录器：org.apache.jackrabbit.vault.packaging.impl.ActivityLog

activity.log在crx-quickstart /logs文件夹中创建。

### 通过 Software Distribution 安装累积修订包 {#install-the-cumulative-fix-pack-via-package-share}

1. 单击 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) 链接以下载包。

1. 打开[包管理器](http://localhost:4502/crx/packmgr/index.jsp)，并单击&#x200B;**[!UICONTROL 上传包]**&#x200B;以上传包。

1. 选择包名称，然后单击&#x200B;**[!UICONTROL 安装]**。

### 自动安装 {#automatic-installation}

可以通过以下方式将 CFP 自动安装到正在运行的实例中：

* 在服务器运行时，将包放入 `../crx-quickstart/install` 中。包会自动进行安装。
* 使用[包管理器中的 HTTP API](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) – 确保使用 `cmd=install&recursive=true` – 这会安装嵌套包。

### 验证安装 {#validate-installation}

1. “产品信息”页面 (`/system/console/ productinfo`) 此时应在“已安装的产品”下显示更新的版本字符串“Adobe Experience Manager，版本 6.3.3.8”。
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
>如果您不使用 AEM Forms，请跳过此部分。

#### 安装 AEM Forms 附加组件 {#install-forms}

1. 确保您已安装 AEM 6.3.3.x CFP 包。
1. 下载适用于您的操作系统的 [AEM Forms 发行版](aem-forms-releases.md)中列出的相应 Forms 附加组件包。
1. 按照[安装 AEM Forms 附加组件包](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)中的所述安装 Forms 附加组件包。

#### 安装 AEM Forms JEE 包 {#install-aem-forms-jee-bundles-package}

AEM Forms JEE 中的修复通过单独的安装程序来交付。有关在 AEM Forms JEE 上安装 CFP 的信息，请参阅[在 AEM Forms JEE 上安装 CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer 安装程序 {#designer-installer}

1. 要安装更新，请运行 Designer 6.2.0_&lt;语言>_Cumulative_QF.msp 文件。
1. 在“欢迎”屏幕上，单击&#x200B;**更新**。安装随即开始。
1. 安装完成后，单击&#x200B;**完成**。

## 配置 AEM Forms JEE 的设置 (JBoss® EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>如果要安装6.3.3.0或更高版本，请执行以下过程来配置JBoss®应用程序服务器的设置。 如果是在 Oracle WebLogic 或 IBM® WebSpehere 应用程序服务器上运行的 AEM Forms 服务器上安装 6.3.3.0，则无需其他配置。有关更多详细信息，请参阅 [AEM 6.3.3.0 发行说明](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)。

## Search&amp;Promote 集成的配置更新 {#configuration-updates-for-search-promote-integration}

如果安装的是 AEM 累积修订包 6.3.0.2 及更高版本，则用于 Search&amp;Promote 集成的 OSGi 配置是 **Apache HTTP 组件代理配置**。不再使用 Day Commons HTTP Client 3.1 中的代理配置。

## 已知问题 {#known-issues}

* 在 AEM CFP 6.3.3.x 的安装过程中可能会出现以下错误和警告，这些错误和警告可以安全忽略：

   * &#42;警告&#42; [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependencies.jar 引发运行时异常。
   * &#42;错误&#42; [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] 等待注册更改完成取消注册时超时。CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver服务缺失，无法发送服务请求，发送状态503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource：无法检查资源 [/bin/receive]，页面管理器不可用
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver：调用错误处理程序导致出现错误
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver 原始错误 null
   * org.apache.sling.engine.impl.DefaultErrorHandler 处理程序 failed:java.io.IOException 出错
   * &#42;错误&#42; [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent 错误（org.osgi.framework.ServiceException：服务工厂返回 null。（组件：com.day.cq.dam.handler.standard.ps.PostScriptHandler）)

**Brand Portal**

* 从6.3.1.2开始，删除了智能收藏集的“Publish到Brand Portal”按钮。

**用户界面**

>[!NOTE]
>
>如果您受到这两个问题的影响，请联系 [AEM 客户关怀团队](https://experienceleague.adobe.com/?support-solution=General#support)。

* 由于管理员搜索功能中有许多请求，观察到CPU利用率很高。 NPR-24229
* 重新打开组件后，未在 pathBrowser 中选择 PathField。NPR-24177

## NPR-27692 所需的配置设置 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>此配置设置适用于 CFP 6.3.3.2 及更高版本。它将指导您更新 `sling` .properties 文件中的启动委托属性。

要手动更新 adobe- LiveCycle® cq -author.ear/ cq .war 中的更改，请按以下所述步骤操作：

* 停止 AEM 服务器。
* 转到 adobe-livecycle-cq-author.ear/cq.war
* 打开 adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml 进行编辑：

   * 将 **sling.bootdelegation.ibm** 参数名称值更新为：

   * `com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat`

   * 完成上述更改后，init-param 应该如下所示：

     &lt;init-param>
&lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>
&lt;/init-param>

* 从 WebSphere® 应用程序服务器中卸载之前的企业存档 (EAR) 文件，并按照 [https://helpx.adobe.com/cn/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/cn/pdf/aem-forms/6-3/install-single-server-websphere.pdf) 第 10.2 节中的步骤来安装更新后的 EAR 文件
* 保存文件并重新启动服务器。[https://helpx.adobe.com/cn/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/cn/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## NPR-23208 所需的配置设置 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>此配置设置适用于 6.3.2.2 及更高版本。它会指导您通过CRX-DE手动更新访问控制列表(ACL)策略，因为由于“merge_preserve”acHandling，ACL不会通过CFP安装进行更新。

**有关手动添加 ACL 策略的文档**

要更新 ACL 策略，请通过 CRX-DE 添加以下访问控制：

`1)` At &quot;/content&quot; path
`a)`主体： reference-adjustment-service
类型：允许
权限：jcr：read、jcr：modifyProperties
限制：rep：glob=&quot;/&#42;/jcr：content&quot;
`b)`主体： reference-adjustment-service
类型：允许
权限：jcr：read、jcr：modifyProperties
限制：rep：glob=&quot;/&#42;/jcr：content/&#42;&quot;

`2)` 在“/content/usergenerated”路径
`a)` 主体：reference-adjustment-service
类型：允许
权限： `jcr:write`

`3)` At &quot;/etc&quot; path
`a)`主体： reference-adjustment-service
类型：允许
权限：jcr：read、jcr：modifyProperties
限制：rep：glob=&quot;/&#42;/jcr：content&quot;
`b)`主体： reference-adjustment-service
类型：允许
权限：jcr：read、jcr：modifyProperties
限制：rep：glob=&quot;/&#42;/jcr：content/&#42;&quot;

## NPR-19450 所需的配置设置 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>此配置设置适用于 CFP 6.3.1.1 及更高版本。

**配置属性 CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL。**

该属性可控制页面 ` /jcr:content` 节点下节点子树的最大深度，在达到该深度之前，存储库中存在的节点将用于获取页面属性。此属性中指定的深度以下存在的任何节点都将被忽略。

默认值为 1。通过覆盖文件constants.js (`/libs/cq/ui/widgets/source/constants.js`)取消注释`CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL`属性来覆盖值。 然后，为其分配所需的值（存储页面属性数据的页面`/jcr:content`下的最大深度）。

**如果用户必须创建多个页面变量，以使页面的 `/jcr:content` 节点下的节点数大于 1000，请按照以下步骤进行配置更改：**

* 配置Apache Sling的JSON Max结果属性。
* 使用`/system/console/ configMgr`获取Servlet。
* 将其值设置为大于 1000（这是当前的默认值）的数字，以使该数字大于在达到上面配置的深度之前 `/jcr:content` 子树中存在的节点总数。

此过程使SlingGETServlet能够返回所有必需的节点。

## Uber Jar {#uber-jar}

适用于6.3.3.8的Uber Jar可在Adobe公共Maven存储库中获取

要在Maven项目中使用Uber Jar，请参阅[如何使用Uber Jar](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)，并在项目POM中包含以下依赖项：

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
| Assets 和 Adobe Creative Cloud 集成 | AEM 6.2 中引入了 [AEM 到 Creative Cloud 的文件夹共享](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)功能，以便创意用户可以从 AEM 访问资源。Creative Cloud应用程序中发布的一项新功能AdobeAsset Link提供了更好的用户体验。 它还提供了更强大的功能，可直接从Photoshop、InDesign和Illustrator内部访问AEM中的资源。</br></br>Adobe 不会再进一步增强文件夹共享功能。虽然该功能包含在 AEM 中，但建议客户使用替换解决方案。 | Adobe 资源链接或桌面应用程序。有关详细信息，请参阅[AEMCreative Cloud集成](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)一文。 | AEM 6.3.3.x |

## 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-1}

以下文本文档列出了 CFP 中包含的 OSGi 包和内容包。

* [AEM 6.3.3.8 中包含的 OSGi 包列表](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [AEM 6.3.3.8 中包含的内容包列表](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [AEM 发行版和更新](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [AEM 6.3 修补程序页面](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [AEM 6.3 发行说明](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [AEM 产品页面](https://business.adobe.com/products/experience-manager/adobe-experience-manager.html)
>* [AEM 6.3 文档](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* 订阅[Adobe优先产品更新](https://www.adobe.com/cn/subscription/priority-product-update.html)
