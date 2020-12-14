---
title: AEM 6.2 累积修复程序包
description: 'null'
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '19954'
ht-degree: 20%

---


# AEM 6.2 Cumulative Fix Pack发行说明{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## 发行信息 {#release-information}

| **产品** | Adobe Experience Manager |
|---|---|
| **版本** | 6.2 |
| **发行版** | [累积修补程序包6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **先决条件** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **正式发布** | 2019年6月06日 |

### 累积修补程序包 {#cumulative-fix-pack}

Adobe 引入了统一交付模式，用于发布修补程序。Adobe现在每个月都会发布累积修复包(CFP)，而不是针对个别问题发布热修复（需通过质量检查）。 CFP 是指多个修补程序的汇总内容包。CFP 主要包括错误修复，但也可能包括功能包。与单个修补程序发行版相比，CFP 具有以下优点：

* 本质上是累积的（例如，CFP 包含以前 CFP 已交付的修补程序）
* 提高了质量保证
* 简化了安装（用户将 CFP 安装为一个不含任何依赖关系的包，最新的服务包除外）

有关CFP和其他类型版本的详细信息，请参见[维护版本车辆](https://docs.adobe.com/content/docs/en/aem/6-2/deploy/maintenance-release-vehicle-definitions.html)。

## 关于此发行版 {#about-the-release}

AEM Cumulative Fix Pack 6.2 SP1-CFP20是AEM 6.2的最后一个累积修补程序包，是一个重要更新，其中包括自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)正式推出以来发布的主要客户修复。

>[!CAUTION]
>
>在没有验证已安装功能包之间的兼容性的情况下应用 CFP，可能会导致系统故障或自定义配置丢失，这些问题可能需要从备份还原才能解决。

>[!NOTE]
>
>* AEM Cumulative Fix Pack 6.2 SP1-CFP10中包含新的Sling `discovery-  api`捆绑Johnzon 1.0.0。 此外，还为CRX存储库中的节点&#x200B;*/var/discovery*&#x200B;添加了服务用户sling-discovery的读和写权限。
   >
   >
* 已添加apache commons **org.apache.commons/commons-email/1.5**&#x200B;的电子邮件捆绑，替换&#x200B;**com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**。
   >
   >
* Adobe建议通过安装文件夹为AEM实例上拥有大量用户的客户部署CFP。

>



## 问题包括{#issues-included}

此部分列出了当前 CFP 中包含的所有问题和修补程序。

此外，此CFP还包含在[以前累积修复包](#previous)中提供的修补程序。

### 集成 {#integration}

* 支持多个活动定位个性化改进。 NPR-29163：适用于 CQ-4264126 的修补程序
* com.day.cq.personalization.impl.TeaserResourceEventHandler 陷入无限循环，并导致对发布实例上的节点进行更新。NPR-28561：适用于 CQ-4263096 的修补程序

### DAM - 常规 {#dam-general}

* 无法显示／隐藏特定dam文件夹中非管理员用户的复制按钮。 NPR-29026：适用于 CQ-4265361 的修补程序

### 漏洞 {#vulnerability}

* CSRF 保护框架不适用于 AEM Foundation 表单。NPR-28612：适用于 GRANITE-22231 的修补程序

### 表单 {#forms}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package}

>[!NOTE]
>
>对于 AEM Forms 客户，请先安装任意 AEM Service Pack、累计修复程序或功能包之后，再安装 AEM Forms 附加组件包，这一点至关重要。

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM Service Pack 和累积修补程序包保持一致。因此，在安装任何AEM Service Pack、Cumulative Fix Pack或Feature Pack后，必须安装AEM forms add-on包。

#### 自适应表单 {#adaptive-forms}

* iOS 12.1设备的涂写组件的可用性问题。 NPR-29082：适用于 CQ-4261765 的修补程序

#### 表单 - 文档安全 {#forms-document-security}

* 使用PDF高级电子签名(PAdES)验证PDF中的所有签名会引发InvalidOperationException。 NPR-27848：适用于 CQ-4244837 的修补程序

#### Forms-通信{#forms-correspondence}

* 在将字母预览为PDF时，位于主控页面的文本字段不遵循从数据选项卡或根据指定的数据链接输入的值。 NPR-29239：适用于 CQ-4266856 的修补程序.

#### 表单 - 交互式通信 {#forms-interactive-communication}

* 添加撇号字符时，字母中预填字段显示为ASCII字符，而不是常规字母。 NPR-28863：适用于 CQ-4262900 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

## 以前的累积修补程序包中包含的修补程序和功能包 {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### 累积修补程序包 19 {#cumulative-fix-pack-1}

AEM Cumulative Fix Pack 6.2 SP1-CFP19是重要更新，包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)通用发布以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 支持对AEM 6.2的MS Translator API v3.0支持
* 成功安装所有SP、CFP和HF的软件包后添加的日志消息。

### 资产 {#assets}

* 如果缺少“编辑ACL”权限，则无法重命名DAM文件夹。 NPR-27555：适用于 CQ-104652 的修补程序
* 在6.2.1 CFP 17及更高版本中，图像预设编辑器工具不响应。 NPR-28147：适用于 CQ-4261041 的修补程序

### 站点 {#sites}

* 链接检查器无法完成作业，因为无响应链接而卡住。 NPR-27373：适用于 CQ-4256030 的修补程序
* 段文件无法正确加载，原因是额外的根路径中断了段的路径。 NPR-28014：适用于 CQ-4260332 的修补程序

### 集成 {#integration-1}

* LiveCopy继承取消在目标容器上无法正常工作。 NPR-28129：适用于 CQ-4259813 的修补程序
* 不考虑目标组件的cq ：操作。 NPR-27616：适用于 CQ-4257497 的修补程序

* 中断继承的图标显示不一致。 NPR-27671：适用于 CQ-4257779 的修补程序

### Felix {#felix}

* 在AEM 6.2 SP1实例上安装CFP 18后，Web控制台组件详细信息在500后失败。 NPR-28350：适用于 CQ-4261095 的修补程序

### 翻译 {#translation}

* 在将MS Translator升级到API v3.0后，在AEM 6.3中支持MS Translator服务。NPR-28123:CQ-4259096的修补程序

### UI - Foundation {#ui-foundation}

* OOTB站点日历显示不正确的日期。 NPR-28392

### Granite {#granite}

* 对于使用sling :basename的资源包，字典不无效。 NPR-27624

### 留存 {#sustenance}

* 应将包管理器活动日志提取到单独的日志文件中。NPR-27323：适用于 Granite-14866 的修补程序
* 在安装完成时将显示error.log中的标准化短语／措辞/log-line。 NPR-27835
* Granite包插件是org.apache.sling.i18n较低版本的依赖项。 适用于 CQ-4263245 的修补程序
* 在安装6.2SP1-CFP15之后的最新CFP时，将删除com.adobe.cq.com.adobe.cq.ui.commons捆绑包。 适用于 CQ-4258808 的修补程序

### 表单 {#forms-1}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-1}

#### 自适应表单 {#adaptive-forms-1}

* AEM Forms 存在 XML 注入漏洞。NPR-27843：适用于 CQ-4257315 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-1}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

### 包含{#osgi-bundles-and-content-packages-included}的OSGI包和内容包

以下文本文档OSGI包的列表以及CFP中包含的内容包。

AEM 6.2 SP1-CFP19中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/cfp19_osgi_bundles.txt)

AEM 6.2SP1-CFP19中包含的内容包列表

[获取文件](assets/do-not-localize/cfp19_content_packages.txt)

### 累积修补程序包 18 {#cumulative-fix-pack-2}

AEM Cumulative Fix Pack 6.2 SP1-CFP18是重要更新，包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)通用发布以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 在DAM CommandLineProcess中增加了对终止长期运行进程的支持。
* 修复了ReplicationEventListener中的会话泄漏。
* 为核心页面组件添加了重定向支持。

### 资产 {#assets-1}

* Camera Raw流程在大量摄取期间卡住，最终阻止所有工作流程处理。 NPR-26990：适用于 NPR-23860 的修补程序
* 下载功能通过资产下载servlet利用AEM Assets，允许匿名用户下载所有资产。 NPR-27054,CQ-4254732的修补程序
* 特殊字符在AEM的电子邮件模板的主题行中显示为断开。 NPR-26470：适用于 CQ-4252368 的修补程序

### 站点 {#sites-1}

* 由于ConfigPostProcessor类的行为不正确，挂起父映像将删除cq :来自子页面的LiveRelationship混合类型。 NPR-26745：适用于 CQ-4254163 的修补程序
* 向核心页面组件添加重定向支持。 NPR-26576：适用于 CQ-110529 的修补程序
* 将Context Hub迁移到jquery 3。 NPR-26956：适用于 CQ-4255472 的修补程序
* 锚点输入字段显示在对话框的浏览器可见部分之外，直到最大化。 NPR-26852：适用于 CQ-4255019 的修补程序
* 复制粘贴在内容片段中插入不需要的&lt;br>的文本。 NPR-26660：适用于 CRTE-151 的修补程序
* 经典siteadmin不会在某些页面的右侧窗格中呈现列表。 NPR-27247：适用于 CQ-4251621 的修补程序
* （经典UI）尝试移动／重命名页面时会生成错误“移动页面时出错。” NPR-27179：适用于 CQ-4235907 的修补程序

### 集成 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever 遍历整个树来收集可用品牌。NPR-27060：适用于 CQ-4255790 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components}

* Foundation列表组件的搜索功能问题。 NPR-26817：适用于 CQ-4250324 的修补程序

### 平台 {#platform}

* 由于特殊字符em dash，发布者刷新缓存时出现问题。 NPR-27199：适用于 CQ-4242790 的修补程序

### 花岗岩{#granite-1}

* 包验证程序无法验证 CFP/SP 中含有的包。NPR-26775：适用于 Granite-22825 的修补程序

### 复制 {#replication}

* ReplicationListener中的JCR会话泄漏。 NPR-27063：适用于 CQ-4232088 的修补程序

### 表单 {#forms-2}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-2}

* Forms 附加组件包中没有新的 AEM Forms 修补程序。

### Forms JEE 安装程序 {#forms-jee-installer-2}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

#### 包含{#osgi-bundles-and-content-packages-included-1}的OSGI包和内容包

AEM 6.2 SP1-CFP18中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/62cfp18updated_bundles.txt)

AEM 6.2 SP1-CFP18中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### 累积修补程序包 17 {#cumulative-fix-pack-3}

AEM Cumulative Fix Pack 6.2 SP1-CFP17是重要更新，包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)通用发布以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 为at-integration.js中的无扩展站点URL添加了支持
* 从S7云服务配置中删除了S7轮询导入程序。
* 对受众视图的更改，以支持多租户实现的文件夹结构。
* 更新至jquerui   clientlib v1.12.1。

### 资产 {#assets-2}

* 从资产UI启动工作流时，用户必须具有写入／删除／修改权限。 NPR-25688：适用于 CQ-4250140 的修补程序
* 即使没有“复制”权限的用户，发布和取消发布按钮也仍然可见。 NPR-25094
* （工作流）智能标记资产工作流不会通过AEM代理配置进行处理。 NPR-25915：适用于 CQ-4248202 的修补程序
* 从S7云服务配置中删除S7轮询导入程序。 NPR-25239：适用于 CQ-95236 的修补程序

### 站点 {#sites-2}

* 工作流从“编辑器”->“页面信息”启动，并在有效负荷中包含上下文路径。 NPR-26389：适用于 CQ-76804 的修补程序
* （外部链接检查器）无效的https链接显示为有效链接。 NPR-25541：适用于 CQ-4201333 的修补程序
* （经典UI）在Live Copy下创建独立页面时，该页面将创建为Live Copy。 NPR-25610：适用于 CQ-4249801 的修补程序
* 激活页面时与设计导入程序组件关联的发布资源问题。 NPR-25638：适用于 CQ-102532 的修补程序
* RTE富文本工具栏涵盖选择列表。 NPR-25165：适用于 CQ-4248948 的修补程序
* 将contexthub迁移到jquery 3。 NPR-25059：适用于 Granite-19902 的修补程序
* 对于嵌套的parsys组件，始终从多个可用组件中应用满足设计的第一个（具有最少的嵌套路径）。 有关详细信息，请参阅[设计路径分辨率](https://helpx.adobe.com/experience-manager/6-3/sites/developing/using/page-templates-static.html)。 NPR-25250：适用于 CQ-4246276 的修补程序

### 集成 {#integration-3}

* 使用OOTB目标集成，定位组件可呈现整个页面而不是空的目标组件。 NPR-25273：适用于 CQ-4248003 的修补程序
* 在“定位”模式中中断继承仍会显示组件为目标，而在“编辑”模式中继承未中断。 NPR-25324：适用于 CQ-4248162 的修补程序
* 在页面上定义个性化并解析受众时，相应的体验会在编辑模式下显示。 NPR-25731：适用于 CQ-4249465 的修补程序
* 将AEM与非默认上下文路径一起使用时，Teaser URL出错。 NPR-25971：适用于 CQ-4250953 的修补程序
* 使用打开项时显示空白。 NPR-25295：适用于 CQ-4246792 的修补程序
* 从创作环境删除的体验在页面激活时从不从发布站点中删除。 NPR-24869：适用于 CQ-4247832 的修补程序

### DAM - DM 客户端 {#dam-dm-client}

* (Chrome、Firefox)VideoPlayer在支持触控的设备上忽略鼠标单击。 适用于 CQ-4247370 的修补程序

### 平台 {#platform-1}

* 允许在获取／释放包时配置最大重试数。 NPR-25328：适用于 Granite-22376 的修补程序
* 复制错误时记录不正确。 NPR-25308：适用于 CQ-4249402 的修补程序
* 将FormsAEM 6.2FormsCFP8安装到CFP14会导致Apache POI失败。 NPR-25053：适用于 Granite-21771 的修补程序

### 花岗岩{#granite-2}

* OakConstraint0022异常导致用户同步进程失败。 NPR-25729:Oak-7428的修补程序

### 社区 {#communities}

* cq -social-as-provider捆绑与mongo驱动程序3.x版本不开始。 NPR-26271：适用于 CQ-4252710 的修补程序

### UI - Foundation {#ui-foundation-1}

* 更新至jquerui   clientlib v1.12.1. NPR-25090:Granite-21981、CQ-4248897的修补程序

* （全搜索）:“标题”属性易受站点中跨站点(XSS)脚本的攻击。 NPR-24994：适用于 Granite-19933 的修补程序

### 表单 {#forms-3}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-3}

#### 自适应表单 {#adaptive-forms-2}

* 从自适应表单提交数据时编码错误。 NPR-25539

#### Forms - 管理 {#forms-management}

* 发布页面时报告为引用的不相关表单资产。 NPR-26167：适用于 CQ-4251004 的修补程序

### 表单 - JEE 安装程序 {#forms-jee-installer-3}

#### 文档安全 {#document-security}

* 变量填充为列表类型，子类型为字符串，但出现“无法强制对象”错误。 NPR-26194：适用于 CQ-4252287 的修补程序
* 安装6.2-SP1-CFP15后无法访问水印配置。 NPR-26130：适用于 CQ-4250984 的修补程序

### 包含{#osgi-bundles-and-content-packages-included-2}的OSGI包和内容包

AEM 6.2 SP1-CFP17中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/62cfp17updated_bundles.txt)

AEM 6.2SP1-CFP17中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### 累积修补程序包 16 {#cumulative-fix-pack-4}

AEM Cumulative Fix Pack 6.2 SP1-CFP16是重要更新，包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)通用发布以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。
* 修复了用户档案弹出窗口中ContextHub图标对齐的问题。
* 修复了下拉组件的显示/隐藏功能。
* 升级到最新的Jackson版本2.8.11

### 资产 {#assets-3}

* 无法从列表视图启动工作流。 NPR-24393：适用于 CQ-4245788 的修补程序
* (Firefox/Chrome)无法在“资源共享”页面下载资源。 NPR-24523：适用于 CQ-4224408 的修补程序
* 提高了AEM中视频预览的默认质量。 NPR-24148：适用于 CQ-4244310 的修补程序

### 集成 {#integration-4}

* 当组件针对发布实例时，闪烁会在目标实例之前显示默认体验。 NPR-23992：适用于 CQ-4242038 的修补程序
* 从创作环境删除的体验在页面激活时从不从发布站点中删除。 NPR-24869：适用于 CQ-4247832 的修补程序

### 平台 {#platform-2}

* 修补 clientlib 中的 jQuery 1.12.4 以包含安全修补程序。NPR-24129：适用于 Granite-20058 的修补程序
* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。NPR-23941：适用于 CQ-4240397 的修补程序
* 删除默认的MERGE_PRESERVE aclHandling。 NPR-24593：适用于 Granite-21889 的修补程序
* 当请求包含无效查询参数时，LineChecker无法将链接外部化。 NPR-24127：适用于 CQ-4241893 的修补程序

### MSM {#msm}

* 跨站点脚本攻击(XSS)的主动修补程序。 NPR-21893：适用于 CQ-4223385 的修补程序
* MSM LiveRelationship:如果BlueprintConfig位于根目录上，则有效转出配置错误。 NPR-23999：适用于 CQ-4243000 的修补程序

### 站点 {#sites-3}

* 在Live Copy区域创建新体验时，需要配置中断继承。 NPR-24995,CQ-4248209的修补程序
* （触屏UI）在锁定或解锁页面时，顶部工具栏上的多个图标会消失。 NPR-23954：适用于 CQ-4243345 的修补程序
* 上下文中的字段未正确对齐。 NPR-23958
* 在锁定的分页符创作时发布操作。 NPR-23970：适用于 CQ-4243203 的修补程序
* /etc/reports/中的OOTB报告无法正常工作，并且不显示历史数据图。 NPR-20035：适用于 CQ-4220180 的修补程序
* 在项目上启动“请求启动”工作流时，启动项创建失败。 NPR-24255：适用于 CQ-4245030 的修补程序
* CFP10安装后，电子邮件忽略的HTML标签和属性。 NPR-24287：适用于 CQ-4240028 的修补程序
* TagPicker:标记元模式标记字段中的标记建议会查询可标记的节点，因此，加载需要很长时间。 NPR-24347：适用于 CQ-4244291 的修补程序
* 代理配置无法与Salesforce集成。 NPR-24418：适用于 CQ-4245300 的修补程序
* (WCM)在创建修订期间，PageManager在异常时将页面检入。 NPR-24565：适用于 CQ-4246203 的修补程序
* 应用CFP14后，“设备模拟器”按钮将从编辑和预览模式中消失。 NPR-24566：适用于 CQ-4247060 的修补程序
* （经典UI）在对话框中创作后，整个标记显示为空。 NPR-24688,CQ-4246407的修补程序
* 首次尝试时无法创建版本。 NPR-24774：适用于 CQ-4232176 的修补程序
* /etc/reports/中的OOTB报告无法正常工作，并且不显示历史数据图。 NPR-24138：适用于 CQ-4220180 的修补程序

### 漏洞 {#vulnerability-1}

* Salesforce 集成容易遭受服务器端请求伪造 (SSRF) 攻击。NPR-24289：适用于 CQ-4245277 的修补程序
* ReportingServicesProxyServlet中的服务器端请求伪造(SSRF)漏洞。 NPR-24657：适用于 CQ-4246880 的修补程序

### 花岗岩{#granite-3}

* 元数据读取操作未结束。 NPR-24240：适用于 Granite-19866 的修补程序
* 将Jetty更新为9.4.11.v20180605以修复漏洞。 NPR-25033：适用于 Granite-22120 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-1}

* 在对页面进行排序时，PageComparator引发ClassCastException。 NPR-24123：适用于 CQ-4244048 的修补程序
* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-24562：适用于 CQ-4222853 的修补程序

### 用户界面 {#user-interface}

* 由于管理员搜索功能中存在大量请求，观察到 CPU 使用率很高。NPR-23588：适用于 Granite-21286 的修补程序
* （经典UI）组件显示默认值，即使关联的表单数据模型服务设置为空字段也是如此。 NPR-21903：适用于 GRANITE-19744 的修补程序
* 当没有请求的FormData时，多字段将引发NPE。 NPR-24513：适用于 Granite-21055 的修补程序

## 表单 {#forms-4}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-4}

#### 核心 {#core}

* (OSGI)AEM FormsOSGI受Jackson数据绑定安全警报影响。 NPR-24274：适用于 CQ-4230245 的修补程序

#### Rights Management{#rights-management}

* 安装AEM 6.2 SP1-CFP14后，Apache POI失败。 NPR-25054、NPR-25052：适用于 CQ-4245898、CQ-4244778 的修补程序

#### HTML5 表单 {#html-forms}

* 在HTML预览中，数据不会填充多行字段的预填。 NPR-23357：适用于 CQ-4244212 的修补程序
* 通过默认预览预览字母时，布局片段映射不会显示，而在单击预览按钮时，布局片段映射会正确显示。 NPR-22993：适用于 CQ-4237745 的修补程序
* 将社交保险号模式应用于模板时文本字段的HTML预览问题。 NPR-23205

#### 自适应表单 {#adaptive-forms-3}

* 将AEM表单添加到parsys组件时出现“Guidelib is not defined”错误。 NPR-24269：适用于 CQ-4244546 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-4}

#### Forms安装LCM {#forms-install-lcm}

* Shell脚本文件中的窗口行结尾导致LCM不在UNIX中运行。 NPR-22958

### 包含{#osgi-bundles-and-content-packages-included-3}的OSGI包和内容包

AEM 6.2 SP1-CFP16中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

AEM 6.2SP1-CFP16中包含的内容包列表

[获取文件](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### 累积修补程序包 15 {#cumulative-fix-pack-5}

AEM Cumulative Fix Pack 6.2 SP1-CFP15是重要更新，包含自[AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html)通用发布以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 基础表中的主动式安全修复可保持设计一致性。
* 增加了对typeHint的支持，可将值保存为字符串。
* 为Forms预填服务提供增强的安全性
* 更新至最新的adobe-reader-extensions-dsc.jar文件，以修复Reader扩展中的问题。
* 调整了验证挂接，以考虑用于提升编号输入的“:invalid”项。

### 资产 {#assets-4}

* 对于 Ptiff 生成流程，EmbedXMP 数据始终设置为“活动”。NPR-22776：适用于 CQ-4234498 的修补程序
* 无法在多值字段中设置多个默认值。 NPR-22900：适用于 CQ-4239000 的修补程序
* (Dynamic Media)选中“动态演绎版”复选框时，下载的zip文件会生成原始的TIFF图像（零字节文件）。 NPR-22410：适用于 CQ-4198471 的修补程序
* （触屏UI）列视图中资产的默认上传位置。 NPR-23475：适用于 CQ-4237057 的修补程序

### 集成 {#integration-5}

* 在目标模式下，作者可以修改从Blueprint继承的组件，而不取消继承。 NPR-22751：适用于 CQ-4237907 的修补程序
* 路径变量未正确编码，导致非持久性跨站点脚本(XSS)。 NPR-22851

### MSM {#msm-1}

* 在转出具有多个转出配置的LiveCopy时，如果ResourceNameConflict出现在根目录下，则转出流将终止，而不包括所有分支。 NPR-22842：适用于 CQ-4236188 的修补程序

### 平台 {#platform-3}

* 在一个请求中实现反向应用的轮询限制。 NPR-23351：适用于 Granite-21135 的修补程序****
* 消息模式更改不会反映在自定义记录器上。 NPR-23486：适用于 CQ-4241974 的修补程序

### 站点 {#sites-4}

* 在富文本编辑器的文本中创建指向文档的链接（带有空格或其他特殊字符）不起作用。 NPR-22289：适用于 CQ-4224321 的修补程序
* 保存具有大值(100000000000)的区段会将提升设置为0，从而导致错误消息。 NPR-22524：适用于 CQ-4237006 的修补程序
* 无法单击多字段组件中的添加项。 NPR-22552：适用于 CQ-4237404 的修补程序
* 当段标题较长时，水平滚动条不可见。 NPR-22615：适用于 CQ-4237001 的修补程序
* 加载空受众会生成错误的JavaScript代码。 NPR-22974：适用于 CQ-4238734 的修补程序
* 当计划激活或取消激活工作流标题时是强制性的，因此自定义工作流标题不会在时间轴中转换。 NPR-23121：适用于 CQ-4237552 的修补程序
* 请求修复站点中目标段相关的问题。 NPR-23128
* (Firefox)选定人物的复选框不正确。 NPR-23345
* 不同模式的标签会与图标一起显示。 NPR-23275
* 将组件从 AEM 6.0 迁移到 AEM 6.2 时出现“无效的递归选择器值”错误。NPR-23503：适用于 CQ-4241258 的修补程序

### 社区 {#communities-1}

* 由于向组发送消息失败，未触发 Web 和邮件通知。NPR-23447：适用于 CQ-4242880 的修补程序

### 翻译 {#translation-1}

* 在翻译配置中设置“不翻译”资产时，将创建资产语言副本。 NPR-22540：适用于 CQ-4237962 的修补程序

### 用户界面 {#user-interface-1}

* 将Omnisearch与连字符查询一起使用会返回服务器错误。 NPR-22999：适用于 Granite-19674 的修补程序
* 日期选取器不支持由隐藏的字段设置的手动设置外部类型提示。更改类型提示会导致转换错误。NPR-23333：适用于 Granite-21194 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-2}

* CAPTCHA组件已弃用以提高安全性，如果您使用的是CAPTCHA组件，则会显示消息“Captcha组件已弃用，不应再使用。” 将在安装6.2 SP2-CFP15或更高版本后显示。 AEM组件可以进行自定义以包含reCAPTCHA以增强安全性NPR-22151:CQ-4220052的修补程序
* WCM Foundation组件“表”易受存储跨站点脚本的攻击。 NPR-23206：适用于 CQ-4240760 的修补程序

### 漏洞 {#vulnerability-2}

* 管理员 UI 项目链接中存在跨站点脚本 (XSS) 漏洞。NPR-23272：适用于 CQ-4241795 的修补程序

## 表单 {#forms-5}

### Forms 附加组件包 {#forms-add-on-package-5}

#### 通信管理 {#correspondence-management}

* 通过默认预览预览字母时，布局片段映射不会显示，而在单击预览按钮时，布局片段映射会正确显示。 NPR-23335：适用于 CQ-4237745 的修补程序
* 在使用直接字母URL时，不填充与XDP中定义的绑定对应的字母中的数据。 NPR-24145：适用于 CQ-4244290 的修补程序

#### 移动Forms{#mobile-forms}

* （对应管理）使用目标XML加载信件时数据未对齐。 NPR-22993：适用于 CQ-4237663 的修补程序

#### Reader扩展服务{#reader-extensions-service}

* 无法在Adobe PDF应用读者扩展。 NPR-23067

#### 表单管理器 {#forms-manager}

* Forms嵌入到网站中的内容不会在重新发布网站页面时发布。 NPR-23014：适用于 CQ-4236566 的修补程序

#### 漏洞 {#vulnerability-3}

* 跨站点脚本的主动修补程序。 NPR-20624：适用于 CQ-4206055 的修补程序
* 表单管理器的注释选项卡中存在存储型跨站点脚本 (XSS) 漏洞。NPR-27157：适用于 CQ-4255556 的修补程序

#### 加密服务{#encryption-service}

* (OSGI)[JEE]在使用“验证PDF进程”进行验证时，带附件的PDF的签名状态不正确。 NPR-23269、NPR-23737

### Forms JEE 安装程序 {#forms-jee-installer-5}

#### 核心 {#core-1}

* 核心文本的静态代码分析中报告的问题应该得到修复。 NPR-13947

#### PDFG 服务 {#pdfg-service}

* HTML到PDF转换器无法工作。 NPR-21545

### 包含{#osgi-bundles-and-content-packages-included-4}的OSGI包和内容包

以下文本文档OSGI包的列表以及CFP中包含的内容包。

AEM 6.2 SP1-CFP15中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/6_2cfp15updated_bundles.txt)

AEM 6.2SP1-CFP15中包含的内容包列表

[获取文件](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### 累积修补程序包 14 {#cumulative-fix-pack-6}

AEM Cumulative Fix Pack 6.2 SP1-CFP14是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 改进了资产的元数据属性的可编辑性。
* 为已处于过期状态的资产重新配置密码到期通知作业。
* 自定义触摸UI控制台以扩展其他区域设置。
* 更新了cq-msm-core，以实现有效的Livecopyindex同步。
* 简化了各种推广的复制功能。

### 资产 {#assets-5}

* 用户无法下载包含免责声明和长文件名的资产。NPR-22163：适用于 CQ-4235274 的修补程序
* 单引号字符可防止在批量视图中更新元数据，当您使用快速工具栏操作打开资产属性时，用户界面会完全断开。 NPR-22317、NPR-22353：适用于 CQ-4236990、CQ-4236469 的修补程序
* 资产到期通知作业不会取消激活过期的资产。 NPR-22346：适用于 CQ-4237188 的修补程序
* 在 Safari 上的资产中使用数字版权管理时，资产下载失败。NPR-22378：适用于 CQ-4236460 的修补程序
* 小图像的Web再现像素大小不准确。 NPR-22435：适用于 CQ-4236742 的修补程序

### 站点 {#sites-5}

* （触屏UI）移动的标记显示在页面属性的新旧位置。 NPR-21921,CQ-4238598的修补程序
* （触屏UI）富文本编辑器从&lt;a>标记中删除除id之外的所有属性。 NPR-22045：适用于 CQ-4234133 的修补程序
* 使用CTRL+V直接在富文本编辑器中粘贴内容会跳过换行符。 NPR-22117：适用于 CUI-5881 的修补程序
* （触屏UI）无法在命名空间下显示40个以上的标记。 NPR-22290：适用于 CQ-99114 的修补程序
* RSS源问题，端口-1到AEM 6.2 NPR-22158:CQ-4233339的修补程序
* (IE)首次在富文本字段中创作任何字符时，将向该字符添加尾随空格。 NPR-22443：适用于 CQ-4235343 的修补程序
* 当尝试与包名称匹配时，Java Use对象由于包声明中的尾随空格字符而冻结SightlyJavaCompilerService。 NPR-22557：适用于 Granite-20836 的修补程序
* 触屏UI控制台不会选取新的语言进行标记。 NPR-22250：适用于 CQ-4239194 的修补程序

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite)发布日期和封面日期是作品集上传到DPS之前必须设置的字段。 NPR-22484

### 商务 {#commerce}

* 商务创建目录向导上存在多个跨站点脚本(XSS)漏洞。 NPR-22344：适用于 CQ-4237017 的修补程序

### MSM {#msm-2}

* LiveCopyIndex同步会导致长索引更新期间线程拥塞。 NPR-22214：适用于 CQ-90667 的修补程序
* 编辑Live Copy中的其他字段时，会禁用cq:cugEnabled属性，因此不保护页面。 NPR-22246：适用于 CQ-4236050 的修补程序
* 挂起页面时，“页面滚出”操作无法更新子项。 NPR-22483：适用于 CQ-4236956 的修补程序
* 转出已在母版中移动的结构会导致错误的 cq:moveTarget。NPR-22373：适用于 CQ-4232536 的修补程序

### 集成 {#integration-6}

* 尝试对优惠选择器库中的优惠进行排序会导致行为不规则。 NPR-22208：适用于 CQ-4235439 的修补程序
* 在长时间运行的查询期间，TargetContentImpl 致使 AEM 运行缓慢。NPR-22361：适用于 CQ-4236907 的修补程序
* Target 引擎（mbox.js、at.js）不使用损坏的 URL，而是使用包含冒号的 URL，这在某些部署中可能会失败。NPR-22366：适用于 CQ-4237854 的修补程序
* 页面个性化需要直接在品牌节点上发布。 NPR-22370：适用于 CQ-4236895 的修补程序

### Foundation {#foundation}

* Apache Sling脚本Sightly模型使用Provider捆绑&#x200B;**org.apache.sling.scripting.sightly.models.provider/1.0.18**。 NPR-22614:Sling-5944、Sling-6866的修补程序

### 项目 {#projects}

* 工作流启动程序无法接受字符串的TypeHint值。 NPR-22436：适用于 CQ-4237855 的修补程序

### 翻译 {#translation-2}

* 调查预览功能存在的问题。NPR-22201：适用于 CQ-4223753 的修补程序

### 用户界面 {#user-interface-2}

* （经典UI）组件显示默认值，即使关联的表单数据模型服务设置为空字段也是如此。 NPR-21903：适用于 GRANITE-19744 的修补程序

### WCM - Foundation 组件  {#wcm-foundation-components-3}

* 以Adobe Campaign形式发布指向导入程序页面的Live Copy页面时出错。 NPR-22470：适用于 CQ-4237164 的修补程序
* 打开Experience Fragments Editor时出错。 NPR-22598：适用于 CQ-4238415 的修补程序

### 工作流 {#workflow}

* Day CQ Workflow Email Notification Service为WorkflowCompleted和WorkflowAborted通知每个Mongo节点触发一封电子邮件。 NPR-22486：适用于 CQ-4238172 的修补程序

## 表单 {#forms-6}

### Forms 附加组件包 {#forms-add-on-package-6}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

#### 自适应表单 {#adaptive-forms-4}

* 在IE11和Chrome中，自适应表单中下拉占位符值不一致。 NPR-22405：适用于 CQ-4227096 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-6}

#### 安装 LCM {#install-lcm}

* 在安装程序和 LCM 中将 Jsafe Jars 更新为 Cryptoj 6.1.3.1。NPR-22744

### 包含的功能包 {#feature-packs-included}

#### 进程管理 {#process-management}

* （HTML工作区）当用户声明任务时，将刷新该特定用户的队列计数，但不会刷新其他用户的队列计数，除非刷新页面。 NPR-19778：适用于 CQ-4233665 的修补程序

### CFP14{#osgi-bundles-and-content-packages-included-in-cfp}中包含的OSGI捆绑和内容包

AEM 6.2 SP1-CFP14中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/6_2cfp14updated_bundles.txt)

AEM 6.2SP1-CFP14中包含的内容包列表

[获](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
取文件AEM Cumulative Fix Pack 6.2 SP1-CFP13是一个重要更新，包含自AEM 6.2 SP1正式发布以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 在将AT.js用作客户端库时，在目标组件设置中启用静态参数字段配置。
* 修复了下拉组件的显示/隐藏功能。
* 使用目标同步受众的修复。
* 增加了通信管理的通用性，以适应特殊字符。

### 资产 {#assets-6}

* 版本清除无法删除旧版本的资产。 NPR-21682：适用于 CQ-4212996 的修补程序
* 不会保留可重新排序文件夹下的文件夹的重新排序。 NPR-21964：适用于 CQ-4231761 的修补程序

### 站点 {#sites-6}

* (TouchUI)(ClassicUI)HTL和核心组件中存在多个跨站点脚本(XSS)漏洞。 NPR-21532：适用于 CQ-4232305 和 CQ-4232511 的修补程序
* 在Internet Explorer 11中，对选定文本创建／设置内容格式(例如，指定／删除新的列表样式)不起作用。 NPR-21533：适用于 CQ-4230689 的修补程序
* (Safari)用户无法视图资产查找器面板中的所有资产。 NPR-21981：适用于 CQ-4213720 的修补程序
* 时间扭曲返回页面乱码的“RecursionTooDeepException”错误，即使日期发生更改，也不会创建任何新版本。 NPR-21707：适用于 CQ-4199536 的修补程序
* 在编辑器中加载页面时，WorkflowStatusprovider(pageinfo.json)被加载三次，导致AEM实例执行缓慢。 NPR-21778：适用于 CQ-59232 的修补程序

### 集成 {#integration-7}

* 在创作受众模式下创建移动类型和浏览器目标在AEM中不起作用。 NPR-21676、NPR-21681：适用于 CQ-4232100 的修补程序
* 在目标组件刷新期间的高延迟下，可在完全刷新组件之前添加其他优惠。 NPR-21744：适用于 CQ-4233158/CQ-4234293 的修补程序
* 用户无法在mbox调用中看到测试静态参数值，当在云配置中以AT.js作为客户端库进行测试时，会看到该值。 NPR-21930：适用于 CQ-4234520 的修补程序

### 平台 {#platform-4}

* 当用户或用户组数量较大时，用户同步的性能问题。 NPR-20431：适用于 CQ-4223282 的修补程序
* 未使用Sling Distribution与用户同步同步的用户。 NPR-21911：适用于 Granite-20404 的修补程序
* 阻止在搜索摘录(在Geometrixx页面上)中高亮显示停止词。 NPR-21835：适用于 Granite-21067 的修补程序\
   注意：此修复需要Oak CFP 1.4.20或更高版本。

### 翻译 {#translation-3}

* 创建转换项目时，启动器用户id缺少jcr属性。 NPR-21715：适用于 CQ-4230713 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-4}

* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-22164：适用于 CQ-4235288 的修补程序

## 表单 {#forms-7}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包  {#forms-add-on-package-7}

#### 自适应表单 {#adaptive-forms-5}

* XML外部实体注入(XXE)在自适应Forms中的应用。 NPR-21982：适用于 CQ-109878 的修补程序
* (iOS11)单击文件附件组件时，文件附件会打开相机而不是设备文件浏览器。 NPR-21926：适用于 CQ-4214348 的修补程序
* 主题创建UI中缺少标题会导致对话框出现异常和无法呈现。 适用于 CQ-4236143 的修补程序

#### 通信管理 {#correspondence-management-1}

* 包含特殊字符的xml数据的渲染问题。 NPR-21712：适用于 CQ-4229137 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-7}

#### 汇编程序服务 {#assembler-service}

* 使用6.2.0-ASM-1017-003生成的PDF文件已损坏。 NPR-21427：适用于 CQ-4228046 的修补程序

#### PDFG 服务 {#pdfg-service-1}

* PNG、JPEG和TIFF文件中意外的页面大小(PDF)导致OCR失败。 NPR-19489：适用于 CQ-4209079 的修补程序

## CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}中包含的OSGI捆绑和内容包

AEM 6.2 SP1-CFP13中包含的OSGi包的列表

[获取文件](assets/do-not-localize/cfp13_bundlecompare-list.txt)

AEM 6.2SP1-CFP13中包含的内容包列表

[获取文件](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP12.1是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 改进了多值字段的元数据处理。
* 在翻译工作流支持多字符（两个以上）国家代码。
* 改进了具有多个嵌套组件的页面的呈现。
* 改进了AEM和Adobe Digital Publishing Suite之间资产发布日期的同步。

### 资产 {#assets-7}

* OmniSearch 中的字符过多导致 AEM 服务器崩溃。NPR-21083：适用于 CQ-4223602 的修补程序
* 在元数据模式的多值字段中的第二个选项中指定的值不会附加到CRX-de中先前指定的值。 NPR-21220：适用于 CQ-4224526 的修补程序
* 在 Safari 上的资产中使用数字版权管理时，资产下载失败。NPR-21387：适用于 CQ-4230287 的修补程序

### 站点 {#sites-7}

* (DAM)(ClassicUI)AEM CQ作者／发布快速启动中的某些SWF文件中存在多个跨站点脚本(XSS)漏洞。 NPR-21073、NPR-21074:NPR-20612的修补程序
* 标记选取器不会翻译多种语言中可用的标记。NPR-21221:CQ-78855的修补程序
* AEM文章控制台的渲染问题（与使用多个嵌套组件一样）使其变得迟缓。 NPR-21271：适用于 CQ-4224158 的修补程序

### 集成 {#integration-8}

* 添加目标框架时，在编辑器的选择模式列表中，定位模式不可用。 NPR-21047

### 按需移动{#mobile-on-demand-1}

* (Digital Publishing Suite)AEM中作品集的出版日期与Folio Producer中显示的日期不匹配。 NPR-21145

### MSM {#msm-3}

* 删除LC中的第一个本地页面后，Live Copy重置过程将停止。 NPR-21276：适用于 CQ-4229743 的修补程序

### 平台 {#platform-5}

* 升级到AEM 6.3后，找不到作为脚本实现的引用标记的自定义taglib。NPR-20149:Granite-18433的修补程序

### 翻译 {#translation-4}

* 翻译工作流失败，但lang_country代码长于2个字符。 NPR-21088：适用于 CQ-4197439 的修补程序
* 在项目完成之前，不应再允许将资产页面提交到翻译项目。 NPR-21219：适用于 CQ-4209908 的修补程序

### 用户界面 {#user-interface-3}

* 选择组件不会在提交表单时删除目标属性。 NPR-21163：适用于 GRANITE-14125 的修补程序
* HTTP.encodePathOfURI扩展多次对加号“+”进行编码。 NPR-21417：适用于 GRANITE-16340 的修补程序

### 漏洞 {#vulnerability-4}

* DAM元数据编辑器中的跨站点脚本(XSS)。 NPR-21434：适用于 CQ-83472 的修补程序
* 多个SWF文件易受跨站点脚本(XSS)攻击。 NPR-20612：适用于 CQ-4213297 的修补程序

## 表单 {#forms-8}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包  {#forms-add-on-package-8}

#### 通信管理 {#correspondence-management-2}

* (IE11)HTML内容的初始呈现仅在左侧进行，而在加载完整的UI后，右侧间歇性地加载。 NPR-21554
* 安装AEM 6.2 SP1-CFP9后，将禁用字母预览提交按钮。 NPR-21547
* 在选择资产链接类型时，“资产选择器”窗口不会在“编辑信函数据绑定”向导中打开。 NPR-21164：适用于 CQ-4194567 的修补程序
* 要编辑内联或可编辑的文本模块，请点按相关的编辑图标，或在字母多次中单击相关文本模块。 NPR-21402

#### 自适应表单 {#adaptive-forms-6}

* AEM Forms提交按钮组件显示type=&quot;button&quot;而不是type=&quot;submit&quot;。 NPR-21007
* 在为可重复面板添加或删除新面板时，数据将保持持续。 NPR-21408

### Forms JEE 安装程序 {#forms-jee-installer-8}

#### 核心 {#core-2}

* 升级到最新的Java 8 Update 131会引发异常：&quot;JsafeJCE提供程序已禁用，FIPS 140要求的自我完整性检查失败&quot;。 NPR-21355

   **注意：** 此NPR需要其他设置，有关详细信息，请 [参阅最新的Java 8更新](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr)。

* 在核心、加密、签名和文档安全中将jsafe Jar更新为cryptoj 6.1.3.1。 NPR-21360、NPR-21361、NPR-21356、NPR-21358

#### 安装 LCM {#install-lcm-1}

* 在安装程序和LCM中将Jsafe Jar更新至Cryptoj 6.1.3.1。 NPR-21362

#### PDFG 服务 {#pdfg-service-2}

* 在PDFG中将Jsafe Jar更新到Cryptoj 6.1.3.1。 NPR-21359

#### 进程管理 {#process-management-1}

* (HTML Workspace)启用列大小调整功能，使名称类别不会被截断。 NPR-19770：适用于 CQ-4233668 的修补程序

#### Reader扩展服务{#reader-extensions-service-1}

* 在RE中将jsafejar更新为cryptoj 6.1.3.1。 NPR-21357

## CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}中包含的OSGI捆绑和内容包

AEM 6.2 SP1-CFP12.1中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

AEM 6.2 SP1-CFP12.1中包含的内容包列表

[获取文件](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP11是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 更新了cq-msm-core，以实现有效的Livecopyindex同步。
* 提高了内容片段的编辑效率。
* 在包管理器中提供用于检测ACL权限的验证选项。
* 引入了活动为客户通信加入电子邮件ID的功能。
* 增强了Dynamic Media文件的视频编码能力。
* Sightly组件和LiveCopy中的修复。

### 资产 {#assets-8}

* Dynamic Media视频编码对名称中包含空格的文件失败。 NPR-20818：适用于 CQ-102469 的修补程序
* AEM CQ作者／发布快速启动中的某些SWF文件中存在多个跨站点脚本(XSS)漏洞。 NPR-21071、NPR-21072
* 用户无法下载包含免责声明和长文件名的资产。NPR-20255：适用于 CQ-4222139 的修补程序

### 站点 {#sites-8}

* AEM和活动集成：特殊链接在Adobe Campaign中被重写，阻止客户发送邮件到：超链接。 NPR-20787：适用于 CQ-4225760 的修补程序
* （触屏UI）将语言设置为法语时AEM可用性问题和性能问题。 NPR-20854：适用于 CQ-4227628 的修补程序
* 在RTE中使用链接插件链接已编码的资产文件将返回空链接。 NPR-20626、NPR-21059：适用于 CQ-4223011 的修补程序
* 内容片段元数据编辑器阻止内容作者保存对内容片段的更改。 NPR-20641：适用于 CQ-4224755 的修补程序
* 页面属性别名导致请求发布／请求取消发布。 NPR-20731：适用于 CQ-4226227 的修补程序
* 文本组件在RTE元素中的链接编码存在问题。 NPR-20755：适用于 CQ-4224321 的修补程序

### 平台 {#platform-6}

* ResourceResolverImpl.map()不调用ResourceDecorator。 NPR-20788：适用于 GRANITE-19718 的修补程序
* org.apache.sling.i18n.DefaultLocaleResolver无法通过org.apache.sling.engine.SlingRequestProcessor处理请求。 NPR-20706：适用于 CQ-94880 的修补程序
* 请求在包管理器中添加验证选项，以检测特定包上是否更改了任何ACL权限／权限。 适用于 CQ-4229196 的修补程序

### 集成 {#integration-9}

* (Search&amp;Promote)内容包的过滤器定义不明确会导致安装时被覆盖的路径。 NPR-20808：适用于 CQ-4227615 的修补程序

### 工作流 {#workflow-1}

* AEM 生产服务器部署存在稳定性问题。NPR-20979：适用于 Granite-19104 的修补程序

### 项目 {#projects-1}

* （触屏UI）无法将团队成员添加到项目。 NPR-20990：适用于 CQ-4205375 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-5}

* Sightly图像组件“链接到”会因缺少。html扩展名而生成403错误。 NPR-20823：适用于 CQ-4195909 的修补程序
* 在使用LiveCopy的Blueprint站点上，尝试删除表单组件会引发NullPointerException并添加回表单组件，而不是删除它。 NPR-20855：适用于 CQ-4204628 的修补程序
* LiveCopyIndex同步会导致长索引更新期间线程拥塞。 NPR-20634：适用于 CQ-90667 的修补程序

### 安全 {#security}

* 主动式XSS库更新。 NPR-21174
* 升级到Apache Commons Email 1.5，它提供了用于发送电子邮件的简化API。 NPR-20509：适用于 Granite-18240 的修补程序
* 应用于Apache Sling XSS Protection API的安全修补程序，可消除XSS绕过的可能性。 NPR-21290：适用于 GRANITE-19924 的修补程序
* XSSAPI#getValidHref函数中绕过XSS。 NPR-21174：适用于 Granite-19924 的修补程序

### 移动应用程序 {#mobile-apps}

* 修复了 AEM 中 OOTB 资产的 curl Head 请求问题。NPR-20511：适用于 CQ-4221520 和 CQ-103024 的修补程序

## 表单 {#forms-9}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

AEM Forms 的主要功能亮点包括：

* 为 Workbench 用户启用了证书身份验证。
* 针对通信管理、HTML5表单和AEM Forms工作区的可用性修复。

### Forms 附加组件包 {#forms-add-on-package-9}

#### HTML5 表单 {#html-forms-1}

* iOS 10和11设备上的涂抹组件的可用性问题。 NPR-21092

#### 通信管理 {#correspondence-management-3}

* （对应UI）单击后禁用提交按钮。 NPR-21078

### Forms JEE 安装程序 {#forms-jee-installer-9}

#### 汇编程序服务 {#assembler-service-1}

* docConverter无法生成PDF/A，错误为“stEvt:action”元素的前缀“stEvt”未绑定。 NPR-21032：适用于 CQ-4222540 的修补程序
* 调用服务OMPFSubmission/PDFA/PDFAtoPDFA时，引发一个名为java.lang.IllegalArgumentException消息：没有枚举常数com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTE。 这会阻止短期签名验证过程在重新启动服务器之前完成。 NPR-20792

#### Workbench {#workbench}

* 为Workbench用户启用证书身份验证。 NPR-17548：适用于 CQ-4214486 的修补程序

#### 进程管理 {#process-management-2}

* 当使用dataref参数呈现移动表单时，准备数据流程将多次调用。 NPR-19801：适用于 CQ-4230427/CQ-4230400 的修补程序

## CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}中包含的OSGI捆绑和内容包

AEM 6.2 SP1-CFP11中包含的OSGi捆绑包的列表

[获取文件](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

AEM 6.2 SP1-CFP11中包含的内容包列表

[获取文件](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP10是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 为测试添加了一个新的实用程序函数onDialogLoaded。
* 为ClientLibraryProxyServlet添加了前端单元测试和配置。
* 多个图像就地编辑器组件中的性能修复。
* Apache Sling JCR ResourceBundleProvider中的配置更新。

### 资产 {#assets-9}

* 如果禁用了资产更新预览，则资产工作流将无效。 NPR-20543：适用于 CQ-4204986 的修补程序
* 花岗岩中添加的类的渲染问题：class属性(cq-damdin-admin-assets-upload)。 NPR-20514：适用于 CQ-4219238 的修补程序
* 标题中具有特殊字符的缩略图资产在NPR-20347的alt属性中显示java对象：CQ-4223620的修补程序
* 由于许可问题，使用 Adobe 专有代码替换版本比较代码。NPR-20273：适用于 CQ-4223758 的修补程序
* 上传具有多个Alpha图层的CMYK PSB文件时的处理问题。 NPR-20251：适用于 CQ-4220869 的修补程序
* 除非在org.apache.sling.i18n 2.5.6中重新启动服务器，否则国际化词典不起作用。NPR-20525:花岗岩修补程序- 19490
* 不会根据具有默认线程转储收集器配置(默认AEM调度程序)的开始期生成线程转储。 NPR-20288:GRANITE-19488/GRANITE-12741/CQ-90647的修补程序。

### 站点 {#sites-9}

* 如果在打开保存的搜索后更改了修改的日期筛选器，则对结果没有影响，显示的结果与修改的日期筛选器之前保存的值相同。 NPR-19739：适用于 CQ-4219425 的修补程序
* 加载包含嵌套组件的页面失败。 NPR-20312
* 删除工作流包时会触发删除请求工作流。 NPR-20266：适用于 CQ-4221686 的修补程序
* （触屏UI）复制／粘贴操作系统剪贴板和内部AEM剪贴板的问题。 NPR-20228：适用于 CQ-4220383 的修补程序
* 加载多个资产（超过100个）时，AEM实例会因列表视图而变得迟缓。 NPR-20034：适用于 CQ-4222695 的修补程序
* [触屏 UI] 通过经典 UI 控制台删除启动项会使所有页面无法编辑。NPR-20520：适用于 CQ-4225074 的修补程序
* 目标下拉列表不能用于对话框中的多个RTE组件。 NPR-20345：适用于 CQ-4220981 的修补程序

### 平台 {#platform-7}

* 使用匿名会话访问时，ClientLibraryProxyServlet不代理发布实例上对客户端库的请求，并引发HTTP 404未找到错误。 NPR-20195：适用于 Granite-14409 的修补程序

### 集成 {#integration-10}

* 选择目标引擎作为“Adobe Target”可阻止加载组件，并在服务器日志中引发错误。 NPR-20058：适用于 CQ-88071、CQ-109698、CQ-4201600 的修补程序

### 商务 {#commerce-1}

* 创建同一页面的产品时不显示确认或重定向弹出消息。 NPR-20257：适用于 CQ-4223414 的修补程序

### 用户界面 {#user-interface-4}

* 当日期选取器是多字段中的字段时，在编辑组件时不会保留日期字段中保存的值。 NPR-20077：适用于 GRANITE-19147 的修补程序
* 如果触发连续查询导致不正确的结果，之前的查询不会被中止。NPR-20397：适用于 GRANITE-19306 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-6}

* 即使从多个图像就地编辑器组件中删除图像后，ImageMap属性仍然存在。 NPR-20142：适用于 CQ-4222982 的修补程序

## 表单 {#forms-10}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包  {#forms-add-on-package-10}

#### 自适应表单 {#adaptive-forms-7}

* 当通过UI进行更改时，对DropDownList执行两次valueCommit脚本。 NPR-19989：适用于 CQ-110212 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-10}

**进程管理**

* CFP包包含AEM FormsHTML Workspace版本2.2.26。NPR-20099
* 将移动表单配置为视图为PDF时，预填表单不起作用。 NPR-20566

**Rights Management**

* CAC/双向身份验证证书选择对话框应将具有增强密钥使用(EKU)的证书显示为客户端身份验证或智能卡登录。 NPR-20708
* Forms JEE 支持 PKCS#11 双向身份验证。NPR-15001

## CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}中包含的OSGI捆绑和内容包

AEM CFP 6.2 SP1-CFP10中包含的OSGi包的列表

[获取文件](assets/do-not-localize/bundle-list-cfp10.txt)

AEM CFP 6.2 SP1-CFP10中包含的内容包列表

[获取文件](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP9是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 改进了Analytics Classic UI配置以进行机密输入。
* 针对Contexthub的独立持久性缓存的修复。
* 准确计算资产维度。
* 优化了将资产发布到Brand Portal时的AEM性能。
* 修复了画布节点中的资源类型值。
* 为文档片段内容启用区分大小写和特殊字符搜索功能。
* 增强的自适应Forms功能，可将PDF作为附件附加到Safari中。\
   提供连接到新的Dynamic Media出版基础架构的新Dynamic Media，以实现更快、更灵活的复制。

### 资产 {#assets-10}

* AEM Assets无法提取InDesign资产的子资产引用，包括指向该资产的重复链接。 NPR-19006：适用于 CQ-4204186 的修补程序
* “排序”选项不用于“商务”下集合中的资产。 NPR-19508：适用于 CQ-4213622 的修补程序
* 当具有与先前现有资产相同名称的资产被移动到同一位置时，cq的值：资产的lastReplicationAction在它们之间进行交换，这会导致创建错误的元数据。 NPR-19531
* 发布大量资产时会显示一条错误消息，尽管所有资产均正确发布。 NPR-19629：适用于 CQ-4219611 的修补程序
* 静态演绎版以固定尺寸列出，不反映实际演绎版的大小。 NPR-20004
* 将多个资产（超过 4 个）发布到 Brand Portal 时，AEM 实例运行缓慢。NPR-20009

### 站点 {#sites-10}

* AEM在用户尝试发布其他用户锁定的页面的/unpublish/create版本时显示意外行为。 NPR-19249;CQ-4215298和CQ-4203856的修补程序
* 手动提升嵌套启动项时，子页面将被删除。 NPR-19704
* 在初始化过程中 ContextHub 存储覆盖默认持久层时出现持久性问题。NPR-19979：适用于 CQ-4218399 的修补程序
* 内容片段与其他按钮重叠。 NPR-19980：适用于 CQ-4221519 的修补程序
* 在SiteAdmin中使用别名查看时，不显示站点页面。 NPR-20053：适用于 CQ-4221478 的修补程序
* 以Adobe Campaign形式发布指向导入程序页面的Live Copy页面时出错。 NPR-20066：适用于 CQ-4220846 的修补程序

### 平台 {#platform-8}

* 已将Apache POI升级到版本3.16，以支持在再现中包含PPT幻灯片的背景图像。 NPR-18286
* 在同一文件夹中上传多个资产时，Internet Browser 11和Edge的渲染问题。 NPR-20062

### 集成 {#integration-11}

* 使用匿名用户访问时，自定义 at.js 文件不会发布。NPR-19542：适用于 CQ-4219592 的修补程序
* 将Analytics现有凭据迁移到WSSE身份验证。 NPR-19962

### Brand Portal {#brand-portal}

* 启用通过 tagadmin/tagging 控制台将标记从 AEM 发布到 Brand Portal 的功能。NPR-20271

## 表单 {#forms-11}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包  {#forms-add-on-package-11}

#### 通信管理 {#correspondence-management-4}

* 启用了在预览字母时搜索文档片段中实际文本的功能。 NPR-19712

#### 自适应表单 {#adaptive-forms-8}

* 增强的自适应Forms功能，可将PDF作为附件附加到Safari中。 为了在现有表单中支持相同功能，我们需要在附件构件和“支持的文件类型”中更改配置，更新值application/pdf，而不是。pdf。 NPR-19623

#### 表单管理器 {#forms-manager-1}

* 如果在自适应表单的字段上未定义validationState，并且发生elementFocusChanged事件，则错误事件(errorState)将返回到Adobe Analytics服务器。 NPR-19513

### Forms JEE 安装程序 {#forms-jee-installer-11}

#### 核心 {#core-3}

* 关闭期间连接管理器不可用。 在取消部署作者EAR之前，Jboss会切断JDBC依赖关系，从而导致损坏问题。 NPR-19703

## 包含的功能包 {#feature-packs-included-1}

* Dynamic Media的缩略图校正和透明度改进。 NPR-15207

## CFP9{#osgi-bundles-and-content-packages-included-in-cfp-5}中包含的OSGI包和内容包

列表AEM 6.2SP1-CFP9中更新的内容包

[获取文件](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

列表AEM 6.2SP1-CFP9中更新的OSGi捆绑包

[获取文件](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP8是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 在Adobe电子邮件模板服务上为自定义用户模板引入标记。
* 桌面应用程序的TouchUI按钮增强功能。
* 单击时禁用提交按钮可防止在翻译页面上提交多个表单。
* 在对话框中配置了多个RTE组件。
* 增强的参考Live Copy中的更新。
* 为文档片段内容启用区分大小写的搜索功能。
* 在AEM Forms安装文档中添加了Linux库列表。

### 资产 {#assets-11}

* 在Safari浏览器上对智能集合应用Omnisearch过滤器时出现的问题。 NPR-19511
* 当有多个与 PDF 资产关联的关键字时，PDF 关键字元数据无法正确提取，并且会以错误方式修改。为解决该问题，已删除 PDF 资产的“主题”字段元数据属性。但是，您可以编辑元数据架构，为“主题”字段添加多值文本字段。NPR-19126
* 工作流通知服务不会对电子邮件中的链接进行编码，这会阻止用户在单击链接后加载链接。 NPR-19490：适用于 CQ-4218055 的修补程序
* 无法使用 Chrome 在列视图中加载页面/资产的完整列表。NPR-19458：适用于 CQ-4214248 的修补程序
* 激活“请求激活”工作流时，AEM收件箱中显示不正确的关闭时间图标。 NPR-19365:CQ-4216174
* 在列表视图中排序的问题。 NPR-19217:CQ-95602
* 在“资产文件夹”设置中更改标题或缩略图图片时，文件夹的原始组和权限会被覆盖。NPR-19283：适用于 CQ-4216080 的修补程序
* Windows 10工作站自动切换到触控模式，禁用部分按钮无法正常工作。 NPR-19183

### 站点 {#sites-11}

* 在对话框中包含多个RTE组件的问题。 NPR-19311：NPR-19587
* 在VersionManagerImpl初始化后，vanilla AEM 6.2中的自动版本清除只能运行一次。 NPR-19315：适用于 CQ-4217175 的修补程序
* 工作流实例卡在“Salesforce.com导出”工作流步骤上。 NPR-19222：适用于 CQ-4212976 的修补程序
* 无法编辑从Live Copy创建的语言副本页面。 NPR-18967
* ReferencesUpdateAction无法在层次结构发生变化时将链接更新到嵌套LiveCopy中。 NPR-18715：适用于 CQ-4214105 的修补程序

### 平台 {#platform-9}

* Adobe 电子邮件模板服务会将标记添加到自定义用户模板。NPR-19190：适用于 CQ-4217113 的修补程序

### 项目 {#projects-2}

* 项目编辑者无法将资产复制/粘贴到项目资产文件夹中。NPR-19619
* 安装6.2 SP1-CFP1后，无法为翻译项目生成预览。 NPR-16481:CQ-4204655

### 集成 {#integration-12}

* 在经典 UI 上的 Adobe Digital Publishing Solution 中，文章的访问属性设置不正确。NPR-19366
* 由于AEM文章控制台中的全尺寸文章，缩览图呈现缓慢。 NPR-19086:CQ-4217148
* 如果用户可以访问多个区域，通过 Campaign 个性化选件时，会出现自动折叠的错误行为。NPR-19290：适用于 CQ-4218029 的修补程序
* 如果对定位模块进行编辑并保存超过一次，则定位模式下不显示定位对话框。NPR-19144：适用于 CQ-4216708 的修补程序

### 工作流 {#workflow-2}

* 用户无法在收件箱经典UI中按用户／组过滤收件箱中的通知。 NPR-19122：适用于 CQ-4215374 的修补程序
* 图像映射在HTL图像组件中不保留选定的坐标。 NPR-18911:CQ-4211584

## 表单 {#forms-12}

* AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-12}

* 当内容从Microsoft Word或Web浏览器复制到通信管理器文本编辑器时，样式将丢失。 NPR-19530
* 没有换行符的文本编辑器的内容不会换行。 NPR-19481
* 启用了在预览字母时搜索文档片段中实际文本的功能。 NPR-17792：适用于 CQ-4214501 的修补程序

#### 通信管理 {#correspondence-management-5}

>[!NOTE]
>
>文本片段的此搜索功能具有一些限制：-
>
>* 文档片段内容区分大小写，标题不区分大小写。
>* 当搜索单词的一部分采用不同的样式或包含特殊字符（如“”或“或\”）时，搜索结果不会高亮显示。
>* 搜索在文档片段中不能用于动态内容（如数据字典元素值或变量值）。


#### 表单管理器 {#forms-manager-2}

* 在AEM 6.2上应用CFP6后，无法编辑自适应Forms的XML模式属性。CQ-4219684的修补程序
* 重新启动服务器时，不启动AEM Forms管理器核心包的所有服务。 适用于 CQ-4217014 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-12}

#### 安装 LCM {#install-lcm-2}

* 安装CFP6后，Microsoft Windows上的管理员屏幕显示版本号6.0。 适用于 CQ-4217573 的修补程序

## 包含的功能包 {#feature-packs-included-2}

* 桌面应用程序的TouchUI按钮增强功能。 NPR-18676

## CFP8{#osgi-bundles-included-in-cfp}中包含的OSGi捆绑包

列表AEM 6.2SP1-CFP8中更新的OSGi捆绑包

[获取文件](assets/do-not-localize/updated-bundles-list-cfp8.txt)

列表AEM 6.2SP1-CFP8中更新的内容包

[获取文件](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP7是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 在具有dc的图像卡上显示标题时的行为变化：title属性设置为字符串[](multifield)。
* 修复了Dynamic MediaCloud Services、触屏UI和安全UI界面的性能问题。
* Apache Felix Http Bridge 3.0.8中的修复
* 解决了创作和发布环境之间的无二进制复制(BLR)。
* 支持目标库文件AT.JS，这是一个用于与Adobe Target进行客户端集成的实现库，专为典型Web实现和单页应用程序设计。
* 通过为Marketing Cloud解决方案(Analytics、DTM、目标和S&amp;P)引入用户可配置的连接超时时间，提高了AEM性能。

### 资产 {#assets-12}

* 在使用配置了Dynamic MediaCloud Services的AEM 6.3测试视频摄取时，会出现“打开的文件太多”异常。 NPR-18734：适用于 CQ-4211407 的修补程序
* 重新启动AEM实例后，页面上资产的虚URL设置不起作用。 NPR-18634;Granite-18085的修补程序
* 在TouchUI中，对于没有发布资产权限的用户，将显示“发布”按钮。 NPR-18620：适用于 CQ-4214042 的修补程序
* 为资产设置许可协议后，资产的下载对话框中就不存在动态演绎版选项。 NPR-18607：适用于 CQ-4212342 的修补程序
* 无法为名称中包含空格的资产下载动态呈现版本。NPR-18571：适用于 CQ-4211738 的修补程序
* 与creative cloud共享资产文件夹时，无法保存多个用户。 NPR-18489：适用于 CQ-103297 的修补程序
* dc:title &amp; dc:crx/de中的description不更改为多字段值。 NPR-18474：适用于 CQ-4209086 的修补程序
* 移动资产操作会导致性能降低。 NPR-18346
* 在打开时间轴时，其中默认设置“显示全部”选项时，不会显示任何项目。 NPR-18302：适用于 CQ-4211957 的修补程序
* 将 ASCII/UTF-8 编码文本文件上传到 AEM Assets 时出现错误，并且缩略图生成失败。NPR-18006：适用于 CQ-4209345 的 CFP
* 即使用户没有复制访问权限，也会显示发布操作按钮。 NPR-17353：适用于 CQ-4209269 的修补程序
* 当使用min:gcc;obfuscate=true启用微型化时，Siteadmin和Miscadmin都不起作用。 NPR-18593：适用于 CQ-4209220 的修补程序
* 每次刷新屏幕之前，不会显示自定义菜单项。 NPR-18500：适用于 CQ-4213581 的修补程序
* 升级moment.js至2.10.6。 NPR-18596;Granite-11881的修补程序
* 对DM宏应用权限会中断管理员用户的视图。 NPR-18544：适用于 CQ-4211729 的修补程序
* 为资产稍后发布会引发非法ArgumentException。 CQ-4214532

### 站点 {#sites-12}

* 在具有MongoDB的活动——活动作者群集上，当时间达到内容的“按时”设置时，两位作者都会尝试为同一内容触发复制。 NPR-18708：适用于 CQ-4210982 的修补程序
* 在移动资源时，如果引用没有jcr:内容节点。 NPR-18664
* 占位符在包含多个 Parsys 组件的页面中不可见。NPR-18645：适用于 CQ-110253 的修补程序
* AbstractCopyMoveCommand中的并发问题。 NPR-18591
* 将文本从另一个AEM实例复制到parsys组件时，将创建parsys，而不设置任何resourceType。 NPR-18511：适用于 CQ-4212306 的修补程序

### 平台 {#platform-10}

* JCR安装程序在安装包后不更新捆绑版本。 NPR-18728;NPR-15135的修补程序
* 二进制b/w作者和发布环境的无二进制复制(BLR)失败。 NPR-18704
* AEM环境中的Apache Felix Http Bridge解析请求。 NPR-18297
* 当使用Sling内容分发同时复制具有相似结构的多个页面时，复制将失败。 NPR-18665;Granite-13712的修补程序
* Sling分发包已建立，未自行清理。 NPR-18601;Granite-16183的修补程序

### 集成 {#integration-13}

* 查看从库文件夹发布的优惠会生成NPE。 NPR-18732：适用于 CQ-4214593 的修补程序
* 在JCR和目标中，当从特定日期更改为“激活／取消激活时”时，开始的活动/结束日期不会更新。 NPR-18612：适用于 CQ-104831 的修补程序
* 与AEM的Analytics集成没有为httpclient连接设置连接或套接字超时。 NPR-18497
* 与AEM的DTM集成没有为httpclient连接设置连接或套接字超时。 NPR-18495
* 与AEM的目标集成没有为httpclient连接设置连接或套接字超时。 NPR-18494
* 与AEM的Search &amp; Promote集成没有为httpclient连接设置连接或套接字超时。 NPR-18493
* 目标活动在添加额外体验后将停用。 NPR-18227：适用于 CQ-4201895 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-7}

* 图像映射在HTL图像组件中不保留选定的坐标。 NPR-18530：适用于 CQ-4211584 的修补程序

### 翻译 {#translation-5}

* 翻译搜索结果中不包括翻译项目的名称。 NPR-18224：适用于 CQ-4210658 的修补程序

### Brand Portal {#brand-portal-1}

* 启用通过 tagadmin/tagging 控制台将标记从 AEM 发布到 Brand Portal 的功能。CQ-4212165

## 表单 {#forms-13}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-13}

#### 通信管理 {#correspondence-management-6}

* 在保存片段之前，正确的数据不会显示在编辑面板中。 NPR-19092
* 将文档片段添加到字母需要大量时间。 NPR-18958
* 如果数据xml文件中存在XML声明，并且通过POST请求启动字母再现，则相应的字母将无法显示数据。 NPR-18870
* 不会为对CM资产采取的操作生成审核日志。 NPR-16618

>[!NOTE]
>
>如果您受到以下两个问题的影响，请不要安装此CFP Add-on包：
>
>* 将粘贴从Word/Web复制到CM文本编辑器显示换行内容。 NPR-19530
>* CM文本编辑器中无换行的内容不会换行。 NPR-19449

>
>
这些问题将在未来的CFP中得到解决。

#### 自适应表单 {#adaptive-forms-9}

* 为可重复面板添加新面板时，将删除上一个面板中下拉字段的值。 NPR-18772
* 标记为仅接受整数的自适应表单字段也接受数字键盘中的几个特殊字符。 NPR-18680
* 用于在引导面板的初始化事件更改按钮标题的脚本无法工作。 NPR-18476
* 对于在规则编辑器下创建的规则，在右面板中看不到滚动条。 NPR-18716

#### AEM Forms 应用程序 {#aem-forms-app}

* Forms在AEM Forms应用程序处于脱机模式或未连接到网络时，无法在该应用程序中正确呈现。 CQ-4218368

### Forms JEE 安装程序  {#forms-jee-installer-13}

#### PDFG 服务 {#pdfg-service-3}

* PDF 生成器无法生成具有指定书签级别的 PDF 文档。适用于 CQ-4211102 的修补程序

## CFP7 {#osgi-bundles-included-in-cfp-1}中包含的OSGi捆绑包

列表AEM 6.2SP1-CFP7中更新的OSGi捆绑包

[获取文件](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

列表AEM 6.2SP1-CFP7中更新的内容包

[获取文件](assets/do-not-localize/cfp7_content_packages.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP6是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 在平板电脑的布局模式下有效管理隐藏的组件。
* 在混合设备上引入快速操作。
* 解决Live Copy的组件级同步问题。

### 资产 {#assets-13}

* 当没有所需权限的用户尝试移动资产上的操作时，客户会被阻止。 NPR-18330：适用于 CQ-4212560 的修补程序
* 合并多个智能内容服务配置会导致可用性问题。 NPR-18273：适用于 CQ-4201557 的修补程序
* 结帐操作/工作流大约在一次时间轴控制台中不可用。 80个片段添加在“资产”文件夹中。 NPR-18257;CQ-4211214和NPR-18251的修补程序；CQ-4211216的修补程序。
* 系统在“内存不足”时崩溃，在“资产”报告期间缺少分页。 NPR-17865：适用于 CQ-4209759 的修补程序
* 已发布的视频无法在编码视频资产上播放。 NPR-17849：适用于 CQ-4210739 的修补程序
* 不会生成PDF的缩略图。 NPR-17831、NPR-17750;CQ-4210547的修补程序
* 过期的资产不会由Adobe CQDAM到期通知作业停用。 NPR-17666：适用于 CQ-107766 的修补程序
* 如果资产没有分配的所有者，资产到期活动将停止。 NPR-17665：适用于 CQ-4197946 的修补程序
* 移动具有超过 150 个传入引用的资产文件夹时，会引发空指针异常。CQ-4200981

### 站点 {#sites-13}

* 个性化仅在为IP范围设置分段规则时适用于第一个IP。 NPR-18121：适用于 CQ-83767 的修补程序
* 启用historyShow属性时，由于NumberFormatException，登录失败。 NPR-18073：适用于 CQ-101965 的修补程序
* 标记的已删除页面在触屏UI中可见。 NPR-18025：适用于 CQ-86694 的修补程序
* 加载包含大量（2000 及以上）受众的页面时，出现性能问题。NPR-17884：适用于 CQ-4209567 的修补程序
* 在删除页面上的其他图像后，无法选择图像。 NPR-17711：适用于 CQ-4201323 的修补程序

### 平台 {#platform-11}

* 对于没有所需权限的用户，触屏UI控件不会隐藏。 NPR-17945：适用于 CQ-4211231 的修补程序
* 标记器字段中缺少日文标记。 NPR-17768：适用于 CQ-4210456 的修补程序
* 启用FastQuerySize时，getsize()查询返回错误结果。 NPR-18018
* 无法访问备用实例上的Web控制台。 NPR-17861;Granite-14582的修补程序

### 商务 {#commerce-2}

* 查询遍历在目录蓝图没有为节定义任何条件时发生。 NPR-18229：适用于 CQ-4211924 的修补程序

### 社区 {#communities-2}

* PollingImporterImpl。 推迟AEM关闭。 NPR-18298：适用于 CQ-96133 的修补程序

### 集成 {#integrations}

* 解决了在 AEM Day HTTP Client 3.1 OSGi 配置了需要摘要身份验证的代理时可能发生的 AEM 搜索组件错误。18128卢比
* 缺少用于还原继承的复选框。 NPR-17753;CQ-4210139的修补程序请求
* 当定位具有多个活动的一个组件时，用户无法设置优先级。 NPR-18658：适用于 CQ-4210727 的修补程序
* 用户无法浏览文件夹/etc/segmentation以选择在文件夹/etc/segmentation/group1下创建的受众。 NPR-18522

### 安全 {#security-1}

* 如果用户对目标文件夹没有写入权限，则移动资产向导将挂起。 NPR-18300
* 请求在Apache Sling API中使用org.apache.sling.servlets.post servelet(2.3.22)的升级版本以预防XSS漏洞。 NPR-18963

### 翻译 {#translation-6}

* 在项目完成之前，不应再允许将资产页面提交到翻译项目。 NPR-18249：适用于 CQ-4209908 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-8}

* 无法在可编辑的模板中使用WCM foundation iparsys组件。 NPR-18223：适用于 CQ-4210384 的修补程序
* 图像映射在HTL图像组件中不保留选定的坐标。 NPR-18032：适用于 CQ-4211584 的修补程序
* 当HTL图像组件呈现时，URL中的文件名将重命名，导致URL中断。 NPR-17908：适用于 CQ-4211587 的修补程序
* 进行更改后无法退出页面属性。 NPR-17832：适用于 CQ-96110 的修补程序

## 表单 {#forms-14}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅[AEM Forms版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-14}

**通信管理**

* 在字母渲染期间，数据字典会被重复读取。 NPR-18482,CQ-4210805的修补程序
* 为 com.adobe.livecycle.content 类添加了 JavaDocs。NPR-18467
* 创建字母时，不保存该字母的说明。 NPR-18039
* 当文本模块已保存且文本模块中的表达式不包含开放或闭合的表达式标记时，未显示错误消息。文本模块显示错误消息，并且无法在信件中呈现。NPR-17798
* 在安装加载项包的日志中出现意外错误。 NPR-18295

**表单管理器**

* AEM Forms UI 按照时间以升序（最早的排在最前面）列出所有资产。用户无法按照时间以降序（最新的排在最前面）重新排列资产。NPR-18451

### Forms JEE 安装程序  {#forms-jee-installer-14}

**输出服务**

* 改进了AEM表单的输出服务的性能问题6.2。NPR-18033

**签名服务**

* 无法使用远程硬件安全模块对PDF文档进行签名。 NPR-18017

## CFP6{#osgi-bundles-included-in-cfp-2}中包含的OSGi捆绑包

列表AEM 6.2SP1-CFP6中更新的OSGi捆绑包

[获取文件](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

列表AEM 6.2SP1-CFP6中更新的内容包

[获取文件](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP5是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 解决了共享、移动、发布和下载资产的几个UI问题。
* 增加了“移动”对话框在显示引用的资产时的容量。
* 解决了与WCM组件和工作流相关的几个问题，如取消发布和版本清除。
* 改进了操作栏在显示工具栏操作和Coral组件方面的响应性。

### 资产 {#assets-14}

* 发布到Brand Portal功能中的性能改进。 NPR-17189：适用于 CQ-4204150 的修补程序
* 使用共享链接选项共享资产不会创建具有平面文件夹结构的zip文件供下载。 NPR-17513：适用于 CQ-4209381 的修补程序
* 在DAM中选择资产并单击发布不会在资产详细信息页面中显示发布到品牌门户选项。 NPR-17351：适用于 CQ-94905 的修补程序
* 在DAM工作流步骤中，必须在最终块中关闭从会话或资源解析器获取的二进制流，以确保不发生资源泄漏。 NPR-17385：适用于 CQ-4209452 的修补程序
* 在DAM中上传Word文档会导致指针出现空异常，并且工作流实例仍卡在“正在运行”状态中。 NPR-17160：适用于 CQ-4207358 的修补程序
* 对于过期的资产，非管理员用户可以在元数据编辑器页面上看到共享、移动、发布和下载按钮。 NPR-16903;CQ-101440/CQ-104535的修补程序
* 对于管理用户，应在“资产”控制台中显示共享、移动、发布和复制等操作。 NPR-16902：适用于 CQ-4207111 的修补程序

### 站点 {#sites-14}

* 使用经典和触控UI移动页面时，“移动”对话框不显示超过150的引用，使用户无法更新这些引用并重新发布页面。 通过为经典UI引入属性，此问题已得到修复：可在siteadmin节点上配置的“maxRefNo”:“/libs/wcm/core/content/siteadmin”。 此属性指定在执行重量移动操作之前显示的最大引用数（默认值150）；如果页面的引用数较多，则不会在movePage对话框中显示这些引用。 此配置还适用于damadmin和miscadmin，方法是在节点上应用配置：`'/libs/wcm/core/content/damadmin'`和`'/libs/wcm/core/content/miscadmin'`。 NPR-17222：适用于 CQ-85878 的修补程序

* 使用WCM组件时，在触屏UI富文本编辑器中删除带空格的超链接。 NPR-17698、NPR-17570;CQ-4206768的修补程序
* 在从页面属性触发取消发布请求工作流时，对于没有复制权限的用户显示JavaScript错误。 NPR-17294：适用于 CQ-102064 的修补程序
* 渲染或导出HTL图像组件时，会将URL更改为数字，并重命名文件名，这会导致链接断开。 NPR-17245：适用于 CQ-59616 的修补程序
* 删除嵌套启动项中的启动项，会导致子启动项变得孤立。NPR-17228：适用于 CQ-4202639 的修补程序
* 在应用了Oak 1.4.13的AEM 6.2中运行版本清除会在日志中不断重复警告。 NPR-17391：适用于 CQ-4206870 的修补程序
* 为ContextHub组件安装修补程序或升级后，内容包将覆盖/etc/segmentation/contexthub中的所有区段，导致所有自定义ContextHub区段丢失。 NPR-17250：适用于 CQ-79958 的修补程序
* 在以工作流用户身份运行嵌套组的工作流时，WorkflowStatusProvider(pageinfo.json)会导致工作流实例锁定。 NPR-17555：适用于 CQ-4202056 的修补程序
* 使用WCM页面编辑器组件时，在创作实例的触屏UI编辑模式下，页面末尾存在大量空白空间。 NPR-17510：适用于 CQ-4205441 的修补程序
* 渲染或导出HTL图像组件时，URL会更改为数字，这会导致链接中断。 NPR-17245：适用于 CQ-59616 的修补程序

### UI {#ui}

* 在慢速连接中，选择资产并单击开发人员工具并不总是在操作栏中显示工具栏操作，并且必须重新加载页面。 NPR-17568：适用于 CQ-108365 的修补程序
* 操作栏应更新为使用两个容器:coral-actionbar-primary和coral-actionbar-secondary，而不是coral-actionbar-容器。 NPR-17591;GRANITE-15225的修补程序

### 按需移动{#mobile-on-demand-2}

* 对AEM Mobile应用程序具有“只读”权限的用户无法从AEM Mobile内容管理页面预览内容。 NPR-17390：适用于 CQ-4209690 的修补程序

### 安全 {#security-2}

* HTMLRendererServlet生成的输出中的XSS漏洞。 NPR-17136
* 请求防止AEM版本在AEM Web协同内容源页面中泄露。 NPR-16219

### 表单 {#forms-15}

#### Forms 附加组件包 {#forms-add-on-package-15}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

**自适应表单**

* 对于具有附件的自适应表单，在第二次提交表单时，将在提交的XML中创建afSubmissionInfo标记的重复项。 NPR-17364
* 使用Google Chrome浏览器时，从表单删除附件后，尝试重新附加同一附件会再次引发错误。 NPR-17297
* 如果基于XSD或基于No-Form模型的自适应Forms中存在嵌套的、可重复的延迟加载面板，则在表单中填充的值不会保留在记录文档(DOR)中。 NPR-17176
* 规则编辑器的错误日志中显示的错误应添加到try/catch块JavaScript代码的catch块中。 NPR-16757
* 单击表单中的文件附件会引发浏览器控制台错误，并且不显示附件预览。 NPR-17174

**通信管理**

* 创建对应UI功能将在UI中添加内联文本或空行时断开。 NPR-17748
* 打开字母进行编辑时浏览器闪烁。 NPR-17576
* 在计算数据字典元素中添加远程函数时，如果函数数大于显示远程函数的选项卡的长度，滚动条不会显示在选项卡中。 NPR-17359
* API方法导入com.adobe.icc.services.api.LetterInstanceService不起作用。 NPR-17922、NPR-16008
* 编辑字母时，在文本模块中添加的变量在“数据绑定”面板中不可见。 NPR-17940
* 当HTML提交操作使用POST方法时，不会启动对应管理UI。 NPR-17595

**表单管理器**

* 如果为AB测试配置了自适应表单，则单击开始AB测试不会开始测试，并会引发浏览器控制台错误。 NPR-17838

**表单服务**

* OSGI表单的静态代码分析中报告的问题应该得到解决。 NPR-13951

#### Forms JEE 安装程序 {#forms-jee-installer-15}

**输出服务**

* 与LiveCycleES4 SP1服务器对同一操作所花费的时间相比，使用AEM forms 6.2 Output Service将特定表单与数据XML合并所花费的时间要多20倍。 它已在Windows和Linux环境上修复。 NPR-17501

**安装 LCM**

* 安装AEM Forms6.2 GM构建并应用AEM 6.2 CFP后，运行的LiveCycle配置管理器会在版本信息中显示一个不需要的分号，并且修补程序安装日期不会更新。 NPR-14322

**进程管理**

* 没有为 AEM Forms 进程填充 TaskContext 变量。CQ-4211857

#### AEM FormsJEE捆绑包{#aem-forms-jee-bundles-package}

* 无论使用JEE管理员UI控制台还是OSGi控制台，表单用户的功能都应相同。 NPR-17670

### CFP5{#feature-packs-included-in-cfp}中包含的功能包

**FormsJEE包**

流程管理-HTML工作区

* 在分配工作区步骤时，如果有多个附件或附注，工作区附件选项卡应显示附件或附注的计数器。 NPR-17771
* 请求支持AEM JEEForms的Office 365，在表单工作流程中提供电子邮件功能。 NPR-13866

**Forms附加包**

通信管理

* 在字母预览期间在文本编辑器中编辑片段时，应显示已处理的文本以进行编辑，而不是显示片段中使用的内联条件。 NPR-15748、NPR-17504

### CFP5{#osgi-bundles-included-in-cfp-3}中包含的OSGi捆绑包

列表在AEM6.2 SP1-CFP5之间更新的OSGi捆绑包

[获取文件](assets/do-not-localize/cfp5_osgi_bundles.txt)

列表AEM 6.2 SP1-CFP5之间更新的内容包

[获取文件](assets/do-not-localize/content-package-cfp5.txt)

AEM Cumulative Fix Pack 6.2 SP1-CFP4是重要更新，包含自AEM 6.2 SP1正式上市以来发布的主要客户修复。

此累积修复包的主要亮点是：

* 针对Camera Raw文件再现、时间轴视图和图像方向的资产修复
* 改进功能

   * 为站点启动WCM
   * 项目工作流
   * ContextHub组件

* 活动、移动点播和翻译修复
* 自适应表单规则编辑器中的可用性改进
* 用于表单中对应管理的增强内嵌条件编辑器
* JEE上AEM表单的流程管理和输出服务修复
* Forms脚本编辑器相关修复

### 平台 {#platform-12}

* 配置云服务时，Search&amp;Promote搜索表单将忽略`environment`设置，使其在创作实例上不可用。 NPR-16594：适用于 CQ-4206076 的修补程序
* 在/apps中叠加向&#x200B;**资产OmniSearch**&#x200B;结果添加或自定义列不起作用。 NPR-16737：适用于 CQ-4206785 的修补程序
* 从AEM 6.1 SP2就地升级到AEM 6.2 SP1后， **诊断工具**页将无法工作。 NPR-17121：适用于 CQ-4196786 的修补程序
* HTL:在选择论坛、创建主题和帖子时，`Sightly SightlyCompiledScript`向`RequestDispatcherOption`添加不正确的`addSelectors`属性。 NPR-17008：适用于 GRANITE-16384 的修补程序

* 添加了`ReportImporter`使用的`ManagedPollConfigs`中对`CRON expressions`的支持。 NPR-16608:CQ-4206066的修补程序请求

* 为LDAP用户上传头像图像失败。 NPR-16561;Granite-17013的修补程序
* 在卡和列表视图中，“用户管理”屏幕上显示的结果数不同。 NPR-16241;GRANITE-16914的修补程序
* 在Google Chrome浏览器的“全屏”模式下查看时，工作流通知无法延迟加载。 NPR-17013：适用于 CQ-4207567 的修补程序

### 资产 {#assets-15}

* 在导入具有已定义方向的图像时，图像方向未正确应用。 NPR-16750：适用于 CQ-4204356 的修补程序
* 资产时间轴视图不显示任何资产，即使默认情况下已设置“显示全部”。 NPR-16957：适用于 CQ-98780 的修补程序
* 当将相机原始数据文件（包括ARW、CR2、NEF、DNG和EPS）添加为资产中的再现时，无法选择或删除这些文件。 当用户单击这些文件时，会自动下载这些文件。 NPR-16949：适用于 CQ-4206846 的修补程序
* 在资产UI中在另一个pdf中创建pdf不会在DAM UI中显示创建的pdf，但crx存储库中会显示这些pdf。 NPR-16833：适用于 CQ-4206501 的修补程序
* 使用触屏 UI 将资产上传为其自身的直接子节点会导致出现问题。资产会作为先前选定的资产的直接子级上传。NPR-16534：适用于 CQ-4204287 的修补程序
* 在DAM UI中，对资产进行注释并在评论中为用户添加标签不会生成邮件通知。 NPR-16589：适用于 CQ-102318 的修补程序

### 项目 {#projects-3}

在清除工作流时，“项目”工作流控制台在页面上显示NullPointerException。 NPR-17017：适用于 CQ-4194269 的修补程序

### 站点 {#sites-15}

* 在创作实例中，`ContextHub`中的文件不会最小化。 NPR-17022：适用于 CQ-79456 的修补程序
* WCM启动项提升需要很长时间才能提升包含页面大树的启动项。 NPR-16480：适用于 CQ-82731 的修补程序
* `ClientContext` 当使用非工作或未完成的规则创建区段(或受众)时，区段条件呈现器崩溃。NPR-16759：适用于 CQ-4205104 的修补程序
* 在WCM启动项中，当从触屏UI的页面属性中启动操作时，与启动项关联的页面不会取消发布。 NPR-16560：适用于 CQ-4204681 的修补程序
* 链接重写器错误地重写包含冒号的href值，假定冒号“:”定义JCR命名空间。 NPR-16753：适用于 CQ-4203762 的修补程序
* 在WCM-Design Importer中，打开测试导入程序页面并尝试上传zip文件会导致以前上传和删除的问题。 NPR-16486：适用于 CQ-90962 的修补程序
* 使用Firefox Safari和Google Chrome浏览器导航到&#x200B;**[!UICONTROL 全局导航]**&#x200B;窗格可提供不同的用户体验。 Firefox浏览器显示&#x200B;**[!UICONTROL 工具]**&#x200B;菜单，而Google Chrome浏览器显示&#x200B;**[!UICONTROL 导航]**&#x200B;菜单。 NPR-16770：适用于 CQ-4200456 的修补程序

### 营销活动 {#campaign}

* 测试AEM活动模板并修改种子地址以包含“附加数据”时，Adobe Campaign下拉框会在触屏UI Context Hub中消失。 NPR-16771：适用于 CQ-105748 的修补程序

### 移动点播{#mobile-on-demand-3}

* 当从AEM作者环境预检出版物时，超过5秒的预检操作会在AEMM上引起异常尖峰-AEM PECS Integration在仪表板上以每秒的高状态请求数显示。 NPR-16908：适用于 CQ-4207055 的修补程序
* 安装AEM-6.2-SP1-CFP1-1.0更新后，AEM Mobile配置管理将失败。 NPR-16909：适用于 CQ-4204892 的修补程序

### 翻译 {#translation-7}

* 在安装6.2 SP1 - CFP1后，预览转换作业不起作用。 NPR-16481：适用于 CQ-4204655 的修补程序
* 使用“翻译”创建的语言副本指向“根主控”而不是本地国家／地区Live Copy。 NPR-17257：适用于 CQ-4208287 的修补程序

### 安全 {#security-3}

* 将文件的二进制文件上传到AEM时，不执行MIME类型验证。 NPR-16617
* 上传 LDAP 用户的头像图像时出现问题。NPR-16561

### 表单 {#forms-16}

#### Forms 附加组件包 {#forms-add-on-package-16}

**自适应表单**

* 在自适应Forms编辑器中，head.jsp中的目标设置注释应替换为新的Context Hub语句。 NPR-17173
* 在自适应Forms规则编辑器中，**[!UICONTROL 选择项]**&#x200B;将事件显示为“null”。 NPR-17139
* 使用前进箭头(>)向前导航时，提交的表单将重新提交。 NPR-17080
* 通过AJAX提交自适应表单时，在出错时不调用“error”回调函数。 NPR-17034
* 在运行时在规则编辑器中单击&#x200B;**[!UICONTROL 保存表单]**&#x200B;按钮不会保存表单。 NPR-16905
* 静态文本应排除在自适应表单的跳位顺序之外。 NPR-16749
* 小数字段的计算值显示不正确。 NPR-16596
* 显示帮助内容的图标应包括在自适应表单的Tab键顺序中。 NPR-16484
* 支持在“ **[!UICONTROL 默认预填服务配置]**”中使用类型为`dataRef=C:/Users/`的常规表达式，以预填自适应Forms的数据。 NPR-16425

* 如果存在嵌套的延迟加载方案，则无法正确触发所有面板的验证。 NPR-15821

**通信管理**

* 如果字母包含空文本模块（一个没有文本的模块），字母再现将失败。 NPR-17054
* 在文本编辑器中粘贴后，换行符和制表符空格将从内容中删除。 NPR-17039
* 如果文本模块以多个字母进行引用，则文本模块的引用显示将花费大量时间。 NPR-17035
* 编辑、保存、删除和设置文档片段的引用需要很长时间。 NPR-17033
* 预览字母时，两端对齐的文本将以其他字体呈现。 NPR-16976
* 如果搜索的文本有多个实例，则搜索功能无法正常工作。 NPR-16920
* 文本编辑器工具栏间歇性地显示在浏览器中。 NPR-16919
* 从规则编辑器中保存表单&#x200B;**[!UICONTROL 构造无效。]** NPR-16905
* 在使用Internet Explorer创建基于数据字典的文本模块时，“字体”下拉框不填充字体系列。 NPR-16944
* 创建文本片段后，预览字母时字母字体会发生变化。 NPR-16830
* 文档片段中开头或表达式之间带制表符空格的字母无法呈现或预览。 NPR-16769

**移动Forms**

* 移动表单预览显示重叠的内容，但表单可正确显示以进行PDF渲染。 NPR-17105

**Forms门户**

* 单击已提交表单的&#x200B;**[!UICONTROL 下载]**&#x200B;链接可打开HTML页面而不是PDF表单。 NPR-17082

* `Upload Comments` 对于已提交的实例，文件附件不会显示在UI中，尽管它们存储在crx存储库中的XML中。NPR-17075

**Reader扩展服务**

* 特定文件未在AEM forms OSGI安装时ReaderExtended。 NPR-16625

#### Forms JEE 安装程序  {#forms-jee-installer-16}

**核心**

* 在升级过程中，Configuration Manager会因超时而失败。 NPR-16774（请参阅[配置组件级操作的超时](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)）。

**流程管理- HTML工作区**

* 开始任务的起始点不以提交起始点时提交的数据开头。 NPR-16917
* 单击HTML工作区中表单的&#x200B;**[!UICONTROL 返回]**&#x200B;按钮不会关闭表单，但会将其返回到组队列。\
   NPR-16352

**进程管理**

* 允许用户将以前任务的显示名称设置为进程实例中的任何下一个任务。 NPR-15382

**输出服务**

* 输出服务无法处理PDF，该PDF被修改为在`date-time format`元数据中包含额外的“milli-sec”字段。 NPR-16838

#### Forms Designer {#forms-designer}

* AEM设计器脚本编辑器不遵循`Calculate Event`和`Validate Event`的“表单属性”默认值。 NPR-15921

### CFP4{#feature-packs-included-in-cfp-1}中包含的功能包

**Forms附加包**

* 在内联条件编辑器中用于通信管理的增强。 NPR-10981

### CFP4{#osgi-bundles-included-in-cfp-4}中包含的OSGi捆绑包

在 AEM 6.2 SP1 与 CFP4 之间更新的 OSGi 包列表

CFP3的主要亮点是：

* 对经典UI和AEM Search组件（使用带摘要身份验证的代理）提供更高效的搜索功能
* 修复了上传资产和显示资产元数据时的问题
* 修复了在标题具有特殊字符时创建文件夹和移动页面时出现的问题。
* 修复了在触屏UI中使用定位同步受众、发布活动和选择目标量度的问题
* 解决了翻译作业的同步问题
* 为Forms预填服务提供增强的安全性
* 改进了表单门户草案和提交部分以及巴克德Forms服务
* 对包含文件附件构件或延迟加载片段的自适应表单的可用性改进。
* 通信管理中的可用性改进包括增强的搜索功能、删除的资源的记录和导入数据字典。

### 平台 {#platform-13}

* **ModelAdapterFactory**&#x200B;中的竞态条件（当两个线程尝试注入相同字段时可能）导致无法构建模型。 NPR-16443:SLING-6584的修补程序
* 包管理器中的验证选项，用于检测/apps下叠加的文件（JSP或JavaScript文件）与/libs下的修补程序中包含的文件（JSP或JavaScript文件）之间的任何冲突。 然后，可以重新基于受影响的叠加，以在/libs下包含来自文件的更改。 NPR-16216：适用于 CQ-81729 的修补程序
* 登录error.log有时会在启动发布者后几秒钟内停止，需要清除才能再次运行。 请求更新日志记录框架并提供Sling日志记录。 NPR-15913：适用于 Granite-15452 的修补程序
* 请求更新JavaScript &quot; `use"` API以避免在HTL JavaScript Use API实现中失败。 NPR-16461:SLING-6780的修补程序

### 站点 {#sites-16}

* 从AEM 6.0升级到AEM 6.2后，经典UI由于大量查询而在搜索标记时显示较慢的性能。 要解决此问题，可以执行[在标记控制台（经典UI）](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr)中禁用复制状态下所述的步骤。 NPR-15842：适用于 CQ-4201748 的修补程序.

* 在触屏UI中创建页面时，“name”的输入检查字段不检查特殊字符“撇号”（与经典UI中相同）。 因此，无法移动页面。 NPR-16404：适用于 CQ-4205321 的修补程序.
* 在富文本编辑器中对两行应用不同样式，然后合并它们将删除对第二行应用的样式。 NPR-16389：适用于 CQ-4203835 的修补程序.
* 在“触屏UI站点”屏幕中，尝试将页面粘贴到没有子页面的页面中时，无法正常工作，因为不显示“粘贴”按钮。 NPR-15894：适用于 CQ-4201696 的修补程序.
* 在内容查找器面板中滚动“页面”选项卡时，经典UI中会无限显示几组页面，而触屏UI则显示有限的少数非重复页面集。 NPR-16271：适用于 CQ-4202371 的修补程序
* 在触屏UI中打开LiveCopy的页面属性并单击保存（不进行任何更改）会写下任何LiveCopy选项卡并创建一个LiveSync配置节点。 NPR-16327：适用于 CQ-108562 的修补程序
* 表单约束无法读取`ConstraintMessage`属性。 NPR-16388：适用于 CQ-101330 的修补程序
* `wcm/foundation/components/parsys`组件不显示&#x200B;**[!UICONTROL “将组件拖动到此处]**”占位符。 NPR:16748:CQ-4205187的修补程序

### 资产 {#assets-16}

* 在安装6.2 SP1或修补程序12430后，pdf光栅器停止工作并导致内存不足问题。 NPR-15991
* 字符串属性`documentNumber`的元数据显示为日期，而它应为数字。 NPR-16134：适用于 GRANITE-16916 的修补程序
* 时间轴事件球标中的文本截断。 NPR-16226：适用于 CQ-85226 的修补程序
* 在内容层次结构下创建标题具有特殊字符的文件夹时，将显示特殊字符的编码形式。 NPR-15935：适用于 CQ-4202987 的修补程序
* 由于使用“创建”按钮时显示的行为不一致，用户在浏览资产时无法上传资产或创建文件夹。 NPR-16410：适用于 CQ-4204793 的修补程序
* 在AEM创作中从文章视图上传共享的HTML资源时遇到意外错误。 NPR-16133:AEMM-4155970的修补程序

### 集成 {#integration-14}

* 在使用摘要身份验证启用代理身份验证时，AEM Search组件将引发ConcurrentModificationException。 NPR-15309：适用于 CQ-4199191 的修补程序
* 在AEM中创建目标A/B测试活动时，受众不同步到目标并显示“无受众”。 NPR-16229：适用于 CQ-4204210 的修补程序
* 在安装SP1+NPR-11577 v1.2后，当在TouchUI中定位时为目标度量选择“使用分析度量”时，从不加载度量的下拉列表。 NPR-16129：适用于 CQ-4204316 的修补程序
* 使用定位时，发布活动不会自动发布整个树，包括品牌和主控。 NPR-15855：适用于 CQ-94630 的修补程序

### 翻译 {#translation-8}

* 同步转换作业不会自动触发，而AEM轮询不会在不戳翻译项目的情况下发生。 NPR-15163：适用于 CQ-90856 的修补程序

### 表单 {#forms-17}

#### Forms 附加组件包 {#forms-add-on-package-17}

**自适应表单**

* 在保存带有附件的自适应表单时，附件的完整路径将添加到生成的XML的`fileAttachment`标签中，而不是添加附件的名称中。 NPR-16529
* 在基于XDP的自适应表单中，提交的XML中存在`afData/afBoundData`包装器，即使预填XML中也没有`afData/afBoundData`包装器。 NPR-16118

* 数字字段中的指数表示法：在使用自适应表单时，如果输入的小数分数超过十个字符的数字总数，则该数字在提交的XML中将变成指数表示法。 NPR-16106
* 对于同时包含文件附件组件和延迟加载片段的表单，提交的数据xml不包含文件附件组件的信息。 NPR-16022
* 对于没有可重复祖先的延迟加载的可重复面板，在面板的第二个实例中的可重复子项无法重复。 NPR-15944
* 当尝试在表单编辑器中将片段保存在片段内时，片段模型根不填充子片段的值。 NPR-15943
* 创建仅包含一个项目的复选框并尝试显示保持项目标题隐藏的复选框标题时，如果项目文本为空，则创建字典操作将引发`ArrayIndexOutOfBoundException`。 未创建字典，且屏幕上未生成错误响应。 NPR-15816
* 对于带有文件附件构件的自适应表单，在预览附加的文件后，表单的某些部分将被禁用。\
   NPR:16611

* 对于允许多个附件的文件附件构件，如果在具有前一个附件的构件上提交了具有附件的新表单实例，则打开添加的附件时将显示错误代码，而不是实际内容。 NPR-16258
* 通过`file://`、`http://`和`ftp://`等协议保护表单预填服务免遭未经授权的访问。 请参阅“使用Configuration Manager[配置预填服务。” ](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)NPR-15414

* 请求在“验证”步骤中以PDF格式而不是HTML格式呈现自适应表单，并将所有附件追加到PDF，以便打印输出显示完整表单。 NPR-9011

**通信管理**

* 在“预览/编辑”模式下处理字母中的文本片段时，如果文本转换为列表，则整个字母功能将断开，并生成JavaScript错误。 NPR-16460
* 每次上传XSD并选择根节点时，浏览器变得无响应，导入XSD文件以在“Corresponce Management”（对应管理）节点中创建数据字典时会失败。 此问题与浏览器无关，不显示在服务器日志中。 NPR-16452
* 在使用Internet Explorer浏览器预览字母并尝试编辑内容的字体大小时，重复值从8到72显示在字体大小下拉列表中。 NPR-16387
* 如果浮动字段显示为XDP片段的输入字段，则在使用Internet Explorer浏览器时，该字段不会在字母预览中展开。 NPR-16367
* 当尝试直接从预览提交信函时，由于隐藏，字母名称的弹出窗口无法正确显示。 NPR-16353
* 编辑字母时添加的行空格不会反映在预览窗口中。 对于文本片段中的列表,PDF输出不显示正确的间距。 NPR-16267
* 使用Internet Explorer浏览器处理文本文档片段时，尝试为文本提供缩进失败，因为光标不允许文本缩进。 NPR-16128
* 向现有文本文档片段添加或修改数据字典需要很长时间，并且不会始终通知用户。 NPR-16102
* 使用Internet Explorer浏览器预览具有可滚动内容的字母时，浏览器滚动条与字母的滚动条重叠，并且无法查看右侧片段的整个内容。 NPR-16068
* 使用Google Chrome浏览器创建或编辑文本文档片段时，颜色选择下拉列表会自动弹出，并且无法删除。 用户需要选择列表作为数据条目类型才能编辑片段。 NPR-16067
* 使用Letterinstance API时，方法`import com.adobe.icc.services.api.LetterInstanceService`不起作用。 NPR-16008
* 在资产书写器配置中将日期显示格式更改为`locale=en_US; dateFormat=MMM dd,yyyy;`不能按预期工作，日期格式将显示为垃圾邮件字符。 NPR-16007
* 重新创作时，即使之前设置的方式不同，数据链接类型也会显示为“用户”。 NPR-16619

**Forms门户**

* 草稿和提交组件的升级方案与数据库示例实施无关。 NPR:16752

**巴科德Forms局**

* BarcodedForms服务(BCF)的静态代码分析报告问题。 NPR-13855

#### Forms JEE 安装程序  {#forms-jee-installer-17}

**流程管理- HTML工作区**

* 通过“file://”、“http://”和ftp://等协议保护表单预填服务免遭未经授权的访问。 有关详细信息，请参阅[使用Configuration Manager](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)配置预填服务。 NPR-15434

**用户管理 **

* SAML登录屏幕在AEM 6.2服务器上显示不当版本(6.1.0)。 NPR-13825
* 如果为AEM Forms配置了单点登录(Kerberos)身份验证，则如果用户身份验证在尝试登录时失败，则返回错误代码“404”。 用户仅在刷新页面后才会被重定向到登录站点。 NPR-15015

#### Forms设计师{#forms-designer-1}

* 在AEM Forms设计器中，将词典拼写检查中的表单区域设置更改为法语（加拿大）不起作用。\
   NPR-15896

### CFP3{#feature-packs-included-in-cfp-2}中包含的功能包

**Forms附加包**

* 在通信管理中删除任何资产时，error.log文件中应记录一条警告消息。 NPR-13225
* 在对应管理中预览字母时增强搜索功能，以启用文本片段内容中的文本搜索，而不是只搜索字母标题或标签。 NPR-16103

### CFP3 {#osgi-bundles-included-in-cfp-5}中包含的OSGi捆绑包

在 AEM 6.2 SP1 与 CFP3 之间更新的 OSGi 包列表

[获取](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
文件Cumulative Fix Pack 2的主要亮点是：

* AEM平台中的稳定性修复和性能改进，包括Sling框架和操作
* 改进了资产管理，并修复了多个用于访问、移动、搜索、上传和发布资产的修复
* 借助内容片段、锚点插件、幻灯片和Context Hub组件中的修复功能改进网站的创作和管理
* 触屏UI中的多个修复，包括文本编辑器、Omnisearch和变体创建过程
* 改善翻译工作流;增强的Microsoft连接器，用于为Azure门户使用新的翻译API
* 项目和活动中的修复
* 借助自适应表单、通信管理和表单门户功能中的修复功能改进创作和管理
* FormsJEE核心、XTG和HTML工作区组件中的修复

### 平台 {#platform-14}

* 如果编辑了直接引用Sling Framework的页面，则会触发`SlingPostProcessor`。 NPR-15754：适用于 CQ-104153 的修补程序

* 导航到页面组件时，在经典UI对话框中不会获取具有`tagBasePath`属性的标记的值。 NPR-15543：适用于 CQ-4199950 的修补程序

* 执行Sling操作时，如果有一个名为“chunk_n_n-1”的块`SlingFileUpload handler.getLastChunk`，则会进入一个包含空块的循环。 NPR-15455:SLING-5701的修补程序

* 当接口扩展另一个接口时，超级接口上的可注射方法不能正确注入。 NPR-15202:SLING- 5710的修补程序
* 使用`com.adobe.granite.infocollector.impl.FilesTraversal`函数调用时，不会阻止潜在的空指针异常。 NPR-15169：适用于 CQ-4197640 的修补程序
* 某些辅助节点的工作流状态不一致，调度该节点的观察事件时显示错误。 NPR-15701：适用于 GRANITE-13786 的修补程序
* 当用户选择CRXDE中的节点（例如/content/dam/），然后选择“访问控制”选项卡时，确保存在访问控制列表，拖放某些元素会移动除所选元素之外的元素。 NPR-15696 GRANITE-16300的修补程序
* 在尝试模拟时从下拉列表中选择用户会导致整个用户弹出窗口消失。 NPR-15774:适用于CQ-4201738/GRANITE-11895的修补程序
* 在Omnisearch中，按标记搜索自动填充的建议不起作用。 NPR-15088：适用于 GRANITE-14426 的修补程序.\
   注意：此修复需要Oak CFP 1.4.11或更高版本。

### Mobile AEM作者{#mobile-aem-author}

* 将AEM Mobile和ContentSync包与混合应用程序一起使用时，AEM会响应由应用程序发出的读取请求（带有时间戳），该请求由最早的包而不是应用程序所请求的包。 NPR-15749：适用于 CQ-104153 的修补程序

### 站点 {#sites-17}

* 如果用户在激活工作流后修改页面，则WCM核心中工作流收件箱的修改状态不会更改。 NPR-15684:CQ-4196974的修补程序
* 当用户单击锚点图标并添加名称时，触屏UI的富文本编辑器中的锚点插件会生成不符合标准的HTML5。 它应在锚点元素的HTML5标记中添加“id”属性，而不是“name”属性。 NPR-15650：适用于 CQ-89782 的修补程序
* 创建具有大量字段的元数据模式并将其应用于内容片段元数据时，内容片段元数据屏幕上不会创建滚动条，使这些字段不可编辑。 NPR-15478：适用于 CQ-4202622 的修补程序
* 编辑`TagInput`字段组件不会显示之前针对对话框字段配置的值。 NPR-15464:适用于CQ-4200360的修补程序

* 在内容片段编辑器UI中，如果创建了内容片段的许多变体，则侧面板不会显示滚动条以导航所有变体。 NPR-15445:适用于CQ-4199444的修补程序
* 从直接用户组中删除用户后，会将其添加到继承的用户组。 NPR-15400：适用于 CQ-98758 的修补程序
* WCM创作：触屏UI作者不允许编辑名称中带有逗号的页面。 NPR-15396：适用于 CQ-4199723 的修补程序
* 使用触控UI进行创作时，函数`Granite.author.editableHelper.doSelectParent`以错误的顺序传递参数，导致JavaScript错误。 NPR-15349：适用于 CQ-4198594 的修补程序
* ContextHub区段显示体验，即使存在退出Cookie也是如此。 NPR-15293：适用于 CQ-4198024 的修补程序
* 经典UI中的幻灯片放映组件无法创建幻灯片或拖放图像以创建新幻灯片。 NPR-15281：适用于 CQ-4194164 的修补程序
* 在站点管理控制台中，用户将显示“创建”选项，如“创建页面”、“创建站点”、“创建Live Copy”、“创建启动项”和“创建目录”菜单项。 NPR-15278：适用于 CQ-94436 的修补程序
* 安装AEM 6.2 Service Pack 1后，“包括子页面”滑块停止用于页面启动。 NPR-15230：适用于 CQ-4198449 的修补程序
* 请求增强版本清除功能，以块形式提取和处理版本，还能将指定路径用于XPath查询。 NPR-15186：适用于 CQ-109205 的修补程序
* “站点”组件的“页面属性”缩略图选项卡上缺少“清除”按钮。 NPR-15143：适用于 CQ-4196997 的修补程序
* 对于使用Live Copy的站点，在siteadmin控制台的“列”窗格中选中“Live Copy”复选框不会正确显示Live Copy状态，只显示HTML标记。 NPR-15108：适用于 CQ-97086 的修补程序
* 在编辑内容片段时，如果用户在收到帖子响应之前单击完成编辑操作(“√”)，则无法正确保存已编辑的内容。 NPR-15014：适用于 CQ-4194095 的修补程序
* 在“时间扭曲”模式下关闭“编辑”页面并尝试从Siteadmin重新打开它会导致状态为“500”的错误，而不是重新打开页面。 NPR-14965：适用于 CQ-109647 的修补程序:
* 在数字资产管理器(DAM)UI中，用户选取器查找可授权内容搜索会导致“内存不足”异常。 NPR:15307:CQ-98542的修补程序

### 资产 {#assets-17}

* 在Omnisearch中搜索资产后，选择资产并尝试通过单击“视图属性”来编辑属性，然后单击“保存”按钮将用户重定向到空白页面。 NPR-15900：适用于 CQ-4202372 的修补程序
* 资产用户界面不响应事件。 选择资产并单击“发布”或“演绎版”不会导致任何活动。 NPR-15828：适用于 CQ-4202247 的修补程序
* 从卡片视图发布资产时，除非刷新页面，否则卡片不会更新为反映已发布状态。 NPR-15826:适用于CQ-102732的修补程序
* 包含资产修补程序的累积修补程序。 NPR-15225
* 如果资产文件夹的名称中包含&amp;符(“&amp;”)字符，则在导航到资产时，文件夹名称不会正确显示。 NPR-15775：适用于 CQ-4201735 的修补程序
* 在资产文件的名称中使用&amp;符(“&amp;”)字符会导致在访问其属性时出现问题。 NPR-15770：适用于 CQ-4201737 的修补程序
* 在导航资产和使用“列视图”显示模式时，如果用户在选择并单击资产后刷新页面，则会显示资产详细信息，而非刷新的内容。 NPR-15768：适用于 CQ-4201727 的修补程序
* PDS摄取借助用于pdf服务的库堆，占用100%的CPU利用率。 NPR-15606适用于GRANITE-12929的修补程序
* 使用Firefox浏览器访问“我的链接共享”UI时不显示共享项目或用户，并且屏幕不可用。 NPR-15539:CQ-4200992的修补程序
* 在使用数字资产管理器时，如果某个页面与一组图像相关联，则将图像移动到新文件夹会中断页面关联，而关联的页面会忽略一些图像。 NPR-15538：适用于 CQ-111479 的修补程序
* 在Dam Viewer组件中，使用“nosamplecontent”运行模式会导致Dynamic Media出错。 NPR-15449：适用于 CQ-4195425 的修补程序
* 在创建视频用户档案时，如果同时选择了高质量和中等质量的视频编码预设，则不会保存所做的更改。 NPR-15447：适用于 CQ-4195482 的修补程序
* 即使由于服务器错误响应而将资产上传到Brand Portal失败，状态也会在Brand Portal UI中更新为“已发布”，因此很难跟踪丢失的文件。 NPR-15442：适用于 CQ-4197968 的修补程序
* 将资产文件夹发布到Brand Portal时，在发布时间超过一小时，某些文件无法发布。 NPR-15441：适用于 CQ-4199493 的修补程序
* 在列视图中使用资产查找器控制台时，尝试创建文件夹失败一次，但成功重试。 NPR-15370：适用于 CQ-4199448 的修补程序
* 如果在DAM UI中选定的资产或文件夹名称中带有逗号，则“引用”选项卡将不可用，并显示一条消息“引用列表不适用于多个选择”。 NPR-15362：适用于 CQ-4199721 的修补程序
* 将文件夹发布到Brand Portal不会更改文件夹的已发布状态，即使文件夹下的资产已成功发布也是如此。 NPR-15292：适用于 CQ-4197667 的修补程序
* 在触屏UI中导航到资产控制台时，激活某些资产时会出现异常，如所示。 NPR-15217:CQ-108779的修补程序
* 当连接通过代理服务器时，将视频发布到Youtube。 NPR-15109:适用于CQ-110332的修补程序
* 使用名称包含点或句点(.)的资产 在数据密钥资源中，不解析到同一资产，输出路径在点处终止。 NPR-15069：适用于 CQ-4195914 的修补程序
* 将AEM 6.2升级到Service Pack 1后，将资产同步到Scene7失败。 dam:Scene7FileStatus属性显示“ `UploadFailed`”状态，即使对于已发布的资产也是如此。 NPR-15269：适用于 CQ-4197708 的修补程序

### 用户界面 {#user-interface-5}

* 在&#x200B;**[!UICONTROL 触控UI]**&#x200B;中，对于使用Internet Chrome浏览器版本56.0.2924.87时不具有type=&#39;datetime&#39;的日期字段，不显示保存的日期。NPR-15383:GRANITE-16481的修补程序
* 在&#x200B;**[!UICONTROL 触控UI]**&#x200B;中，富文本编辑器在呈现线程和题注元素时从HTML表中删除它们。 NPR-15267：适用于 CRTE-41 的修补程序
* `FileUpload Validator` 当autostart为true或手动调用并在这些情 `uploadFile()` 况下生成无效验证报告时，不处理这些情况。NPR-15295：适用于 GRANITE-13499 的修补程序

* Omnisearch不允许使用/apps的客户添加列数据源，因为它假定位置配置列在&#x200B;*/libs/granite/omnisearch/content/metadata/*&#x200B;下。 NPR-13188 GRANITE-16479的修补程序
* 使用&#x200B;**[!UICONTROL 触控UI]**&#x200B;时，产品变体的创建级别与产品不同。 未通知用户变型创建过程的状态。 NPR-15345:CQ-4198948的修补程序

**Scene7**

* 运行Scene7工作流会导致打开的文件不关闭。 请求改进AEM-S7服务，以便维护和重用具有共享池配置的单个HttpClient实例。 NPR-15357:CQ-109958的修补程序

### 翻译 {#translation-9}

* 使用翻译项目时，从英语主控更新语言副本，将生成11个单独的启动项，所有启动项的名称和源根目录相同，但启动项根目录稍有不同，以防页面名称遵循设置模式。 NPR-15605：适用于 CQ-4200699 的修补程序
* 当语言根的名称中包含连字符和短划线时，不会为页面创建翻译项目。 NPR-15171:CQ-96286的修补程序
* 请求更新Microsoft连接器以能够使用Microsoft Translator API,Microsoft在Azure门户中提供这些API。 NPR-15320：适用于 CQ-101010 的修补程序

### 项目 {#projects-4}

* 只有20个不活动项目显示在项目屏幕中，但存储库中存在20多个不活动项目。 NPR-15656：适用于 CQ-4200903 的修补程序

### 营销活动 {#campaign-1}

* 在使用活动-定位和MAC —— 测试和目标集成组件时，取消发布活动不会更新主控UI中的活动状态。 NPR-15401:CQ-4199839的修补程序
* 在AEM Commerce中移动产品时，产品移动向导会忽略产品名称、标题、引用页面、创建作者和创建日期的预填值。 NPR-15228：适用于 CQ-98617 的修补程序

### 安全 {#security-4}

* 使用GET方法添加到表单的CSRF令牌参数。 NPR-15229

### 表单 {#forms-18}

#### Forms 附加组件包 {#forms-add-on-package-18}

`**Adaptive Forms**`

* 使用输入XML预填充自适应表单时，默认值会被xml中的空值覆盖。 NPR-15721
* 提交的XML中存在`afData/afBoundData`包装器，但即使预填XML在基于XML模式的自适应表单中也没有`afData/afBoundData`包装器。 NPR-15541

* Accordion栏中的标题应为可编辑的HTML“h2”标题，而不是“a”标记。 NPR-15475
* 屏幕阅读器用户无法访问表单面板的折叠布局。 用户无法使用屏幕阅读器软件（如JAWS或NVDA）单独通过键盘导航到折叠选项卡。 NPR-15474

`**Correspondence Management**`

* 保存、删除和设置文档片段的引用需要大量时间。 NPR-15939
* 在CCR UI中，在管理资产中设置的选项卡对齐方式包含多个标题。 NPR-15818
* 文本模块的缩览图不显示对齐的内容，但文本包含使用Google Chrome中的选项卡创建的对齐内容。 NPR-15819

`**Forms Portal**`

* 预填服务不适用于XDPForms。 NPR-15466
* 当将自适应表单草稿和提交到数据库时，当数据库连接因任何原因（例如，长时间不活动后）而失败时，自适应表单的状态将损坏。 NPR-15297

#### Forms JEE 安装程序  {#forms-jee-installer-18}

`**Core**`

* 升级到Java 1.8.0_121-b13的最新版本后，AEM Forms无法访问管理员用户界面。 NPR-15330

`**XTG**`

* 使用输出服务将特定表单与数据xml合并时，响应时间是ES4 SP1服务器对同一操作所花费时间的20倍。 NPR-15283

#### AEM Forms 应用程序 {#aem-forms-app-1}

* 恢复未保存的任务时，恢复未保存的任务时显示的消息需要更清晰，以减少用户错误。 NPR-15377
* AEM Forms应用程序不渲染通过自定义模板创建的表单。 NPR-15892
* 用户无法登录AEM Forms应用程序。 NPR-15891

AEM 6.2 SP2-CFP1的主要亮点是：

* 简化站点中的复制功能：

   * 对各种转出、LiveCopy和写入错误问题的修复

* 在以下期间增强触屏UI响应：

   * 资产搜索
   * 基于大小的排序

* 增强智能集合中的标签管理
* 在对文件夹执行CRUD操作期间，访问控制更紧

### 平台 {#previous}

* 请求在复制代理启动期间删除`ReplicationQueue#forceRetry` API调用，因为此类调用会显着减慢实例的运行速度，尤其是当它有许多复制代理时。 NPR-14032：适用于 GRANITE-13095 的修补程序
* 请求`DurboImportConfigurationProviderService` OSGi配置以支持可存储一组值的字段。 NPR-14570：适用于 CQ-108684 的修补程序
* 迁移到AEM 6.2后，在页面中使用Sightly组件会导致页面的“属性”对话框停止工作。 NPR-14328：适用于 CQ-108355 的修补程序
* 取消调度以前调度的作业不会删除&#x200B;*/var/eventing/scheduled-jobs*&#x200B;下的相应节点。 NPR-14253:SLING-5666的修补程序
* 当管理员尝试模拟为已删除的用户时，用户界面将无法刷新。 NPR-14247：适用于 CQ-107446 的修补程序
* XSS保护检查导致Sightly组件中的编码不正确。 NPR-14004：适用于 CQ-93821 的修补程序
* 请求将Jackrabbit Filevault升级到3.1.30以解决多个问题。 NPR-13454
* 当Sling分发将分发包从作者同步到发布时，会发生缓存错误。 NPR-13034：适用于 GRANITE-13970 的修补程序

### 站点 {#sites-18}

* VersionManager的问题从版本历史记录中清除错误版本。 NPR-14372
* WCM Sightly Foundation parsys组件忽略组件声明标签名称`cq:htmlTag / cq:tagName`。 NPR-14225
* 在触屏UI中，当使用Sightly Parsys渲染通过JavaScript插入的组件时，刷新页面后将忽略自定义装饰。 NPR-14122
* 目标下拉列表列表在创建多个富文本字段（如链接）时，在触屏UI对话框中不起作用。 NPR-13911
* 在对话框（触屏UI）中编辑具有多个富文本编辑器(RTE)属性的文本字段时，焦点会随机转移到特定RTE属性。 NPR-13703
* 默认现成视频组件不渲染视频缩略图。 NPR-14976
* 信息缓慢加载到模板编辑器的“实时使用实例”选项卡中。 NPR-14880：适用于 CQ-83417 的修补程序
* 在AEM 6.2实例上安装修补程序-10936将禁用iparsys组件。 NPR-14330：适用于 CQ-106982 的修补程序
* 迁移到AEM 6.1 SP1后出现多个转出组件问题和Live Copy问题。 NPR-15256
* 即使对于多个转出配置，页面转出操作也无法创建超出一级的子项。 NPR-15055
* 从编辑器提交PageProperties对话框时，LiveCopy选项卡中未更改的数据将被重写。 NPR-14693
* 当从编辑器提交PageProperties对话框时，MSM后处理器会从请求中写入一些参数，而不是`msm:writeLiveCopyConfig`参数。 NPR-14434
* 与转出组件、Live Copy和MSM的其他方面相关的多个问题。 NPR-12235

### 资产 {#assets-18}

* UnPack工作流无法处理图像文件名称中具有特殊字符的图像。 NPR-15227：适用于 CQ-103887 的修补程序
* 具有条件重复表达式的资产无法正常显示。 当用户预览`*CDN3835RLCEN*`字母模板时，不会显示位于“正文”目标区域中的任何资源。 当资产`*VIPReassement*`（是可选资产）处于未选中状态时，将在字母中显示预先选择的其他资产。 NPR-14844

* 创建智能收藏集时，保存智能收藏集时不保留样式标签。 NPR-15081：适用于 CQ-4195494 的修补程序
* 在多个用户进行并发搜索期间，资产搜索查询在触屏UI中运行缓慢。 NPR-15019:CQ-4195405的Hotifx
* 当原始资产重新上传到其他位置时，为类型`Long[]`的属性提取的元数据将转换为类型`String[]`。 NPR-15016:CQ-4195005的修补程序

* 用户无法删除保存的搜索或智能收藏集。 NPR-14924：适用于 CQ-108494 的修补程序
* 在基础元数据模式的下拉字段中使用TypeHint的布尔值，批量（追加模式）编辑资产的元数据时，会生成错误。 NPR-14529：适用于 CQ-106876 的修补程序
* 没有复制权限的用户无法删除资产文件夹。 NPR-14321：适用于 CQ-88271 的修补程序
* 当尝试在渠道编辑器中编辑视频的视频用户档案时，设计对话框不打开，并在错误日志中引发空指针异常。 NPR-14144：适用于 CQ-81101 的修补程序
* 资产的属性页面中显示的系统生成的“已创建”时间戳属性不正确。 NPR-13992：适用于 CQ-95029 的修补程序
* 请求在AEM AssetsNPR-13851中为无读取访问权限的用户启用重复资产检测：CQ-102281的修补程序
* 用户无法从属性页面批量编辑资产的元数据。 NPR-13721：适用于 CQ-100703 的修补程序
* 上传重复资产时经典UI中的错误消息不正确。 错误消息不指示上载失败的原因。 NPR-13691：适用于 CQ-99272 的修补程序
* AEM Assets无法在列表视图中按大小一次对超过50个资源进行排序，当文件夹包含大量资源时。 CQ-100588
* 如果资产／文件夹URI太长，则选择多个资产会引发响应代码为414（请求-URI太长）的错误。 NPR-13516：适用于 CQ-76076 的修补程序
* 当用户在“配置列”对话框中选择所有选项时，“资产报告”页面会变得无响应。 NPR-13187：适用于 CQ-95589 的修补程序
* Safari和Internet Explorer中的标记选取器出现意外行为。 NPR-13134
* 通过编辑“资产管理员搜索”边栏中保存的搜索，可将其保存为嵌套的智能选择，这会导致环境稳定性问题。 NPR-13119：适用于 CQ-99460 的修补程序
* 移动文件（或文件夹）然后重命名它后，“cq:name”元数据不反映新文件名（文件夹名称）。 NPR-13036：适用于 CQ-99141 的修补程序
* 名称中包含特殊字符的资产无法从通过电子邮件共享的下载链接下载。 NPR-12872：适用于 CQ-95795 的修补程序
* 当资产数量很大时生成的现成资产报表会导致大量遍历，而搜索未达到任何索引和CPU使用高峰。 NPR-12811：适用于 CQ-84409 的修补程序
* AMSAEM Assets上的用户通过不同的网络创作实例访问，这些网络无法使用区块上传来上传资产，而无法删除文件夹权限。 NPR-12768：适用于 CQ-82715 的修补程序
* 在使用资产搜索边栏进行基于标记的资产搜索时，“提前键入”功能不会将其自身限制为根路径，并显示所有命名空间的标记。 NPR-12666
* 静态演绎版组件引发空指针异常。 NPR-12665
* 请求禁用MissingMetadataNotificationJob，因为它导致徽章通知UI中断页面，运行时异常为“无法扫描输入”。 NPR-12500：适用于 CQ-93573 的修补程序
* 标记字段的“禁用编辑”选项在TouchUI的资产属性页面中不起作用。 NPR-12429：适用于 CQ-88835 的修补程序
* AEM Assets6.2中的API修复，用于配套应用程序SMB实施。 NPR-11099
* 自Jquery更新以来，用户无法选择资产集合并在内容片段的“关联内容”面板中确认选择。 NPR-14847:CQ-4194209的支持
* 尽管在客户端调用了无限排序，但只对当前在UI中显示的文章／横幅／集合进行排序。 NPR-14493：适用于 CQ-109926 的修补程序
* 请求为AEM移动点播服务实施全搜索功能。 对任何文章、集合或横幅的关键字搜索不返回任何匹配项。 NPR-14093：适用于 CQ-101394 的修补程序
* 在对话框中使用Coral-select组件(*granite/ui/components/coral/foundation/form/select*)时，当选定值包含单个项时，值初始化在Internet Explorer（IE11或Edge浏览器）上无法正确工作。 NPR-13395：适用于 CQ-101013 的修补程序

### 项目 {#projects-5}

* 将使用翻译方法创建的翻译项目导出为“human”，将翻译提供程序导出为“none”时，不会生成translation_export_summary.xml文件，因为缺少GUID映射文件。 NPR-13137：适用于 CQ-91976 的修补程序
* 在AEM项目中，在创建设置了到期日属性的项目时，由于服务器和客户端之间的时区差异，日期转换设置的时间不正确。 NPR-13003：适用于 CQ-98288 的修补程序
* 更新翻译项目时，翻译作业中会丢失“在站点中显示”选项。 NPR-12966：适用于 CQ-93740 的修补程序
* 为导出的站点页面创建翻译项目时，该项目在预览中无法正确呈现。 NPR-12964：适用于 CQ-84627 的修补程序

### 工作流 {#workflow-3}

* “工作流”控制台的“存档”选项卡中的有效负荷链接会在单击时返回一个错误，响应代码为“404”。 NPR-14993：适用于 CQ-4194977 的修补程序
* 使用AEM默认工作流时，CQ邮件发送器无法向缺少单个成员电子邮件地址的组发送电子邮件通知。 NPR-14804:CQ-91499的修补程序请求
* 触屏UI中收件箱和通知徽章的性能改进。 NPR-14145：适用于 CQ-101125 的修补程序
* 在启动预览时，用户无法从工作流收件箱控制台中工作流有效负荷。 NPR-13226：适用于 CQ-100275 的修补程序
* 使用SAML身份验证处理程序配置的“saml_request_path”Cookie显示使用额外“?”设置的Cookie 字符。 此外，当SAML响应发布回AEM时，AEM &#39;saml_request_path&#39; cookie会返回无效值，因为已编码的字符。 NPR-13517:适用于GRANITE-11722和GRANITE-14414的主动式修补程序

### 解决方案集成{#solution-integration}

* 在将AEM 6.2与Search&amp;Promote集成后，如果用户搜索返回横幅的词，搜索功能将变得无响应。 NPR-14549：适用于 CQ-109631 的 CFP

### Dynamic Media {#dynamic-media}

* 在AEM激活期间创建和取消的大量AEM-Scene7sling作业在复制期间作为存档作业记录。 NPR-12835：适用于 CQ-86115 的修补程序

### 安全 {#security-5}

* 请求解决WCMDebug过滤器中的输入验证问题。 NPR-12444:CQ-94890的修补程序请求
* 在使用创建启动向导时主动请求更正XSS行为。\
   NPR-13062:CQ-99577的修补程序请求

#### Forms 附加组件包 {#forms-add-on-package-19}

`Adaptive Forms`

* 使用自适应表单创建可重复面板时，无法在运行时更新面板标题。 NPR-15325
* 如果在保存或提交时设置单选按钮的默认值，并选择非默认值的值，则预填时不显示该值。 NPR-15304
* 使用选项事件动态填充下拉框并提交选定项目的值时，Google Chrome显示错误行为。 NPR-15198
* 使用自适应表单创建可重复面板时，无法在运行时更新面板标题。 NPR-15181
* 对自适应表单使用编辑模式时，会遇到JavaScript错误，如“组件的处理程序无效”和“guidelib is undefined”。 NPR-15112
* 重复面板中的延迟加载片段不能按预期工作。 NPR-13916、NPR-14785

`Correspondence Management`

* 设置了`'Repeat with condition'`表达式的对应管理资产未正确显示。 NPR-14844
* 搜索Corresponce Management资产(如信函、文档片段或任何其他类型)时，工具栏中缺少“下载队列”图标。 NPR-14745
* 在创建列表模块时，切换资产特定属性（如可编辑、必填）不起作用。 NPR-14689
* 表达式生成器实用程序中的“数据元素”面板会在条件模块创建时不选择数据字典而继续加载。 NPR-14688
* 在预览字母时，用户无法使用制表符空格以表格格式对齐内容。 NPR-14481
* 当从用户界面批量导出Corresponce Management资源时，AEM Forms服务器会生成不必要的日志。 NPR-15226
* 预览字母时，两端对齐的文本将以其他字体显示。 NPR-15468

`**Forms Portal**`

* 提交新的门户草稿时，Forms门户网站中提交的表单的附件不可见。 NPR-13515

`**Forms Manager**`

* 在&#x200B;*FormsandDocuments*&#x200B;目录中导航时，当用户复制任何资产然后导航到其他文件夹时，不会显示粘贴按钮。 CQ-111327

#### Forms JEE 安装程序 {#forms-jee-installer-19}

`Rights Management`

* 用户登录相关审核事件记录的时间无效。 审计事件的正确时间无法跟踪。 NPR-13107
* Adobe AcrobatReader和Microsoft Office无法打开受扩展身份验证保护的文档。 NPR-14482

`Process Management`

* 当将HTML工作区中转发的草稿任务返回给初始用户时，该任务不会显示在初始用户的队列中。 NPR-15178

`Assembler Service`

* AEM Forms验证PDF/A-2b时，签名数超过两个。 NPR-14101

`XTG`

* 使用打印机旁路托盘打印文档时，`GeneratePrintedOutput`功能不允许从右旁路托盘取纸。 NPR-14079

#### Forms设计师{#forms-designer-2}

* Forms设计器在用户将所选表单区域设置作为法语（加拿大）运行拼写检查实用程序时崩溃。 NPR-13740
* Forms设计器在用户选择计算表单字段的事件或验证事件并将语言更改为JavaScript并在&#x200B;**[!UICONTROL 脚本编辑器]**&#x200B;窗口中输入`this.`时崩溃。 NPR-12974

### CFP1{#feature-packs-included-in-cfp-3}中包含的功能包

`Mobile Forms` (Forms附加包):

* 从XDP文件创建自适应表单时，辅助功能的Tab键不遵循设置的模式。 NPR-12562

`Adaptive forms` (Forms附加包):

* 自适应表单的规则构建器不提供基于角色的访问。 作者所做的更改无法跟踪。 NPR-12840

`Core` (Forms JEE 安装程序):

* Jboss+未启用CoreCross来源资源共享(CORS)功能作为Servlet过滤器。 NPR-13050

## 通过软件分发下载CFP的说明{#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>对于AEM Forms客户，在安装任何AEM Service Pack、Cumulative Service Pack或Feature Pack后，必须安装AEM forms Add-on包。

您可以直接从“软件分发”下载CFP包，或执行以下步骤：

1. 打开[软件分发](https://experience.adobe.com/downloads)。 您需要Adobe ID才能登录软件分发。
1. 点按标题菜单中的&#x200B;**[!UICONTROL Adobe Experience Manager]**。
1. 点按包名称，选择&#x200B;**[!UICONTROL 接受EULA条款]**，然后点按&#x200B;**[!UICONTROL 下载]**。

## CFP {#installation-instructions-for-cfp}的安装说明

此部分将向您介绍安装 CFP 的要求和步骤。

### 安装之前  {#before-you-install}

>[!NOTE]
>
>Adobe 提供的可选功能包依赖于发行版本和累积修补程序包。如果您已安装功能包，请联系 [AEM 客户关怀团队](https://helpx.adobe.com/cn/marketing-cloud/contact-support.html)以验证与 AEM 6.2 的累积修补程序包的兼容性。

>[!NOTE]
>
>我们建议您先对每个新的安装包运行验证，然后再尝试安装包。预验证分析并报告在安装前发现的任何错误，并预先警告用户此类错误、叠加和权限。
>
>可访问位于[https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/en/aem/6-2/administer/content/package-manager.html#Package%20Validator)的“验证”选项文档

* AEM 6.2 Service Pack 1是CFP的先决条件。 有关安装说明，请参阅 [AEM 6.2 Service Pack 1 发行说明](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。

* 可从AEM实例直接访问[软件分发](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20)上的累积修复包下载。
* 对于使用（RDBMK或MongoDB）的群集部署，CFP包可以安装在使用包管理器的任何作者实例上。

* 在安装累积修补程序包之前，请确保拍摄快照或备份您的 AEM 实例。
* 不支持卸载 CFP。

### 通过软件分发安装CFP {#install-the-cfp-via-package-share}

请执行以下步骤在现有AEM 6.2 SP1实例上安装累积修补程序包：

1. 单击[软件分发](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip)链接以下载软件包。

1. 打开[包管理器](http://localhost:4502/crx/packmgr/index.jsp)并单击&#x200B;**[!UICONTROL 上传包]**&#x200B;以上传包。

1. 选择包名称，然后单击&#x200B;**[!UICONTROL 安装]**。

### 自动安装 {#automatic-installation}

可以通过以下方式将 CFP 自动安装到正在运行的实例中：

* 在服务器运行时，将包放入。./crx-quickstart/install中。 包会自动进行安装。
* 使用包管理器](https://helpx.adobe.com/experience-manager/6-2/sites/administering/using/package-manager.html)中的[ HTTP API —— 确保使用`cmd=install&recursive=true` —— 以便安装嵌套包。

### 验证安装 {#validate-installation}

1. “产品信息”页(/system/console/productinfo)现在应在“已安装产品”下显示更新的版本字符串“Adobe Experience Manager，版本6.2.0.SP1-CFP20”。
1. 所有 OSGi 包在 OSGi 控制台中均为“活动”或“片段”（使用 Web 控制台：/system/console/bundles）。

>[!NOTE]
>
>成功安装包时，将显示一条信息性消息，指示内容包已成功安装，如“已成功安装内容包AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20”。

>[!NOTE]
>
>自AEM 6.2 SP1-CFP1以来，Jackrabbit FileVault中的日志级别已针对大多数消息从INFO更改为DEBUG。 要获取安装在AEM 6.2 SP1-CFP1或更高版本上的内容包的安装日志，请为`org.apache.jackrabbit.vault.packaging.impl`启用DEBUG日志级别。

### 安装 AEM Forms {#install-forms}

>[!NOTE]
>
>如果您不使用 AEM Forms，请跳过此部分。

#### 安装 AEM Forms 附加组件  {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms仅在JEE上**)在JEE上的AEM Forms上安装CFP的过程在[AEM FormsJEE上安装CFP中有介绍。](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee)

1. 确保已安装AEM 6.2 SP1 CFP包。
1. 下载操作系统[AEM Forms版本](aem-forms-releases.md)中列出的相应Forms加载项包。
1. 按照[安装AEM forms加载项包](https://helpx.adobe.com/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html)中的说明安装Forms加载项包。

#### 安装 AEM Forms JEE 包 {#install-aem-forms-jee-bundles-package}

AEM Forms JEE 中的修复通过单独的安装程序来交付。有关在 AEM Forms JEE 上安装 CFP 的信息，请参阅[在 AEM Forms JEE 上安装 CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer 安装程序  {#designer-installer}

1. 要安装更新，请运行Designer6.2.0_&lt;Language>_Cumulative_QF.msp文件。
1. 在“欢迎”屏幕上，单击&#x200B;**更新**。安装随即开始。
1. 安装完成后，单击&#x200B;**完成**。

## DTM、Analytics、Search &amp; Promote连接的用户可配置超时参数{#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

在AEM Cumulative Fix Pack 6.2 SP1-CFP7及更高版本中，可根据以下详细信息对以上所有连接配置连接超时时间：

| **连接** | **连接超时*** | **套接字超时**** |
|---|---|---|
| DTM | 30000ms | 30000ms |
| 分析 | 30000ms | 30000ms |
| 目标 | 60000ms | 30000ms |
| Search&amp;Promote | 30000ms | 30000ms |

* **连接超时*** —— 在建立连接之前超时（以毫秒为单位）。超时值为零被解释为无限超时。
* **套接字超时****-等待数据或两个连续数据包之间最长不活动时间的超时（以毫秒为单位）。

>[!NOTE]
>
>在AEM Cumulative Fix Pack 6.2 SP1-CFP6及更高版本中，用于Search &amp; Promote集成的OSGi配置是Apache HTTP Components Proxy Configuration。 不再使用 Day Commons HTTP Client 3.1 中的代理配置。

## 在标记控制台（经典UI）中禁用复制状态(NPR-15842){#disable-replication-status-in-tagging-console-classic-ui-npr}

如果您使用的是CFP3或更高版本，请按照以下说明在经典UI的标记控制台中禁用复制状态：

* 在&#x200B;*/apps*&#x200B;中叠加&#x200B;*&quot;/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js&quot;*

* 添加`replicationStateRequired`:第416行后的“false”。

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## 最新的Java 8 Update 131引发异常(NPR-21355){#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>这些配置设置针对使用文档安全的AEM Forms客户。

CFP12.1中包含NPR-21355。如果安装的是CFP12.1或更高版本，请执行以下过程在JBoss应用程序服务器上配置NPR-21355。 如果要在运行于OracleWebLogic或IBM WebSpehere应用程序服务器上的AEM Forms服务器上安装CFP12.1，则无需进行任何其他配置：

1. 备份、删除和创建新module.xml文件。 文件的默认位置为[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. 打开新创建的module.xml文件进行编辑。 将以下代码添加到文件：

   ```xml
   <module xmlns="urn:jboss:module:1.1"
   name="com.adobe.livecycle">
   <resources>
   <resource-root path="cryptojcommon.jar"/>
   <resource-root path="cryptojce.jar"/>
   <resource-root path="jcmFIPS.jar"/>
   <resource-root path="certj.jar"/>
   <resource-root path="cglib.jar"/>
   </resources>
   <dependencies>
   <module name="javax.api"/>
   <module name="asm.asm"/>
   </dependencies>
   </module>
   ```

1. 创建位于[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/adobe/livecycle/main/的jsafeFIPS.jar、jsafeJCEFIPS.jar和certjFIPS.jar文件的备份，并从上述目录中删除文件。

   联系[Adobe支持](https://helpx.adobe.com/marketing-cloud/contact-support.html)以获取新的JAR文件。 将从[Adobe支持](https://helpx.adobe.com/marketing-cloud/contact-support.html)获取的JAR文件放在[AEM_Forms_安装目录]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. （仅限Windows）修改`[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat`或`domain.conf.bat`配置文件：

   * 对于独立配置中的JBoss服务器，打开standalone.conf.bat进行编辑。
   * 对于群集配置中的JBoss服务器，打开domain.conf.bat进行编辑。

   在末尾添加以下行并保存文件：

   设置&quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   设置&quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. （仅限基于Linux的OS）修改[AEM_Forms_Installation_directory]/jboss/standalone.conf或domain.conf配置文件：

   * 对于独立配置中的JBoss服务器，打开standalone.conf进行编辑。
   * 对于群集配置中的JBoss服务器，打开domain.conf进行编辑。

   在末尾添加以下行并保存文件：

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## NPR-19778 所需的配置设置 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778是CFP14的一部分。

默认情况下，当用户声明任务时，共享队列的计数不会刷新给其他用户。 为此，我们引入了一种新的属性。 请按照以下步骤在AEM实例上配置此属性：

1. 转到“管理员UI”->“服务”->“工作区”->“全局管理”。
1. 导出全局设置。
1. 在下载的XML文件中，添加标签`<client_tasksPollingInterval>10</client_tasksPollingInterval>`此处，10是以秒为单位的示例值。 您可以相应地修改它。
1. 保存文件。
1. 返回“管理员UI”->“服务”->“工作区”->“全局管理”。
1. 在“导入全局设置”部分导入xml文件。
1. 您现在可以注销系统并重新登录。
1. 为工作区中的其他用户刷新共享队列开始的计数。
1. 要关闭轮询，请将值更改为0，然后再次导入XML文件。

## UI更改{#ui-changes}

* 在具有dc的图像卡上显示标题时的行为变化：title属性设置为字符串[](multifield):在UI中，图像卡上只会显示最新更改的标题，但所有标题都将保存在CRX中。 适用于 CQ-4217165 的修补程序

## 已知问题 {#known-issues}

* 从CFP18更新AEM 6.2SP1-CFP19和AEM 6.2SP1-CFP20会更改根重定向到经典UI欢迎页面，而不是/sites.html/content。 你可能必须纠正吊具：目标属性(使用CRX Explorer从/welcome.html到/index.html)。 在从CFP17或旧版本进行更新时不会观察到此问题。

安装AEM 6.2 SP1-CFPx时，可能会发生以下临时错误。 但是，这些错误不需要解决，因为它们不会影响AEM实例并在安装CFP后离开：

* 将AEM 6.2SP1-CFP20实例升级到AEM 6.5时，某些虚URL可能无法正常工作：

   * */projects.html*
   * */sites.html*

但是，解决方法是在升级后重新启动AEM实例。

* 打开Web控制台组件详细信息页面时，收到HTTP 500内部服务器错误。
* **创建组件实例**&#x200B;和&#x200B;**服务工厂返回的错误**&#x200B;由于存储库重新启动而发生：

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)]由于无法绑定引用profileManager，无法创建组件实例
   * org.apache.sling.commons.调度程序FrameworkEvent ERROR(org.osgi.framework.ServiceException:服务工厂返回null。 (组件：com.day.cq.tating.impl.TagGarbageCollector(1687))

* 在Mongo和DB2中安装CFP时观察到的错误：**org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry:异常：java.lang.NullPointerException**。 在CFP8上安装CFP后不会发生此错误。
* (AdobeGranite维护调度程序更新任务)com.adobe.granite.maintenance.impl.TaskScheduler:找不到名为WorkflowPurgeTask的窗口granite:weekly的维护任务
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* 在AEM 6.2 SP1上安装CFPx时，将从DAM更新资产工作流中删除之前添加的智能标签资产的工作流步骤。

请参阅AEM 6.2 SP1]中[已知问题的列表(https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known问题)。

## Uber Jar {#uber-jar}

用于6.2 SP1-CFP20的Uber Jar可在[Adobe公共Maven存储库](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/)中找到。

要在Maven项目中使用Uber Jar，请在项目POM中包含以下依赖项：

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## 包含{#osgi-bundles-and-content-packages-included-5}的OSGI包和内容包

以下文本文档OSGI包的列表以及CFP中包含的内容包。

* [AEM 6.2 SP1-CFP20中包含的OSGi包的列表](assets/do-not-localize/updated.txt)
* [AEM 6.2SP1-CFP20中包含的内容包列表](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 修补程序页面](https://helpx.adobe.com/cn/experience-manager/kb/aem62-available-hotfixes.html)
>* [AEM 6.2 SP1发行说明](https://docs.adobe.com/content/docs/en/aem/6-2/release-notes/sp1.html)
>* [AEM 6.2 发行说明](https://docs.adobe.com/docs/cn/aem/6-2/release-notes.html)
>* [AEM 产品页面](http://www.adobe.com/cn/solutions/web-experience-management.html)
>* [AEM 6.2 文档](https://docs.adobe.com/content/docs/en/aem/6-2.html)
>* [订阅](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) Adobe [优先级产品更新](https://docs.adobe.com/content/help/en/release-notes/experience-cloud/current.html)

