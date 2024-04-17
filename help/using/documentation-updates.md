---
title: Experience Manager近期文档更新
description: 在Experience Manager文档中了解新增内容、更新内容或修改内容。
contentOwner: trushton
exl-id: 8c136a03-f961-4854-af38-45457b85d289
source-git-commit: 437dad5fffe71592b6f9f9b4099a253e3a55b0c8
workflow-type: tm+mt
source-wordcount: '1945'
ht-degree: 94%

---

# [!DNL Experience Manager] 文档：最近文档更新 {#aem-documentation-recent-documentation-updates}

本页列出了自新年伊始对 Adobe Experience Manager 文档做出的重要更改和更新。

您还可以查看[先前的文档更新](previous-documentation-updates.md)。

## [!DNL Experience Manager] as a [!DNL Cloud Service] {#aem-as-a-cloud-service}

本页列出了有关 [!DNL Adobe Experience Manager] 的重要文档更改和更新。

您还可以查看[先前的文档更新](previous-documentation-updates.md)。

## [!DNL Adobe Experience Manager] as a [!DNL Cloud Service] {#aem-cloud-service}

>[!NOTE]
>
>Experience Manager as a Cloud Service 每月发布一次。
>
>有关各个发行版本（当前版本和早期版本）的文档，请参阅[发行说明](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/release-notes/release-notes/release-notes-current)。

| 日期 | 主题 | 更改 |
| --- | --- | --- |
| 2021 年 11 月 25 日 | 带 Dynamic Media 的 AEM - 配置 | 您现在可以直接从 AEM 上的 Dynamic Media 中配置常规设置和发布设置，而不必使用 Dynamic Media 桌面应用程序。<br>请参阅[配置 Dynamic Media 常规设置](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/dm-general-settings)和[为图像服务器配置 Dynamic Media 发布设置](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/dm-publish-settings)。<br>另请参阅[配置 Dynamic Media - Scene7 模式](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dms7) |
| 2021 年 11 月 4 日 | 带 Dynamic Media 的 AEM - 智能裁切 | 使用最新的 Adobe Sensei 服务改进了图像资源的智能裁切和智能色板功能。文档更新包括以下内容：<br>• 在图像配置文件的“裁切选项”对话框中新增了&#x200B;**[!UICONTROL 跨目标分辨率保留裁切内容]**&#x200B;选项。<br>• 在手动重新对齐多个资源的智能裁切窗口或调整其大小时，即使您稍后决定重新处理这些资源，也会维护并保留所做的这些编辑。不过，如果您在图像配置文件的&#x200B;**[!UICONTROL 响应式图像裁切]**&#x200B;区域中编辑宽度和/或高度，则这些资源需要重新处理。<br>• 新的智能裁切和色板支持的图像文件格式表。<br>有关这些更新，请参阅[图像配置文件](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/image-profiles)。 |
| 2021 年 11 月 3 日 | 智能裁切视频查看器 API | Dynamic Media 查看器参考指南中现在提供了新的[智能裁切视频查看器 API 文档](https://experienceleague.adobe.com/en/docs/dynamic-media-developer-resources/library/viewers-for-aem-assets-only/smartcropvideo/c-html5-aem-smartcropvideo-viewer-reference)。 |
| 2020 年 12 月 2 日 | 批次集预设 | 了解如何使用 Dynamic Media 中的批次集预设自动创建图像集和旋转集。请参阅[批次集预设](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/batch-set-presets-dm)。 |
| 2020 年 12 月 2 日 | Dynamic Media 中的辅助功能 | Dynamic Media 和 Dynamic Media 查看器在整个创作用户界面中都支持键盘控件和各类辅助技术，如 JAWS 和 NVDA 屏幕阅读器。请参阅 [Dynamic Media 中的辅助功能](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/accessibility-dm)。 |
| 2020 年 10 月 29 日 | 核心组件 | 核心组件版本 2.12.0 中引入了新的 POST 表单处理程序；通过上下文感知配置包含自定义 CSS、JavaScript 和元数据标记的功能；以及可简化自定义组件中的数据层集成的 **DataLayerBuilderutility**。该版本与[创作文档](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction)以及[可在 GitHub 上获取的开发人员详细信息和项目下载](https://github.com/adobe/aem-core-wcm-components)一起提供。 |
| 2020 年 9 月 24 日 | 完成新的 Dynamic Media 配置后发送收件箱通知 | 当设置完新的 Dynamic Media 配置时，您将在 Experience Manager 收件箱中收到相应状态通知。此通知会告知您配置是否成功。如果配置失败，此通知将提供错误代码。请在联系 Adobe 客户关怀部门时提供此错误代码。<br>请参阅[对新的 Dynamic Media 配置进行故障排除](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/config-dm)。 |
| 2020 年 9 月 24 日 | 在 Dynamic Media 配置中重置密码。 | 允许在 Dynamic Media 中首次设置临时密码和后续重置密码，而不是通过 Dynamic Media Classic 进行。请参阅[在 Cloud Services 中创建 Dynamic Media 配置](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/config-dm)中的步骤 6 和 7，以及[更改 Dynamic Media 密码](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/config-dm)。 |
| 2020 年 9 月 24 日 | 使用 Dynamic Media 中的“选择性发布”功能 | 您可以选择在文件夹级别向 Experience Manager 或 Dynamic Media 发布资产或从中取消发布资产。您可以通过使用“管理出版物”或“快速发布”来完成此任务，而不是仅依赖 Dynamic Media 配置，其设置全局适用于 Dynamic Media 实例中的所有文件夹。<br>请参阅[使用 Dynamic Media 中的“选择性发布”功能](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/selective-publishing)。 |
| 2020 年 9 月 11 日 | 单页面应用程序 | 单页面应用程序 (SPA) 编辑器 JavaScript SDK [现已开源](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/hybrid/reference-materials)。 |
| 2020 年 8 月 27 日 | Dynamic Media 中的 CDN 失效功能 | 您现在可以从 Dynamic Media 发送请求，以使 CDN 缓存在几分钟内过期。当您更新资产并希望这些更改立即在您的网站上生效时，此功能非常有用。<br>请参阅[通过 Dynamic Media 使 CDN 缓存失效](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/invalidate-cdn-cache-dynamic-media)。 |
| 2020 年 8 月 11 日 | 用于发布页面的打开和关闭时间属性 | 使用[打开和关闭时间属性](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/sites-console/page-properties)发布页面时，请查看“页面属性”中的“基本”选项卡，您现在可以[预配置自动复制](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/operations/replication)。 |
| 2020 年 7 月 23 日 | 核心组件 | 核心组件版本 2.11.0 中引入了对 AMP 的支持，该版本现在与[创作文档](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction)以及[可在 GitHub 上获取的开发人员详细信息和项目下载](https://github.com/adobe/aem-core-wcm-components)一起提供。 |
| 2020 年 7 月 15 日 | Sling 备忘单 | 已将 [Sling 备忘单](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/full-stack/sling-cheatsheet)更新为引用 [HTL。](https://experienceleague.adobe.com/en/docs/experience-manager-htl/content/overview) |
| 2020 年 6 月 24 日 | 内容片段 | [已对文档进行了更新，因为模型现在为标准模型。](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-fragments/content-fragments) |
| 2020 年 6 月 19 日 | Experience Manager | Adobe 旨在从其代码、文档和体验中使用公平的术语。<br>为此，已更新该文档集。 |
| 2020 年 6 月 19 日 | 核心组件 | 核心组件版本 2.10.0 中引入了 PDF 查看器组件，该版本现在与[创作文档](https://experienceleague.adobe.com/en/docs/experience-manager-core-components/using/introduction)以及[可在 GitHub 上获取的开发人员详细信息和项目下载](https://github.com/adobe/aem-core-wcm-components)一起提供。 |
| 2020 年 6 月 4 日 | 使用 Brand Portal 配置 Experience Manager Assets as a Cloud Service | Adobe I/O 已升级到 Adobe Developer Console，现在具有新品牌标识、用户界面和工作流。已基于最新的 Adobe Developer Console 工作流更新文档，以[使用 Brand Portal 配置 Experience Manager Assets as a Cloud Service。](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal) |
| 2020 年 6 月 1 日 | 富文本编辑器 (RTE) | 以下有关富文本编辑器 (RTE) 的文章适用于 Adobe Experience Manager as a Cloud Service：<br>- [配置 RTE](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/configuring-and-extending/rich-text-editor)<br>- [配置每个插件](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins)<br>- [配置 RTE 以创建无障碍页面](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/configuring-and-extending/rte-accessible-content)<br>- [使用 RTE 创作内容](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/page-editor/rich-text-editor) |
| 2020 年 5 月 29 日 | 核心组件 | 核心组件版本 2.9.0 中引入了与 Adobe Client Data Layer 的集成以及一个新的进度条组件，该版本现在与“创作文档”以及“可在 GitHub 上获取的开发人员详细信息和项目下载”一起提供。 |
| 2020 年 5 月 19 日 | 辅助功能和 WCAG 2.1 准则 | 有关 WCAG 2.1 准则的更新：<br>- [Adobe Experience Manager as a Cloud Service 和 Web 无障碍准则](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/compliance/accessibility/web-accessibility)<br>- [WCAG 2.1 快速指南](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/compliance/accessibility/quick-guide-wcag)<br>- [创建无障碍内容（WCAG 2.1 合规）](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/page-editor/accessible-content) |
| 2020 年 5 月 4 日 | Dynamic Media 中不受支持的图像格式 | 关于 Dynamic Media 中不受支持的光栅图像文件格式的子类型的信息。<br>请参阅 [Dynamic Media 中不受支持的光栅图像格式](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/administer/assets-formats)。 |
| 2020 年 4 月 20 日 | 内容片段 | 关于 [Experience Manager Assets HTTP API 中的内容片段支持](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/admin/assets-api-content-fragments)、[自定义和扩展内容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/configuring-and-extending/content-fragments-customizing)以及[用于呈现的内容片段配置组件](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/configuring-and-extending/content-fragments-configuring-components-rendering)的信息。 |
| 2020 年 4 月 9 日 | 使用 Brand Portal 配置 Experience Manager Assets as a Cloud Service | Experience Manager Assets as a Cloud Service 现在支持 Brand Portal。 您可以在 Adobe I/O 上使用 Experience Manager Assets as a Cloud Service 配置 Brand Portal 租户：<br>- [使用 Brand Portal 配置 Experience Manager Assets as a Cloud Service ](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/brand-portal/configure-aem-assets-with-brand-portal)<br>- [将资产发布到 Brand Portal](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/brand-portal/publish-to-brand-portal) |
| 2020 年 4 月 9 日 | Adobe Asset Link v2.0 版本 | Adobe Asset Link 2.0 支持使用多个 Adobe Experience Manager 环境，并支持 Experience Manager as a Cloud Service。 在使用 AAL 将资产上传到文件夹后，营销人员可使用 Experience Manager 配置自动执行资产处理工作流。 <br>请参阅 [Adobe Asset Link](https://helpx.adobe.com/cn/cn/enterprise/using/adobe-asset-link.html)。 |
| 2020 年 3 月 24 日 | 配置 Dynamic Media 云服务 | 在配置 Dynamic Media 云服务时有新选项可用：<br>**选择性发布** - 当选择此选项时，即意味着自动发布资产仅供安全预览。可显式地将资产发布到 Experience Manager，而不发布到 DMS7 以供投放在公共域中。<br>请参阅[配置 Dynamic Media 云服务](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/config-dm)。 |
| 2020 年 3 月 2 日 | Dynamic Media — 智能裁剪 | 在 Dynamic Media 组件中使用智能裁切时，现在有一个新选项可用：<br>**启用宽高比匹配** - 选择此选项可让 Dynamic Media 选取一个最符合原始图像宽高比的智能裁切演绎版。<br>请参阅[使用智能裁剪时](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/adding-dynamic-media-assets-to-pages)。 |
| 2020 年 2 月 25 日 | 基于角色的权限 | Cloud Manager 预配置了一些具有适当权限的角色。每个角色均具有特定权限、预配置任务或与之关联的权限。[“基于角色的权限”页面](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager)列出了可用功能以及能够执行各项功能的角色。 |
| 2020 年 2 月 15 日 | 云中的调度程序 | 为阐明可用选项以及各个选项的使用方式，已对[调度程序和 CDN](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/dispatcher) 以及[明确使调度程序缓存失效](https://experienceleague.adobe.com/en/docs/experience-manager-dispatcher/using/configuring/page-invalidate)部分进行了更新。 |

## [!DNL Experience Manager] 6.5 {#aem-65}

| 日期 | 主题 | 更改 |
| --- | --- | --- |
| 2021 年 11 月 25 日 | [!DNL Experience Manager] 6.5 Service Pack 11 | 现已推出 [[!DNL Experience Manager] 6.5 Service Pack 11](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-11)。 |
| 2021 年 11 月 3 日 | 智能裁切视频查看器 API | Dynamic Media 查看器参考指南中现在提供了新的[智能裁切视频查看器 API 文档](https://experienceleague.adobe.com/en/docs/dynamic-media-developer-resources/library/viewers-for-aem-assets-only/smartcropvideo/c-html5-aem-smartcropvideo-viewer-reference)。 |
| 2021 年 8 月 26 日 | [!DNL Experience Manager] 6.5 Service Pack 10 | 现已推出 [[!DNL Experience Manager] 6.5 Service Pack 10](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-10)。 |
| 2021 年 5 月 27 日 | [!DNL Experience Manager] 6.5 Service Pack 9 | 现已推出 [[!DNL Experience Manager] 6.5 Service Pack 9](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-9)。 |
| 2021 年 3 月 11 日 | [!DNL Experience Manager] 6.5 Service Pack 8 | 现已推出 [[!DNL Experience Manager] 6.5 Service Pack 8](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-8)。 |
| 2020 年 11 月 25 日 | Dynamic Media 中的辅助功能 | Dynamic Media 和 Dynamic Media 查看器在整个创作用户界面中都支持键盘控件和各类辅助技术，如 JAWS 和 NVDA 屏幕阅读器。请参阅 [Dynamic Media 中的辅助功能](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/accessibility-dm)。 |
| 2020 年 11 月 26 日 | Experience Manager 6.5 Service Pack 7 | 现已推出 [Experience Manager 6.5 Service Pack 7](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-7)。 |
| 2020 年 9 月 3 日 | Dynamic Media 中的 CDN 失效功能 | 您现在可以从 Dynamic Media 发送请求，以使 CDN 缓存在几分钟内过期。当您更新资产并希望这些更改立即在您的网站上生效时，此功能非常有用。<br>请参阅[通过 Dynamic Media 使 CDN 缓存失效](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/invalidate-cdn-cache-dynamic-media)。 |
| 2020 年 9 月 3 日 | 使用 Dynamic Media 中的“选择性发布”功能 | 您可以选择在文件夹级别向 Experience Manager 或 Dynamic Media 发布资产或从中取消发布资产。您可以通过使用&#x200B;**[!UICONTROL 管理出版物]**&#x200B;或&#x200B;**[!UICONTROL 快速发布]**&#x200B;来完成此任务，而不是仅依赖 **Dynamic Media 配置**，其设置全局适用于 Dynamic Media 实例中的所有文件夹。<br>请参阅[使用 Dynamic Media 中的“选择性发布”功能](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/selective-publishing)。 |
| 2020 年 9 月 3 日 | Experience Manager 6.5 Service Pack 6 | 现已推出 [Experience Manager 6.5 Service Pack 6](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-6)。 |
| 2020 年 7 月 29 日 | 多站点管理器 | 已对[创建同步操作](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/extending-aem/extending-msm)和[创建转出配置](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/extending-aem/extending-msm)过程进行了更新。 |
| 2020 年 7 月 15 日 | Sling 备忘单 | 已将 [Sling 备忘单](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/implementing/developing/platform/sling-cheatsheet)更新为引用 [HTL。](https://experienceleague.adobe.com/en/docs/experience-manager-htl/content/overview) |
| 2020 年 6 月 19 日 | Adobe Experience Manager | Adobe 旨在从其代码、文档和体验中使用公平的术语。<br>因此对此文档集作出了更新以反映此公平性。 |
| 2020 年 6 月 4 日 | 使用 Brand Portal 配置 Experience Manager Assets | Adobe I/O 已升级到 Adobe Developer Console，现在具有新品牌标识、用户界面和工作流。已基于最新的 Adobe Developer Console 工作流更新文档，以使用 Brand Portal 配置 Experience Manager Assets：<br>- [使用 Brand Portal 配置 Experience Manager Assets ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal)<br>- [将旧配置升级到 Adobe Developer Console](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/brandportal/configure-aem-assets-with-brand-portal) |
| 2020 年 6 月 4 日 | Experience Manager 6.5 Service Pack 5 | 现已推出 [Experience Manager 6.5 Service Pack 5](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-5)。 |
| 2020 年 5 月 25 日 | 辅助功能和 WCAG 2.1 准则 | 有关 WCAG 2.1 准则的更新：<br>- [Adobe Experience Manager as a Cloud Service 和 Web 无障碍准则](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/compliance/accessibility/web-accessibility)<br>- [WCAG 2.1 快速指南](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/compliance/accessibility/quick-guide-wcag)<br>- [创建无障碍内容（WCAG 2.1 合规）](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/page-editor/accessible-content) |
| 2020 年 4 月 13 日 | 资产版本控制 | 已更新有关如何创建、预览和恢复的内容和视频 [Experience Manager中的资源版本](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/managing/manage-assets). |
| 2020 年 4 月 13 日 | 资产处理 | 新增了有关如何使用工作流处理资产的概述。此外，还新增了介绍如何[自动触发资产处理工作流](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/using/assets-workflow)的主题。 |
| 2020 年 3 月 30 日 | Dynamic Media — 智能成像 | “智能成像帮助”主题已全面更新，其中新增了一些信息，包括描述新增的智能成像优化的图像资产示例。<br>请参阅[智能成像](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/imaging-faq)。 |
| 2020 年 3 月 5 日 | Experience Manager 6.5 Service Pack 4 | 现已推出 [Experience Manager 6.5 Service Pack 4](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/release-notes/service-pack/6-5-4)。 |
| 2020 年 3 月 4 日 | 配置 Dynamic Media — Scene7 模式 | 可在“Dynamic Media 配置”页面上的“工具”>“云服务”中找到新增的“同步所有内容”选项。<br>请参阅[创建 Dynamic Media 配置](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/config-dms7)。 |
