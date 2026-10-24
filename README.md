# Asphalt 游戏资源工作流

目标：研究游戏模型与贴图的提取、格式转换、Blender 编辑和渲染，以及经验证支持的资源回导。

## 候选源码与工具

| 项目 | 用途 | 适用范围与验证状态 |
| --- | --- | --- |
| [Game-Engines-Filetypes-Reverse-Engineering](https://github.com/lOlbas/Game-Engines-Filetypes-Reverse-Engineering) | Gameloft 格式的读取脚本与二进制结构模板 | 研究项目；包含 BDAE 等格式资料。尚未在本项目中测试。 |
| [oac-bdae-parser](https://github.com/pixel3rr0r/oac-bdae-parser) | C++ BDAE 解析与 OpenGL 模型查看 | 作者针对 Order and Chaos Online 4.2.5a 的 BDAE 0.0.0.779；不代表支持 Asphalt。尚未测试。 |
| A9Tool（历史工具线索） | Asphalt 9 模型、贴图转换调查入口 | 未确认源码许可证、当前版本兼容性、回导能力；不作为可用依赖。 |

A9Tool 历史讨论入口：[Asphalt 9 Legends jmodel dump](https://reshax.com/topic/423-asphalt-9-legends-jmodel-dump/)。这是调查线索，不是经过验证的下载来源。

## 当前状态

本仓库目前保存项目说明和候选工具来源，尚未包含第三方实现、可运行转换器或游戏资源。
两份候选源码项目的许可证尚未确认；此次未能读取其根目录 LICENSE，不能由此断言不存在其他许可证文件。复制或修改源码前需进一步核对授权条款并保留要求的声明。

## 实际处理流程

1. 记录游戏名称、版本、平台和原文件路径；保留原件，在副本上操作。
2. 检查文件头与格式版本，区分封包、模型和贴图，不通过改后缀模拟转换。
3. 根据实际格式匹配解析器，先验证单个样本，再进行批量处理。
4. 导入 Blender，核对网格、UV、材质、骨骼、层级、比例和坐标轴。
5. 按需求编辑、渲染或导出通用格式，并重新导入检查结果。
6. 仅在有匹配的写入器或打包器且验证通过时尝试游戏资源回导；解析或提取成功不代表能回导。
7. 替换前备份并记录文件校验值，失败时恢复原件。

## 下一步所需样本

- 游戏名称与确切版本。
- PC、安卓或 iOS 平台。
- 一个原始模型或封包文件及其关联贴图。
- 目标：提取渲染、转换通用格式，或替换回游戏。
