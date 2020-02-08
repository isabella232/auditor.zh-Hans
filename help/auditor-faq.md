---
description: 'null'
seo-description: 'null'
seo-title: Auditor 常见问题解答
title: Auditor常见问题解答
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Auditor常见问题解答{#auditor-faq}

本文包含有关Adobe Experience Platform Auditor的常见问题解答。

* [什么是Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [我的公司是否有资格使用Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Auditor对哪些Adobe技术进行评级？](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [我可以执行多少次审计？](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [什么是审核？](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [审计需要多长时间？](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [报告中提供了哪些信息？](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [这些信息具有多大可操作性？](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [Auditor是否可以审核非Adobe技术？](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [我是否可以将我的IP地址列入白名单以允许扫描页面……](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [Auditor是否使用与Observepoint相同的IP范围？](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## 什么是Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

Auditor是Adobe Experience cloud的一项服务，它与ObservePoint共同开发，后者是验证数字实施的专家。

借助Auditor，客户一次最多可扫描500个网页并收到一份报告，其中显示了如何改进其Adobe Experience cloud实施，以便获得其Adobe投资的全部价值。

## 我是否有资格使用Auditor? {#section-f90094050d1e44929066a942833435cf}

所有Adobe Experience cloud客户组织均可免费访问Auditor（自2018年5月1日起）。 每个用户必须同意Adobe/ObservePoint在Adobe Experience Cloud UI中的使用条款，然后才能访问该功能。 要选择退出条款，请联系您的客户经理。

## 如何访问Auditor? {#section-531ff85f94384831a89cbb4109549daf}

登录 [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com) 后，您可以通过单击顶部导航中的&#x200B;**[!UICONTROL 激活]**，找到 Auditor。您也可以直接转到 [https://auditor.adobe.com](https://auditor.adobe.com)。

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

## 我可以执行多少次审计？ {#section-caac1e50ce1249aeba76308f3ef03fa0}

您可以执行的审核数量没有限制。 用户一次只能进行一次审核。 如果尝试使用与正在运行的审计相同的设置启动审计，则会发生错误。

## 什么是审核？ {#section-6d068ed69ece4a1bb6d0c34454550c45}

ObservePoint技术当前对文档链接中的URL进行爬网。 按钮、分页构件和其他此类页面元素中的链接不会进行爬网。

## 如何为Auditor测试提出新标准？ {#section-926e6ef9225b4f0bb19c2927d634cd77}

您可以单击以下页面上的&#x200B;**[!UICONTROL 共享反馈]**，通过 Auditor 社区提交测试建议：[https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## 审计需要多长时间？ {#section-5086ae27ef1f4671a9d951348654633a}

导致审计完成所需时间的因素很多，包括：

* 页面加载时间

   ObservePoint引擎在浏览器中加载审核的每页。 页面加载越快，审核完成得越快。
* 同时连接

   Adobe Auditor使用单一连接访问每个页面。 完整的ObservePoint帐户一次最多使用10个引擎。
* 网络静默

   加载每个页面后，审核会等待7秒的网络静默，然后继续到下一页。 如果页面在页面加载后发送了大量网络请求，则等待将在60秒后超时。
* 页面重试次数

   如果找不到页面或标记，则审核会存储该URL，并在审核后面返回到它。 审核将访问最多三次页面，以确保错误不是由临时问题引起的。
* 正在处理

   运行审核后，它收集的所有数据都会通过规则进行处理和过滤。 此处理时间很大，尽管它不像扫描本身那样需要花费太多时间。

>[!NOTE]
>
>Adobe Auditor一次只运行一次扫描。 完整的ObservePoint帐户可以连续运行许多审计。

## 报告中提供了哪些信息？ {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

每次扫描都会生成一个报告，其中显示已扫描的URL、在这些网页上发现的问题以及有关如何更正发现的问题的建议。

扫描结果分为三类：

* 配置
* 标签一致性
* 标记存在

除了这三个类别之外，报告还提供警报，其中包含您应该了解但不一定需要立即采取行动的信息。

这些类别中的建议随后又分为三个额外的类别：

* 强烈推荐
* 推荐
* 已通过

## 这些信息具有多大可操作性？ {#section-9308c1ea882048b781087ae6d2eee9f0}

通过Auditor提供的所有建议旨在帮助您采取行动解决Adobe Experience cloud解决方案（如DTM或Target）的实施问题。 为了促进这一点，审计员小组已开展了大量工作，就需要在哪里做什么提供非常详细的说明。 您可以导出所有扫描的URL和所有测试结果的电子表格，以便轻松找准问题区域。 以下是DTM实施的一个建议示例：

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom回调最后一个</b> </p> <p>正确的DTM实现需要_satellite.pageBottom()函数。 在结束&lt;/body&gt;标记前添加内联脚本，以确保DTM功能正确。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Auditor是否可以审核非Adobe技术？ {#section-f6e73c56083b4815bbf901296038bcd4}

否。但是，ObservePoint的完整产品允许客户审核和监控您的所有营销标签和技术。 作为Adobe客户，您有权访问免费试用帐户。 要访问试用帐户，请访 [问ObservePoint的Auditor页面](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&utm_medium=Auditor&utm_campaign=Premium)。

## 我是否可以将我的IP地址列入白名单，以允许扫描受登录名保护的页面？ {#section-011e4f54c58140ffb93bedeb0745b6cc}

当前不支持此功能，没有完整的ObservePoint产品。

## Auditor是否使用与ObservePoint相同的IP范围？ {#section-39512b156e194787981bdd572ff5b5a9}

搜索由ObservePoint执行，因此使用相同的IP地址。

有关更多 [详细信息](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) ，请参阅ObservePoint文档。
