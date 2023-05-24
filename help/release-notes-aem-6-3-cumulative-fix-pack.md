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

Adobe 引入了统一交付模式，用于发布修补程序。现在，Adobe 每月会发布一个累积修订包 (CFP)（需通过质量检查），而不是针对个别问题发布修补程序。CFP是用于多个修复的聚合内容包。 CFP主要包括错误修复，但可能还包括功能包。 与各个修补程序版本相比，它们具有以下优势：

* 具有累积性质（例如，CFP包含通过以前的CFP交付的修复）
* 提高质量保证
* 简化安装（用户将CFP作为单个包进行安装，该包除最新版Service Pack之外，没有任何依赖关系）

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
>从AEM版本6.3.3.1开始，支持MongoDB Enterprise 3.6。

## 问题列表 {#changes}

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

* 主控页面的页面属性加载失败，并返回NullPointerException。 添加cq：blueprint属性解决了此问题(NPR-30901)。
* 未从根节点上的blueprintConfig正确检索转出配置。 对Blueprint和活动副本都会触发停用。 只应为Blueprint触发停用(NPR-30866)。
* 当用户转出页面时，转出配置对话框显示重复的Live Copy路径(NPR-30438)。
* 现成的基架富文本编辑器(RTE)。 意外地将内嵌字体大小应用到元素（NPR-31283、NPR-30922）。
* 无法同步包含现成设计导入程序组件的Adobe活动中的活动(NPR-30890)。
* 富文本编辑器 (RTE). 不允许将嵌入的表作为列表项插入(NPR-30878)。
* 如果用户的焦点位于左侧边栏字段并使用键盘快捷方式粘贴内容，则会粘贴页面编辑器剪贴板的内容，而不是从左侧边栏字段复制的内容 (NPR-31173)。
* 用户编辑内容片段时，会恢复内容片段的已删除变量 (NPR-31272)。
* AEM Site 没有创建语言副本的选项 (NPR-30690)。
* 页面编辑器的操作没有控件来转出 Live Copy (NPR-30613)。

### 社区 {#communities}

* 活动和通知标题不一致 (NPR-30940)。
* AEM创作环境中未填充Analytics报表，出现空白页(NPR-30905)。
* Communities博客中的分页功能无法正常工作(NPR-30827)。

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

* Dynamic Video的视频聚合仅返回结果集中的前100项。 NPR-30441：适用于CQ-4213561的修补程序
* 通过DatapowerAdobe智能标记连接问题。 NPR-30026：适用于 CQ-4269457 的修补程序
* 无法使用Assets界面打开其名称具有百分比符号(%)的文件夹的解压缩存档。 NPR-29989：适用于 CQ-4270467 的修补程序
* 处理大型PDF文件的子资源会导致OutOfMemoryError (OOME)异常。 NPR-29851：适用于 CQ-4269574 的修补程序

### 站点 {#sites-2}

* AEM与Campaign集成期间出现ContextHub错误。 NPR-30624：适用于 CQ-4250790 的修补程序
* 如果AEM服务器重新启动，则不会重新调用资源上保存的“onTime”或“offTime”元数据属性。 NPR-30412：适用于 CQ-4272784 的修补程序
* 在生成CSV导出时，为列表视图添加自定义列会破坏报表。 NPR-30208：适用于 CQ-4273344 的修补程序
* /etc/reports/中的OOTB报告无法正常工作，并且不会显示历史数据图表。 NPR-30016：适用于 CQ-4220180 的修补程序
* resourceType请求参数的值将被复制到HTML标签属性的值中，该属性用双引号封装。 NPR-29832：适用于 CQ-4255365 的修补程序

### 社区 {#communities-1}

* AEM Communities审核控制台存在重复内容问题。 NPR-30667：适用于 CQ-4276829 的修补程序

### 翻译 {#translation}

* 翻译问题 - 只有少数组件使用机器翻译进行了翻译。NPR-30079：适用于 CQ-4273764 的修补程序
* 使用翻译框架时，向多个翻译作业添加页面会触发错误。 NPR-29746：适用于 CQ-4270953 的修补程序

### 表单 {#forms-2}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-2}

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM Service Pack 和累积修补程序包保持一致。因此，请务必在安装任意 AEM Service Pack、累积修补程序包或功能包之后安装 AEM Forms 附加组件包。

#### HTML5 表单 {#html-forms-1}

* 在浏览模式下使用 NonVisual Desktop Access 读取 HTML5 表单时，Chrome 浏览器会读取表单设计中每个可缩放矢量图形 (SVG) 前的“图形”。NPR-30451：适用于 CQ-4274732 的修补程序

#### 表单 - 后端集成 {#forms-backend-integration}

* 创建表单数据模型(FDM)时无法查看数据库连接的服务/数据源。 NPR-30108：适用于 CQ-4273359 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-1}

#### 表单 - 文档服务 {#forms-document-services}

* 对HTML到PDF服务执行负载测试时，该测试失败并出现错误，并且文件类型设置已从AEM表单服务器中删除。 NPR-30111、NPR-30086：适用于 CQ-4271495 的修补程序

### 累积修补程序包 6.3.3.5 {#cumulative-fix-pack-3}

AEM 累积修补程序包 6.3.3.5 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.5 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.17。

### 资产 {#assets-3}

* 针对 S3 多部分支持更新了 DAM DMGateway 接口。NPR-29740：适用于Q-4226303的修补程序
* 无法从资源详细信息页面中删除视频资源上的图像演绎版。 NPR-29417：适用于 CQ-4268675 的修补程序
* 所有者无法在专用文件夹中创建专用文件夹。 NPR-29397：适用于 CQ-4229830 的修补程序
* 上传大于2 GB的Adobe Illustrator图稿文件会生成Java栈空间错误。 NPR-29265：适用于 CQ-4226217 的修补程序
* 在DAM CQ Mime类型服务为m3u8应用文本后，资产变得不可用。 NPR-29259：适用于 CQ-4264052 的修补程序
* 尝试在Edge中创建收藏集时，“创建”选项不起作用。 NPR-29248：适用于 CQ-4265699 和 CQ-4265438 的修补程序
* 资产链接共享在文件夹中为某些资产显示空白灰色卡片。 NPR-29831：适用于 CQ-4270187 的修补程序
* 添加到资产的新标记无法保存，且从属性中消失。适用于 CQ-4271931、CQ-4270476 的修补程序

### 站点 {#sites-3}

* 与Multifield一起使用时，CoralUI在组件级别存储fileReferenceParameter而不是多字段级别。 NPR-29535：适用于 CQ-4266129 的修补程序
* 在AEM 6.3.3.3上尝试比较最新页面版本和当前页面版本时出现问题。NPR-29532：适用于CQ-4269639的修补程序
* 路径字段将在根路径中打开，与指定的搜索路径无关。 NPR-29398：适用于 CQ-4268897 的修补程序
* （体验片段）FacebookApplication#setUpApp 使用已弃用的 API，该 API 不再可用。NPR-29213：适用于 CQ-4266630 的修补程序
* 在实例上启用缩小功能后，将组件添加到WCM页面时生成错误警报。 NPR-29476：适用于 CQ-4266197 的修补程序
* 转出期间不会从Blueprint传播空属性和多个属性。 使用Blueprint重置Live Copy对组件无效。NPR-29252：适用于CQ-4264928、CQ-4264926、CQ-4267722的修补程序
* 在源编辑模式下从全屏最小化富文本编辑器会导致内容丢失。 NPR-28838：适用于 CQ-4260584 的修补程序

### 社区 {#communities-2}

* 没有版主权限的访客和成员可以通过粘贴URL查看未批准和待处理的帖子。 NPR-29726：适用于 CQ-4271124 的修补程序
* 观察到用户登录Community时响应时间长达40-50秒。 NPR-29679：适用于 CQ-4269444 的修补程序
* 以不同的用户名登录时无法重置密码，并且密钥为的电子邮件似乎是以交换的用户名和电子邮件生成的。 NPR-29281：适用于 CQ-4268694 的修补程序

### 体验片段 {#experience-fragments}

* 使用智能图像时无法将体验片段导出到目标。 适用于 CQ-4269606 的修补程序

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
* 在Brand Portal复制代理中添加了套接字超时和连接超时。

### 资产 {#assets-4}

* 如果重新上传具有相同名称的存档文件，则不会为新处理的资产生成呈现版本。NPR-28643：适用于 CQ-4262286 的修补程序
* 工作流 CommandLineProcess 因文件名中含有单引号而失败。NPR-28805：适用于 CQ-4262287 的修补程序
* 集合页面和使用过滤器的集合页面之间的值不同。 NPR-28642：适用于 CQ-4261405 的修补程序
* 上传大型zip存档资产时触发CommitFailedException。 NPR-28528：适用于 CQ-4260903 的修补程序
* 编辑包含特殊字符的文件夹时，无法保存文件夹元数据。 NPR-28211：适用于 CQ-4260401 的修补程序
* 无法从资源详细信息页面中删除视频资源的图像演绎版。 NPR-29149：适用于 CQ-4266073 的修补程序
* 使用DMComponent的DMS7桌面视频交付使用渐进式下载在发布模式下播放视频，而不会进行流式传输。 NPR-28754：适用于 CQ-4263732 的修补程序
* 无法创建/编辑图像预设，因为限制对/etc/dam/video/dynamicmedia的访问会禁用图像管理器的功能。 NPR-28662：适用于 CQ-4263022 的修补程序
* 与DMS7编码视频文件的链接共享导致空文件夹。 NPR-28851：适用于 CQ-4206743 的修补程序
* 从AEM到Brand Portal的复制长时间卡住。 NPR-28913：适用于 CQ-4254932 的修补程序

### 社区 {#communities-3}

* 无法打开Outlook发送和收件箱文件夹中包含附件的邮件。 NPR-28559：适用于 CQ-4217072 的修补程序

### 站点 {#sites-4}

* 适用于6.3的SuggestionHandler中存在跨站点脚本(XSS)。NPR-28692：适用于CQ-4253821的修补程序
* 深度转出结束时将不包含相应LiveCopy中的所有分支。 NPR-29175：适用于 CQ-4239472 的修补程序
* (MSM) 使用 oak-index 实施 LiveCopyIndex。NPR-29198：适用于 CQ-4222472 的修补程序
* 文件“coral.js”包含易受攻击版本的“handlebars.js”库。 NPR-26973：适用于 CQ-4255377 的修补程序
* 如果将 Target 组件与嵌套式布局容器和文本组件一起使用，则在编辑文本或单击容器时，会引发以下 JavaScript 错误：“无法读取值为 null 的属性 currentPos”。NPR-29077：适用于 CQ-4246594 的修补程序
* （触屏 UI）无法将标记批量更新到已使用其他标记进行标记的页面。NPR-28729：适用于 CQ-4262922 的修补程序
* 在卡片视图中打开该变量会导致500错误。 NPR-28611：适用于 CQ-4263571 的修补程序
* 转出已在母版中移动的结构会导致错误的 cq:moveTarget。NPR-28968：适用于 CQ-4265280 的修补程序

### 集成 {#integration}

* （云服务配置）在根级别出现的“继承自”复选框应被删除。NPR-28771：适用于 CQ-4259676 的修补程序
* com.day.cq.personalization.impl.TeaserResourceEventHandler进入无限循环，导致更新发布实例上的节点。 NPR-28561：适用于 CQ-4263096 的修补程序
* 使用Brightedge凭据失败，出现连接错误。 NPR-29167：适用于 CQ-4265872 的修补程序
* OfferproxyTandtProvider.java中存在编译问题，因为缺少“Resource”类的import语句： missing import语句： import org.apache.sling.api.resource.Resource。 NPR-28772

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

AEM Forms的主要功能亮点包括：

* 启用了用于在“策略集视图”页面上每页选择项目的选项。
* 为所有浏览器添加了共享队列功能。

### Forms 附加组件包 {#forms-add-on-package-4}

#### 表单 - 工作流 {#forms-workflow}

* 共享队列响应任务会在HTML5工作区中打开一个Flash元素。 NPR-29161：适用于 CQ-4266498 的修补程序
* 如果按钮包含Umlaut字符，则无法从工作区提交。 NPR-29014：适用于 CQ-4263172 的修补程序

#### 表单 - 文档安全 {#forms-document-security}

* 启用选项，以便在策略集视图页面上选择每页的项目。 NPR-29243：适用于CQ-4268567和CQ-4265132的修补程序

#### 表单 - 文档服务 {#forms-document-services-1}

* OSGi 表单汇编程序无法处理 Acrobat 文件。NPR-29049：适用于 CQ-4254426 的修补程序

#### HTML5 表单 {#html-forms-2}

* 在Designer中将XDP作为PDF预览，与将XDP作为HTML预览时，会遇到不同的行为。 NPR-28602：适用于 CQ-4260239 的修补程序

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
* 策略设置列表分页更改为每页限制50条记录。
* 已将 rep: cache 添加到发布实例上 AEM Communities 用户同步侦听器中的可忽略节点。
* 为列表和卡片视图按钮添加了 aria 标签。
* 执行任何搜索时为逗号包含一个转义字符。
* 为内容策略启用了综合资源支持。

#### 资产 {#assets-5}

* 无法下载多个.jp2、.max、.oft、.msg类型的文件。 NPR-28002：适用于 CQ-4210856 的修补程序
* ImageServer 发布设置不会复制到混合交付中。NPR-28329：适用于 CQ-4253030 的修补程序

#### 社区 {#communities-4}

* 在Publish上为AEM Communities Enablement组件启用了键盘导航。 NPR-27739：适用于 CQ-4253856 的修补程序
* 启用键盘导航以触发内容播放。 NPR-27738：适用于 CQ-4254026 的修补程序
* 为列表和卡片视图按钮添加了 aria 标签。NPR-27736：适用于 CQ-4254027 的修补程序
* （补丁包）已将 rep: cache 添加到发布实例上 AEM Communities 用户同步侦听器中的可忽略节点。NPR-27841：适用于 CQ-4247234 的修补程序
* 在 UI 级别的搜索框中，特殊字符带有转义字符 (\) 前缀。NPR-27839：适用于 CQ-4259757 的修补程序
* 在快速搜索中搜索诸如 (、+、? 之类的字符时出现错误。NPR-28212：适用于 CQ-4260969 的修补程序
* 无法使用API删除用户生成的内容中的注释。 NPR-28075：适用于 CQ-4260534 的修补程序
* 在发布新评论时，发布到下一页的评论以黄色突出显示。 NPR-28148：适用于 CQ-4259681 的修补程序
* 无法打开Outlook发送和收件箱文件夹中包含附件的邮件。 NPR-28559：适用于 CQ-4217072 的修补程序

#### 站点 {#sites-5}

* 在 AEM 6.3 中运行版本清除，会导致日志中持续不断地反复出现警告。NPR-27750：适用于CQ-4206870的修补程序
* 富文本编辑器全屏模式不支持样式插件。 NPR-27622：适用于 CQ-4258674 的修补程序
* 将内容框架加载到 editor.js 中后，未清除“loaderPromises”列表。NPR-27768：适用于 CQ-4205337 的修补程序
* 若未设置父组件，则无法在嵌套的 Parsys 上设置模板策略。NPR-27987：适用于 CQ-4246095 的修补程序
* 组件浏览器未对用户输入进行清理，因此可能会引发javascript错误。 NPR-27986：适用于 CQ-4247590 的修补程序
* 用户尝试编辑内容片段时，页面显示为空白。NPR-27669
* 用户单击注释后，注释高亮会立即消失。 BPR-27196：适用于CQ-4254423的修补程序

#### 集成 {#integration-1}

* ResourceResolver未解析目标组件的多个域。 NPR-28265：适用于 CQ-107847 的修补程序
* 由于未显示任何操作，LiveCopy继承取消无法在目标容器上正确执行。 NPR-28129：适用于 CQ-4259813 的修补程序

#### 复制 {#replication-1}

* DispatcherFlushRules中断6.3.3.1中的复制NPR-28150：适用于CQ-4261401的修补程序

#### Campaign — 定位 {#campaign-targeting-1}

* TargetedContentManager中的NullPointerException。 适用于 CQ-4263485 的修补程序

#### 社交 — SCORM {#social-scorm}

* 在播放器中删除对可共享内容对象引用模型 (SCORM) 云的引用。适用于 CQ-4260779 的修补程序

#### DAM - 常规 {#dam-general}

* 通过链接共享电子邮件下载返回空/损坏的zip。 适用于 CQ-4259686 的修补程序

#### Mac - Test&amp;Target集成 {#mac-test-target-integration}

* 无法对默认受众之外的受众配置“目标组件”选项。适用于 CQ-4261370 的修补程序

#### 翻译 {#translation-1}

* 将 MS Translator 升级到 API v3.0 后，在 AEM 6.3 中启用对 MS Translator 服务的支持。NPR-28365：适用于 CQ-4259096 的修补程序

### 表单 {#forms-5}

### Forms 附加组件包 {#forms-add-on-package-5}

#### 表单 - 工作流 {#forms-workflow-1}

* 无法在HTML5工作区上呈现PDF forms。 NPR-28059：适用于 CQ-4260373 的修补程序

#### 表单 - 文档服务 {#forms-document-services-2}

* 在管理控制台的“策略集”视图中，无法看到除列出的前 1000 项之外的任何其他策略集。NPR-28060、NPR-26047：适用于 CQ-4249865 的修补程序
* 引发名称为 java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE 的异常，导致短暂的进程无法完成。NPR-28652

#### Forms — 自适应Forms {#forms-adaptive-forms}

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
* 在文件夹元数据架构中添加了对“规则”选项卡的支持，以及在资产文件夹中实施该选项卡的功能。
* 为发布时的组列表页面启用了分页支持。
* 启用使用任意数字配置的unreadCount通知。 默认值设置为20。
* 修复了外部链接检查器中的问题。

#### 资产 {#assets-6}

* 动态下拉列表不支持级联下拉列表。 NPR-27044：适用于CQ-4252564的修补程序
* 改进查询以使用ExpiryNotification功能。 NPR-26999：适用于 CQ-4251188 的修补程序
* 规则从元数据架构迁移到文件夹元数据架构。 NPR-27771：适用于CQ-4257737、CQ-4257735、CQ-4259822的补丁包
* 资产引用调整无法更新属于Sling ResourceCollections一部分的资产的引用。 NPR-26759：适用于 CQ-4252605 的修补程序
* 通过链接共享电子邮件下载会返回空/损坏的zip文件。 NPR-27997：适用于 CQ-4259686 的修补程序
* 混合视频编码不完整且未创建缩略图。 NPR-27122：适用于 CQ-4255080 的修补程序

#### 站点 {#sites-6}

* 暂停父页面会导致从缺失页面中删除 cq : LiveRelationship mixin 类型NPR-26996：适用于 CQ-4254113 的修补程序
* （外部链接检查器）内部链接在各个页面上显示为已损坏，但外部链接并非如此。NPR-27481：适用于 CQ-4257780 的修补程序
* 编辑其他Cloud Service属性时，页面配置继承中断。 NPR-27311：适用于 CQ-4256785 的修补程序
* 将核心组件表单与Foundation表单一起使用时出现空指针异常。 NPR-27333：适用于 CQ-4249176 的修补程序
* 富文本编辑器删除空的alt标记。 NPR-26938：适用于 CQ-4253267 的修补程序
* （经典 UI）存在多个下拉列表时，selectionchanged 侦听器出现性能问题。NPR-27115：适用于 CQ-4237215 的修补程序
* 当富文本编辑器与多个字段组合时，出现“Uncaught TypeError： fieldAPI.getName is not a function at foundation.js”错误。 NPR-27146：适用于CQ-4253155、CQ-4259967的修补程序
* 即使单击Safari浏览器中的单选按钮，焦点/光标仍保留在富文本编辑器上。 NPR-27144：适用于 CQ-4249635 的修补程序
* 用户尝试编辑内容片段时，页面显示为空白。 NPR-27669
* 无法为体验片段创建版本。 NPR-27689：适用于 CQ-4259009 的修补程序

#### 集成 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever遍历整个树以收集可用的品牌。 NPR-27060：适用于 CQ-4255790 的修补程序
* 目标组件不考虑 cq: 操作。NPR-27616：适用于 CQ-4257497 的修补程序

#### Sling {#sling}

* 如果将data-sly-use与具有相同名称的类一起使用，则会生成不相容的代码。 NPR-27282：适用于Sling-7581的修补程序

#### 商务 {#commerce-1}

* 已更新到 Apache Felix Http Jetty 4.0.6。NPR-26472：适用于 Granite-22916 的修补程序

#### DAM - DM 客户端 {#dam-dm-client}

* 在Dynamic Media组件中指定断点后，图像未显示。 适用于 CQ-4256168 的修补程序

#### dam - DMServices {#dam-dmservices}

* 包含相关视频的 MixedMediaSet 无法正确同步。适用于 CQ-4251650 的修补程序
* 对于混合媒体集，无法在查看器预设编辑器中播放视频。适用于 CQ-4251442 的修补程序

#### DAM - 常规 {#dam-general-1}

* 应用SP3补丁后缺少指向内容片段模型的链接。 适用于 CQ-4259029 的修补程序

#### DAM - UI {#dam-ui}

* 安装SP3后，文件夹元数据架构UI损坏。 适用于 CQ-4257737 的修补程序

#### 社区 {#communities-5}

* 为发布时列出的组添加分页支持。 NPR-26953：适用于 CQ-4246525 的修补程序
* 未读计数通知的设置不能超过21。 NPR-27496：适用于 CQ-4252829 的修补程序
* 用户订阅限制限制为1000。 NPR-27615：适用于 CQ-4254689 的修补程序
* 在论坛中上传图像以外的附件（例如.pdf）时发现错误。 NPR-27375：适用于 CQ-4257753 的修补程序
* 行点击时回复链接不起作用。 NPR-24556：适用于 CQ-4256138 的修补程序
* 删除UGC时未删除与UGC的关系。 NPR-27631：适用于 CQ-4258706 的修补程序
* 如果使用数据库存储资源提供程序(DSRP)设置社区，则无法按关键字搜索中的地址值搜索。 NPR-27652：适用于 CQ-4253261 的修补程序
* 确认删除后单击图像上的垃圾桶图标会永久删除附件。 NPR-27340：适用于 CQ-4255150 的修补程序
* 论坛帖子及回复会添加到第二个页面的顶部，刷新后，帖子会移动到第一个页面顶部的正确位置。 NPR-27341：适用于 CQ-4247338 的修补程序
* “启用Scorm资源”完成状态标签在UI中显示为空。 NPR-27152：适用于 CQ-4249994 的修补程序
* 启用“允许拥有特权”后，拥有特权的成员应只能为社区成员用户撰写。 NPR-27901：适用于 CQ-4251235 的修补程序

#### 留存 {#sustenance}

* 应在一个单独的日志文件中提取包管理器活动日志。 NPR-27323：适用于 Granite-14866 的修补程序

#### 翻译 {#translation-2}

* 翻译预览不适用于 we.retail 示例内容。NPR-27170：适用于 CQ-4241179 的修补程序

* 主动式platform.login修复。 NPR-26961
* 使用Tomcat的AEM WAR中，“保存并关闭”页面属性未返回到正确的页面。 NPR-27567：适用于 Granite-23671 的修补程序

* 保存后，通过 sourceEdit 功能输入的文本将丢失。适用于 CQ-4259273 的修补程序

### 表单 {#forms-6}

### Forms 附加组件包 {#forms-add-on-package-6}

#### 表单 - 文档安全 {#forms-document-security-1}

* JEE客户端SDK出现并发问题。 NPR-27572：适用于 CQ-4247156 的修补程序

#### 表单 - 文档服务 {#forms-document-services-3}

* 在WebSphere上创建基于SOAP的表单数据模型失败。 NPR-27692：适用于 CQ-4253702 的修补程序

#### Forms — 自适应表单 {#forms-adaptive-forms-1}

* AEM Forms 存在 XML 注入漏洞。NPR-27863：适用于 CQ-4257315 的修补程序
* 一旦在站点页面中配置了错误的表单并选中“表单覆盖整个页面宽度”复选框，AEM Forms容器组件将不可见。 NPR-25972：适用于CQ-4239287、CQ-4249133的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* 在WebSphere上创建基于SOAP的表单数据模型失败。 NPR-27692：适用于 CQ-4253702 的修补程序

#### 包含的OSGi包和内容包 {#osgi-bundles-and-content-packages-included}

AEM 6.3.3.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/63332bundle_list.txt)

AEM 6.3.3.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6332content_package.txt)

### 累积修补程序包 6.3.3.1 {#cumulative-fix-pack-7}

AEM 累积修补程序包 6.3.3.1 是一个重要更新，它包括自 2018 年 9 月 AEM 6.3 Service Pack 3 (6.3.3.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.3.1 依赖于 AEM 6.3 Service Pack 3。因此，您必须先安装 AEM 6.3 Service Pack 3，然后再安装 AEM 累积修补程序包 6.3.3.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 3 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.14。
* 谓词和搜索的性能改进。
* 修复了默认值在FormData处理时出现的问题。
* 已将FormBuilder升级到最新的Handlebars版本。
* 在对话框模式下为RTE的编辑配置添加了配置servlet。
* 添加了对复合字段的支持。
* 使用编辑对话框的内容策略启用/禁用富文本编辑器的工具栏项。

#### 资产 {#assets-7}

* 启用 IDS 分离后，DAM 更新资产工作流不再链接引用。NPR-26135：适用于 CQ-4250933 的修补程序
* 无法解压缩由取消存档器步骤创建的名称中包含%的文件夹。 NPR-26275：适用于 CQ-4251482 的修补程序
* 单引号字符会阻止元数据更新。 NPR-26808：适用于 CQ-4254305 的修补程序
* (Omnisearch) 在收藏集中搜索时，出现性能问题。NPR-26714：适用于 CQ-4253408 的修补程序
* 将GQLConverter与文本中包含“OR”字母的全文搜索结合使用时，处理方式不正确。 NPR-26564：适用于 CQ-4247362 的修补程序
* 来自多租户的共享资产链接会在租户ID之前附加以形成无效URL。 NPR-26482：适用于 CQ-4253540 的修补程序
* 在 Dynamic Media 云配置 UI 中，禁用“公司根文件夹路径”。NPR-26361：适用于 CQ-4249505 的修补程序
* .mos RAW文件的摄取时间延长。 NPR-26296：适用于 CQ-4250661 的修补程序
* 资产链接共享不允许使用数字用户 ID 添加多个内部用户。NPR-26206：适用于 CQ-4251466 的修补程序
* 使用 deflate64 算法压缩的 ZIP 文件损坏。NPR-26793：适用于 CQ-4253995 的修补程序
* 缩略图生成过程无法正确用于复杂的 PDF 文件，从而导致缩略图中缺少图像的部分内容。NPR-26057：适用于 CQ-4250944 的修补程序
* 生成缩略图时出现栈内存使用问题。 NPR-25545：适用于 CQ-4246960 的修补程序
* 在资产上创建大量关系会导致错误。 NPR-26309：适用于 CQ-4250708 的修补程序
* “删除演绎版”选项不起作用，并引发错误“没有可删除的内容”。 NPR-26007：适用于 CQ-4213414 的修补程序
* 无法删除多值字段的默认值。 NPR-25116：适用于 CQ-4247856 的修补程序
* （DM 混合模式）带有 Dynamic Media 的 AEM 6.3.2 的目录复制中断。NPR-26406：适用于 CQ-4251306 的修补程序

#### 站点 {#sites-7}

* Sites修复的主动式反向移植。 NPR-26963
* 如果“标题”和“名称”的大小写类型不同，则会创建两次标记。 NPR-26877：适用于 CQ-4254134 的修补程序
* “编辑”对话框中的富文本编辑器功能不受策略控制。 NPR-27059、NPR-26750：适用于 CQ-4241130 的修补程序
* Client Context segment.js缓存与非缓存问题。 NPR-26622：适用于 CQ-4253486 的修补程序
* 经典 UI 中子规则的区段规则 (/etc/segmentation) 激活导致发布下降。NPR-26601：适用于 CQ-4253588 的修补程序
* 添加“特殊字符”会将“富文本编辑器”对话框滚动到顶部。 NPR-26435：适用于 CQ-4249869 的修补程序
* （触屏 UI）从全屏切换到浮动对话框时，多个富文本编辑器的工具栏变得不可用。NPR-25652：适用于 CQ-4206008 的修补程序
* 提升多页面启动会为每个页面创建多个版本。 NPR-26810：适用于 CQ-4254663 的修补程序
* 标记移动操作未反映在结构化内容片段模型标记字段中。 NPR-26801：适用于 CQ-4251805 的修补程序
* （触屏 UI）重命名 Blueprint 中的页面后，无法从页面编辑器取消发布子页面。NPR-26774：适用于 CQ-4254175 的修补程序
* 未发布的页面无法使用引用。NPR-26749：适用于 CQ-4254372 的修补程序
* 将变量创建为 Live Copy 需要用户刷新页面才能得以反映。NPR-26663：适用于 CQ-4254328 的修补程序
* （经典 UI）返回页面属性后，缩略图图像不再使用继承并从站点管理和 Sidekick 中消失，导致图像显示为空白。NPR-26562：适用于 CQ-4252346 的修补程序
* 创建页面的版本并触发比较时，/content/版本历史记录中的节点将列在Blueprint的实时副本列表中。 NPR-26506：适用于 CQ-4243957 的修补程序
* 体验片段管理员编辑器中的URL不允许叠加图。 NPR-26318：适用于 CQ-4252156 的修补程序

#### 平台 {#platform}

* 包含测试事件的 ReplicationEventListener 中出现会话泄漏。NPR-25937：适用于 CQ-4251090 的修补程序
* 复制使用过期的OAuth令牌，从而导致多个错误。 NPR-25894：适用于 GRANITE-22388 的修补程序

#### 集成 {#integration-3}

* 升级到Handlebars 4后，由于使用不兼容的模板，嵌入了AEM的TSDK会中断。 NPR-26699：适用于 CQ-4248974 的修补程序
* 使用新资产发布页面时，会在不发出通知的情况下停用发布实例中的子页面。 NPR-24869：适用于 CQ-4247832 的修补程序
* 复制使用过期的oauth令牌。 NPR-25984：适用于 Granite-22388 的修补程序

#### 复制 {#replication-2}

* Http传输可能会泄漏打开的会话。 适用于Granite-17434的修补程序
* 多个复制代理同时访问访问令牌节点时，日志中出现异常。 NPR-26964：适用于GRANITE-23276、Granite-23155的修补程序

#### ContextHub {#contexthub}

* 文件“coral.js”包含易受攻击版本的“handlebars.js”库。 适用于 CQ-4255377 的修补程序

#### DAM - DM 客户端 {#dam-dm-client-1}

* 删除图像资源的副本会导致原始图像资源不可用。 适用于 CQ-4251648 的修补程序
* 从S7服务器冗余下载额外的图像内容。 适用于 CQ-4248770 的修补程序

#### Granite {#granite}

* AEM OAuth提供程序不执行不区分大小写的搜索。 NPR-26133：适用于 GRANITE-22650 的修补程序
* 包验证器不会验证CFP/SP中包含的包。 NPR-26775：适用于 Granite-22825 的修补程序

#### 社区 {#communities-6}

* 搜索结果存在分隔符问题。 NPR-27051：适用于 CQ-4248939 的修补程序
* 在 Adobe 存储资源提供程序中，将下拉列表值从“达拉斯”更改为“弗吉尼亚”。NPR-26936：适用于 CQ-4254434 的修补程序
* 在 SocialTagManager 中启用对本地化标题搜索的支持。NPR-26932：适用于 CQ-4250276 的修补程序
* 创建论坛帖子时，附件图像不显示缩略图。 NPR-26380：适用于 CQ-4253105 的修补程序
* 从Word插件粘贴时无法加载多个图像。 NPR-26728：适用于 CQ-4253638 的修补程序
* 无法筛选审核页面中的内容。 NPR-26697：适用于 CQ-4213766 的修补程序
* （安全漏洞）由于 JWT 配置错误，导致帐户接管。NPR-26440：适用于 CQ-4253314 的修补程序
* 从Adobe存储资源提供程序检索数据时速度较慢。 NPR-26237：适用于 NPR-24152 的修补程序
* 私人消息撰写页面的行为不稳定且缓慢。 NPR-26120：适用于 CQ-4250923 的修补程序
* “全部标记为已读”通知只将前10个标记为未读，而不刷新页面。 NPR-27036：适用于 CQ-4254058 的修补程序
* Communities评论部分分页点击和页面加载行为。 NPR-27030：适用于 CQ-4251228 的修补程序
* （论坛搜索）“返回”按钮跳过页面，并返回到 forum.html。NPR-26949：适用于 CQ-4254804 的修补程序
* 未读通知数增加不超过21。 NPR-26947：适用于 CQ-4251251 的修补程序
* （SearchScheduledPosts 作业）在 ConfigMgr 中添加启用/禁用切换开关。NPR-26924：适用于 CQ-4250463 的修补程序
* 在“指定任务”页面上滚动时，Tomcat Context(/aempublish)路径会断开。 NPR-26919：适用于 CQ-4254345 的修补程序
* 创建组和成员时出现NullPointerException。 NPR-26778：适用于 CQ-4248095 的修补程序
* 版主取消固定和取消精选内容不适用于MySQL单责任原则(SRP)。 NPR-26767：适用于 CQ-4251520 的修补程序
* 某些字符存在搜索功能问题。 NPR-26726：适用于 CQ-4247744 的修补程序
* 为审核UI和启用资源启用深层链接。 NPR-26705：适用于 CQ-4251381 的修补程序
* 论坛组件上的搜索问题。 NPR-26577：适用于 CQ-4251303 的修补程序
* 在Communities消息中同时搜索名字和姓氏不会返回预期结果。 NPR-26377：适用于 CQ-4253150 的修补程序
* 删除回复时分页未更新。 NPR-26327
* 删除帖子会起作用，但控制台会出现错误，并且帖子在UI中仍然可见。 NPR-26292：适用于 CQ-4252803 的修补程序
* 分页不会动态更新，并且回复列表持续变长。 NPR-26145：适用于 CQ-4251586 的修补程序
* 在包含5万~10万用户的组上无法加载组设置。 NPR-25642：适用于 CQ-4238426 的修补程序
* 目录资源播放器的上下文路径失败。 NPR-25640：适用于 CQ-4238426 的修补程序
* （论坛搜索）- 包含大量帖子的线程的分页链接不适用于通知。适用于 CQ-4254202 的修补程序
* 使用Firefox时，审核控制台仅显示5个条目。 适用于 CQ-4254128 的修补程序
* 创建站点时组不可见。 NPR-27148：适用于 CQ-4251788 的修补程序
* 将组和成员添加到“角色”设置中，并在博客功能中允许拥有权限的成员时，出现空指针异常。NPR-21732、NPR-27176：适用于 CQ-4255909 的修补程序
* 编辑站点并在角色设置中添加成员会引发空指针异常。 NPR-27132：适用于 CQ-4255909 的修补程序

#### 用户界面 {#user-interface}

* 主动平台登录修复。 NPR-26961
* （多字段）允许复合项目拥有自定义名称。NPR-26493：适用于 Granite-20568 的修补程序
* 粘贴页面后，列视图在刷新之前不会更新。 NPR-26030：适用于 CQ-4236346 的修补程序
* 主动式granite.ui.commons修复。 NPR-26960
* 主动式granite.ui.content修复。 NPR-26959
* 主动式CQ/体验日志修复。 NPR-26943
* 主动式Foundation UI反向移植。 NPR-26942
* (IE 11) 键入负值时，数字字段中会显示“NaN”。NPR-26701：适用于 CQ-100826 的修补程序
* （Coral 多字段）嵌套的多字段使用错误模板来创建项目。NPR-25649：适用于 CUI-6743 的修补程序
* 更新 granite coralui2 和 coralui3 clientlib 以从内部版本中删除 Handlebars。NPR-25606：适用于 Granite-22116 的修补程序

### 表单 {#forms-7}

### Forms 附加组件包 {#forms-add-on-package-7}

#### 表单 - 文档安全 {#forms-document-security-2}

* 非活动密钥的服务器日志中出现主体密钥滚动更新异常。 NPR-26748：适用于 CQ-4253705 的修补程序
* 无法创建或修改Document Security的水印设置。 NPR-26267、NPR-26129：适用于 CQ-4250234 的修补程序

#### 表单 - 文档服务 {#forms-document-services-4}

* 使用“验证 PDF/A”进行 PDF/A 验证时，未显示有效。NPR-25934：适用于 CQ-4248558 的修补程序

#### 表单 - 交互式通信 {#forms-interactive-communication}

* 编辑、保存可编辑的PDF，然后打开/关闭HTML预览时，可在同一窗口中查看和查看信件的PDF预览和预览功能。 NPR-26770：适用于 CQ-4253217 的修补程序

#### 表单 - 工作流 {#forms-workflow-2}

* 工作区间歇性挂起并重复显示起始点。 NPR-26461：适用于 CQ-4253439 的修补程序
* 当任务名称中使用大括号时，日志中会引发ESAPI异常。 适用于 CQ-4256627 的修补程序
* 打开与起点关联的非预填充自适应表单/表单集时，会引发空指针异常。 适用于 CQ-4256124 的修补程序
* 无法使用全局设置发送电子邮件。 NPR-26163：适用于 CQ-111110 的修补程序
* 应用axis.jar文件后无法打开工作区。 NPR-26131：适用于 CQ-4251126 的修补程序
* “刷新”按钮无法将最新数据从服务器同步到自适应表单。适用于 CQ-4255670 的修补程序
* 从管理员 UI 设置搜索模板，然后使用该模板在 AEM Forms 工作区中搜索任务会引发异常。适用于 CQ-4255649 的修补程序
* 名称中带有圆括号符号的应用程序下的进程跟踪详细信息未显示在 HTML 工作区中。适用于 CQ-4242101 的修补程序
* 在HTML工作区的首选项屏幕中保存更改会引发异常。 适用于 CQ-4241485 的修补程序
* 最新JEE设置的批量审批中断。 适用于 CQ-4241486 的修补程序
* 最新6.4 JEE服务器上的任务/起始点草稿失败。 适用于 CQ-4241484 的修补程序
* 设置Date()。getTime()。toString参数以初始化会话而不是Date.toString()。 适用于 CQ-4241483 的修补程序
* 打开 /lc/ws 时，发现 HTML 参数中存在易受攻击的字符异常。适用于 CQ-4241481 的修补程序

#### 漏洞 {#vulnerability-1}

* 表单管理器的注释选项卡中存在存储型跨站点脚本 (XSS) 漏洞。NPR-27157：适用于 CQ-4255556 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* 企业安全API的代码审查。 适用于 CQ-4255638 的修补程序
* 未能在WAS9中将esapi.properties作为类加载器资源加载。 适用于 CQ-4255631 的修补程序
* 在域配置期间单击添加身份验证会引发错误。 适用于 CQ-4255634 的修补程序
* Forms JEE 支持 PKCS#11 双向身份验证。NPR-21372
* 修复了核心的静态代码分析中报告的问题。 适用于 CQ-104446 的修补程序
* 运行 LCM 时，部署 adobe.livecycle.weblogic.ear 和 adobe.livecycle.websphere.ear 会失败。适用于 CQ-4255629、CQ-4255630 的修补程序
* 应用程序管理中出现无效的错误消息。NPR-23289：适用于CQ-4233163、CQ-4255636的修补程序
* 在域配置期间单击“添加身份验证”会导致错误。 适用于 CQ-4255634 的修补程序

#### 表单 - JEE 连接器 {#forms-jee-connector}

* 修复了连接器的静态代码分析中报告的问题。 NPR-22260

#### PDFG 服务 {#pdfg-service-1}

* 从LiveCycle升级到AEM 6.2表单后，日志中出现org.jgroups.Message错误。 NPR-26795：适用于 CQ-4220415 的修补程序
* AEM forms — 迁移样式时出错。 适用于 CQ-4251969 的修补程序
* 修复了PDFG静态代码分析报告中报告的问题。 NPR-23251：适用于 CQ-4213930 的修补程序

#### 6.3.3.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-3}

AEM 6.3.3.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/63sp3cfp1bundlelist.txt)

AEM 6.3.3.1 中包含的内容包列表

### 累积修补程序包 6.3.2.2 {#cumulative-fix-pack-8}

AEM 累积修补程序包 6.3.2.2 是一个重要更新，它包括自 2018 年 4 月 AEM 6.3 Service Pack 2 (6.3.2.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包 6.3.2.2 依赖于 AEM 6.3 Service Pack 2。因此，您必须先安装 AEM 6.3 Service Pack 2，然后再安装 AEM 累积修补程序包 6.3.2.x。有关安装说明，请参阅 [AEM 6.3 Service Pack 2 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp2-release-notes.html)。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.11。
* 在Brand Portal上启用了子资源和多页面资源查看器。
* 已将字段类型的长度更改为255，以支持不同类型附件的所有可能的mime类型。
* 已配置当图像违反上载条件时来自服务器的错误消息。
* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。
* 更新至cq-wcm-content和com.adobe.cq.launches.it.serverside的最新版本。
* 将com.adobe.granite.ui.coralui3-rte更新至已发布的最新版本。
* 当 expressionResolver 为 null 时，确定的呈现条件返回正常结果。
* Coral.ColumnView：添加了对“按住 Shift 键单击”的支持。

### 资产 {#assets-8}

* 资产文件夹封闭用户组(CUG)字段不返回“所有人”组。 NPR-23163：适用于 CQ-4239377 的修补程序
* 搜索智能收藏集保存的搜索不会返回所有结果。 NPR-23243：适用于 CQ-4240355 的修补程序
* (ExpiryNotificationJobImpl) 优化了现有查询。NPR-23330：适用于 CQ-4205249 的修补程序
* （元数据配置文件）创建时设置的标准标记值在保存后不可用。NPR-23370：适用于 CQ-4235458 的修补程序
* （触屏 UI）由于 JS 错误，无法移动多个资产。NPR-23395：适用于 CQ-4241279 的修补程序
* 下载大小与显示的信息不匹配不正确，导致用户混淆。 NPR-23418：适用于 CQ-4242774 的修补程序
* 为文件扩展名LSR和SKETCH提取的mimetype不正确，并导致文件下载无效。 NPR-23644：适用于 CQ-4243260 的修补程序
* (Firefox/Chrome) 无法在“资产共享”页面中下载资产。NPR-23963：适用于 CQ-4244391 的修补程序
* 预览后，搜索面板中的资产管理员搜索彩块化消失。 NPR-23964：适用于 CQ-4244410 的修补程序
* 取消发布搜索表单会完全删除默认搜索表单。 NPR-23291：适用于 CQ-4241382 的修补程序
* (Brand Portal) 应在复制时筛选出目录谓词中的搜索。NPR-23292：适用于 CQ-4241385 的修补程序
* 发布到Brand Portal UI操作不可用。 NPR-23293：适用于 CQ-4241161 的修补程序
* “发布/取消发布到Brand Portal”按钮应该对内容片段不可用。 NPR-23318：适用于 CQ-4245086 的修补程序
* (Brand Portal) 发布资产后允许创建子资产。NPR-23331：适用于 CQ-4242018 的修补程序
* Dynamic Media请求不使用代理/HTTP公共客户端。 NPR-10727：适用于CQ-45695、CQ-88800的修补程序
* 无法在Dynamic Media S7 (DMS7)中为单个演绎版MP4视频资源添加批注。 NPR-22046：适用于 CQ-4215912 的修补程序
* 对于 Ptiff 生成流程，EmbedXMP 数据始终设置为“活动”。NPR-22903：适用于 CQ-4234498 的修补程序
* 大量图像预设存在动态演绎版显示/选择问题。 NPR-23151：适用于 CQ-4217511 的修补程序
* Dynamic Media编码视频 — 修改/重新上传启动器出现问题。 NPR-23237：适用于 CQ-4240260 的修补程序
* 修复了 Dynamic Media S7 中 HTTP 转发器的代理处理问题。NPR-24001：适用于 CQ-244140 的修补程序

### 站点 {#sites-8}

* 查询生成器差异导致 6.2 与 6.3 之间的 xPath 转换不同。NPR-23245：适用于 CQ-4240396 的修补程序
* 展开对话框时，页面属性中的“缩略图”选项卡不起作用。NPR-22844：适用于 CQ-4241474 的修补程序
* Parsys中断了模拟器设备框架宽度，并裁切掉其中添加的任何组件。 NPR-22926：适用于 CQ-4238224 的修补程序
* 执行多个启动项时，会在Author中提升该启动项，但是由于缺少复制权限，因此不会在Publish服务器上复制更改。 NPR-22934：适用于 CQ-4234746 的修补程序
* 用户在第一个会话中锁定的页面，可以被另一个会话中的其他用户修改。NPR-23057：适用于 CQ-4199017 的修补程序
* 修复了列表视图中的可重新排序选项。 NPR-23065：适用于 CQ-4239321 的修补程序
* （页面编辑器）再次打开对话框时，图像组件上的图像消失。NPR-23156：适用于 CQ-4239978 的修补程序
* 模板编辑器仅显示20个模板/文件夹，滚动到页面底部时不会加载其他模板/文件夹。 NPR-23185：适用于 CQ-4238483 的修补程序
* （经典 UI）移动或重命名页面时产生错误。NPR-23213：适用于 CQ-4240971 的修补程序
* 无法编辑/创建ContextHub段。 NPR-23218：适用于 CQ-4226948 的修补程序
* （富文本编辑器）- 替换操作会更改单词的格式。NPR-23271：适用于 CQ-4239677 的修补程序
* XF变体的Blueprint选项卡中缺少转出按钮。 NPR-23320：适用于 CQ-4240404 的修补程序
* 由于已被弃用，经典UI无法编辑CUG。 NPR-24122：适用于 4241823 的修补程序
* 用于防止有害内容促销的主动修复。 NPR-24387：适用于 4244993 的修补程序
* 一次大约 在Assets的某个文件夹中添加80个片段，从时间轴控制台触发工作流时遇到错误。 NPR-23393：适用于CQ-4211216的修补程序
* 无法将图像从内容查找器拖放到富文本编辑器对话框中。 NPR-23403：适用于 CQ-4242094 的修补程序
* 将组件从 AEM 6.0 迁移到 AEM 6.2 时出现“无效的递归选择器值”错误。NPR-23532：适用于 CQ-4241258 的修补程序
* （富文本编辑器）工具提示显示插件的变量名称，而不是可读的插件名称。NPR-23550：适用于 CQ-4243269 的修补程序
* 无法在移动设备/平板电脑版本中使用所需的选择下拉列表保存对话框。 NPR-23904：适用于 CQ-4243096 的修补程序
* 样式系统选项显示在安装6.3.2.1之后的所有页面上。 NPR-23972：适用于 CQ-4244394 的修补程序
* 由于已被弃用，经典UI无法编辑CUG。 NPR-24122：适用于 4241823 的修补程序
* 用于防止有害内容促销的主动修复。 NPR-24387：适用于 4244993 的修补程序
* 移动资产时，资产引用不会更新。 NPR-23208：适用于 CQ-4239879 的修补程序

### 平台 {#platform-1}

* 如果在搜索Facet中使用标记谓词，则智能收藏集在保存后不显示结果。 NPR-23401：适用于 Granite-21278 的修补程序
* 修补 clientlib 中的 jQuery 1.12.4 以包含安全修补程序。NPR-24128：适用于 Granite-20058 的修补程序
* 除非重新启动捆绑包，否则国际化翻译不会更新。 NPR-23193：适用于Sling-7190的修补程序
* ReplicationEventListener中的资源解析程序未关闭。 NPR-23240：适用于 CQ-4241350 的修补程序
* 在“Day CQ Mail Service”中支持STARTTLS。 NPR-23941：适用于 CQ-4240397 的修补程序
* JCR投诉标记名称应根据标记标题自动填充。 NPR-24173：适用于 CQ-4199411 的修补程序

### 集成 {#integration-4}

* (Target) 将 API 类型用作 XML 时，不会激活营销活动。NPR-23199：适用于 CQ-4240936 的修补程序****
* 对于中间文件夹结构，配置引用复制失败。 NPR-23485：适用于 CQ-4242751 的修补程序

### 漏洞 {#vulnerability-2}

* Salesforce 集成容易遭受服务器端请求伪造 (SSRF) 攻击。NPR-24289：适用于 CQ-424527 的修补程序
* 管理员UI项目链接中存在跨站点脚本(XSS)。 NPR-23272：适用于 CQ-4241795 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components}

* Foundation表容易遭受存储型跨站点脚本攻击。 NPR-23214：适用于 CQ-4240760 的修补程序

### 翻译 {#translation-3}

* 创建语言副本时未删除Live Copy属性。 NPR-23123：适用于 CQ-4230641 的修补程序

### 用户界面 {#user-interface-1}

* DatePicker不支持手动设置隐藏字段设置的外部类型提示。 更改类型提示时出现转换错误。 NPR-23371：适用于 Granite-21194 的修补程序
* Coral.ColumnView：添加对Shift +单击的支持。 NPR-23404：适用于 Granite-13338 的修补程序
* 选择具有空值的项目时，选择RT不会验证。 NPR-23405：适用于 Granite-21283 的修补程序
* (OMEGA) 仅以英语报告“功能”。NPR-23990：适用于 Granite-21231 的修补程序
* 修复了Coral.Autocomplete API。 NPR-23516

### Granite {#granite-1}

* Apache Http客户端跟踪连接和高栈利用率导致AEM服务器崩溃。 NPR-23906：适用于 Granite-21056 的修补程序

### 商务 {#commerce-2}

* 营销活动json输出不包含servlet上下文根。 NPR-23733：适用于 CQ-4243827 的修补程序

### 社区 {#communities-7}

* 对社区的搜索因几个字而失败。 NPR-23256：适用于 CQ-4240717 的修补程序
* 无法为社区管理者角色分配组的问题。 NPR-23317：适用于 CQ-4241233/CQ-4221399 的修补程序
* 创建具有相似资源名称的资源时出现问题。 NPR-23319：适用于 CQ-4240700 的修补程序
* (ContextPath) 在社区组成员列表中搜索组成员时，中断消息功能因 Jetty 配置和错误而中断。NPR-23336：适用于CQ-4241519、CQ-4242080的修补程序
* 上传图像到Communities论坛时未显示在Adobe存储资源提供程序(ASRP)中。 NPR-23397：适用于 CQ-4242497 的修补程序
* 已删除的创意在活动中显示为活动链接。 NPR-23406
* 无法通过以上下文根运行的AEM加载imsmanifest.xml。 NPR-23483：适用于 CQ-4242193 的修补程序
* 旧版Handlebars中存在安全漏洞。 NPR-23518：适用于 CQ-4243055 的修补程序
* 通道服务无法正常工作。 NPR-23543：适用于 CQ-4242217 的修补程序
* 通过Dispatcher访问时社区组件出现问题，并为其启用Sling Dynamic Include。 NPR-23586：适用于CQ-4242360、CQ-4241522的修补程序
* 当搜索通过搜索产生许多结果的搜索词，然后输入新的搜索词时，不重置分页。 NPR-23739：适用于 CQ-4222593 的修补程序
* 对论坛组件执行搜索时出现问题。 NPR-23838：适用于 CQ-4243770 的修补程序
* （社区审核标记）无法批量允许已标记的消息。NPR-23845：适用于 CQ-4243962 的修补程序
* 尽管选择了默认排序顺序，但排序按钮文本未显示默认选定值。 NPR-23881：适用于 CQ-4243375 的修补程序
* 由于向组发送消息失败，未触发 Web 和邮件通知。NPR-23934：适用于 CQ-4242880 的修补程序
* 使用DSRP配置时不会显示有关标记用户和原因的详细信息。 NPR-23973：适用于 CQ-4243205 的修补程序
* 未标记用户的标记原因仍然可见/ NPR-23974：适用于CQ-4243822的修补程序
* 将两个同名文件附加到表单帖子两次，会导致服务器错误。 NPR-24166：适用于 CQ-4244367 的修补程序
* 使用数据库存储资源开发人员(DSRP)无法存储mime类型超过15个字符的附件。 NPR-24174
* 将违反上传标准的图像拖放到帖子文本中时，会引发服务器错误，并向用户显示一般错误消息。 NPR-24243
* 修复了多个AEM Communities服务器端问题。 NPR-23971：适用于CQ-4243144、CQ-4242145、CQ-4243365、CQ-4244098的修补程序
* 修复了若干Adobe Social问题。 NPR-24242：适用于 CQ-4245054、CQ-4245120、CQ-4245296 的修补程序

### 营销活动 {#campaign}

* 营销活动json输出不包含servlet上下文根。 NPR-23733：适用于 CQ-4243827 的修补程序

### MSM {#msm}

* 转出页面时，LiveCopy 不会显示从母版继承的打开/关闭时间属性。NPR-23873：适用于 CQ-4243431 的修补程序
* LiveCopy操作不会忽略已删除组件的子节点。 NPR-23058：适用于 CQ-4211662 的修补程序

### 卸载 {#offloading}

* 请求机制在处理后或定期从工作线程实例中清理资产。NPR-23638：适用于 Granite-21337 的修补程序

## 表单 {#forms-8}

### Forms 附加组件包 {#forms-add-on-package-8}

#### 自适应表单 {#adaptive-forms-1}

* 将ReCaptchaConfigService移动到内部包。 适用于 CQ-4217459 的修补程序
* 数值字段不遵循最小值。 NPR-23967：适用于 CQ-4244830 的修补程序
* 在自适应Forms与AdobeSign的集成中支持多分片。 NPR-23383

#### 后端集成 {#backend-integration}

* (FDM)（Web 服务）在 WSDL 解析器中支持 WSDL 的扩展结构。NPR-23640，NPR:23236: 适用于 4205821 的修补程序
* 在Forms加载项客户端SDK中包含SDLInvokerParams。 NPR-23157

### Forms JEE 安装程序 {#forms-jee-installer-7}

#### 进程管理 {#process-management}

* 应用新的axis.jar文件后无法打开工作区。 NPR-23316
* LiveCycle在PMAdmin上易受到XSS攻击。 NPR-23267
* 升级到 AEM 6.1 Forms 后，访问特定用户的任务列表时，HTML 工作区会冻结。NPR-23943

#### 核心 {#core}

* Forms JEE 支持 PKCS#11 双向身份验证。NPR-21372

#### PDFG 服务 {#pdfg-service-2}

* 同时处理TIFF文件（大小约为50 KB ）时，纸张捕获服务崩溃。 NPR-23556

#### Forms Designer {#forms-designer}

* AEM Forms Server输出 — 注释缺少替代描述。 NPR-22207
* 为通过Designer和Output Service生成的XML表单添加PDF/UA支持。 NPR-23132

### 6.3.2.2 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-4}

AEM 6.3.2.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_3_2_2_bundle-list.txt)

AEM 6.3.2.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### 累积修补程序包 6.3.2.1 {#cumulative-fix-pack-9}

AEM 累积修补程序包 6.3.2.1 是一个重要更新，它包括自 2018 年 4 月 AEM 6.3 Service Pack 2 (6.3.2.0) 正式发布以来的若干内部修补程序和客户修补程序。

**AEM 累积修补程序包**&#x200B;的主要功能亮点包括：

* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.10。
* 改进了经典UI中Parsys组件的呈现方式。
* 更新了Sling模型包以包含字符集修复。
* 已针对所有资源类型异步发布到Brand Portal。
* 将coralui-component-richtexteditor.git从0.1.15更新到0.1.16
* 修复了下拉组件的显示/隐藏功能。
* 为核心图像组件启用了图像翻转。
* 更新了felix http包以启用会话属性。

* 由于内存消耗问题，移除了 Sling 模型上的 cache=true。

### 资产 {#assets-9}

* 在“资产文件夹”设置中更改标题或缩略图图片时，文件夹的原始组和权限会被覆盖。NPR-22171：适用于 CQ-4216080 的修补程序
* UI会引发虚假错误“发布到Brand Portal失败”，而作业会添加到复制队列并且资产会发布到Brand Portal。 NPR-22179：适用于 CQ-4205273 的修补程序
* （触屏 UI）列视图中资产的默认上传位置。NPR-22465：适用于 CQ-4237057 的修补程序
* 尝试将资产架构从/conf/global复制到/conf/ mytenant时，AEM会引发StackOverflow错误。 NPR-22489：适用于 CQ-4235875 的修补程序
* 由于文件夹名称末尾有空格，因此尝试解压缩ZIP存档失败。 NPR-22522：适用于 CQ-4238036 的修补程序
* 使用资源标题列排序不适用于搜索结果。 NPR-22908：适用于 CQ-4239076 的修补程序
* Youtube视频使用完整路径进行标记，而不是标记名称本身。 NPR-22976：适用于 CQ-4238669 的修补程序
* 在可重新排序的文件夹下重新排序文件夹不会持久保留。 NPR-23125：适用于 CQ-4231761 的修补程序
* 尝试使用共享链接共享收藏集时，出现HTTP 504：网关超时错误。 NPR-21928：适用于 CQ-4234507 的修补程序
* 当一个PDF资源有多个关联的关键字时，无法正确提取和正确修改PDF关键字元数据。 要解决此问题，已为PDF资源删除主题字段元数据属性。 但是，您可以编辑元数据架构以便为主题字段添加多值文本字段。 NPR-21972：适用于 4215741 的修补程序****
* 如果在显示2个弹出窗口之间更改了选定的文件夹，则会删除错误的资源。 NPR-21980：适用于 CQ-4233675 的修补程序
* (DAM) 添加到收藏集向导时，出现多个跨站点脚本 (XSS) 漏洞。NPR-22432：适用于 CQ-4327086 的修补程序
* 在 Safari 上的资产中使用数字版权管理时，资产下载失败。用户无法下载包含免责声明和长文件名的资产。NPR-22747：适用于 CQ-4236460 和 CQ-4235274 的修补程序
* 将公共共享设置为将资产发布到Brand Portal时的默认选项。 NPR-21931：适用于 CQ-4218816 的修补程序

### 站点 {#sites-9}

* 工作流收件箱中的新项目显示页面路径而非页面标题。NPR-21634：适用于 CQ-4230672 的修补程序
* 可编辑的结构组件在编辑时丢失了响应式网格所需的CSS类名称。 NPR-21741：适用于 CQ-4232374 的修补程序
* （触屏 UI）HTL 组件存在多个跨站点脚本 (XSS) 漏洞。NPR-21899：适用于 CQ-4232511 的修补程序
* 无法更改内容片段混合媒体图像资源类型。 NPR-21907：适用于 CQ-4233401 的修补程序
* 触屏UI对话框的RTE全屏正在隐藏RTE插件。 NPR-22034：适用于 CQ-4235457 的修补程序
* （触屏 UI）富文本编辑器会从 &lt;a> 标记中删除 id 以外的所有其他属性。NPR-22044：适用于 CQ-4234133 的修补程序
* 由于长时间运行的查询（超过6个）产生了多个栈叠Parsys，导致AEM运行缓慢。 NPR-22134：适用于 CQ-4233904 的修补程序
* 无法更改名称中包含冒号的节点的权限。 NPR-22136：适用于 CQ-4236221 的修补程序
* （经典 UI）富文本编辑器输出 html 将“list-position-style: inside;”作为内嵌样式添加到 &lt;ul> 标记中。NPR-22145：适用于 CRTE-114 的修补程序
* 当文本为空时，使TreeNode回退到name属性。 NPR-22146：适用于 CQ-4234724/CQ-4236300 的修补程序
* RSS馈送问题，从端口–1到AEM 6.3。NPR-22176：适用于CQ-4233339的修补程序
* （经典 UI）粘贴文本快捷键 (Ctrl+V) 对 OOTB 文本（富文本）组件不起作用。NPR-22224：适用于 CQ-4236224 的修补程序
* 在键入文本时，Tagfield 的筛选功能无法按预期发挥作用。NPR-22236：适用于 CQ-4236655 的修补程序
* （页面编辑器）在图像映射组件中粘贴文本数据时，也会粘贴文本组件。NPR-22264：适用于 CQ-4236230 的修补程序
* 对话框文件上载字段必填项导致对话框提交时出现问题。 NPR-22464：适用于 CQ-4222192 的修补程序
* 如果无法激活移动的页面或其反向链接，移动w/o复制权限会启动激活工作流请求。 NPR-22467：适用于 CQ-4211765 的修补程序
* 加载包含大量（2000 及以上）受众的页面时，出现性能问题。NPR-22478：适用于CQ-4209567的修补程序
* 在初始化过程中 ContextHub 存储覆盖默认持久层时出现持久性问题。NPR-22479：适用于 CQ-4218399 的修补程序
* 如果未在第一个内容根上选中“包含子页面”，则包含多个页面的启动不会将子页面发布到发布服务器。 NPR-22482：适用于 CQ-4237818 的修补程序
* （触屏 UI）通过经典 UI 控制台删除启动项会使所有页面无法编辑。NPR-22491：适用于 CQ-4225074 的修补程序
* 由于对话框中的额外空间，图像组件出现问题。 NPR-22528：适用于 CQ-4238183 的修补程序
* 使用inlide模式打开组件时，之前加载的插件第二次不可见。 NPR-22591：适用于 CQ-4236850 的修补程序
* 删除嵌套启动项中的启动项，会导致子启动项变得孤立。NPR-22621：适用于CQ-4202639的修补程序
* （经典 UI Sidekick）当页面处于工作流锁定阶段时，“工作流”选项卡被禁用。NPR-22722：适用于 CQ-4237557 的修补程序
* 在页面上翻转添加到图像组件中的图像后，更改未保存，并且原始图像显示在页面上。 呈现支持已通过 [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141) 添加到图像核心组件。NPR-22801：适用于 CQ-4221539 的修补程序
* 当用户尝试从锚点菜单删除现有锚点时，富文本编辑器组件窗口关闭，并且更改保持未保存状态。 NPR-22802：适用于 CQ-4238167 的修补程序
* Omnisearch筛选器未显示站点控制台中的所有操作。 NPR-22804：适用于 CQ-4239007 的修补程序
* 操作系统剪贴板以及内部 AEM 剪贴板的触屏 UI 中存在复制/粘贴问题。NPR-22807：适用于 CQ-4220383 的修补程序
* Lucene搜索返回的摘录突出显示不一致。 NPR-22879：适用于 CQ-4238513 的修补程序
* 在发布实例关闭的情况下激活页面会导致绿色状态而不是变为琥珀色。 NPR-22927：适用于 CQ-4236310 的修补程序
* (StyleSystem) 从弹出窗口中选择样式时，屏幕位置会跳转。NPR-23183：适用于 CQ-4238867 的修补程序
* （管理发布）需要多次点击，方可移至日历的下个月。NPR-23508：适用于 CQ-4242732 的修补程序

### 平台 {#platform-2}

* Sling导出程序servlet无法正确导出日语字符。 NPR-22153：适用于 CQ-4228920 的修补程序
* 启动期间调度程序死锁。 NPR-22440：适用于Sling-7004的修补程序
* 无法在两个发布实例之间同步组。NPR-21943：适用于 Granite-19564 的修补程序
* org.apache.sling.i18n共享会话/资源解析程序存在性能问题。 NPR-23390：适用于Sling-7543的修补程序

### 集成 {#integration-5}

* com.day.cq.analytics.sitecatalyst中的ResourceResolver未关闭。 NPR-22323：适用于 CQ-4236515 的修补程序
* 长时间运行的查询期间，TargetContentImpl会导致AEM运行缓慢。 NPR-22361：适用于 CQ-4236907 的修补程序
* 目标引擎(mbox.js、at.js)不使用损坏的URL，并使用包含冒号的URL，这可能会导致某些部署失败。 NPR-22366：适用于 CQ-4237854 的修补程序
* 提供自定义at.js或mbox.js时，include脚本将以文本形式写入page，而不是HTML标签。 NPR-22441：适用于 CQ-4203691 的修补程序
* 在“目标”模式下，作者无需取消继承即可修改从Blueprint继承的组件。 NPR-22751：适用于 CQ-4237907 的修补程序
* 由于缺少jcr ：content节点，PersonalizationDataSource引发空指针异常。 NPR-22850：适用于 CQ-4222122 的修补程序
* 使用非英语时，AEM定位失败。 NPR-22917：适用于 CQ-4218213 的修补程序
* 发布包含目标内容的页面时缺少相关资源。 NPR-23064：适用于 CQ-4227119 的修补程序
* 用户在 mbox 调用中看不到测试静态参数值，而在云配置中使用 AT.js 作为客户端库进行测试时，则可以看到这些值。NPR-21930：适用于 CQ-4234520 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-1}

* 取消选中取消/禁用继承复选框后，iParsys将创建位置偏移。 NPR-21905：适用于 CQ-4230951 的修补程序
* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-22327：适用于 CQ-4222853 的修补程序
* 为了提高安全性，已弃用 CAPTCHA 组件。如果您使用的是 CAPTCHA 组件，则在安装 6.3.2.1 或更高版本后，将显示“Captcha 组件已弃用，不应再使用”消息。可以自定义 AEM 组件来包含 reCAPTCHA 以提高安全性。NPR-22151：适用于 CQ-4220052 的修补程序

### WCM - 页面编辑器 {#wcm-page-editor}

* 使用无效选择器时导致反射型跨站点脚本攻击 (XSS)。适用于 CQ-4270397 的修补程序

### 翻译 {#translation-4}

* 调查预览功能存在的问题。NPR-22114：适用于 CQ-4223753 的修补程序

### 用户界面 {#user-interface-2}

* 设置“最小值”和“最大值”日期范围时，Coral Calendar月份选取器出现问题。 NPR-22716：适用于 CUI-7187 的修补程序
* （经典 UI）即使关联的表单数据模型服务设置为空字段，组件也会显示默认值。NPR-22272：适用于 GRANITE-19744 的修补程序

### Granite {#granite-2}

* 内存泄漏导致资产共享 AEM 发布者实例出现稳定性问题。NPR-22205、NPR-23178：适用于Sling-5668、Sling-7292和Sling-7470的修补程序。
* 不稳定的服务ID不应用于会话属性名称。 NPR-22821：适用于 Granite-21059 的修补程序
* 当 http 白板管理的会话失效时，如果容器会话不含其他会话属性，则容器会话也将失效。NPR-23059：适用于FELIX-5819的修补程序
* LogbackManager在启动时可能会丢失一些OSGi配置。 NPR-23060：适用于 Granite-19791 的修补程序

### 商务 {#commerce-3}

* 在“体验片段”菜单中启用创建工作流。 NPR-22347：适用于 CQ-4221661 的修补程序
* 体验片段错误可在WeRetail上重现。 NPR-21958：适用于 CQ-4220061 的修补程序
* 激活包含已删除体验片段的页面会引发NullPointerException。 NPR-23179：适用于 CQ-4239939 的修补程序

### 项目 {#projects}

* （多语言项目）项目不会列出超过 19 种语言的翻译作业。NPR-22498：适用于 CQ-4229978 的修补程序

### 工作流 {#workflow}

* （经典 UI）启用或禁用工作流启动器会导致不良行为。NPR-22907：适用于 CQ-4239153 的修补程序

## 表单 {#forms-9}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

AEM Forms的主要功能亮点包括：

* 添加了对HTML5输入类型的支持。
* 修复了基本SOAP标头身份验证。
* 添加了对超链接的标题属性的支持。
* 在Forms Designer的辅助功能树中启用了PDF/UA标识符。
* 为 Workbench 用户启用了证书身份验证。
* 增加了对生成符合PDF/A-2a或PDF/A-3a的PDF文件的支持。

### Forms 附加组件包 {#forms-add-on-package-9}

#### 表单 - 管理员 UI {#forms-admin-ui}

* 检查ECM连接器配置页面的密码字段时，密码以纯文本显示。 NPR-22508：适用于 CQ-4236065 的修补程序

#### 表单服务 {#forms-service}

* 启用 SSL 后，“提交”和“放弃”事件不适用于表单分析。NPR-22637：适用于 CQ-4237973 的修补程序

#### 用户管理 {#user-management}

* 由于cglib-nodep版本不正确，无法同步LDAP。 NPR-22493：适用于 CQ-4234099 的修补程序

#### 自适应表单 {#adaptive-forms-2}

* 在调用函数后，规则编辑器的自定义函数添加一个额外的 ;，即使自定义函数返回 true，验证也会失败。NPR-22481：适用于 CQ-4235499 的修补程序
* 显示最小和最大验证消息时，无论选择何种日期模式，日期选取器组件都不遵循该模式。 NPR-22444：适用于 CQ-4236269 的修补程序
* 提交请求中发送的日期格式应与日期选取器组件中提供的模式一致。 NPR-22384
* Android 6.0 Samsung设备不遵循为自适应表单文本框指定的最大字符数。 NPR-22363、NPR-22364：适用于 CQ-4235205 的修补程序
* (Microsoft Edge) (IE 11) 具有多行字段的自适应表单文本字段组件显示“Null”作为默认值，而不是空白。NPR-22284：适用于 CQ-69107 的修补程序
* 自适应Forms中的SOAP UTF-8输入编码返回错误，并出现乱码页面。 NPR-20105：适用于 CQ-4222669 的修补程序
* 一旦在站点页面中配置了错误的表单，AEM Forms容器组件便不可编辑。 适用于 CQ-4237456 的修补程序
* 在JEE服务器上执行开发测试时失败。 适用于 CQ-4222082 的修补程序
* 由于Calvin框架中的缩小问题，JEE服务器上的AF测试失败。 适用于 CQ-4217220 的修补程序

#### 表单管理器 {#forms-manager}

* (Firefox) 无法更新自适应表单的 XML 架构属性，因为记录文档 (DOR) 中的选项未在属性页面中预先选择。NPR-22298：适用于 CQ-4237402 的修补程序
* 发布网站时，发布页面后修改的Forms不会再发布。 NPR-23013：适用于 CQ-4236566 的修补程序

#### 后端集成 {#backend-integration-1}

* SOAP服务的OOTB基本身份验证不适用于FDM集成中的基本身份验证。 NPR-23238：适用于 CQ-4241308 的修补程序

#### 通信管理 {#correspondence-management}

* 在信件内部使用并预览 OOTB XDP 时，会显示内容与页脚重叠。适用于 CQ-4212414 的修补程序

#### 汇编程序服务 {#assembler-service}

* 关于 PDF/A-1b 合规检查错误的 Acrobat DC 报告和 AEM 报告存在差异。NPR-22051、NPR-22050：适用于 CQ-4226128、CQ-4227671 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-8}

#### Workbench {#workbench}

* 为 Workbench 用户启用了证书身份验证。NPR-20644：适用于 CQ-4214486 的修补程序
* 使用Workbench下载服务器日志仅适用于一台服务器，对于另一台服务器则不起作用。 NPR-21079：适用于 CQ-4229842 的修补程序

#### 进程管理 {#process-management-1}

* （HTML 工作区）滚动条存在屏幕大小问题。NPR-23288
* （HTML 工作区）进程起点未按字母数字顺序排序。NPR-22841：适用于 CQ-4238944 的修补程序
* （HTML 工作区）关闭工作区中的表单时触发“准备数据”。NPR-21127：适用于 CQ-4224574 的修补程序
* （HTML 工作区）调用的进程需要较长说明的注释时，“注释”展开按钮不起作用。适用于 CQ-4241488 的修补程序

#### 核心 {#core-1}

* 启动计划程序时遇到错误。 NPR-22990
* 阻止浏览器存储输入到HTML表单中的凭据。 NPR-21762：适用于 CQ-4206543 的修补程序
* 应修复Core静态代码分析中报告的问题。 适用于 CQ-104446 的修补程序

#### PDFG 服务 {#pdfg-service-3}

* PDF 生成器无法生成具有指定书签级别的 PDF 文档。NPR-22921、NPR-22285：适用于 CQ-4230562 的修补程序
* 增加了对生成符合PDF/A-2a或PDF/A-3a的PDF文件的支持。 NPR-23021：适用于 CQ-4214172 的修补程序

#### Forms Designer {#forms-designer-1}

* 从设计器另存为PDF时缺少PDF/UA标识符。 NPR-23137
* 从Designer另存为PDF时，不会标记路径对象，例如边框、下划线和超链接。 NPR-23136
* 从Designer另存为PDF时，图像对象没有边界框。 NPR-23134
* 从Designer另存为PDF时，在Designer中定义的内联超链接不会进行标记，也不会有替换文本。 NPR-23133
* 使用AEM 6.3 Forms Designer打开XML数据包时，会从XML源中删除XHTML格式。 NPR-21178：适用于LC-3917046的修补程序

#### 安装 LCM {#install-lcm}

* 在安装程序和 LCM 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21370

#### 签名服务 {#signatures-service}

* 尝试通过HSM对PDF文档进行数字签名/认证时遇到异常。 NPR-21154：适用于 CQ-4226978 的修补程序

### 6.3.2.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-5}

AEM 6.3.2.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list_002_.txt)

AEM 6.3.2.1 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_comparison.txt)

AEM累积修补程序包6.3.1.2是一个重要更新，它包括自2017年10月AEM 6.3 Service Pack 1 (6.3.1.0)正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包的主要功能亮点包括：

* 修改了UI以支持在AEM Assets中实施CUG功能。
* 修复了许可证检查页面上的UI问题，以获得更好的体验。
* 在AEM Forms应用程序中启用了OSGi工作流任务支持。

### 资产 {#assets-10}

* 修改了UI以支持在AEM Assets中实施CUG功能。 NPR-19485
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
* 将用户添加到收藏集时出现性能问题。 NPR-20699：适用于 CQ-4225733 的修补程序
* 对于 Dynamic Media 集，不应允许从 AEM 发布到 Brand Portal。NPR-20320：适用于 CQ-4221147 的修补程序
* 含有空格和重音符号的视频不会在“呈现版本”页面上生成任何视频。NPR-19961：适用于 CQ-4221014 的修补程序
* 解决了Assets API的多个文件夹处理问题。 NPR-20569
* 当AEM服务配置中的目标路径指向根路径中的子文件夹时，AEM Dynamic Media Classic(以前的Scene7)无法从服务器同步资产。 CQ-4228265
* 已添加 Apache Commons `{org.apache.commons/commons-email/1.5}` 的电子邮件包，用于替换 `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`。

### 站点 {#sites-10}

* 管理员权限问题：无法从页面属性中移除“已关闭的用户组”成员。 NPR-20631
* 通过管理发布发布发布发布页面时，键入的工作流名称应在“通知”框中可用。 NPR-20046：适用于 CQ-4221586 的修补程序
* 在富文本编辑器中的两行上应用样式化文本，然后将它们合并为一个段落，会删除样式化跨区。NPR-20110：适用于 CQ-4223051 的修补程序
* 在“属性”编辑对话框的多个选项卡中对字段属性所做的更改有时不会保存。NPR-20286
* 内容片段中粘贴内容的末尾出现意外标记。NPR-20413：适用于 CQ-4224014 的修补程序
* 在 Adobe Campaign 中实施了一种机制，用于从外部定位资源中获取内容资源的策略。NPR-20667
* 富文本插件不适用于多字段触屏 UI 中的内嵌和全屏栏。NPR-20973

### 营销活动 {#campaign-1}

* 占位符在包含多个 Parsys 组件的页面中不可见。NPR-20436：适用于CQ-4215000的修补程序

### 商务 {#commerce-4}

* 体验片段在Internet Explorer 11中无法正常显示。 NPR-20161：适用于 CQ-4223319 的修补程序
* 在商务工作流中，当基于具有多个图像的主要产品创建变量时，会自动插入空白图像。NPR-20068：适用于 CQ-4222048 的修补程序
* 在产品控制台的收藏集页面上按标记筛选不起作用。 NPR-20292：适用于 CQ-4224023 的修补程序

### 社区 {#communities-8}

* 搜索结果与searchresult组件不一致。 NPR-20070：适用于 CQ-4220913 的修补程序
* 对于已发布的组件上的任何与版主相关的活动，不会触发电子邮件通知。 NPR-20122
* 为匿名社区用户显示无结果的空白分页。 NPR-20136：适用于 CQ-4220738 的修补程序
* 配置在检测到UGC为垃圾邮件时或用户在经过预审核的网站上发布帖子时的警报触发器。 NPR-20274：适用于 CQ-96850 的修补程序
* 解决了 AEM Communities 站点页面中的多个问题，包括错误的重定向和页面刷新问题。NPR-20344
* CommunityUserOperationExtension遇到类转换异常。 NPR-20532：适用于 CQ-4224385 的修补程序
* 创建社区站点后，用户无法从站点地图中打开它，因为上下文路径未添加到 URL 前面。NPR-20730

### 集成 {#integration-6}

* 将 Analytics 现有凭证迁移到 WSSE 身份验证。NPR-19962：适用于 CQ-4218071 的修补程序
* 进行任何修改后重新激活区段会失败并引发错误。 NPR-20054：适用于 CQ-4218401 的修补程序
* Search&amp;Promote 云服务配置忽略表单检索方法，导致其在创作实例上不可用。NPR-20447：适用于 CQ-4206076 的修补程序
* 安装 Search&amp;Promote 功能后，内容包中模糊不清的筛选器定义导致路径被覆盖。NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* 每次显示属性时，TXT 类型资产的元数据属性会显示在不同的元数据编辑器中。NPR-20239

### 平台 {#platform-3}

* 解决了资源解析程序未关闭的异常。NPR-19749：适用于 Granite-19143 的修补程序
* 请求在操作功能板中显示自定义卡片，以及默认的运行状况检查。NPR-20145
* 页面编辑器的注释层在 Internet Explorer 11 中无法正常工作。NPR-20222：适用于 CQ-4222818 的修补程序
* 在复制代理中将用户代理设置为管理员时出现会话泄漏。NPR-20578
* 没有为其他data-sly-resource语句取消设置requestAttributes。 NPR-20639：适用于 4226206 的修补程序
* 修复了 AEM 中 OOTB 资产的 curl Head 请求问题。NPR-20781：适用于 CQ-4221520 的修补程序

### 项目 {#projects-1}

* 从“项目”控制台访问不同项目需要较长时间才能加载。 NPR-20314
* 安装AEM 6.3.0.1会删除dam-update-service用户的密钥库。 NPR-20018
* 在某些自定义部署中，尝试在addTask模块中选择被分配人的用户需要更长的时间来填充用户选取器中的列表。 NPR-20283：适用于 CQ-4224193 的修补程序

### 用户界面 {#user-interface-3}

* Colorfield设置为“始终必需”，无论对话框中有什么属性。 NPR-19702
* 在Internet Explorer 11上，多字段组件滚动条未全屏显示。 NPR-20261：适用于 CQ-4219782 的修补程序
* 如果触发连续查询导致不正确的结果，之前的查询不会被中止。NPR-20398：适用于 GRANITE-19306 的修补程序

### 工作流 {#workflow-1}

* 用户在其收件箱中收到工作流任务时，不会发出相关通知。NPR-20213：适用于 CQ-4221639 的修补程序
* 在单击工作流模型的对话框参与者步骤中的下拉列表后，OOTB Granite 用户选取器未加载任何用户。NPR-20236

## 表单 {#forms-10}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-10}

#### 自适应表单 {#adaptive-forms-3}

* 缺少对重复面板的整合表达式的支持。NPR-20861
* 即使关联的表单数据模型服务未返回值，下拉列表也会显示上次存储的值。 NPR-20710
* 无法在规则编辑器中编辑具有布尔约束的现有规则。 NPR-21128

#### 表单门户 {#form-portal}

* 即使自适应表单的资产类型不是 XDP，也会为其显示 HTML 配置文件。NPR-20079

#### 后端集成 {#backend-integration-2}

* 无法将开关组件的值设置为true/false。 NPR-21111

#### OSGI工作流 {#osgi-workflow}

* 管理工作流提交仅列出十个应用程序。CQ-4230193

#### HTML5 表单 {#html-forms-3}

* 如果在辅助功能配置中未定义，则 XDP 表单对象（例如子表单）的名称会显示为其工具提示。NPR-20523

### Forms JEE 安装程序 {#forms-jee-installer-9}

#### 进程管理 {#process-management-2}

* FormSetPrefillApp 起点未预填充 AEM Forms 应用程序中的表单集字段。NPR-20950

#### Forms - AEM(LiveCycle) {#forms-aem-livecycle}

* 安装最新的 CTJPEG2K 库，以解决关键安全漏洞。这会影响 XMLFM（AEM 和 IfBA）、RM、PDFG 模块。NPR-20625：NPR-21337。

### 包含的功能包 {#feature-packs-included}

#### AEM Forms 应用程序 {#aem-forms-app}

* 在AEM Forms应用程序中启用了OSGi工作流任务支持。 CQ-4222638

### 6.3.1.2 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-6}

AEM 6.3.1.2 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_3_1_2-bundle-list.txt)

AEM 6.3.1.2 中包含的内容包列表

[获取文件](assets/do-not-localize/6_3_1_2-content-package-list.txt)
AEM 累积修补程序包 6.3.1.1 是一个重要更新，它包括自 2017 年 10 月 AEM 6.3 Service Pack 1 (6.3.1.0) 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包的主要功能亮点包括：

* 为默认的元数据架构表单启用了“发布到 Brand Portal”操作。
* 对于将 dc: title 属性设置为 String []（多字段）的图像，在图像卡片上显示标题时发生行为更改。
* 已将服务器端时间渲染替换为基础时间组件。
* 启用了从tagadmin/tagging控制台将标记从AEM发布到Brand Portal的功能。
* 发布了JSON API以使用内容片段。
* 内置存储库 (Apache Jackrabbit Oak) 已更新至版本 1.6.5。

### 资产 {#assets-11}

* 将具有相同属性的两个字段映射到不同类型的属性字段会引发内部错误。 NPR-19462：适用于CQ-4216828的HF
* dc： title和dc： description不会更改为crx /de中的多字段值。 NPR-19570：适用于CQ-4209086的HF
* Dynamic Viewer加载质量最低的视频演绎版，用于在创作模式下测试视频播放体验。 NPR-19004
* 无法为名称中包含空格的资产下载动态呈现版本。NPR-19433：适用于 CQ-4211738 的修补程序
* 无法使用 Chrome 在列视图中加载页面/资产的完整列表。NPR-19566：适用于 CQ-4214248 的修补程序
* 选择任何架构、搜索 Facet 或预设时，“发布到 Brand Portal”选项不可用。NPR-19550
* 在列视图中选择资源并单击编辑时，页面返回错误。 NPR-20301：适用于 CQ-4224052 的修补程序
* 在跨越正时区和负时区时，资产到期显示处于关闭状态。 NPR-20329：适用于 CQ-4219333 的修补程序

### 营销活动 {#campaign-2}

* 为营销活动选择默认体验后，营销活动滑块组件未显示。NPR-19213

### 集成 {#integration-7}

* 通过匿名用户访问时，自定义at.js文件不会发布。 NPR-19542：适用于 CQ-4219592 的修补程序
* 配置向导中的“定位引擎”字段设置为ContextHub (AEM)，而不是Adobe Target。 NPR-19320：适用于CQ-4218465的HF
* 创建体验时，受众部分损坏。 NPR-19110
* 如果对定位模块进行编辑并保存超过一次，则定位模式下不显示定位对话框。NPR-19144：适用于 CQ-4216708 的修补程序
* 在经典 UI 上的 Adobe Digital Publishing Solution 中，文章的访问属性设置不正确。NPR-19367
* 如果用户可以访问多个区域，通过 Campaign 个性化选件时，会出现自动折叠的错误行为。NPR-19290：适用于 CQ-4218029 的修补程序

### 站点 {#sites-11}

* 将实例升级到AEM 6.1SP2-CFP3后，由于Sidekick.js中的代码更改，多复合字段下拉列表值未重新填充。 NPR-19450：适用于CQ-4194771的HF
* 在创作模式下，WCMMode.EDIT不适用于目标组件。 NPR-19387
* 发布了JSON API以使用内容片段。 NPR-19500
* 粗体、斜体、下划线功能不适用于创作对话框中的富文本编辑器字段。 NPR-19670、NPR-19718：适用于 CQ-4219088 的修补程序

### Mobile On-Demand {#mobile-on-demand-1}

* 由于使用全尺寸图像导致呈现过程缓慢，AEM 文章控制台出现呈现问题。NPR-19088

### 翻译 {#translation-5}

* 无法为翻译项目生成预览。 NPR-19289

### 安全 {#security}

* SSL 连接错误。无法与服务器建立安全连接。NPR-19628

### 社区 {#communities-9}

* 通过预审核的网站发布内容时会触发邮件。 NPR-20008
* 电子邮件通知不适用于已发布组件上与版主相关的任何活动。 NPR-19767：适用于CQ-4218060的HF

### 平台 {#platform-4}

* AEM 生产服务器部署存在稳定性问题。NPR-19707
* 升级到 AEM 6.3 后，未找到引用作为脚本实施的标记的自定义 taglib。NPR-19087
* AEM 6.3.1 的 HTL 错误修复。NPR-19161
* 富文本字段在多字段组件中不可编辑。NPR-19604：适用于 Granite-16755 的修补程序
* Adobe 电子邮件模板服务会将标记添加到自定义用户模板。NPR-19190
* 适用于 Oak 1.6.5 的修补程序。NPR-19148

### 商务 {#commerce-5}

* 选择XF变体编辑器后“启动工作流”按钮不起作用。 NPR-19642：适用于 CQ-4207796 的修补程序

### 项目 {#projects-2}

* 项目编辑者无法将资产复制/粘贴到项目资产文件夹中。NPR-19619: 适用于 CQ-4215321 的修补程序

### 网站内容管理 {#web-content-management}

* 在转出屏幕中，无法选中或取消选中与LiveCopy页面对应的复选框。 NPR-19518
* 批量编辑页面属性无法正确使用，因为当前所有选项卡和字段均可用于批量编辑。 NPR-19451
* 在经典UI中编辑图像时，OOTB属性和图像对齐方式属性不显示。 NPR-19488：适用于CQ-4217914的HF

### 用户界面 {#user-interface-4}

* 使用Google Chrome浏览器时，用户无法在触屏UI中使用列视图加载页面/资产的完整列表。 NPR-19566：适用于 CQ-4214248 的修补程序

### Brand Portal {#brand-portal-1}

* 无法从AEM发布包含注释和批注的资源。 NPR-19590：适用于 CQ-4218386 的修补程序
* 启用通过 tagadmin/tagging 控制台将标记从 AEM 发布到 Brand Portal 的功能。NPR-20271：适用于 CQ-4223948 的修补程序
* 修复Brand Portal cloudservice配置UI上的“已启用”字段。 适用于 CQ-4211101 的修补程序
* 搜索表单复制失败。 适用于 CQ-4220080 的修补程序

## 表单 {#forms-11}

通过发行版附带的附加组件包和其他补丁安装程序提供 AEM Forms 修补程序。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-11}

#### 自适应表单 {#adaptive-forms-4}

* 提交到JEE工作流未从JEE端将输出参数返回到AEM，并引发“由于值不是原始值而忽略”错误。 NPR-20265
* 自适应Forms不允许在Safari中将PDF作为附件。 NPR-19625
* RestoreGuideState覆盖customcontextproperty映射。 CQ-4222877
* 使用Cloud Service配置Google reCaptcha时，在需要配置org.apache.http.proxyconfigurator以进行外部连接的环境中，POST调用似乎不会通过PROXY。 NPR-20454
* 安装时基于XSD架构的自适应Forms会为数字字段提交有问题的XML值，其区域设置使用“”以外的小数分隔符。 从而导致出现错误。NPR-20444
* 向第三方服务器发出 HTTP 请求时，不接受为“Apache HTTP 组件代理配置”设置的代理设置。使用 HTTP GET 或 POST 调用时出现连接超时问题。NPR-20457、NPR-20456、NPR-20455、NPR-20451

#### 表单数据集成 {#forms-data-integration}

* 对于非英语语言环境，作为SOAP服务输出的UTF-8字符无法正确复制到自适应Forms字段中。 NPR-20238：NPR-20103

#### 通信管理 {#correspondence-management-1}

* 在文本编辑器中，从Word文件复制粘贴内容会丢失其内容颜色和字体。 NPR-19521

#### 汇编程序服务 {#assembler-services}

* 在对PDFA-1b格式的文档进行合规性验证期间，Acrobat和AEM的结果存在差异。 NPR-19280

#### 工作流 {#workflow-2}

* 允许http调用通过代理进行连接的工作流签名步骤。 NPR-20529

#### HTML5 表单 {#html-forms-4}

* 添加了对preSubmit事件的支持。 NPR-20604

### Forms JEE 安装程序 {#forms-jee-installer-10}

#### 进程管理 {#process-management-3}

* 将表单最大化/最小化并将其另存为草稿或转发后，工作流“附件”、“注释”和“详细信息”选项卡在工作区中无法使用。NPR-20243
* 在HTML工作区中提交数据后，多行文本字段(TextArea)未保留文本中的新行字符或换行符。 NPR-20085

#### 进程报告 {#process-reporting}

* 由于空指针异常，进程报表无法正确获取数据。 NPR-19759

>[!NOTE]
>
>安装中列出的LiveCycle嵌入包 [AEM Forms版本](aem-forms-releases.md) 文章来解决此问题。

#### 标准服务 {#standard-services}

* docConvertor 不支持 PDF 中的拼合透明度，且无法生成 PDF/A。NPR-16228：适用于 CQ-4214488 的修补程序

#### 核心 {#core-2}

* 当AEM Forms服务器在JBoss应用程序的群集配置中运行时，该应用程序服务器与数据库断开连接。 这可能会导致数据损坏问题。 NPR-19724

### 包含的功能包 {#feature-packs-included-1}

* 由于资产缺少必填字段验证，因此无法将下拉元数据架构字段设为必填字段。 NPR-17882：适用于CQ-4208373的FP

### 6.3.1.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-7}

AEM CFP 6.3.1.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list.txt)

AEM CFP 6.3.1.1 中包含的内容包列表

[获取文件](assets/do-not-localize/content-package-list.txt)

AEM 累积修补程序包 6.3.0.2 是一个重要更新，它包括自 2017 年 4 月 AEM 6.3 正式发布以来的若干内部修补程序和客户修补程序。

AEM 累积修补程序包的主要功能亮点包括：

* 用户访问控制的可审计性
* 包含内置存储库的1.6.2版本(Apache Jackrabbit Oak)
* 解决了无结尾标记的资源解析程序问题
* 简化了智能内容服务的配置
* 解决了内容片段验证问题
* 改进了混合设备上元数据架构的可编辑性
* 解决了活动副本中的组件级同步问题
* 提高了列视图中内容密集型页面的可用性
* 改进了长标题页面对页面命名约定的合规性
* 改进了触屏UI上的Campaign个性化体验
* 修复了各种项目叠加问题

### 平台 {#platform-5}

* 适用于 Oak 1.6.2 的修补程序。NPR-16993
* 使用过滤器打开Omnisearch时，不再设置路径。 NPR-17398：适用于 CQ-4204870 的修补程序
* 要求AEM中用户权限更改的可审核性。 NPR-17061
* 延迟连接到DMCloud Services会导致“打开的文件过多”异常。 CQ-4211407

### 资产 {#assets-12}

* 使用不同选项配置智能内容服务时出现可用性问题。 NPR-18200：适用于 CQ-4201557 的修补程序
* 二进制流中的资源泄漏到S3数据存储。 NPR-18041：适用于 CQ-4209506 的修补程序
* 将ASCII/UTF-8编码文本文件上传到AEM Assets时出现错误，并且缩略图生成失败。 NPR-18006：适用于 CQ-4209345 的 CFP
* 默认元数据架构导致内容片段验证失败。 NPR-17769：适用于 CQ-4211111 的修补程序
* com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner中的资源解析程序未关闭。 NPR-17598：适用于 CQ-4209018 的 CFP
* 请求创建多个复制代理以将资产发布到Brand Portal。 NPR-17189
* 日语文件夹下资产的审核任务不起作用。 CQ-4204782
* 从资产的属性页面移动资产时，会发生空指针异常。 CQ-4204251
* 如果资产已多次链接到InDesign文档，则AEM无法跟踪资产页面中对该资产的后续引用。 CQ-4204186
* 在混合设备上的Chrome中编辑元数据架构表单时，在该表单中添加新选项卡时出现问题。 CQ-4201810
* 上传重复资产时，（删除/保留）选项将应用于所有资产，即使未在检测到的重复资产对话框中选择该选项也是如此。 CQ-4201673
* 移动包含超过150个传入引用的资产文件夹时，会引发空指针异常。 CQ-4200981
* 对于下载的资源文件夹，如果在解压缩ZIP文件的内容时发生冲突，则默认选项将显示为“创建版本”而不是“保留两者”。 CQ-97800
* 对应用程序具有只读权限的用户无法从AEM Mobile内容管理预览内容。 NPR-17486：适用于 CQ-4209690 的 CFP
* “创建目录”按钮在“目录”控制台的列视图中不起作用。 CQ-4209952

### 站点 {#sites-12}

* 通过data-sly-resource属性嵌入图像/视频组件时出现问题。 NPR-18182：适用于 CQ-4212100 的 CFP
* 在 LiveCopy 中重新应用继承时，修改后的本地化组件无法恢复为原始形式。NPR-18172：适用于 CQ-4211379 的修补程序
* 在触屏UI的列视图中导航大量内容的页面时出现问题。 NPR-17799：适用于 CQ-4199611 的修补程序
* `com.day.cq.wcm.core.impl.VersionManagerImpl` 中的资源解析程序未关闭。NPR-17789：适用于 CQ-4211152 的 CFP
* 长页面标题没有按照约定生成页面名称。 NPR-17633：适用于 CQ-4209056 的修补程序
* 在部署在Jboss EAP 6.4上的AEM 6.3中，在触屏UI上创建页面时出现问题。NPR-17589：适用于CQ-4210137的修补程序
* 当存在嵌套组时，工作流状态提供程序会导致实例锁定。 NPR-17556：适用于CQ-4202056的CFP请求
* 以下对象中的资源解析程序未关闭：

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497：适用于 CQ-4208673 的 CFP
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495：适用于 CQ-4208668 的 CFP
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494：适用于 CQ-4208669 的 CFP
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493：适用于 GRANITE-17404 的 CFP

### 集成 {#integrations-1}

* 解决了在 AEM Day HTTP Client 3.1 OSGi 配置了需要摘要身份验证的代理时可能发生的 AEM 搜索组件错误。NPR-18128：适用于 NPR-18029 的修补程序
* 通过经典UI个性化营销活动和相关体验时出现问题。 NPR-18127：适用于 CQ-4211559 的修补程序
* 将品牌/区域设置为站点的根页面时，一旦取消继承，就无法恢复子页面中的区域。 NPR-17753：适用于 CQ-4210139 的修补程序

### 工作流 {#workflow-3}

* 在非临时工作流中，不会保留在外部流程步骤之前所做的流程历史记录和元数据更改。 NPR-17848：适用于 GRANITE-17757 的修补程序
* 工作流对话框字段中的值未保留在工作项节点中。 NPR-17734：适用于 CQ-4210369 的修补程序
* 从收件箱编辑任务时出现无法分析的日期错误。 CQ-4208749

### 项目 {#projects-3}

* 修复了各种项目叠加问题。 NPR-17733
* 重新构建项目模块中的pod会降低其可配置性。 CQ-4209859
* 将页面添加到翻译作业后，资产路径将更改为各自的本地化站点。 CQ-4206007

### 安全 {#security-1}

* 上传 LDAP 用户的头像图像时出现问题。NPR-16561
* 请求使用 Apache Sling API 中的升级版 org.apache.sling.servlets.post servlet (2.3.22) 来预先制止 XSS 漏洞。NPR-18963

## 表单 {#forms-12}

AEM Forms 修补程序通过随发行版一起提供的 Forms 附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

AEM Forms的主要功能亮点包括：

* 修复了通信管理文本模块、信件预览和以编程方式启动创建通信管理UI的问题。
* 修复了 PDF/A-1b 验证、将大型图像文件转换为 PDF，以及 PDF 生成器中的日语 PDF 文档的问题。
* 修复了通信管理、文档安全和论坛工作流的可用性问题。
* 添加了对捕获潦草签名字段的审核事件的支持。

### Forms 附加组件包 {#forms-add-on-package-12}

**通信管理**

* 在编辑通信管理片段时，文本编辑器显示内嵌条件以及已处理的文本。CQ-4211930
* 创建通信管理信件时，信件的描述未保存。 NPR-18089
* 项目符号列表上下方的附加边距在文本编辑器中可见，但在HTML和PDF呈现中不可见。 NPR-18126
* 当HTML提交使用POST方法时，创建通信UI无法启动。 NPR-18202
* 当文本模块被保存并且文本模块中的表达式不包含开头或结尾表达式标记时，不显示错误消息。 文本模块显示一条错误消息，无法在信件中呈现。 NPR-18535
* 添加新内容或按Enter键时，会向文本模块添加div标记。 NPR-18240

**汇编程序**

* 在验证PDF文档是否符合PDF/A-1b规范时，AEM Forms返回验证错误：PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED。 通过Adobe预检和第三方软件验证时，PDF文档未返回错误。 NPR-18011
* 验证PDF文档是否符合PDF/A-1b合规性时，AEM Forms返回验证错误：表单字段有多个外观。 PDF文档符合PDF/A-1b标准。 NPR-18013

**监视文件夹**

* 选择使用工作流处理文件时，在创建监视文件夹时，工作流模型选择下拉列表显示被截断。 NPR-17566

**HTML5 表单**

* AEM Forms不会捕获涂写签名字段的审核事件。 NPR-15286

**Forms Manger**

* AEM Forms UI按最早的顺序列出所有资源。 用户无法按最新的顺序对资产重新排序。 NPR-18450

**Java API参考**

为 com.adobe.livecycle.content 类添加了 JavaDocs。NPR-18468

### Forms JEE 安装程序 {#forms-jee-installer-11}

**PDF生成器**

* PDF生成器服务无法将大于100 MB的图像转换为PDF文档。 Ref# CQ-4208628
* 在将PDF生成器服务与日语OCR结合使用时，生成反向PDF。 NPR-17602

**进程管理**

* 没有为AEM Forms进程填充TaskContext变量。 NPR-18199

**文档安全**

* Microsoft Excel和Microsoft PowerPoint需要更长的时间来打开受AEM Document Security Extension for Microsoft Office保护的文档。 CQ-4212358
* 创建新策略且策略名称与现有策略名称相同时，发生内部服务器错误。 NPR-18247

## 包含的功能包 {#feature-packs-included-2}

* 要求AEM中用户权限更改的可审核性。 NPR-17061

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
* 不支持卸载CFP。

### 添加新的记录器 {#adding-new-loggers}

要配置调试级别日志记录并在 SP/CFP 安装期间检索活动日志，您可以按照以下步骤操作：

* 您可以在默认位置 [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) 添加新的日志记录器，该日志记录器具有以下属性：

   * 日志级别：调试
   * 加总：false
   * 日志文件：logs/activity.log
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
>如果您没有使用AEM Forms，请跳过此部分。

#### 安装AEM Forms加载项 {#install-forms}

1. 确保您已安装 AEM 6.3.3.x CFP 包。
1. 下载适用于您的操作系统的 [AEM Forms 发行版](aem-forms-releases.md)中列出的相应 Forms 附加组件包。
1. 按照[安装 AEM Forms 附加组件包](https://helpx.adobe.com/cn/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html)中的所述安装 Forms 附加组件包。

#### 安装 AEM Forms JEE 包 {#install-aem-forms-jee-bundles-package}

AEM Forms JEE中的修补程序通过单独的安装程序提供。 有关在JEE上的AEM Forms上安装CFP的信息，请参阅 [在AEM Forms JEE上安装CFP](install-cfp-aem-forms-jee.md).

#### Forms Designer安装程序 {#designer-installer}

1. 要安装更新，请运行 Designer 6.2.0_&lt;语言>_Cumulative_QF.msp 文件。
1. 在欢迎屏幕上，单击 **更新**. 安装随即开始。
1. 安装完成后，单击 **结束**.

## AEM Forms JEE (JBoss EAP)的配置设置 {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>如果要安装6.3.3.0或更高版本，请执行以下过程来配置JBoss应用程序服务器的设置。 如果要在运行于OracleWebLogic或AEM Forms WebSpehere应用程序服务器上的IBM服务器上安装6.3.3.0，则无需进行其他配置。 有关更多详细信息，请参阅 [AEM 6.3.3.0 发行说明](https://helpx.adobe.com/cn/experience-manager/6-3/release-notes/sp3-release-notes.html)。

## Search&amp;Promote 集成的配置更新 {#configuration-updates-for-search-promote-integration}

如果安装的是 AEM 累积修补程序包 6.3.0.2 及更高版本，则用于 Search&amp;Promote 集成的 OSGi 配置是 **Apache HTTP 组件代理配置**。不再使用 Day Commons HTTP Client 3.1 中的代理配置。

## 已知问题 {#known-issues}

* 在 AEM CFP 6.3.3.x 的安装过程中可能会出现以下错误和警告，这些错误和警告可以安全忽略：

   * &#42;警告&#42; [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependencies.jar引发运行时异常。
   * &#42;错误&#42; [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] 等待注册更改完成取消注册时超时。 CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl ServletResolver 服务缺失，无法发送服务请求，发送状态 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource：无法检查资源 [/bin/receive]，页面管理器不可用
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver：调用错误处理程序导致出现错误
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver原始错误null
   * org.apache.sling.engine.impl.DefaultErrorHandler错误处理程序失败：java.io.IOException
   * &#42;错误&#42; [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent错误(org.osgi.framework.ServiceException：服务工厂返回null。 （组件：com.day.cq.dam.handler.standard.ps.PostScriptHandler）)

**Brand Portal**

* 从6.3.1.2开始，已删除智能收藏集的“发布到Brand Portal”按钮。

**用户界面**

>[!NOTE]
>
>如果您受到这两个问题中的任何一个的影响，请联系 [AEM客户关怀](https://helpx.adobe.com/cn/marketing-cloud/contact-support.html).

* 由于管理员搜索功能中存在大量请求，观察到 CPU 使用率很高。NPR-24229
* 重新打开组件时，在pathBrowser中未选择PathField。 NPR-24177

## NPR-27692 所需的配置设置 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>此配置设置适用于 CFP 6.3.3.2 及更高版本。它将指导您更新 `sling` .properties 文件中的启动委托属性。

要手动更新 adobe- livecycle - cq -author.ear/ cq .war 中的更改，请按以下所述步骤操作：

* 停止AEM服务器。
* 转到adobe-livecycle-cq-author.ear/cq.war
* 打开adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml进行编辑：

   * 将 **sling.bootdelegation.ibm** 参数名称值更新为：

      * com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat
   * 进行上述更改后，init-param应如下所示：

      * &lt;init-param>\
         &lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>\
         &lt;/init-param>


* 从 Websphere 应用程序服务器中卸载之前的企业存档 (EAR) 文件，并按照 [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf) 的第 10.2 节中的步骤来安装更新后的 EAR 文件
* 保存文件并重新启动服务器。[https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## NPR-23208 所需的配置设置 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>此配置设置适用于 6.3.2.2 及更高版本。它会指导您通过 CRX-DE 手动更新访问控制列表 (ACL) 策略，因为 ACL 由于“merge_preserve”acHandling 无法通过 CFP 安装进行更新。

**有关手动添加ACL策略的文档**

要更新ACL策略，请通过CRX-DE添加以下访问控制：

`1)` 路径：“/content”\
`a)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
限制：rep：glob=&quot;/&#42;/jcr：content&quot;\
`b)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
限制：rep：glob=&quot;/&#42;/jcr：content/&#42;”

`2)` 路径：“/content/usergenerated”\
`a)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:write

`3)` 路径：“/etc”\
`a)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
限制：rep：glob=&quot;/&#42;/jcr：content&quot;\
`b)` 主体：reference-adjustment-service\
类型：允许\
权限：jcr:read、jcr:modifyProperties\
限制：rep：glob=&quot;/&#42;/jcr：content/&#42;”

## NPR-19450 所需的配置设置 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>此配置设置适用于 CFP 6.3.1.1 及更高版本。

**配置属性 CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL。**

该属性可控制页面 ` /  jcr   :content` 节点下节点子树的最大深度，在达到该深度之前，存储库中存在的节点将用于获取页面属性。此属性中位于指定深度以下的任何节点都将被忽略。

默认值为 1。可以通过覆盖文件constants.js (`/libs/cq/ui/widgets/source/constants.js`)取消对CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL属性的注释，并为其指定所需的值（页面的/jcr ：content下的最大深度，在达到该深度之前，将存储页面属性的数据）。

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
| Assets与Adobe Creative Cloud集成 | AEM 6.2 中引入了 [AEM 到 Creative Cloud 的文件夹共享](https://helpx.adobe.com/cn/experience-manager/6-3/sites/administering/using/creative-cloud.html)功能，以便创意用户可以从 AEM 访问资产。Creative Cloud应用程序中发布的一项新功能AdobeAsset Link提供了更好的用户体验，以及更强大的直接从Photoshop、InDesign和Illustrator中访问AEM资源的功能。<br /> Adobe将不再对文件夹共享功能做进一步增强。 虽然此功能包含在AEM中，但强烈建议使用替代功能。 | AdobeAsset Link或桌面应用程序。 有关更多信息，请参阅 [AEMCreative Cloud集成](https://helpx.adobe.com/cn/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html) 文章。 | AEM 6.3.3.x |

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

