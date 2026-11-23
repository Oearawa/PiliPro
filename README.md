# PiliPro

基于 [dev4harmony/PiliPlus](https://github.com/dev4harmony/PiliPlus) 改的一个鸿蒙（HarmonyOS NEXT）第三方客户端自用版。

平时在鸿蒙设备上用 PiliPlus 看高码率视频或者赶上线路抽风时，偶尔会加载偏慢，所以把 [Bilibili-thread-ripper](https://github.com/MrTangLuyao/Bilibili-thread-ripper) 的多线程并发拉流思路合了进来，顺手改了独立名字和包名发出来，有同样需求的可以直接拿去用。

## 和原版有什么区别

- **内置多线程拉流加速**：整合了并发拉流模块，可以在设置里随时开关，用来改善部分场景下起播慢、缓冲卡顿的问题。
- **独立包名，可与原版共存**：应用包名改为了 `com.oearawa.pilipro`，桌面直接显示 `PiliPro`，和原版 PiliPlus 互不冲突，导出和备份文件前缀也做了隔离。
- **紧跟上游同步**：主体功能和鸿蒙端适配都跟随 `dev4harmony/PiliPlus` 更新，不额外魔改界面。

## 下载与安装

1. 前往 [Releases](https://github.com/Oearawa/PiliPro/releases) 页面下载最新版本的 `-unsigned.hap` 安装包。
2. 由于发布的是未签名包，需要自行签名后再安装到鸿蒙设备上。
3. 每个版本都附带了 `SHA256SUMS.txt`，下载后可按需核对文件完整性。

## 一些说明

- 本项目以自用为主，有空会跟着上游不定期同步更新。
- 如果开启多线程拉流后遇到播放或拖动异常，可以先在设置里关掉该选项对比排查；确认是加速模块引起的问题欢迎提 Issue 反馈。
- 涉及原版通用功能或特定机型适配的问题，建议优先关注上游仓库的进展。

## 致谢

感谢以下开源项目：

- [dev4harmony/PiliPlus](https://github.com/dev4harmony/PiliPlus)（鸿蒙端适配上游）
- [MrTangLuyao/Bilibili-thread-ripper](https://github.com/MrTangLuyao/Bilibili-thread-ripper)（多线程拉流加速方案）

## 开源协议

延续上游协议，本项目基于 [GPL-3.0](LICENSE) 开源。
