---
description: 此参考可提供有关 Auditor 执行的标记存在测试的更多信息。
seo-description: 此参考可提供有关 Auditor 执行的标记存在测试的更多信息。
seo-title: 标记存在
title: 标记存在
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: ht
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 标记存在

此参考可提供有关 Auditor 执行的标记存在测试的更多信息。

Auditor 会评估标记是否存在，以及标记在页面代码中的位置是否正确。

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
   <td colname="col3"> <p>使用 Advertising Cloud Launch Extension 实施 Advertising Cloud 标记。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - 已实施区段像素</b> </p> <p>权重：5 </p> </td> 
   <td colname="col2"> <p> 将您的 Advertising Cloud 区段像素升级为新的 Advertising Cloud 纯图像标记。采用已弃用的 AMO 区段标记可能会导致数据丢失。 </p> </td> 
   <td colname="col3"> <p>通过 Advertising Cloud Launch Extension 实施 Advertising Cloud 区段像素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - 在 DOM 中加载</b> </p> <p>权重：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/zh_CN/sc/implement/" format="https" scope="external"> 其他信息</a> </p> </td> 
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
   <td colname="col2"> <p> 未检测到 DTM <code> pageBottom</code> 标记。 </p> <p>如果相关的调用位于 <code> if</code> 语句中，且该语句会导致类似 <code> if (false) {_satellite.pageBottom()}</code> 的结果，那么就有可能会发生上述情况。因此，尽管它存在并且置入到正确的位置，但是仍有可能无法触发该标记。 </p> </td> 
   <td colname="col3"> <p>在每个页面上安装 DTM <code> pageBottom</code> 调用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID 服务 - 代码存在</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/overview.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>未找到 Experience Cloud ID 服务代码。强烈推荐使用 Experience Cloud ID (MCID)，以确保您能够充分利用 Experience Cloud 解决方案，并且这对于跨 Experience Cloud 解决方案的 ID 管理至关重要。 </p> </td> 
   <td colname="col3"> <p> 安装最新版本的 MCID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID 服务 - Cookie 存在</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 未找到 <span class="codeph">AMCV_</span> Cookie。必须从 <span class="codeph">VisitorAPI.js</span> 代码实例化一个访客对象。 </p> </td> 
   <td colname="col3"> <p> 如果这是 DTM 实施，请验证 AdobeOrg ID 是否正确输入到 MCID 工具中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID 服务 - MID 值存在</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/id-service/using/intro/cookies.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在 <span class="codeph"> AMCV_</span> Cookie 中未找到 MID 值。 </p> </td> 
   <td colname="col3"> <p>再次测试，检查是否存在任何 MCID API 延迟。如果这种情况持续存在，请联系 Adobe 客户关怀团队。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Launch - 已加载库</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在 DOM 中未找到全局 _satellite 对象。未安装或无法执行 Launch。 </p> </td> 
   <td colname="col3"> <p>验证是否已在页面上实施 Launch 库，且没有遭到后续脚本活动的阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - 没有多个嵌入脚本</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>页面上不应加载多个嵌入脚本。生产站点应当只加载一个 Launch 库。 </p> </td> 
   <td colname="col3"> <p>验证页面上是否只加载了生产库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - &lt;body&gt; 中存在 pageBottom 回调函数</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页面的 <span class="codeph">&lt;body&gt;</span> 标记中没有找到 <span class="codeph">_satellite.pageBottom()</span> 回调函数，它是 Launch 的必需函数。 </p> <p>如果根本在页面上找不到 <span class="codeph">pageBottom</span> 调用，或者如果它位于 <span class="codeph">&lt;head&gt;</span> 标记中（或其他一些意外的位置），测试则会失败。只有在从 <span class="codeph">&lt;body&gt;</span> 标记中找到 <span class="codeph">pageBottom</span> 的情况下，测试才会通过。如果页面上根本不存在这项调用，则无法正常运转，而且另外两个 <span class="codeph">pageBottom</span> 测试也将失败。 </p> </td> 
   <td colname="col3"> <p>为了确保 Launch 正常运行，请在紧接着闭合的 <span class="codeph">&lt;/body&gt;</span> 标记之前添加内联脚本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - 异步部署时，不应该存在 pageBottom 回调函数</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>在页面上找到 <span class="codeph">_satellite.pageBottom()</span> 回调函数，异步部署 Launch 时，不应该存在 pageBottom 回调函数。 </p> </td> 
   <td colname="col3"> <p>请移除 <span class="codeph">_satellite.pageBottom()</span> 脚本，以启用适当的 Launch 功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - 代码存在</b> </p> <p>权重：5 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>应当在 DOM 中定义 Target。 </p> </td> 
   <td colname="col3"> <p>安装最新版本的 Target (at.js)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target - 库已加载到 &lt;head&gt; 中</b> </p> <p>权重：4 </p> <p><a href="https://docs.adobe.com/content/help/zh-Hans/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> Target 库应该加载到 <span class="codeph">&lt;head&gt;</span> 标记中。 </p> </td> 
   <td colname="col3"> <p> 检查以确保 Target 库已加载到 <span class="codeph">&lt;head&gt;</span> 标记中。 </p> </td> 
  </tr> 
 </tbody> 
</table>
