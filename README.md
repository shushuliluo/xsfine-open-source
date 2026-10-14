# XSFiNE 开源组件源码与许可材料

本仓提供本地 XSFiNE 0.5.0 发行材料核查涉及的三个 PDF 包 `0.1.1` 的固定上游源码、许可证与获取信息。它是独立的公开组件源码仓库，不包含 XSFiNE 产品源码、私有 Git 历史、账号数据、部署配置、签名材料或产品字体，也不是整个应用的合规证明。

## 包与固定源码

| npm 包 | 版本 | 上游源码目录 |
| --- | --- | --- |
| `@toeverything/pdfium` | `0.1.1` | `vendor/pdfium-builder/packages/pdfium/` |
| `@toeverything/pdf-viewer` | `0.1.1` | `vendor/pdfium-builder/packages/pdf-viewer/` |
| `@toeverything/pdf-viewer-types` | `0.1.1` | `vendor/pdfium-builder/packages/types/` |

官方 npm 元数据均声明 `MPL-2.0`，并指向 `toeverything/pdfium-builder` 的提交 [`858b43b88a030c2aff1d44908deadb9443032500`](https://github.com/toeverything/pdfium-builder/tree/858b43b88a030c2aff1d44908deadb9443032500)。`vendor/pdfium-builder/` 原样保留该提交的完整 64 个文件，包括构建脚本、WASM 补丁、示例及两个上游测试 PDF；没有混入用户文档或产品字体文件。上游文件未作修改。

`SOURCE-MANIFEST.json` 记录源码下载地址、压缩包与逐文件 SHA-256、三个官方 npm tarball 的 SHA-1/SHA-256/SHA-512 integrity，以及许可文件来源。`metadata/npm/` 保留获取时的官方版本元数据。下载核验了三个 tarball 的官方 integrity；其中 viewer 的 6 个 `src/` 文件和 types 的 1 个 `src/` 文件与固定快照逐字节相同。`pdfium` npm 包只有生成产物，不能据此证明其完整底层源码版本。本仓不重新分发 npm 二进制。

## 许可证与原版权

三个发布包及上游测试资源包的 `package.json` 声明 MPL-2.0；正文保存在 [`licenses/MPL-2.0.txt`](licenses/MPL-2.0.txt)，来源是 [Mozilla 官方文本](https://www.mozilla.org/media/MPL/2.0/index.txt)。原始文件、版权和许可声明均保留；参见 [`NOTICE.md`](NOTICE.md)。

固定上游提交没有根 LICENSE 文件。这里没有将一份总许可证覆盖上游全部文件，也没有把 PDFium 及其其他第三方依赖统一改成 MPL-2.0。具体文件继续以各自原始通知、所属包声明及权利人许可为准。

## 底层 PDFium 仍待闭环

固定上游 `justfile` 与 GitHub Action 的默认值是 `PDFIUM_VERSION=6666`，构建会拉取 `origin/chromium/6666` 并应用本仓保留的补丁。默认值不是实际 `0.1.1` 发布二进制所用 revision 的证明。

本次从 PDFium 官方 Gitiles 查询该默认分支，解析为 [`94fb006b18bec0f1c18fa0d1692214a46ab88442`](https://pdfium.googlesource.com/pdfium/+/94fb006b18bec0f1c18fa0d1692214a46ab88442)。该固定提交的 LICENSE 原文保存在 [`licenses/reference/PDFium-chromium-6666-LICENSE.txt`](licenses/reference/PDFium-chromium-6666-LICENSE.txt)，含 PDFium BSD 通知及 Apache-2.0 正文，**仅作候选参考**。它不证明 npm WASM 的实际 revision，也不包含完整 DEPS 第三方许可闭包。

仍需向上游取得发布构建的准确 PDFium commit、DEPS/第三方 revision、工具链版本及对应源码和完整通知，再与发布产物对应。现在不能声称本仓已经提供完整 WASM 对应源码、可以重现原发布产物，或已经完成底层许可合规。

## 获取源码

固定上游完整源码可直接从 [GitHub 源码归档](https://codeload.github.com/toeverything/pdfium-builder/tar.gz/858b43b88a030c2aff1d44908deadb9443032500) 下载，也可读取本仓 `vendor/pdfium-builder/`。源码归档 SHA-256 为：

```text
f1e81f940ba683a6ba9ca776e94a5d1883a45d4ec0276b52f1a6b0ba69bbfd04
```

本仓不运行或启用被保留的上游 CI。公开入口为 https://github.com/shushuliluo/xsfine-open-source 。应用内开源通知应提供本仓地址和对应版本的固定提交。
