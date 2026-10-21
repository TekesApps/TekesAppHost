# TekesAppHost

共享原生 App 宿主框架：一套 Host 源码，构建时固定模块组合，产出不同 target apps。

每个窗口采用 `left / middle / right` 三列，每列由 `toolbar + content` 组成。每个 Panel 使用独立模块进程运行预定的 content WASM；content 向 Host 注册本列 toolbar。Host 使用 native TekesUI 的 Panel、toolbar 和 splitter 组件呈现三列布局，合成模块的内容画面，并路由输入、事件与请求。

## 当前状态

设计阶段，尚无实现代码、可运行宿主或性能验证。本文不承诺现有 TekesUI 已支持 WASM、跨进程 GPU 共享或完整输入桥接。

- [框架设计](docs/design/architecture.md)
- [MIT License](LICENSE)

本仓库仅定义通用 Host，不规定具体业务模块目录或业务数据结构。TekesUI 保持独立的通用 UI 库。
