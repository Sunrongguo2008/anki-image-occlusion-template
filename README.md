# Anki 图片遮挡模板（跨端交互版）

跨端图片遮挡复习模板，支持前面遮挡编辑、正反面缩放和平移手势，**无需插件**即可在 Anki Desktop 和移动端使用。

## 效果预览

桌面端正面（浅色） | 桌面端背面（浅色）
---|---
<img src="https://github.com/user-attachments/assets/69d6f1b6-7db9-4e3c-81d0-542f4d098a35" > | <img src="https://github.com/user-attachments/assets/c1619ebe-2de6-47bb-92d1-661576daa3f0" >
桌面端正面（深色） | 桌面端背面（深色）
<img src="https://github.com/user-attachments/assets/6662da1d-ef03-4624-9fd7-5cdcb2c54daa" > | <img src="https://github.com/user-attachments/assets/ed963dc0-693f-4c4e-b1e3-7dc4a7c58e94" />
移动端正面（浅色） | 移动端背面（浅色）
<img src="https://github.com/user-attachments/assets/3a879c28-80f1-4522-9a26-f65608fb33c9" > | <img src="https://github.com/user-attachments/assets/21cf3f54-1f3f-490b-8e5c-1bcad6f4769b" >
移动端正面（深色） | 移动端背面（深色）
<img src="https://github.com/user-attachments/assets/729ed8d9-97c0-429a-b4a2-1642495fd6b2" > | <img src="https://github.com/user-attachments/assets/c774cc0c-54a2-448f-bf98-ba9d94e584eb" >

## 快速开始

### 获取模板
1. 从[Releases页面](https://github.com/Sunrongguo2008/anki-image-occlusion-template/releases)下载Deck.apkg文件
2. 导入到Anki中

### 查看卡片
1. 浏览时所有内容默认被遮挡  
2. 单击遮挡区域可单独查看  
3. 按`W`键或者按`揭示下一个遮挡`按钮可按顺序揭示遮挡区域  
4. 按`Q`键重新隐藏最新揭示的区域
5. 按`+`/`-`或者手指捏合放大/缩小图像
6. 图片大小>显示区域时，拖动图片可移动图片位置

### 制作/修改卡片

1. **准备阶段**  
   - 将图片粘贴到卡片image字段  
   - 创建新卡片  

2. **创建遮挡区域**  
   - 点击"预览"按钮预览卡片  
   - 点击"开启创建遮挡"进入编辑模式  
   - 在图片上拖拽绘制矩形遮挡区域  
   - 自动生成带有序号的遮挡层  

3. **调整设置**  
   - 拖拽移动现有遮挡位置  
   - 右键点击（桌面端）或者长按（移动端）删除不需要的遮挡  
   - 双击序号修改揭示顺序 

4. **保存配置**  
   - 点击"复制遮挡区域坐标"按钮，并手动复制文本框内的片段  
   - 退出预览模式，将剪贴板内容粘贴到`Opinions`字段  
   - 退出编辑模式完成卡片制作  

## 字段说明

| 字段 | 是否必填 | 用途 | 正面（front） | 背面（back） |
| --- | --- | --- | --- | --- |
| `Deck` | Anki自动填充 | 显示牌组路径信息 | 显示 | 显示 |
| `Question` | 建议 | 题干文本 | 显示 | 显示 |
| `Image` | 必填 | 图片主体（遮挡与缩放对象） | 显示 | 显示 |
| `Opinions` | 据指南必填 | 遮挡坐标串 | 读取并渲染遮挡 | 不显示遮挡编辑 |
| `Answer` | 可选 | 答案文本 | 不显示 | 显示 |
| `Tags` | 可选 | 标签 chip | 显示 | 显示 |
| `Note` | 可选 | 备注内容 | 不显示 | 显示（带提示） |

`Opinions` 固定格式（不了解不影响使用）：

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
- ❓ AnkiMobile（不知道啊，我没苹果手机。用的请在[Issue](https://github.com/Sunrongguo2008/anki-image-occlusion-template/issues)上回答一下我能不能用）
- front 为固定页，不允许纵向滚动。
- back 允许纵向滚动，用于查看下方答案/笔记。

## 常见问题（FAQ）

1. ~~`+/-` 快捷键无反应怎么办？~~（应该已修复）
   - ~~先点击一次卡片内容区，再按快捷键。~~
2. 更换了图片后遮挡错位？
   - 需要重建遮挡并重新覆盖 `Opinions`。
3. 放大后卡顿正常吗？
   - 可能出现，属于设备渲染性能上限表现。
4. 遮挡位置与图片不一致？
   - 优先检查 `Opinions` 是否为最新复制结果，格式是否为 `x%,y%,w%,h%,order;...`，尝试重建遮挡并重新覆盖 `Opinions`。

## 参与贡献

- 提交 [Issue](https://github.com/Sunrongguo2008/anki-image-occlusion-template/issues) 反馈问题或建议。
- 提交 [Pull Request](https://github.com/Sunrongguo2008/anki-image-occlusion-template/pulls) 改进模板。

## 致谢

- [ikkz/anki-template](https://github.com/ikkz/anki-template)
- [e-chehil/anki-quizify](https://github.com/e-chehil/anki-quizify)
