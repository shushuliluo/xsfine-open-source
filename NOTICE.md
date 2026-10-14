# 第三方组件许可通知

以下 PDF 组件采用本节所述许可证：

- `@toeverything/pdfium`，版本 `0.1.1`
- `@toeverything/pdf-viewer`，版本 `0.1.1`
- `@toeverything/pdf-viewer-types`，版本 `0.1.1`

三个组件的 npm 发布信息均标明作者为 `toeverything`，许可证为 `MPL-2.0`。各文件中的原始版权、许可声明和免责声明保留在 [源码目录](vendor/pdfium-builder) 中。

## Mozilla Public License 2.0

对于上游采用 MPL-2.0 授权的源码，适用以下通知：

> This Source Code Form is subject to the terms of the Mozilla Public License, v. 2.0. If a copy of the MPL was not distributed with this file, You can obtain one at https://mozilla.org/MPL/2.0/.

[阅读 MPL-2.0 全文](licenses/MPL-2.0.txt)。你可以依照该许可证获取、使用、修改和分发其覆盖的源码；本通知不减少或替代许可证赋予你的权利。

## 获取源码

源码位于 [vendor/pdfium-builder](vendor/pdfium-builder)，上游提交为 [`858b43b88a030c2aff1d44908deadb9443032500`](https://github.com/toeverything/pdfium-builder/tree/858b43b88a030c2aff1d44908deadb9443032500)，未经修改。下载地址、发布包元数据与校验值见 [SOURCE-MANIFEST.json](SOURCE-MANIFEST.json)。

## PDFium 及其他依赖

PDFium 引擎及其依赖按各自许可证授权，不能统一视为 MPL-2.0 组件。

[PDFium 许可参考文本](licenses/reference/PDFium-chromium-6666-LICENSE.txt) 来自官方提交 `94fb006b18bec0f1c18fa0d1692214a46ab88442`，对应上游构建脚本默认分支。该文本仅描述这一参考版本，不代表 npm WASM 发布文件中全部依赖的许可证清单。源码与构建环境的覆盖范围见 [README](README.md#源码范围)。

## 字体

字体按各自的 SIL Open Font License 1.1 授权。完整许可和版权记录见[字体许可目录](licenses/fonts)；它们不适用上面的 MPL-2.0 通知。具体字体是否包含于某一应用版本，以该版本随附的通知为准。

## AFFiNE affine_common 原生组件

Copyright (c) 2022-present TOEVERYTHING PTE. LTD. and its affiliates.

对应源码在 [vendor/affine-native/](vendor/affine-native/)，上游固定提交为 `4a7c931ecaf140adfb265962b1e92a465781b143`，原路径为 `packages/common/native/`。原始许可保存在该目录的 [LICENSE](vendor/affine-native/LICENSE)：其 Community Edition 范围适用 MPL-2.0，其余范围继续依原始条款。MPL 正文见 [licenses/AFFiNE-native-MPL-2.0.txt](licenses/AFFiNE-native-MPL-2.0.txt)。

该源码快照未作修改，保留原版权及许可通知。
