# iOS 图片资源的各种尺寸

横竖屏高宽比的计算是建立在 iPad 支持横竖屏切换，iPhone 不支持横竖屏切换的基础上。

## 分辨率

| 机型 | 比例 | 对角线(英寸) | 分辨率(pixels) | 竖屏比例 | 横屏比例 |
|:--------:| -------- | -------- |:--------:|:--------| :--------|
| iPhone | 1x | | 320 x 480  | 1.5 |
| iPhone 4/4s | 2x | 3.5 | 640 x 960 | 1.5 |
| iPhone 5/5s | 2x | 4 | 640 x 1136 | 1.775 |
| iPhone 6/6s/7/8	| 2x | 4.7 | 750 x 1334 | 1.778 |
| iPhone 6+/6s+/7+/8+ | 3x | 5.5 | 1242 x 2208 | 1.777 |
| iPhone X | 3x | 5.8 | 1125 × 2436 | 2.165 (MAX) |
| iPhone XS | 3x | 5.8 | 1125 × 2436 | 2.165 (MAX) |
| iPhone XS Max | 3x | 6.5 | 1242 x 2688  | 2.164 |
| iPhone XR | 2x | 6.1 | 828 x 1792  | 2.164 |
| iPad | 1x | 7.9 | 768 x 1024 | 1.333 | 0.750 |
| iPad mini 4 | 2x | 7.9 | 1536 × 2048 | 1.333 | 0.750 |
| 9.7" iPad | 2x | 9.7 | 1536 x 2048 | 1.333 | 0.750 |
| 10.5" iPad pro | 3x | 10.5 | 1668 x 2224 | 1.334 | 0.7496 (MIN) |
| 12.9" iPad pro | 3x | 12.9 | 2048 x 2732 | 1.334 | 0.7496 (MIN) |

## App 内用图

### Logo

| 一倍大小 | 比例 | size(pixels) | 机型 | 备注 |
|:--------:| -------- |:--------:|:--------:|:--------:|
| 20 | 1x | 20 x 20 |
| 20 | 2x | 40 x 40 | | == 40 |
| 20 | 3x | 60 x 60 |
| 29 | 1x | 29 x 29 |
| 29 | 2x | 58 x 58 |
| 29 | 3x | 87 x 87 |
| 40 | 1x | 40 x 40 | | == 40 |
| 40 | 2x | 80 x 80 |
| 40 | 3x | 120 x 120 | | == 120 |
| 60 | 2x | 120 x 120 | | == 120 |
| 60 | 3x | 180 x 180 |
| 76 | 1x | 76 x 76 | iPad App |
| 76 | 2x | 152 x 152 | iPad App |
| 83.5 | 2x | 167 x 167 | iPad Pro App |

### 启动图

| 平台 | 比例 | size(pixels) | 备注 |
| :--------: | :--------: |:--------:|:--------:|
| iPhone | 2x | 640 × 960 |
| iPhone | retina4 | 640 × 1136 |
| iPad | 1x | 768 × 1024 |
| iPad | 2x | 1536 × 2048 |

### 默认启动广告图

客户端等比缩放后，取中间部分

| 平台 | 比例 | size(pixels) | 备注 |
| :--------: | :--------: |:--------:|:--------:|
| 自适应 | 1x | 667/0.75 × 667 | 890 × 667 |
| 自适应 | 2x | 1334/0.75  × 1334 | 1780 × 1334 |
| 自适应 | 3x | 2001/0.75 × 2001 | 2670x2001 |

### 后台配置启动广告图

取最大的图，客户端等比缩放后，取中间部分

| 平台 | 比例 | size(pixels) | 备注 |
| :--------: | :--------: |:--------:|:--------:|
| 自适应 | 3x | 2001/0.75 × 2001 | 2670x2001 |

### 引导图

客户端等比缩放后，取中间部分,其中 0.75 是 iOS 所有设备中最小高宽比。

| 平台 | 比例 | size(pixels) | 备注 |
| :--------: | :--------: |:--------:|:--------:|
| 自适应 | 1x | 667/0.75 × 667 | 890 × 667 |
| 自适应 | 2x | 1334/0.75 × 1334 | 1780 × 1334 |
| 自适应 | 3x | 2001/0.75 × 2001 | 2670 x 2001 |

## iTunes Connect 用图

### Logo

此图标将用于 App Store，其格式必须为 JPG 或 PNG，最低分辨率至少为 72 DPI，并采用 RGB 色彩空间。它不能包含图层或圆角。

取 1024 x 1024

### 截屏

* [iTunes Connect Properties](https://developer.apple.com/library/content/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Appendices/Properties.html)

| 机型 | 屏幕 | 分辨率(pixels) |
|:--------:| -------- |:--------:|
| iPhone4 | 3.5-Inch Retina | 640 x 960 |
| iPhone5 | 4-Inch Retina | 640 x 1136 |
| iPhone6 | 4.7-Inch Retina | 750 x 1334 |
| iPhone6+ | 5.5-Inch Retina | 1242 x 2208 |
| iPad | 9.7-Inch Retina | 1536 x 2048 |
| iPad pro | 12.9-Inch Retina | 2048 x 2732 |

## 注意

自适应的图片只有中间部分是有效部分，左边和右边部分可能不显示。在所有设备中中间宽度显示的最小宽度为 `2001/2.165 = 924.249`。其中 2.165 是 iOS 所有设备中最大高宽比。