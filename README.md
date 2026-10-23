# breeze-binary

Rossi / Breeze 的模型与二进制资源托管。应用按需从这里下载，不随 APK 打包。

## realsr-qnn-android.7z

Android 端 QNN（Qualcomm HTP NPU）超分模型包，应用内「设置 → 超分」选择
NPU 引擎后首次使用时自动下载，解压到 `super_resolution/qnn/`。
也可手动下载后从设置页导入。

- `qnn/manifest.json` — 各 DLC 的 SHA-256 清单（应用编译上下文前的完整性判据）
- `qnn/realcugan-se-x2-no-denoise.dlc` — Real-CUGAN SE 2×（无降噪），默认模型
- `qnn/realcugan-pro-x2-denoise3x.dlc` — Real-CUGAN Pro 2×（降噪 3 档）

**SHA-256（整个 7z）**

```
ab28e6938c7ce4c724689dda07fdfc048929bb37b0188c9dd84a682ca5ed50d6
```

**来源与许可**：FP16 DLC 提取自
[HaoweiLi97/mihon_img_upscale](https://github.com/HaoweiLi97/mihon_img_upscale)
v1.3.16 发布包（Apache License 2.0，上游由 QAIRT 2.49.0 从 ONNX 转换）。
重新提取与打包方法见 rossi 仓 `script/models/package_qnn_models.py`。
