# 水野俊 · 个人介绍网站

一个完全**单机、离线**的中英双语个人介绍站点。双击 `index.html` 就能在浏览器打开，不需要联网、不需要服务器。

## 怎么打开

直接双击 `index.html`，或用浏览器打开任意 `.html` 文件即可。

## 目录结构

```
个人介绍网站/
├── index.html       欢迎页（入口）
├── about.html       关于我
├── experience.html  经历
├── skills.html      技能
├── interests.html   兴趣
├── game.html        兴趣·游戏
├── music.html       兴趣·音乐
├── sport.html       兴趣·运动
├── travel.html      兴趣·旅行
├── movie.html       兴趣·影视
├── contact.html     联系
├── css/styles.css  样式（配色在这里改）
├── js/main.js      文案（中英文都在这里改）
└── images/         所有照片放这里
```

## 想改文案

打开 `js/main.js`，文件最上面的 `dict` 里分 `zh`（中文）和 `en`（英文）两份。找到对应的句子直接改就行。

- 例如改「关于我」的自我介绍，搜索 `aboutP1`、`aboutP2`、`aboutP3`。
- 技能那一页目前是**占位内容**：改 `skills.html` 里 `.skill-pill` 的文字即可（编程/办公里的 Python、Word 等是直接写死在页面里的；语言/正在学那两组在 `js/main.js` 里改 `skEnglish`、`skCsbase` 等）。

## 想放照片

把图片放进 `images/` 文件夹，文件名按下面命名，后缀 `.jpg` `.png` `.jpeg` 都行，页面会自动显示：

| 位置 | 文件名 |
| --- | --- |
| 头像（关于页） | `avatar` |
| 微信二维码（联系页） | `wechat-qr` |
| 游戏截图 1~3 | `game-1` `game-2` `game-3` |
| 音乐 1~3 | `music-1` `music-2` `music-3` |
| 运动（篮球/羽毛球两张、健身一张） | `sport-1` `sport-1b` `sport-3` |
| 旅行（青岛4张、惠州4张、北京3张，其余各1张） | 青岛 `travel-7` `travel-7b` `travel-7c` `travel-7d`、惠州 `travel-6` `travel-6b` `travel-6c` `travel-6d`、北京 `travel-3` `travel-3b` `travel-3c`、广州 `travel-5`、珠海 `travel-4`、日本 `travel-1`、越南 `travel-2` |
| 影视（电影3张，番剧、短剧各1张） | 番剧 `movie-1`、短剧 `movie-2`、电影 `movie-3` `movie-3b` `movie-3c` |

> 照片没放进去时，格子里显示的是占位提示文字；放进去后图片会自动盖住提示。

## 想改配色

打开 `css/styles.css`，最上面的 `:root` 里就是全部颜色：

- `--bg` 奶白底
- `--sky` 天蓝
- `--coral` 浅珊瑚

改这几个变量即可全局生效。

## 中英切换

右上角的语言按钮切换中英文，选择会记住（存在浏览器 localStorage 里）。

## 联系信息

邮箱和微信号在 `contact.html` 里，改了记得也同步改一下 `js/main.js` 中 `emailLabel`/`wechatLabel` 旁边的说明（如有需要）。
