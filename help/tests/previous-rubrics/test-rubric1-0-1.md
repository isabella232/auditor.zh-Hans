---
description: 'null'
seo-description: 'null'
seo-title: 测试标准1.0.1
title: 测试标准1.0.1
uuid: 2ed2572e-ddb8-4899-b3a9-1329afdd7905
translation-type: tm+mt
source-git-commit: 712d0768e5e5394372293bf8231c91489519bcd1

---


# 测试标准1.0.1{#test-rubric}

## 测试标准1.0.1 {#topic-25ed23afdfaf4a12b149ff276965b043}

## 警报 {#alerts}

此参考提供了有关Auditor显示的测试警报的更多信息。

警报显示您应该注意的问题，但这不会影响您的得分。 这些是最佳实践建议，在某些情况下可能不适用于您的实施。

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
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 实施了正确的转化标签</b> </p> <p>粗细：0 </p> </td> 
   <td colname="col2"> <p>检查是否使用了正确的转换标记。 </p> <p> <p>警告： 使用已弃用的TubeMogul转换标签可能会导致数据丢失。 </p> </p> </td> 
   <td colname="col3"> <p>将您的转换像素升级到新的Advertising cloud仅限图像的转换标签。 </p> <p>通过Advertising Cloud Launch Extension，可以最轻松地实现这一点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 使用的JS标记正确</b> </p> <p>粗细：0 </p> </td> 
   <td colname="col2"> <p>Advertising cloud应使用最新的JavaScript标记。 </p> </td> 
   <td colname="col3"> <p>将Advertising Cloud javaScript升级到最新版本。 使用已弃用的JavaScript版本可能会导致功能丢失。 </p> <p>通过使用Advertising Cloud Launch Extension，可以更轻松地实现这一点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 仅限图像的标签</b> </p> <p>粗细：0 </p> </td> 
   <td colname="col2"> <p>Advertising cloud图像像素格式应与以下推荐格式之一匹配： </p> <p> 
     <ul id="ul_D85BE9C8A8654DE890E1A814E3573D86"> 
      <li id="li_E2AEDD76AC7044E8AD6AE8375858D198"> <p><span class="codeph"> http(s)://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_1EEFA03516BF445294B5EC5DED891758"> <p><span class="codeph"> http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;</span> </p> </li> 
      <li id="li_F72206B142214217BDD34356D2F3D8AD"> <p><span class="codeph"> http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?</span> </p> </li> 
     </ul> </p> </td> 
   <td colname="col3"> <p>将您的Advertising cloud像素升级到新的Advertising cloud仅图像标记，这可确保您充分利用Advertising cloud的完整功能。 </p> <p>通过Advertising Cloud Launch Extension，可以最轻松地实现这一点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 支持段像素DSP同步</b> </p> <p>粗细：0 </p> </td> 
   <td colname="col2"> <p>检查TubeMogul段像素是否包含DSP同步设置，并建议将该设置添加到像素。 </p> <p>DSP同步设置由查询字符串参数的使用决定，因此 </p> <p>如果标记被触发到<span class="codeph"> (“https://rtd.tubemogul.com/upi/?sid=&lt;HASH_VALUE&gt;”</span> </p> <p> 或 <span class="codeph"> “http(s)://rtd-tm.everesttech.net/upi/?sid=&lt;HASH_VALUE&gt;”</span> </p> <p> 或 <span class="codeph"> “http(s)://pixel.everesttech.net/px2/&lt;NUMERIC_ID&gt;?”</span> </p> <p>标记包含URL参 <span class="codeph"> 数"sid=")</span> </p> <p>然后检查URL参数 <span class="codeph"> "cs=0"</span> 或<span class="codeph"> "cs=1"是否存在，如果不建议将</span><span class="codeph"></span> "cs=1"添加到这些像素，以便受众匹配率可以提高。 </p> </td> 
   <td colname="col3"> <p> 将URL参数“cs=1” <span class="codeph"> 添加到Advertising cloud像素中</span> ，以便进行DSP同步，从而提高受众匹配率。 </p> <p>通过Advertising Cloud Launch Extension，可以最轻松地实现这一点。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom回调位置</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 其他信息</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>动态标签管理需 <span class="codeph"> 要_satellite.pageBottom()函数</span> 。 在结束body标签之前添加内联脚本，以确保DTM功能正确。 </p> <p> <p>注意：最好将标签作为 <i>&lt;body&gt;</i> 中的 <span class="codeph"> 最后一个</span>标签。 如果在 <span class="codeph"> &lt;body&gt;标签中找到它</span> ，它有可能正常工作，但由于它不是最佳实践，它可能运行不正确，或出现意外或不希望的结果。 </p> </p> </td> 
   <td colname="col3"> <p>在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，确保DTM功能正确。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM —— 自托管</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/deployment.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> DTM库托管在Adobe的Akamai实例上，该实例位于 <span class="filepath"> assets.adobedtm.com</span>。 </p> <p> 自托管是加载DTM的推荐方法，因为它通过缓存控制、减少第三方脚本依赖关系和增强对发布过程的控制提供对网站性能的更大控制。 DTM库可以通过您自己的Web托管或CDN进行托管和管理。 </p> </td> 
   <td colname="col3"> <p>自托管是在页面上加载DTM的推荐方法。 尽管通过Akamai CDN进行DTM托管在大多数情况下都有效，但自托管可提高页面性能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Experience Cloud ID服务——仅使用一个AdobeOrg</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_id_request.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>在正常的MCID实施中，应使用单个AdobeOrg。 </p> </td> 
   <td colname="col3"> <p>验证此实施是否存在多个AdobeOrg ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项- page底部回调位置</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>如果同步部 <span class="codeph"> 署， </span>则启动项应在页面正文中最后定义pageBottom回调函数 </p> <p> <p>注意：最好将标签作为 <i>&lt;body&gt;</i> 中的 <span class="codeph"> 最后一个</span>标签。 如果在 <span class="codeph"> &lt;body&gt;标签中找到它</span> ，它有可能正常工作，但由于它不是最佳实践，它可能运行不正确，或出现意外或不希望的结果。 </p> </p> </td> 
   <td colname="col3"> <p>在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，确保DTM功能正确。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——自托管</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>启动库托管在Adobe的Akamai实例 <span class="filepath"> assets.adobedtm.com上</span>。 </p> <p>自托管是加载Launch的推荐方法，因为它通过缓存控制、减少第三方脚本依赖关系和加强对发布过程的控制提供了对网站性能的更好控制。 可以通过您自己的Web托管或CDN托管和管理启动库。 </p> </td> 
   <td colname="col3"> <p>尽管通过Akamai CDN启动托管在大多数情况下都有效，但建议将自托管作为提高页面性能的第一步。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——应异步部署</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>启动应异步部署以获得最佳性能。 </p> </td> 
   <td colname="col3"> <p>在内联脚本中包含async参数，以确保正确的异步启动功能 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> 目标- mbox中的内容默认</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/target/ov2/r_target-atjs-mboxcreate.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 使用at.js时，mboxDefault中应存在内容。 </p> </td> 
   <td colname="col3"> <p>验证内容是否可用。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 配置 {#configuration}

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
    </draft-comment> <p><b>启动项——最新版本</b> </p> <p>粗细：2 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
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

## 标签一致性 {#tag-consistency}

此参考提供了有关Auditor执行的标记一致性测试的更多信息。

Auditor的一致性测试会在所有扫描的页面中查找不一致的内容。 这些值或配置应在站点上的所有页面上相同，以确保准确的数据收集。

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>分析——一致的代码版本 </b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/choose-implementation-method.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 找到多个版本的Analytics代码。 </p> </td> 
   <td colname="col3"> <p>将所有Analytics实例替换为当前版本。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 标记存在 {#tag-presence}

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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 代码呈现</b> </p> <p>粗细：5 </p> </td> 
   <td colname="col2"> <p> DOM中不提供Advertising cloud标记。 </p> </td> 
   <td colname="col3"> <p>使用Advertising Cloud Launch扩展实施Advertising cloud标记。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Advertising Cloud —— 实施细分像素</b> </p> <p>粗细：5 </p> </td> 
   <td colname="col2"> <p> 将您的Advertising cloud细分像素升级到新的Advertising cloud仅图像标记。 使用已弃用的AMO区段标记可能会导致数据丢失。 </p> </td> 
   <td colname="col3"> <p>使用Advertising Cloud Launch Extension实施Advertising cloud细分像素。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>分析——在DOM中加载</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/sc/implement/" format="https" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 未检测到Adobe Analytics标记。 </p> </td> 
   <td colname="col3"> <p>安装最新版Analytics。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM —— 已加载库</b> </p> <p>粗细：5 </p> <p>其他信息: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/c_Troubleshooting.html" format="html" scope="external"> DTM疑难解答</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 添加页眉和页脚代码</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> 在DOM中找不到全局_satellite对象。 动态标签管理未安装或无法执行。 </p> </td> 
   <td colname="col3"> <p>验证DTM库是否已在页面上实现，且未被后续脚本活动阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> DTM —— 一个嵌入代码</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 生产站点只应加载一个DTM库。 </p> </td> 
   <td colname="col3"> <p>验证页面上仅加载生产库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM - pageBottom回调存在于&lt;body&gt;中</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页 <span class="codeph"> 面的</span><span class="codeph"></span> &lt;body&gt;（动态标签管理需要）中找不到_satellite.pageBottom()回调。 </p> <p>如果在页面上 <span class="codeph"> 找 </span>不到pageBottom调用，或者它位于 <span class="codeph"> &lt;head&gt;</span> 标签中（或其他一些意外位置），则此测试将失败。 仅当在&lt;body&gt;标 <span class="codeph"> 记中找到pageBottom</span> 时 <span class="codeph"> ，它才会传递</span> 。 如果它根本不在页面上，它将无法正常工作，另外两个pageBottom <span class="codeph"> 测试也将失败</span> 。 </p> </td> 
   <td colname="col3"> <p>在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，确保DTM功能正确。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>DTM —— 已触发pageBottom标签</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 未检 <span class="codeph"> 测到DTM pageBottom</span> 标签。 </p> <p>如果调用位于 <span class="codeph"> if</span> 语句中，并导致与if(false){_satellite.pageBottom()}类似的结果，则 <span class="codeph"> 可能会发生这种情况</span>。 因此，尽管它可能存在并正确放置，但标签仍可能无法触发。 </p> </td> 
   <td colname="col3"> <p>在每页安 <span class="codeph"> 装DTM page</span> Bottom调用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务——代码存在</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-overview.htmlimplementation-guides.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>找不到Experience Cloud ID服务代码。 强烈建议使用Experience Cloud ID(MCID)，以确保您能够充分利用Experience cloud解决方案的价值，并且对于跨Experience cloud解决方案的ID管理至关重要。 </p> </td> 
   <td colname="col3"> <p> 安装MCID的最新版本。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务- Cookie存在</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid-implementation-guides.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 找 <span class="codeph"> 不到AMCV_</span> Cookie。 必须从VisitorAPI.js代码实例化访 <span class="codeph"> 客对象</span> 。 </p> </td> 
   <td colname="col3"> <p> 如果这是DTM实施，请验证AdobeOrg ID是否正确输入到MCID工具中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Experience Cloud ID服务- MID价值存在</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html#concept_37156268512445F287CD4BBB2839FFAA__section_C55AF54828DC4CCE89F6118655D694C8" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在AMCV_cookie中找不到MID <span class="codeph"> 值</span> 。 </p> </td> 
   <td colname="col3"> <p>再次测试以检查任何MCID API延迟。 如果该情况仍然存在，请与Adobe客户服务联系。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> 启动项——已加载库</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在DOM中找不到全局_satellite对象。 未安装启动项或无法执行启动项。 </p> </td> 
   <td colname="col3"> <p>验证启动库是否已在页面上实现且未被后续脚本活动阻止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——没有多个嵌入脚本</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p>页面上不应加载多个嵌入脚本。 生产站点只应加载一个启动库。 </p> </td> 
   <td colname="col3"> <p>验证页面上仅加载生产库。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项- pageBottom回调存在于&lt;body&gt;中</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
   <td colname="col2"> <p> 在页 <span class="codeph"> 面的</span><span class="codeph"></span> &lt;body&gt;中找不到_satellite.pageBottom()回调，这是Launch必需的。 </p> <p>如果在页面上 <span class="codeph"> 找 </span>不到pageBottom调用，或者它位于 <span class="codeph"> &lt;head&gt;</span> 标签中（或其他一些意外位置），则此测试将失败。 仅当在&lt;body&gt;标 <span class="codeph"> 记中找到pageBottom</span> 时 <span class="codeph"> ，它才会传递</span> 。 如果它根本不在页面上，它将无法正常工作，另外两个pageBottom <span class="codeph"> 测试也将失败</span> 。 </p> </td> 
   <td colname="col3"> <p>在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，以确保正确的启动功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——异步部署时，pageBottom回调不应存在</b> </p> <p>粗细：5 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/experience-cloud/launch/t_quick-start.html" format="html" scope="external"> 其他信息</a> </p> </td> 
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
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> 目标——加载到&lt;head&gt;中的库</b> </p> <p>粗细：4 </p> <p><a href="https://docs.adobe.com/content/help/en/target/using/implement-target/implementing-target.html" format="html" scope="external"> 其他信息</a> </p> 
    <draft-comment>
      TE61c380082a4b4706b28a84aa047599a7 
    </draft-comment> </td> 
   <td colname="col2"> <p> 应将Target库加载到 <span class="codeph"> &lt;head&gt;标签中</span> 。 </p> </td> 
   <td colname="col3"> <p> 检查以确保Target库已加载到 <span class="codeph"> &lt;head&gt;标签中</span> 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

