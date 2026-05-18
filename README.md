# bbccc

[English](README.en.md)

基于浏览器和 ChArUco 标定板的相机标定工具。

bbccc 目前是一个单页面工具，可以在浏览器中生成可打印的 ChArUco 标定板、采集相机样本、调用 OpenCV.js 完成相机标定，并导出 JSON 格式的标定结果。

项目名 `bbccc` 来自 “browser-based ChArUco camera calibration”。这个名字主要是为了仓库和链接简洁；工具本身会尽量保持直接：打开页面、打印标定板、采集样本、执行标定。

## 使用

打开 GitHub Pages 页面：

https://a7t.ink/bbccc/

也可以下载 `docs/index.html` 后在本地浏览器中打开。

如果需要访问摄像头，推荐使用 HTTPS 页面。本地文件能否直接访问摄像头取决于浏览器的安全策略。

## 功能

- 在浏览器中加载 OpenCV.js。
- 生成可打印的 ChArUco 标定板。
- 检查标定板是否能放入 A4 等常见纸张。
- 导出高分辨率 PNG 和 1:1 PDF 标定板。
- 通过 USB 摄像头采集标定样本。
- 按标定板面积、Marker 数量、ChArUco 角点数量和视角多样性筛选样本。
- 在浏览器中执行相机标定。
- 导出 JSON 格式的标定结果。

## 隐私

摄像头画面在浏览器本地处理。工具不会把相机图像或采集样本上传到服务器。

当前版本会从 CDN 加载第三方 JavaScript 依赖，包括 OpenCV.js 和 jsPDF。未来版本可能会提供更自包含的单文件构建。

## 开发

当前版本刻意保持简单：

```text
docs/
  index.html
  .nojekyll
```

GitHub Pages 可以设置为从 `main / docs` 发布。

项目未来可能迁移到现代前端工具链，但保持方便的浏览器使用体验，并尽量提供单文件分发，是一个设计目标。

## 许可证

MIT License。见 `LICENSE`。
