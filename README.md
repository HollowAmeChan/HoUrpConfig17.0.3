# Ho Universal Render Pipeline Config 17.0.3

这个包是 Hollow 本地 URP 系统使用的配置包。它提供 URP shader 配置常量，并把这些常量同时生成到 C# 和 HLSL。

## 在整套系统里的定位

`HoUrpConfig17.0.3` 与 `HoUrp17.3.0` 配套使用。

当前定义的 URP shader 选项包括：

- 低端移动平台最大可见灯光数：`16`
- 移动平台 / WebGPU 最大可见灯光数：`32`
- 桌面平台最大可见灯光数：`256`
- 是否把 fog keyword 切换成动态分支：`0`

这些值会进入 URP shader 编译路径，因此会影响整套 Unity 项目的 shader variant 和运行时灯光上限。

## 重要文件

- `Runtime/ShaderConfig.cs`：带 `[GenerateHLSL]` 的 C# 配置源。
- `Runtime/ShaderConfig.cs.hlsl`：自动生成的 HLSL include。
- `Runtime/Unity.RenderPipelines.Universal.Config.Runtime.asmdef`：runtime 程序集定义。
- `Tests/Editor/ConfigurationTest.cs`：编辑器侧配置验证。
- `Documentation~/`：Unity package 文档入口。

## 安装

通常与本地 URP 包一起使用：

```json
{
  "dependencies": {
    "com.unity.render-pipelines.universal": "file:D:/Unity_Fork/HoUrp17.3.0",
    "com.unity.render-pipelines.universal-config": "file:D:/Unity_Fork/HoUrpConfig17.0.3"
  }
}
```

## 重新生成 shader include

不要手改 `Runtime/ShaderConfig.cs.hlsl`。需要改配置时，先改 `Runtime/ShaderConfig.cs`，然后在 Unity 中执行：

```text
Edit > Rendering > Generate Shader Includes
```

提交时应同时提交 C# 源文件和重新生成的 HLSL 文件。
