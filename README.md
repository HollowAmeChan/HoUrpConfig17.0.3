# Ho Universal Render Pipeline Config 17.0.3

Ho 渲染体系的 URP Shader 配置包，与 HoUrp17.3.0 配套使用。

## 功能

- **灯光上限配置**：定义低端移动、移动 / WebGPU 与桌面平台的最大可见灯光数。
- **雾计算配置**：控制雾关键字是否采用动态分支。
- **跨语言配置同步**：由 C# 配置源生成 HLSL 常量，供 URP 运行时与 Shader 共用。

配置源见 [ShaderConfig.cs](Runtime/ShaderConfig.cs)。

## Ho 渲染体系相关仓库

| 仓库 | 用途 |
| --- | --- |
| [HoUrp17.3.0](https://github.com/HollowAmeChan/HoUrp17.3.0) | URP 渲染基座 |
| [lilToon-URP-Extensions](https://github.com/HollowAmeChan/lilToon-URP-Extensions) | 光照、阴影、反射与后处理扩展 |
| HoShader | 下一代材质底座，项目正在迁移，仓库目前为私有 |
| [HoUnityTools](https://github.com/HollowAmeChan/HoUnityTools) | 角色、动画与创作工具 |

## 日期版本与安装包

推送默认分支后自动发布日期版本（`YYYYMMDD-HHMMSS`）与 Unity 安装包；在 GitHub Releases 下载 `.tgz`，通过 Package Manager 从 tarball 安装。版本对齐、手动发布与安装说明见 [发布说明](.github/RELEASING.md)。
