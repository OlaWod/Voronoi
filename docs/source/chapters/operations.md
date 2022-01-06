# 执行结果

## 打开页面

示例操作：在浏览器正确打开[https://olawod.github.io/Voronoi/](https://olawod.github.io/Voronoi/) 或 `index.html` 后，将随机生成 100 个点并生成 Voronoi 图，显示如下画面：

![open](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/open.png)

## 随机生成 N 个点

功能：清空当前画布，重新随机生成 N 个点并生成 Voronoi 图。

输入框中的字符将转换为 int 类型，因此当输入浮点数（如3.6）时将被向下取整，当输入非法字符（+数字）（如 '#%@', ''#66', '-8'）时将赋为0；当输入数字+非法字符（如 '66#!'）时将取非法字符前面的数字（66）；其余规则详见 JavaScript 的 parseInt 用法。该页面其余输入框规则同理。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，在按钮 "随机生成" 那一行的输入框中输入要生成的点数 N=10，点击按钮 "随机生成" 后，显示如下画面：

![randgen](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/randgen.png)

注意，程序执行时间与 N 呈正相关，请根据自身电脑及浏览器配置酌情填写生成点数。

## 随机添加 N 个点

功能：在当前 Voronoi 图上随机添加 N 个点。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，当前 Voronoi 图中共有 10 个点时，在按钮 "随机添加" 那一行的输入框中输入要添加的点数 N=5，点击按钮 "随机添加" 后，显示如下画面：（左图为添加前，右图为添加后）

![randadd](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/randadd.jpg)

注意，程序执行时间与 N 呈正相关，请根据自身电脑及浏览器配置酌情填写添加点数。

## 添加新点（鼠标点击）

功能：鼠标点击 Canvas 画布，即可在点击处添加新点，并生成新的 Voronoi 图。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，鼠标点击右上角前与点击右上角后，显示如下画面：（左图为点击前，右图为点击后）

![addclick](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/addclick.jpg)

## 添加新点（输入坐标）

功能：在当前 Voronoi 图上添加新点，新点坐标为输入框中的值，并生成新的 Voronoi 图。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，在按钮 "添加一点" 那一行的输入框中输入要生成的点的横坐标=700 与纵坐标=500，点击按钮 "添加一点" 后，显示如下画面：（左图为添加前，右图为添加后）

![addtext](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/addtext.jpg)

## 求最近邻（鼠标位置）

功能：在按钮 "求最近邻" 那一行的输入框中显示当前鼠标坐标，并在右边显示该坐标的最近邻，同时在画布上对当前鼠标所在的区域做高亮显示。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，将鼠标移到坐标（367, 344） 后，显示如下画面：

![neighbormm](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/neighbormm.png)

可以看到，点（367, 344）的最近邻是点9，其坐标是（349.4, 309.2），其所在区域被高亮显示。

## 求最近邻（输入坐标）

功能：输入要求最近邻的点的坐标，显示该点的最近邻，并在画布上对该点所在的区域做高亮显示。

注意，画布大小为 800 × 600，因此横坐标的有效范围为 (0, 800)，不包含 0 和 800；纵坐标的有效范围为 (0, 600)，不包含 0 和 600。若输入越界则不予显示。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，在按钮 "求最近邻" 那一行的输入框中输入要求最近邻的点的横坐标=400 与纵坐标=400，点击按钮 "求最近邻" 后，显示如下画面：

![neighbortext](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/neighbortext.png)

可以看到，点（400, 400）的最近邻是点12，其坐标是（479, 424.4），其所在区域被高亮显示。

## 求最近邻（勾选 "求当前图上所有点的最近邻"）

功能：勾选控制面板中第一行的 "求当前图上所有点的最近邻"，显示当前 Voronoi 图解对应的 Delaunay 三角剖分（浅灰线），并显示每个 cell 对应的 site 的最近邻（蓝色箭头）。

注意，勾选此项将无法再进行交互（控制面板的其他功能将被禁用，鼠标交互也将被禁用），因此请交互完后再勾选此项求最近邻，若要重新进行交互请取消勾选此项。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，勾选控制面板中第一行的 "求当前图上所有点的最近邻" 后，显示如下画面：

![neighbortext](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/neighborall.png)

可以看到，浅灰线为当前 Voronoi 图解对应的 Delaunay 三角剖分，每个蓝色箭头表示每个 cell 对应的 site （箭头起点）的最近邻（箭头终点）。

## 清空画布

功能：将 Voronoi 图清空，将画布清空。

示例操作：在未勾选 "求当前图上所有点的最近邻" 时，点击按钮 "清空" 后，显示如下画面：

![reset](https://cdn.jsdelivr.net/gh/OlaWod/Voronoi@2.0/docs/source/assets/reset.png)
