---
title: 更新发放车辆定义
description: 本文详细介绍了各种类型的 [!DNL Experience Manager] 版本，包括完整版本、功能包和服务包。
contentOwner: AK
translation-type: tm+mt
source-git-commit: 11ff4f7d66038a80697afe5f104c560137e130f4
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 5%

---


# [!DNL Experience Manager] 更新版车辆定义  {#update-release-vehicle-definitions}

此文档包括有关[!DNL Adobe Experience Manager]版本的各种类型的详细信息，包括[!DNL Adobe]提供给其客户的完整版本、功能包和服务包。

>[!NOTE]
>
>有关[!DNL Experience Manager]更新版本的发布计划，请参阅[[!DNL Experience Manager] 更新版本路线图](update-releases-roadmap.md)

## 完整版本{#full-release}

| 项目 | 描述 |
|-------|------|
| 定义 | <ul> <li> 计划发行 </li> <li> 支持特定版本的升级路径（发行说明中定义） </li> </ul> |
| 命名 | <ul> <li> 主要版本的版本号根据公式X+1.Y.Z增加。 </li> <li> 次要版本的版本号根据公式X.Y+1.Z增加 </li> </ul> 其中X是主版本号，Y是次版本号，Z是修补程序号。 |
| 包含 | <ul> <li> 新增功能 </li> <li>  改进 </li> <li>  错误修复 </li> </ul> |
| 文档 | <ul> <li> 发行说明可在文档门户上找到 </li> <li> 有关功能、改进和错误修复的文档可在文档门户上找到 </li> </ul> |
| Cadence | 每年 |
| 可用性和安装 | <ul> <li> 以独立产品安装程序形式提供 </li> <li>  可从授权网站和Managed Services </li> <li> 授权网站可能需要内容存储库迁移 </li> </ul> |
| 测试级别 | 由QA完全验证 |

## Service Pack {#service-pack}

| 项目 | 描述 |
|-----|-----|
| 定义 | <ul> <li> 计划发行 </li> <li> 当前，无法回滚 </li> </ul> |
| 命名 | <ul> <li> 修补程序版本号是单位数 </li> <li> 安装后，将根据公式X.Y.Z.SPx增加已安装的发行版号补丁号码 </li> </ul> 其中X是主版本号，Y是次版本号，Z是修补程序号。 x是服务包编号。 |
| 包含 | <ul> <li> 新增功能</li> <li>  改进 </li> <li> 错误修复 </li> <li> Common Interest功能包（如果有） </li> </ul> |
| 文档 | <ul> <li> 文档门户上提供的发行说明 </li> <li> 文档门户上关于功能、改进和错误修复的文档 </li> </ul> |
| Cadence | 季度 |
| 可用性和安装 | <ul> <li> 以包形式交付 </li> <li> 可用于软件分发</li> <li>  需要现有功能安装 </li> </ul> |
| 测试级别 | <ul> <li> 已验证所有修复QA </li> <li>  借助自动化运行，实现整体包完整性 </li> </ul> |

## 累积修补程序包  {#cumulative-fix-pack-aem}

| 项目 | 描述 |
|-----|-----|
| 定义 | <ul> <li> 单投放释放固定 </li> <li> 包含单个组件的内容包的聚合器内容包 </li> <li>  CFP是热修复程序的翻转，但其中没有改进。  </li> </ul> |
| 命名 | X.Y.Z.CFPx <br>其中X是主版本号，Y是次版本号，Z是补丁号。 x是累积服务包编号。 |
| 包含 | CFP是包含所有组件在指定日期之前的修复的累积修补程序包。 例如，如果客户应用CFP3，则CFP3 = CFP1 + CFP2。 |
| 文档 | 文档门户上提供的发行说明 |
| Cadence | 季度 |
| 可用性和安装 | <ul> <li> 以包形式交付 </li> <li>  可用于软件分发 </li> <li>  取决于发布的最新服务包 </li> <li>  CFP是自我依赖的。 客户无需担心查找／解析依赖项。 CFP应安装在最新发布的Service Pack上。 </li> <li>  CFP可以作为单个包进行安装，这可以改善客户体验。  </li> </ul> |
| 测试级别 | 在集成级别和回归测试中验证的QA |

## 叠加 {#overlay}

| 项目 | 详细信息 |
|-------|--------|
| 命名 | overlay-&lt;票证ID> |
| 包含 | JS或JSP文件的错误修复 |
| 文档 | 无 |
| Cadence | 根据需要 |
| 可用性和安装 | <ul> <li> 由[!DNL Experience Manager]客户服务部以包送货  </li> <li> 未必包含在Service Pack或完整版本中 </li> </ul> |
| 测试级别 | 由客户关怀部门验证 |

## 功能包{#feature-pack}

| 项目 | 详细信息 |
|--------|-----|
| 定义 | <ul> <li>功能包是附加功能，通过Service Pack提供。 如果[!DNL Experience Manager]版本已发布其最后一个服务包，Adobe将来不会为它提供任何功能包。 </li> <li> FP包含产品增强功能，计划在后续产品发布中发布，但根据[!DNL Adobe's]产品管理的决定提前发布。</li> <li>  功能始终与下一个主要版本合并，然后移植到客户所需的[!DNL Experience Manager]版本 </li> <li>  Common Interest和GA功能包合并到下一个服务包中  </li> </ul> |
| 命名 | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| 包含 | <ul> <li> 新增功能 </li> <li> 改进 </li> <li> 错误修复（增量产品更新） </li> </ul> |
| 文档 | adobe.com上提供相关文档。 |
| Cadence | 因产品区域而异 |
| 可用性和安装 | <ul> <li>通过Service Pack交付 </li> <li> 适用于软件分发。 客户通过软件分发接受[!DNL Adobe's]条款和条件。 </li> </ul> |
| 测试级别 | 通用可用性功能包已通过QA验证。 |

* 1:OAK修复不是作为单独的热修复提供的。 但是，它们包含在后续的Cumulative Oak热修复中。 如有必要，可以在最新COFP上提供诊断版本。 前提是客户拥有最新的COFP运行。 诊断构建只提供与热修复相同级别的质量保证。 因此，他们提供的质量保证级别与累积修补程序包、服务包或产品版本不同。 最终的修复将与下一个CFP一起提供。
