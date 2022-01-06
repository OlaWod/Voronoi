# 程序功能

## index.html

主页面。

主要元素：标题、Canvas 画布（用于绘制 Voronoi 图解）、控制面板（包含若干按钮与输入框等）。

## voronoi/demo.js

本项目的顶层逻辑。声明类并定义对象 VoronoiDemo。

### VoronoiDemo.init()

初始化。加载页面时调用。

随机初始化 100 个点，生成 Voronoi 图解并绘制在 Canvas 画布上。

### VoronoiDemo.clearSites()

点击 “清空” 按钮时调用。

清空所有点，清空 Voronoi 图解，清空用于组织 Voronoi 图中的 cell 的四叉树。

### VoronoiDemo.randomSites(n, clear)

随机生成 / 添加 n 个点。点击 “随机生成”（clear=true） / “随机添加” （clear=false）按钮时调用。

若 clear=true （点击 “随机生成”），则清空 sites。接着往 sites 中添加 n 个随机点，清空用于组织 cell 的四叉树并重新计算 Voronoi 图。

### VoronoiDemo.addSite(x, y)

往 sites 中添加坐标为（x, y）的点，并重新计算 Voronoi 图解。

### VoronoiDemo.addSiteClick(e)

通过鼠标点击的方式来添加新点。鼠标点击 Canvas 画布时调用。

获取鼠标坐标，往 sites 中添加该点，重新计算 Voronoi 图解，重新在 Canvas 画布上绘制。

### VoronoiDemo.addSiteText()

添加坐标为输入框中坐标的点。点击 “添加一点” 时调用。

获取输入框中的坐标，往 sites 中添加该点，重新计算 Voronoi 图解，重新在 Canvas 画布上绘制。

### VoronoiDemo.recompute()

清空用于组织 cell 的四叉树并重新计算 Voronoi 图。当图中的点发生变化（如添加新点、清空）时调用。

### VoronoiDemo.updateStats()

更新页面上的当前点数。当图中的点发生变化（如添加新点、清空）时调用。

### VoronoiDemo.buildTreemap()

将 Voronoi 图中的 cell 插入四叉树中。

### VoronoiDemo.cellUnderMouse(ev)

获取当前鼠标坐标，获取该坐标所在的 cell，对此 cell 高亮显示，并在页面上显示此 cell 对应的点的 id 及坐标（该点即为鼠标所在位置的最近邻）。鼠标在 Canvas 画布上移动时调用。

### VoronoiDemo.getNearestCell()

获取输入框中的坐标，获取该坐标所在的 cell，对此 cell 高亮显示，并在页面上显示此 cell 对应的点的 id 及坐标（该点即为输入框中坐标的最近邻）。点击 “求最近邻” 时调用。

### VoronoiDemo.cellFromPoint(x, y)

若调用时四叉树为空则构建四叉树。接着在四叉树中找到点（x, y）所在的 cell。

### VoronoiDemo.renderCell(id, fillStyle, strokeStyle)

在 Canvas 画布上绘制索引为 id 的 cell 所对应的边和点。

### VoronoiDemo.render()

在 Canvas 画布上绘制 Voronoi 图解

### VoronoiDemo.normalizeEventCoords(target, e)

将鼠标相对于整个页面的坐标转换为相对于 Canvas 画布的坐标。

### VoronoiDemo.delaunayForNearest()

遍历每个 cell 的边，求每个 cell 对应的 site 的最近邻。勾选 "求当前图上所有点的最近邻" 时调用。

## voronoi/Voronoi.js

声明构建最近点 Voronoi 图解所需的各种数据结构和函数。

三个主要数据结构：

1. Voronoi 图

其成员主要包括 vertices（voronoi 图的所有顶点）、edges（voronoi 图的所有边）、cells
（voronoi 图的所有区块）、各种中间状态等。

2. 有序事件队列

用 RBTree 实现点事件队列与顶点事件队列。

3. 海滩线

用 RBTree 实现海滩线。

## voronoi/QuadTree.js

声明类 QuadTree 及其所需的数据结构和函数。

在基于四叉树的最近邻查找算法中用到该四叉树。

## voronoi/style.css

用于修饰 index.html 中各个元素的样式和布局。
