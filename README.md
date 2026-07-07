# TornadoScope 🌪️

**龙卷风灾损智能检测研究平台**

---

融合深度学习目标检测、零样本标注与无人机航测技术，构建覆盖中美 17 场龙卷风事件的灾损影像数据库，实现灾后建筑损伤的自动化识别、分级与空间分析。

## 🔬 核心能力

- **多源数据融合** — TornadoNet 公开数据集 + 自采无人机航拍 + 社交媒体灾情影像
- **零样本自动标注** — Grounding DINO 文本提示检测，生成 1,850 个灾损标注框
- **YOLOv8n 模型** — 轻量级网络，支持 DS0–DS4 五级建筑损伤分类
- **无人机正射测绘** — OpenDroneMap 拼接 496 张航拍影像生成地理配准正射图
- **GIS 空间分析** — 检测结果空间叠加 + Leaflet 交互地图

## 📊 数据规模

| 指标 | 数量 |
|------|------|
| 龙卷风事件 | 17（中美） |
| 灾损影像 | 1,278 |
| 人工标注 | 2,728 |
| AI 检测框 | 1,850 |
| 无人机航拍 | 496 |
| 灾损类别 | 9 |

## 🛠 技术栈

`YOLOv8` `Grounding DINO` `OpenDroneMap` `SQLite` `Leaflet` `ECharts` `Python`

## 🚀 部署

纯静态页面，双击 `index.html` 即可本地预览。或通过任意静态托管服务部署：

```bash
# 本地预览（推荐，解决视频自动播放）
cd website
python -m http.server 8080
# 浏览器打开 http://localhost:8080
```

## 📂 项目结构

```
website/
├── index.html          # 主页面（NVIDIA 设计系统风格）
└── assets/
    ├── tornado_funnel.mp4    # Hero 龙卷风视频
    ├── orthophoto_preview.jpg # 正射影像预览
    ├── *_detection*.jpg       # AI 检测样例
    └── *.png                  # 数据可视化图表
```

## 📝 许可

MIT License
