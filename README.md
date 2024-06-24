<div align="center">

# Fortune

_🙏 今日运势 🙏_ 

### Fork From [nonebot_plugin_fortune](https://github.com/MinatoAquaCrews/nonebot_plugin_fortune)

</div>
<p align="center">

  <a href="https://github.com/ANGJustinl/nonebot_plugin_fortune/blob/master/LICENSE">
	<img src="https://img.shields.io/github/license/ANGJustinl/nonebot_plugin_fortune?color=blue">
  </a>

  <a href="https://github.com/nonebot/nonebot2">
	<img src="https://img.shields.io/badge/ANGANGBOT v3.0+-green">
  </a>

  <a href="https://github.com/ANGJustinl/nonebot_plugin_fortune/releases/tag/v0.4.12">
	<img src="https://img.shields.io/github/v/release/ANGJustinl/nonebot_plugin_fortune?color=orange">
  </a>

  <a href="https://www.codefactor.io/repository/github/ANGJustinl/nonebot_plugin_fortune">
	<img src="https://img.shields.io/codefactor/grade/github/ANGJustinl/nonebot_plugin_fortune/master?color=red">
  </a>

  <a href="https://results.pre-commit.ci/latest/github/ANGJustinl/nonebot_plugin_fortune/master">
	<img src="https://results.pre-commit.ci/badge/github/ANGJustinl/nonebot_plugin_fortune/master.svg" alt="pre-commit.ci status">
  </a>

</p>

## 版本

[v0.1](https://github.com/ANGJustinl/nonebot_plugin_fortune/releases/tag/v0.1)

⚠️ 适配nonebot2 `^2.0.0rc4`

## 安装

1. 安装方式：

   - 通过 `pip` 或 `nb` 安装：由于pypi无法发行过大安装包，由此安装的插件不包含 `resource/img` 下**所有抽签主题图片**。所有抽签主题图片资源在 [`v0.4.10 release`](https://github.com/MinatoAquaCrews/nonebot_plugin_fortune/releases/tag/v0.4.10) Assets提供，下载至本地后，更改 `FORTUNE_PATH` 配置即可；

   - 通过 `zip` 或 `git clone` 安装：包含 `resource` 下所有插件资源；

2. 抽签主题图片 `img` 、字体 `font` 、文案 `fortune` 等资源均位于 `./resource` 下，可在 `env` 中设置 `FORTUNE_PATH`；

   ```shell
   FORTUNE_PATH="your-path-to-resource"    # For example, "./my-data/fortune"，其下有img、font、fortune文件夹等资源
   ```

   ⚠️️ 插件启动时，将自动检查资源是否缺失（**除字体与图片**资源）

3. 在 `env` 下设置 `xxx_FLAG` 以启用或关闭抽签随机主题（默认全部开启），例如：

   ```shell
   AMAZING_GRACE_FLAG=false    # 奇异恩典·圣夜的小镇
   ARKNIGHTS_FLAG=true         # 明日方舟
   ASOUL_FLAG=true             # A-SOUL
   AZURE_FLAG=true             # 碧蓝航线
   DC4_FLAG=false              # dc4
   EINSTEIN_FLAG=true          # 爱因斯坦携爱敬上
   GENSHIN_FLAG=true           # 原神
   GRANBLUE_FANTASY_FLAG=true  # 碧蓝幻想
   HOLOLIVE_FLAG=true          # Hololive
   HOSHIZORA_FLAG=true         # 星空列车与白的旅行
   LIQINGGE_FLAG=true          # 李清歌
   ONMYOJI_FLAG=false          # 阴阳师
   PCR_FLAG=true               # 公主连结
   PRETTY_DERBY_FLAG=true      # 赛马娘
   PUNISHING_FLAG=true         # 战双帕弥什
   SAKURA_FLAG=true            # 樱色之云绯色之恋
   SUMMER_POCKETS_FLAG=false   # 夏日口袋
   SWEET_ILLUSION_FLAG=true    # 灵感满溢的甜蜜创想
   TOUHOU_FLAG=true            # 东方
   TOUHOU_LOSTWORD_FLAG=true   # 东方归言录
   TOUHOU_OLD_FLAG=false       # 东方旧版
   WARSHIP_GIRLS_R_FLAG=true   # 战舰少女R
   ```

   **请确保不全为 `false`，否则会抛出错误**

4. 在 `resource/fortune_setting.json` 内配置**指定抽签**规则，例如：

   ```json
   {
     "group_rule": {
       "123456789": "random",
       "987654321": "azure",
       "123454321": "granblue_fantasy"
     },
     "specific_rule": {
       "凯露": ["pcr/frame_1.jpg", "pcr/frame_2.jpg"],
       "可可萝": ["pcr/frame_41.jpg"]
     }
   }
   ```

   _group_rule会自动生成，specific_rule可手动配置_

   ⚠️ 将在 `v0.5.0` 弃用

   指定凯露签，由于存在两张凯露的签底，配置凯露签的**路径列表**即可；其余类似，**请确保图片路径、格式输入正确**！

5. 占卜一下你的今日运势！🎉

## 抽签图片及文案资源

1. [opqqq-plugin](https://github.com/opq-osc/opqqq-plugin)：原神、PCR、Hololive抽签主题；

2. 感谢江樂丝提供东方签底；

3. 东方归言录(Touhou Lostword)：[KafCoppelia](https://github.com/KafCoppelia)；

4. [FloatTech-zbpdata/Fortune](https://github.com/FloatTech/zbpdata)：其余主题签；

5. 战舰少女R(Warship Girls R)：[veadex](https://github.com/veadex)、[EsfahanMakarov](https://github.com/EsfahanMakarov)；

6. 运势文案：[KafCoppelia](https://github.com/KafCoppelia)。`copywriting.json` 整合了関係運、全体運、勉強運、金運、仕事運、恋愛運、総合運、大吉、中吉、小吉、吉、半吉、末吉、末小吉、凶、小凶、半凶、末凶、大凶及700+条运势文案！来源于Hololive早安系列2019年第6.10～9.22期，有修改。
