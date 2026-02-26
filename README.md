# Anki 图片遮挡模板（跨端交互版）

跨端图片遮挡复习模板，支持前面遮挡编辑、正反面缩放和平移手势，无需插件即可在 Anki Desktop 和移动端使用。

## 快速开始

1. 从 [Releases 页面](https://github.com/Sunrongguo2008/anki-image-occlusion-template/releases) 下载 `Deck.apkg`。
2. 在 Anki 中导入牌组。
3. 新建卡片并填写字段（至少 `Question + Image`，如需遮挡还需 `Opinions`）。

## 字段说明

| 字段 | 是否必填 | 用途 | 正面（front） | 背面（back） |
| --- | --- | --- | --- | --- |
| `Deck` | 建议 | 显示牌组路径信息 | 显示 | 显示 |
| `Question` | 建议 | 题干文本 | 显示 | 显示 |
| `Image` | 必填 | 图片主体（遮挡与缩放对象） | 显示 | 显示 |
| `Opinions` | 遮挡卡必填 | 遮挡坐标串 | 读取并渲染遮挡 | 不显示遮挡编辑 |
| `Answer` | 可选 | 答案文本 | 不显示 | 显示 |
| `Tags` | 可选 | 标签 chip | 显示 | 显示 |
| `Note` | 可选 | 备注内容 | 不显示 | 显示（带提示） |

`Opinions` 固定格式：

```text
x%,y%,w%,h%,order;x%,y%,w%,h%,order;...
```

示例：

```text
12.50,20.00,18.00,10.00,1;41.20,58.10,22.80,9.50,2
```

## 正面（front）使用说明

### 复习模式

- 点击遮挡块：单独切换该遮挡显示/隐藏。
- `W`：揭示下一个遮挡（按序号）。
- `Q`：隐藏最近一次揭示的遮挡。
- 按钮或快捷键 `+/-`：缩放图片。
- 手势：双指缩放、单指平移（桌面端可鼠标拖动平移）。

### 编辑模式

1. 点击 `开启编辑模式`（再次点击可退出）。
2. 在图片上拖拽创建新遮挡。
3. 拖动遮挡可移动位置。
4. 桌面端右键遮挡可删除。
5. 双击遮挡序号可修改顺序号。
6. 点击 `复制遮挡坐标`，将结果粘贴到 `Opinions` 字段。

说明：

- front 保留三个主按钮：`开启编辑模式`、`复制遮挡坐标`、`揭示下一个遮挡`。
- front 图片区右下有固定 `+/-` 缩放按钮。
- front 在编辑模式下会禁用图片手势，避免与遮挡编辑冲突。

## 背面（back）使用说明

- 显示内容：`Deck`、`Question`、图片区、`Answer`、`Tags`、`Note`（若有）。
- `Note` 存在时会先显示提示：`往下滑动查看笔记`。
- 背面底部仅保留 `+/-` 缩放控件，不提供遮挡编辑。
- 支持按钮/快捷键缩放，支持双指缩放与单指平移。

## 缩放与手势规则

- 缩放按钮：图片区右下角固定 `-` 与 `+`。
- 缩放快捷键：
  - 放大：`+` / `=` / `NumpadAdd`
  - 缩小：`-` / `_` / `NumpadSubtract`
- 最小缩放倍数：`0.3`（相对默认适配）。
- 不设代码级最大缩放上限（实际受设备渲染能力限制）。

## 快捷键总表

| 页面 | 快捷键 | 功能 |
| --- | --- | --- |
| front | `W` | 揭示下一个遮挡 |
| front | `Q` | 隐藏最近揭示遮挡 |
| front | `+ / = / NumpadAdd` | 放大图片 |
| front | `- / _ / NumpadSubtract` | 缩小图片 |
| back | `+ / = / NumpadAdd` | 放大图片 |
| back | `- / _ / NumpadSubtract` | 缩小图片 |

## 兼容性与页面行为

- ✅ Anki Desktop（2.1.50+）
- ✅ AnkiDroid（最新版）
- front 为固定页，不允许纵向滚动。
- back 允许纵向滚动，用于查看下方答案/笔记。

## 常见问题（FAQ）

1. `+/-` 快捷键无反应怎么办？
   - 先点击一次卡片内容区，再按快捷键。
2. 更换了图片后遮挡错位？
   - 需要重建遮挡并重新覆盖 `Opinions`。
3. 放大后卡顿正常吗？
   - 可能出现，属于设备渲染性能上限表现。
4. 遮挡位置与图片不一致？
   - 优先检查 `Opinions` 是否为最新复制结果，格式是否为 `x%,y%,w%,h%,order;...`。

## 效果预览

> 以下截图资源暂保留，截图待更新到新布局（文案已更新）。

桌面端正面（浅色） | 桌面端背面（浅色）
---|---
<img src="https://github.com/user-attachments/assets/7c09810c-4540-48ba-8b7a-e7114e7f7e42" > | <img src="https://github.com/user-attachments/assets/4a3a3331-49ca-411d-a19d-2213233a46c3" >
桌面端正面（深色） | 桌面端背面（深色）
<img src="https://github.com/user-attachments/assets/15d034b4-0516-4eab-a610-5ceba060013c" > | <img src="https://github.com/user-attachments/assets/98623ecb-de1b-41a1-85a9-c75d94c099d3" >
移动端正面（浅色） | 移动端背面（浅色）
<img src="https://github.com/user-attachments/assets/3a879c28-80f1-4522-9a26-f65608fb33c9" > | <img src="https://github.com/user-attachments/assets/21cf3f54-1f3f-490b-8e5c-1bcad6f4769b" >
移动端正面（深色） | 移动端背面（深色）
<img src="https://github.com/user-attachments/assets/729ed8d9-97c0-429a-b4a2-1642495fd6b2" > | <img src="https://github.com/user-attachments/assets/c774cc0c-54a2-448f-bf98-ba9d94e584eb" >


## 参与贡献

- 提交 Issue 反馈问题或建议。
- 提交 Pull Request 改进模板。

## 致谢

- [ikkz/anki-template](https://github.com/ikkz/anki-template)
- [e-chehil/anki-quizify](https://github.com/e-chehil/anki-quizify)
