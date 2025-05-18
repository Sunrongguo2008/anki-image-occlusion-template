# Anki 交互式遮挡卡片模板
⚠️我本人编程能力有限，因此用了Claude3.7辅助编写，可能会有bug（反正目前我没发现bug），强烈欢迎Issues和PR为项目做贡献~~帮我~~。
## 介绍
这是一个增强型Anki图片遮挡模板，允许用户在图片上创建多个可交互的矩形遮挡区域。特别适用于语言学习、医学解剖等需要记忆图片细节的场景。

## 特色功能
📱 **跨平台兼容**  
- 不需要使用插件维持运转
- 可以在AnkiDroid移动端制作/修改卡片！
- 自动处理不同屏幕尺寸  
- 触摸操作优化（长按/双击）

✅ **智能遮挡系统**  
- 支持依次揭示遮挡（点击遮挡、键盘快捷键、点击按钮）
- 支持自定义揭示顺序
- 可创建多个矩形遮挡层
- 揭示/隐藏单个或多个遮挡区域

✏ **可视化编辑**  
- 电脑端Anki/Ankidroid均可直接制卡
- 拖拽创建/移动遮挡
- 右键删除/双击编辑序号
- 实时显示遮挡顺序编号

🎨 **漂亮的外观**  
- 借鉴~~偷走~~了[e-chehil的quizify模板](https://github.com/e-chehil/anki-quizify)
- ~~有些冗余代码没有删干净~~

## 使用方法
⌨️ **快捷键支持**  
- `W`键：揭示下一个遮挡  
- `Q`键：隐藏最新揭示的遮挡  


### 查看卡片
1. 正常浏览时所有内容被遮挡
2. 单击遮挡区域可查看
3. 按`W`键顺序揭示遮挡
4. 按`Q`键重新隐藏最新揭示的区域

### 制作/修改卡片
1. **准备阶段**  
   - 将图片粘贴到卡片image字段，创建卡片

2. **创建遮挡**  
   - 点击"预览"预览卡片
   - 点击"开启创建遮挡"进入编辑模式  
   - 在图片上拖拽绘制矩形区域  
   - 自动生成带序号的遮挡层  

3. **调整设置**  
   - 拖拽移动现有遮挡位置  
   - 右键点击删除不需要的遮挡  
   - 双击序号修改揭示顺序（自动交换序号）  

4. **保存配置**  
   - 点击"复制遮挡区域坐标"按钮  
   - 将剪贴板内容粘贴到`Opinions`字段  
   - 退出编辑模式完成制作  

> 💡 提示：遮挡坐标以图片百分比存储，确保在不同设备上显示一致

## 兼容性
- Anki Desktop (2.1.50+)  
- AnkiDroid (最新版)

## 注意事项
1. 编辑模式仅用于编辑，编辑模式下无法正常复习卡片。复习需要关闭编辑模式。
2. 修改图片后需要重新设置遮挡

## 反馈
- 本人编程能力有限，强烈欢迎PR为项目做贡献~~帮我~~
- 欢迎开issue讨论

## 截图
<img src="https://github.com/user-attachments/assets/ad92706a-a09c-4d5c-bbb5-127b793af87b"/>
<img src="https://github.com/user-attachments/assets/5c47f48a-2a84-41b9-ace2-c678c8f70e5b"/>
<img src="https://github.com/user-attachments/assets/adc6c5e5-03ce-4ec0-b199-c2015918703b" width="400px" />
<img src="https://github.com/user-attachments/assets/eca604c4-9159-45cb-86bd-5c94e4d2c809" width="400px" />
<img src="https://github.com/user-attachments/assets/953755f6-a208-4b61-b4e6-107c64935542" width="400px" />
<img src="https://github.com/user-attachments/assets/1c26fec2-3bad-4d6a-b36f-d101f63b4a7e" width="400px" />
