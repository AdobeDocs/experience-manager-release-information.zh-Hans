---
title: 在 AEM Forms JEE 上安装累积修补程序包
description: 在 AEM Forms JEE 上安装和配置累积修补程序包 (CFP) 的步骤概述
contentOwner: AK
translation-type: ht
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: ht
source-wordcount: '1102'
ht-degree: 100%

---


# 在 AEM [!DNL  Forms] JEE 上安装累积修补程序包{#installing-cumulative-fix-packs-on-aem-forms-jee}

## 在 AEM 6.3 [!DNL Forms JEE] 上安装 CFP {#install-cfp-forms-6-3}

按照指定的顺序，执行以下步骤，在 AEM 6.3 [!DNL Forms JEE] 上安装累积修补程序包。

1. 联系 [Adobe 支持人员](https://www.adobe.com/cn/account/sign-in.supportportal.html)以获取 AEM 6.3 [!DNL Forms JEE] CFP 安装程序。
1. 运行 CFP 安装程序，并按照[安装和配置 AEM  [!DNL Forms JEE]](#install-and-configure-aem-forms-jee) 中的所述配置 AEM [!DNL Forms JEE]。
1. 安装最新的 AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. 安装适用于 AEM CFP [6.3.3.x](aem-forms-releases.md) 的 [!DNL Forms] 附加组件包

### 安装 AEM [!DNL Forms JEE] 包 {#install-aem-forms-jee-bundles-package}

[AEM [!DNL  Forms JEE] 包](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG)（aemfd-jee-bundles-package-6.3CFP1；版本 1.0.2）为 AEM [!DNL Forms JEE] 上的 [!DNL Forms] 用户提供了与 AEM [!DNL Forms OSGi] 上相同的权限和功能。检查包管理器中已安装的包，如果尚未安装，请安装包。

### CQ-4208044 的附加说明 {#additional-instructions-for-cq}

如果将 AEM 6.3 [!DNL Forms JEE] 服务器与 Oracle 数据库一起使用，请在部署 CFP1 后（即，在运行配置管理器后）配置以下设置。运行企业域同步时，需要此设置才能同步用户、组和组成员。请参阅 [AEM 6.3 发行说明](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205)中的问题 CQ-4208044。

1. 登录 **Admin** 用户界面。
1. 导航到 **[!UICONTROL Settings]** > **[!UICONTROL User Management]** > **[!UICONTROL Configuration]** > **[!UICONTROL Import and Export Configuration File]**。
1. 导出 config.xml 文件。
1. 在 *config.xml* 中，修改域配置下的“`groupMemberDBQueryBatchSize`”条目。示例条目：

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. 再次导入修改后的文件，然后重新运行同步。

## 在 AEM 6.2 [!DNL  Forms JEE] 上安装 CFP {#install-cfp-on-aem-62-forms-jee}

按照指定的顺序，执行以下步骤，在 AEM 6.2 [!DNL Forms JEE] 上安装累积修补程序包。

>[!NOTE]
>
>如果您在 AEM 6.2 [!DNL Forms OSGi] 上，请按照 [AEM 6.2 CFP 发行说明](release-notes-aem-6-2-cumulative-fix-pack.md)中的安装说明操作。

1. 联系 [Adobe 支持人员](https://www.adobe.com/cn/account/sign-in.supportportal.html)以获取 AEM 6.2 [!DNL Forms JEE] CFP 安装程序。
1. 运行 CFP 安装程序，并按照[安装和配置 AEM  [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee) 中的所述配置 AEM [!DNL Forms JEE]。
1. 安装 [AEM 修补程序 12785 版本 7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785)。
1. 安装 [AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。
1. 安装最新的 [AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md)。
1. 安装适用于 [AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md) 的 [!DNL Forms] 附加组件包。

### 安装 AEM [!DNL Forms JEE] 包 {#install-aem-forms-jee-bundles-package-1}

[AEM Forms JEE 包](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24)（aemfd-jee-bundles-package-6.2CFP5；版本 1.0.2）为 AEM [!DNL Forms JEE] 上的 [!DNL Forms] 用户提供了与 AEM [!DNL Forms OSGi] 上相同的权限和功能。检查包管理器中已安装的包，如果尚未安装，请安装包。

### 为组件级别的操作配置超时 (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>安装 AEM 6.2 CFP4 之后，您可以按照以下说明为 DSC 操作配置超时，以防由于升级过程中超时而出现问题。（请参阅 [AEM 6.2 CFP4 发行说明](release-notes-aem-6-2-cumulative-fix-pack.md)中的 NPR-16774）。

DSC 部署需要的时间是可变的，因此，部署可能会失败。要更改 DSC 操作（例如安装、加载、开始和停止）的超时，您需要使用带 -D 选项的 JVM 参数来设置 `adobe.component.registry.timeout`。

指定键值（以秒为单位）。例如：`-Dadobe.component.registry.timeout=300`

您还可以使用以下三个属性更改组件级别的超时：

1. `adobe.all-component.timeout`：覆盖产品所有服务的超时。
1. `adobe.<serviceName>.timeout`：只覆盖键中所述服务 (&lt;serviceName>) 的超时。如果在服务级别设置了该值，则使用此命令只会覆盖指定服务的超时值（如果在应用程序级别设置）。
1. `adobe.<serviceName>.<operationName>.timeout`：只覆盖键中所述的特定服务的操作 (&lt;serviceName>.&lt;operationName>) 的超时。如果在操作级别设置了该值，则使用此命令只会覆盖指定服务的超时值（如果在应用程序级别或服务级别设置）。

**示例：**

使用以下命令设置组件级别的超时：

1. 要将所有服务操作的超时值设置为 600 秒，请使用：

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. 要将 `DesigntimeService` 操作的超时值设置为 500 秒，请使用：

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. 要将 `DesigntimeService's previewLCA` 操作的超时值设置为 700 秒，请使用：

   set `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. 要将 `DSC operations`（例如加载、安装等）设置为 600 秒，请使用：

   set &quot;`JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## 安装和配置 AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. 备份 /deploy 文件夹。如果您决定卸载快速修补程序，则必须执行此操作。
1. 停止应用程序服务器。
1. 将补丁安装程序存档文件提取到硬盘驱动器。
1. 在根据您所使用的操作系统命名的目录中：

   **Windows**

   导航到安装介质上的相应目录，或硬盘上您在其中复制了安装程序的文件夹：

   * （Windows 32 位）：Disk1\InstData\Windows\VM
   * （Windows 64 位）：Disk1\InstData\Windows_64bit\VM

   然后，双击以下名称的文件：

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux、Solaris、AIX**

   导航到相应的目录：

   * (Linux)：Disk1/InstData/Linux/ NoVM
   * (Solaris)：Disk1/InstData/Solaris/ NoVM
   * (AIX)：Disk1/InstData/AIX/VM

   在命令提示符下，键入：

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   这会启动安装向导，引导您完成安装。

1. 在“Introduction”面板上，单击 **[!UICONTROL Next]**。
1. 在“Choose Install Folder”屏幕上，验证显示的默认位置对于您的现有安装是否正确，或者单击 **[!UICONTROL Browse]** 以选择当前安装 AEM [!DNL Forms] 的替代文件夹，然后单击 **[!UICONTROL Next]**。
1. 阅读“Quick Fix Patch Summary”信息，然后单击 **[!UICONTROL Next]**。
1. 阅读“Pre-Installation Summary”信息，然后单击 **[!UICONTROL Install]**。
1. 安装完成后，单击 **[!UICONTROL Next]** 以将快速修补程序更新应用到已安装的文件。
1. 默认情况下，“Start Configuration Manager”复选框处于选中状态。单击 **[!UICONTROL Done]** 以运行配置管理器。

   要稍后运行配置管理器，请先取消选择 **[!UICONTROL Start Configuration Manager]** 选项，然后再单击 **[!UICONTROL Done]**。您稍后可以使用 *`[AEM_forms_root]`/configurationManager/bin* 目录中的相应脚本来启动配置管理器。

1. 根据您的应用程序服务器，选择以下文档之一，然后按照&#x200B;*配置和部署 AEM[!DNL Forms]* 部分中的说明操作。

   对于 AEM [!DNL Forms] 6.3，请参阅：

   * [安装和部署 AEM  [!DNL Forms]  for JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [安装和部署 AEM  [!DNL Forms]  for WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [安装和部署 AEM  [!DNL Forms]  for WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   对于 AEM [!DNL Forms] 6.2，请参阅：

   * [安装和部署 AEM  [!DNL Forms]  for JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62_cn)
   * [安装和部署 AEM  [!DNL Forms]  for WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62_cn)
   * [安装和部署 AEM  [!DNL Forms]  for WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62_cn)

   对于 AEM Forms 6.1，请参阅：

   * [安装和部署 AEM  [!DNL Forms]  for JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61_cn)
   * [安装和部署 AEM  [!DNL Forms]  for WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61_cn)
   * [安装和部署 AEM  [!DNL Forms]  for WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61_cn)



1. 重新启动 AEM [!DNL Forms] JEE 服务器。
