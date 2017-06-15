# 三方资源管理

主要处理所有引入的第三方音视频内容的上下架增删改查管理，以及从属版块和栏目的增删改查管理

### 三方资源标准数据与要求如下：

| 数据字段 | 使用示例与规格 | 所属对象 | 阶段 |
| :--- | :--- | :--- | :--- |
| 编码格式 | UTF-8，GB18030 | 字符集规范 | P1 |
| 防盗链验证 | Y/N | 白名单，域名/地区/平台/版本 | P2 |
| 原始创建时间 | 2017-04-15 01:15:43 |  | P1 |
| 最后更新时间 | 2017-05-15 01:15:46 |  | P1 |
| 最后缓存更新时间 | 2017-06-15 01:15:51 |  | P1 |

| **视频（Video）** |  |  |  |
| 文件编号 | T1234567890 | （唯一标识） | P1 |
| 原文件名 | S1234567890 | 合名（唯一性） | P1 |
| MD5 | 11AFAD2D3555EAB7F251A05C0B7915F9 | 散列函数（资源文件校验） | P2 |
| SHA1 | A48A9D261882A3AF795E4A9CECC47E8EA098EA7E | 数字签名（资源文件校验） | P2 |
| CRC32 | 5DB7252F | 循环冗余效验程序库（资源文件校验） | P2 |
| 文件类别编号 | 15，16 |  | P1 |
| 文件地址 | &lt;sousUrl&gt;Array | CDN-Url | P1 |
| 资源时长 | 225s |  | P1 |
| 资源标签 | &lt;tagId&gt;儿童 |  | P1 |
| 资源类型 | 广场舞 |  | P1 |
| 资源语言 | 英语、国语 |  | P1 |
| 关联教师 | &lt;teacherId&gt;李小萌 | **关联类信息** | P1 |
| 关联章节 | &lt;chapterId&gt; |  | P2 |
| 关联课程 | &lt;classId&gt; |  | P2 |
| 关联类别 | &lt;categoryId&gt;Array |  | P2 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P2 |
| 订阅用户总数 | 235 | **用户类信息** | P1 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P1 |
| 分享用户总数 | 98 |  | P1 |
| 分享用户列表 | &lt;userId&gt;Array |  | P1 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 供应机构 | &lt;agencyId&gt;歌者盟|  |  |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，供应机构，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P2 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** | P1 |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |

| **教师（Teacher）** |  |  |  |
| 教师编号 | T1234567890 | （唯一标识） | P1 |
| 教师名 | 李小萌 |  | P1 |
| 教师标签 | &lt;arttagId&gt; |  | P1 |
| 教师头像类型 | {S/M/L} |  | P1 |
| 教师头像地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 教师中文首字母 | LXM |  | P1 |
| 所属机构 | &lt;textInfo&gt; |  | P2 |
| 教师介绍 | &lt;textInfo&gt; |  | P2 |
| 关联课程 | &lt;albumId&gt;Array | **关联类信息** | P2 |
| 关联三方资源 | &lt;songId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 关联话题 | &lt;topicId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 订阅用户总数 | 268 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |

| **机构（Agency）** |  |  |  |
| 机构编号 | A1234567890 | （唯一标识） | P1 |
| 机构名 | 歌者盟，KEEP |  | P1 |
| 机构标签 | &lt;agencyId&gt; |  | P1 |
| 机构标识类型 | {S/M/L} |  | P1 |
| 机构标识地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 机构中文首字母 | GZM |  | P1 |
| 机构介绍 | &lt;textInfo&gt; |  | P2 |
| 关联课程 | &lt;classId&gt;Array | **关联类信息** | P2 |
| 关联教师 | &lt;teacherId&gt;Array |  | P2 |
| 关联三方资源 | &lt;songId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 关联话题 | &lt;topicId&gt;Array |  | P2 |
| 关联小组 | &lt;groupId&gt;Array |  | P2 |
| 订阅用户总数 | 268 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 345 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |


| **章节（Chapter）** |  |  |  |
| 章节编号 | C1234567890 | （唯一标识） | P1 |
| 章节名称 | 上手臂练习，唱法技巧1 |  | P1 |
| 章节标签 | &lt;songtagId&gt; |  | P1 |
| 章节封面类型 | {S/M/L} |  | P1 |
| 章节封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 课程时间 | 2017-06-16 02:00:09 |  | P2 |
| 资源总数 | 18 |  | P1 |
| 章节时长 | 56分钟 |  | P1 |
| 章节介绍 | &lt;textInfo&gt; |  | P2 |
| 关联教师 | &lt;teacherId&gt;Array | **关联类信息** | P1 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P1 |
| 关联机构 | &lt;agencyId&gt;Array |  | P1 |
| 关联三方资源 | &lt;songId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 订阅用户总数 | 325 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 分享用户总数 | 678 |  | P2 |
| 分享用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 345 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P1 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** |  |

| **课程（Class）** |  |  |  |
| 课程编号 | C1234567890 | （唯一标识） | P1 |
| 课程名称 | 瑜伽分体式，腹肌锻炼 |  | P1 |
| 课程标签 | &lt;songtagId&gt; |  | P1 |
| 课程封面类型 | {S/M/L} |  | P1 |
| 课程封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 课程时间 | 2017-06-16 02:00:09 |  | P2 |
| 章节总数 | 18 |  | P1 |
| 课程总时长 | 56分钟 |  | P1 |
| 课程介绍 | &lt;textInfo&gt; |  | P2 |
| 关联教师 | &lt;teacherId&gt;Array | **关联类信息** | P1 |
| 关联栏目 | &lt;sectionId&gt;Array |  | P1 |
| 关联机构 | &lt;agencyId&gt;Array |  | P1 |
| 关联三方资源 | &lt;songId&gt;&lt;ticketId&gt;&lt;perpId&gt;Array |  | P2 |
| 订阅用户总数 | 325 | **用户类信息** | P2 |
| 订阅用户列表 | &lt;userId&gt;Array |  | P2 |
| 分享用户总数 | 678 |  | P2 |
| 分享用户列表 | &lt;userId&gt;Array |  | P2 |
| 用户评论总数 | 345 |  | P2 |
| 用户评论 | &lt;ctnId&gt;userId+textInfo+time+likeNum+reId |  | P2 |
| 上下架状态 | Y/N | **业务类信息** | P1 |
| 推荐状态 | Y/N |  | P1 |
| 版权信息 | &lt;copyrightInfo&gt;Array | 分地域，版权公司，渠道/平台/版本 | P1 |
| 付费信息 | &lt;payInfo&gt;Array | 会员/单付/试用，渠道/平台/版本，生效时间周期 | P1 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** |  |

| **类别（Category）** |  |  |  |
| 类别编号 | C1234567890 | （唯一标识） | P1 |
| 类别名称 | 广场舞，运动健身 |  | P1 |
| 类别封面类型 | {S/M/L} |  | P1 |
| 类别封面地址 | &lt;imageUrl&gt;{S} |  | P1 |
| 课程总数 | 18 |  | P1 |
| 关联栏目 | &lt;sectionId&gt;Array | **关联类信息** | P1 |

| **栏目（Section）** |  |  |  |
| 栏目编号 | C1234567890 | 唯一标识 | P1 |
| 栏目名称 | 交谊舞，歌唱发音练习 |  | P1 |
| 栏目封面类型 | {S/M/L} |  | P1 |
| 栏目封面地址 | &lt;imageUrl&gt;{L} |  | P1 |
| 创建者 | &lt;adminId&gt; |  | P1 |
| 栏目介绍 | &lt;textInfo&gt; |  | P1 |
| 关联内容 | &lt;song/art/album/sheet-Id&gt;Array | **关联类信息** | P1 |
| 开关状态 | Y/N | **业务类信息** | P1 |
| 上下架时间周期 | 2017-04-01 00:00至2017-06-30 23:59 | 自动上下架 | P2 |
| 调用类数据 | &lt;userId+view+play+down+pay+like+coms+re&gt; | **数据系统引入** | P1 |
| 搜索系数 | &lt;x-y-z&gt; |  | P1 |
| 推荐系数 | &lt;x-y-z&gt; | **推荐系统引入** | P2 |


### 资源文件类型如下：

| 文件类别 | 类别编号 | 文件所属业务 | 平台 | 阶段 |
| :--- | :--- | :--- | :--- | :--- |
| 视频 | 34 | 标清 | TV |  |
|  | 35 | 高清 | TV |  |
|  | 36 | 4K | TV |  |
|  | 44 新 | 标清 | Phone |  |
|  | 45 新 | 高清 | Phone |  |
|  |  |  |  |  |
| 音频 | 47 新 | 音频原唱 | Phone |  |
|  | 48 新 | 电视旧版音频原唱 | TV |  |
|  |  |  |  |  |

### 视频编解码格式要求如下：

| 类别编号 | 分辨率 | 帧数/s | 码率 | 码率模式 | 格式 | 编码器 | 规格 | 级别 | 容器 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 36 | 3840x2160 | 20000K | 平均 | H.264 | x.264 High5.1 |  |  | MP4 |
| 35 | 1920x1080 | 25 | 5000K | 平均 | H.264 | x.264 High4.0 | High | 4.0 | MP4 |
| 45 新 | 1920x1080 | 25 | 5000K | 平均 | H.264 | x.264 High4.0 |  |  | MP4 |
| 34 | 720x404 | 25 | 3000K | 平均 | H.264 | x.264 High4.0 |  |  | MP4 |
| 44 新 | 720x404 | 25 | 3000K | 平均 | H.264 | x.264 High4.0 | Main | 4.0 | MP4 |

### 音频编解码格式要求如下：

| 文件编号 | 音频 | 采样率 | 码率 | 码率模式 | 编码器 | 格式 | 声道 | 容器 |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 34，35，36 |  | 44100Hz | 96K | VBR | Nero Encoder | LC-AAC | Stereo | MP4 |
| 44，45 新 |  | 44100Hz | 96K | VBR | Nero Encoder | LC-AAC | Stereo | MP4 |
| 47，48 新 |  | 44100Hz | 128K | CBR | LAME MP3 | MP3 | Stereo | MP3 |
