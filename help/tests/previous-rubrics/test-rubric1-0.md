---
description: 有关 Adobe Experience Platform Auditor 测试的信息
seo-description: 有关 Adobe Experience Platform Auditor 测试的信息
seo-title: 测试评分标准 0.0.8
title: 测试评分标准 0.0.8
uuid: c62b7169-a650-4650-876f-c254eb57cb25
translation-type: ht
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: ht
source-wordcount: '2008'
ht-degree: 100%

---


# 测试评分标准 0.0.8{#test-rubric}

## 测试评分标准 0.0.8

<!-- Note to writer: Please review the tables on this page for formatting and accuracy. Compare to original file.-->

![](assets/space.png)

## 警报 {#alerts}

此参考可提供有关 Adobe Experience Platform Auditor 显示的测试警报的更多信息。

警报会显示您应该注意的问题，但是不会影响您的得分。

<table id="table_031432C9BB804A6F90E7FF572739E169"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> 测试 </th> 
    <th colname="col2" class="entry"> 标准 </th> 
    <th colname="col3" class="entry"> 推荐 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 已实施正确的转化标记</b> </p> <p>权重：0 </p> </td> 
    <td colname="col2"> <p>检查是否使用了正确的转化标记。 </p> <p> <p>警告：使用已弃用的 TubeMogul 转化标记可能会导致数据丢失。 </p> </p> </td> 
    <td colname="col3"> <p>将您的转化像素升级为新的 Advertising Cloud 纯图像转化标记。 </p> <p>使用 Adobe Experience Platform Launch 的 Advertising Cloud Extension，可以非常轻松地实现这一目标。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 纯图像标记</b> </p> <p>权重：0 </p> </td> 
    <td colname="col2"> <p>Advertising Cloud 图像像素格式，应当与以下一种推荐的格式匹配： </p> <p> 
      <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
       <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
       <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
      </ul> </p> </td> 
    <td colname="col3"> <p>将您的 Advertising Cloud 像素升级为新的 Advertising Cloud 纯图像标记，这可以确保您能够充分利用 Advertising Cloud 的完整功能。 </p> <p>使用 Platform Launch 的 Advertising Cloud Extension，可以非常轻松地实现这一目标。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 已启用区段像素 DSP 同步</b> </p> <p>权重：0 </p> </td> 
    <td colname="col2"> <p>检查 TubeMogul 区段像素是否包含 DSP 同步设置，并推荐将该设置添加到这个像素中。 </p> <p>DSP 同步设置是根据查询字符串参数的使用情况来确定的，为此 </p> <p>如果标记被触发到<span class="codeph">（"https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或<span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或<span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>并且标记包含 URL 参数 <span class="codeph">"sid="）</span> </p> <p>那么请检查 URL 参数 <span class="codeph">"cs=0"</span> 或 <span class="codeph">"cs=1"</span> 是否存在，如果不存在，推荐将 <span class="codeph">"cs=1"</span> 添加到这些像素中，以便提高受众匹配率。 </p> </td> 
    <td colname="col3"> <p> 将 URL 参数 <span class="codeph">"cs=1"</span> 添加到您的 Advertising Cloud 像素中，以便可以实现 DSP 同步，从而增加受众匹配率。 </p> <p>使用 Platform Launch 的 Advertising Cloud Extension，可以非常轻松地实现这一目标。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - 置入 pageBottom 回调函数</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他信息</a> </p> 
     <!--
       TEa9df69942f404055a64262889c8b21d3 
     --> </td> 
    <td colname="col2"> <p> Dynamic Tag Management 要求使用 <span class="codeph">_satellite.pageBottom()</span> 函数。 </p> <p>最佳做法是将该标记作为 <span class="codeph">&lt;body&gt;</span> 中的<i>最后一个</i>标记。如果在 <span class="codeph">&lt;body&gt;</span> 标记中找到了该函数，则表明存在正常运行的机率，然而由于这不是最佳的做法，所以可能会无法正确运行，或者会出现意外或不希望的结果。 </p> </td> 
    <td colname="col3"> <p>为了确保 DTM 正常运行，请在紧接着闭合的 <span class="codeph">&lt;/body&gt;</span> 标记之前添加内联脚本。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud ID 服务 - 仅使用一个 AdobeOrg</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/id-request.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p>在正常实施 MCID 的过程中，应当使用一个 AdobeOrg。 </p> </td> 
    <td colname="col3"> <p>验证这项实施中是否存在多个 AdobeOrg ID。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target - mboxDefault 中的内容</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 使用 at.js 时，mboxDefault 中应当存在相关内容。 </p> </td> 
    <td colname="col3"> <p>验证内容是否可用。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 配置 {#configuration}

此参考可提供有关 Platform Auditor 执行配置测试的更多信息。

Platform Auditor 会根据其他规则和推荐的最佳做法来评估标记。

<table id="table_A8A1FC360482447185C8460A18426638"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> 测试 </th> 
    <th colname="col2" class="entry"> 标准 </th> 
    <th colname="col3" class="entry"> 推荐 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 转化名称仅使用字母数字字符</b> </p> <p>权重：3 </p> </td> 
    <td colname="col2"> <p>除“<span class="codeph">ev_transid</span>”参数之外（<span class="codeph">ev_transid</span> 值可包含文本或数值），<span class="codeph">ev_conversion_property_name</span> 参数应当只包含数值和小数值 </p> <p>查找 <span class="codeph">everesttech.net</span> 像素，其中包含以 <span class="codeph">ev_</span> 开头的 URL 参数。 </p> <p>示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47</span> </p> </td> 
    <td colname="col3"> <p> 确保事务属性参数仅包含数值和小数值。 </p> <p> <p>警告：任何其他值类型都可能会导致数据丢失。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 转化名称使用 URL 安全字符</b> </p> <p>权重：3 </p> </td> 
    <td colname="col2"> <p> 转化属性名称不应包含 &amp; 符号或问号。 </p> <p> 示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>确保事务属性参数不包含非编码的 &amp; 符号或问号。这会破坏 URL 格式。 </p> <p> <p>警告：包含非编码的 &amp; 符号或问号的属性参数（例如：<span class="codeph">ev_formComplete?=1</span> 或 <span class="codeph">ev_formComplete&amp;Submit=1</span>），可能会导致数据丢失。 </p> </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 已正确实施事务 ID</b> </p> <p>权重：1 </p> </td> 
    <td colname="col2"> <p> 属性名称 <span class="codeph"> ev_transid=</span> 不应为空。 </p> <p>示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
    <td colname="col3"> <p>属性名称 <span class="codeph">ev_transid=</span> 不应当没有任何值 (<span class="codeph">ev_transid=</span>)。如果没有任何值，则可能会丢失事务数据。为 <span class="codeph">ev_transid=</span> 赋值，或从像素中删除此参数。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - 在 DOM 中实例化</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/en/analytics/implementation/testing-and-validation/testing-and-validation-process/impl-validation.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 未安装或无法执行 Adobe Analytics 代码。在 Web 页面上未找到 Analytics 代码时，返回值为 0。 </p> </td> 
    <td colname="col3"> <p>验证是否已在页面上实施 Analytics 标记，且没有遭到后续脚本活动的阻止。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - 实例化一次</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/home.html" format="https" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 在页面上多次检测到 Adobe Analytics 代码。在 Web 页面上未找到 Analytics 代码时，返回值为 0。 </p> </td> 
    <td colname="col3"> <p>确保页面上仅有一个 Analytics 标记。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - 最新版本</b> </p> <p>权重：3 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 您的页面没有运行最新版本的 Analytics 代码库。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。在 Web 页面上未找到 Analytics 代码时，返回值为 0。 </p> </td>       
    <td colname="col3"> <p>安装最新版本的 Analytics 代码库。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - 自托管</b> </p> <p>权重：4 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/client-side-information.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 将 DTM 库托管在 Adobe 位于 <span class="filepath">assets.adobedtm.com</span> 的 Akamai 实例上。 </p> <p> 推荐采用自托管方法来加载 DTM，因为这种方法可通过缓存控制、减少第三方脚本依赖项以及增强对发布过程的控制，更好地控制网站的性能。您可以通过自己的 Web 托管或 CDN 来托管并管理 DTM 库。 </p> </td> 
    <td colname="col3"> <p>推荐采用自托管方法在页面上加载 DTM。尽管通过 Akamai CDN 来托管 DTM 的方法适用于大多数情况，但是，自托管方法可提升页面性能。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - DOM 就绪后，异步加载第三方标记</b> </p> <p>权重：3 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/resources/load-order.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p>要在良好的用户体验与收集准确的数据之间达成一种平衡，则应当在 DOM 就绪后触发第三方标记。这将可以确保执行相关的跟踪脚本，同时又不会影响站点的正常运转。 </p> </td> 
    <td colname="col3"> <p>解决这个问题的方法是：调整 DOM 就绪后触发执行第三方像素的所有规则。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID 服务 - 最新版本</b> </p> <p>权重：2 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/tools/macid.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 您的页面没有运行最新版本的访客 ID 服务代码库 <span class="codeph">visitorAPI.js</span>。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。 </p> </td> 
    <td colname="col3"> <p>安装最新版本的访客 ID 服务代码库。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - 最新版本</b> </p> <p>权重：2 </p> <p><a href="https://marketing.adobe.com/resources/help/zh_CN/dtm/target/" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 您的页面没有运行最新版本的 Target 代码库。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。 </p> </td> 
    <td colname="col3"> <p>安装最新版本的 Target 代码库。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - mboxDefault 先于 mboxCreate </b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p><span class="codeph">mboxCreate</span> 的正确用法类似于下面的示例： </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
    <td colname="col3"> <p>调用 <span class="codeph">mboxCreate()</span> 之前，请务必包含 <span class="codeph">&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> 标记。at.js 并不会为您添加此标记。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Target - 有效的 DOCTYPE</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/client-side/functions-overview/mboxcreate-atjs.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 检测到无效的 DOCTYPE。在这种情况下，将不会触发 mbox。 </p> <p>对于 at.js，DOCTYPE 必须处于“标准”模式，否则 Target 将无法正常运作。 </p> </td> 
    <td colname="col3"> <p>更新页面上的 DOCTYPE。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 标记一致性 {#tag-consistency}

此参考可提供有关 Platform Auditor 执行标记一致性测试的更多信息。

Platform Auditor 会评估标记在各个 URL 中是否一致。

<table id="table_4F9ED873BAF741D19BFB0F297B3A1FDB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> 测试 </th> 
    <th colname="col2" class="entry"> 标准 </th> 
    <th colname="col3" class="entry"> 推荐 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - 一致的代码版本 </b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/home.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 找到多个版本的 Analytics 代码。 </p> </td> 
    <td colname="col3"> <p>将 Analytics 的所有实例替换为当前版本。 </p> </td> 
   </tr> 
  </tbody> 
</table>

![](assets/space.png)

## 标记存在 {#tag-presence}

此参考可提供有关 Platform Auditor 执行的标记存在测试的更多信息。

Platform Auditor 会评估标记是否存在，以及标记在页面代码中的位置是否正确，等等。

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
  <thead> 
   <tr> 
    <th colname="col1" class="entry"> 测试 </th> 
    <th colname="col2" class="entry"> 标准 </th> 
    <th colname="col3" class="entry"> 推荐 </th> 
   </tr>
  </thead>
  <tbody> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 代码存在</b> </p> <p>权重：5 </p> </td> 
    <td colname="col2"> <p> DOM 中不提供 Advertising Cloud 标记。 </p> </td> 
    <td colname="col3"> <p>通过 Platform Launch 的 Advertising Cloud Extension 实施 Advertising Cloud 标记。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Advertising Cloud - 已实施区段像素</b> </p> <p>权重：5 </p> </td> 
    <td colname="col2"> <p> 将您的 Advertising Cloud 区段像素升级为新的 Advertising Cloud 纯图像标记。采用已弃用的 AMO 区段标记可能会导致数据丢失。 </p> </td> 
    <td colname="col3"> <p>通过 Platform Launch 的 Advertising Cloud Extension 实施 Advertising Cloud 区段像素。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Analytics - 在 DOM 中加载</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/analytics/implementation/home.html" format="https" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 未检测到 Adobe Analytics 标记。 </p> </td> 
    <td colname="col3"> <p>安装最新版本的 Analytics。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM - 已加载库</b> </p> <p>权重：5 </p> <p>其他信息： </p> <p> 
      <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
       <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/admin/c-troubleshooting.html" format="html" scope="external">DTM 故障诊断</a> </li> 
       <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external">添加页眉和页脚代码</a> </li> 
      </ul> </p> </td> 
    <td colname="col2"> <p> 在 DOM 中未找到全局 _satellite 对象。未安装或无法执行 Dynamic Tag Management。 </p> </td> 
    <td colname="col3"> <p>验证是否已在页面上实施 DTM 库，且没有遭到后续脚本活动的阻止。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> DTM - 一个嵌入代码</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 生产站点应当只加载一个 DTM 库。 </p> </td> 
    <td colname="col3"> <p>验证页面上是否只加载了生产库。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - &lt;body&gt; 中存在 pageBottom 回调函数</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 在页面的 <span class="codeph">&lt;body&gt;</span> 标记中没有找到 <span class="codeph">_satellite.pageBottom()</span> 回调函数，它是 Dynamic Tag Management 的必需函数。 </p> <p>如果根本在页面上找不到 <span class="codeph">pageBottom</span> 调用，或者如果它位于 <span class="codeph">&lt;head&gt;</span> 标记中（或其他一些意外的位置），测试则会失败。只有在从 <span class="codeph">&lt;body&gt;</span> 标记中找到 <span class="codeph">pageBottom</span> 的情况下，测试才会通过。如果页面上根本不存在这项调用，则无法正常运转，而且另外两个 <span class="codeph">pageBottom</span> 测试也将失败。 </p> </td> 
    <td colname="col3"> <p>为了确保 DTM 正常运行，请在紧接着闭合的 <span class="codeph">&lt;/body&gt;</span> 标记之前添加内联脚本。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>DTM - 已触发 pageBottom 标记</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 未检测到 DTM <span class="codeph">pageBottom</span> 标记。 </p> <p>如果相关的调用位于 <span class="codeph">if</span> 语句中，且该语句会导致类似 <span class="codeph">if (false) {_satellite.pageBottom()}</span> 的结果，那么就有可能会发生上述情况。因此，尽管它存在并且置入到正确的位置，但是仍有可能无法触发该标记。 </p> </td> 
    <td colname="col3"> <p>在每个页面上安装 DTM <span class="codeph">pageBottom</span> 调用。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID 服务 - Cookie 存在</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/tools/macid.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 未找到 <span class="codeph">AMCV_</span> Cookie。必须从 <span class="codeph">VisitorAPI.js</span> 代码实例化一个访客对象。 </p> </td> 
    <td colname="col3"> <p> 如果这是 DTM 实施，请验证 AdobeOrg ID 是否正确输入到 MCID 工具中。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b>Experience Cloud ID 服务 - MID 值存在</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/cookies.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 未在 <span class="codeph">AMCV_</span> Cookie 中找到 MID 值。 </p> </td> 
    <td colname="col3"> <p>再次测试，检查是否存在任何 MCID API 延迟。如果这种情况持续存在，请联系 Adobe 客户关怀团队。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Experience Cloud ID 服务 - 应该安装</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/overview.html" format="html" scope="external"> 其他信息</a> </p> </td> 
    <td colname="col2"> <p> 未找到 Experience Cloud ID 服务代码。强烈推荐使用 ECID，以确保您能够充分利用 Experience Cloud 解决方案，并且这对于跨 EC 解决方案的 ID 管理至关重要。 </p> </td> 
    <td colname="col3"> <p>请安装最新版本的 MCID。 </p> </td> 
   </tr> 
   <tr> 
    <td colname="col1"> <p><b> Target - 库已加载到 &lt;head&gt; 中</b> </p> <p>权重：4 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> 
     <!--
       TE61c380082a4b4706b28a84aa047599a7 
     --> </td> 
    <td colname="col2"> <p> Target 库应该加载到 <span class="codeph">&lt;head&gt;</span> 标记中。 </p> </td> 
    <td colname="col3"> <p> 检查以确保 Target 库已加载到 <span class="codeph">&lt;head&gt;</span> 标记中。 </p> </td> 
   </tr> 
  </tbody> 
</table>
