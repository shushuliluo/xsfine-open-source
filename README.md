# XSFiNE 第三方组件源码

本仓库提供 XSFiNE 使用的第三方组件源码快照、许可证和版本信息，供用户获取源码、查阅授权条款，以及开发者参考上游实现。

## 组件版本

当前收录以下 PDF 组件，版本均为 `0.1.1`：

| 组件 | 源码 | 许可证 |
| --- | --- | --- |
| `@toeverything/pdfium` | [packages/pdfium](vendor/pdfium-builder/packages/pdfium) | MPL-2.0 |
| `@toeverything/pdf-viewer` | [packages/pdf-viewer](vendor/pdfium-builder/packages/pdf-viewer) | MPL-2.0 |
| `@toeverything/pdf-viewer-types` | [packages/types](vendor/pdfium-builder/packages/types) | MPL-2.0 |

源码来自 [toeverything/pdfium-builder](https://github.com/toeverything/pdfium-builder)，固定于提交 [`858b43b8`](https://github.com/toeverything/pdfium-builder/tree/858b43b88a030c2aff1d44908deadb9443032500)。`vendor/pdfium-builder/` 保留该提交的完整源码，包括构建脚本、补丁、示例与测试资源；上游文件未经修改。

## 获取与使用

你可以直接浏览 [源码目录](vendor/pdfium-builder)，或克隆本仓库：

```sh
git clone https://github.com/shushuliluo/xsfine-open-source.git
```

也可以下载[对应提交的上游源码归档](https://codeload.github.com/toeverything/pdfium-builder/tar.gz/858b43b88a030c2aff1d44908deadb9443032500)。该归档的 SHA-256 为：

```text
f1e81f940ba683a6ba9ca776e94a5d1883a45d4ec0276b52f1a6b0ba69bbfd04
```

构建与开发说明见[上游 README](vendor/pdfium-builder/README.md)。源码归档、各文件校验值及 npm 发布信息见 [SOURCE-MANIFEST.json](SOURCE-MANIFEST.json)。

## 许可与版权

组件的授权条款、版权声明及源码获取说明见 [NOTICE.md](NOTICE.md)；MPL-2.0 全文见 [licenses/MPL-2.0.txt](licenses/MPL-2.0.txt)。使用、修改或分发组件时，请遵守对应文件及组件的许可证。第三方组件的版权归各自权利人所有。

## AFFiNE 原生公共组件

[`vendor/affine-native/`](vendor/affine-native/) 提供 AFFiNE `affine_common` crate 的原始源码，来自固定提交 [`4a7c931ecaf140adfb265962b1e92a465781b143`](https://github.com/toeverything/AFFiNE/tree/4a7c931ecaf140adfb265962b1e92a465781b143/packages/common/native)。该目录完整保留上游 `packages/common/native/` 的 48 个文件，包括测试素材，未作修改。

该组件的[原始许可](vendor/affine-native/LICENSE)对随 AFFiNE Community Edition 分发的部分适用 MPL-2.0；[MPL 正文](licenses/AFFiNE-native-MPL-2.0.txt)一并提供。其他部分仍按原始许可的范围处理。本目录只包含 `affine_common`，不包含整个 Electron 应用或其他原生 crate。来源及逐文件校验值见 `SOURCE-MANIFEST.json` 的 `nativeSources`。

## 字体许可

Inter、Kalam、Poppins 等字体的版权与完整 OFL 文本见[字体许可目录](licenses/fonts)。该目录提供许可通知，不包含字体文件。

## 源码范围

上述 PDF 源码目录收录的是 `pdfium-builder` 项目及其三个 npm 包对应的上游源码快照。PDFium 引擎源码和构建工具链由上游构建脚本另行获取，不包含在这个快照中。

上游脚本默认使用 `chromium/6666`；该默认分支不能确定 npm 发布的 WASM 二进制实际采用的 PDFium 提交、依赖和工具链版本。因此，此快照不提供该 WASM 二进制的完整可复现构建环境。详细版本信息见 [来源清单](SOURCE-MANIFEST.json#pdfiumBinaryProvenance)。

## 反馈

如果你发现源码链接、组件版本或许可说明存在问题，请通过本仓库的 [Issues](https://github.com/shushuliluo/xsfine-open-source/issues) 反馈，并注明组件名称与版本。请勿在公开议题中提交个人信息或私人文档。
