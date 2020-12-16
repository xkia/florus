# Florus

Florus is a piece of Javascript code applied to the *Scriptable* App, displaying date, lunar date, weekday, year progress, weather information, events reminder, funds valuation, stock quotes, as well as random motto, via widget in iOS 14.

![](https://wt365.github.io/lib/florus/screenshot1.jpg)
![](https://wt365.github.io/lib/florus/screenshot2.jpg)

Florus是一则应用于*Scriptable* App的Javascript脚本，它可以在iOS14小组件中实现：

* 显示日期、星期、农历、全年进度
* 显示指定位置的天气状况、温度、三小时内降雨/降雪提醒
* 显示日历中事项或自编事项的倒数天数
* 显示指定基金的估值
* 显示指定股票的行情
* 从一言数据库中随机显示一句话及其出处
* 支持小、中、大三种尺寸，不同尺寸下显示适合的内容容量
* 支持黑色调与白色调两种配色方案，亦可自动切换

### 食用方法

1. 将florus.js中的全部代码复制。（手机视图中或需点击`View code`展开后再点击florus.js可见。）
2. iOS14用户安装**Scriptable** App。打开App，点击右上角 `+号` 新建脚本，将已复制的代码粘贴入。
3. 将代码中设置区内的**位置纬度经度**、**提醒事项模式**及**自编提醒事项**、**金融功能开关**及**基金/股票代码**、**配色方案**改成自己需要的。
4. 点击左上角 `Done` ，保存脚本后可长按对其重命名（比如 *Florus* ）。
5. 长按iOS14桌面空白处，点击左上角 `+号` 添加小组件，选择Scriptable。建议中尺寸，其它尺寸亦可。
6. 长按刚才添加的组件，点击**编辑小组件**，Script处选择 *Florus* 即可。

### 设置说明

* 位置设置 **loc**：先纬度，后经度，用于显示天气。
* 提醒事项模式 **EM**：可选值 0 或 1
	* *EM=0* 时为自编事项（默认）。请按样例格式自行在脚本里（Events段）添加事项，可添加任意多行，无需按时间顺序，会自动排序后显示未来最近的3项（中尺寸）、4项（小尺寸）或6项（大尺寸）。
	* *EM=1* 时为从日历中读取事项（须授权同意Scriptable访问日历）。
* 金融功能开关 **FF**：可选值 0, 1, 2
	* *FF=0* 时不开启金融功能（默认），将正常显示提醒事项。
	* *FF=1* 时开启基金估值显示，请设置一组基金代码Fcodes。
	* *FF=2* 时开启股票行情显示，请设置一组股票代码Fcodes。
	* 金融功能开启（FF=1或FF=2）时，中、小尺寸下将不显示提醒事项，中尺寸显示最多3项基金估值或6项股票行情，小尺寸显示最多4项基金估值/股票行情；大尺寸将同时显示最多6项提醒事项和最多6项基金估值/股票行情。
* 配色方案 **cs**：可选值 0, 1, 2
	* *cs=0* 时为黑色调。
	* *cs=1* 时为白色调。
	* *cs=2* 时为自动切换色调（默认）。

### 注意事项

* 推荐使用中尺寸组件，但小尺寸和大尺寸也同样支持。另外，作者机型为iPhoneXS，其他设备可自行适当调整字号大小。
* 农历已经支持到2021年底了，2022年之前我会再更新一下。
* 作者比较懒，更多好玩的功能我想到了再慢慢加……

*designed and coded with love by Tingyu.*