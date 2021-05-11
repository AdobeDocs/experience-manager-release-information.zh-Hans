---
title: '[!DNL Experience Manager] 近期文档更新'
description: ' [!DNL Experience Manager]  文档中的新增内容、更新内容或修改内容'
contentOwner: trushton
exl-id: 8c136a03-f961-4854-af38-45457b85d289
translation-type: tm+mt
source-git-commit: fa68729be0642a7369e2a1bef643fac32a76bc3e
workflow-type: tm+mt
source-wordcount: '3247'
ht-degree: 99%

---

# [!DNL Experience Manager] 文档：近期文档更新 {#aem-documentation-recent-documentation-updates}

本页列出了有关 [!DNL Adobe Experience Manager] 的重要文档更改和更新。

您还可以查看[先前的文档更新](previous-documentation-updates.md)。

## [!DNL Adobe Experience Manager] as a [!DNL Cloud Service] {#aem-as-a-cloud-service}

>[!NOTE]
>
>AEM as a Cloud Service 每月发布一次。
>
>有关各个发行版本（当前版本和早期版本）的文档，请参阅[发行说明](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/release-notes/release-notes/release-notes-current.html?lang=zh-Hans)。

| 日期 | 主题 | 所做更改 |
| --- | --- | --- |
| 2020 年 12 月 2 日 | 批次集预设 | 了解如何使用 Dynamic Media 中的批次集预设自动创建图像集和旋转集。请参阅[批次集预设](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/batch-set-presets-dm.html#dynamicmedia)。 |
| 2020 年 12 月 2 日 | Dynamic Media 中的辅助功能 | Dynamic Media 和 Dynamic Media 查看器在整个创作用户界面中都支持键盘控件和各类辅助技术，如 JAWS 和 NVDA 屏幕阅读器。请参阅 [Dynamic Media 中的辅助功能](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/dynamicmedia/accessibility-dm.html#dynamicmedia)。 |
| 2020 年 10 月 29 日 | 核心组件 | 核心组件版本 2.12.0 中引入了新的 POST 表单处理程序；通过上下文感知配置包含自定义 CSS、JavaScript 和元数据标记的功能；以及可简化自定义组件中的数据层集成的 **DataLayerBuilderutility**。该版本与[创作文档](https://docs.adobe.com/content/help/zh-Hans/experience-manager-core-components/using/introduction.html)以及[可在 GitHub 上获取的开发人员详细信息和项目下载](https://github.com/adobe/aem-core-wcm-components)一起提供。 |
| 2020 年 9 月 24 日 | 完成新的 Dynamic Media 配置后发送收件箱通知 | 当设置完新的 Dynamic Media 配置时，您将在 [!DNL Experience Manager] 收件箱中收到相应状态通知。此通知会告知您配置是否成功。如果配置失败，此通知将提供错误代码。请在联系 Adobe 客户关怀部门时提供此错误代码。<br>请参阅[对新的 Dynamic Media 配置进行故障排除](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#troubleshoot-dm-config)。 |
| 2020 年 9 月 24 日 | 在 Dynamic Media 配置中重置密码。 | 允许在 Dynamic Media 中首次设置临时密码后重置密码，这与使用 Dynamic Media Classic 时不同。请参阅[在  [!DNL Cloud Service] 中创建新的 Dynamic Media 配置](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#configuring-dynamic-media-cloud-services)中的步骤 6 和 7，以及[更改 Dynamic Media 密码](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#change-dm-password)。 |
| 2020 年 9 月 24 日 | 使用 Dynamic Media 中的“选择性发布”功能 | 通过使用“管理发布”或“快速发布”，您可以在文件夹级别选择向 [!DNL Experience Manager] 或 Dynamic Media 发布或取消发布资产，也可以选择从中发布或取消发布资产，而不是仅依赖其设置全局应用于 Dynamic Media 实例中的所有文件夹的 Dynamic Media 配置。<br>请参阅[使用 Dynamic Media 中的“选择性发布”功能](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/dynamicmedia/selective-publishing.html)。 |
| 2020 年 9 月 11 日 | 单页应用程序 | 单页应用程序 (SPA) 编辑器 JavaScript SDK [现已开源](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/headless/spa/reference-materials.html)。 |
| 2020 年 8 月 27 日 | Dynamic Media 中的 CDN 失效功能 | 您现在可以从 Dynamic Media 发送请求，以使 CDN 缓存在几分钟内过期。当您更新资产并希望这些更改立即在您的网站上生效时，此功能非常有用。<br>请参阅[通过 Dynamic Media 使 CDN 缓存失效](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/dynamicmedia/invalidate-cdn-cache-dynamic-media.html)。 |
| 2020 年 8 月 11 日 | 用于发布页面的打开和关闭时间属性 | 使用[打开和关闭时间属性](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/sites/authoring/fundamentals/page-properties.html#basic)发布页面时，请查看“页面属性”中的“基本”选项卡，您现在可以[预配置自动复制](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/operations/replication.html?lang=zh-Hans#on-and-off-times-trigger-configuration)。 |
| 2020 年 7 月 23 日 | 核心组件 | 核心组件版本 2.11.0 中引入了对 AMP 的支持，该版本现在与[创作文档](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html)以及[可在 GitHub 上获取的开发人员详细信息和项目下载](https://github.com/adobe/aem-core-wcm-components)一起提供。 |
| 2020 年 7 月 15 日 | Sling 备忘单 | 已将 [Sling 备忘单](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/developing/sling-cheatsheet.html)更新为引用 [HTL](https://docs.adobe.com/content/help/zh-Hans/experience-manager-htl/using/overview.html)。 |
| 2020 年 6 月 24 日 | 内容片段 | [已对文档进行了更新，因为模型现在为标准模型。](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/content-fragments/content-fragments.html) |
| 2020 年 6 月 19 日 | [!DNL Adobe Experience Manager] | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |
| 2020 年 6 月 19 日 | 核心组件 | 核心组件版本 2.10.0 中引入了 PDF 查看器组件，该版本现在与[创作文档](https://docs.adobe.com/content/help/en/experience-manager-core-components/using/introduction.html)以及[可在 GitHub 上获取的开发人员详细信息和项目下载](https://github.com/adobe/aem-core-wcm-components)一起提供。 |
| 2020 年 6 月 4 日 | 使用 Brand Portal 配置 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] | Adobe I/O 已升级到 Adobe Developer Console，现在具有新品牌标识、用户界面和工作流。我们已根据最新的[使用 Brand Portal 配置  [!DNL Experience Manager Assets] as a [!DNL Cloud Service] ](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html) 这一 Adobe Developer Console 工作流对文档进行了相应更新。 |
| 2020 年 6 月 1 日 | 富文本编辑器 (RTE) | 以下有关富文本编辑器 (RTE) 的文章适用于 [!DNL Experience Manager] as a [!DNL Cloud Service]：<br>- [配置 RTE](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/configuring-and-extending/rich-text-editor.html)<br>- [配置每个插件](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/configuring-and-extending/configure-rich-text-editor-plug-ins.html)<br>- [配置 RTE 以创建无障碍页面](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/configuring-and-extending/rte-accessible-content.html)<br>- [使用 RTE 创作内容](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/sites/authoring/fundamentals/rich-text-editor.html) |
| 2020 年 5 月 29 日 | 核心组件 | 核心组件版本 2.9.0 中引入了与 Adobe Client Data Layer 的集成以及一个新的进度条组件，该版本现在与“创作文档”以及“可在 GitHub 上获取的开发人员详细信息和项目下载”一起提供。 |
| 2020 年 5 月 19 日 | 辅助功能和 WCAG 2.1 准则 | 有关 WCAG 2.1 准则的更新：<br>- [[!DNL Experience Manager] as a [!DNL Cloud Service]  和 Web 无障碍准则](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/onboarding/accessibility/web-accessibility.html)<br>- [《WCAG 2.1 快速指南》](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/onboarding/accessibility/quick-guide-wcag.html)<br>- [创建无障碍内容（WCAG 2.1 合规）](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |
| 2020 年 5 月 4 日 | Dynamic Media 中不受支持的图像格式 | 关于 Dynamic Media 中不受支持的光栅图像文件格式的子类型的信息。<br>请参阅 [Dynamic Media 中不受支持的光栅图像格式](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/administer/assets-formats.html#unsupported-image-formats-dynamic-media)。 |
| 2020 年 4 月 20 日 | 内容片段 | 关于 [ [!DNL Experience Manager]  Assets HTTP API 中的内容片段支持](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/admin/assets-api-content-fragments.html)、[自定义和扩展内容片段](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/configuring-and-extending/content-fragments-customizing.html)以及[用于呈现的内容片段配置组件](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/configuring-and-extending/content-fragments-configuring-components-rendering.html)的信息。 |
| 2020 年 4 月 9 日 | 使用 Brand Portal 配置 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] | [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 现在支持 Brand Portal。您可以在 Adobe I/O 上为 Brand Portal 租户配置 [!DNL Experience Manager Assets] as a [!DNL Cloud Service]：<br>- [使用 Brand Portal 配置  [!DNL Experience Manager Assets] as a [!DNL Cloud Service] ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)<br>- [将资产发布到 Brand Portal](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/brand-portal/publish-to-brand-portal.html) |
| 2020 年 4 月 9 日 | Adobe Asset Link v2.0 版本 | Adobe Asset Link 2.0 支持与多个 [!DNL Experience Manager] 环境结合使用，也支持 [!DNL Experience Manager] as a [!DNL Cloud Service]。在使用 AAL 将资产上传到文件夹后，[!DNL Experience Manager] 支持营销人员配置自动执行的资产处理工作流。<br>请参阅 [Adobe Asset Link](https://helpx.adobe.com/cn/enterprise/using/adobe-asset-link.html)。 |
| 2020 年 3 月 24 日 | 配置 Dynamic Media 云服务 | 在配置 Dynamic Media 云服务时，现在有一个新的可用选项：<br>**选择性发布** — 如果选择该选项，即表示只会为了安全预览自动发布资产，且可以通过明确将资产发布到 [!DNL Experience Manager]，将其交付到公共域中，而无需发布到 DMS7。<br>请参阅[配置 Dynamic Media 云服务](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/dynamicmedia/config-dm.html#configuring-dynamic-media-cloud-services)。 |
| 2020 年 3 月 2 日 | Dynamic Media — 智能裁剪 | 在 Dynamic Media 组件中使用智能裁剪时，现在有一个新选项可用：<br>**启用宽高比匹配** - 选择此选项以使 Dynamic Media 可选取一个最符合原始图像宽高比的智能裁剪演绎版。<br>请参阅[使用智能裁剪时](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/assets/dynamicmedia/adding-dynamic-media-assets-to-pages.html#when-working-with-smart-crop)。 |
| 2020 年 2 月 25 日 | 基于角色的权限 | Cloud Manager 预配置了一些具有适当权限的角色。每个角色都有相关联的特定权限、预配置的任务或权限。[基于角色的权限](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/onboarding/what-is-required/role-based-permissions.html)页面列出了可用功能以及能够执行各项功能的角色。 |
| 2020 年 2 月 15 日 | 云中的调度程序 | 为阐明可用选项以及各个选项的使用方式，已对[调度程序和 CDN](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/dispatcher/overview.html#dispatcher-cdn) 以及[明确使调度程序缓存失效](https://docs.adobe.com/content/help/zh-Hans/experience-manager-cloud-service/implementing/dispatcher/overview.html#explicit-invalidation)部分进行了更新。 |

## [!DNL Experience Manager] 6.5 {#aem-65}

| 日期 | 主题 | 所做更改 |
| --- | --- | --- |
| 2021 年 3 月 11 日 | [!DNL Experience Manager] 6.5 Service Pack 8 | 提供了 [[!DNL Experience Manager] 6.5 Service Pack 8](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=zh-Hans#service-pack)。 |
| 2020 年 11 月 25 日 | Dynamic Media 中的辅助功能 | Dynamic Media 和 Dynamic Media 查看器在整个创作用户界面中都支持键盘控件和各类辅助技术，如 JAWS 和 NVDA 屏幕阅读器。请参阅 [Dynamic Media 中的辅助功能](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/accessibility-dm.html?lang=zh-Hans#dynamic)。 |
| 2020 年 11 月 26 日 | [!DNL Experience Manager] 6.5 Service Pack 7 | 提供了 [[!DNL Experience Manager]  6.5 Service Pack 7](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html#service-pack)。 |
| 2020 年 9 月 3 日 | Dynamic Media 中的 CDN 失效功能 | 您现在可以从 Dynamic Media 发送请求，以使 CDN 缓存在几分钟内过期。当您更新资产并希望这些更改立即在您的网站上生效时，此功能非常有用。<br>请参阅[通过 Dynamic Media 使 CDN 缓存失效](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/dynamic/invalidate-cdn-cache-dynamic-media.html)。 |
| 2020 年 9 月 3 日 | 使用 Dynamic Media 中的“选择性发布”功能 | 通过使用&#x200B;**“管理发布”**&#x200B;或&#x200B;**“快速发布”**，您可以在文件夹级别选择向 [!DNL Experience Manager] 或 Dynamic Media 发布或取消发布资产，也可以选择从中发布或取消发布资产，而不是仅依赖其设置全局应用于 Dynamic Media 实例中的所有文件夹的 **“Dynamic Media 配置”**。<br>请参阅[使用 Dynamic Media 中的“选择性发布”功能](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/dynamic/selective-publishing.html)。 |
| 2020 年 9 月 3 日 | [!DNL Experience Manager] 6.5 Service Pack 6 | 提供了 [[!DNL Experience Manager]  6.5 Service Pack 6](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html?lang=zh-Hans)。 |
| 2020 年 7 月 29 日 | 多站点管理器 | 已对[创建新同步操作](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/developing/extending-aem/extending-msm.html#creating-a-new-synchronization-action)和[创建新转出配置](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/developing/extending-aem/extending-msm.html#creating-a-new-rollout-configuration)过程进行了更新。 |
| 2020 年 7 月 15 日 | Sling 备忘单 | 已将 [Sling 备忘单](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/developing/platform/sling-cheatsheet.html)更新为引用 [HTL](https://docs.adobe.com/content/help/en/experience-manager-htl/using/overview.html)。 |
| 2020 年 6 月 19 日 | Adobe Experience Manager | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |
| 2020 年 6 月 4 日 | 使用 Brand Portal 配置 [!DNL Experience Manager Assets] | Adobe I/O 已升级到 Adobe Developer Console，现在具有新品牌标识、用户界面和工作流。我们已根据最新的“使用 Brand Portal 配置 [!DNL Experience Manager Assets]”这一 Adobe Developer Console 工作流对文件进行了相应更新：<br>- [使用 Brand Portal 配置  [!DNL Experience Manager Assets] ](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html)<br>- [将旧版配置升级到 Adobe Developer Console](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65) |
| 2020 年 6 月 4 日 | [!DNL Experience Manager] 6.5 Service Pack 5 | 提供了 [[!DNL Experience Manager]  6.5 Service Pack 5](https://experienceleague.adobe.com/docs/experience-manager-65/release-notes/service-pack/sp-release-notes.html)。 |
| 2020 年 5 月 25 日 | 辅助功能和 WCAG 2.1 准则 | 有关 WCAG 2.1 准则的更新：<br>- [Adobe Experience Manager as a  [!DNL Cloud Service]  和 Web 无障碍准则](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/web-accessibility.html)<br>- [《WCAG 2.1 快速指南》](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/onboarding/accessibility/quick-guide-wcag.html)<br>- [创建无障碍内容（WCAG 2.1 合规）](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/sites/authoring/fundamentals/accessible-content.html) |
| 2020 年 4 月 13 日 | 资产版本控制 | 已更新有关如何创建、预览以及恢复 [ [!DNL Experience Manager] 中资产版本](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/managing/managing-assets-touch-ui.html#asset-versioning)的内容和视频。 |
| 2020 年 4 月 13 日 | 资产处理 | 新增了有关如何使用工作流处理资产的概述。此外，还新增了介绍如何[自动触发资产处理工作流](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/using/assets-workflow.html)的主题。 |
| 2020 年 3 月 30 日 | Dynamic Media — 智能成像 | “智能成像帮助”主题已全面更新，其中新增了一些信息，包括描述新增的智能成像优化的图像资产示例。<br>请参阅[智能成像](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/dynamic/imaging-faq.html)。 |
| 2020 年 3 月 5 日 | [!DNL Experience Manager] 6.5 Service Pack 4 | 提供了 [[!DNL Experience Manager]  6.5 Service Pack 4](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/release-notes/sp-release-notes.html)。 |
| 2020 年 3 月 4 日 | 配置 Dynamic Media — Scene7 模式 | “Dynamic Media 配置”页面的“工具”>“云服务”中现在新增了一个选项，即“同步所有内容”。<br>请参阅[创建 Dynamic Media 配置](https://docs.adobe.com/content/help/zh-Hans/experience-manager-65/assets/dynamic/config-dms7.html#configuring-dynamic-media-cloud-services)。 |

## [!DNL Experience Manager] 6.4 {#aem-64}

| 日期 | 主题 | 所做更改 |
| --- | --- | --- |
| 2021 年 2 月 25 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 4 | 提供了 [[!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 4](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/cfp-release-notes.html?lang=zh-Hans)。 |
| 2020 年 11 月 26 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 3 | 提供了 [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 3](https://experienceleague.adobe.com/docs/experience-manager-64/release-notes/cfp-release-notes.html)。 |
| 2020 年 9 月 3 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 2 | 提供了 [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 2](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/release-notes/cfp-release-notes.html)。 |
| 2020 年 7 月 29 日 | [多站点管理器] | 已对[创建新同步操作](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/developing/extending-aem/extending-msm.html#creating-a-new-synchronization-action)和[创建新转出配置](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/developing/extending-aem/extending-msm.html#creating-a-new-rollout-configuration)过程进行了更新。 |
| 2020 年 6 月 19 日 | Adobe Experience Manager | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |
| 2020 年 6 月 4 日 | [!DNL Experience Manager] 6.4 Service Pack 8 Cumulative Fix Pack 1 | 提供了 [[!DNL Experience Manager]  6.4 Service Pack 8 Cumulative Fix Pack 1](https://docs.adobe.com/content/help/en/experience-manager-64/release-notes/cfp-release-notes.html)。 |
| 2020 年 4 月 13 日 | 资产处理 | 新增了有关如何使用工作流处理资产的概述。此外，还新增了介绍如何[自动触发资产处理工作流](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/assets/using/assets-workflow.html)的主题。 |
| 2020 年 3 月 30 日 | Dynamic Media — 智能成像 | “智能成像帮助”主题已全面更新，其中新增了一些信息，包括描述新增的智能成像优化的图像资产示例。<br>请参阅[智能成像](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/assets/dynamic/imaging-faq.html)。 |
| 2020 年 3 月 5 日 | [!DNL Experience Manager] 6.4 Service Pack 8 | 提供了 [[!DNL Experience Manager]  6.4 Service Pack 8](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/release-notes/sp-release-notes.html)。 |

## [!DNL Experience Manager] 6.3 {#aem-2}

| 日期 | 主题 | 所做更改 |
| --- | --- | --- |
| 2020 年 6 月 19 日 | Adobe Experience Manager | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |
| 2020 年 3 月 30 日 | Dynamic Media — 智能成像 | “智能成像帮助”主题已全面更新，其中新增了一些信息。<br>请参阅[智能成像](https://helpx.adobe.com/cn/experience-manager/6-3/assets/using/imaging-faq.html)。 |
| 2020 年 3 月 5 日 | [!DNL Experience Manager] 6.3.3.8 | 提供了适用于 [!DNL Experience Manager] 6.3 的 [Cumulative Fix Pack 6.3.3.8](https://helpx.adobe.com/cn/experience-manager/release-notes--aem-6-3-cumulative-fix-pack.html)。 |

## [!DNL Experience Manager] 6.2 {#aem-62}

| 日期 | 主题 | 所做更改 |
|---|---|---|
| 2020 年 6 月 19 日 | Adobe Experience Manager | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |

## [!DNL Experience Manager] 6.1 {#aem-61}

| 日期 | 主题 | 所做更改 |
|---|---|---|
| 2020 年 6 月 19 日 | Adobe Experience Manager | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |

## [!DNL Experience Manager] 桌面应用程序 {#aem-desktop-app}

| 日期 | 主题 | 所做更改 |
|---|---|---|
| 2020 年 8 月 27 日 | [!DNL Experience Manager] 桌面应用程序 2.0.3.2<br>[!DNL Experience Manager] 桌面应用程序支持 [!DNL Experience Manager] as a [!DNL Cloud Service]、[!DNL Experience Manager] 6.5、[!DNL Experience Manager] 6.4 以及 [!DNL Experience Manager] 6.3（含兼容包）。 | [!DNL Experience Manager] 桌面应用程序 2.0.3.2 对创意人员、营销人员和行业用户公开可用，可用于处理 [!DNL Experience Manager Assets]。<br>请参阅[发行说明](https://docs.adobe.com/content/help/zh-Hans/experience-manager-desktop-app/using/release-notes.html)。 |

## [!DNL Experience Manager Assets Brand Portal] {#aem-assets-brand-portal}

| 日期 | 主题 | 所做更改 |
| --- | --- | --- |
| 2020 年 10 月 27 日 | 从 [!DNL Experience Manager Assets] Brand Portal 下载资产 | 本文档涵盖以下重要更新：<br>- [改进了下载体验](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/download/brand-portal-download-assets.html)，使下载变得更加简捷、快速。管理员可以配置更多下载配置，以根据用户和企业的需求提供下载体验。<br>- 现在，从任何页面都可以一键导航到“文件”、“[收藏集](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/share/brand-portal-share-collection.html)”以及“共享的链接”。<br>- 用户现在可以[选择并下载特定的呈现版本](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/download/brand-portal-download-assets.html#download-assets-from-asset-details-page)。可在“资源详细信息”页面中的“演绎版”面板中找到下载演绎版的新选项。<br>- 为来宾用户会话设置 15 分钟的超时时间，可确保所有并发用户获得更好的体验。 |
| 2020 年 10 月 27 日 | [!DNL Experience Manager Assets] Brand Portal 2020.10.0 版 | 在 Brand Portal 2020.10.0 中，做出了以下改进：改善了资产下载工作流；新增了用于排除呈现版本的选项；允许直接从“呈现版本”面板进行下载；添加了允许特定用户组的访问和下载权限的配置；允许用户从任何 Brand Portal 页面轻松导航到“文件”、“收藏集”和“共享的链接”。<br>- [Brand Portal 新增功能](https://docs.adobe.com/content/help/zh-Hans/experience-manager/brand-portal/using/whats-new.html)<br>- [Brand Portal 2020.10.0 发行说明](https://docs.adobe.com/content/help/zh-Hans/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
| 2020 年 9 月 3 日 | 从 [!DNL Experience Manager Assets] Brand Portal 下载资产 | Brand Portal 管理员可以配置下载设置，以便在用户从 Brand Portal 下载资产时为其提供更加轻松便捷的下载体验。<br>本文档涵盖以下重要更新：<br>- [从 Brand Portal 下载资产](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/download/brand-portal-download-assets.html)<br>- [加速下载指南](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/download/accelerated-download.html)<br>- [应用图像预设](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/admin-tools/brand-portal-image-presets.html) |
| 2020 年 8 月 12 日 | [!DNL Experience Manager Assets] Brand Portal 6.4.7 版 | Brand Portal 6.4.7 中引入了新功能，这些新功能可改善 Brand Portal 用户的资产下载和 PDF 查看体验。<br>- [Brand Portal 新增功能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>- [Brand Portal 6.4.7 发行说明](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
| 2020 年 6 月 19 日 | Adobe Experience Manager | 在 Adobe，我们力图在所有代码、文档和体验中使用相同或者可互换使用的术语。<br>为此，我们一直在对此文档集进行一系列更新，且将来会继续进行更新。 |
| 2020 年 6 月 4 日 | [!DNL Experience Manager Assets] Brand Portal 6.4.6.2 版 | 在 Brand Portal 6.4.6.2 中，我们已根据最新的“使用 Brand Portal 配置 [!DNL Experience Manager Assets]”这一 Adobe Developer Console 工作流对文档进行了相应更新。此外，该版本中还包含有关“资产源”功能的修复。<br>有关详细信息，请参阅以下文章：<br>- [使用 Brand Portal 配置  [!DNL Experience Manager Assets] ](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br>- [Brand Portal 6.4.6.2 发行说明](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/introduction/brand-portal-release-notes.html)<br>- [Brand Portal 新增功能](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/introduction/whats-new.html)<br>- [常见问题解答](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/introduction/brand-portal-faqs.html)<br>- [Brand Portal 中的资产源](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/asset-sourcing-in-brand-portal/brand-portal-asset-sourcing.html)<br>- [Brand Portal 概述](https://docs.adobe.com/content/help/zh-Hans/experience-manager-brand-portal/using/introduction/brand-portal.html) |
| 2020 年 4 月 9 日 | 使用 Brand Portal 配置 [!DNL Experience Manager Assets] as a [!DNL Cloud Service] | [!DNL Experience Manager Assets] as a [!DNL Cloud Service] 现在支持 Brand Portal。您可以在 Adobe I/O 上为 Brand Portal 租户配置 [!DNL Experience Manager Assets] as a [!DNL Cloud Service]：<br>- [使用 Brand Portal 配置  [!DNL Assets] as a [!DNL Cloud Service] ](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/configure-aem-assets-with-brand-portal.html)<br>- [将资产发布到 Brand Portal](https://docs.adobe.com/content/help/en/experience-manager-cloud-service/assets/brand-portal/publish-to-brand-portal.html) |
| 2020 年 3 月 6 日 | 使用 Brand Portal 配置 [!DNL Assets]（内部部署版和 Managed Services 版） | 对于不同的 Experience Manager 版本，新增了关于如何[在 Adobe I/O 上使用 Brand Portal 配置 Experience Manager Assets](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html) 这一主题的文档。<br>有关详细信息，请参阅以下文章：<br>**AEM 6.5**<br>- [使用 Brand Portal 配置  [!DNL Assets] ](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br>- [将旧版配置升级到 Adobe I/O](https://docs.adobe.com/content/help/en/experience-manager-65/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-65)<br>**AEM 6.4**<br>- [使用 Brand Portal 配置  [!DNL Assets] ](https://docs.adobe.com/content/help/en/experience-manager-brand-portal/using/publish/configure-aem-assets-with-brand-portal.html)<br>- [将旧版配置升级到 Adobe I/O](https://docs.adobe.com/content/help/zh-Hans/experience-manager-64/assets/brandportal/configure-aem-assets-with-brand-portal.html#upgrade-integration-64)<br>**AEM 6.3**<br>- [使用 Brand Portal 配置  [!DNL Assets] ](https://helpx.adobe.com/cn/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html)<br>- [将旧版配置升级到 Adobe I/O](https://helpx.adobe.com/cn/experience-manager/6-3/assets/using/brand-portal-configuring-integration.html#Upgradeconfiguration) |
| 2020 年 2 月 27 日 | [!DNL Assets] Brand Portal 6.4.6 版 | 在 Brand Portal 6.4.6 中，[!DNL Assets] 与 Brand Portal 之间的授权渠道已更改为 Adobe I/O。[!DNL Experience Manager Assets] 6.3 和更高版本支持使用 Adobe I/O 配置 Brand Portal。<br>- [Brand Portal 新增功能](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/using/whats-new.html)<br>- [Brand Portal 发行说明](https://docs.adobe.com/content/help/en/experience-manager/brand-portal/release-notes/brand-portal-release-notes.html) |
