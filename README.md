# Recognizer
## ARKit SpriteKit IOS

IOS 11.4+

## 功能
(1) 实现一个扫码的功能，能够识别图片中的字母数字组合。

(2) 实现一个动物识别功能，将摄像头对准动物图片时，程序能判断出是什么动物。

(3) 实现一个打怪物的游戏，在手机屏幕上出现一些怪物，与真实场景互动，点击屏幕可以攻击怪物，并作出响应（声音、画面等）。

启动动画：包含两个图标，相机和放大镜的移动，以及背景的颜色和透明度变化

——通过在AppDelegate中添加一个函数，在进入主界面之前先调用动画页面，动画完成之后再进入主界面。

主界面：包含一个app图标和一个滑动解锁的标签，添加了右划手势识别，标签上添加了动画实现滑动高亮效果。

——使用CAGradientLayer和CABasicAnimation来实现该动画效果。

相机界面：左下角右下角两个switch按钮，控制相机的三种模式，中间是一个添加按钮，能够在识别到动物的时候添加动物图标，最上方是相机参数提示框。

——扫码：类似于popcode，本程序通过识别图片ARImage的形式实现这个功能。

——扫动物：使用了CoreML框架，应用了一个mlmodel，该模型主要功能是识别图片中的主要物体，实现了实时对相机拍摄到的物体进行识别并且返回结果。

——打怪物：场景中会随机生成怪物，通过在场景中随机生成Anchor来实现，并且通过SKAciton赋予了动物动画以及打击时播放声音，通过AVFoundation中的AVAudioPlayer来播放背景音乐。

相机参数界面：提示当前识别到的东西和一些其它参数。

场景构建：主要用于游戏模式随机在场景中生成怪物

## 效果图：

启动动画

![](https://github.com/chenzhengang/Recognizer/blob/master/image/启动动画.png)

滑动开启

![](https://github.com/chenzhengang/Recognizer/blob/master/image/滑动开启.png)

popcode

![](https://github.com/chenzhengang/Recognizer/blob/master/image/popcode.png)

检测动物

![](https://github.com/chenzhengang/Recognizer/blob/master/image/检测动物.png)

打怪兽

![](https://github.com/chenzhengang/Recognizer/blob/master/image/打怪兽.png)

