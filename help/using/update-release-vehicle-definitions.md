---
title: 更新版本发行方式定义
description: 本文详细介绍了各种类型的  [!DNL Experience Manager]  发行版本，包括完整版本、功能包和 Service Pack。
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: ce1026216ccb79a3c268b3f6b24698fa3a3388dc
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# [!DNL Experience Manager] 更新版本发行方式定义 {#update-release-vehicle-definitions}

本文档详细介绍了 [!DNL Adobe] 为其客户提供的各种类型的 [!DNL Adobe Experience Manager] 发行版本，包括完整版本、功能包和 Service Pack。

>[!NOTE]
>
>有关 [!DNL Experience Manager] 更新版本的发行计划，请参阅 [[!DNL Experience Manager]  更新版本发行路线图](update-releases-roadmap.md)

## 完整版本 {#full-release}

| 项目 | 描述 |
|-------|------|
| 定义 | <ul> <li> 按计划发行 </li> <li> 对于在发行说明中指定的特定版本支持升级路径 </li> </ul> |
| 命名 | <ul> <li> 主要版本的版本号按照公式 X+1.Y.Z 递增。 </li> <li> 次要版本的版本号按照公式 X.Y+1.Z 递增。 </li> </ul> 其中 X 是主版本号，Y 是次版本号，Z 是修补程序版本号。 |
| 包含项 | <ul> <li> 新增功能 </li> <li>  改进功能 </li> <li>  错误修复 </li> </ul> |
| 文档 | <ul> <li> 发行说明可在文档门户中找到 </li> <li> 有关新增功能、改进功能和错误修复的文档可在文档门户中找到 </li> </ul> |
| 发行频率 | 每年 |
| 可用性和安装 | <ul> <li> 以独立产品安装程序的形式提供 </li> <li>  可从授权网站和 Managed Services 中获取 </li> <li> 授权网站可能会要求进行内容存储库迁移 </li> </ul> |
| 测试级别 | 已由 QA 全面验证 |

## Service Pack {#service-pack}

| 项目 | 描述 |
|-----|-----|
| 定义 | <ul> <li> 按计划发行 </li> <li> 当前无法回滚 </li> </ul> |
| 命名 | <ul> <li> 修补程序版本号是一个个位数 </li> <li> 安装后，将按照公式 X.Y.Z.SPx 递增安装的修补程序版本号位数 </li> </ul> 其中 X 是主版本号，Y 是次版本号，Z 是修补程序版本号。x 是 Service Pack 版本号。 |
| 包含项 | <ul> <li> 新增功能</li> <li>  改进功能 </li> <li> 错误修复 </li> <li> Common Interest 功能包（如果有） </li> </ul> |
| 文档 | <ul> <li> 发行说明可在文档门户中找到 </li> <li> 有关新增功能、改进功能和错误修复的文档可在文档门户中找到 </li> </ul> |
| 发行频率 | 每季度 |
| 可用性和安装 | <ul> <li> 以包形式提供 </li> <li> 可在 Software Distribution 上获取</li> <li>  要求现有安装正常运行 </li> </ul> |
| 测试级别 | <ul> <li> 所有修复均已通过 QA 验证 </li> <li>  自动运行全面的包健全性测试 </li> </ul> |

## 累积修订包  {#cumulative-fix-pack-aem}

| 项目 | 描述 |
|-----|-----|
| 定义 | <ul> <li> 用于发布修补程序的统一交付模式 </li> <li> 包含各个组件的内容包的汇总内容包 </li> <li>  CFP 是修补程序的汇总包，其中不包含任何功能改进。  </li> </ul> |
| 命名 | X.Y.Z.CFPx  <br> 其中 X 是主版本号，Y 是次版本号，Z 是修补程序版本号。x 是累积 Service Pack 版本号。 |
| 包含项 | CFP 是指累积修补程序包，其中包含所有组件在指定日期之前所具有的修补程序。例如，如果客户应用 CFP3，则 CFP3 = CFP1 + CFP2。 |
| 文档 | 发行说明可在文档门户中找到 |
| 发行频率 | 每季度 |
| 可用性和安装 | <ul> <li> 以包形式提供 </li> <li>  可在 Software Distribution 上获取 </li> <li>  取决于发布的最新 Service Pack </li> <li>  CFP 是独立的。客户无需担心要查找/解决依赖项。CFP 应安装在最新发布的 Service Pack 上。 </li> <li>  CFP 可以作为单个包进行安装，以改善客户体验。  </li> </ul> |
| 测试级别 | 在集成级别已通过 QA 验证并已进行回归测试 |

## 叠加 {#overlay}

| 项目 | 详细信息 |
|-------|--------|
| 命名 | 覆盖-&lt;票证 ID> |
| 包含项 | 对 JS 或 JSP 文件的错误修复 |
| 文档 | 无 |
| 发行频率 | 按需 |
| 可用性和安装 | <ul> <li> 由 [!DNL Experience Manager] 客户关怀部门以包形式提供  </li> <li> 不一定包含在 Service Pack 或完整版本中 </li> </ul> |
| 测试级别 | 已由客户关怀部门验证 |

## 功能包 {#feature-pack}

| 项目 | 详细信息 |
|--------|-----|
| 定义 | <ul> <li>功能包是附加功能，通过 Service Pack 提供。如果某个 [!DNL Experience Manager] 版本已发布其最后一版 Service Pack，则 Adobe 将来不会为该版本提供任何功能包。 </li> <li> 功能包中包含产品增强功能，这些功能计划在后续产品版本中推出，但由 [!DNL Adobe's] 产品管理部门决定提前发行。</li> <li>  这些功能始终会合并到下一个主要版本中，然后移植到客户所需的 [!DNL Experience Manager] 版本 </li> <li>  Common Interest 和 GA 功能包将合并到下一版 Service Pack 中  </li> </ul> |
| 命名 | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| 包含项 | <ul> <li> 新增功能 </li> <li> 改进功能 </li> <li> 错误修复（增量产品更新） </li> </ul> |
| 文档 | 相关文档位于 adobe.com 上。 |
| 发行频率 | 因产品市场区域而异 |
| 可用性和安装 | <ul> <li>通过 Service Pack 提供 </li> <li> 可在 Software Distribution 上获取。客户通过 Software Distribution 接受 [!DNL Adobe's] 条款和条件。 </li> </ul> |
| 测试级别 | General Availability 功能包已通过 QA 验证。 |

* 1：不以个别修补程序的形式提供 Oak 修补程序。但是，它们包含在后续的累积 Oak 修补程序中。如有必要，可以提供基于最新 COFP 的诊断版本。但前提是客户必须运行最新的 COFP。诊断版本仅提供与修补程序相同级别的质量保证。因此，诊断版本无法提供像累积修订包、服务包或产品版本那样多的质量保证。最终修补程序将随下一个 CFP 一起提供。
