# Eternity

自己编译的美化版 **RikkaHub 2.5.3**（安卓 AI 聊天客户端），加了一堆阅读/美化向的设置。

> 基于开源项目 [rikkahub/rikkahub](https://github.com/rikkahub/rikkahub) 的 2.5.3 版本，通过补丁方式加入美化功能；源码版权归原作者。

## 下载

**[⬇️ 点这里去 Releases 下载最新 APK](https://github.com/shisan921/rikka-build/releases/latest)**

- 文件名：`app-github-universal-release.apk`（约 19 MB）
- 安装前请先卸载官方 RikkaHub（包名相同、签名不同，装不上覆盖包）
- 数据不通用，自己备份好再卸载

## 加了什么

- **颜色自定义**：用户气泡 / AI 气泡 / 聊天背景 / 输入框 / 主色调 / 正文文字色，取色盘 + 记忆色
- **透明度设置**：气泡、思维链、侧边栏元素
- **插图素材**：输入框 / 侧边栏 / 用户气泡 / AI 气泡背景图（相册选图）+ 圆角 + 遮罩 + 不透明度
- **对白样式**：引号内的文字单独上色、行级底色、实线 / 虚线 / 点线三种下划线、行首竖线，颜色和间距都能调
- **字体库**：导入的字体可以存多个，随时切换
- **阅读排版**：字号（50%–140% 连续）、行距、段落间距、字间距、头像大小、完整时间显示
- **主题基色**：给一个颜色，自动生成整套浅色/深色配色
- 自己的图标和名字：**Eternity**

## 自己编译

仓库里的 `.github/workflows/build.yml` 会：

1. 拉取上游 `rikkahub/rikkahub` 的 2.5.3（含子模块）
2. 打上 `beautify.patch`
3. 用 JDK 21 编译 release 版
4. 上传到 Actions Artifacts，并发布到 Releases

Fork 本仓库 → 打开 `Actions` → 选 `编一个我自己的 Rikka` → `Run workflow`，跑完就能在 Releases 拿到自己的包。

## 说明

- 每个版本都用自己的签名证书（存在 Actions 缓存里），所以后续版本可以直接覆盖安装
- 补丁是累计的：`beautify.patch` 里包含全部改动，直接整文件替换即可
