**该文件夹下存放 mpv 的脚本**

以下为脚本及功能介绍

| 脚本名 | 简要说明 |
| --- | --- |
| autoload.lua | 自动加载同级目录的文件（配置文件 [autoload.conf](../script-opts/autoload.conf)） |
| autodeint.lua        | 自动检测去交错（默认禁用，需快捷键启用）       |
| autosave.lua         | 每隔1分钟自动保存进度（而不是退出时）    |
| bookmarker-menu.lua  | 书签菜单（配置文件 [bookmarker_menu.conf](../script-opts/bookmarker_menu.conf)） |
| boss-key.lua         | 老板键                                   |
| change-refresh.lua   | 更改刷新率（配置文件 [changerefresh.conf](../script-opts/changerefresh.conf)） |
| channel_mixer.lua    | 调节各通道音                             |
| chapter_list.lua | 章节列表（依赖 [scroll-list.lua](../script-modules/scroll-list.lua)） |
| chapterskip.lua | 跳过指定章节（配置文件 [chapterskip.conf](../script-opts/chapterskip.conf)） |
| copy_subortime.lua | 复制当前字幕内容或播放时间 |
| cycle_adevice.lua | 快捷键切换音频输出设备 |
| delete_file.lua | 退出时删除标记文件 |
| dynamic-crop.lua | 自动检测黑边并裁切（[autocrop.lua](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autocrop.lua) 改进版；配置文件 [dynamic_crop.conf](../script-opts/dynamic_crop.conf)） |
| exit-fullscreen.lua | 播放列表结束后退出全屏 |
| file-browser.lua | 内置文件浏览器（依赖 [user-input.lua](../scripts/user-input.lua);[user-input-module.lua](../script-modules/user-input-module.lua) ；配置文件 [file_browser.conf](../script-opts/file_browser.conf)） |
| fuzzydir.lua | 外挂音轨/字幕路径检测增强 |
| history-bookmark.lua | 记录并恢复视频目录播放记录（可确认是否恢复该目录上次播放进度） |
| local-language.lua | OSD 显示本地化 |
| manager.lua | 一键更新指定脚本和着色器（配置文件 [manager.json](../manager.json)） |
| menu.lua | 简易自定义菜单（依赖 [scroll-list.lua](../script-modules/scroll-list.lua)；配置文件 [menu.json](../script-opts/menu.json)） |
| mpv-webp.lua | 剪切指定片段为 webp 动图（依赖 ffmpeg；配置文件 [webp.conf](../script-opts/webp.conf)） |
| onedrive-hook.lua | 转换 onedrive 共享链接为播放链接 |
| ontop_playback.lua            | 仅在播放时启用置顶                                           |
| open-file-dialog.lua | 快捷键载入文件                                               |
| ordered-chapters-playlist.lua | 有序章节播放列表 |
| pause-when-minimize.lua | 最小化时暂停播放 |
| playlistmanager.lua | 高级播放列表（配置文件 [playlistmanager.conf](../script-opts/playlistmanager.conf)） |
| recent.lua | 播放记录菜单（配置文件 [recent.conf](../script-opts/recent.conf)） |
| segment-linking.lua | 实现对 matroska [硬段链接](https://www.ietf.org/archive/id/draft-ietf-cellar-matroska-06.html#name-hard-linking) 的支持 |
| skiptosilence.lua | 跳至播放文件的下一个静音位置（另类地实现跳 op 的方法；配置文件 [skiptosilence.conf](../script-opts/skiptosilence.conf)） |
| slicing_copy.lua | 剪切视频片段（依赖 ffmpeg；配置文件 [slicing_copy.conf](../script-opts/slicing_copy.conf)） |
| SmartHistory.lua              | 恢复最后的播放记录并播放                                       |
| SmartCopyPaste-II.lua         | 智能复制粘贴视频路径及进度                                   |
| sub-select.lua | 指定字幕轨道优先级/黑白名单（配置文件 [sub_select.conf](../script-opts/sub_select.conf)；[sub-select.json](../script-opts/sub-select.json)） |
| Thumbnailer*.lua          | 缩略图引擎(依赖 [Thumbnailer_OSC.lua](../scripts/Thumbnailer_OSC.lua)；配置文件 [thumbnailer.conf](../script-opts/thumbnailer.conf)) |
| Thumbnailer_OSC.lua           | 缩略图引擎搭配的 OSC 界面（配置文件 [Thumbnailer_OSC.conf](../script-opts/Thumbnailer_OSC.conf)） |
| trackselect.lua               | 指定音频轨道优先级/黑白名单（配置文件 [trackselect.conf](../script-opts/trackselect.conf)） |
| UndoRedo.lua                  | 智能跳跃记录操作                                             |
| user-input.lua                | [功能扩展插件](https://github.com/CogentRedTester/mpv-user-input) |

1. 部分脚本为**个人修改版本**，主要改进功能实现或键位绑定方式。如：bookmarker-menu.lua; boss-key.lua; chapter_list.lua; chapterskip.lua; copy_subortime.lua; fuzzydir.lua; local-language.lua; menu.lua; skiptosilence.lua; SmartHistory.lua; SmartCopyPaste-II.lua
2. 所有脚本预绑定的静态键位已被 [mpv.conf](../mpv.conf) 中的`input-default-bindings=no`参数屏蔽，可查看 [input.conf](../input.conf)  的"LUA 脚本"部分示例参考绑定所需键位  
   - 本配置绑定的快捷键及功能请参考 [快捷键.md](../快捷键.md) 文件
3. 部分脚本存在动态绑定键位，可查看对应脚本及配置文件相关部分（或[快捷键.md](../快捷键.md)中相关说明）
4. **MPV已知问题**：当 scripts 文件夹内脚本绑定的`mp.add_key_binding`总数超过一定阈值时，会导致 osc.lua 交互功能失效。本配置已针对该问题进行脚本优化
