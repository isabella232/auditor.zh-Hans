---
description: 此参考提供了有关 Auditor 执行的测试的更多信息。
seo-description: 此参考提供了有关 Auditor 执行的测试的更多信息。
seo-title: 测试参考
title: 测试参考
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: ht
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# 测试参考{#test-reference}

此参考提供了有关 Auditor 执行的测试的更多信息。

**当前测试评分标准版本：** 1.0.5

每个测试都要经过加权处理。您的测试得分等于分配的权重。如果您通过了一个权重为 5 的测试，那么您将获得 5 分。

* 0：通过警报，提醒您应该注意的问题，但是不影响您的得分。
* 1：建议进行优化。不影响数据准确性。
* 2：如果未通过这个测试，则意味着您将不能访问 Experience Cloud 中的最新功能和修复。
* 3：测试效能并判断实施期间是否遵循了最佳做法。
* 4：失败，这意味着您可能正在收集不可靠的数据。
* 5：失败，这意味着您可能会遭遇数据丢失。

测试通过/失败。检测是否符合测试条件，不存在针对部分合规情况的分量得分。例如，在检测是否含有最新版本的 Adobe 解决方案时，如果您使用的版本与最新版本之间只相差一个版本，那么这种情况下您的得分与相关五个版本的得分是一样的。最新版本包括性能改进和错误修复，因此建议安装最新版本。

**强烈建议**&#x200B;修复任何 4 级或 5 级结果。

**建议**&#x200B;修复任何 1 级到 3 级的结果。

## Auditor 对哪些 Adobe 技术进行评分？{#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID 服务（以前称为 Marketing Cloud ID 服务）
* Target

目前，以下 Adobe 解决方案未包含在测试评分标准中。计划在未来的更新中，支持这些解决方案。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## 测试类别 {#section-630181db21ef4eec9ce6a13a0482bb55}

此测试参考把测试分为以下类别：
