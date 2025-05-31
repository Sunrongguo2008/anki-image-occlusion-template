# Anki 交互式遮挡卡片模板

## 介绍

这是一款功能强大的Anki图片遮挡模板，支持在单张图片上创建多个可交互的遮挡区域，特别适用于语言学习、医学解剖、地理识图等需要记忆图片细节的场景。模板采用创新的"一卡多空"设计，让您能够逐步揭示图片中的关键信息，大幅提升记忆效率。

## 核心优势

🪄 **一卡多空 & 依次揭示**  
- 单张图片支持创建多个遮挡区域  
- 按预设顺序逐步揭示关键信息  
- 支持自定义揭示顺序和分组控制  
- 通过点击、快捷键或按钮实现精准控制  

🌐 **跨平台免插件体验**  
- **无需任何插件** - 在电脑和手机上均可直接使用  
- Anki Desktop 和 AnkiDroid **完美兼容**  
- 移动端支持完整的卡片制作和编辑功能  
- 自动适应不同屏幕尺寸和设备类型  

🖱️ **直观的编辑体验**  
- 电脑/手机端均可直接创建和编辑卡片  
- 拖拽式创建/移动遮挡区域  
- 双击编辑遮挡顺序编号  
- 右键单击删除不需要的遮挡  
- 实时显示遮挡序号和编辑状态  

⌨️ **高效操作支持**  
- `W`键：揭示下一个遮挡区域  
- `Q`键：隐藏最新揭示的遮挡区域  
- 触摸屏优化：支持长按和双击操作  
- 按钮控制：一键揭示/隐藏所有区域  

🎨 **精美视觉设计**  
- 简洁现代的UI界面  
- 清晰的遮挡层标识  
- 响应式布局适配各种设备  
- 借鉴优化了[e-chehil的quizify模板](https://github.com/e-chehil/anki-quizify)的优秀设计  

## 使用方法

### 获取模板
1. 从[Releases页面](https://github.com/Sunrongguo2008/anki-image-occlusion-template/releases)下载Deck.apkg文件
2. 导入到Anki中即可开始使用

### 查看卡片
1. 浏览时所有内容默认被遮挡  
2. 单击遮挡区域可单独查看  
3. 按`W`键按顺序揭示遮挡区域  
4. 按`Q`键重新隐藏最新揭示的区域  

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
   - 右键点击删除不需要的遮挡  
   - 双击序号修改揭示顺序（自动交换序号）  

4. **保存配置**  
   - 点击"复制遮挡区域坐标"按钮  
   - 将剪贴板内容粘贴到`Opinions`字段  
   - 退出编辑模式完成卡片制作  

## 兼容性
- ✅ Anki Desktop (2.1.50+)  
- ✅ AnkiDroid (最新版本)  

## 注意事项
1. 编辑模式仅用于卡片制作，复习时请关闭编辑模式  
2. 更换图片后需要重新设置遮挡区域  
3. 确保使用最新版Anki以获得最佳体验  

## 参与贡献
我们欢迎各种形式的贡献！如果您发现任何问题或有改进建议：
- 请提交issue与我们讨论  
- 欢迎提交pull request完善项目  

## 效果预览
桌面端正面（浅色） | 桌面端背面（浅色）
---|---
<img src="https://github.com/user-attachments/assets/7c09810c-4540-48ba-8b7a-e7114e7f7e42" > | <img src="https://github.com/user-attachments/assets/4a3a3331-49ca-411d-a19d-2213233a46c3" >
桌面端正面（深色） | 桌面端背面（深色）
<img src="https://github.com/user-attachments/assets/15d034b4-0516-4eab-a610-5ceba060013c" > | <img src="https://github.com/user-attachments/assets/98623ecb-de1b-41a1-85a9-c75d94c099d3" >
移动端正面（浅色） | 移动端背面（浅色）
<img src="https://github.com/user-attachments/assets/ea63478c-aae2-43cb-afc6-d31afbe3406f" > | <img src="https://github.com/user-attachments/assets/b96e8468-530e-4347-a652-69b2aeeb80b6" >
移动端正面（深色） | 移动端背面（深色）
<img src="https://github.com/user-attachments/assets/d3481cda-dae0-4edf-b452-06bc76a505ce" > | <img src="https://github.com/user-attachments/assets/cc0859be-8c14-41f0-b4a1-bb80ab7ac403" >
