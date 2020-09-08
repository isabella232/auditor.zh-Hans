---
description: 此参考可提供有关 Auditor 显示的测试警报的更多信息。
seo-description: 此参考可提供有关 Auditor 显示的测试警报的更多信息。
seo-title: 警报
title: 警报
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: ht
source-git-commit: 77ced60ff8e05515521d89d16c32cbad42d1e8d0
workflow-type: ht
source-wordcount: '904'
ht-degree: 100%

---


# 警报{#alerts}

此参考可提供有关 Auditor 显示的测试警报的更多信息。

警报会显示您应该注意的问题，但是不会影响您的得分。这些是推荐的最佳做法，在某些情况下可能不适用于您的实施。

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
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 已实施正确的转化标记</b> </p> <p>权重：0 </p> </td> 
   <td colname="col2"> <p>检查是否使用了正确的转化标记。 </p> <p> <p>警告：使用已弃用的 TubeMogul 转化标记可能会导致数据丢失。 </p> </p> </td> 
   <td colname="col3"> <p>将您的转化像素升级为新的 Advertising Cloud 纯图像转化标记。 </p> <p>通过 Advertising Cloud Launch Extension，可以轻松实现这一目标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 已使用正确的 JS 标记</b> </p> <p>权重：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud 应使用最新的 JavaScript 标记。 </p> </td> 
   <td colname="col3"> <p>将 Advertising Cloud JavaScript 升级到最新版本。使用已弃用的 JavaScript 版本可能会导致功能丧失。 </p> <p>通过使用 Advertising Cloud Launch Extension，可以更轻松地实现这一目标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 纯图像标记</b> </p> <p>权重：0 </p> </td> 
   <td colname="col2"> <p>Advertising Cloud 图像像素格式，应当与以下一种推荐的格式匹配： </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>将您的 Advertising Cloud 像素升级为新的 Advertising Cloud 纯图像标记，这可以确保您能够充分利用 Advertising Cloud 的完整功能。 </p> <p>通过 Advertising Cloud Launch Extension，可以轻松实现这一目标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - 已启用区段像素 DSP 同步</b> </p> <p>权重：0 </p> </td> 
   <td colname="col2"> <p>检查 TubeMogul 区段像素是否包含 DSP 同步设置，并推荐将该设置添加到这个像素中。 </p> <p>DSP 同步设置是根据查询字符串参数的使用情况来确定的，为此 </p> <p>如果标记被触发到<span class="codeph">（"https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或<span class="codeph"> "http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;"</span> </p> <p> 或<span class="codeph"> "http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?"</span> </p> <p>并且标记包含 URL 参数 <span class="codeph">"sid="）</span> </p> <p>那么请检查 URL 参数 <span class="codeph">"cs=0"</span> 或 <span class="codeph">"cs=1"</span> 是否存在，如果不存在，推荐将 <span class="codeph">"cs=1"</span> 添加到这些像素中，以便提高受众匹配率。 </p> </td> 
   <td colname="col3"> <p> 将 URL 参数 <span class="codeph">"cs=1"</span> 添加到您的 Advertising Cloud 像素中，以便可以实现 DSP 同步，从而增加受众匹配率。 </p> <p>通过 Advertising Cloud Launch Extension，可以轻松地实现这一目标。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    --> <p><b>DTM - 置入 pageBottom 回调函数</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他信息</a> </p> 
    <!--
      TEa9df69942f404055a64262889c8b21d3 
    --> </td> 
   <td colname="col2"> <p>Dynamic Tag Management 要求使用 <span class="codeph">_satellite.pageBottom()</span> 函数。为了确保 DTM 正常运行，请在紧接着闭合的 <span class="codeph">&lt;/body&gt;</span> 标记之前添加内联脚本。 </p> <p> <p>注意：最佳做法是将该标记作为 <span class="codeph">&lt;body&gt;</span> 中的<i>最后一个</i>标记。如果在 <span class="codeph">&lt;body&gt;</span> 标记中找到了该函数，则表明存在正常运行的机率，然而由于这不是最佳的做法，所以可能会无法正确运行，或者会出现意外或不希望的结果。 </p> </p> </td> 
   <td colname="col3"> <p>为了确保 DTM 正常运行，请在紧接着闭合的 <span class="codeph">&lt;/body&gt;</span> 标记之前添加内联脚本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - 自托管</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/dtm/using/client-side/client-side-information.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 将 DTM 库托管在 Adobe 位于 <span class="filepath">assets.adobedtm.com</span> 的 Akamai 实例上。 </p> <p> 推荐采用自托管方法来加载 DTM，因为这种方法可通过缓存控制、减少第三方脚本依赖项以及增强对发布过程的控制，更好地控制网站的性能。您可以通过自己的 Web 托管或 CDN 来托管并管理 DTM 库。 </p> </td> 
   <td colname="col3"> <p>推荐采用自托管方法在页面上加载 DTM。尽管通过 Akamai CDN 来托管 DTM 的方法适用于大多数情况，但是，自托管方法可提升页面性能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Experience Cloud ID 服务 - 仅使用一个 AdobeOrg</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/id-request.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>在正常实施 MCID 的过程中，应当使用一个 AdobeOrg。 </p> </td> 
   <td colname="col3"> <p>验证这项实施中是否存在多个 AdobeOrg ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.5 
    --> <p><b>Launch - 置入 pageBottom 回调函数</b> </p> <p>权重：0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> 其他信息</a> </p> 
    <!--
      TE48c499b022f545c5bccc6f8bde169685 
    --> </td> 
   <td colname="col2"> <p>如果要实现同步部署，Launch 则应该在页面正文的最后，定义一个 <span class="codeph">pageBottom</span> 回调函数。 </p> <p> <p>注意：最佳做法是将该标记作为 <span class="codeph">&lt;body&gt;</span> 中的<i>最后一个</i>标记。如果在 <span class="codeph">&lt;body&gt;</span> 标记中找到了该函数，则表明存在正常运行的机率，然而由于这不是最佳的做法，所以可能会无法正确运行，或者会出现意外或不希望的结果。 </p> </p> </td> 
   <td colname="col3"> <p>Launch 要求使用 <span class="codeph">_satellite.pageBottom()</span> 函数才能进行同步部署。为了确保 Launch 正常运行，请在紧接着闭合的 <span class="codeph">&lt;/body&gt;</span> 标记之前添加内联脚本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 自托管</b> </p> <p>权重：0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> Launch 入门指南</a> </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/launch/using/reference/client-side-info/asynchronous-deployment.html" format="https" scope="external"> Launch 异步部署</a> </p> </td> 
   <td colname="col2"> <p>将 Launch 库托管在 Adobe 位于 <span class="filepath"> assets.adobedtm.com</span> 的 Akamai 实例上。 </p> <p>推荐采用自托管方法来加载 Launch，因为这种方法可通过缓存控制、减少第三方脚本依赖项以及增强对发布过程的控制，更好地控制网站的性能。您可以通过自己的 Web 托管或 CDN 来托管并管理 Launch 库。 </p> </td> 
   <td colname="col3"> <p>尽管通过 Akamai CDN 来托管 Launch 的方法适用于大多数情况，但是，推荐实施自托管方法以作为提升页面性能的第一步。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - 应当异步部署</b> </p> <p>权重：0 </p> <p><a href="https://adobe.com/go/launch_help_get_started" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>为了优化性能，应当异步部署 Launch。 </p> </td> 
   <td colname="col3"> <p>将异步参数纳入内联脚本，以确保正确实施 Launch 的异步部署。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b> Target - mboxDefault 中的内容</b> </p> <p>权重：0 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 使用 at.js 时，mboxDefault 中应当存在相关内容。 </p> </td> 
   <td colname="col3"> <p>验证内容是否有效。 </p> </td> 
  </tr> 
 </tbody> 
</table>

