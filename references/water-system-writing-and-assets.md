# Water System Writing And Assets

## 水系介绍编写规则

每幅全流域或专题水系图必须配套一篇同名水系介绍，深度至少参照 `北江水系.md` 和 `乌江水系.md`，不能只罗列河长、面积和支流名称。默认包含以下内容：

- **规范元数据与读图说明**：使用 Obsidian frontmatter，标明区域、省份、数据源、标签和别名；正文开头嵌入 `scripts/outputs/` 下的主图，并说明河网层级、边界、颜色、数据尺度及用途限制。
- **源流与水系结构**：解释源头、主流认定、干流名称变化、主要汇流点、上中下游分段、河口或入江关系，以及全球水文数据面积与官方面积存在差异的原因。
- **主要支流**：用表格说明支流的岸别或汇流关系、覆盖区域、重要盆地或聚落、跨省属性，以及对旅行地理的意义。
- **分水岭与山地骨架**：明确流域四周及内部重要山脉、山岭、垭口和代表峰，说明它们分隔了哪些相邻水系、如何控制河流方向与区域交通。重要山脉不得因为版面拥挤随意删去。
- **古道、航道与迁徙通道**：梳理沿河古驿道、盐道、商道、航运、关隘、渡口、码头、军事路线和人口迁徙，解释水路与陆路如何共同构成历史交通网络。
- **峡谷、河谷与风景名胜**：记录真实存在的峡谷、库区、瀑布、湿地、古城、古镇、桥梁、寺观、文保点、自然保护地和代表性景区，并说明其与水系或地貌的关系。若没有正式命名的大峡谷，应如实描述河谷或峡段，不得为了凑栏目虚构地名。
- **重要地理节点与水利工程**：至少覆盖源头、盆地、汇流口、河口、三角洲、跨省断面、重要城市、水库和水利枢纽，解释每个节点为何重要。
- **地理意义与旅行主题**：从地貌阶梯、区域文化、聚落与农业、跨省治理、生态保护等角度总结流域意义，并给出能串联自然、人文和交通结构的延伸观察路线。
- **资料来源与可信度**：优先采用水利部、流域管理机构、地方政府、自然保护地规划和学术资料；区分官方事实、地图推断与近似位置，避免景区宣传腔和未经核实的传说。

当前北江水系图脚本位于 `个人笔记本/OneNote/户外旅行/水系/scripts/`，成品位于 `scripts/outputs/`，可作为后续水系图的实现参考。

## 水系图产物目录

已生成的水系图：

| 水系     | 文件                  | 位置                                 | 数据来源                                                                |
| ------ | ------------------- | ---------------------------------- | ------------------------------------------------------------------- |
| 北江全流域  | `北江全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS + HydroRIVERS + OSM + Esri                              |
| 东江全流域  | `东江全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS L6 + HydroRIVERS + OSM + Esri World Imagery z10 + 阿里云省界 |
| 乌江全流域  | `乌江全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS + HydroRIVERS + OSM + Esri World Imagery z9 + 阿里云省界       |
| 韩江全流域  | `韩江全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS + HydroRIVERS + OSM + Esri World Imagery z9 + 阿里云省界       |
| 榕江全流域  | `榕江全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS L8 + HydroRIVERS + OSM + Esri World Imagery z9 + 阿里云省界    |
| 练江全流域  | `练江全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS L8 + HydroRIVERS + OSM + Esri World Imagery z12 + 阿里云省界   |
| 渭河全流域  | `渭河全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS L6 + HydroRIVERS + Esri World Imagery z9 + 阿里云省界           |
| 汾河全流域  | `汾河全流域水系图.png/svg`  | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS L6 + HydroRIVERS + Esri World Imagery z10 + 阿里云省界          |
| 南盘江全流域 | `南盘江全流域水系图.png/svg` | `OneNote/户外旅行/水系/scripts/outputs/` | HydroBASINS L6 + HydroRIVERS(干流 NEXT_DOWN 单路径追踪, 背景 ORD≥4) + OSM + **Esri World Imagery z10(WGS-84)** + 阿里云省界（云/黔/桂）；含相邻干流北盘江/红水河 |
| 北盘江（地形分层设色） | `北盘江水系图_地形渲染.png` | `OneNote/户外旅行/水系/scripts/outputs/` | AWS Terrain DEM(z10) 晕渲 + pysheds 水文分析 + OSM |
| 赣江（地形分层设色） | `赣江水系图_地形渲染.png/svg` | `OneNote/户外旅行/水系/scripts/outputs/` | AWS Terrain DEM(z10) 晕渲 + pysheds D8 水文分析 + 阿里云省界；流域面积约 8.42 万 km² |
| 湘江（地形分层设色） | `湘江水系图_地形渲染.png/svg` | `OneNote/户外旅行/水系/scripts/outputs/` | AWS Terrain DEM(z10) 晕渲 + pysheds D8 水文分析 + 阿里云省界；乔口控制点圈定约 9.37 万 km²；支流浅蓝 `#56B4E9`，干流同色相、同饱和度但 HSL 明度降低 50% 为 `#12618D`，两者共用流量—线宽函数；干流周围为淡白高斯渐变背景，山脉名逐字拉开 |
| 汉江全流域（模式 C） | `汉江全流域水系图.png/svg` | `OneNote/户外旅行/水系/scripts/outputs/` | **模式 C**：Esri World Imagery z9 底图 + AWS Terrain DEM(z9) + pysheds D8 河网/流域/干流 + 阿里云省界（陕/鄂/豫等）+ OSM 长江；干流经嶓冢山重建 |
| 云南元江（模式 C + 模式 B 标注） | `云南元江水系图.png/svg` | `OneNote/户外旅行/水系/scripts/outputs/` | **模式 C**：Esri World Imagery z10 底图 + AWS Terrain DEM(z10) + pysheds D8 河网/流域/干流 + 阿里云云南省界；采用模式 B 标注体系与河网视觉：支流浅蓝 `#56B4E9`，干流同色相 HSL 明度降低 50% 为 `#12618D`，干流周围保留淡白高斯渐变背景，河网线宽只随集水面积连续变化；图例置左下角并内嵌真实 10 km 比例尺。2026-07-07 修订：哀牢山与大雪锅山峰点校正到元江／红河干流西侧，删除红河谷、大春河、南昏河等误导或拥挤标注；南溪河按 OSM 同名 `waterway=river` 几何与公开资料作为经核实订正通道绘制并标注；技术出水口下移到南溪河汇入后的 DEM 下游格，重算流域面积约 38,489 km²，南溪河流域已纳入边界；小河底河保留为有来源元数据约束的 DEM 专属支流通道 |
| 独龙江（地形分层设色） | `独龙江水系图_地形渲染.png/svg` | `OneNote/户外旅行/水系/scripts/outputs/` | **模式 B**：AWS Terrain DEM(z10) 晕渲 + pysheds D8 水文分析 + OSM 注记 + 阿里云云南/西藏边界 + OSM `admin_level=2` 中缅国界（Natural Earth 10m `admin_0_boundary_lines_land` 备用复核）；出境控制点 DEM 圈定地形集水面积约 4,217 平方千米，图文说明中单独区分公开资料常见“国内流域面积 1,947 平方千米”的统计口径；支流浅蓝 `#56B4E9`，干流同色相深蓝 `#12618D`，干支流共用集水面积—线宽函数，干流周围为淡白高斯渐变背景；标注日东河、克劳龙河、麻必洛、独龙江、担当利卡山、高黎贡山、伯舒拉岭及独龙江乡谷地节点。 |

脚本结构：
- 北江：`OneNote/户外旅行/水系/scripts/` 下 `make_beijiang_basin_map.py`、`beijiang_config.py`、`beijiang_data.py`
- 东江：`OneNote/户外旅行/水系/scripts/dongjiang/` 下 `make_dongjiang_basin_map.py`、`dongjiang_config.py`、`dongjiang_data.py`
- 乌江：`OneNote/户外旅行/水系/scripts/wujiang/` 下 `make_wujiang_basin_map.py`、`wujiang_config.py`、`wujiang_data.py`
- 韩江：`OneNote/户外旅行/水系/scripts/hanjiang/` 下 `make_hanjiang_basin_map.py`、`hanjiang_config.py`、`hanjiang_data.py`
- 榕江：`OneNote/户外旅行/水系/scripts/rongjiang/` 下 `make_rongjiang_basin_map.py`、`rongjiang_config.py`、`rongjiang_data.py`
- 练江：`OneNote/户外旅行/水系/scripts/lianjiang/` 下 `make_lianjiang_basin_map.py`、`lianjiang_config.py`、`lianjiang_data.py`
- 渭河：`OneNote/户外旅行/水系/scripts/weihe/` 下 `make_weihe_basin_map.py`、`weihe_config.py`
- 汾河：`OneNote/户外旅行/水系/scripts/fenhe/` 下 `make_fenhe_basin_map.py`、`fenhe_config.py`
- 北盘江：`OneNote/户外旅行/水系/scripts/beipanjiang/` 下 `make_beipanjiang_basin_map.py`、`beipanjiang_config.py`、`beipanjiang_data.py`
- 南盘江：`OneNote/户外旅行/水系/scripts/nanpanjiang/` 下 `make_nanpanjiang_basin_map.py`、`nanpanjiang_config.py`、`nanpanjiang_data.py`。复用顶层共享 `scripts/cache/hydrosheds/` 的 HydroSheds shapefile 免重下；相邻干流几何缓存于 `cache/adjacent_rivers.geojson`
- 地形分层设色通用工具集：`OneNote/户外旅行/水系/scripts/terrain_dem/` 下 `fetch_dem.py`、`watershed_pysheds.py`、`final_map.py`（另含卫星版 `build_map2.py`、地形晕渲 `build_relief.py`、纯 Python 备选 `watershed.py`）、`venv/`、`requirements.txt`、`README.md`。多流域参数在 `terrain_runtime.py`；赣江以 `ganjiang_render_config.py`、`render_ganjiang.py` 完成专属排版，中间数据位于 `runs/ganjiang/`；湘江以 `xiangjiang_render_config.py`、`render_xiangjiang.py` 完成统一浅蓝河色、干支流共用流量线宽、干流淡白高斯背景与山脉逐字排布，中间数据位于 `runs/xiangjiang/`。
- 独龙江（模式 B）：在 `terrain_runtime.py` 中新增 `dulongjiang` 配置；`render_dulongjiang.py` 与 `dulongjiang_render_config.py` 完成专属排版，中间数据位于 `runs/dulongjiang/`。当前 OneDrive 同步后的 `terrain_dem/venv/bin/python` 可能只是 `python3.14` 文本入口；可用 `PYTHONPATH=./venv/lib/python3.14/site-packages WATERSHED_NAME=dulongjiang $(cat ./venv/bin/python3.14) -u watershed_pysheds.py` 和同样前缀运行 `render_dulongjiang.py`。
- 汉江（模式 C）：`OneNote/户外旅行/水系/scripts/hanshui/` 下 `hanshui_config.py`（范围/出水口/河源/标注）、`prepare_hanshui_hydro.py`（DEM 下载 + pysheds 水文分析 → `cache/`）、`make_hanshui_basin_map.py`（Mercator 像素空间渲染）。运行环境复用 `terrain_dem/venv`；目录名用 `hanshui` 以避免与韩江 `hanjiang` 拼音冲突。
- 云南元江（模式 C + 模式 B 标注）：`OneNote/户外旅行/水系/scripts/yuanjiang/` 下 `yuanjiang_config.py`（范围/源头/出水口/标注/视觉参数）、`yuanjiang_style.py`（Mercator 投影、HSL 明度、流量—线宽函数、干流白色渐变）、`prepare_yuanjiang_hydro.py`（DEM 下载 + pysheds D8 水文分析 → `cache/`）、`make_yuanjiang_basin_map.py`（Esri 卫星底图 + DEM 河网渲染）、`test_yuanjiang_map.py`（坐标、面积、干流样式、标注侧向、南溪河流域纳入与比例尺等回归测试）。本图按用户要求采用左下角图例与真实 10 km 比例尺；哀牢山和峰点必须位于同纬度干流西侧；南溪河使用 OSM 订正通道且其流域必须被 DEM basin mask 纳入；缺乏可见 DEM 河道支撑或 OSM/公开资料订正依据的河名不得硬吸附到干流。
