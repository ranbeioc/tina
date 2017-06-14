# 条目元数据管理

即有关原始曲目的信息结构类型数据的增删改查管理。对条目名称别名，多关联角色标记，栏目与板块信息的增删改查处理。同时扩充对专辑和歌单和周边类数据的支持。

曲库核心标准数据与要求如下：

| 字段名 | 使用示例与规格 | 所属对象 | 实施阶段 |
| :--- | :--- | :--- | :--- |
| 编码格式 | UTF-8，GB18030 | 字符集规范 | P1 |
| 防盗链验证 | Y/N | 白名单，域名/平台/版本 | P2 |
| 原始创建时间 | 2017-04-15 01:15:43 |  | P1 |
| 最后更新时间 | 2017-05-15 01:15:46 |  | P1 |
| 最后缓存更新时间 | 2017-06-15 01:15:51 |  | P1 |
|  |  |  |  |
| **曲目（Song）** |  |  |  |
| 曲目编号 | T1234567890 | （唯一标识） | P1 |
| 原文件名 | S1234567890 | 合名（唯一性） | P1 |
| MD5 | 11AFAD2D3555EAB7F251A05C0B7915F9 | 散列函数（文件校验） | P2 |
| SHA1 | A48A9D261882A3AF795E4A9CECC47E8EA098EA7E | 数字签名（文件校验） | P2 |
| CRC32 | 5DB7252F | 循环冗余效验程序库（文件校验） | P2 |
| 歌曲名 | First Love，笨小孩 |  | P1 |
| 演唱类型 | 国/合/演/消/Remix/Live |  | P1 |
| 歌曲封面类型 | {S/M/L} | （尺寸规范另述，下同） | P1 |
| 歌曲封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 歌曲中文首字母 | N/A，BXH |  | P1 |
| 歌曲别名 | 初恋，N/A |  | P2 |
| 歌曲别名中文首字母 | CL， N/A |  | P2 |
| 歌曲时长 | 225s |  | P1 |
| 歌曲风格 | &lt;songtagId&gt;流行 |  | P1 |
| 歌曲类型 | MTV |  | P1 |
| 歌曲语言 | 日语/英语、国语/粤语 |  | P1 |
| 关联艺术家 | &lt;artId&gt;Array | **关联类信息** | P1 |
| 关联专辑 | &lt;albumId&gt;Array |  | P2 |
| 关联歌单 | &lt;sheetId&gt;Array |  | P2 |
| 关联资讯 | &lt;infoId&gt;Array |  | P3 |
| 关联歌曲文件地址 | &lt;songUrl&gt;{type} | 请求所属歌曲文件列表 | P1 |
| 关联三方资源 | &lt;videoId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 关联翻唱作品 | &lt;ugcId+userId+TopNum&gt;Array |  | P1 |
| 关联话题 | &lt;topicId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 订阅用户总数 | 235 | **用户类信息** | P1 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P1 |
| 分享用户总数 | 98 |  | P1 |
| 分享用户列表 | &lt;userId&gt;Array |  | P1 |
| 用户评论总数 | 687 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用 | P2 |
|  |  |  |  |
| **艺术家（Art）** |  |  |  |
| 歌手编号 | K1234567890 | （唯一标识） | P1 |
| 歌手名 | 宇多田光，刘德华 |  | P1 |
| 歌手标签 | &lt;arttagId&gt; |  | P1 |
| 歌手头像类型 | {S/M/L} |  | P1 |
| 歌手头像地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 合唱歌手编号 | N/A，&lt;singerId&gt;柯受良/吴宗宪 | 多人 | P1 |
| 歌手中文首字母 | YDTG，LDH |  | P1 |
| 歌手别名 | Hikaru Utada，Andy |  | P2 |
|  | 宇多田ヒカル/うただ ヒカル |  | P2 |
| 歌手昵称 | ヒッキー/Hikki，华仔 |  | P1 |
| 歌手别名中文首字母 | N/A，HZ |  | P1 |
| 作词 | 宇多田光，刘德华 |  | P2 |
| 作曲 | 宇多田光，高枫 |  | P2 |
| 伴奏 | N/A，N/A |  | P2 |
| 伴舞 | N/A，N/A |  | P2 |
| 歌手生日 | 6-14 |  | P2 |
| 歌手星座 | 白羊座，狮子座 |  | P2 |
| 歌手所获奖项 | 台湾金曲奖最佳男歌手，MTV年度最佳唱片 |  | P3 |
| 歌手风格 | &lt;songtagId&gt;摇滚 |  | P2 |
| 歌手介绍 | &lt;textInfo&gt; |  | P2 |
| 关联专辑 | &lt;albumId&gt;Array | **关联类信息** | P2 |
| 关联歌单 | &lt;sheetId&gt;Array |  | P2 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P1 |
| 关联资讯 | &lt;infoId&gt;Array |  | P3 |
| 关联三方资源 | &lt;videoId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 关联翻唱用户 | &lt;userId&gt;Array |  | P1 |
| 关联话题 | &lt;topicId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 订阅用户总数 | 268 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 658 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用 | P1 |
|  |  |  |  |
| **专辑（Album）** |  |  |  |
| 专辑编号 | Z1234567890 | （唯一标识） | P1 |
| 专辑名称 | First Love，笨小孩 |  | P1 |
| 专辑标签 | &lt;songtagId&gt; |  | P1 |
| 专辑封面类型 | {S/M/L} |  | P1 |
| 专辑封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 发行时间 | 1999-3-10，1998-11-1 |  | P2 |
| 发行公司 | EMI，上海音像公司 |  | P2 |
| 专辑介质 | 数字/CD，VCD/DVD，录像带 |  | P2 |
| 条形码 | 2009307450035 |  | P3 |
| ISRC\(中国\) | CNE029838200，N/A |  | P3 |
| 歌曲总数 | 18 |  | P1 |
| 专辑风格 | &lt;tagId&gt;民谣 |  | P1 |
| 专辑语言 | 日语/英语、国语/粤语 |  | P1 |
| 专辑时长 | 56分钟 |  | P1 |
| 专辑所获奖项 | 日本唱片协会、格莱美最佳外语专辑 |  | P3 |
| 专辑介绍 | &lt;textInfo&gt; |  | P2 |
| 关联艺术家 | &lt;artId&gt;Array | **关联类信息** | P1 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P1 |
| 关联资讯 | &lt;infoId&gt;Array |  | P3 |
| 关联三方资源 | &lt;videoId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 订阅用户总数 | 325 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 分享用户总数 | 678 |  | P2 |
| 分享用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 345 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用 | P1 |
|  |  |  |  |
| **歌单（Sheet）** |  |  |  |
| 歌单编号 | D1234567890 | （唯一标识） | P2 |
| 歌单名称 | 遇见薛子谦 |  | P2 |
| 歌单封面类型 | {S/M/L} |  | P2 |
| 歌单封面地址 | &lt;imageUrl&gt;{S} |  | P2 |
| 创建用户 | &lt;usersId&gt; |  | P2 |
| 歌曲总数 | 29 |  | P2 |
| 歌单标签 | &lt;song+diytagId&gt; |  | P2 |
| 歌单介绍 | &lt;textInfo&gt; |  | P2 |
| 关联话题 | &lt;topicId&gt;Array | **关联类信息** | P2 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 用户评论总数 | 367 | **用户类信息** | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 订阅用户总数 | 325 |  | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 分享用户总数 | 354 |  | P2 |
| 分享用户列表 | &lt;userId&gt;Array |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用 | P1 |
|  |  |  |  |
| **栏目（Section）** |  |  |  |
| 栏目编号 | C1234567890 | 唯一标识 |  |
| 栏目名称 | K歌之王串烧 |  |  |
| 栏目封面类型 | {S/M/L} |  |  |
| 栏目封面地址 | &lt;imageUrl&gt;{L} |  |  |
| 创建者 | &lt;adminId&gt; |  |  |
| 栏目介绍 | &lt;textInfo&gt; |  |  |
|  |  | 关联类信息 |  |
|  |  |  |  |
|  |  |  |  |
|  |  |  |  |

主要的的管理资源项和目标如下：

| 数据对象 | 主要管理项 | 功能项 | 实施目标 | 实施阶段 |
| :--- | :--- | :--- | :--- | :--- |
| 曲目加工 | 加工曲目文件 |  |  | P1 |
|  | 自动 |  |  |  |
| 曲目元数据 | 导入新曲目 | 通过后台导入信息表自动入库 | 由曲库管理员主动处理，技术员配合 | P1 |
|  |  | 通过增量扫描读取新曲目入库 | 由曲库管理员自动处理 | P2 |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |



