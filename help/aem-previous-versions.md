---
title: AEM、CQ和CRX的旧版本
description: 旧版 Adobe Experience Manager、CQ 和 CRX 的文档包。
translation-type: tm+mt
source-git-commit: 47b391ed659264b611f08d2fa9e45a923be5c445
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 23%

---


# [!DNL Adobe Experience Manager]、CQ和CRX {#older-versions-aem-cq-crx}的旧版本

## [!DNL Experience Manager]文档的旧版本{#older-version-aem-documentation}

本页所列的[!DNL Experience Manager]、CQ和CRX版本为“生命周期结束”，不再由Adobe正式出售。 您可以根据需要查阅我们针对这些旧版本最后发布的一版官方文档以进行自助。我们建议您升级到最新版本（当前为[[!DNL Experience Manager] 6.5](https://experienceleague.adobe.com/docs/experience-manager-65.html)）。

>[!NOTE]
>
>要了解[!DNL Experience Manager]版本何时将结束核心支持，请参见[产品和技术支持时段](https://helpx.adobe.com/cn/support/programs/eol-matrix.html)并搜索`AEM`。

### 安装之前 {#before-installation}

在下载包之前，请先确定谁将使用其内容。这将决定包的部署方式：

* 开发人员可在本地进行安装以便快速参考。
* 为了满足更为广泛的组织文档需求，建议在一个可从内部访问的非生产 AEM 创作实例中部署该包。

>[!NOTE]
>
>用户必须登录[!DNL Experience Manager]实例才能访问[!DNL Experience Manager]作者上的此内容。 默认情况下，此内容无法在 AEM 发布中访问（因其位于 /libs 下）。

## 软件分发位置{#software-distribution-locations}

您需要有效的Adobe ID:

* 如果您没有Adobe ID，可以在www.adobe.com创建
如果您在创建或管理Adobe ID时需要帮助，请参阅本指南[](https://helpx.adobe.com/manage-account.html)

| [!DNL Experience Manager] 版本 | 软件分发链接 |
|:-----------:|:--------------------------------------------------:|
| [!DNL Experience Manager] 6.1 | [从软件分发下载AEM-DOCS-6.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-1.zip) |
| [!DNL Experience Manager] 6.0 | [从软件分发下载AEM-DOCS-6.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-6-0.zip) |
| [!DNL Experience Manager] 5.6.1 | [从软件分发下载AEM-DOCS-5.6.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6-1.zip) |
| [!DNL Experience Manager] 5.6 | [从软件分发下载AEM-DOCS-5.6](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-6.zip) |
| CQ 5.5 | [从软件分发下载CQ-DOCS-5.5](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Fadobe%2Fpackages%2Faem-docs%2Faem-docs-5-5.zip) |
| CQ 5.4 | [从软件分发下载CQ-DOCS-5.4](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-4.zip) |
| CQ 5.3 | [从软件分发下载CQ-DOCS-5.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/aem-docs-5-3.zip) |
| CRX 2.3 | [从软件分发下载CRX-DOCS-2.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-3.zip) |
| CRX 2.2 | [从软件分发下载CRX-DOCS-2.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-2.zip) |
| CRX 2.1 | [从软件分发下载CRX-DOCS-2.1](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-1.zip) |
| CRX 2.0 | [从软件分发下载CRX-DOCS-2.0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/aem-docs/crx-docs-2-0.zip) |

## 如何安装文档包 {#how-to-install-documentation-package}

要安装旧版文档包，您必须在本地驱动器或网络驱动器上安装并运行[!DNL Experience Manager]。

### 下载文档包{#download-documentation-package}

1. 从上表中，选择要下载的[!DNL Experience Manager]文档版本的链接。 例如，AEM 5.6.1。

1. 使用您的Adobe ID登录。 如果您没有 ID，请创建一个。

1. 选择&#x200B;**[!UICONTROL 下载]**&#x200B;按钮。

1. 以下是您将看到的内容示例：

![软件分发示例](assets/screen_shot_2020-07-10at161922.jpg)

### 在本地实例{#install-package-local-instance}上安装软件包

1. 打开[!DNL Experience Manager]用户界面。 在Web浏览器中输入：`http://localhost:4502/`。 以管理员身份登录。

1. 选择&#x200B;**[!UICONTROL 工具]** > **[!UICONTROL 部署]** > **[!UICONTROL 包]**。

1. 从包管理器UI中，选择&#x200B;**[!UICONTROL 上传包]**。

1. 浏览到您将 AEM 5.6.1 包 (aem-docs-5-6-1.zip) 下载到的位置。

1. 选择该包，然后单击&#x200B;**[!UICONTROL 确定]**。

1. 上传包后，您将需要安装它。

1. 在包管理器UI中，找到该包并选择&#x200B;**[!UICONTROL 安装]**。

1. 在确认对话框中，再次选择&#x200B;**[!UICONTROL 安装]**。 注意：安装过程将需要花费几分钟时间。

1. 在Web浏览器中，启动文档页面。 在AEM 5.6.1示例中，URL为：http://localhost:4502/libs/aem-docs/content/en/cq/5-6-1.html。

## 从[!DNL Experience Manager]社区{#get-help-from-aem-community}获取帮助

如果您对使用Experience Manager有任何疑问，建议您[在论坛 [!DNL Experience Manager] ](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community)中联系我们经验丰富的社区专家。
