# WebMapsByLeaflet

基于 Leaflet 的交互式地图应用，支持多图源切换、坐标系转换、GPS定位和距离测量功能。

## 功能特性

- **多图源支持**：Google卫星镜像、ArcGIS卫星、Google卫星
- **坐标系支持**：WGS-84 和 GCJ-02 双坐标系自动转换
- **坐标显示**：实时显示鼠标位置经纬度（度分秒格式）
- **坐标复制**：一键复制当前坐标到剪贴板
- **GPS定位**：浏览器定位功能，自动转换坐标系
- **距离测量**：多点距离测量工具，支持公里/米单位切换
- **响应式设计**：适配桌面和移动设备

## 项目结构

```
WebMapsByLeaflet/
├── index.html          # 主应用文件
├── lib/leaflet/        # Leaflet 库文件
│   ├── leaflet.js
│   ├── leaflet.css
│   └── svg/           # 图标资源
├── run.bat             # 启动脚本
└── LICENSE             # 许可证文件
```

## 使用说明

### 启动应用
1. 双击运行 `run.bat` 或在命令行执行：
   ```bash
   python -m http.server 80
   ```
2. 在浏览器中访问 `http://localhost`

### 地图操作
- **左键点击**：固定当前坐标位置
- **右键点击**：取消固定坐标
- **鼠标移动**：实时显示当前坐标

### 工具栏功能
- **图层选择**：切换不同地图源
- **坐标徽标**：显示当前坐标系（WGS-84/GCJ-02）
- **复制按钮**：复制固定坐标或定位坐标
- **GPS按钮**：定位到当前位置
- **图钉按钮**：固定/取消固定坐标
- **尺子按钮**：进入/退出测量模式

### 测量模式
1. 点击尺子按钮进入测量模式
2. 左键点击添加测量点
3. 右键拖拽平移地图
4. 再次点击尺子按钮退出测量

## 技术栈

- **Leaflet** v1.9.4：开源地图库
- **坐标转换算法**：WGS-84 ↔ GCJ-02 标准转换
- **浏览器API**：Geolocation API、Clipboard API

## 许可证

GNU Affero General Public License v3.0 - 详见 [LICENSE](LICENSE) 文件

## 致谢

- [Leaflet](https://github.com/Leaflet/Leaflet) - 开源地图库