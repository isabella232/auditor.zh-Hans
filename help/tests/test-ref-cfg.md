---
description: 此参考提供了有关Auditor执行的配置测试的更多信息。
seo-description: 此参考提供了有关Auditor执行的配置测试的更多信息。
seo-title: 配置
title: 配置
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# 配置

此参考提供了有关Auditor执行的配置测试的更多信息。

配置测试会扫描您的实施中的特定设置、值或潜在冲突。 Auditor根据其他规则和建议的最佳实践评估标记。

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
    </draft-comment> <p><b>Advertising Cloud —— 转换名称仅使用字母数字字符</b> </p> <p>粗细：3 </p> </td> 
   <td colname="col2"> <p>ev_conversion_property_name <span class="codeph"> (ev_conversion_property_name</span> )参数应仅包含数字和小数值，EXCEPT表示“<span class="codeph"> ev_transid”(ev_transid)参数(ev_transid</span><span class="codeph"></span> (ev_transid)值可包含文本或数值) </p> <p>查找 <span class="codeph"> 包含以ev_开头的URL参数的</span> everestech.net像素 <span class="codeph"></span>。 </p> <p>示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> 确保您的事务属性参数只包含数字和小数值。 </p> <p> <p>警告： 任何其他值类型都可能导致数据丢失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 转换名称使用URL安全字符</b> </p> <p>粗细：3 </p> </td> 
   <td colname="col2"> <p> 转换属性名称不应包含和号或问号。 </p> <p> 示例： </p> <p><span class="codeph"> http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>确保事务属性参数不包含非编码的&amp;符号或问号。 这将破坏URL格式。 </p> <p> <p>警告：包含非编码&amp;符号或问号的属性参数(例如：ev_ <span class="codeph"> formComplete?=1</span> or <span class="codeph"> ev_formComplete&amp;Submit=1</span>)，可能导致数据丢失。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 正确实施的交易ID</b> </p> <p>粗细：1 </p> </td> 
   <td colname="col2"> <p> 属性名 <span class="codeph"> ev_transid=</span> 不应为空。 </p> <p>示例： </p> <p> <span class="codeph"> http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>属性名 <span class="codeph"> ev_transid=</span> ，不应保留不带值(<span class="codeph"> ev_transid=</span>)。 如果保留该值时没有值，则可能会丢失事务数据。 为ev_transid=赋值 <span class="codeph"></span> ，或从像素中删除参数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>分析——在DOM中实例化</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/impl_testing.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> Adobe Analytics代码未安装或无法执行。 在未找到分析代码网页时返回0。 </p> </td> 
   <td colname="col3"> <p>验证Analytics标记是否已在页面上实现且未被后续脚本活动阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>分析——实例化一次</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页面上检测到Adobe Analytics代码不止一次。. 在未找到分析代码网页时返回0。 </p> </td> 
   <td colname="col3"> <p>确保页面上仅有一个Analytics标记。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Analytics —— 最新版本</b> </p> <p>粗细：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/appmeasurement/release" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 您的页面未运行最新版本的Analytics代码库。 支持Experience cloud技术的代码库不断更新和调整，以利用性能改进并提供最新功能。 在未找到分析代码网页时返回0。 </p> </td> 
   <td colname="col3"> <p>安装Analytics库的最新版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM —— 第三方标记在DOM就绪后异步加载</b> </p> <p>粗细：3 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/load_order.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>要在良好的用户体验和收集准确数据之间取得平衡，应在DOM就绪时触发第三方标记。 这将确保这些跟踪脚本在不影响站点功能的情况下执行。 </p> </td> 
   <td colname="col3"> <p>通过调整执行第三方像素的所有规则以在DOM Ready处触发，解决此问题。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务——最新版本</b> </p> <p>粗细：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/macid.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 您的页面未运行最新版本的访客ID服务代码库visitorAPI.js <span class="codeph"></span>。 支持Experience cloud技术的代码库不断更新和调整，以利用性能改进并提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安装最新版本的访客ID服务库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——最新版本</b> </p> <p>粗细：2 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>这些页面未运行最新版本的启动代码库(Turbrie)。 支持Experience cloud技术的代码库不断更新和调整，以利用性能改进并提供最新功能。 </p> </td> 
   <td colname="col3"> <p> 通过重建和发布启动库来更新启动库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Target —— 最新版本</b> </p> <p>粗细：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/dtm/update-target-tool.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 您的页面未运行最新版本的Target代码库。 支持Experience cloud技术的代码库不断更新和调整，以利用性能改进并提供最新功能。 </p> </td> 
   <td colname="col3"> <p>安装Target库的最新版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>目标- mboxDefault优先于mboxCreate </b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>正确使用mboxCreate <span class="codeph"> 后</span> ，外观类似于： </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-客户内容—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>在调用 <span class="codeph"> mboxCreate()之前，请务必包含&lt;div class="mboxDefault"&gt;&lt;/div&gt;</span><span class="codeph"> 标签</span>。 at.js不会为您添加一个。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>目标——有效的DOCTYPE</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 检测到无效的DOCTYPE。 在此方案中不会触发mbox。 </p> <p>对于at.js,DOCTYPE必须处于“标准”模式，否则Target将无法工作。 </p> </td> 
   <td colname="col3"> <p>更新页面上的DOCTYPE。 </p> </td> 
  </tr> 
 </tbody> 
</table>

