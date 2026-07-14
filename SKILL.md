---
name: outdoor-mapmaking
description: >-
  Build and maintain the outdoor travel map products in this OneDrive notes
  workspace: water-system maps, road-trip route maps, peak check-in maps, and
  mountain terrain/ridge maps. Use when creating, revising, validating, or
  linking maps under 个人笔记本/OneNote/户外旅行, especially when the request
  mentions 水系图, 自驾路线图, 登顶山峰打卡地图, 山峰打卡图, 山脉地形图,
  DEM, 卫星底图, Natural Earth, HydroRIVERS, HydroBASINS, pysheds, or
  地形晕渲.
---

# Outdoor Mapmaking Skill

本技能包承接原 `个人笔记本/项目上下文.md` 中的户外制图长规则，目的是让项目上下文只保留入口，避免每次协作都读取数百行制图细则。

## 使用边界

当任务涉及以下任一地图，必须先读取本入口，然后按任务类型继续读取对应 reference：

- 水系图：先读 `references/water-system-maps.md`，再按用户选择读取 `water-system-mode-*.md`
- 自驾路线图：`references/road-trip-route-maps.md`
- 登顶山峰/山峰打卡图：`references/peak-checkin-maps.md`
- 山脉地形图/山脊线图：`references/mountain-terrain-maps.md`

只读取相关 reference，不要一次性加载全部文件；除非用户要求整理整个制图体系。

## 模式/底图选择硬规则

凡地图任务存在多种模式或多种底图，且用户没有在当前请求中明确指定，必须先停下来让用户选择，不能直接制作、下载数据或渲染成品。可以先读取对应 reference 以列出选择项，但只能做方案说明，不能开始实现。

必须询问的场景：

- 水系图：先让用户在模式 A（卫星底图）、模式 B（DEM 地形分层设色）、模式 C（卫星底图 + DEM 河网）中选择。
- 自驾路线图：先让用户选择底图风格，例如 `Esri.WorldTopoMap`、`CartoDB.Positron`、`CartoDB.Voyager`、`Esri.WorldShadedRelief`、`Esri.WorldGrayCanvas` 或离线浅灰纸底；同时说明哪些底图需要叠加 NE 河流/海岸线。
- 登顶山峰/山峰打卡图：先让用户选择省域 DEM/高程渲染模式，还是山脉卫星底图模式；如果卫星底图也有多种瓦片源，也要先确认。
- 山脉地形图：若用户没有指定表现方式，先确认是 DEM 晕渲 + 山脊线专题图，还是只做山峰打卡/卫星轨迹图。

若用户已经明确指定模式或底图，按指定执行，不再重复确认；但发现指定方案和数据坐标系、可用缓存或目标用途明显冲突时，先指出冲突并等待确认。

## 通用硬约束

- 先读当前代码、配置、缓存和既有产物，再修改；不要凭记忆断言历史实现。
- 地理对象位置不能靠版面感觉估计：山峰、山脉、河流、国境线、省界、海岸线必须有 OSM、Natural Earth、HydroRIVERS/HydroBASINS、DataV、DEM 或公开资料支撑。
- 有可见输出的改动，完成前必须重新生成 PNG，并目视检查整图和问题局部；不能只看脚本成功退出。
- 新制图产物默认只输出 PNG；历史已有 SVG 可保留，但后续新图不再强制 SVG。
- 文字标注不得相互重叠，也不得压住关键点位、图标、河线、城市、省名或图例；密集标注优先使用引导线，不用缩小到不可读字号解决。
- 如果用户报告具体错位、重叠、漏标或颜色问题，先定位根因再改，必要时做局部裁图或像素/包围盒检查。

## 项目内关键入口

- 户外旅行规则与调试纪律：`个人笔记本/OneNote/户外旅行/CLAUDE.md`
- 水系脚本根目录：`个人笔记本/OneNote/户外旅行/水系/scripts/`
- 自驾路线脚本根目录：`个人笔记本/OneNote/户外旅行/自驾路线/附件/`
- 山峰打卡地图脚本：`个人笔记本/OneNote/户外旅行/户外运动经历/附件/山峰打卡地图/脚本/`
- 苍山山峰打卡卫星图脚本：`个人笔记本/OneNote/户外旅行/户外运动经历/附件/苍山山峰打卡地图/脚本/`
- 苍山山脉地形图脚本：`个人笔记本/OneNote/户外旅行/户外运动经历/附件/苍山山脉图/脚本/`
