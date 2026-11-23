# 黑潮防线 · 网页版

团结引擎（Tuanjie 2022.3.62t15 / Unity URP）构建的 3D 三人共斗 Roguelike PVE，浏览器直接开玩。

**在线游玩：<https://stockholm754-source.github.io/black-tide/>**

## 操作

| 按键 | 作用 |
|---|---|
| WASD | 移动（Ctrl 慢走） |
| 鼠标左键 | 普攻（自动朝最近敌人，可按住） |
| 空格 / 右键 / Shift | 闪避（前 0.24s 完美闪避窗口） |
| E | 共鸣技能 |
| Q | 共鸣解放（能量满） |
| R | 声骸技能 |
| V | 武器技能 |
| Tab | 切换操控角色 |
| 1 / 2 | 协奏接力 |
| 按住 F | 救援倒地的队友 |
| B | 增益三选一（面板里按 1/2/3） |
| G / Esc | 商店 |
| H | 教学面板 |
| M | 大地图 |
| F1 | 自动代打 |
| F2 | 重开本局 |

Xbox / XInput 手柄在 Windows 浏览器里同样可用（左摇杆移动、X 普攻、B 闪避、RB 技能、RT 大招）。

## 关于这个构建

- 真实 Unity 工程的 WebGL 构建，包含主菜单与开放地图一局（三人共斗、Boss 潮汐骑、黑潮涌浪、割草构筑）。
- 网页版没有可写磁盘，局内 CSV 跑局记录自动停写，不影响游戏。
- 中文字体：浏览器没有系统字体，构建内嵌了 Noto Sans SC（SIL OFL 1.1）。
- 资源包体积约 130 MB，为规避 GitHub 单文件 100 MB 限制，数据文件切成 `part0` / `part1`，由 `index.html` 合并成 Blob 后再交给 Unity 加载。

## 当前状态（2026-11-23）

- 能加载、能进主菜单、能开局：HUD、小地图、增益、伤害数字、中文全部正常。
- 已知问题：3D 场景（地面/废墟/场景道具）在浏览器里渲染成黑色，只剩角色与 UI 可见；原因是自定义 `BlackTide/*` 着色器在 WebGL(gles3) 下的表现，正在修。

## 源码

Unity 工程源码：<https://github.com/stockholm754-source/black-tide-defense>
