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
| [HoTools](https://github.com/HollowAmeChan/HoTools) | Blender 角色、模型、贴图、动画与自动化工具 |
| [HoGLTF](https://github.com/HollowAmeChan/HoGLTF) | Blender glTF 导出与 Ho 材质契约桥接 |
| [HoUrp17.3.0](https://github.com/HollowAmeChan/HoUrp17.3.0) | URP 渲染基座 |
| [lilToon](https://github.com/HollowAmeChan/lilToon) | 角色 / NPR 着色器 |
| [lilToon-URP-Extensions](https://github.com/HollowAmeChan/lilToon-URP-Extensions) | 光照、阴影、反射与后处理扩展 |
| [lilToon-UnityGLTF-Extensions](https://github.com/HollowAmeChan/lilToon-UnityGLTF-Extensions) | glTF 材质契约导入 |
| [HoUnityTools](https://github.com/HollowAmeChan/HoUnityTools) | 角色、动画与创作工具 |

## 可选材质合集

- [HoShader](https://github.com/HollowAmeChan/HoShader)：宝石、皮肤、绒毛等独立材质与 Shader 实验合集，按需选用。
