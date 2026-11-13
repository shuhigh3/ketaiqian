# 课态签（ketaiqian）

一款大学生自用辅助应用：课表查询与上课提醒、按课表自动改微信状态、每晚自动查寝签到、
学习通/知到的自动刷课与刷题。只在自己的账号与本机上使用。

本仓库只放**安装包与版本清单**，供应用内「检查更新」使用；源码不在这里。

## 下载安装

最新版：<https://github.com/shuhigh3/ketaiqian/releases/latest>

- 首次安装需要在系统里给「课态签」打开「安装未知应用 / 允许来自此来源」。
- 从 1.16.1 起是固定签名（同一把 keystore），之后的版本可以直接覆盖安装，课表、登录态、设置都保留。
- 早期 debug 签名包与本包签名不同，只能卸载重装一次。

## 更新清单

`version.json`（仓库根目录）：

```json
{
  "versionCode": 47,
  "versionName": "1.16.1",
  "apkUrl": "https://github.com/shuhigh3/ketaiqian/releases/download/v1.16.1/ketai-1.16.1.apk",
  "notes": "新增「检查更新」：读这份文件、下载新包并覆盖安装"
}
```

应用里右上角三点 → 检查更新 → 填清单地址（填一次会记住）：

- 国内网络优先：<https://fastly.jsdelivr.net/gh/shuhigh3/ketaiqian@main/version.json>
- GitHub 原始链接：<https://raw.githubusercontent.com/shuhigh3/ketaiqian/main/version.json>
  （部分网络下不可达，会报「连接超时」）

## 每次发版

1. 改 `versionCode` / `versionName`（两个都加一），出 release 包；
2. 新建 Release，tag 用 `v<版本号>`，上传安装包并把资产名写成 `ketai-<版本号>.apk`；
3. 更新本文件所在仓库的 `version.json` 四项；
4. 手机上检查更新 → 下载并安装。

安装包在交给系统安装器前会自检包名、版本号与签名，三项都对才允许安装。
