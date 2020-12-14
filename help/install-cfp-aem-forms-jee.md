---
title: 在AEM FormsJEE上安装累积修复包
description: 在AEM FormsJEE上安装和配置累积修补程序包(CFP)的步骤摘要
contentOwner: AK
translation-type: tm+mt
source-git-commit: 050be3e2fc20242d222344bc9202752eda336b2e
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 1%

---


# 在AEM[!DNL  Forms] JEE{#installing-cumulative-fix-packs-on-aem-forms-jee}上安装累积修复包

## 在AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}上安装CFP

按照指定的顺序，执行以下步骤在AEM 6.3 [!DNL Forms JEE]上安装累积修补程序包。

1. 联系[Adobe支持](https://www.adobe.com/account/sign-in.supportportal.html)以获取CFP的AEM 6.3 [!DNL Forms JEE]安装程序。
1. 运行CFP安装程序并按照[安装和配置AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee)中的说明配置AEM [!DNL Forms JEE]。
1. 安装最新的AEM CFP [6.3.3.x](release-notes-aem-6-3-cumulative-fix-pack.md)
1. 安装AEM CFP [ 6.3.3.x](aem-forms-releases.md)的[!DNL Forms] Add-on软件包

### 安装AEM [!DNL Forms JEE]捆绑包{#install-aem-forms-jee-bundles-package}

[[!DNL  Forms JEE] AEMpackage](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq630/cumulativefixpack/fd/AEM-FORMS-6.3-CFP1-JEE-PKG) (aemfd-jee-bundles-package-6.3CFP1;版本1.0.2)为AEM上 [!DNL Forms] 的用户提供 [!DNL Forms JEE] 的权限和功能与AEM相同 [!DNL Forms OSGi]。检查包管理器中已安装的包，如果尚未安装，请安装该包。

### CQ-4208044的附加说明{#additional-instructions-for-cq}

如果将AEM 6.3 [!DNL Forms JEE]服务器与Oracle数据库一起使用，请在部署CFP1后（即在运行Configuration Manager后）配置以下设置。 运行企业域同步时，需要此设置才能同步用户、组和组成员。 请参见[AEM 6.3发行说明](release-notes-aem-6-3-cumulative-fix-pack.md#main-pars-header-853219205)中的问题CQ-4208044。

1. 登录&#x200B;**Admin** UI。
1. 导航到&#x200B;**[!UICONTROL 设置]** > **[!UICONTROL 用户管理]** > **[!UICONTROL 配置]** > **[!UICONTROL 导入和导出配置文件]**
1. 导出config.xml文件。
1. 在&#x200B;*config.xml*&#x200B;中修改域配置下的“ `groupMemberDBQueryBatchSize`”条目。 示例条目：

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot; />

1. 再次导入修改后的文件，然后重新运行同步。

## 在AEM 6.2 [!DNL  Forms JEE] {#install-cfp-on-aem-62-forms-jee}上安装CFP

按照指定的顺序，执行以下步骤在AEM 6.2 [!DNL Forms JEE]上安装累积修复包。

>[!NOTE]
>
>如果您在AEM 6.2 [!DNL Forms OSGi]上，请按照[AEM 6.2 CFP发行说明中的安装说明操作。](release-notes-aem-6-2-cumulative-fix-pack.md)

1. 联系[Adobe支持](https://www.adobe.com/account/sign-in.supportportal.html)以获取CFP的AEM 6.2 [!DNL Forms JEE]安装程序。
1. 运行CFP安装程序并按照[安装和配置AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee)中的说明配置AEM [!DNL Forms JEE]。
1. 安装[AEM Hotfix 12785版本7.0](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/hotfix/cq-6.2.0-hotfix-12785)。
1. 安装[AEM 6.2 Service Pack 1](https://docs.adobe.com/docs/en/aem/6-2/release-notes/sp1.html)。
1. 安装最新的[AEM 6.2 Service Pack1 CFP](release-notes-aem-6-2-cumulative-fix-pack.md)。
1. 安装[AEM 6.2 Service Pack 1 CFP](aem-forms-releases.md)的[!DNL Forms] Add-on软件包。

### 安装AEM [!DNL Forms JEE]捆绑包{#install-aem-forms-jee-bundles-package-1}

[AEM Forms](https://www.adobeaemcloud.com/content/packageshare/tools/login.html?resource=%2Fcontent%2Fmarketplace%2FmarketplaceProxy.html%3FpackagePath%3D%2Fcontent%2Fcompanies%2Fpublic%2Fadobe%2Fpackages%2Fcq620%2Fcumulativefixpack%2Ffd%2FAEM-FORMS-6.2-SP1-CFP5-JEE-PKG&amp;$$login$$=%24%24login%24%24) JEE包(aemfd-jee-bundles-package-6.2CFP5;版本1.0.2)为AEM上 [!DNL Forms] 的用户提供 [!DNL Forms JEE] 的权限和功能与AEM相同 [!DNL Forms OSGi]。检查包管理器中已安装的包，如果尚未安装，请安装该包。

### 配置组件级操作的超时(NPR-16774){#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>在发布AEM 6.2 CFP4后，您可以按照以下说明配置DSC操作的超时，以防由于升级过程中超时而出现问题。 (请参见[AEM 6.2 CFP4发行说明](release-notes-aem-6-2-cumulative-fix-pack.md)中的NPR-16774)。

DSC部署可能会因此失败而需要一个可变时间。 要更改DSC操作(如安装、加载、开始和停止)的超时，需要使用带-D选项的JVM参数设置`adobe.component.registry.timeout`。

以秒为键指定值。 例如：`-Dadobe.component.registry.timeout=300`

您还可以使用以下三个属性更改组件级别的超时：

1. `adobe.all-component.timeout`:覆盖产品所有服务的超时。
1. `adobe.<serviceName>.timeout`:只覆盖键中所述服务(&lt;servicename>)的超时。如果设置了服务级别的值，则使用此命令只会覆盖指定服务的超时值（如果它设置在应用程序级别）。
1. `adobe.<serviceName>.<operationName>.timeout`:它只覆盖特定服务操作的超时(&lt;servicename>.&lt;operationname>)。如果该值设置在“操作”级别，则使用此命令只会覆盖指定服务的超时值（如果它设置在“应用程序”级别或“服务”级别）。

**示例：**

使用以下命令设置组件级的超时：

1. 将所有服务操作的超时设置为600秒：

   设置 &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`&quot;

1. 要将`DesigntimeService`操作值超时设置为500秒，请使用：

   设置 &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`&quot;

1. 要将`DesigntimeService's previewLCA`操作值超时设置为700秒，请使用：

   设置 `"JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`&quot;

1. 要将`DSC operations`（如加载、安装等）设置为600秒，请使用：

   设置 &quot; `JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`&quot;

## 安装和配置AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. 备份/deploy文件夹。 如果您决定卸载快速修复，则此操作是必需的。
1. 停止应用程序服务器。
1. 将修补程序安装程序存档文件解压到硬盘。
1. 在根据您所使用的操作系统命名的目录中：

   **Windows**

   导览至硬盘上的安装介质或文件夹中的相应目录，您在该目录下复制了安装程序：

   * （Windows 32位）:Disk1\InstData\Windows\VM
   * （Windows 64位）:Disk1\InstData\Windows_64bit\VM

   然后，多次单击名为：

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe(**AEM [!DNL Forms] 6.1**)

   **Linux、Solaris、AIX**

   导航到相应的目录：

   * (Linux):Disk1/InstData/Linux/NoVM
   * (Solaris):Disk1/InstData/Solaris/ NoVM
   * (AIX):Disk1/InstData/AIX/VM

   在命令提示符下，键入：

   * 。/aemforms63_cfp_install.bin(**AEM [!DNL Forms] 6.3**)
   * 。/aemforms62_cfp_install.bin(**AEM [!DNL Forms] 6.2**)
   * 。/aemforms61_cfp_install.bin(**AEM [!DNL Forms] 6.1**)

   这将启动一个安装向导，指导您完成安装。

1. 在“简介”面板上，单击&#x200B;**[!UICONTROL 下一步]**。
1. 在“选择安装文件夹”屏幕上，验证显示的默认位置是否适用于您的现有安装，或单击&#x200B;**[!UICONTROL 浏览]**&#x200B;选择当前安装AEM [!DNL Forms]的备用文件夹，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 阅读“快速修复补丁程序摘要”信息，然后单击&#x200B;**[!UICONTROL 下一步]**。
1. 阅读“预安装摘要”信息，然后单击“安装&#x200B;****”。
1. 安装完成后，单击&#x200B;**[!UICONTROL Next]**&#x200B;将快速修复更新应用到已安装的文件。
1. 默认情况下，开始配置管理器复选框处于选中状态。 单击&#x200B;**[!UICONTROL 完成]**&#x200B;以运行Configuration Manager。

   要稍后运行Configuration Manager，请取消选择&#x200B;**[!UICONTROL 开始配置管理器]**&#x200B;选项，然后单击&#x200B;**[!UICONTROL 完成]**。 您以后可以使用&#x200B;*`[AEM_forms_root]`/configurationManager/bin*&#x200B;目录中的相应脚本开始Configuration Manager。

1. 根据您的应用程序服务器，选择以下文档之一，然后按照&#x200B;*配置和部署AEM[!DNL Forms]*&#x200B;部分中的说明操作。

   对于AEM [!DNL Forms] 6.3，请参阅：

   * [安装和部 [!DNL Forms] 署AEMfor JBoss](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-jboss.pdf)
   * [安装和部 [!DNL Forms] 署AEMfor WebSphere](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
   * [安装和部 [!DNL Forms] 署AEMfor WebLogic](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-weblogic.pdf)

   对于AEM [!DNL Forms] 6.2，请参阅：

   * [安装和部 [!DNL Forms] 署AEMfor JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_62)
   * [安装和部 [!DNL Forms] 署AEMfor WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_62)
   * [安装和部 [!DNL Forms] 署AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_62)

   有关AEM Forms6.1，请参阅：

   * [安装和部 [!DNL Forms] 署AEMfor JBoss](http://www.adobe.com/go/learn_aemforms_installJBoss_61)
   * [安装和部 [!DNL Forms] 署AEMfor WebSphere](http://www.adobe.com/go/learn_aemforms_installWebSphere_61)
   * [安装和部 [!DNL Forms] 署AEMfor WebLogic](http://www.adobe.com/go/learn_aemforms_installWebLogic_61)



1. 重新启动AEM [!DNL Forms] JEE服务器。
