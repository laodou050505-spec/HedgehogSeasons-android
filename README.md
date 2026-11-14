# 刺猬的四季 — Android Gradle 工程（Unity 导出）

本仓库是 Unity 工程用 Export Project 在本地导出的 Android Gradle 工程，供云端打包使用。
Unity 源码工程在 [HedgehogSeasons](https://github.com/laodou050505-spec/HedgehogSeasons)，本工程由其提交 `81454c03cdf068a3390340d7d8c77ae34a3b1f02` 导出。

- Unity 6000.5.5f1，脚本后端 IL2CPP
- IL2CPP 已预编译：libil2cpp.so 在 unityLibrary/src/main/jniLibs/arm64-v8a，工程中已不含 Il2CppOutputProject，打包时不编译 IL2CPP
- 目标架构只有 arm64-v8a，不导出调试符号（debugSymbolLevel none）
- compileSdk / targetSdk 36，minSdk 29
- 包名 `com.hedgehog.seasons`，版本 0.1.1107

构建：`gradle assembleRelease`，产物在 `launcher/build/outputs/apk/release/`。
`local.properties` 未提交，请按构建环境设置 Android SDK 路径。
