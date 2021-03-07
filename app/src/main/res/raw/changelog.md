# alpha更新日志

## Magisk (7717f0a6-alpha)
- 基于 7717f0a6 ，相关修改参考上游更新日志
- 正确处理来自magiskd的任何数据
- 支持SharedUserId
- 还原boot镜像后删除备份文件
- 内置当前版本更新日志
- 当无法下载stub时使用本地版本，现在Magisk可以完全离线使用
- 支持bootimg v4格式

### 如何在Recovery使用APK文件？
一般情况建议通过Magisk应用来安装和卸载Magisk。
如果坚持使用自定义Recovery，将Magisk APK文件的`.apk`扩展名改为`.zip`即可刷入。
要卸载Magisk，zip文件名需要包含`uninstall`，例如将apk文件重命名为`uninstall.zip`。文件名不包含`uninstall`则会进行安装操作。

# 上游更新日志

## 2021.5.12 Magisk v23.0

This release is focused on fixing regressions and bugs.

Note: Magisk v22 is the last major version to support Jellybean and Kitkat. Magisk v23 only supports Android 5.0 and higher.

### Bug Fixes

- [App] Update snet extension. This fixes SafetyNet API errors.
- [App] Fix a bug in the stub app that causes APK installation to fail
- [App] Hide annoying errors in logs when hidden as stub
- [App] Fix issues when patching ODIN tar files when the app is hidden
- [General] Remove all pre Android 5.0 support
- [General] Update BusyBox to use proper libc
- [General] Fix C++ undefined behaviors
- [General] Several `sepolicy.rule` copy/installation fixes
- [MagiskPolicy] Remove unnecessary sepolicy rules
- [MagiskHide] Update package and process name validation logic
- [MagiskHide] Some changes that prevents zygote deadlock

### Full Changelog: [here](https://topjohnwu.github.io/Magisk/changes.html)
