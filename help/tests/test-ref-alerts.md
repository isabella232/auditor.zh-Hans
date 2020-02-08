---
description: 此参考提供了有关Auditor显示的测试警报的更多信息。
seo-description: 此参考提供了有关Auditor显示的测试警报的更多信息。
seo-title: 警报
title: 警报
uuid: 8f05b3c1-2427-4691-a88f-1de98f120a02
translation-type: tm+mt
source-git-commit: 762ff31ca4d5ed69d1b813589e419c51a40d5920

---


# 警报{#alerts}

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
      CAce6db25bc8c443409f0fcc5ac9d622c3 
    </draft-comment> <p><b>DTM - pageBottom回调位置</b> </p> <p>粗细：0 </p> <p><a href="https://experiencecloud.adobe.com/resources/help/en_US/dtm/t_add_header_fooder_code.html" format="html" scope="external"> 其他信息</a> </p> 
    <draft-comment>
      TEa9df69942f404055a64262889c8b21d3 
    </draft-comment> </td> 
   <td colname="col2"> <p>动态标签管理需 <span class="codeph"> 要_satellite.pageBottom()函数</span> 。 在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，确保DTM功能正确。 </p> <p> <p>注意：最好将标签作为 <i>&lt;body&gt;</i> 中的 <span class="codeph"> 最后一个</span>标签。 如果在 <span class="codeph"> &lt;body&gt;标签中找到它</span> ，它有可能正常工作，但由于它不是最佳实践，它可能运行不正确，或出现意外或不希望的结果。 </p> </p> </td> 
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
      1.0.5 
    </draft-comment> <p><b>启动项- page底部回调位置</b> </p> <p>粗细：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他信息</a> </p> 
    <draft-comment>
      TE48c499b022f545c5bccc6f8bde169685 
    </draft-comment> </td> 
   <td colname="col2"> <p>如果同步部 <span class="codeph"> 署， </span>则启动项应在页面正文中最后定义pageBottom回调函数。 </p> <p> <p>注意：最好将标签作为 <i>&lt;body&gt;</i> 中的 <span class="codeph"> 最后一个</span>标签。 如果在 <span class="codeph"> &lt;body&gt;标签中找到它</span> ，它有可能正常工作，但由于它不是最佳实践，它可能运行不正确，或出现意外或不希望的结果。 </p> </p> </td> 
   <td colname="col3"> <p>Launch需要 <span class="codeph"> _satellite.pageBottom()函数</span> 才能进行同步部署。 在结束&lt;/body&gt;标签前添加内联脚 <span class="codeph"> 本</span> ，以确保正确的启动功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——自托管</b> </p> <p>粗细：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> Launch快速入门</a> </p> <p><a href="https://docs.adobelaunch.com/client-side-information/asynchronous-deployment" format="https" scope="external"> 启动异步部署</a> </p> </td> 
   <td colname="col2"> <p>启动库托管在Adobe的Akamai实例 <span class="filepath"> assets.adobedtm.com上</span>。 </p> <p>自托管是加载Launch的推荐方法，因为它通过缓存控制、减少第三方脚本依赖关系和加强对发布过程的控制提供了对网站性能的更好控制。 可以通过您自己的Web托管或CDN托管和管理启动库。 </p> </td> 
   <td colname="col3"> <p>尽管通过Akamai CDN启动托管在大多数情况下都有效，但建议将自托管作为提高页面性能的第一步。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>启动项——应异步部署</b> </p> <p>粗细：0 </p> <p><a href="https://docs.adobelaunch.com/getting-started" format="https" scope="external"> 其他信息</a> </p> </td> 
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

