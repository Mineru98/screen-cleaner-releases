<p align="center">
  <img src="assets/thumbnail.svg" alt="ScreenCleaner" width="100%"/>
</p>

<p align="center">
  <a href="README.md">English</a> &nbsp;|&nbsp; <a href="README.ko.md">한국어</a> &nbsp;|&nbsp; <a href="README.ja.md">日本語</a> &nbsp;|&nbsp; <b>简体中文</b>
</p>

<br/>

# ScreenCleaner

> *你拿起了擦布，开始擦拭屏幕。然而 — 窗口突然飞走了，音乐开始大声播放，更糟糕的是，一封写了一半的邮件发送给了你的老板。*
>
> *这个场景是不是很熟悉？*

---

## 为什么要做这个应用

一切总是以同样的方式开始。

坐在桌前，你突然注意到它 — 那个污渍。那个在你的 MacBook 屏幕上悄悄生长了好几周的指纹、灰尘和不明痕迹组成的"星座"。每次视频通话时，它总是以最糟糕的角度反射光线。

于是你拿起超细纤维布，向前倾身，开始擦拭。

就在那一刻，MacBook 背刺了你。

手掌扫过键盘。一连串按键触发：标签页切换了，文件被重命名了，半写好的邮件发送出去了。你手忙脚乱地撤销操作，等你回过神来，擦布被遗忘在桌上，而那个污渍依然在原地 — 嘲笑着你。

问题不在于擦布。问题在于 **MacBook 没有"清洁模式"**。

这就是 ScreenCleaner 诞生的原因。

---

## 这个应用做什么

**ScreenCleaner** 是一个小巧的 macOS 菜单栏应用，只专注于一件事：让你在安全的时间窗口内擦拭屏幕，不会发生任何意外。

点击**开始清洁**后：

- **在系统层面阻止所有键盘输入** — 无论你怎么按键盘，都不会有任何输入
- **将屏幕调暗为黑色**，让每个污渍和划痕清晰可见
- **倒计时计时器**（1、3、5、10 分钟或自定义）帮你管理清洁时间

计时器结束后，一切恢复原样。屏幕干净，毫无混乱。

---

## 安装方法

### Homebrew（推荐）

```bash
brew tap Mineru98/tap
brew install --cask screen-cleaner
```

### 手动安装

1. 从 [Releases](https://github.com/Mineru98/screen-cleaner-releases/releases) 下载最新的 `.dmg` 文件
2. 打开 `.dmg`，将 **ScreenCleaner.app** 拖入 `/Applications`
3. 启动应用，按提示授予**辅助功能**权限

---

## 系统要求

| | |
|---|---|
| **macOS** | 14 Sonoma 或更高版本 |
| **权限** | 辅助功能（键盘阻止所需） |
| **架构** | Apple Silicon 和 Intel |

---

## 使用方法

1. 从应用程序或菜单栏启动 **ScreenCleaner**
2. 首次启动时授予**辅助功能**权限
3. 选择计时器预设 — **1 / 3 / 5 / 10 分钟** — 或输入自定义时长
4. 点击**开始清洁**
5. 自由擦拭屏幕
6. 计时器结束后，所有设置自动恢复

### 紧急退出

清洁过程中改变主意了？**按住 ESC 键 5 秒**即可立即退出。

---

## 功能特性

- 通过 `CGEventTap` 实现系统级键盘阻止 — 任何输入都无法通过
- 使用黑色遮罩将屏幕调暗，清洁时污渍更清晰可见
- 崩溃安全：即使应用意外退出，屏幕亮度也会自动恢复
- 极简 UI — 只有计时器和按钮，简洁明了
- 常驻菜单栏，需要时随时调用

---

## 源代码

完整源代码托管于 [Mineru98/screen-cleaner](https://github.com/Mineru98/screen-cleaner)。

---

## 许可证

[MIT](https://github.com/Mineru98/screen-cleaner/blob/main/LICENSE)
