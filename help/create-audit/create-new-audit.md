---
description: 在Adobe Experience Platform审计师中创建新审计
seo-description: 在Adobe Experience Platform审计师中创建新审计
seo-title: 在Adobe Experience Platform审计师中创建新审计
title: 在Adobe Experience Platform审计师中创建新审计
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 73%

---


# 新建审核{#create-a-new-audit}

>[!NOTE]
>
>对于用户，限制每次只能运行一项审核。如果您尝试运行的审核与正在运行的审核设置相同，则会发生错误。如果要取消当前正在运行的审核以便新建一个审核，则可以使用错误消息中的链接。

如果需要，请使用页面底部的链接，以访问功能齐全且免费的 ObservePoint 试用帐户。

1. 从 Auditor 列表中，单击 **[!UICONTROL New Audit]**（新建审核）。

   将会打开 [!DNL New Audit] 屏幕。

   ![](assets/config.png)

1. （必须）命名审核。

   名称最多可包含 250 个字符。
1. （必须）指定起始 URL。

   指定起始 URL 时，必须填写协议。起始 URL 是审核开始爬网的页面。开始后，Adobe Experience Platform审计师会按照从起始URL开始的链接，搜索最多500页。 有关更多信息，请参阅[包含和排除过滤器](../create-audit/filters.md)。起始 URL 最多可包含 250 个字符。

   >[!NOTE]
   >
   >在某些情况下，完成 500 个页面的扫描可能需要长达 48 小时。

1. 指定一个或多个电子邮件地址，用于接收关于审核的通知。

   您可以指定多个电子邮件地址，每个邮件地址之间用逗号分隔。默认情况下，会通知请求者。将实时验证电子邮件地址。如果输入的地址无效，屏幕上则会显示相关通知。

   每个电子邮件地址的长度不超过 250 个字符，包括域名后辍在内（例如 .com）。

1. Specify [!UICONTROL Include Filters].

   此字段可包含精确的 URL、部分 URL或正则表达式。使用此字段可指定您希望每个 URL 满足的条件。Any crawled URLs that do not match the [!UICONTROL Include Filter] criteria are not included in the audit results.

   您可以输入希望审核扫描的目录。或者，您可以执行跨域或自我分派审核，其中，您需要在一个域开始审核，并在另一个域结束审核。为此，请键入要遍历的域；对于复杂的 URL 模式，请使用正则表达式。

   >[!NOTE]
   >
   >如果您的过滤器中包含页面，但它未连接到您的起始URL，或者平台审计器在到达该页面前扫描了500页，则不会扫描该页面，测试结果也不会包含该页面。

   “Include Filter”（包含过滤器）限制每行最多为 1,000 个字符。

   有关更多信息，请参阅[包含列表](../create-audit/filters.md)。
1. 指定“Exclude Filter”（排除过滤器）。

   The [!UICONTROL Exclude List] prevents URLs from being audited. Use exact URLs, partial URLs, or regular expressions, just as you would in the [!UICONTROL Include List].

   一种常见做法是，如果审核涉及用户会话，则排除注销链接（例如：`/logout` 表示包含字符串 `/logout` 的任意 URL)。

   “Exclude Filter”（排除过滤器）限制每行最多为 1,000 个字符。

   有关更多信息，请参阅[排除列表](../create-audit/filters.md)。
1. （可选）如果需要，您可以测试包含和排除过滤器，并测试 URL。

   输入过滤器和 URL，然后单击 **[!UICONTROL Apply]**（应用）以运行测试。

   ![](assets/test-advanced-filters.png)

1. 单击 **[!UICONTROL Run Report]**（运行报告）。
