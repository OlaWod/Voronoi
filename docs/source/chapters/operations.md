# 执行结果

## 打开页面

在浏览器正确打开 https://olawod.github.io/Voronoi/ 或 index.html 后，将随机生成 100 个点并生成 Voronoi 图，显示如下画面：

![open](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/open.png)

## 随机生成 N 个点

清空当前画布，重新随机生成 N 个点并生成 Voronoi 图。

输入框中的字符将转换为 int 类型，因此当输入浮点数（如3.6）时将被向下取整，当输入非法字符（+数字）（如 '#%@', ''#66', '-8'）时将赋为0；当输入数字+非法字符（如 '66#!'）时将取非法字符前面的数字（66）；其余规则详见 JavaScript 的 parseInt 用法。该页面其余输入框规则同理。

在按钮 "随机生成" 那一行的输入框中输入要生成的点数 N=200，点击按钮 "随机生成" 后，显示如下画面：

![open](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/randgen.png)

注意，程序执行时间与 N 呈正相关，请根据自身电脑及浏览器配置酌情填写生成点数。

## 随机添加 N 个点

在当前 Voronoi 图上随机添加 N 个点。

当前 Voronoi 图中共有 100 个点时，在按钮 "随机添加" 那一行的输入框中输入要添加的点数 N=50，点击按钮 "随机添加" 后，显示如下画面：

![open](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/randadd.png)

注意，程序执行时间与 N 呈正相关，请根据自身电脑及浏览器配置酌情填写添加点数。

## 添加新点（鼠标点击）

鼠标点击 Canvas 画布，即可在点击处添加新点，并生成新的 Voronoi 图。

鼠标点击左上角前与点击左上角后，显示如下画面：（左图为点击前，右图为点击后）

![addclick](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/addclick.jpg)

## 添加新点（输入坐标）

在当前 Voronoi 图上添加新点，新点坐标为输入框中的值，并生成新的 Voronoi 图。

在按钮 "添加一点" 那一行的输入框中输入要生成的点的横坐标=100 与纵坐标=100，点击按钮 "添加一点" 后，显示如下画面：（左图为添加前，右图为添加后）

![addtext](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/addtext.jpg)

## 求鼠标所在位置的最近邻

在按钮 "求最近邻" 那一行的输入框中显示当前鼠标坐标，并在右边显示该坐标的最近邻，同时在画布上对当前鼠标所在的区域做高亮显示。

将鼠标移到坐标（358, 196） 后，显示如下画面：

![neighbormm](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/neighbormm.png)

可以看到，点（358, 196）的最近邻是点30，其坐标是（362, 171.8），其所在区域被高亮显示。

## 输入坐标求最近邻

输入要求最近邻的点的坐标，显示该点的最近邻，并在画布上对该点所在的区域做高亮显示。

在按钮 "求最近邻" 那一行的输入框中输入要求最近邻的点的横坐标=300 与纵坐标=300，点击按钮 "求最近邻" 后，显示如下画面：

![neighbortext](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/neighbortext.png)

可以看到，点（300, 300）的最近邻是点61，其坐标是（331.1, 294.5），其所在区域被高亮显示。

## 清空画布

将 Voronoi 图清空，将画布清空。

点击按钮 "清空" 后，显示如下画面：

![reset](https://raw.githubusercontent.com/OlaWod/Voronoi/main/docs/source/assets/reset.png)
