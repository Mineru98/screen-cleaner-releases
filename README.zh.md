<p align="center">
  <img src="assets/thumbnail.svg" alt="ScreenCleaner" width="100%"/>
</p>

<p align="center">
  <a href="README.md">English</a> &nbsp;|&nbsp; <a href="README.ko.md">한국어</a> &nbsp;|&nbsp; <a href="README.ja.md">日本語</a> &nbsp;|&nbsp; <b>简体中文</b>
</p>

<br/>

# ScreenCleaner

## 为什么要做这个应用

说真的，MacBook 的屏幕真的会脏。

鼓起勇气拿起擦布，结果手碰到键盘，标签页飞走了，文件名变成了"哈哈哈哈"，B站突然开始放视频……

最后不是在擦屏幕，而是花了 5 分钟收拾残局。

屏幕还是脏的。

macOS 没有清洁模式，所以我做了一个。

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

### 清洁模式中可用的按键

清洁模式下，只有以下三个键有效，其余所有按键均被屏蔽。

| 按键 | 功能 |
|------|------|
| `F1` | 降低屏幕亮度 |
| `F2` | 提高屏幕亮度 |
| `ESC`（按住 5 秒） | 取消清洁并恢复所有设置 |

> 单击 ESC 不会有任何反应，需要持续按住 5 秒才能退出。

---

## 功能特性

- 通过 `CGEventTap` 实现系统级键盘阻止 — 任何输入都无法通过
- 使用黑色遮罩将屏幕调暗，清洁时污渍更清晰可见
- 崩溃安全：即使应用意外退出，屏幕亮度也会自动恢复
- 极简 UI — 只有计时器和按钮，简洁明了
- 常驻菜单栏，需要时随时调用
