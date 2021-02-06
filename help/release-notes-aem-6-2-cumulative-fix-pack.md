---
title: AEM 6.2 累积修补程序包
description: Experience Manager6.2累积修复包发行说明。 深入了解Experience Manager组件中各种累积修复包中修复的问题。
translation-type: tm+mt
source-git-commit: 98d91e0367912d8962bb2f45ae972f50ccb71b5f
workflow-type: tm+mt
source-wordcount: '19975'
ht-degree: 99%

---


# AEM 6.2 累积修补程序包发行说明{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived via UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## 发行信息 {#release-information}

| **产品** | Adobe Experience Manager |
|---|---|
| **版本** | 6.2 |
| **发行版** | [累积修补程序包 6.2 SP1-CFP20](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) |
| **先决条件** | [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html) |
| **正式发布** | 2019 年 6 月 6 日 |

### 累积修补程序包 {#cumulative-fix-pack}

Adobe 引入了统一交付模式，用于发布修补程序。现在，Adobe 每月会发布一个累积修补程序包 (CFP)（需通过质量检查），而不是针对个别问题发布修补程序。CFP 是指多个修补程序的汇总内容包。CFP 主要包括错误修复，但也可能包括功能包。与单个修补程序发行版相比，CFP 具有以下优点：

* 本质上是累积的（例如，CFP 包含以前 CFP 已交付的修补程序）
* 提高了质量保证
* 简化了安装（用户将 CFP 安装为一个不含任何依赖关系的包，最新的服务包除外）

有关 CFP 和其他发行版类型的更多信息，请参阅[维护版本工具](https://docs.adobe.com/content/docs/cn/aem/6-2/deploy/maintenance-release-vehicle-definitions.html)。

## 关于此发行版 {#about-the-release}

AEM 累积修补程序包 6.2 SP1-CFP20 是 AEM 6.2 的最新累积修补程序包，它是一个重要更新，包括自 [AEM 6.2 SP1](https://helpx.adobe.com/cn/experience-manager/6-2/release-notes/sp1.html) 正式发布以来的一些关键客户修补程序。

>[!CAUTION]
>
>在没有验证已安装功能包之间的兼容性的情况下应用 CFP，可能会导致系统故障或自定义配置丢失，这些问题可能需要从备份还原才能解决。

>[!NOTE]
>
>* AEM 累积修补程序包 6.2 SP1-CFP10 中包含一个新的 Sling `discovery-  api` 包 Johnzon 1.0.0。此外，还为 CRX 存储库中的节点 */var/discovery* 添加了拥有读取和写入权限的服务用户 sling-discovery。
   >
   >
* 添加了 Apache Commons **org.apache.commons/commons-email/1.5** 的电子邮件包，用于替换 **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**。
   >
   >
* 对于在 AEM 实例上拥有大量用户的客户，Adobe 建议通过安装文件夹来部署 CFP。

>



## 包含的问题 {#issues-included}

此部分列出了当前 CFP 中包含的所有问题和修补程序。

此外，此 CFP 还包含[以前的累积修补程序包](#previous)交付的修补程序。

### 集成 {#integration}

* 对多项营销活动定位个性化改进功能打补丁。NPR-29163：适用于 CQ-4264126 的修补程序
* com.day.cq.personalization.impl.TeaserResourceEventHandler 陷入无限循环，并导致对发布实例上的节点进行更新。NPR-28561：适用于 CQ-4263096 的修补程序

### DAM - 常规 {#dam-general}

* 无法在特定 dam 文件夹中为非管理员用户显示/隐藏复制按钮。NPR-29026：适用于 CQ-4265361 的修补程序

### 漏洞 {#vulnerability}

* CSRF 保护框架不适用于 AEM Foundation 表单。NPR-28612：适用于 GRANITE-22231 的修补程序

### 表单 {#forms}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package}

>[!NOTE]
>
>对于 AEM Forms 客户，请在安装任意 AEM Service Pack、累积修补程序包或功能包之后，再安装 AEM Forms 附加组件包，这一点至关重要。

>[!NOTE]
>
>AEM Forms 附加组件包有助于使表单功能与 AEM Service Pack 和累积修补程序包保持一致。因此，请务必在安装任意 AEM Service Pack、累积修补程序包或功能包之后安装 AEM Forms 附加组件包。

#### 自适应表单 {#adaptive-forms}

* iOS 12.1 设备上的涂写组件存在可用性问题。NPR-29082：适用于 CQ-4261765 的修补程序

#### 表单 - 文档安全 {#forms-document-security}

* 在 PDF 中使用“PDF 高级电子签名”(PAdES) 验证所有签名会引发 InvalidOperationException。NPR-27848：适用于 CQ-4244837 的修补程序

#### 表单 - 通信 {#forms-correspondence}

* 在以 PDF 格式预览信件时，放置在母版页上的文本字段不接受从数据选项卡或根据指定的数据链接输入的值。NPR-29239：适用于 CQ-4266856 的修补程序.

#### 表单 - 交互式通信 {#forms-interactive-communication}

* 添加撇号字符后，信件中的预填充字段显示为 ASCII 字符，而不是常规字母。NPR-28863：适用于 CQ-4262900 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

## 以前的累积修补程序包中包含的修补程序和功能包 {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### 累积修补程序包 19 {#cumulative-fix-pack-1}

AEM 累积修补程序包 6.2 SP1-CFP19 是一个重要更新，它包括自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 启用了针对 AEM 6.2 的 MS Translator API v3.0 支持
* 成功安装所有 SP、CFP 和 HF 的软件包后，添加了日志消息。

### 资产 {#assets}

* 如果缺少“编辑 ACL”权限，则无法重命名 DAM 文件夹。NPR-27555：适用于 CQ-104652 的修补程序
* 在 6.2.1 CFP 17 及更高版本中，图像预设编辑器工具无响应。NPR-28147：适用于 CQ-4261041 的修补程序

### 站点 {#sites}

* 链接检查器无法完成作业，因无响应链接而卡住。NPR-27373：适用于 CQ-4256030 的修补程序
* 由于附加的根路径破坏了区段路径，区段文件无法正确加载。NPR-28014：适用于 CQ-4260332 的修补程序

### 集成 {#integration-1}

* 无法在目标容器上正确取消 LiveCopy 继承。NPR-28129：适用于 CQ-4259813 的修补程序
* 目标组件未考虑 cq :action。NPR-27616：适用于 CQ-4257497 的修补程序

* 中断继承的图标显示不一致。NPR-27671：适用于 CQ-4257779 的修补程序

### Felix {#felix}

* 在 AEM 6.2 SP1 实例上安装 CFP 18 后，Web 控制台组件详细信息失败，出现 500 错误。NPR-28350：适用于 CQ-4261095 的修补程序

### 翻译 {#translation}

* 将 MS Translator 升级到 API v3.0 后，在 AEM 6.3 中启用对 MS Translator 服务的支持。NPR-28123：适用于 CQ-4259096 的修补程序

### UI - Foundation {#ui-foundation}

* OOTB Sites 日历显示不正确的日期。NPR-28392

### Granite {#granite}

* 对于使用 sling :basename 的资源包，词典不会失效。NPR-27624

### 留存 {#sustenance}

* 应将包管理器活动日志提取到单独的日志文件中。NPR-27323：适用于 Granite-14866 的修补程序
* 安装完成后，error.log 中将会显示标准化短语/措辞/日志行。NPR-27835
* Granite 包插件正在挑选较低版本的 org.apache.sling.i18n 的依赖项。适用于 CQ-4263245 的修补程序
* 在 6.2SP1-CFP15 之后安装最新 CFP 时，将会删除 com.adobe.cq.com.adobe.cq.ui.commons 包。适用于 CQ-4258808 的修补程序

### 表单 {#forms-1}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-1}

#### 自适应表单 {#adaptive-forms-1}

* AEM Forms 存在 XML 注入漏洞。NPR-27843：适用于 CQ-4257315 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-1}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

### 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included}

以下文本文档列出了 CFP 中包含的 OSGi 包和内容包。

AEM 6.2 SP1-CFP19 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/cfp19_osgi_bundles.txt)

AEM 6.2 SP1-CFP19 中包含的内容包列表

[获取文件](assets/do-not-localize/cfp19_content_packages.txt)

### 累积修补程序包 18 {#cumulative-fix-pack-2}

AEM 累积修补程序包 6.2 SP1-CFP18 是一个重要更新，它包括自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 在 DAM CommandLineProcess 中添加了支持终止长时间运行的进程的功能。
* 修复了 ReplicationEventListener 中的会话泄漏。
* 添加了对核心页面组件的重定向支持。

### 资产 {#assets-1}

* Camera Raw 进程在大量摄取期间卡住，最终阻止所有工作流处理。NPR-26990：适用于 NPR-23860 的修补程序
* 下载功能通过 assetdownload servlet 利用 AEM Assets，允许匿名用户下载所有资产。NPR-27054：适用于 CQ-4254732 的修补程序
* 在 AEM 中电子邮件模板的主题行上，特殊字符显示为断开。NPR-26470：适用于 CQ-4252368 的修补程序

### 站点 {#sites-1}

* 由于 ConfigPostProcessor 类的行为不正确，暂停父图像会从子页面中删除 cq : LiveRelationship 混合类型。NPR-26745：适用于 CQ-4254163 的修补程序
* 添加了对核心页面组件的重定向支持。NPR-26576：适用于 CQ-110529 的修补程序
* 将 ContextHub 迁移到 jQuery 3。NPR-26956：适用于 CQ-4255472 的修补程序
* 对话框中的锚点输入字段显示在浏览器可见部分之外，直到最大化才能看到。NPR-26852：适用于 CQ-4255019 的修补程序
* 在内容片段中复制粘贴文本时，插入多余的 &lt;br>。NPR-26660：适用于 CRTE-151 的修补程序
* 经典 siteadmin 不会在某些页面的右侧窗格中呈现列表。NPR-27247：适用于 CQ-4251621 的修补程序
* （经典 UI）尝试移动/重命名页面时，会生成以下错误：“移动页面时出错。”NPR-27179：适用于 CQ-4235907 的修补程序

### 集成 {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever 遍历整个树来收集可用品牌。NPR-27060：适用于 CQ-4255790 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components}

* Foundation 列表组件存在搜索功能问题。NPR-26817：适用于 CQ-4250324 的修补程序

### 平台 {#platform}

* 由于存在特殊字符长破折号 (—)，发布程序刷新缓存时出现问题。NPR-27199：适用于 CQ-4242790 的修补程序

### 花岗岩{#granite-1}

* 包验证程序无法验证 CFP/SP 中含有的包。NPR-26775：适用于 Granite-22825 的修补程序

### 复制 {#replication}

* ReplicationListener 中的 JCR 会话泄漏。NPR-27063：适用于 CQ-4232088 的修补程序

### 表单 {#forms-2}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-2}

* Forms 附加组件包中没有新的 AEM Forms 修补程序。

### Forms JEE 安装程序 {#forms-jee-installer-2}

* Forms JEE 安装程序中没有新的 AEM Forms 修补程序。

#### 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-1}

AEM 6.2 SP1-CFP18 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/62cfp18updated_bundles.txt)

AEM 6.2 SP1-CFP18 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### 累积修补程序包 17 {#cumulative-fix-pack-3}

AEM 累积修补程序包 6.2 SP1-CFP17 是一个重要更新，它包括自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 添加了对 at-integration.js 中的无扩展名站点 URL 的支持
* 从 S7 云服务配置中删除了 S7 轮询导入程序。
* 更改了受众视图，以支持多租户实施的文件夹结构。
* 更新至 jqueryui clientlib v1.12.1。

### 资产 {#assets-2}

* 从资产 UI 启动工作流时，用户需要具有写入/删除/修改权限。NPR-25688：适用于 CQ-4250140 的修补程序
* 即使用户没有“复制”权限，他们仍可看到“发布”和“取消发布”按钮。NPR-25094
* （工作流）智能标记资产工作流不会通过 AEM 代理配置进行处理。NPR-25915：适用于 CQ-4248202 的修补程序
* 从 S7 云服务配置中删除了 S7 轮询导入程序。NPR-25239：适用于 CQ-95236 的修补程序

### 站点 {#sites-2}

* 从“编辑器”>“页面信息”启动的工作流在有效负荷中包含上下文路径。NPR-26389：适用于 CQ-76804 的修补程序
* （外部链接检查器）无效的 https 链接显示为有效链接。NPR-25541：适用于 CQ-4201333 的修补程序
* （经典 UI）在 Live Copy 下创建独立页面时，该页面将创建为 Live Copy。NPR-25610：适用于 CQ-4249801 的修补程序
* 激活页面后，发布与设计导入程序组件关联的资源时出现问题。NPR-25638：适用于 CQ-102532 的修补程序
* RTE 富文本工具栏包含选择列表。NPR-25165：适用于 CQ-4248948 的修补程序
* 将 ContextHub 迁移到 jQuery 3。NPR-25059：适用于 Granite-19902 的修补程序
* 对于 Parsys 嵌套组件，始终从多个可用组件中应用第一个（具有最少的嵌套路径）令人满意的设计。有关更多信息，请参阅[设计路径解析](https://helpx.adobe.com/cn/experience-manager/6-3/sites/developing/using/page-templates-static.html)。NPR-25250：适用于 CQ-4246276 的修补程序

### 集成 {#integration-3}

* 使用 OOTB Target 集成定位组件时，会呈现整个页面，而不是空的目标组件。NPR-25273：适用于 CQ-4248003 的修补程序
* 在定位模式中，中断继承仍会将组件显示为“已定位”，并且在编辑模式中继承未中断。NPR-25324：适用于 CQ-4248162 的修补程序
* 在页面上定义个性化并解析受众时，相应的体验会在编辑模式下显示。NPR-25731：适用于 CQ-4249465 的修补程序
* 将 AEM 与非默认上下文路径一起使用时，会出现错误的 Teaser URL。NPR-25971：适用于 CQ-4250953 的修补程序
* 使用输出内容时呈现空白。NPR-25295：适用于 CQ-4246792 的修补程序
* 激活页面时，永远不会从发布站点中移除已从创作环境删除的体验。NPR-24869：适用于 CQ-4247832 的修补程序

### DAM - DM 客户端 {#dam-dm-client}

* （Chrome、Firefox）在已启用触控功能的设备上，VideoPlayer 会忽略鼠标单击。适用于 CQ-4247370 的修补程序

### 平台 {#platform-1}

* 允许配置在获取/释放包时的最大重试次数。NPR-25328：适用于 Granite-22376 的修补程序
* 发生复制错误时的日志记录不正确。NPR-25308：适用于 CQ-4249402 的修补程序
* 安装 Forms AEM 6.2 Forms CFP8 至 CFP14 会导致 Apache POI 失败。NPR-25053：适用于 Granite-21771 的修补程序

### 花岗岩{#granite-2}

* 用户同步过程失败，并出现 OakConstraint0022 异常。NPR-25729：适用于 Oak-7428 的修补程序

### 社区 {#communities}

* 使用 Mongo 驱动程序 3.x 版本无法启动 cq -social-as-provider 包。NPR-26271：适用于 CQ-4252710 的修补程序

### UI - Foundation {#ui-foundation-1}

* 更新至 jqueryui clientlib v1.12.1。NPR-25090：适用于 Granite-21981、CQ-4248897 的修补程序

* (Omnisearch)：“标题”属性容易遭受站点中的跨站点脚本 (XSS) 攻击。NPR-24994：适用于 Granite-19933 的修补程序

### 表单 {#forms-3}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-3}

#### 自适应表单 {#adaptive-forms-2}

* 从自适应表单提交数据时编码错误。NPR-25539

#### 表单 - 管理 {#forms-management}

* 发布页面时，不相关的表单资产报告为引用。NPR-26167：适用于 CQ-4251004 的修补程序

### 表单 - JEE 安装程序 {#forms-jee-installer-3}

#### 文档安全 {#document-security}

* 变量以“列表”数据类型填充，子类型为字符串，但出现“无法强制对象”错误。NPR-26194：适用于 CQ-4252287 的修补程序
* 安装 6.2-SP1-CFP15 后，无法访问水印配置。NPR-26130：适用于 CQ-4250984 的修补程序

### 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-2}

AEM 6.2 SP1-CFP17 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/62cfp17updated_bundles.txt)

AEM 6.2 SP1-CFP17 中包含的内容包列表

[获取文件](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### 累积修补程序包 16 {#cumulative-fix-pack-4}

AEM 累积修补程序包 6.2 SP1-CFP16 是一个重要更新，它包括自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。
* 修复了配置文件弹出窗口中的 ContextHub 图标对齐问题。
* 修复了下拉组件的显示/隐藏功能。
* 升级到最新的 Jackson 版本 2.8.11

### 资产 {#assets-3}

* 无法从列表视图启动工作流。NPR-24393：适用于 CQ-4245788 的修补程序
* (Firefox/Chrome) 无法在“资产共享”页面中下载资产。NPR-24523：适用于 CQ-4224408 的修补程序
* 提高了 AEM 中视频预览的默认质量。NPR-24148：适用于 CQ-4244310 的修补程序

### 集成 {#integration-4}

* 在发布实例上定位某个组件后，系统会出现闪烁，显示默认体验位于目标体验之前。NPR-23992：适用于 CQ-4242038 的修补程序
* 激活页面时，永远不会从发布站点中移除已从创作环境删除的体验。NPR-24869：适用于 CQ-4247832 的修补程序

### 平台 {#platform-2}

* 修补 clientlib 中的 jQuery 1.12.4 以包含安全修补程序。NPR-24129：适用于 Granite-20058 的修补程序
* 在每日 CQ 邮件服务中添加了 STARTTLS 支持。NPR-23941：适用于 CQ-4240397 的修补程序
* 删除默认的 MERGE_PRESERVE aclHandling。NPR-24593：适用于 Granite-21889 的修补程序
* 当请求包含无效查询参数时，LineChecker 无法将链接外部化。NPR-24127：适用于 CQ-4241893 的修补程序

### MSM {#msm}

* 针对跨站点脚本 (XSS) 攻击的主动修补程序。NPR-21893：适用于 CQ-4223385 的修补程序
* 如果 BlueprintConfig 位于根目录上，则会出现 MSM LiveRelationship: 有效 RolloutConfig 错误。NPR-23999：适用于 CQ-4243000 的修补程序

### 站点 {#sites-3}

* 在 Live Copy 区域中创建新体验时，需要配置要中断的继承。NPR-24995：适用于 CQ-4248209 的修补程序
* （触屏 UI）在锁定或解锁页面时，顶部工具栏上的多个图标消失。NPR-23954：适用于 CQ-4243345 的修补程序
* ContextHub 中的字段未正确对齐。NPR-23958
* 在锁定的页面上执行发布操作会中断创作。NPR-23970：适用于 CQ-4243203 的修补程序
* /etc/reports/ 中的 OOTB 报告无法正常工作，且不显示历史数据图。NPR-20035：适用于 CQ-4220180 的修补程序
* 在项目上启动“请求启动项”工作流时，启动项创建失败。NPR-24255：适用于 CQ-4245030 的修补程序
* 安装 CFP10 后，电子邮件会忽略 HTML 标记和属性。NPR-24287：适用于 CQ-4240028 的修补程序
* 标记选取器：标记元数据架构“标记”字段中的标记建议会查询可标记的节点，因此，需要较长时间才能加载。NPR-24347：适用于 CQ-4244291 的修补程序
* Salesforce 集成因代理配置而失败。NPR-24418：适用于 CQ-4245300 的修补程序
* (WCM) 在创建修订版期间出现异常时，PageManager 会将页面保留为已签入状态。NPR-24565：适用于 CQ-4246203 的修补程序
* 应用 CFP14 后，“设备模拟器”按钮从编辑和预览模式中消失。NPR-24566：适用于 CQ-4247060 的修补程序
* （经典 UI）在对话框中创作后，整个标记显示为空。NPR-24688：适用于 CQ-4246407 的修补程序
* 首次尝试时无法创建版本。NPR-24774：适用于 CQ-4232176 的修补程序
* /etc/reports/ 中的 OOTB 报告无法正常工作，且不显示历史数据图。NPR-24138：适用于 CQ-4220180 的修补程序

### 漏洞 {#vulnerability-1}

* Salesforce 集成容易遭受服务器端请求伪造 (SSRF) 攻击。NPR-24289：适用于 CQ-4245277 的修补程序
* ReportingServicesProxyServlet 中存在服务器端请求伪造 (SSRF) 漏洞。NPR-24657：适用于 CQ-4246880 的修补程序

### 花岗岩{#granite-3}

* 元数据读取操作未终止。NPR-24240：适用于 Granite-19866 的修补程序
* 将 Jetty 更新为 9.4.11.v20180605，以修复漏洞。NPR-25033：适用于 Granite-22120 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-1}

* 对页面进行排序时，PageComparator 会引发 ClassCastException。NPR-24123：适用于 CQ-4244048 的修补程序
* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-24562：适用于 CQ-4222853 的修补程序

### 用户界面 {#user-interface}

* 由于管理员搜索功能中存在大量请求，观察到 CPU 使用率很高。NPR-23588：适用于 Granite-21286 的修补程序
* （经典 UI）即使关联的表单数据模型服务设置为空字段，组件也会显示默认值。NPR-21903：适用于 GRANITE-19744 的修补程序
* 当不存在请求的表单数据时，多字段会引发空指针异常。NPR-24513：适用于 Granite-21055 的修补程序

## 表单 {#forms-4}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-4}

#### 核心 {#core}

* (OSGi) AEM Forms OSGi 受 Jackson 数据绑定安全警报影响。NPR-24274：适用于 CQ-4230245 的修补程序

#### 权限管理 {#rights-management}

* 安装 AEM 6.2 SP1-CFP14 后，Apache POI 失败。NPR-25054、NPR-25052：适用于 CQ-4245898、CQ-4244778 的修补程序

#### HTML5 表单 {#html-forms}

* 在 HTML 预览中，数据未使用多行字段的预填充内容进行填充。NPR-23357：适用于 CQ-4244212 的修补程序
* 通过默认预览来预览信件时，不显示布局片段映射，而在单击预览按钮时，会正确显示布局片段映射。NPR-22993：适用于 CQ-4237745 的修补程序
* 将社保号模式应用于模板时，文本字段的 HTML 预览出现问题。NPR-23205

#### 自适应表单 {#adaptive-forms-3}

* 将 AEM 表单添加到 Parsys 组件时，出现“未定义 Guidelib”错误。NPR-24269：适用于 CQ-4244546 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Shell 脚本文件中的窗口行结尾导致 LCM 无法在 UNIX 中运行。NPR-22958

### 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-3}

AEM 6.2 SP1-CFP16 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

AEM 6.2 SP1-CFP16 中包含的内容包列表

[获取文件](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### 累积修补程序包 15 {#cumulative-fix-pack-5}

AEM 累积修补程序包 6.2 SP1-CFP15 是一个重要更新，它包括自 [AEM 6.2 SP1](https://helpx.adobe.com/experience-manager/6-2/release-notes/sp1.html) 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 在 Foundation 表中实施主动安全修复，以保持设计的一致性。
* 添加了对 TypeHint 的支持，可将值保存为字符串。
* 增强了表单预填充服务的安全性
* 更新至最新的 adobe-reader-extensions-dsc.jar 文件，以获取 Reader 扩展中的修补程序。
* 调整了验证挂接，以考虑用于提升数输入的“:invalid”项。

### 资产 {#assets-4}

* 对于 Ptiff 生成流程，EmbedXMP 数据始终设置为“活动”。NPR-22776：适用于 CQ-4234498 的修补程序
* 在多值字段中无法设置多个默认值。NPR-22900：适用于 CQ-4239000 的修补程序
* (Dynamic Media) 选中“动态呈现版本”复选框时，下载的 zip 文件会生成原始的 TIFF 图像，并且文件具有零字节。NPR-22410：适用于 CQ-4198471 的修补程序
* （触屏 UI）列视图中资产的默认上传位置。NPR-23475：适用于 CQ-4237057 的修补程序

### 集成 {#integration-5}

* 在 Target 模式中，作者可以修改从 Blueprint 继承的组件，而无需取消继承。NPR-22751：适用于 CQ-4237907 的修补程序
* 路径变量无法正确编码，从而导致非持久性跨站点脚本 (XSS)。NPR-22851

### MSM {#msm-1}

* 在转出具有多个转出配置的 LiveCopy 时，如果根目录下出现 ResourceNameConflict，则转出流程将会终止，而不包括所有分支。NPR-22842：适用于 CQ-4236188 的修补程序

### 平台 {#platform-3}

* 在反向应用程序的一个请求中实施轮询限制。NPR-23351：适用于 Granite-21135 的修补程序****
* 消息模式更改未反映在自定义日志记录器中。NPR-23486：适用于 CQ-4241974 的修补程序

### 站点 {#sites-4}

* 如果在富文本编辑器的文本中创建的指向文档的链接包含空格或其他特殊字符，则该链接不起作用。NPR-22289：适用于 CQ-4224321 的修补程序
* 保存具有大型值 (10000000000) 的区段会将提升设置为 0，从而导致出现错误消息。NPR-22524：适用于 CQ-4237006 的修补程序
* 在多字段组件中，无法单击“添加”项。NPR-22552：适用于 CQ-4237404 的修补程序
* 当区段具有长标题时，水平滚动条不可见。NPR-22615：适用于 CQ-4237001 的修补程序
* 加载空受众会生成错误的 JavaScript 代码。NPR-22974：适用于 CQ-4238734 的修补程序
* 在计划激活或取消激活时，必须提供工作流标题，因此，自定义工作流标题在时间轴中未翻译。NPR-23121：适用于 CQ-4237552 的修补程序
* 请求提供针对站点中 Target 区段相关问题的修补程序。NPR-23128
* (Firefox) 选定角色对应的复选框不正确。NPR-23345
* 不同模式的标签会与图标一起显示。NPR-23275
* 将组件从 AEM 6.0 迁移到 AEM 6.2 时出现“无效的递归选择器值”错误。NPR-23503：适用于 CQ-4241258 的修补程序

### 社区 {#communities-1}

* 由于向组发送消息失败，未触发 Web 和邮件通知。NPR-23447：适用于 CQ-4242880 的修补程序

### 翻译 {#translation-1}

* 在翻译配置中设置“不翻译”资产时，将会创建资产语言副本。NPR-22540：适用于 CQ-4237962 的修补程序

### 用户界面 {#user-interface-1}

* 将 Omnisearch 与连字符查询一起使用，会返回服务器错误。NPR-22999：适用于 Granite-19674 的修补程序
* 日期选取器不支持由隐藏的字段设置的手动设置外部类型提示。更改类型提示会导致转换错误。NPR-23333：适用于 Granite-21194 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-2}

* 为了提高安全性，已弃用 CAPTCHA 组件。如果您使用的是 CAPTCHA 组件，则在安装 6.2 SP2-CFP15 或更高版本后，将显示“Captcha 组件已弃用，不应再使用”消息。可以自定义 AEM 组件来包含 reCAPTCHA 以提高安全性。NPR-22151：适用于 CQ-4220052 的修补程序
* WCM Foundation 组件“表”容易遭受存储型跨站点脚本攻击。NPR-23206：适用于 CQ-4240760 的修补程序

### 漏洞 {#vulnerability-2}

* 管理员 UI 项目链接中存在跨站点脚本 (XSS) 漏洞。NPR-23272：适用于 CQ-4241795 的修补程序

## 表单 {#forms-5}

### Forms 附加组件包 {#forms-add-on-package-5}

#### 通信管理 {#correspondence-management}

* 通过默认预览来预览信件时，不显示布局片段映射，而在单击预览按钮时，会正确显示布局片段映射。NPR-23335：适用于 CQ-4237745 的修补程序
* 使用直接信件 URL 时，不会填充与 XDP 中定义的绑定相对应的信件数据。NPR-24145：适用于 CQ-4244290 的修补程序

#### 移动设备表单 {#mobile-forms}

* （通信管理）使用目标 XML 加载信件时，数据未对齐。NPR-22993：适用于 CQ-4237663 的修补程序

#### Reader 扩展服务 {#reader-extensions-service}

* 无法在 Adobe PDF 上应用 Reader 扩展。NPR-23067

#### 表单管理器 {#forms-manager}

* 重新发布站点页面时，不会发布嵌入到站点的表单。NPR-23014：适用于 CQ-4236566 的修补程序

#### 漏洞 {#vulnerability-3}

* 针对跨站点脚本的主动修补程序。NPR-20624：适用于 CQ-4206055 的修补程序
* 表单管理器的注释选项卡中存在存储型跨站点脚本 (XSS) 漏洞。NPR-27157：适用于 CQ-4255556 的修补程序

#### 加密服务 {#encryption-service}

* (OSGi) [JEE] 使用“验证 PDF 进程”进行验证时，包含附件的 PDF 的签名状态不正确。NPR-23269、NPR-23737

### Forms JEE 安装程序 {#forms-jee-installer-5}

#### 核心 {#core-1}

* 应修复 Core-ext 静态代码分析中报告的问题。NPR-13947

#### PDFG 服务 {#pdfg-service}

* HTML 至 PDF 转换器不起作用。NPR-21545

### 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-4}

以下文本文档列出了 CFP 中包含的 OSGi 包和内容包。

AEM 6.2 SP1-CFP15 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_2cfp15updated_bundles.txt)

AEM 6.2 SP1-CFP15 中包含的内容包列表

[获取文件](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### 累积修补程序包 14 {#cumulative-fix-pack-6}

AEM 累积修补程序包 6.2 SP1-CFP14 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 改进了资产元数据属性的可编辑性。
* 为已处于过期状态的资产重新配置了“密码到期通知”作业。
* 自定义触屏 UI 控制台以扩展其他区域设置。
* 更新了 cq-msm-core，以实现有效的 Livecopyindex 同步。
* 简化了各种转出的复制功能。

### 资产 {#assets-5}

* 用户无法下载包含免责声明和长文件名的资产。NPR-22163：适用于 CQ-4235274 的修补程序
* 单引号字符会阻止在批量视图中更新元数据，当您使用快速工具栏操作打开资产属性时，用户界面会完全损坏。NPR-22317、NPR-22353：适用于 CQ-4236990、CQ-4236469 的修补程序
* “资产到期通知”作业不会停用已过期的资产。NPR-22346：适用于 CQ-4237188 的修补程序
* 在 Safari 上的资产中使用数字版权管理时，资产下载失败。NPR-22378：适用于 CQ-4236460 的修补程序
* 小图像的 Web 呈现版本像素大小不准确。NPR-22435：适用于 CQ-4236742 的修补程序

### 站点 {#sites-5}

* （触屏 UI）已移动的标记会显示在页面属性中的旧位置和新位置。NPR-21921：适用于 CQ-4238598 的修补程序
* （触屏 UI）富文本编辑器会从 &lt;a> 标记中删除 id 以外的所有其他属性。NPR-22045：适用于 CQ-4234133 的修补程序
* 使用 CTRL+V 直接在富文本编辑器中粘贴内容会跳过换行符。NPR-22117：适用于 CUI-5881 的修补程序
* （触屏 UI）在命名空间下无法显示超过 40 个标记。NPR-22290：适用于 CQ-99114 的修补程序
* 从端口 -1 到 AEM 6.2 的 RSS 馈送问题。NPR-22158：适用于 CQ-4233339 的修补程序
* (IE) 首次在富文本字段中创作任何字符时，将向该字符添加尾随空格。NPR-22443：适用于 CQ-4235343 的修补程序
* 当尝试与包名称匹配时，由于包声明中存在尾随空格字符，Java Use 对象冻结 SightlyJavaCompilerService。NPR-22557：适用于 Granite-20836 的修补程序
* 触屏 UI 控制台不会选取新的标记语言。NPR-22250：适用于 CQ-4239194 的修补程序

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) 必须为作品集设置“出版日期”和“封面日期”字段，然后才能将其上传到 DPS。NPR-22484

### 商务 {#commerce}

* 商务“创建目录”向导中存在多个跨站点脚本 (XSS) 漏洞。NPR-22344：适用于 CQ-4237017 的修补程序

### MSM {#msm-2}

* 在长时间索引更新期间，LiveCopyIndex 同步会导致线程阻塞。NPR-22214：适用于 CQ-90667 的修补程序
* 编辑 LiveCopy 中的其他字段时会禁用 cq:cugEnabled 属性，从而导致页面不受保护。NPR-22246：适用于 CQ-4236050 的修补程序
* 页面处于暂停状态时，“页面转出”操作无法更新子项。NPR-22483：适用于 CQ-4236956 的修补程序
* 转出已在母版中移动的结构会导致错误的 cq:moveTarget。NPR-22373：适用于 CQ-4232536 的修补程序

### 集成 {#integration-6}

* 尝试对选件选择器库中的选件进行排序时，导致出现异常行为。NPR-22208：适用于 CQ-4235439 的修补程序
* 在长时间运行的查询期间，TargetContentImpl 致使 AEM 运行缓慢。NPR-22361：适用于 CQ-4236907 的修补程序
* Target 引擎（mbox.js、at.js）不使用损坏的 URL，而是使用包含冒号的 URL，这在某些部署中可能会失败。NPR-22366：适用于 CQ-4237854 的修补程序
* 页面个性化需要对品牌节点具有发布权限。NPR-22370：适用于 CQ-4236895 的修补程序

### Foundation {#foundation}

* Apache Sling Scripting Sightly Models 使用提供程序包 **org.apache.sling.scripting.sightly.models.provider/1.0.18**。NPR-22614：适用于 Sling-5944、Sling-6866 的修补程序

### 项目 {#projects}

* 工作流启动程序无法接受字符串的 TypeHint 值。NPR-22436：适用于 CQ-4237855 的修补程序

### 翻译 {#translation-2}

* 调查预览功能存在的问题。NPR-22201：适用于 CQ-4223753 的修补程序

### 用户界面 {#user-interface-2}

* （经典 UI）即使关联的表单数据模型服务设置为空字段，组件也会显示默认值。NPR-21903：适用于 GRANITE-19744 的修补程序

### WCM - Foundation 组件  {#wcm-foundation-components-3}

* 发布指向 Adobe Campaigns 中的导入程序页面的 Live Copy 页面时出错。NPR-22470：适用于 CQ-4237164 的修补程序
* 打开体验片段编辑器时出现 JavaScript 错误。NPR-22598：适用于 CQ-4238415 的修补程序

### 工作流 {#workflow}

* Day CQ 工作流电子邮件通知服务会在每个 Mongo 节点为 WorkflowCompleted 通知和 WorkflowAborted 通知触发一封电子邮件。NPR-22486：适用于 CQ-4238172 的修补程序

## 表单 {#forms-6}

### Forms 附加组件包 {#forms-add-on-package-6}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

#### 自适应表单 {#adaptive-forms-4}

* 在 IE 11 与 Chrome 中，自适应表单中的下拉列表占位符值不一致。NPR-22405：适用于 CQ-4227096 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-6}

#### 安装 LCM {#install-lcm}

* 在安装程序和 LCM 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-22744

### 包含的功能包 {#feature-packs-included}

#### 进程管理 {#process-management}

* （HTML 工作区）用户声明任务后，将为该特定用户刷新队列计数，但不会为其他用户刷新队列计数，除非刷新页面。NPR-19778：适用于 CQ-4233665 的修补程序

### CFP14 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-cfp}

AEM 6.2 SP1-CFP14 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/6_2cfp14updated_bundles.txt)

AEM 6.2 SP1-CFP14 中包含的内容包列表

[获取文件](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
AEM 累积修补程序包 6.2 SP1-CFP13 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 将 AT.js 用作客户端库时，在“目标组件设置”中启用了“静态参数”字段配置。
* 修复了下拉组件的显示/隐藏功能。
* 修复了使用 Target 同步受众的问题。
* 增加了通信管理的多功能性，以允许使用特殊字符。

### 资产 {#assets-6}

* 版本清除无法删除旧版本的资产。NPR-21682：适用于 CQ-4212996 的修补程序
* 在可重新排序的文件夹下重新排序文件夹不会持久保留。NPR-21964：适用于 CQ-4231761 的修补程序

### 站点 {#sites-6}

* （触屏 UI）（经典 UI）HTL 和核心组件中存在多个跨站点脚本 (XSS) 漏洞。NPR-21532：适用于 CQ-4232305 和 CQ-4232511 的修补程序
* 在 Internet Explorer 11 中，无法正常对选定文本创建内容/设置内容格式（例如，指定/删除新的列表样式）。NPR-21533：适用于 CQ-4230689 的修补程序
* (Safari) 用户无法在资产查找器面板中查看所有资产。NPR-21981：适用于 CQ-4213720 的修补程序
* 时间扭曲返回“RecursionTooDeepException”错误且页面出现乱码，即使更改了日期也不会创建任何新版本。NPR-21707：适用于 CQ-4199536 的修补程序
* 在编辑器中加载页面时，会加载 WorkflowStatusprovider (pageinfo.json) 三次，从而导致 AEM 实例执行缓慢。NPR-21778：适用于 CQ-59232 的修补程序

### 集成 {#integration-7}

* 在 Target 创作模式下创建的移动设备类型和浏览器受众在 AEM 中不起作用。NPR-21676、NPR-21681：适用于 CQ-4232100 的修补程序
* 在刷新目标组件期间的高延迟下，可以在组件完全刷新之前添加其他选件。NPR-21744：适用于 CQ-4233158/CQ-4234293 的修补程序
* 用户在 mbox 调用中看不到测试静态参数值，而在云配置中使用 AT.js 作为客户端库进行测试时，则可以看到这些值。NPR-21930：适用于 CQ-4234520 的修补程序

### 平台 {#platform-4}

* 当用户或组数量较大时，用户同步出现性能问题。NPR-20431：适用于 CQ-4223282 的修补程序
* 使用 Sling Distribution 进行用户同步时未同步某些用户。NPR-21911：适用于 Granite-20404 的修补程序
* 阻止在搜索摘录中高亮显示停止词（在 Geometrixx 页面上）。NPR-21835：适用于 Granite-21067 的修补程序\
   注意：此修补程序需要 Oak CFP 1.4.20 或更高版本。

### 翻译 {#translation-3}

* 创建翻译项目时，启动程序用户 ID 缺少 jcr 属性。NPR-21715：适用于 CQ-4230713 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-4}

* 表单下拉组件的显示/隐藏功能无法按预期使用。NPR-22164：适用于 CQ-4235288 的修补程序

## 表单 {#forms-7}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-7}

#### 自适应表单 {#adaptive-forms-5}

* 自适应表单中存在 XML 外部实体注入 (XXE) 漏洞。NPR-21982：适用于 CQ-109878 的修补程序
* (iOS 11) 单击文件附件组件时，文件附件会打开相机而不是设备文件浏览器。NPR-21926：适用于 CQ-4214348 的修补程序
* 主题创建 UI 中缺少标题会导致异常情况，且无法呈现对话框。适用于 CQ-4236143 的修补程序

#### 通信管理 {#correspondence-management-1}

* 包含特殊字符的 xml 数据存在呈现问题。NPR-21712：适用于 CQ-4229137 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-7}

#### 汇编程序服务 {#assembler-service}

* 使用 6.2.0-ASM-1017-003 生成的 PDF 文件被损坏。NPR-21427：适用于 CQ-4228046 的修补程序

#### PDFG 服务 {#pdfg-service-1}

* 由于 PNG、JPEG 和 TIFF 文件中的意外页面大小 (PDF)，OCR 失败。NPR-19489：适用于 CQ-4209079 的修补程序

## CFP13 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-cfp-1}

AEM 6.2 SP1-CFP13 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/cfp13_bundlecompare-list.txt)

AEM 6.2 SP1-CFP13 中包含的内容包列表

[获取文件](assets/do-not-localize/cfp13_contentpackage-list.txt)

AEM 累积修补程序包 6.2 SP1-CFP12.1 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 改进了多值字段的元数据处理。
* 在翻译工作流中，支持多字符（两个以上）国家/地区代码。
* 改进了包含多个嵌套组件的页面的呈现。
* 改进了 AEM 与 Adobe Digital Publishing Suite 之间资产出版日期的同步。

### 资产 {#assets-7}

* OmniSearch 中的字符过多导致 AEM 服务器崩溃。NPR-21083：适用于 CQ-4223602 的修补程序
* 在元数据架构的多值字段中的第二个选项中指定的值未附加到 CRX-de 中先前指定的值。NPR-21220：适用于 CQ-4224526 的修补程序
* 在 Safari 上的资产中使用数字版权管理时，资产下载失败。NPR-21387：适用于 CQ-4230287 的修补程序

### 站点 {#sites-7}

* (DAM)（经典 UI）AEM CQ“创作”/“发布”快速启动中的某些 SWF 文件存在多个跨站点脚本 (XSS) 漏洞。NPR-21073、NPR-21074：适用于 NPR-20612 的修补程序
* 标记选取器不会翻译提供的多种语言的标记。NPR-21221：适用于 CQ-78855 的修补程序
* AEM 文章控制台存在呈现问题，因为使用多个嵌套组件使其变得缓慢。NPR-21271：适用于 CQ-4224158 的修补程序

### 集成 {#integration-8}

* 添加 Target 框架时，在编辑器的“选择模式”列表中无法使用“定位”模式。NPR-21047

### Mobile On-Demand {#mobile-on-demand-1}

* (Digital Publishing Suite) AEM 中作品集的出版日期与 Folio Producer 中显示的日期不匹配。NPR-21145

### MSM {#msm-3}

* 删除 LC 中的第一个本地页面后，Live Copy 重置进程将停止。NPR-21276：适用于 CQ-4229743 的修补程序

### 平台 {#platform-5}

* 升级到 AEM 6.3 后，未找到引用作为脚本实施的标记的自定义 taglib。NPR-20149：适用于 Granite-18433 的修补程序

### 翻译 {#translation-4}

* 翻译工作流失败，因为 lang_country 代码超过 2 个字符。NPR-21088：适用于 CQ-4197439 的修补程序
* 在翻译项目完成之前，不应允许将资产页面再次提交到该项目。NPR-21219：适用于 CQ-4209908 的修补程序

### 用户界面 {#user-interface-3}

* 选择组件不会在表单提交过程中删除目标属性。NPR-21163：适用于 GRANITE-14125 的修补程序
* 展开 HTTP.encodePathOfURI 会对加号“+”进行双重编码。NPR-21417：适用于 GRANITE-16340 的修补程序

### 漏洞 {#vulnerability-4}

* DAM 元数据编辑器中存在跨站点脚本 (XSS) 漏洞。NPR-21434：适用于 CQ-83472 的修补程序
* 多个 SWF 文件容易遭受跨站点脚本 (XSS) 攻击。NPR-20612：适用于 CQ-4213297 的修补程序

## 表单 {#forms-8}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-8}

#### 通信管理 {#correspondence-management-2}

* (IE 11) 加载完整的 UI 后，HTML 内容的初始呈现仅在左侧进行，而右侧会间歇性地加载。NPR-21554
* 安装 AEM 6.2 SP1-CFP9 后，将禁用信件预览提交按钮。NPR-21547
* 选择资产链接类型时，“资产选择器”窗口未在“编辑信件数据绑定”向导中打开。NPR-21164：适用于 CQ-4194567 的修补程序
* 要编辑内嵌或可编辑的文本模块，请点按相关的“编辑”图标，或在信件预览中双击相关文本模块。NPR-21402

#### 自适应表单 {#adaptive-forms-6}

* AEM Forms 提交按钮组件显示 type=&quot;button&quot;，而不是 type=&quot;submit&quot;。NPR-21007
* 在为可重复面板添加新面板或删除面板时，数据会持久保留。NPR-21408

### Forms JEE 安装程序 {#forms-jee-installer-8}

#### 核心 {#core-2}

* 升级到最新的 Java 8 Update 131 会引发以下异常：“JsafeJCE 提供程序已禁用，FIPS 140 要求的自身完整性检查失败”。NPR-21355

   **注意：**&#x200B;此 NPR 需要其他设置，有关详细信息，请参阅[最新的 Java 8 更新](release-notes-aem-6-2-cumulative-fix-pack.md#latest-java-update-throws-an-exception-npr)。

* 在核心、加密、签名以及文档安全中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21360、NPR-21361、NPR-21356、NPR-21358

#### 安装 LCM {#install-lcm-1}

* 在安装程序和 LCM 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21362

#### PDFG 服务 {#pdfg-service-2}

* 在 PDFG 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21359

#### 进程管理 {#process-management-1}

* （HTML 工作区）启用列大小调整功能，使名称类别在显示时不会被截断。NPR-19770：适用于 CQ-4233668 的修补程序

#### Reader 扩展服务 {#reader-extensions-service-1}

* 在 RE 中，将 Jsafe Jar 更新为 Cryptoj 6.1.3.1。NPR-21357

## CFP12.1 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-cfp-2}

AEM 6.2 SP1-CFP12.1 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

AEM 6.2 SP1-CFP12.1 中包含的内容包列表

[获取文件](assets/do-not-localize/cfp12_contentpackage-list.txt)

AEM 累积修补程序包 6.2 SP1-CFP11 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 更新了 cq-msm-core，以实现有效的 Livecopyindex 同步。
* 提高了内容片段的编辑效率。
* 在包管理器中提供验证选项,以检测 ACL 权限。
* 引入了营销活动功能，可为客户通信包含电子邮件 ID。
* 增强了 Dynamic Media 文件的视频编码功能。
* 修复了 Sightly 组件和 LiveCopy。

### 资产 {#assets-8}

* 对于名称中包含空格的文件，Dynamic Media 视频编码失败。NPR-20818：适用于 CQ-102469 的修补程序
* AEM CQ“创作”/“发布”快速启动中的某些 SWF 文件存在多个跨站点脚本 (XSS) 漏洞。NPR-21071、NPR-21072
* 用户无法下载包含免责声明和长文件名的资产。NPR-20255：适用于 CQ-4222139 的修补程序

### 站点 {#sites-8}

* AEM 与 Campaign 集成：特殊链接在 Adobe Campaign 中被重写，从而阻止客户在电子邮件中发送 mailto: 超链接。NPR-20787：适用于 CQ-4225760 的修补程序
* （触屏 UI）将语言设置为法语时，出现 AEM 可用性问题和性能问题。NPR-20854：适用于 CQ-4227628 的修补程序
* 在 RTE 中使用链接插件关联已编码的资产文件时，会返回空链接。NPR-20626、NPR-21059：适用于 CQ-4223011 的修补程序
* 内容片段元数据编辑器阻止内容作者保存对内容片段的更改。NPR-20641：适用于 CQ-4224755 的修补程序
* 页面属性别名导致“请求发布/请求取消发布”。NPR-20731：适用于 CQ-4226227 的修补程序
* 在 RTE 元素中进行链接编码时出现文本组件问题。NPR-20755：适用于 CQ-4224321 的修补程序

### 平台 {#platform-6}

* ResourceResolverImpl.map() 不调用 ResourceDecorator。NPR-20788：适用于 GRANITE-19718 的修补程序
* org.apache.sling.i18n.DefaultLocaleResolver 无法通过 org.apache.sling.engine.SlingRequestProcessor 处理请求。NPR-20706：适用于 CQ-94880 的修补程序
* 请求在包管理器中添加验证选项，以检测特定包上是否有任何 ACL 权限/特权被更改。适用于 CQ-4229196 的修补程序

### 集成 {#integration-9}

* (Search&amp;Promote) 内容包的筛选器定义不明确会导致安装时路径被覆盖。NPR-20808：适用于 CQ-4227615 的修补程序

### 工作流 {#workflow-1}

* AEM 生产服务器部署存在稳定性问题。NPR-20979：适用于 Granite-19104 的修补程序

### 项目 {#projects-1}

* （触屏 UI）无法将团队成员添加到项目。NPR-20990：适用于 CQ-4205375 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-5}

* Sightly 图像组件“link to”因缺少 .html 扩展名而生成 403 错误。NPR-20823：适用于 CQ-4195909 的修补程序
* 在使用 LiveCopy 的 Blueprint 站点上，当尝试删除表单组件时，会引发空指针异常并添加回表单组件，而不是删除组件。NPR-20855：适用于 CQ-4204628 的修补程序
* 在长时间索引更新期间，LiveCopyIndex 同步会导致线程阻塞。NPR-20634：适用于 CQ-90667 的修补程序

### 安全 {#security}

* 主动 XSS 库更新。NPR-21174
* 升级到 Apache Commons Email 1.5，它提供了用于发送电子邮件的简化 API。NPR-20509：适用于 Granite-18240 的修补程序
* 对 Apache Sling XSS Protection API 应用了安全修补程序，以消除绕过 XSS 攻击的可能性。NPR-21290：适用于 GRANITE-19924 的修补程序
* 在 XSSAPI#getValidHref 函数中绕过 XSS 攻击。NPR-21174：适用于 Granite-19924 的修补程序

### 移动应用程序 {#mobile-apps}

* 修复了 AEM 中 OOTB 资产的 curl Head 请求问题。NPR-20511：适用于 CQ-4221520 和 CQ-103024 的修补程序

## 表单 {#forms-9}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

AEM Forms 的主要功能亮点包括：

* 为 Workbench 用户启用了证书身份验证。
* 修复了通信管理、HTML5 表单以及 AEM Forms 工作区的可用性问题。

### Forms 附加组件包 {#forms-add-on-package-9}

#### HTML5 表单 {#html-forms-1}

* iOS 10 和 11 设备上的涂写组件存在可用性问题。NPR-21092

#### 通信管理 {#correspondence-management-3}

* （通信 UI）单击一下后，会禁用提交按钮。NPR-21078

### Forms JEE 安装程序 {#forms-jee-installer-9}

#### 汇编程序服务 {#assembler-service-1}

* docConverter 无法生成 PDF/A，出现“未绑定‘stEvt:action’元素的前缀‘stEvt’”错误。NPR-21032：适用于 CQ-4222540 的修补程序
* 调用服务 OMPFSubmission/PDFA/PDFtoPDFA 时，触发名称为 java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE 的异常。这会导致短暂的签名验证过程在重新启动服务器之前无法完成。NPR-20792

#### Workbench {#workbench}

* 为 Workbench 用户启用证书身份验证。NPR-17548：适用于 CQ-4214486 的修补程序

#### 进程管理 {#process-management-2}

* 使用 dataref 参数呈现移动设备表单时，会多次调用准备数据进程。NPR-19801：适用于 CQ-4230427/CQ-4230400 的修补程序

## CFP11 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-cfp-3}

AEM 6.2 SP1-CFP11 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

AEM 6.2 SP1-CFP11 中包含的内容包列表

[获取文件](assets/do-not-localize/cfp11_contentpackage-list.txt)

AEM 累积修补程序包 6.2 SP1-CFP10 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 添加了一个新的实用程序函数 onDialogLoaded 以用于测试目的。
* 向 ClientLibraryProxyServlet 添加了前端单元测试和配置。
* 修复了多个图像就地编辑器组件中的性能问题。
* 更新了 Apache Sling JCR ResourceBundleProvider 中的配置。

### 资产 {#assets-9}

* 如果禁用了资产更新工作流，将无法预览资产。NPR-20543：适用于 CQ-4204986 的修补程序
* 在 granite: class 属性 (cq-damadmin-admin-assets-upload) 中添加的类存在呈现问题。NPR-20514：适用于 CQ-4219238 的修补程序
* 标题中包含特殊字符的缩略图资产在 alt 属性中显示 java 对象。NPR-20347：适用于 CQ-4223620 的修补程序
* 由于许可问题，使用 Adobe 专有代码替换版本比较代码。NPR-20273：适用于 CQ-4223758 的修补程序
* 上传具有多个 Alpha 层的 CMYK PSB 文件时出现处理问题。NPR-20251：适用于 CQ-4220869 的修补程序
* 除非在 org.apache.sling.i18n 2.5.6 中重新启动服务器，否则国际化词典不起作用。NPR-20525：适用于 Granite-19490 的修补程序
* 没有根据使用默认线程转储收集器配置（默认的 AEM 启动）设置的计划程序时间段生成任何线程转储。NPR-20288：适用于 GRANITE-19488/GRANITE-12741/CQ-90647 的修补程序。

### 站点 {#sites-9}

* 如果在打开保存的搜索后，修改的日期筛选器发生了更改，则对结果没有影响，显示的结果与修改的日期筛选器以前保存的值相同。NPR-19739：适用于 CQ-4219425 的修补程序
* 包含嵌套组件的页面加载失败。NPR-20312
* 删除工作流包时，会触发“请求删除”工作流。NPR-20266：适用于 CQ-4221686 的修补程序
* （触屏 UI）使用操作系统剪贴板和内部 AEM 剪贴板执行复制/粘贴操作时出现问题。NPR-20228：适用于 CQ-4220383 的修补程序
* 加载多个资产（超过 100 个）时，列表视图中的 AEM 实例运行缓慢。NPR-20034：适用于 CQ-4222695 的修补程序
* （触屏 UI）通过经典 UI 控制台删除启动项会使所有页面无法编辑。NPR-20520：适用于 CQ-4225074 的修补程序
* “目标”下拉列表不适用于对话框中的多个 RTE 组件。NPR-20345：适用于 CQ-4220981 的修补程序

### 平台 {#platform-7}

* 使用匿名会话进行访问时，ClientLibraryProxyServlet 不会将请求代理到发布实例上的客户端库，并引发“HTTP 404 未找到”错误。NPR-20195：适用于 Granite-14409 的修补程序

### 集成 {#integration-10}

* 选择目标引擎作为 Adobe Target，会阻止组件加载，并在服务器日志中引发错误。NPR-20058：适用于 CQ-88071、CQ-109698、CQ-4201600 的修补程序

### 商务 {#commerce-1}

* 创建同一页面的产品时，不显示确认或重定向弹出消息。NPR-20257：适用于 CQ-4223414 的修补程序

### 用户界面 {#user-interface-4}

* 如果日期选取器是多字段中的某个字段，则在编辑组件时，不会保留日期字段中保存的值。NPR-20077：适用于 GRANITE-19147 的修补程序
* 如果触发连续查询导致不正确的结果，之前的查询不会被中止。NPR-20397：适用于 GRANITE-19306 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-6}

* 即使从多个图像就地编辑器组件中删除图像后，ImageMap 属性也仍然存在。NPR-20142：适用于 CQ-4222982 的修补程序

## 表单 {#forms-10}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-10}

#### 自适应表单 {#adaptive-forms-7}

* 当通过 UI 更改时，为 DropDownList 执行 valueCommit 脚本两次。NPR-19989：适用于 CQ-110212 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-10}

**进程管理**

* CFP 包中包含 AEM Forms HTML 工作区版本 2.2.26。NPR-20099
* 将移动设备表单配置为以 PDF 格式查看时，预填充的表单不起作用。NPR-20566

**权限管理**

* CAC/双向身份验证证书选择对话框应显示证书，并将增强型密钥用法 (EKU) 作为客户端身份验证或智能卡登录。NPR-20708
* Forms JEE 支持 PKCS#11 双向身份验证。NPR-15001

## CFP10 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-cfp-4}

AEM 6.2 SP1-CFP10 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list-cfp10.txt)

AEM 6.2 SP1-CFP10 中包含的内容包列表

[获取文件](assets/do-not-localize/contentpackage-list-cfp10.txt)

AEM 累积修补程序包 6.2 SP1-CFP9 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 改进了 Analytics 经典 UI 配置以进行密钥输入。
* 修复了 ContextHub 的独立持久性缓存。
* 准确计算资产维度。
* 优化了将资产发布到 Brand Portal 时的 AEM 性能。
* 修复了画布节点中的 Resourcetype 值。
* 为文档片段内容启用了区分大小写和特殊字符搜索功能。
* 增强了自适应表单功能，可将 PDF 作为附件附加到 Safari 中。\
   提供了可连接到新 Dynamic Media 发布基础架构的新 Dynamic Media，以实现更快速、更灵活的复制。

### 资产 {#assets-10}

* AEM Assets 无法提取 InDesign 资产的子资产引用，包括指向资产的重复链接。NPR-19006：适用于 CQ-4204186 的修补程序
* 排序选项不适用于商务下的收藏集内的资产。NPR-19508：适用于 CQ-4213622 的修补程序
* 当某个与预先存在的资产具有相同名称的资产被移动到同一位置时，资产的 cq: lastReplicationAction 值会在二者之间交换，这会导致创建错误的元数据。NPR-19531
* 发布大量资产时，尽管所有资产均正确发布，仍会显示一条错误消息。NPR-19629：适用于 CQ-4219611 的修补程序
* 静态呈现版本以固定尺寸列出，且不反映实际呈现版本的大小。NPR-20004
* 将多个资产（超过 4 个）发布到 Brand Portal 时，AEM 实例运行缓慢。NPR-20009

### 站点 {#sites-10}

* 当用户尝试发布/取消发布/创建被另一用户锁定的页面版本时，AEM 会出现意外行为。NPR-19249：适用于 CQ-4215298 和 CQ-4203856 的修补程序
* 手动提升嵌套启动项时，子页面将被删除。NPR-19704
* 在初始化过程中 ContextHub 存储覆盖默认持久层时出现持久性问题。NPR-19979：适用于 CQ-4218399 的修补程序
* 内容片段与其他按钮重叠。NPR-19980：适用于 CQ-4221519 的修补程序
* 在 SiteAdmin 中使用别名查看时，不显示站点页面。NPR-20053：适用于 CQ-4221478 的修补程序
* 发布指向 Adobe Campaigns 中的导入程序页面的 Live Copy 页面时出错。NPR-20066：适用于 CQ-4220846 的修补程序

### 平台 {#platform-8}

* 已将 Apache POI 升级到版本 3.16，以支持在呈现版本中包含 PPT 幻灯片的背景图像。NPR-18286
* 上传同一文件夹中的多个资产时，Internet 浏览器 11 和 Edge 出现渲染问题。NPR-20062

### 集成 {#integration-11}

* 使用匿名用户访问时，自定义 at.js 文件不会发布。NPR-19542：适用于 CQ-4219592 的修补程序
* 将 Analytics 现有凭证迁移到 WSSE 身份验证。NPR-19962

### Brand Portal {#brand-portal}

* 启用通过 tagadmin/tagging 控制台将标记从 AEM 发布到 Brand Portal 的功能。NPR-20271

## 表单 {#forms-11}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

### Forms 附加组件包 {#forms-add-on-package-11}

#### 通信管理 {#correspondence-management-4}

* 启用了预览信件时在文档片段中搜索实际文本的功能。NPR-19712

#### 自适应表单 {#adaptive-forms-8}

* 增强了自适应表单功能，可将 PDF 作为附件附加到 Safari 中。为了在现有表单中支持相同功能，我们需要更改附件小部件和“支持的文件类型”中的配置，更新值 application/pdf 以替代 .pdf。NPR-19623

#### 表单管理器 {#forms-manager-1}

* 如果在自适应表单的字段中未定义 validationState 但发生了 elementFocusChanged 事件，则错误事件 (errorState) 会返回到 Adobe Analytics 服务器。NPR-19513

### Forms JEE 安装程序 {#forms-jee-installer-11}

#### 核心 {#core-3}

* 关闭期间连接管理器不可用。在取消部署创作 EAR 之前，Jboss 切断了 JDBC 依赖项，从而导致损坏问题。NPR-19703

## 包含的功能包 {#feature-packs-included-1}

* 改进了 Dynamic Media 中的缩略图校正和透明度。NPR-15207

## CFP9 中包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-in-cfp-5}

AEM 6.2 SP1-CFP9 中更新的内容包列表

[获取文件](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

AEM 6.2 SP1-CFP9 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

AEM 累积修补程序包 6.2 SP1-CFP8 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 在 Adobe 电子邮件模板服务中为自定义用户模板引入了标记。
* 增强了桌面应用程序中的触屏 UI 按钮。
* 单击时禁用了提交按钮，以防止在翻译页面上提交多个表单。
* 在对话框中配置了多个 RTE 组件。
* 增强了 Live Copy 中的 ReferenceUpdates。
* 为文档片段内容启用了区分大小写的搜索功能。
* 向 AEM Forms 安装文档中添加了 Linux 库列表。

### 资产 {#assets-11}

* 在 Safari 浏览器上对智能收藏集应用 Omnisearch 筛选器时出现问题。NPR-19511
* 当有多个与 PDF 资产关联的关键字时，PDF 关键字元数据无法正确提取，并且会以错误方式修改。为解决该问题，已删除 PDF 资产的“主题”字段元数据属性。但是，您可以编辑元数据架构，为“主题”字段添加多值文本字段。NPR-19126
* 工作流通知服务不对电子邮件中的链接进行编码，这会导致用户在单击链接后，无法加载链接。NPR-19490：适用于 CQ-4218055 的修补程序
* 无法使用 Chrome 在列视图中加载页面/资产的完整列表。NPR-19458：适用于 CQ-4214248 的修补程序
* 激活“请求激活”工作流时，AEM 收件箱中显示不正确的关闭时间图标。NPR-19365：CQ-4216174
* 在列表视图中排序时出现问题。NPR-19217：CQ-95602
* 在“资产文件夹”设置中更改标题或缩略图图片时，文件夹的原始组和权限会被覆盖。NPR-19283：适用于 CQ-4216080 的修补程序
* Windows 10 工作站自动切换到触控模式，导致某些按钮无法正常使用。NPR-19183

### 站点 {#sites-11}

* 在对话框中包含多个 RTE 组件时出现问题。NPR-19311：NPR-19587
* 初始化 VersionManagerImpl 后，原版 AEM 6.2 中的自动版本清除只运行一次。NPR-19315：适用于 CQ-4217175 的修补程序
* 在“Salesforce.com 导出”工作流步骤中，工作流实例卡住。NPR-19222：适用于 CQ-4212976 的修补程序
* 无法编辑从 Live Copy 创建的语言副本页面。NPR-18967
* ReferencesUpdateAction 无法通过层次结构更改将链接更新到嵌套 LiveCopy 中。NPR-18715：适用于 CQ-4214105 的修补程序

### 平台 {#platform-9}

* Adobe 电子邮件模板服务会将标记添加到自定义用户模板。NPR-19190：适用于 CQ-4217113 的修补程序

### 项目 {#projects-2}

* 项目编辑者无法将资产复制/粘贴到项目资产文件夹中。NPR-19619
* 安装 6.2 SP1-CFP1 后，无法生成翻译项目的预览。NPR-16481：CQ-4204655

### 集成 {#integration-12}

* 在经典 UI 上的 Adobe Digital Publishing Solution 中，文章的访问属性设置不正确。NPR-19366
* 由于 AEM 文章控制台中的全尺寸文章，缩略图呈现缓慢。NPR-19086：CQ-4217148
* 如果用户可以访问多个区域，通过 Campaign 个性化选件时，会出现自动折叠的错误行为。NPR-19290：适用于 CQ-4218029 的修补程序
* 如果对定位模块进行编辑并保存超过一次，则定位模式下不显示定位对话框。NPR-19144：适用于 CQ-4216708 的修补程序

### 工作流 {#workflow-2}

* 用户无法在经典 UI 的收件箱中按用户/组筛选收件箱中的通知。NPR-19122：适用于 CQ-4215374 的修补程序
* 图像映射未保留 HTL 图像组件中的选定坐标。NPR-18911：CQ-4211584

## 表单 {#forms-12}

* AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-12}

* 从 Microsoft Word 或 Web 浏览器将内容复制到通信管理器文本编辑器时，会丢失内容的样式。NPR-19530
* 文本编辑器中不含换行符的内容不会自动换行。NPR-19481
* 启用了预览信件时在文档片段中搜索实际文本的功能。NPR-17792：适用于 CQ-4214501 的修补程序

#### 通信管理 {#correspondence-management-5}

>[!NOTE]
>
>文本片段的这项搜索功能具有一些限制：
>
>* 文档片段内容区分大小写，但标题不区分大小写。
>* 如果搜索词的一部分采用不同的样式或包含特殊字符（如 &quot;、&#39; 或 \），则搜索结果不会高亮显示。
>* 搜索不适用于文档片段中的动态内容（例如数据词典元素值或变量值）。


#### 表单管理器 {#forms-manager-2}

* 在 AEM 6.2 上应用 CFP6 后，无法编辑自适应表单的 XML 架构属性。适用于 CQ-4219684 的修补程序
* 重新启动服务器时，AEM Forms 管理器核心包的所有服务不启动。适用于 CQ-4217014 的修补程序

### Forms JEE 安装程序 {#forms-jee-installer-12}

#### 安装 LCM {#install-lcm-2}

* 安装 CFP6 后，Microsoft Windows 上的管理员屏幕显示版本号为 6.0。适用于 CQ-4217573 的修补程序

## 包含的功能包 {#feature-packs-included-2}

* 增强了桌面应用程序中的触屏 UI 按钮。NPR-18676

## CFP8 中包含的 OSGi 包 {#osgi-bundles-included-in-cfp}

AEM 6.2 SP1-CFP8 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/updated-bundles-list-cfp8.txt)

AEM 6.2 SP1-CFP8 中更新的内容包列表

[获取文件](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

AEM 累积修补程序包 6.2 SP1-CFP7 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 对于将 dc: title 属性设置为 String []（多字段）的图像，在图像卡片上显示标题时发生行为更改。
* 修复了 Dynamic Media 云服务、触屏 UI 和安全 UI 界面的性能问题。
* 修复了 Apache Felix Http Bridge 3.0.8 中的问题。
* 解决了创作与发布环境之间的无二进制复制 (BLR) 问题。
* 支持目标库文件 AT.js，这是用于与 Adobe Target 进行客户端集成的实施库，专为典型的 Web 实施和单页应用程序而设计。
* 通过为 Marketing Cloud 解决方案（Analytics、DTM、Target 以及 S&amp;P）引入用户可配置的连接超时时间段，提高了 AEM 性能。

### 资产 {#assets-12}

* 在使用配置了 Dynamic Media 云服务的 AEM 6.3 测试视频摄取时，会导致出现“打开的文件过多”异常。NPR-18734：适用于 CQ-4211407 的修补程序
* 重新启动 AEM 实例后，页面上资产的“虚 URL”设置不起作用。NPR-18634：适用于 Granite-18085 的修补程序
* 在触屏 UI 中，会向没有资产发布权限的用户显示“发布”按钮。NPR-18620：适用于 CQ-4214042 的修补程序
* 为资产设置许可协议后，资产的下载对话框中不存在动态呈现版本选项。NPR-18607：适用于 CQ-4212342 的修补程序
* 无法为名称中包含空格的资产下载动态呈现版本。NPR-18571：适用于 CQ-4211738 的修补程序
* 与 Creative Cloud 共享资产文件夹时，无法保存多个用户。NPR-18489：适用于 CQ-103297 的修补程序
* dc: title 和 dc: description 在 crx/de 中不会更改为多字段值。NPR-18474：适用于 CQ-4209086 的修补程序
* 移动资产操作导致性能下降。NPR-18346
* 在设置了默认“显示全部”选项的情况下打开时间轴时，时间轴中未显示任何项目。NPR-18302：适用于 CQ-4211957 的修补程序
* 将 ASCII/UTF-8 编码文本文件上传到 AEM Assets 时出现错误，并且缩略图生成失败。NPR-18006：适用于 CQ-4209345 的 CFP
* 即使用户没有复制权限，也会显示“发布”操作按钮。NPR-17353：适用于 CQ-4209269 的修补程序
* 使用 min:gcc;obfuscate=true 启用缩小功能后，Siteadmin 和 Miscadmin 无法运行。NPR-18593：适用于 CQ-4209220 的修补程序
* 每次刷新屏幕之前，不会显示自定义菜单项。NPR-18500：适用于 CQ-4213581 的修补程序
* 将 moment.js 升级至 2.10.6。NPR-18596：适用于 Granite-11881 的修补程序
* 对 DM 宏应用权限，会中断管理员用户的视图。NPR-18544：适用于 CQ-4211729 的修补程序
* 稍后发布资产会引发非法参数异常。CQ-4214532

### 站点 {#sites-12}

* 在具有 MongoDB 的双活作者群集上，当时间达到为内容设置的“按时”时，两位作者都会尝试为同一内容触发复制。NPR-18708：适用于 CQ-4210982 的修补程序
* 使用不含 jcr: 内容节点的引用移动资源时，会引发空指针异常。NPR-18664
* 占位符在包含多个 Parsys 组件的页面中不可见。NPR-18645：适用于 CQ-110253 的修补程序
* AbstractCopyMoveCommand 中存在并发问题。NPR-18591
* 将文本从另一个 AEM 实例复制到 Parsys 组件时，将创建 Parsys，而不设置任何 resourceType。NPR-18511：适用于 CQ-4212306 的修补程序

### 平台 {#platform-10}

* 安装包后，JCR 安装程序不更新包版本。NPR-18728：适用于 NPR-15135 的修补程序
* 在创作与发布环境之间对二进制文件执行无二进制复制 (BLR) 失败。NPR-18704
* 请求在 AEM 环境中解析 Apache Felix Http Bridge。NPR-18297
* 当使用 Sling Content Distribution 同时复制具有相似结构的多个页面时，复制失败。NPR-18665：适用于 Granite-13712 的修补程序
* Sling 分发包正在构建，但未自行清理。NPR-18601：适用于 Granite-16183 的修补程序

### 集成 {#integration-13}

* 查看从库文件夹发布的选件时，导致出现空指针异常。NPR-18732：适用于 CQ-4214593 的修补程序
* 当从特定日期更改为“激活时”/“停用时”时，JCR 和 Target 中的活动开始日期/结束日期不会更新。NPR-18612：适用于 CQ-104831 的修补程序
* Analytics 与 AEM 的集成没有为 httpclient 连接设置连接或套接字超时。NPR-18497
* DTM 与 AEM 的集成没有为 httpclient 连接设置连接或套接字超时。NPR-18495
* Target 与 AEM 的集成没有为 httpclient 连接设置连接或套接字超时。NPR-18494
* Search &amp; Promote 与 AEM 的集成没有为 httpclient 连接设置连接或套接字超时。NPR-18493
* 添加额外体验后，Target 活动被停用。NPR-18227：适用于 CQ-4201895 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-7}

* 图像映射未保留 HTL 图像组件中的选定坐标。NPR-18530：适用于 CQ-4211584 的修补程序

### 翻译 {#translation-5}

* 翻译搜索结果中未包含翻译项目的名称。NPR-18224：适用于 CQ-4210658 的修补程序

### Brand Portal {#brand-portal-1}

* 启用通过 tagadmin/tagging 控制台将标记从 AEM 发布到 Brand Portal 的功能。CQ-4212165

## 表单 {#forms-13}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-13}

#### 通信管理 {#correspondence-management-6}

* 在保存片段之前，编辑面板中不会显示正确的数据。NPR-19092
* 将文档片段添加到信件需要大量时间。NPR-18958
* 如果数据 xml 文件中存在 XML 声明，并且通过 POST 请求启动信件呈现，则相应的信件无法显示数据。NPR-18870
* 对 CM 资产采取的操作不会生成审核日志。NPR-16618

>[!NOTE]
>
>如果您受到以下两个问题的影响，请不要安装此 CFP 附加组件包：
>
>* 从 Word/Web 复制并粘贴内容到 CM 文本编辑器时，内容中显示换行符。NPR-19530
>* CM 文本编辑器中无换行符的内容不会自动换行。NPR-19449

>
>
这些问题将在以后的 CFP 中解决。

#### 自适应表单 {#adaptive-forms-9}

* 为可重复面板添加新面板时，将删除上一个面板中下拉字段的值。NPR-18772
* 标记为仅接受整数的自适应表单字段，也接受从数字键盘输入的几个特殊字符。NPR-18680
* 用于在 guideroot 面板的初始化事件中更改按钮标题的脚本不起作用。NPR-18476
* 对于在规则编辑器下创建的规则，在右侧面板中看不到滚动条。NPR-18716

#### AEM Forms 应用程序 {#aem-forms-app}

* 当 AEM Forms 应用程序处于脱机模式或未连接到网络时，表单无法在该应用程序中正确呈现。CQ-4218368

### Forms JEE 安装程序  {#forms-jee-installer-13}

#### PDFG 服务 {#pdfg-service-3}

* PDF 生成器无法生成具有指定书签级别的 PDF 文档。适用于 CQ-4211102 的修补程序

## CFP7 中包含的 OSGi 包 {#osgi-bundles-included-in-cfp-1}

AEM 6.2 SP1-CFP7 中包含的 OSGi 包列表

[获取文件](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

AEM 6.2 SP1-CFP7 中更新的内容包列表

[获取文件](assets/do-not-localize/cfp7_content_packages.txt)

AEM 累积修补程序包 6.2 SP1-CFP6 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 在平板电脑中的布局模式下有效管理隐藏的组件。
* 在混合设备上引入快速操作。
* 解决 Live Copy 的组件级同步问题。

### 资产 {#assets-13}

* 当没有所需权限的用户尝试对资产执行移动操作时，客户会被阻止。NPR-18330：适用于 CQ-4212560 的修补程序
* 合并多个智能内容服务配置会导致可用性问题。NPR-18273：适用于 CQ-4201557 的修补程序
* 在“资产”文件夹中添加了大约 80 个片段后，无法从“时间轴”控制台中使用签出操作/工作流。NPR-18257：适用于 CQ-4211214 的修补程序以及 NPR-18251：适用于 CQ-4211216 的修补程序。
* 资产报告期间系统崩溃，出现“内存不足”和“缺少分页”错误。NPR-17865：适用于 CQ-4209759 的修补程序
* 发布的视频无法在已编码的视频资产上播放。NPR-17849：适用于 CQ-4210739 的修补程序
* 不会生成 PDF 的缩略图。NPR-17831、NPR-17750：适用于 CQ-4210547 的修补程序
* Adobe CQ DAM 到期通知作业不会停用已过期的资产。NPR-17666：适用于 CQ-107766 的修补程序
* 如果资产没有分配所有者，将停止资产到期活动。NPR-17665：适用于 CQ-4197946 的修补程序
* 移动具有超过 150 个传入引用的资产文件夹时，会引发空指针异常。CQ-4200981

### 站点 {#sites-13}

* 为 IP 范围设置分段规则后，个性化仅适用于第一个 IP。NPR-18121：适用于 CQ-83767 的修补程序
* 启用 historyShow 属性后，登录因 NumberFormatException 而失败。NPR-18073：适用于 CQ-101965 的修补程序
* 触屏 UI 中显示标记的已删除页面。NPR-18025：适用于 CQ-86694 的修补程序
* 加载包含大量（2000 及以上）受众的页面时，出现性能问题。NPR-17884：适用于 CQ-4209567 的修补程序
* 删除页面上的其他图像后，无法选择图像。NPR-17711：适用于 CQ-4201323 的修补程序

### 平台 {#platform-11}

* 对于没有所需权限的用户，触屏 UI 控件不会隐藏。NPR-17945：适用于 CQ-4211231 的修补程序
* 标记选取器字段中缺少日文标记。NPR-17768：适用于 CQ-4210456 的修补程序
* 启用 FastQuerySize 后，getsize() 查询返回错误结果。NPR-18018
* 备用实例上的 Web 控制台不可访问。NPR-17861：适用于 Granite-14582 的修补程序

### 商务 {#commerce-2}

* 当目录 Blueprint 没有为区域定义任何条件时，会发生查询遍历。NPR-18229：适用于 CQ-4211924 的修补程序

### 社区 {#communities-2}

* PollingImporterImpl. 会延迟关闭 AEM。NPR-18298：适用于 CQ-96133 的修补程序

### 集成 {#integrations}

* 解决了在 AEM Day HTTP Client 3.1 OSGi 配置了需要摘要身份验证的代理时可能发生的 AEM 搜索组件错误。NPR 18128
* 缺少用于还原继承的复选框。NPR-17753：适用于 CQ-4210139 的修补程序请求
* 当定位一个具有多个活动的组件时，用户无法设置优先级。NPR-18658：适用于 CQ-4210727 的修补程序
* 用户无法浏览文件夹 /etc/segmentation 以选择在文件夹 /etc/segmentation/group1 下创建的受众。NPR-18522

### 安全 {#security-1}

* 如果用户没有目标文件夹的写入权限，“移动资产”向导会挂起。NPR-18300
* 请求使用 Apache Sling API 中的升级版 org.apache.sling.servlets.post Servlet (2.3.22) 来预先制止 XSS 漏洞。NPR-18963

### 翻译 {#translation-6}

* 在翻译项目完成之前，不应允许将资产页面再次提交到该项目。NPR-18249：适用于 CQ-4209908 的修补程序

### WCM - Foundation 组件 {#wcm-foundation-components-8}

* 无法在可编辑的模板中使用 WCM Foundation iparsys 组件。NPR-18223：适用于 CQ-4210384 的修补程序
* 图像映射未保留 HTL 图像组件中的选定坐标。NPR-18032：适用于 CQ-4211584 的修补程序
* 当 HTL 图像组件呈现时，URL 中的文件名将重命名，从而导致 URL 断开。NPR-17908：适用于 CQ-4211587 的修补程序
* 进行更改后无法退出“页面属性”。NPR-17832：适用于 CQ-96110 的修补程序

## 表单 {#forms-14}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 [AEM Forms 发行版](aem-forms-releases.md)。

### Forms 附加组件包 {#forms-add-on-package-14}

**通信管理**

* 在信件呈现过程中，数据词典会被重复读取。NPR-18482：适用于 CQ-4210805 的修补程序
* 为 com.adobe.livecycle.content 类添加了 JavaDocs。NPR-18467
* 创建信件时，信件说明未保存。NPR-18039
* 当文本模块已保存且文本模块中的表达式不包含开放或闭合的表达式标记时，未显示错误消息。文本模块显示错误消息，并且无法在信件中呈现。NPR-17798
* 在安装附加组件包时，日志中出现意外错误。NPR-18295

**表单管理器**

* AEM Forms UI 按照时间以升序（最早的排在最前面）列出所有资产。用户无法按照时间以降序（最新的排在最前面）重新排列资产。NPR-18451

### Forms JEE 安装程序  {#forms-jee-installer-14}

**输出服务**

* 改进了 AEM Forms 6.2 输出服务的性能问题。NPR-18033

**签名服务**

* 无法使用远程硬件安全模块对 PDF 文档进行签名。NPR-18017

## CFP6 中包含的 OSGi 包 {#osgi-bundles-included-in-cfp-2}

AEM 6.2 SP1-CFP6 中更新的 OSGi 包列表

[获取文件](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

AEM 6.2 SP1-CFP6 中更新的内容包列表

[获取文件](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

AEM 累积修补程序包 6.2 SP1-CFP5 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 解决了共享、移动、发布和下载资产的几个 UI 问题。
* 增加了“移动”对话框在显示引用资产时的容量。
* 解决了与 WCM 组件和工作流（例如取消发布和版本清除）相关的几个问题。
* 改进了操作栏在显示工具栏操作和 Coral 组件方面的响应性。

### 资产 {#assets-14}

* 改进了“发布至 Brand Portal”功能的性能。NPR-17189：适用于 CQ-4204150 的修补程序
* 使用“共享链接”选项共享资产时，不会创建具有平面文件夹结构的 zip 文件以供下载。NPR-17513：适用于 CQ-4209381 的修补程序
* 选择 DAM 中的资产并单击“发布”时，“资产详细信息”页面中不显示“发布至 Brand Portal”选项。NPR-17351：适用于 CQ-94905 的修补程序
* 在 DAM 工作流步骤中，必须在最终块中关闭从会话或资源解析器获取的二进制流，以确保不会发生资源泄漏。NPR-17385：适用于 CQ-4209452 的修补程序
* 在 DAM 中上传 Word 文档会引发空指针异常，并且工作流实例停留在“正在运行”状态。NPR-17160：适用于 CQ-4207358 的修补程序
* 非管理员用户可以在元数据编辑器页面上看到已过期资产的“共享”、“移动”、“发布”和“下载”按钮。NPR-16903：适用于 CQ-101440/CQ-104535 的修补程序
* 在“资产”控制台中，应向管理用户显示“共享”、“移动”、“发布”和“复制”等操作。NPR-16902：适用于 CQ-4207111 的修补程序

### 站点 {#sites-14}

* 使用经典 UI 和触控 UI 移动页面时，“移动”对话框显示的引用不超过 150 个，从而导致用户无法更新这些引用和重新发布页面。通过为经典 UI 引入“maxRefNo”属性，此问题已得到修复，该属性可在 siteadmin 节点“/libs/wcm/core/content/siteadmin”上配置。该属性指定在执行大量移动操作之前显示的最大引用数（默认值是 150）；如果页面的引用数超过该数值，则这些引用不会显示在 movePage 对话框中。此配置还适用于 damadmin 和 miscadmin，方法是分别在 `'/libs/wcm/core/content/damadmin'` 和 `'/libs/wcm/core/content/miscadmin'` 节点上应用配置。NPR-17222：适用于 CQ-85878 的修补程序

* 使用 WCM 组件时，带有空格的超链接在触屏 UI 富文本编辑器中会被删除。NPR-17698、NPR-17570：适用于 CQ-4206768 的修补程序
* 从页面属性触发“请求取消发布”工作流时，会向没有复制权限的用户显示 JavaScript 错误。NPR-17294：适用于 CQ-102064 的修补程序
* 呈现或导出 HTL 图像组件会将 URL 更改为数字，并重命名文件名，从而导致链接断开。NPR-17245：适用于 CQ-59616 的修补程序
* 删除嵌套启动项中的启动项，会导致子启动项变得孤立。NPR-17228：适用于 CQ-4202639 的修补程序
* 在应用了 Oak 1.4.13 的 AEM 6.2 中运行版本清除，会导致日志中持续不断地反复出现警告。NPR-17391：适用于 CQ-4206870 的修补程序
* 在安装 ContextHub 组件的修补程序或升级后，内容包将覆盖 /etc/segmentation/contexthub 中的所有区段，从而导致所有自定义 ContextHub 区段丢失。NPR-17250：适用于 CQ-79958 的修补程序
* 在以嵌套组作为工作流用户运行工作流时，WorkflowStatusProvider (pageinfo.json) 会导致工作流实例锁定。NPR-17555：适用于 CQ-4202056 的修补程序
* 使用 WCM 页面编辑器组件时，在创作实例的触屏 UI 编辑模式下，页面末尾存在大量空白。NPR-17510：适用于 CQ-4205441 的修补程序
* 呈现或导出 HTL 图像组件会将 URL 更改为数字，从而导致链接断开。NPR-17245：适用于 CQ-59616 的修补程序

### UI {#ui}

* 在慢速连接中，选择资产并单击“开发人员工具”并不总是会在操作栏中显示工具栏操作，并且必须重新加载页面。NPR-17568：适用于 CQ-108365 的修补程序
* 操作栏应更新为使用两个容器：coral-actionbar-primary 和 coral-actionbar-secondary，而不是一个 coral-actionbar-container。NPR-17591：适用于 GRANITE-15225 的修补程序

### Mobile On-Demand {#mobile-on-demand-2}

* 对 AEM Mobile 应用程序具有“只读”权限的用户无法从 AEM Mobile 内容管理页面预览内容。NPR-17390：适用于 CQ-4209690 的修补程序

### 安全 {#security-2}

* HTMLRendererServlet 生成的输出中存在 XSS 漏洞。NPR-17136
* 请求防止在 AEM Web 整合信息源页面中披露 AEM 版本。NPR-16219

### 表单 {#forms-15}

#### Forms 附加组件包 {#forms-add-on-package-15}

AEM Forms 修补程序通过随发行版一起提供的附加组件包和其他补丁安装程序进行交付。有关详细信息，请参阅 AEM Forms 发行版。

**自适应表单**

* 对于带有附件的自适应表单，在第二次提交表单时，将会在提交的 XML 中创建 afSubmissionInfo 标记的重复条目。NPR-17364
* 使用 Google Chrome 浏览器时，在从表单中删除附件后，尝试再次重新附加同一附件会引发错误。NPR-17297
* 如果基于 XSD 或基于无表单模型的自适应表单中存在嵌套的可重复延迟加载面板，则在表单中填充的值不会保留在记录文档 (DOR) 中。NPR-17176
* 错误日志中显示的有关规则编辑器的错误应添加到 try/catch 块 JavaScript 代码的 catch 块中。NPR-16757
* 单击表单中的文件附件，会引发浏览器控制台错误，并且不显示附件预览。NPR-17174

**通信管理**

* 如果在 UI 中添加了内嵌文本或空白行，则“创建通信”UI 功能会损坏。NPR-17748
* 打开信件进行编辑时，浏览器闪烁。NPR-17576
* 在数据词典计算元素中添加远程函数时，如果函数数量大于显示远程函数的选项卡的长度，则滚动条不会显示在选项卡中。NPR-17359
* API 方法 import com.adobe.icc.services.api.LetterInstanceService 不起作用。NPR-17922、NPR-16008
* 编辑信件时，在文本模块中添加的变量未显示在“数据绑定”面板中。NPR-17940
* 当 HTML 提交操作使用 POST 方法时，通信管理 UI 不会启动。NPR-17595

**表单管理器**

* 如果为 AB 测试配置了自适应表单，则单击“开始 AB 测试”不会开始测试，并且会引发浏览器控制台错误。NPR-17838

**表单服务**

* 应修复 OSGi 表单的静态代码分析中报告的问题。NPR-13951

#### Forms JEE 安装程序 {#forms-jee-installer-15}

**输出服务**

* 使用 AEM Forms 6.2 输出服务将特定表单与数据 XML 合并所花费的时间，是使用 LiveCycle ES4 SP1 服务器执行相同操作所花费的时间的 20 倍。已在 Windows 和 Linux 环境中修复该问题。NPR-17501

**安装 LCM**

* 安装 AEM Forms 6.2 GM 版并应用 AEM 6.2 CFP 后，运行 LiveCycle 配置管理器会在版本信息中显示一个多余的分号，并且不会更新修补程序安装日期。NPR-14322

**进程管理**

* 没有为 AEM Forms 进程填充 TaskContext 变量。CQ-4211857

#### AEM Forms JEE 包 {#aem-forms-jee-bundles-package}

* 无论使用 JEE 管理员 UI 控制台还是 OSGi 控制台，表单用户的功能都应相同。NPR-17670

### CFP5 中包含的功能包 {#feature-packs-included-in-cfp}

**Forms JEE 包**

流程管理 - HTML 工作区

* 在分配工作区步骤中，如果有多个附件或注释，工作区附件选项卡应显示附件或注释的计数器。NPR-17771
* 请求在 AEM JEE Forms 中支持 Office 365，以便在表单工作流中提供电子邮件功能。NPR-13866

**Forms 附加组件包**

通信管理

* 预览信件期间在文本编辑器中编辑片段时，应显示已处理的文本（而不是片段中使用的内嵌条件）以进行编辑。NPR-15748、NPR-17504

### CFP5 中包含的 OSGi 包 {#osgi-bundles-included-in-cfp-3}

AEM 6.2 SP1-CFP5 中更新的 OSGi 包列表

[获取文件](assets/do-not-localize/cfp5_osgi_bundles.txt)

AEM 6.2 SP1-CFP5 中更新的内容包列表

[获取文件](assets/do-not-localize/content-package-cfp5.txt)

AEM 累积修补程序包 6.2 SP1-CFP4 是一个重要更新，它包括自 AEM 6.2 SP1 正式发布以来的一些关键客户修补程序。

此累积修补程序包的主要功能亮点包括：

* 修复了 Camera Raw 文件呈现版本的资产、时间轴视图和图像方向问题
* 改进了

   * 站点的 WCM 启动项
   * 项目工作流
   * ContextHub 组件

* 修复了营销活动、Mobile On-Demand 和翻译问题
* 改进了自适应表单规则编辑器的可用性
* 增强了表单中通信管理的内嵌条件编辑器
* 修复了 JEE 上的 AEM Forms 的进程管理和输出服务问题
* 修复了脚本编辑器的 Forms Designer 相关问题

### 平台 {#platform-12}

* 配置云服务后，Search&amp;Promote 搜索表单会忽略 `environment` 设置，使其在创作实例上不可用。NPR-16594：适用于 CQ-4206076 的修补程序
* 通过在 /apps 中叠加来向&#x200B;**资产 OmniSearch** 结果添加列或自定义列不起作用。NPR-16737：适用于 CQ-4206785 的修补程序
* 从 AEM 6.1 SP2 就地升级到 AEM 6.2 SP1 后，**诊断工具**页面无法正常运行。NPR-17121：适用于 CQ-4196786 的修补程序
* HTL：在选择论坛、创建主题和帖子时，`Sightly SightlyCompiledScript` 会将不正确的 `addSelectors` 属性添加到 `RequestDispatcherOption`。NPR-17008：适用于 GRANITE-16384 的修补程序

* 在 `ReportImporter` 使用的 `ManagedPollConfigs` 中添加了对 `CRON expressions` 的支持。NPR-16608：适用于 CQ-4206066 的修补程序请求

* 为 LDAP 用户上传头像图片失败。NPR-16561：适用于 Granite-17013 的修补程序
* 在卡片视图和列表视图中，“用户管理”屏幕上显示的结果数不同。NPR-16241：适用于 GRANITE-16914 的修补程序
* 在 Google Chrome 浏览器的“全屏”模式下查看时，工作流通知无法延迟加载。NPR-17013：适用于 CQ-4207567 的修补程序

### 资产 {#assets-15}

* 在导入已定义方向的图像时，无法正确应用图像方向。NPR-16750：适用于 CQ-4204356 的修补程序
* 资产时间轴视图不显示任何资产，即使默认情况下设置为“显示全部”也是如此。NPR-16957：适用于 CQ-98780 的修补程序
* 将 Camera Raw 文件（包括 ARW、CR2、NEF、DNG 和 EPS）作为呈现版本添加到资产中后，无法选择或删除这些文件。当用户单击这些文件时，会自动下载这些文件。NPR-16949：适用于 CQ-4206846 的修补程序
* 在资产 UI 中的一个 PDF 内部创建另一个 PDF 时，不会在 DAM UI 中显示已创建的 PDF，但是这些 PDF 在 CRX 存储库中均可见。NPR-16833：适用于 CQ-4206501 的修补程序
* 使用触屏 UI 将资产上传为其自身的直接子节点会导致出现问题。资产会作为先前选定的资产的直接子级上传。NPR-16534：适用于 CQ-4204287 的修补程序
* 在 DAM UI 中，对资产添加注释以及在注释中标记用户，不会生成邮件通知。NPR-16589：适用于 CQ-102318 的修补程序

### 项目 {#projects-3}

清除工作流后，“项目”工作流控制台会在页面上显示空指针异常。NPR-17017：适用于 CQ-4194269 的修补程序

### 站点 {#sites-15}

* 在创作实例上，`ContextHub` 中的文件不会最小化。NPR-17022：适用于 CQ-79456 的修补程序
* WCM 启动项提升需要较长时间，才能提升包含大型页面树的启动项。NPR-16480：适用于 CQ-82731 的修补程序
* 当使用非有效或未完成的规则创建区段（或受众）时，`ClientContext` 区段条件呈现器崩溃。NPR-16759：适用于 CQ-4205104 的修补程序
* 在 WCM 启动项中，当从触屏 UI 的页面属性中启动操作时，与启动项关联的页面不会取消发布。NPR-16560：适用于 CQ-4204681 的修补程序
* 链接重写程序错误地重写了包含冒号的 href 值，它假定冒号“:”定义的是 JCR 命名空间。NPR-16753：适用于 CQ-4203762 的修补程序
* 在 WCM 设计导入程序中，如果之前上传了某个 zip 文件后将其删除，则打开测试导入程序页面并再次尝试上传该 zip 文件会导致出现问题。NPR-16486：适用于 CQ-90962 的修补程序
* 使用 Firefox、Safari 和 Google Chrome 浏览器导航到&#x200B;**[!UICONTROL 全局导航]**&#x200B;窗格时，会获得不同的用户体验。Firefox 浏览器显示&#x200B;**[!UICONTROL 工具]**&#x200B;菜单，而 Google Chrome 浏览器则显示&#x200B;**[!UICONTROL 导航]**&#x200B;菜单。NPR-16770：适用于 CQ-4200456 的修补程序

### 营销活动 {#campaign}

* 测试 AEM 营销活动模板和修改种子地址以包含“其他数据”时，Adobe Campaign 下拉列表会在触屏 UI ContextHub 中消失。NPR-16771：适用于 CQ-105748 的修补程序

### Mobile On-Demand {#mobile-on-demand-3}

* 当从 AEM 创作环境预检发布时，超过 5 秒的预检操作会在 AEMM - AEM PECS 集成 Splunk 功能板上引起异常峰值，导致每秒出现大量状态请求。NPR-16908：适用于 CQ-4207055 的修补程序
* 安装 AEM-6.2-SP1-CFP1-1.0 更新后，AEM Mobile 配置管理失败。NPR-16909：适用于 CQ-4204892 的修补程序

### 翻译 {#translation-7}

* 安装 6.2 SP1-CFP1 后，无法预览翻译作业。NPR-16481：适用于 CQ-4204655 的修补程序
* 使用“翻译”创建的语言副本指向“根母版”，而不是本地国家/地区 LiveCopy。NPR-17257：适用于 CQ-4208287 的修补程序

### 安全 {#security-3}

* 将文件的二进制文件上传到 AEM 后，不执行 MIME 类型验证。NPR-16617
* 上传 LDAP 用户的头像图像时出现问题。NPR-16561

### 表单 {#forms-16}

#### Forms 附加组件包 {#forms-add-on-package-16}

**自适应表单**

* 在自适应表单编辑器中，head.jsp 中的 Target 设置注释应替换为新的 ContextHub 语句。NPR-17173
* 在自适应表单规则编辑器中，**[!UICONTROL 选择项目]**&#x200B;将事件显示为“null”。NPR-17139
* 使用前进箭头 (>) 向前导航时，已提交的表单会重新提交。NPR-17080
* 通过 AJAX 提交自适应表单时，如果发生错误，永远不会调用“error”回调函数。NPR-17034
* 在运行时单击规则编辑器中的&#x200B;**[!UICONTROL 保存表单]**&#x200B;按钮不会保存表单。NPR-16905
* 应从自适应表单的 Tab 键顺序中排除静态文本。NPR-16749
* 十进制字段的计算值显示不正确。NPR-16596
* 显示帮助内容的图标应包含在自适应表单的 Tab 键顺序中。NPR-16484
* 支持在“**[!UICONTROL 默认预填充服务配置]**”中使用 `dataRef=C:/Users/` 类型的正则表达式，用于预填充自适应表单的数据。NPR-16425

* 如果存在嵌套延迟加载情况，则无法正确触发所有面板的验证。NPR-15821

**通信管理**

* 如果信件包含空文本模块（一个没有任何文本的模块），则信件呈现会失败。NPR-17054
* 在文本编辑器中粘贴内容后，会从内容中删除换行符和制表符空格。NPR-17039
* 如果文本模块在多个信件中被引用，则文本模块的引用显示会花费较长时间。NPR-17035
* 编辑、保存、删除和设置文档片段的引用需要较长时间。NPR-17033
* 预览信件时，两端对齐的文本将以不同字体呈现。NPR-16976
* 如果搜索的文本多次出现，则搜索功能无法正常运行。NPR-16920
* 文本编辑器工具栏间歇性地显示在浏览器中。NPR-16919
* 规则编辑器中的&#x200B;**[!UICONTROL 保存表单]**&#x200B;结构不起作用。NPR-16905
* 使用 Internet Explorer 创建基于数据词典的文本模块时，“字体”下拉列表不填充字体系列。NPR-16944
* 创建文本片段后，在预览信件时，信件字体发生更改。NPR-16830
* 文档片段中开头或表达式之间含有制表符空格的信件无法呈现或预览。NPR-16769

**移动设备表单**

* 移动设备表单预览显示重叠的内容，但是可以正确显示表单以呈现 PDF。NPR-17105

**Forms Portal**

* 单击已提交表单的&#x200B;**[!UICONTROL 下载]**&#x200B;链接，会打开 HTML 页面而不是 PDF 表单。NPR-17082

* 对于已提交的实例，文件附件的 `Upload Comments` 不会显示在 UI 中，但是它们存在于 CRX 存储库内所存储的 XML 中。NPR-17075

**Reader 扩展服务**

* 在 AEM Forms OSGi 安装中，特定文件未进行 Reader 扩展。NPR-16625

#### Forms JEE 安装程序  {#forms-jee-installer-16}

**核心**

* 在升级过程中，配置管理器因超时而失败。NPR-16774（请参阅[为组件级别的操作配置超时](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)）。

**流程管理 - HTML 工作区**

* “启动”任务的起始点不是以在起始点提交的数据开头。NPR-16917
* 单击 HTML 工作区中某个表单的&#x200B;**[!UICONTROL 返回]**&#x200B;按钮，不会关闭该表单，而是会将其返回到“组队列”。\
   NPR-16352

**进程管理**

* 允许用户将以前任务的显示名称设置为进程实例中的任何后续任务。NPR-15382

**输出服务**

* 输出服务无法处理以下 PDF：修改为在 `date-time format` 元数据中包含附加“milli-sec”字段。NPR-16838

#### Forms Designer {#forms-designer}

* AEM Forms Designer 脚本编辑器不采用 `Calculate Event` 和 `Validate Event` 的“表单属性”默认值。NPR-15921

### CFP4 中包含的功能包 {#feature-packs-included-in-cfp-1}

**Forms 附加组件包**

* 增强了通信管理的内嵌条件编辑器。NPR-10981

### CFP4 中包含的 OSGi 包 {#osgi-bundles-included-in-cfp-4}

在 AEM 6.2 SP1 与 CFP4 之间更新的 OSGi 包列表

CFP3 的主要功能亮点包括：

* 使用需要摘要身份验证的代理，提高了经典 UI 和 AEM 搜索组件的搜索功能效率。
* 修复了上传资产和显示资产元数据时出现的问题
* 修复了在标题中含有特殊字符的情况下，创建文件夹和移动页面时出现的问题。
* 修复了在触屏 UI 中使用定位同步受众、发布营销活动，以及选择目标量度的问题
* 解决了翻译作业的同步问题
* 增强了表单预填充服务的安全性
* 改进了 Forms Portal 草稿和提交组件以及条形码表单服务
* 改进了包含文件附件小部件或延迟加载片段的自适应表单的可用性。
* 改进了“通信管理”的可用性，包括增强的搜索功能、记录已删除的资产，以及导入数据词典。

### 平台 {#platform-13}

* 当两个线程尝试注入相同字段时，可能会出现 **ModelAdapterFactory** 争用情况，进而导致无法构建模型。NPR-16443：适用于 SLING-6584 的修补程序
* 包管理器中的验证选项，用于检测 /apps 下叠加的文件（JSP 或 JavaScript 文件）与 /libs 下的修补程序中包含的此类文件之间是否存在任何冲突。然后，受影响的叠加可以重新设置为包含对 /libs 下文件的更改。NPR-16216：适用于 CQ-81729 的修补程序
* 启动发布程序后，error.log 中的日志记录有时会停止几秒钟，需要清除才能再次运行。请求更新日志记录框架并提供 Sling 日志记录。NPR-15913：适用于 Granite-15452 的修补程序
* 请求更新 JavaScript `use"` API，以避免 HTL JavaScript Use API 实施失败。NPR-16461：适用于 SLING-6780 的修补程序

### 站点 {#sites-16}

* 从 AEM 6.0 升级到 AEM 6.2 后，在搜索标记时，因大量查询而导致经典 UI 性能缓慢。要解决此问题，可执行[在标记控制台中禁用复制状态（经典 UI）](release-notes-aem-6-2-cumulative-fix-pack.md#disable-replication-status-in-tagging-console-classic-ui-npr)中所述的步骤。NPR-15842：适用于 CQ-4201748 的修补程序.

* 在触屏 UI 中创建页面时，“name”字段的输入检查不检查特殊字符“撇号”（与经典 UI 中的情况相同）。因此，无法移动页面。NPR-16404：适用于 CQ-4205321 的修补程序。
* 在富文本编辑器中对两行应用不同样式后将两行合并，会删除应用于第二行的样式。NPR-16389：适用于 CQ-4203835 的修补程序.
* 在触屏 UI“站点”屏幕中，无法尝试将页面粘贴到不含子页面的页面中，因为不显示“粘贴”按钮。NPR-15894：适用于 CQ-4201696 的修补程序.
* 在内容查找器面板中滚动“页面”选项卡时，经典 UI 中会无限显示几组页面，而触屏 UI 则仅显示有限的少数几个非重复页面。NPR-16271：适用于 CQ-4202371 的修补程序
* 在触屏 UI 中打开 LiveCopy 的“页面属性”并单击“保存”（不进行任何更改）时，会写下任何 LiveCopy 选项卡并创建一个 LiveSync 配置节点。NPR-16327：适用于 CQ-108562 的修补程序
* 表单约束无法读取 `ConstraintMessage` 属性。NPR-16388：适用于 CQ-101330 的修补程序
* `wcm/foundation/components/parsys` 组件未显示“**[!UICONTROL 将组件拖动到此处]**”占位符。NPR-16748：适用于 CQ-4205187 的修补程序

### 资产 {#assets-16}

* 安装 6.2 SP1 或修补程序 12430 后，PDF 光栅器停止工作并导致内存不足问题。NPR-15991
* 字符串属性 `documentNumber` 的元数据显示为日期，然而它应该是数字。NPR-16134：适用于 GRANITE-16916 的修补程序
* 时间轴事件气球中的文本截断。NPR-16226：适用于 CQ-85226 的修补程序
* 在内容层次结构下创建标题中含有特殊字符的文件夹时，会显示特殊字符的编码形式。NPR-15935：适用于 CQ-4202987 的修补程序
* 由于使用“创建”按钮时显示的行为不一致，用户在浏览资产时无法上传资产或创建文件夹。NPR-16410：适用于 CQ-4204793 的修补程序
* 在 AEM 创作中，从文章视图上传共享的 HTML 资源时出现意外错误。NPR-16133：适用于 AEMM-4155970 的修补程序

### 集成 {#integration-14}

* 启用需要摘要身份验证的代理身份验证时，AEM 搜索组件会引发 ConcurrentModificationException。NPR-15309：适用于 CQ-4199191 的修补程序
* 在 AEM 中创建 Target A/B 测试活动时，受众未同步到 Target 且显示“无受众”。NPR-16229：适用于 CQ-4204210 的修补程序
* 安装 SP1+NPR-11577 v1.2 后，在触屏 UI 中定位时，如果为目标量度选择“使用 Analytics 量度”，则永远无法加载量度的下拉列表。NPR-16129：适用于 CQ-4204316 的修补程序
* 使用定位时，发布营销活动不会自动发布整个树，包括品牌和母版。NPR-15855：适用于 CQ-94630 的修补程序

### 翻译 {#translation-8}

* 同步翻译作业不会自动触发，并且在未存入翻译项目的情况下，AEM 轮询不会发生。NPR-15163：适用于 CQ-90856 的修补程序

### 表单 {#forms-17}

#### Forms 附加组件包 {#forms-add-on-package-17}

**自适应表单**

* 在保存带有附件的自适应表单时，附件的完整路径（而不是附件的名称）会添加到生成的 XML 的 `fileAttachment` 标记中。NPR-16529
* 在基于 XDP 的自适应表单中，提交的 XML 中存在 `afData/afBoundData` 包装器，即使预填充 XML 不包含 `afData/afBoundData` 包装器也是如此。NPR-16118

* 数字字段中的指数表示法：使用自适应表单时，如果输入的数字的十进制小数总计超过十个字符，则该数字在提交的 XML 中将会变成指数符号。NPR-16106
* 对于同时包含文件附件组件和延迟加载片段的表单，提交的数据 xml 不包含文件附件组件的信息。NPR-16022
* 对于没有可重复父项的延迟加载可重复面板，面板的第二个实例中的可重复子项无法重复。NPR-15944
* 尝试在表单编辑器中将一个片段保存在另一个片段内时，片段模型根不填充子片段的值。NPR-15943
* 当创建仅包含一个项目的复选框，然后尝试显示复选框标题并隐藏项目标题时，如果项目文本为空，则创建词典操作会引发 `ArrayIndexOutOfBoundException`。此时不会创建词典，且屏幕上也不会生成错误响应。NPR-15816
* 对于带有文件附件小部件的自适应表单，在预览附加的文件后，表单的某些部分会被禁用。\
   NPR-16611

* 对于允许使用多个附件的文件附件小部件，如果在含有先前附件的小部件上提交了一个具有附件的新表单实例，则在打开添加的附件时将会显示错误代码，而不是实际内容。NPR-16258
* 保护表单预填充服务免遭通过 `file://`、`http://` 和 `ftp://` 之类的协议进行的未经授权访问。请参阅“[使用配置管理器配置预填充服务](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)”。NPR-15414

* 请求在“验证”步骤中以 PDF 格式而不是 HTML 格式呈现自适应表单，并将所有附件附加到 PDF，以便打印输出可显示完整表单。NPR-9011

**通信管理**

* 在“预览”/“编辑”模式下处理信件中的文本片段时，如果文本转换为列表，则将损坏整个信件功能，并生成 JavaScript 错误。NPR-16460
* 导入 XSD 文件以在“通信管理”节点中创建数据词典时失败，因为每次上传 XSD 并选中根节点后，浏览器均无响应。此问题与浏览器无关，不会显示在服务器日志中。NPR-16452
* 使用 Internet Explorer 浏览器预览信件并尝试编辑内容的字体大小时，在字体大小下拉列表中看到从 8 到 72 的重复值。NPR-16387
* 如果浮动字段显示为 XDP 片段中的输入字段，则在使用 Internet Explorer 浏览器预览信件时，该字段不会展开。NPR-16367
* 尝试直接从预览提交信件时，信件名称的弹出窗口由于被隐藏而无法正确显示。NPR-16353
* 编辑信件时添加的行空格未反映在预览窗口中。对于文本片段中的列表，PDF 输出不显示正确的间距。NPR-16267
* 使用 Internet Explorer 浏览器处理文本文档片段时，尝试为文本提供缩进失败，因为光标不允许文本缩进。NPR-16128
* 在现有文本文档片段中添加或修改数据词典需要很长时间，并且不会始终通知用户。NPR-16102
* 使用 Internet Explorer 浏览器预览包含可滚动内容的信件时，浏览器滚动条与信件的滚动条重叠，并且无法在右侧查看片段的整个内容。NPR-16068
* 使用 Google Chrome 浏览器创建或编辑文本文档片段时，颜色选择下拉列表会自动弹出，并且无法删除。用户需要选择列表作为数据条目类型才能编辑片段。NPR-16067
* 使用 Letterinstance API 时，`import com.adobe.icc.services.api.LetterInstanceService` 方法不起作用。NPR-16008
* 在资产编辑器配置中将日期显示格式更改为 `locale=en_US; dateFormat=MMM dd,yyyy;`，无法按预期起作用，并且日期格式会显示为乱码。NPR-16007
* 即使之前设置的方式不同，重新创作时，信件中的数据链接类型也会显示为“用户”。NPR-16619

**Forms门户**

* 草稿和提交组件的升级方案不适用于数据库示例实施。NPR-16752

**条形码表单服务 (BCF)**

* 条形码表单服务 (BCF) 的静态代码分析报告问题。NPR-13855

#### Forms JEE 安装程序  {#forms-jee-installer-17}

**流程管理 - HTML 工作区**

* 保护表单预填充服务免遭通过“file://”、“http://”和“ftp://”之类的协议进行的未经授权访问。有关详细信息，请参阅[使用配置管理器配置预填充服务](https://helpx.adobe.com/aem-forms/6-2/prepopulate-adaptive-form-fields.html#main-pars_header_944235754)。NPR-15434

**用户管理 **

* 在 AEM 6.2 服务器上，SAML 登录屏幕显示不正确的版本 (6.1.0)。NPR-13825
* 在为 AEM Forms 配置了单点登录 (Kerberos) 身份验证的情况下，如果用户在尝试登录时身份验证失败，则会返回错误代码“404”。仅在刷新页面后，用户才会被重定向到登录站点。NPR-15015

#### Forms设计师{#forms-designer-1}

* 在 AEM Forms Designer 中，无法将词典拼写检查中的表单区域设置更改为“法语（加拿大）”。\
   NPR-15896

### CFP3 中包含的功能包 {#feature-packs-included-in-cfp-2}

**Forms 附加组件包**

* 在通信管理中删除任何资产时，error.log 文件中应记录一条警告消息。NPR-13225
* 增强在通信管理中预览信件时的搜索功能，以便能够在文本片段内容中搜索文本，而不是只搜索信件标题或标签。NPR-16103

### CFP3 中包含的 OSGi 包 {#osgi-bundles-included-in-cfp-5}

在 AEM 6.2 SP1 与 CFP3 之间更新的 OSGi 包列表

[获取文件](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt)
累积修补程序包 2 的主要功能亮点包括：

* AEM 平台中的稳定性修复和性能改进，包括 Sling 框架和操作
* 通过修复若干有关访问、移动、搜索、上传和发布资产的问题，改进了资产管理
* 通过修复内容片段、锚点插件、幻灯片以及 ContextHub 组件中的问题，改进了站点创作和管理
* 修复了触屏 UI 中的若干问题，其中涉及文本编辑器、Omnisearch 和变量创建过程
* 改进了翻译工作流；增强了 Microsoft Connector，以便为 Azure 门户使用新的翻译 API
* 修复了项目和营销活动中的问题
* 通过修复自适应表单、通信管理和 Forms Portal 功能中的问题，改进了创作和管理
* 修复了 Forms JEE 核心、XTG 和 HTML 工作区组件中的问题

### 平台 {#platform-14}

* 如果编辑直接引用 Sling 框架的页面，则会触发 `SlingPostProcessor`。NPR-15754：适用于 CQ-104153 的修补程序

* 导航到页面组件时，经典 UI 对话框中不会获取具有 `tagBasePath` 属性的标记的值。NPR-15543：适用于 CQ-4199950 的修补程序

* 执行 Sling 操作时，如果有一个名为“chunk_n_n-1”的块，则 `SlingFileUpload handler.getLastChunk` 会陷入包含空块的无线循环。NPR-15455：适用于 SLING-5701 的修补程序

* 当一个接口扩展另一个接口时，超级接口上的可注入方法无法正确注入。NPR-15202：适用于 SLING-5710 的修补程序
* 使用 `com.adobe.granite.infocollector.impl.FilesTraversal` 函数调用时，无法阻止潜在的空指针异常。NPR-15169：适用于 CQ-4197640 的修补程序
* 某些辅助节点的工作流状态不一致，并且在为该节点调度观察事件时显示错误。NPR-15701：适用于 GRANITE-13786 的修补程序
* 当用户在 CRXDE 中选择节点（例如 /content/dam/），然后选择“访问控制”选项卡时（确保存在访问控制列表），拖放某些元素会移动除选定元素之外的其他元素。NPR-15696：适用于 GRANITE-16300 的修补程序
* 在尝试模拟时从下拉列表中选择用户，会导致整个用户弹出窗口消失。NPR-15774：适用于 CQ-4201738/GRANITE-11895 的修补程序
* 在 Omnisearch 中，无法按包含自动填充建议的标记进行搜索。NPR-15088：适用于 GRANITE-14426 的修补程序。\
   注意：此修补程序需要 Oak CFP 1.4.11 或更高版本。

### Mobile AEM 创作 {#mobile-aem-author}

* 将 AEM Mobile 和 ContentSync 包与混合应用程序一起使用时，AEM 会使用最早的包来响应应用程序发出的获取请求（带有时间戳），而不是使用应用程序请求的包。NPR-15749：适用于 CQ-104153 的修补程序

### 站点 {#sites-17}

* 如果用户在激活工作流后修改页面，则 WCM Core 中工作流收件箱的修改状态不会更改。NPR-15684：适用于 CQ-4196974 的修补程序
* 在用户单击锚点图标并添加名称后，触屏 UI 富文本编辑器中的锚点插件会生成不合规的 HTML5。它应在锚点元素的 HTML5 标记中添加“id”属性，而不是“name”属性。NPR-15650：适用于 CQ-89782 的修补程序
* 创建具有大量字段的元数据架构并将其应用于内容片段元数据后，内容片段元数据屏幕上不会创建滚动条，从而导致这些字段无法编辑。NPR-15478：适用于 CQ-4202622 的修补程序
* 编辑 `TagInput` 字段组件不会显示以前针对对话框字段配置的值。NPR-15464：适用于 CQ-4200360 的修补程序

* 在内容片段编辑器 UI 中，如果创建了内容片段的多个变量，则侧面板不会显示用于导览所有变量的滚动条。NPR-15445：适用于 CQ-4199444 的修补程序
* 从直接组中删除用户后，这些用户会添加到继承的组。NPR-15400：适用于 CQ-98758 的修补程序
* WCM 创作：触屏 UI 创作不允许编辑名称中带有逗号的页面。NPR-15396：适用于 CQ-4199723 的修补程序
* 使用触屏 UI 进行创作时，函数 `Granite.author.editableHelper.doSelectParent` 以错误的顺序传递参数，从而导致 JavaScript 错误。NPR-15349：适用于 CQ-4198594 的修补程序
* 即使存在选择禁用 Cookie，ContextHub 区段仍会显示体验。NPR-15293：适用于 CQ-4198024 的修补程序
* 经典 UI 中的“幻灯片放映”组件无法创建幻灯片或拖放图像以创建新幻灯片。NPR-15281：适用于 CQ-4194164 的修补程序
* 在站点管理控制台中，无论权限如何，都会向用户显示各种“创建”选项，例如“创建页面”、“创建站点”、“创建 Live Copy”、“创建启动项”和“创建目录”菜单项。NPR-15278：适用于 CQ-94436 的修补程序
* 安装 AEM 6.2 Service Pack 1 后，“包括子页面”滑块停止用于页面启动项。NPR-15230：适用于 CQ-4198449 的修补程序
* 请求增强版本清除功能，以便以块形式获取和处理版本，并且还能将指定的路径用于 XPath 查询。NPR-15186：适用于 CQ-109205 的修补程序
* “站点”组件的“页面属性”缩略图选项卡上缺少“清除”按钮。NPR-15143：适用于 CQ-4196997 的修补程序
* 对于使用 Live Copy 的站点，在站点管理控制台的“列”窗格中选中“Live Copy”复选框不会正确显示 Live Copy 状态，而只显示 HTML 标记。NPR-15108：适用于 CQ-97086 的修补程序
* 编辑内容片段时，如果用户在收到 Post 响应之前单击“完成”（“√”）以完成编辑，则无法正确保存已编辑的内容。NPR-15014：适用于 CQ-4194095 的修补程序
* 在“时间扭曲”模式下关闭“编辑”页面并尝试从 Siteadmin 重新打开该页面时，会导致出现状态为“500”的错误，而不是重新打开页面。NPR-14965：适用于 CQ-109647 的修补程序
* 在 Digital Asset Manager (DAM) UI 中，“用户选取器查找可授权项”搜索会导致“内存不足”异常。NPR-15307：适用于 CQ-98542 的修补程序

### 资产 {#assets-17}

* 在 Omnisearch 中搜索资产后，选择资产并尝试通过单击“查看属性”来编辑属性，然后单击“保存”按钮，会将用户重定向到空白页面。NPR-15900：适用于 CQ-4202372 的修补程序
* 资产用户界面不响应事件。选择资产并单击“发布”或“呈现版本”不会执行任何活动。NPR-15828：适用于 CQ-4202247 的修补程序
* 从卡片视图发布资产时，除非刷新页面，否则卡片不会更新以反映已发布状态。NPR-15826：适用于 CQ-102732 的修补程序
* 包含资产修补程序的累积修补程序。NPR-15225
* 如果资产文件夹的名称中包含与号（“&amp;”）字符，则在导航到资产时，文件夹名称无法正确显示。NPR-15775：适用于 CQ-4201735 的修补程序
* 在资产文件的名称中使用与号（“&amp;”）字符，会导致在访问文件属性时出现问题。NPR-15770：适用于 CQ-4201737 的修补程序
* 在导航资产和使用“列视图”显示模式时，如果用户在选择并单击资产后刷新页面，则会显示资产详细信息，而不是刷新的内容。NPR-15768：适用于 CQ-4201727 的修补程序
* PDS 摄取占用 100% 的 CPU 利用率，其中许多库用于 PDF 服务。NPR-15606：适用于 GRANITE-12929 的修补程序
* 使用 Firefox 浏览器访问“我的链接共享”UI 时，不会显示共享项目或用户，并且屏幕不可用。NPR-15539：适用于 CQ-4200992 的修补程序
* 使用 Digital Asset Manager 时，如果某个页面与一组图像相关联，则将这些图像移动到新文件夹会断开页面关联，并且关联的页面会缺少一些图像。NPR-15538：适用于 CQ-111479 的修补程序
* 在 DAM 查看器组件中，使用“nosamplecontent”运行模式会导致 Dynamic Media 出错。NPR-15449：适用于 CQ-4195425 的修补程序
* 创建视频配置文件时，如果同时选择了高质量和中等质量的视频编码预设，则不会保存所做的更改。NPR-15447：适用于 CQ-4195482 的修补程序
* 即使由于服务器错误响应导致资产上传到 Brand Portal 失败，Brand Portal UI 中的状态仍会更新为“已发布”，这样便难以跟踪缺失的文件。NPR-15442：适用于 CQ-4197968 的修补程序
* 将资产文件夹发布到 Brand Portal 时，如果发布时间超过一小时，则某些文件将无法发布。NPR-15441：适用于 CQ-4199493 的修补程序
* 在列视图中使用资产查找器控制台时，尝试创建文件夹会失败一次，但再试一次会成功。NPR-15370：适用于 CQ-4199448 的修补程序
* 如果在 DAM UI 中选定的资产或文件夹名称中带有逗号，则“引用”选项卡将不可用，并且会显示消息“引用列表不适用于多个选项”。NPR-15362：适用于 CQ-4199721 的修补程序
* 将文件夹发布到 Brand Portal 不会更改文件夹的已发布状态，即使文件夹下的资产已成功发布也是如此。NPR-15292：适用于 CQ-4197667 的修补程序
* 在触屏 UI 中导航到资产控制台后，激活某些资产时会显示异常。NPR-15217：适用于 CQ-108779 的修补程序
* 通过代理服务器进行连接时，将视频发布到 Youtube。NPR-15109：适用于 CQ-110332 的修补程序
* 在 data-sly-resource 中使用名称包含圆点或句点 (.) 的资产，不会解析到同一资产，输出路径将在圆点处终止。NPR-15069：适用于 CQ-4195914 的修补程序
* 将 AEM 6.2 升级到 Service Pack 1 后，将资产同步到 Scene7 失败。dam:Scene7FileStatus 属性显示“`UploadFailed`”状态，即使对于已发布的资产也是如此。NPR-15269：适用于 CQ-4197708 的修补程序

### 用户界面 {#user-interface-5}

* 在&#x200B;**[!UICONTROL 触屏 UI]** 中，使用 Internet Chrome 浏览器版本 56.0.2924.87 时，对于没有 type=&#39;datetime&#39; 的日期字段，不会显示保存的日期。NPR-15383：适用于 GRANITE-16481 的修补程序
* 在&#x200B;**[!UICONTROL 触屏 UI]** 中，富文本编辑器在呈现线程和标题元素时，会从 HTML 表中删除它们。NPR-15267：适用于 CRTE-41 的修补程序
* `FileUpload Validator` 不处理将 autostart 设置为 true 或手动调用 `uploadFile()` 时的情况，并且在这些情况下会生成无效的验证报告。NPR-15295：适用于 GRANITE-13499 的修补程序

* Omnisearch 不允许使用 /apps 的客户添加列数据源，因为它假定位置配置列在 */libs/granite/omnisearch/content/metadata/* 下。NPR-13188：适用于 GRANITE-16479 的修补程序
* 使用&#x200B;**[!UICONTROL 触屏 UI]** 时，产品变量的创建级别与产品不同。系统不会通知用户变量创建过程的状态。NPR-15345：适用于 CQ-4198948 的修补程序

**Scene7**

* 运行 Scene7 工作流导致打开的文件不会关闭。请求改进 AEM-S7 服务，以便通过共享池配置来维护和重用单个 HttpClient 实例。NPR-15357：适用于 CQ-109958 的修补程序

### 翻译 {#translation-9}

* 使用翻译项目时，从英语母版更新语言副本，将会生成 11 个单独的启动项，所有这些启动项的名称和源根均相同，但如果页面名称遵循某种设置模式，则启动项根稍有不同。NPR-15605：适用于 CQ-4200699 的修补程序
* 当语言根的名称中包含连字符和短划线时，无法为页面创建翻译项目。NPR-15171：适用于 CQ-96286 的修补程序
* 请求更新 Microsoft Connector，以便能够使用 Microsoft Translator API，Microsoft 在 Azure 门户中提供了该 API。NPR-15320：适用于 CQ-101010 的修补程序

### 项目 {#projects-4}

* 虽然存储库中有超过 20 个不活动项目，但项目屏幕中只显示 20 个不活动项目。NPR-15656：适用于 CQ-4200903 的修补程序

### 营销活动 {#campaign-1}

* 在使用“营销活动 - 定位”和“MAC - 测试”以及 Target 集成组件时，取消发布活动不会更新母版 UI 中的活动状态。NPR-15401：适用于 CQ-4199839 的修补程序
* 在 AEM Commerce 中移动产品时，“产品移动”向导缺少产品名称、标题、引用的页面、创建作者以及创建日期的预填充值。NPR-15228：适用于 CQ-98617 的修补程序

### 安全 {#security-4}

* 已使用 GET 方法将 CSRF 令牌参数添加到表单。NPR-15229

### 表单 {#forms-18}

#### Forms 附加组件包 {#forms-add-on-package-18}

`**Adaptive Forms**`

* 使用输入 XML 预填充自适应表单时，默认值会被 xml 中的空值覆盖。NPR-15721
* 在基于 XML 架构的自适应表单中，提交的 XML 中存在 `afData/afBoundData` 包装器，即使预填充 XML 不包含 `afData/afBoundData` 包装器也是如此。NPR-15541

* 可折叠项栏中的标题应为可编辑的 HTML“h2”标题，而不是“a”标记。NPR-15475
* 屏幕阅读器用户无法访问表单面板的可折叠项布局。使用屏幕阅读器软件（例如 JAWS 或 NVDA）时，用户无法仅通过键盘导航到可折叠项选项卡。NPR-15474

`**Correspondence Management**`

* 保存、删除和设置文档片段的引用需要较长时间。NPR-15939
* 在“管理资产”中设置的关于包含多个标题的文本制表符对齐方式，在 CCR UI 中损坏。NPR-15818
* 尽管文本包含在 Google Chrome 中使用制表符创建的对齐内容，但是文本模块的缩略图不显示对齐的内容。NPR-15819

`**Forms Portal**`

* 预填充服务不适用于 XDP 表单。NPR-15466
* 在存储自适应表单草稿并将其提交到数据库时，如果因任何原因（例如，长时间不活动后）导致数据库连接失败，则自适应表单的状态将会损坏。NPR-15297

#### Forms JEE 安装程序  {#forms-jee-installer-18}

`**Core**`

* 升级到最新版 Java 1.8.0_121-b13 后，在 AEM Forms 中无法访问管理员用户界面。NPR-15330

`**XTG**`

* 使用输出服务将特定表单与数据 XML 合并时的响应时间，是使用 ES4 SP1 服务器执行相同操作所花费的时间的 20 倍。NPR-15283

#### AEM Forms 应用程序 {#aem-forms-app-1}

* 恢复未保存的任务时，显示的关于恢复未保存任务的消息应该更加清晰明了，以减少用户错误。NPR-15377
* AEM Forms 应用程序不呈现通过自定义模板创建的表单。NPR-15892
* 用户无法登录 AEM Forms 应用程序。NPR-15891

AEM 6.2 SP2-CFP1 的主要功能亮点包括：

* 简化了站点中的复制功能：

   * 修复了各种转出、LiveCopy 和错误写入问题

* 增强了触屏 UI 在下列情况中的响应：

   * 资产搜索
   * 基于大小的排序

* 增强了智能收藏集中的 Tag management
* 加强了对文件夹执行 CRUD 操作期间的访问控制

### 平台 {#previous}

* 请求在复制代理启动期间删除 `ReplicationQueue#forceRetry` API 调用，因为此类调用会显著降低实例的运行速度，尤其是当它有许多复制代理时。NPR-14032：适用于 GRANITE-13095 的修补程序
* 请求 `DurboImportConfigurationProviderService` OSGi 配置，用于支持可以存储一组值的字段。NPR-14570：适用于 CQ-108684 的修补程序
* 迁移到 AEM 6.2 后，在页面中使用 Sightly 组件会导致页面的“属性”对话框停止工作。NPR-14328：适用于 CQ-108355 的修补程序
* 取消计划以前计划的作业不会删除 */var/eventing/scheduled-jobs* 下的相应节点。NPR-14253：适用于 SLING-5666 的修补程序
* 当管理员尝试以已删除用户的身份模拟时，用户界面无法刷新。NPR-14247：适用于 CQ-107446 的修补程序
* XSS 防护检查导致 Sightly 组件中的编码不正确。NPR-14004：适用于 CQ-93821 的修补程序
* 请求将 Jackrabbit Filevault 升级到 3.1.30 以解决多个问题。NPR-13454
* Sling Distribution 将分发包从创作环境同步到发布环境时出现缓存错误。NPR-13034：适用于 GRANITE-13970 的修补程序

### 站点 {#sites-18}

* VersionManagerImpl 从版本历史记录中清除不正确的版本时出现问题。NPR-14372
* WCM Sightly Foundation Parsys 组件忽略组件声明标记名称 `cq:htmlTag / cq:tagName`。NPR-14225
* 在触屏 UI 中，当使用 Sightly Parsys 呈现通过 JavaScript 插入的组件时，自定义修饰在页面刷新后会被忽略。NPR-14122
* 如果创建了多个富文本字段（例如链接），“目标”下拉列表在触屏 UI 对话框中无法使用。NPR-13911
* 在触屏 UI 对话框中编辑具有多个富文本编辑器 (RTE) 属性的文本字段时，焦点会随机转移到特定 RTE 属性。NPR-13703
* 默认的现成可用视频组件不呈现视频缩略图。NPR-14976
* 在模板编辑器的“实时使用情况”选项卡中，信息加载缓慢。NPR-14880：适用于 CQ-83417 的修补程序
* 在 AEM 6.2 实例上安装修补程序 10936，会禁用 iparsys 组件。NPR-14330：适用于 CQ-106982 的修补程序
* 迁移到 AEM 6.1 SP1 后，出现多个转出组件问题和 Live Copy 问题。NPR-15256
* 即使对于多个转出配置，页面转出操作也无法创建超出第一级的子项。NPR-15055
* 从编辑器提交 PageProperties 对话框时，将会重写 LiveCopy 选项卡中未更改的数据。NPR-14693
* 从编辑器提交 PageProperties 对话框时，MSM Post 处理器会从请求（而不是 `msm:writeLiveCopyConfig` 参数）写入一些参数。NPR-14434
* 与转出组件、Live Copy 以及 MSM 的其他方面相关的多个问题。NPR-12235

### 资产 {#assets-18}

* “解包”工作流无法处理图像文件名中包含特殊字符的图像。NPR-15227：适用于 CQ-103887 的修补程序
* 无法正常显示具有 Repeat with Condition 表达式的资产。当用户预览 `*CDN3835RLCEN*` 信件模板时，未显示位于“正文”目标区域中的资产。如果取消选择预先选定的资产 `*VIPReassement*`（可选资产），则信件中会显示预先选定的其他资产。NPR-14844

* 创建智能收藏集时，在保存智能收藏集后不保留样式标记。NPR-15081：适用于 CQ-4195494 的修补程序
* 在多个用户进行并发搜索期间，资产搜索查询在触屏 UI 中运行缓慢。NPR-15019：适用于 CQ-4195405 的修补程序
* 将原始资产重新上传到其他位置后，为 `Long[]` 类型的属性提取的元数据将转换为 `String[]` 类型。NPR-15016：适用于 CQ-4195005 的修补程序

* 用户无法删除保存的搜索或智能收藏集。NPR-14924：适用于 CQ-108494 的修补程序
* 在基础元数据架构的下拉字段中为 TypeHint 使用布尔值时，批量编辑资产元数据（附加模式）会生成错误。NPR-14529：适用于 CQ-106876 的修补程序
* 没有复制权限的用户无法删除资产文件夹。NPR-14321：适用于 CQ-88271 的修补程序
* 尝试在渠道编辑器中编辑视频的视频配置文件时，设计对话框未打开，并且在错误日志中引发空指针异常。NPR-14144：适用于 CQ-81101 的修补程序
* 资产的属性页面中显示的由系统生成的“创建日期”时间戳属性不正确。NPR-13992：适用于 CQ-95029 的修补程序
* 请求为在 AEM Assets 中没有“读取”权限的用户启用重复资产检测。NPR-13851：适用于 CQ-102281 的修补程序
* 用户无法从属性页面批量编辑资产的元数据。NPR-13721：适用于 CQ-100703 的修补程序
* 上传重复资产时，经典 UI 中的错误消息不正确。错误消息未说明上传失败的原因。NPR-13691：适用于 CQ-99272 的修补程序
* 当文件夹包含大量资产时，AEM Assets 在列表视图中无法按资产大小一次对超过 50 个资产进行排序。CQ-100588
* 如果资产/文件夹 URI 过长，则选择多个资产会引发响应代码为 414（请求 URI 过长）的错误。NPR-13516：适用于 CQ-76076 的修补程序
* 用户在“配置列”对话框中选择所有选项时，“资产报告”页面会变得无响应。NPR-13187：适用于 CQ-95589 的修补程序
* Safari 和 Internet Explorer 中的标记选取器出现意外行为。NPR-13134
* 编辑从资产管理员搜索边栏中保存的搜索，会将其保存为嵌套式智能选项，这将导致出现环境稳定性问题。NPR-13119：适用于 CQ-99460 的修补程序
* 移动文件（或文件夹）并对其重命名后，“cq:name”元数据不反映新的文件名（文件夹名称）。NPR-13036：适用于 CQ-99141 的修补程序
* 无法从通过电子邮件共享的下载链接下载名称中包含特殊字符的资产。NPR-12872：适用于 CQ-95795 的修补程序
* 当资产数量很大时，生成的现成可用的资产报告会导致大量遍历，其中搜索未找到任何索引，并且 CPU 使用率达到峰值。NPR-12811：适用于 CQ-84409 的修补程序
* 从不同网络访问 AMS AEM Assets 创作实例的用户在没有文件夹删除权限的情况下无法使用块上传来上传资产。NPR-12768：适用于 CQ-82715 的修补程序
* 在使用资产搜索边栏进行基于标记的资产搜索时，“提前键入”功能不会将其自身限制为根路径，而是显示所有命名空间的标记。NPR-12666
* 静态呈现版本组件引发空指针异常。NPR-12665
* 请求禁用 MissingMetadataNotificationJob，因为它会导致徽章通知 UI 损坏页面，且出现“无法扫描输入”的运行时异常。NPR-12500：适用于 CQ-93573 的修补程序
* 标记字段的“禁用编辑”选项在触屏 UI 的资产属性页面中不起作用。NPR-12429：适用于 CQ-88835 的修补程序
* 修复 AEM Assets 6.2 中的 API 问题，以便实施配套应用程序 SMB。NPR-11099
* 自更新 Jquery 以来，用户无法选择资产收藏集并在内容片段的“关联内容”面板中确认选择。NPR-14847：适用于 CQ-4194209 的补丁包
* 尽管在客户端调用无限排序，但只对 UI 中当前显示的文章/横幅/收藏集进行排序。NPR-14493：适用于 CQ-109926 的修补程序
* 请求为 AEM Mobile On-Demand 服务实施 Omnisearch 功能。对任何文章、收藏集或横幅的关键字搜索不返回任何匹配项。NPR-14093：适用于 CQ-101394 的修补程序
* 在对话框中使用 Coral-select 组件 (*granite/ui/components/coral/foundation/form/select*) 时，如果选定的值包含单个项目，则无法在 Internet Explorer（IE 11 或 Edge 浏览器）中正确初始化值。NPR-13395：适用于 CQ-101013 的修补程序

### 项目 {#projects-5}

* 导出使用翻译方法“human”和翻译提供程序“none”创建的翻译项目时，没有生成 translation_export_summary.xml 文件，因为缺少 GUID 映射文件。NPR-13137：适用于 CQ-91976 的修补程序
* 在 AEM 项目中，如果创建的项目设置了到期日期属性，则日期转换设置的时间不正确，因为服务器与客户端之间存在时区差异。NPR-13003：适用于 CQ-98288 的修补程序
* 更新翻译项目后，翻译作业中缺少“在站点中展现”选项。NPR-12966：适用于 CQ-93740 的修补程序
* 为导出的站点页面创建翻译项目后，该项目在预览中无法正确呈现。NPR-12964：适用于 CQ-84627 的修补程序

### 工作流 {#workflow-3}

* 单击“工作流”控制台的“存档”选项卡中的有效负荷链接时，会返回响应代码为“404”的错误。NPR-14993：适用于 CQ-4194977 的修补程序
* 使用 AEM 默认工作流时，CQ 邮件程序无法向缺少单个成员电子邮件地址的组发送电子邮件通知。NPR-14804：适用于 CQ-91499 的修补程序请求
* 改进了触屏 UI 中收件箱和通知徽章的性能。NPR-14145：适用于 CQ-101125 的修补程序
* 启动工作流时，用户无法从工作流“收件箱”控制台预览有效负荷。NPR-13226：适用于 CQ-100275 的修补程序
* 使用 SAML 身份验证处理程序配置的“saml_request_path”Cookie 显示 Cookie 设置了一个额外的“?”字符。此外，当 SAML 响应回发到 AEM 时，AEM“saml_request_path”Cookie 会因字符已编码而返回无效值。NPR-13517：适用于 GRANITE-11722 和 GRANITE-14414 的主动修补程序

### 解决方案集成 {#solution-integration}

* 将 AEM 6.2 与 Search&amp;Promote 集成后，如果用户搜索某个词时返回一个横幅，则搜索功能将变得无响应。NPR-14549：适用于 CQ-109631 的 CFP

### Dynamic Media {#dynamic-media}

* 在 AEM 激活过程中创建和取消的大量 AEM-Scene7 sling 作业在复制期间记录为存档作业。NPR-12835：适用于 CQ-86115 的修补程序

### 安全 {#security-5}

* 请求解决 WCMDebug 筛选器中的输入验证问题。NPR-12444：适用于 CQ-94890 的修补程序请求
* 使用“创建启动项”向导时，主动请求更正 XSS 行为。\
   NPR-13062：适用于 CQ-99577 的修补程序请求

#### Forms 附加组件包 {#forms-add-on-package-19}

`Adaptive Forms`

* 使用自适应表单创建可重复面板时，无法在运行时更新面板标题。NPR-15325
* 如果在保存或提交时设置单选按钮的默认值，并且选择了除默认值以外的某个值，则该值不会显示在预填充中。NPR-15304
* 使用选项事件动态填充下拉列表并提交选定项目的值时，Google Chrome 显示错误行为。NPR-15198
* 使用自适应表单创建可重复面板时，无法在运行时更新面板标题。NPR-15181
* 使用自适应表单的编辑模式时，遇到 JavaScript 错误，例如“组件的处理程序无效”和“未定义 guidelib”。NPR-15112
* 重复面板中的延迟加载片段无法按预期使用。NPR-13916、NPR-14785

`Correspondence Management`

* 无法正确显示包含 `'Repeat with condition'` 表达式集的通信管理资产。NPR-14844
* 搜索通信管理资产（例如信件、文档片段或任何其他类型）时，工具栏中缺少“下载队列”图标。NPR-14745
* 创建列表模块时，无法切换特定于资产的属性（例如可编辑和必需属性）。NPR-14689
* 如果创建条件模块而未选择数据词典，则表达式生成器实用程序中的“数据元素”面板会持续加载。NPR-14688
* 在预览信件时，用户无法使用制表符空格以表格式对齐内容。NPR-14481
* 从用户界面批量导出通信管理资产时，AEM Forms 服务器生成不必要的日志。NPR-15226
* 预览信件时，两端对齐的文本以不同字体显示。NPR-15468

`**Forms Portal**`

* 从 Forms Portal 提交新的草稿后，Forms Portal 中已提交表单的附件将不可见。NPR-13515

`**Forms Manager**`

* 在 *FormsandDocuments* 目录中导航时，如果用户复制任何资产并导航到其他文件夹，则不会显示“粘贴”按钮。CQ-111327

#### Forms JEE 安装程序 {#forms-jee-installer-19}

`Rights Management`

* 与用户登录相关的审核事件记录的时间无效。无法跟踪审核事件的正确时间。NPR-13107
* Adobe Acrobat Reader 和 Microsoft Office 无法打开受扩展身份验证保护的文档。NPR-14482

`Process Management`

* 将 HTML 工作区中转发的草稿任务返回给初始用户时，该任务不会显示在初始用户的队列中。NPR-15178

`Assembler Service`

* AEM Forms 无法验证具有两个以上签名的 PDF/A-2b。NPR-14101

`XTG`

* 使用打印机旁路纸盒打印文档时，`GeneratePrintedOutput` 函数不允许从右侧旁路纸盒取纸。NPR-14079

#### Forms设计师{#forms-designer-2}

* 当用户使用“法语（加拿大）”作为选定的表单区域设置来运行拼写检查实用程序时，Forms Designer 崩溃。NPR-13740
* 当用户选择表单字段的计算事件或验证事件，然后将语言更改为 JavaScript 并在&#x200B;**[!UICONTROL 脚本编辑器]**&#x200B;窗口中输入 `this.` 时，Forms Designer 崩溃。NPR-12974

### CFP1 中包含的功能包 {#feature-packs-included-in-cfp-3}

`Mobile Forms`（Forms 附加组件包）：

* 从 XDP 文件创建自适应表单时，辅助功能的 Tab 键顺序不遵循设置的模式。NPR-12562

`Adaptive forms`（Forms 附加组件包）：

* 自适应表单的规则生成器不提供基于角色的访问权限。无法跟踪作者所做的更改。NPR-12840

`Core`（Forms JEE 安装程序）：

* 没有为 Jboss+ 启用核心跨域资源共享 (CORS) 功能作为 Servlet 筛选器。NPR-13050

## 通过 Software Distribution 下载 CFP 说明 {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>对于 AEM Forms 客户，请在安装任意 AEM Service Pack、累积修补程序包或功能包之后，再安装 AEM Forms 附加组件包，这一点至关重要。

您可以直接从 Software Distribution 下载 CFP 包，或者执行以下步骤：

1. 打开 [Software Distribution](https://experience.adobe.com/downloads)。您需要 Adobe ID 才能登录 Software Distribution。
1. 点按标题菜单中的 **[!UICONTROL Adobe Experience Manager]**。
1. 点按包名称，选择&#x200B;**[!UICONTROL 接受 EULA 条款]**，然后点按&#x200B;**[!UICONTROL 下载]**。

## CFP 安装说明 {#installation-instructions-for-cfp}

此部分将向您介绍安装 CFP 的要求和步骤。

### 安装之前 {#before-you-install}

>[!NOTE]
>
>Adobe 提供的可选功能包依赖于发行版本和累积修补程序包。如果您已安装功能包，请联系 [AEM 客户关怀团队](https://helpx.adobe.com/cn/marketing-cloud/contact-support.html)以验证与 AEM 6.2 的累积修补程序包的兼容性。

>[!NOTE]
>
>我们建议您先对每个新的安装包运行验证，然后再尝试安装包。预验证会分析并报告安装之前发现的任何错误，并主动向用户发出有关此类错误、叠加和权限的警告。
>
>您可以访问相关文档以了解“验证”选项，网址为：[https://docs.adobe.com/content/docs/cn/aem/6-2/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/cn/aem/6-2/administer/content/package-manager.html#Package%20Validator)

* AEM 6.2 Service Pack 1 是安装 CFP 的先决条件。有关安装说明，请参阅 [AEM 6.2 Service Pack 1 发行说明](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。

* 可在 [Software Distribution](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/cumulativefixpack/AEM-6.2-SP1-CFP20) 中下载累积修补程序包，您可以直接从 AEM 实例访问 Software Distribution。
* 对于使用 RDBMK 或 MongoDB 的群集部署，可以在使用包管理器的任何创作实例上安装 CFP 包。

* 在安装累积修补程序包之前，请确保拍摄快照或备份您的 AEM 实例。
* 不支持卸载 CFP。

### 通过 Software Distribution 安装 CFP {#install-the-cfp-via-package-share}

执行以下步骤，在现有 AEM 6.2 SP1 实例上安装累积修补程序包：

1. 单击 [Software Distribution](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) 链接以下载包。

1. 打开[包管理器](http://localhost:4502/crx/packmgr/index.jsp)，并单击&#x200B;**[!UICONTROL 上传包]**&#x200B;以上传包。

1. 选择包名称，然后单击&#x200B;**[!UICONTROL 安装]**。

### 自动安装 {#automatic-installation}

可以通过以下方式将 CFP 自动安装到正在运行的实例中：

* 在服务器运行时，将包放入 ../crx-quickstart/install 中。包会自动进行安装。
* 使用[包管理器中的 HTTP API](https://helpx.adobe.com/cn/experience-manager/6-2/sites/administering/using/package-manager.html) – 确保使用 `cmd=install&recursive=true` – 这会安装嵌套包。

### 验证安装 {#validate-installation}

1. “产品信息”页面 (/system/console/productinfo) 此时应在“已安装的产品”下显示更新的版本字符串“Adobe Experience Manager，版本 6.2.0.SP1-CFP20”。
1. 所有 OSGi 包在 OSGi 控制台中均为“活动”或“片段”（使用 Web 控制台：/system/console/bundles）。

>[!NOTE]
>
>成功安装包后，会显示一条信息性消息，指示已成功安装内容包，例如“已成功安装内容包 AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20”。

>[!NOTE]
>
>自 AEM 6.2 SP1-CFP1 起，对于大多数消息，Jackrabbit FileVault 中的日志级别已从“信息”更改为“调试”。要获取在 AEM 6.2 SP1-CFP1 或更高版本上安装的内容包的安装日志，请为 `org.apache.jackrabbit.vault.packaging.impl` 启用“调试”日志级别。

### 安装 AEM Forms {#install-forms}

>[!NOTE]
>
>如果您不使用 AEM Forms，请跳过此部分。

#### 安装 AEM Forms 附加组件  {#install-aem-forms-add-on}

>[!NOTE]
>
>（**仅限 JEE 上的 AEM Forms**）[在 AEM Forms JEE 上安装 CFP](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee) 中介绍了在 JEE 上的 AEM Forms 中安装 CFP 的操作步骤。

1. 确保您已安装 AEM 6.2 SP1 CFP 包。
1. 下载适用于您的操作系统的 [AEM Forms 发行版](aem-forms-releases.md)中列出的相应 Forms 附加组件包。
1. 按照[安装 AEM Forms 附加组件包](https://helpx.adobe.com/cn/experience-manager/6-2/forms/using/installing-configuring-aem-forms-osgi.html)中的所述安装 Forms 附加组件包。

#### 安装 AEM Forms JEE 包 {#install-aem-forms-jee-bundles-package}

AEM Forms JEE 中的修复通过单独的安装程序来交付。有关在 AEM Forms JEE 上安装 CFP 的信息，请参阅[在 AEM Forms JEE 上安装 CFP](install-cfp-aem-forms-jee.md)。

#### Forms Designer 安装程序  {#designer-installer}

1. 要安装更新，请运行 Designer6.2.0_&lt;语言>_Cumulative_QF.msp 文件。
1. 在“欢迎”屏幕上，单击&#x200B;**更新**。安装随即开始。
1. 安装完成后，单击&#x200B;**完成**。

## DTM、Analytics、Target、Search &amp; Promote 连接的用户可配置超时参数 {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

使用 AEM 累积修补程序包 6.2 SP1-CFP7 及更高版本时，可根据以下详细信息对上述所有连接配置连接超时时间段：

| **连接** | **连接超时*** | **套接字超时**** |
|---|---|---|
| DTM | 30000 毫秒 | 30000 毫秒 |
| Analytics | 30000 毫秒 | 30000 毫秒 |
| Target | 60000 毫秒 | 30000 毫秒 |
| Search&amp;Promote | 30000 毫秒 | 30000 毫秒 |

* **连接超时*** - 在建立连接之前的超时时间（以毫秒为单位）。超时值为零被解释为无限超时。
* **套接字超时**** - 等待数据的超时时间，或两个连续数据包之间的最长不活动时间段（以毫秒为单位）。

>[!NOTE]
>
>使用 AEM 累积修补程序包 6.2 SP1-CFP6 及更高版本时，用于 Search &amp; Promote 集成的 OSGi 配置是 Apache HTTP 组件代理配置。不再使用 Day Commons HTTP Client 3.1 中的代理配置。

## 在标记控制台中禁用复制状态（经典 UI）(NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

如果您使用的是 CFP3 或更高版本，请按照以下说明在经典 UI 的标记控制台中禁用复制状态：

* 在 */apps* 中叠加“*/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js*”

* 在第 416 行之后添加 `replicationStateRequired`: &quot;false&quot;。

   ```js
   415    baseParams: {
   416                    count: "false",
   417                    "replicationStateRequired": "false"
   418                },
   ```

## 最新的 Java 8 Update 131 引发异常 (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>这些配置设置专门针对使用文档安全的 AEM Forms 客户。

CFP12.1 中包含 NPR-21355。如果您安装的是 CFP12.1 或更高版本，请执行以下操作步骤，在 JBoss 应用程序服务器上配置 NPR-21355。如果是在 Oracle WebLogic 或 IBM WebSphere 应用程序服务器上运行的 AEM Forms 服务器上安装 CFP12.1，则无需其他配置：

1. 备份、删除和新建 module.xml 文件。该文件的默认位置为：[AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. 打开新创建的 module.xml 文件进行编辑。将以下代码添加到该文件：

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

1. 创建位于 [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/ 的 jsafeFIPS.jar 文件、jsafeJCEFIPS.jar 文件和 certjFIPS.jar 文件的备份，并从上述目录中删除这些文件。

   联系 [Adobe 支持团队](https://helpx.adobe.com/marketing-cloud/contact-support.html)以获取新的 JAR 文件。将 [Adobe 支持团队](https://helpx.adobe.com/marketing-cloud/contact-support.html)提供的 JAR 文件放在 [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. （仅限 Windows）修改 `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` 或 `domain.conf.bat` 配置文件：

   * 对于独立配置中的 JBoss 服务器，请打开 standalone.conf.bat 进行编辑。
   * 对于群集配置中的 JBoss 服务器，请打开 domain.conf.bat 进行编辑。

   在末尾添加以下行并保存文件：

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   set &quot;JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

1. （仅限基于 Linux 的操作系统）修改 [AEM_Forms_Installation_directory]/jboss/standalone.conf 或 domain.conf 配置文件：

   * 对于独立配置中的 JBoss 服务器，请打开 standalone.conf 进行编辑。
   * 对于群集配置中的 JBoss 服务器，请打开 domain.conf 进行编辑。

   在末尾添加以下行并保存文件：

   JAVA_OPTS=&quot;$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true&quot;

   JAVA_OPTS=&quot;$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE&quot;

## NPR-19778 所需的配置设置 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>NPR-19778 是 CFP14 的一部分。

默认情况下，当某个用户声明任务时，不会为其他用户刷新共享队列的计数。为此，我们引入了一个新属性。请按照以下步骤在 AEM 实例上配置此属性：

1. 转到“管理员 UI”>“服务”>“工作区”>“全局管理”。
1. 导出全局设置。
1. 在下载的 XML 文件中，添加标记 `<client_tasksPollingInterval>10</client_tasksPollingInterval>`。其中，10 是示例值（以秒为单位）。您可以相应地对其进行修改。
1. 保存文件。
1. 返回到“管理员 UI”>“服务”>“工作区”>“全局管理”。
1. 在“导入全局设置”部分导入 xml 文件。
1. 现在，您可以退出系统并重新登录。
1. 对于工作区中的其他用户，共享队列的计数开始刷新。
1. 要关闭轮询，请将值更改为 0，然后再次导入 XML 文件。

## UI 更改 {#ui-changes}

* 对于将 dc: title 属性设置为 String []（多字段）的图像，在图像卡片上显示标题时发生行为更改：尽管所有标题都将保存在 CRX 中，但 UI 中的图像卡片上只显示最新更改的标题。适用于 CQ-4217165 的修补程序

## 已知问题 {#known-issues}

* 从 CFP18 更新 AEM 6.2 SP1-CFP19 和 AEM 6.2 SP1-CFP20 会将根重定向更改为经典 UI 欢迎页面，而不是 /sites.html/content。您可能必须使用 CRX Explorer 将 sling: target 属性从 /welcome.html 更改为 /index.html。从 CFP17 或更低版本进行更新时，未发现此问题。

安装 AEM 6.2 SP1-CFPx 时，可能会发生以下短暂的错误。但是，无需解决这些错误，因为它们不会影响 AEM 实例，并且在 CFP 安装完毕后便会消失：

* 将 AEM 6.2 SP1-CFP20 实例升级到 AEM 6.5 时，某些虚 URL 可能无法正常运行，例如：

   * */projects.html*
   * */sites.html*

不过，解决方法是：升级后重新启动 AEM 实例。

* 打开 Web 控制台组件详细信息页面时，收到 HTTP 500 内部服务器错误。
* 由于重新启动存储库，发生&#x200B;**创建组件实例**&#x200B;和&#x200B;**服务工厂返回 null** 错误：

   * com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] 由于绑定引用 profileManager 失败，无法创建组件实例。
   * org.apache.sling.commons.scheduler FrameworkEvent 错误（org.osgi.framework.ServiceException：服务工厂返回 null。（组件：com.day.cq.tagging.impl.TagGarbageCollector (1687)））

* 在 Mongo 和 DB2 中的 CFP 安装中发现错误：**org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exception: java.lang.NullPointerException**。在 CFP8 上安装 CFP 后，不会出现此错误。
* （Adobe Granite 维护计划程序更新任务）com.adobe.granite.maintenance.impl.TaskScheduler：找不到名称为 WorkflowPurgeTask for window granite:weekly 的维护任务
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
* 在包含智能标记功能包的 AEM 6.2 SP1 上安装 CFPx 时，将从 DAM 更新资产工作流中删除之前添加的智能标记资产工作流步骤。

请参阅 [AEM 6.2 SP1 中的已知问题]列表 (https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html#Known Issues)。

## Uber Jar {#uber-jar}

适用于 6.2 SP1-CFP20 的 Uber Jar 可在 [Adobe 公共 Maven 存储库](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.2.SP1-CFP19/)中获取。

要在 Maven 项目中使用 Uber Jar，请在项目 POM 中包含以下依赖项：

```XML
<dependency>
    <groupId>com.adobe.aem</groupId>
    <artifactId>uber-jar</artifactId>
    <version>6.2.SP1-CFP20</version>
    <classifier>apis</classifier>
    <scope>provided</scope>
</dependency>
```

## 包含的 OSGi 包和内容包 {#osgi-bundles-and-content-packages-included-5}

以下文本文档列出了 CFP 中包含的 OSGi 包和内容包。

* [AEM 6.2 SP1-CFP20 中包含的 OSGi 包列表](assets/do-not-localize/updated.txt)
* [AEM 6.2 SP1-CFP20 中包含的内容包列表](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [AEM 6.2 修补程序页面](https://helpx.adobe.com/cn/experience-manager/kb/aem62-available-hotfixes.html)
>* [AEM 6.2 SP1 发行说明](https://docs.adobe.com/content/docs/cn/aem/6-2/release-notes/sp1.html)
>* [AEM 6.2 发行说明](https://docs.adobe.com/docs/cn/aem/6-2/release-notes.html)
>* [AEM 产品页面](http://www.adobe.com/cn/solutions/web-experience-management.html)
>* [AEM 6.2 文档](https://docs.adobe.com/content/docs/cn/aem/6-2.html)
>* [订阅](https://campaign.adobe.com/webApp/adbePriorityProductSubscribe) [Adobe 产品更新早知道](https://docs.adobe.com/content/help/zh-Hans/release-notes/experience-cloud/current.html)

