---
description: 有关 Adobe Experience Platform Auditor 的常见问题和解答
seo-description: 有关 Adobe Experience Platform Auditor 的常见问题和解答
seo-title: Adobe Experience Platform Auditor 常见问题解答
title: Adobe Experience Platform Auditor 常见问题解答
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 71%

---


# Adobe Experience Platform Auditor 常见问题解答{#auditor-faq}

本文包含有关 Adobe Experience Platform Auditor 的常见问题解答。

* [什么是Adobe Experience Platform审计师？](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [我的公司是否有资格使用Platform Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Platform Auditor对哪些Adobe技术进行评级？](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [我可以运行多少次审核？](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [审核会爬网哪些内容？](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [审核需要花费多长时间？](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [报表会提供哪些信息？](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [这些信息的可操作性如何？](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Platform Auditor能否审核非Adobe技术？](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [我是否可以批准我的 IP 地址，以允许扫描页面...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Platform Auditor是否使用与Observepoint相同的IP范围？](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## 什么是Adobe Experience Platform审计师？ {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Platform Auditor是Adobe Experience Cloud的一项服务，它与ObservePoint共同开发，后者是验证数字实施方面的专家。

借助Platform Auditor，客户一次最多可扫描500个网页并收到报告，其中显示如何改进其Adobe Experience Cloud实施，以便获得其Adobe投资的全部价值。

## Am I eligible to use Platform Auditor? {#section-f90094050d1e44929066a942833435cf}

所有Adobe Experience Cloud客户组织均可免费访问Platform Auditor（自2018年5月1日起）。 每位用户必须同意 Adobe/ObservePoint 在 Adobe Experience Cloud UI 中的使用条款，然后才能访问 Auditor 的功能。若要选择退出条款，请联系您的客户经理。

## How do I access Platform Auditor? {#section-531ff85f94384831a89cbb4109549daf}

After logging in at [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), you can find Platform Auditor by clicking on **[!UICONTROL Activation]** in the top navigation. 您也可以直接转到 [https://auditor.adobe.com](https://auditor.adobe.com)。

## Which Adobe technologies does Platform Auditor grade? {#section-52833b71c05448aaae508e6070a387f5}

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
* Adobe Experience Platform Launch

## 我可以运行多少次审核？{#section-caac1e50ce1249aeba76308f3ef03fa0}

您可以不限次数地运行审核。对于用户，限制每次只能运行一项审核。如果您尝试运行的审核与正在运行的审核设置相同，则会发生错误。

## 审核会爬网哪些内容？{#section-6d068ed69ece4a1bb6d0c34454550c45}

目前，ObservePoint 技术可以爬网在文档链接中找到的 URL。对于按钮、分页小组件，以及其他此类页面元素中的链接，则不进行爬网。

## How do I suggest new criteria for Platform Auditor tests? {#section-926e6ef9225b4f0bb19c2927d634cd77}

You can submit test suggestions via the Platform Auditor Community by clicking **[!UICONTROL Share Feedback]** on this page: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## 审核需要花费多长时间？{#section-5086ae27ef1f4671a9d951348654633a}

完成审核的时间取决于多种因素，其中包括：

* 页面加载时间

   ObservePoint 引擎会在浏览器中加载审核的每个页面。加载页面的速度越快，完成审核的时间就会越早。
* 同时连接的数目

   Platform Auditor使用单一连接访问每个页面。 拥有完整访问权限的 ObservePoint 帐户一次最多可使用 10 个引擎。
* 网络静默时间

   加载每个页面后，审核会等待 7 秒钟的网络静默时间，然后再继续加载下一个页面。如果在页面加载后，页面发送了大量网络请求，则等待将在 60 秒后超时。
* 页面重试次数

   如果找不到页面或标记，审核则会存储相关 URL，并稍后于审核期间返回到该页面或标记。审核期间，访问页面的次数可多达三次，以确保错误不是因临时问题而引起。
* 处理时间

   运行审核后，收集的所有数据都将依据规则进行处理和过滤。尽管处理过程不像扫描那样需要花费大量时间，但是这个过程非常重要。

>[!NOTE]
>
>Platform Auditor一次只运行一次扫描。 拥有完整权限的 ObservePoint 帐户可以连续运行多项审核。

## 报表会提供哪些信息？{#section-752d6b82f6744a3182c4ce16ea6b5d3f}

每次扫描都会生成一份报表，其中显示了已扫描的 URL、在相关网页上发现的问题，以及有关如何更正发现的问题的建议。

扫描结果分为三类：

* 配置
* 标记一致性
* 标记存在

除了这三个类别之外，报表还会提供警报，其中包含了您应该注意但不一定需要立即采取措施的信息。

这些类别中的推荐，随后又将划分为三个其他的类别：

* 强烈建议
* 建议
* 已通过

## 这些信息的可操作性如何？{#section-9308c1ea882048b781087ae6d2eee9f0}

通过平台审计师提供的所有建议旨在帮助您采取行动解决实施Adobe Experience Cloud解决方案(如DTM或目标)时遇到的问题。 为此，平台审计员团队做了大量工作，以提供非常精细的说明，说明需要在哪里做什么。 您可以导出包含所有扫描的 URL 和所有测试结果在内的电子表格，以便轻松实现问题区域的精准定位。以下是 DTM 实施的一个推荐示例：

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>最后置入 pageBottom 回调函数</b> </p> <p>正确实施 DTM 必然需要 _satellite.pageBottom() 函数。为了确保 DTM 正常运行，请在紧接着闭合的 &lt;/body&gt; 标记之前添加内联脚本。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Can Platform Auditor audit non-Adobe technology? {#section-f6e73c56083b4815bbf901296038bcd4}

否。但是，ObservePoint 的完整产品服务允许客户审核并监控其所有营销标记和技术。作为 Adobe 客户，您有权访问免费的试用帐户。To access your trial account visit [ObservePoint’s Platform Auditor Page](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## 我是否可以批准我的 IP 地址，以允许扫描受登录名保护的页面？{#section-011e4f54c58140ffb93bedeb0745b6cc}

当前，若没有完整的 ObservePoint 产品服务，则不支持这项功能。

## Does Platform Auditor use the same IP ranges as ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

因为是由 ObservePoint 执行爬网，所以会使用相同的 IP 地址。

有关更多详细信息，请参阅 [ObservePoint 文档](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list)。
