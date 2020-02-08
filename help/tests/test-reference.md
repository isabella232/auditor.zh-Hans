---
description: 此参考提供了有关Auditor执行的测试的更多信息。
seo-description: 此参考提供了有关Auditor执行的测试的更多信息。
seo-title: 测试参考
title: 测试参考
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
translation-type: tm+mt
source-git-commit: 0c116f699b697ad010ee074ac67159a49ec09ccd

---


# 测试参考{#test-reference}

此参考提供了有关Auditor执行的测试的更多信息。

**当前测试标准版本：** 1.0.5

每个测试都有权重。 您的测试得分等于分配的权重。 如果通过5个重量的测试，您将获得5个点。

* 0:提醒您应该注意的问题，但这不会影响您的得分。
* 1:建议进行优化。 不影响数据准确性。
* 2:未通过此测试意味着您将无法访问Experience cloud中的最新功能和修复。
* 3:测试效率以及实施是否遵循最佳实践。
* 4:失败意味着您可能正在收集不可靠的数据。
* 5:失败意味着您可能会看到数据丢失。

测试通过／失败。 他们测试是否符合测试条件，因此对于部分符合性没有部分得分。 例如，如果测试检查Adobe解决方案的最新版本，而您只落后于一个版本，则获得的分数与您先前的五个版本相同。 最新版本包括性能改进和错误修复，因此建议在最新版本上安装。

**强烈建议**&#x200B;修复任何 4 级或 5 级结果。

**建议**&#x200B;修复任何 1 级到 3 级的结果。

## Auditor对哪些Adobe技术进行评级？ {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Advertising Cloud Search
* Analytics
* DTM
* Experience Cloud ID服务（以前称为Marketing Cloud ID服务）
* Target

以下Adobe解决方案当前未包含在测试框架中。 对这些解决方案的支持计划在将来进行更新。

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Launch

## 测试类别 {#section-630181db21ef4eec9ce6a13a0482bb55}

此测试参考将测试分为以下类别：
