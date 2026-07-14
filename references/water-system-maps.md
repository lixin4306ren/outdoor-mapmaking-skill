# 水系图制作规则索引

水系图有多种制作模式。用户没有明确指定时，必须先让用户选择模式，不能直接制作、下载数据或渲染。

## 选择项

- 模式 A：卫星底图（HydroBASINS + HydroRIVERS + OSM + Esri/其他卫星影像）。读取 `water-system-mode-a-satellite.md`。
- 模式 B：DEM 地形分层设色（AWS Terrain DEM + pysheds D8 水文分析 + OSM 注记）。读取 `water-system-mode-b-terrain.md`。
- 模式 C：卫星底图 + DEM 河网（Esri World Imagery + AWS Terrain DEM + pysheds）。读取 `water-system-mode-c-satellite-dem.md`。

## 读取顺序

1. 总是先读 `water-system-common.md`，确认模式选择、通用硬约束和禁止事项。
2. 只读取用户选择的模式文件。
3. 需要写配套水系介绍、查历史产物或脚本目录时，再读 `water-system-writing-and-assets.md`。

## 必须先询问的情况

- 用户只说“做一张水系图”“修改水系图风格”“做某流域地图”，但没有说明模式。
- 用户只指定“卫星/地形”但没有明确是否用 HydroRIVERS 还是 DEM 河网。
- 用户要求换底图但没指定瓦片源或坐标系处理方式。
