## 目录文件说明

1. china.json 中国地图
2. province 目录下为所有省份、直辖市
3. citys 目录下为所有市
4. county 目录下为所有区域
5. other 中为直辖市的地图，与 province 目录下的直辖市有所不同，other 的直辖市不显示具体的区域信息

## ohter 目录下的直辖市对比

> 可以根据自己的实际场景使用不同的 GeoJSON 

province 目录下的直辖市

![image-20210810112336958](other\images\image-20210810112336958.png)



other 目录下的直辖市

![image-20210810112148350](other\images\image-20210810112148350.png)

## other/index.html

用于提取 `province`目录中直辖市数据，提取出  `other` 目录下直辖市所需要数据的工具。

注意：index.html 直接打开无效，需要在项目的根目录运行 ` http-server.cmd -p 3002` 命令。

在打开链接：[http://localhost:3002/other/index.html](http://localhost:3002/other/index.html)

红框中的数据就是 `GeoJson` 中 `features.geometry.coordinates` 所需的数据。

其他省份需要「不绘制具体的市的信息」也可以使用该工具，替换 `features.geometry.coordinates` 中的值，还需要将 `json` 文件中的 `features.geometry.type` 设为 `MultiPolygon`

![image-20210810112914847](.\other\images\image-20210810112914847.png)