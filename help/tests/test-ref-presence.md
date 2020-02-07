---
description: 此参考提供了有关Auditor对标记状态执行的测试的更多信息。
seo-description: 此参考提供了有关Auditor对标记状态执行的测试的更多信息。
seo-title: 标记存在
title: 标记存在
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 标记存在

此参考提供了有关Auditor对标记状态执行的测试的更多信息。

Auditor评估标记是否存在，以及它是否在页面代码中的正确位置。

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
   <td colname="col1"> <p><b>Advertising Cloud —— 代码呈现</b> </p> <p>粗细：5 </p> </td> 
   <td colname="col2"> <p> DOM中不提供Advertising cloud标记。 </p> </td> 
   <td colname="col3"> <p>使用Advertising Cloud Launch扩展实施Advertising cloud标记。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud —— 实施细分像素</b> </p> <p>粗细：5 </p> </td> 
   <td colname="col2"> <p> 将您的Advertising cloud细分像素升级到新的Advertising cloud仅图像标记。 使用已弃用的AMO区段标记可能会导致数据丢失。 </p> </td> 
   <td colname="col3"> <p>使用Advertising Cloud Launch Extension实施Advertising cloud细分像素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>分析——在DOM中加载</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 未检测到Adobe Analytics标记。 </p> </td> 
   <td colname="col3"> <p>安装最新版Analytics。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM —— 已加载库</b> </p> <p>粗细：5 </p> <p>其他信息: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/en/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> DTM疑难解答</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 添加页眉和页脚代码</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> 在DOM中找不到全局_satellite对象。 动态标签管理未安装或无法执行。 </p> </td> 
   <td colname="col3"> <p>验证DTM库是否已在页面上实现，且未被后续脚本活动阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM —— 一个嵌入代码</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 生产站点只应加载一个DTM库。 </p> </td> 
   <td colname="col3"> <p>验证页面上仅加载生产库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - pageBottom回调存在于&lt;body&gt;中</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页 <span class="codeph"> 面的</span><span class="codeph"></span> &lt;body&gt;（动态标签管理需要）中找不到_satellite.pageBottom()回调。 </p> <p>如果在页面上 <span class="codeph"> 找 </span>不到pageBottom调用，或者它位于 <span class="codeph"></span> &lt;head&gt;标签中（或其他一些意外位置），则此测试将失败。 仅当在&lt;body&gt;标 <span class="codeph"> 记中找到pageBottom</span> 时 <span class="codeph"> ，它才会传递</span> 。 如果它根本不在页面上，它将无法正常工作，另外两个pageBottom <span class="codeph"> 测试也将失败</span> 。 </p> </td> 
   <td colname="col3"> <p>在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，确保DTM功能正确。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM —— 已触发pageBottom标签</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 未检 <code> pageBottom</code> 测到DTM标记。 </p> <p>如果调用位于导致类似内容的 <code> if</code> 语句中，则可能会发生这种情况 <code> if (false) {_satellite.pageBottom()}</code>。 因此，尽管它可能存在并正确放置，但标签仍可能无法触发。 </p> </td> 
   <td colname="col3"> <p>在每页安 <code> pageBottom</code> 装DTM调用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务——代码存在</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>找不到Experience Cloud ID服务代码。 强烈建议使用Experience Cloud ID(MCID)，以确保您能够充分利用Experience cloud解决方案的价值，并且对于跨Experience cloud解决方案的ID管理至关重要。 </p> </td> 
   <td colname="col3"> <p> 安装MCID的最新版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务- Cookie存在</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 找 <span class="codeph"> 不到AMCV_</span> Cookie。 必须从VisitorAPI.js代码实例化访 <span class="codeph"> 客对象</span> 。 </p> </td> 
   <td colname="col3"> <p> 如果这是DTM实施，请验证AdobeOrg ID是否正确输入到MCID工具中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务- MID价值存在</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在AMCV_cookie中找不到MID <span class="codeph"> 值</span> 。 </p> </td> 
   <td colname="col3"> <p>再次测试以检查任何MCID API延迟。 如果该情况仍然存在，请与Adobe客户服务联系。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> 启动项——已加载库</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在DOM中找不到全局_satellite对象。 未安装启动项或无法执行启动项。 </p> </td> 
   <td colname="col3"> <p>验证启动库是否已在页面上实现且未被后续脚本活动阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>启动项——没有多个嵌入脚本</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>页面上不应加载多个嵌入脚本。 生产站点只应加载一个启动库。 </p> </td> 
   <td colname="col3"> <p>验证页面上仅加载生产库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>启动项- pageBottom回调存在于&lt;body&gt;中</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页 <span class="codeph"> 面的</span><span class="codeph"></span> &lt;body&gt;中找不到_satellite.pageBottom()回调，这是Launch必需的。 </p> <p>如果在页面上 <span class="codeph"> 找 </span>不到pageBottom调用，或者它位于 <span class="codeph"> &lt;head&gt;</span> 标签中（或其他一些意外位置），则此测试将失败。 仅当在&lt;body&gt;标 <span class="codeph"> 记中找到pageBottom</span> 时 <span class="codeph"> ，它才会传递</span> 。 如果它根本不在页面上，它将无法正常工作，另外两个pageBottom <span class="codeph"> 测试也将失败</span> 。 </p> </td> 
   <td colname="col3"> <p>在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，以确保正确的启动功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>启动项——异步部署时，pageBottom回调不应存在</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>在页 <span class="codeph"> 面上找到_satellite.pageBottom()回调</span> ，在异步部署Launch时不应该这样。 </p> </td> 
   <td colname="col3"> <p>删除<span class="codeph"> _satellite.pageBottom()脚本</span> ，以启用正确的启动功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> 目标——代码状态</b> </p> <p>粗细：5 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>目标应在DOM中定义。 </p> </td> 
   <td colname="col3"> <p>安装Target(at.js)的最新版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> 目标——加载到&lt;head&gt;中的库</b> </p> <p>粗细：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 应将Target库加载到 <span class="codeph"> &lt;head&gt;标签中</span> 。 </p> </td> 
   <td colname="col3"> <p> 检查以确保Target库已加载到 <span class="codeph"> &lt;head&gt;标签中</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>
