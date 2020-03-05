---
description: 此参考可提供有关 Auditor 执行的配置测试的更多信息。
seo-description: 此参考可提供有关 Auditor 执行的配置测试的更多信息。
seo-title: 配置
title: 配置
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: ht
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 配置

此参考可提供有关 Auditor 执行的配置测试的更多信息。

配置测试会扫描实施中的特定设置、值或潜在冲突。Auditor 会根据其他规则和推荐的最佳做法来评估标记。

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - 转化名称仅使用字母数字字符</b> </p> <p>权重：3 </p> </td> 
   <td colname="col2"> <p>除“<span class="codeph">ev_transid</span>”参数之外（<span class="codeph">ev_transid</span> 值可包含文本或数值），<span class="codeph">ev_conversion_property_name</span> 参数应当只包含数值和小数值 </p> <p>查找 <span class="codeph">everesttech.net</span> 像素，其中包含以 <span class="codeph">ev_</span> 开头的 URL 参数。 </p> <p>示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> 确保事务属性参数仅包含数值和小数值。 </p> <p> <p>警告：任何其他值类型都可能会导致数据丢失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - 转化名称使用 URL 安全字符</b> </p> <p>权重：3 </p> </td> 
   <td colname="col2"> <p> 转化属性名称不应包含 &amp; 符号或问号。 </p> <p> 示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>确保事务属性参数不包含非编码的 &amp; 符号或问号。这会破坏 URL 格式。 </p> <p> <p>警告：包含非编码的 &amp; 符号或问号的属性参数（例如：<span class="codeph">ev_formComplete?=1</span> 或 <span class="codeph">ev_formComplete&amp;Submit=1</span>），可能会导致数据丢失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud - 已正确实施事务 ID</b> </p> <p>权重：1 </p> </td> 
   <td colname="col2"> <p> 属性名称 <span class="codeph"> ev_transid=</span> 不应为空。 </p> <p>示例： </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>属性名称 <span class="codeph">ev_transid=</span> 不应当没有任何值 (<span class="codeph">ev_transid=</span>)。如果没有任何值，则可能会丢失事务数据。为 <span class="codeph">ev_transid=</span> 赋值，或从像素中删除此参数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - 在 DOM 中实例化</b> </p> <p>权重：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 未安装或无法执行 Adobe Analytics 代码。在 Web 页面上未找到 Analytics 代码时，返回值为 0。 </p> </td> 
   <td colname="col3"> <p>验证是否已在页面上实施 Analytics 标记，且没有遭到后续脚本活动的阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - 实例化一次</b> </p> <p>权重：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/zh_CN/sc/implement/" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页面上多次检测到 Adobe Analytics 代码。在 Web 页面上未找到 Analytics 代码时，返回值为 0。 </p> </td> 
   <td colname="col3"> <p>确保页面上仅有一个 Analytics 标记。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics - 最新版本</b> </p> <p>权重：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 您的页面没有运行最新版本的 Analytics 代码库。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。在 Web 页面上未找到 Analytics 代码时，返回值为 0。 </p> </td> 
   <td colname="col3"> <p>安装最新版本的 Analytics 代码库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - DOM 就绪后，异步加载第三方标记</b> </p> <p>权重：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/zh_CN/dtm/load_order.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>要在良好的用户体验与收集准确的数据之间达成一种平衡，则应当在 DOM 就绪后触发第三方标记。这将可以确保执行相关的跟踪脚本，同时又不会影响站点的正常运转。 </p> </td> 
   <td colname="col3"> <p>解决这个问题的方法是：调整 DOM 就绪后触发执行第三方像素的所有规则。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID 服务 - 最新版本</b> </p> <p>权重：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/zh_CN/dtm/macid.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 您的页面没有运行最新版本的访客 ID 服务代码库 <span class="codeph">visitorAPI.js</span>。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。 </p> </td> 
   <td colname="col3"> <p>安装最新版本的访客 ID 服务代码库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Launch - 最新版本</b> </p> <p>权重：2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>这些页面未运行最新版本的 Launch 代码库 (Turbrie)。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。 </p> </td> 
   <td colname="col3"> <p> 通过重建和发布 Launch 库来更新 Launch 库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - 最新版本</b> </p> <p>权重：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 您的页面没有运行最新版本的 Target 代码库。为了利用性能改进并提供最新功能，我们会不断地更新和调整旨在支持 Experience Cloud 技术的代码库。 </p> </td> 
   <td colname="col3"> <p>安装最新版本的 Target 代码库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - mboxDefault 先于 mboxCreate </b> </p> <p>权重：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p><span class="codeph">mboxCreate</span> 的正确用法类似于下面的示例： </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Customer content--&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>调用 <span class="codeph">mboxCreate()</span> 之前，请务必包含 <span class="codeph">&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> 标记。at.js 并不会为您添加此标记。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target - 有效的 DOCTYPE</b> </p> <p>权重：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 检测到无效的 DOCTYPE。在这种情况下，将不会触发 mbox。 </p> <p>对于 at.js，DOCTYPE 必须处于“标准”模式，否则 Target 将无法正常运作。 </p> </td> 
   <td colname="col3"> <p>更新页面上的 DOCTYPE。 </p> </td> 
  </tr> 
 </tbody> 
</table>

