# Gao_Aquatic_Autopilot

[![License](https://img.shields.io/badge/License-Commercial%20Proprietary-red.svg)](LICENSE)
[![C++](https://img.shields.io/badge/C%2B%2B-20-blue.svg)](https://isocpp.org/)
[![Version](https://img.shields.io/badge/version-5.0.0-brightgreen.svg)](.version)

Gao_Aquatic_Autopilot 是 4A 系统的水域空间分支，专为水面无人船（USV）和水下潜航器（AUV/ROV）设计。

## 支持构型
- Q-1 水面航行：三自由度运动学（纵荡、横摇、偏航）+ 视线法引导控制
- Q-2 水下潜航：四自由度动力学（纵荡、横荡、垂荡、偏航）+ 深度/航向控制

## 依赖
- Gao_4A_Autopilot（基座）

## 构建与运行
```bash
./build_all.sh
./build/gao_autopilot
```
## 切换构型
修改 `edge/config/morphology.yaml` 文件，例如：
```yaml
morphology: "Q-2"   # Q-1 或 Q-2
```

## 目录结构
```text
edge/
├── morphologies/Q-1/  # USV 动力学与控制器
├── morphologies/Q-2/  # AUV 动力学与控制器
├── shared/            # 波浪补偿、水下导航
├── safety/            # 漏水检测、深度超限
└── hardware/          # 推进器、水深传感器驱动
```

## 许可证
商业专有。

## 作者
Yongji Gao
Email: bonaventure@163.com
