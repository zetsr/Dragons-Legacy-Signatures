# Dragons-Legacy-Signatures

### 2025/3/17

目前所有特征码均能扫描成功。

### *string* game_version
`只能在主菜单扫`

`42 75 69 6C 64 20 ?? 2E` = `Build ?.`

### *string* local_player_steam_name
`无法处理名称包含Unicode字符的情况`

`00 00 70 03 ?? ?? ?? ?? 00 00 00 00 00 00 00 00 00 00 0B + 0x14`

### *float* view_distance
~~`有时候不稳定，需调查。`~~

~~`00 ?? ?? ?? 00 00 96 43 00 00 C8 42 00 00 96 44`~~

`使用这个->` `00 ?? ?? [42-44] 00 00 96 43 00 00 C8 42 00 00 96 44`

### *float* fps_max
`?? ?? ?? ?? 00 00 70 42 74 00 2E 00 4D 00 61 00 78`

### *float* render_distance <sup>0=No-Foliage</sup>
`?? ?? ?? ?? ?? ?? ?? ?? 00 00 00 00 00 00 80 3F 00 00 00 00 00 00 34 42 00 00 80 3F`

### *float* local_player_health <sup>info<sup>
`不稳定，需调查。`

`行不通，失效实体的内存不会被释放，所有东西都是过时的。`

~~`?? ?? ?? ?? ?? ?? ?? ?? E6 79 ?? ?? ?? 00 03 00`~~

### *byte* local_player_SkinIndex <sup>info<sup>
`local_player_health - 0x4`

### *byte* local_player_Gender <sup>info<sup>
`local_player_health - 0x3`

### *float* local_player_armor <sup>info<sup>
`local_player_health + 0x4`

### *byte* local_player_stamina <sup>info<sup> <sup>无限耐力<sup> 
`local_player_health + 0x8`

### *byte* local_player_bile <sup>info<sup>
`local_player_health + 0x9`

### *byte* local_player_hunger <sup>info<sup>
`local_player_health + 0xA`

### *byte* local_player_thirsty <sup>info<sup>
`local_player_health + 0xB`

### *byte* local_player_disease <sup>info<sup>
`local_player_health + 0xC`

### *byte* local_player_stats_VitalityHealth <sup>info<sup>
`local_player_health + 0x1C`

### *byte* local_player_stats_OverallQuality <sup>info<sup>
`local_player_stats_VitalityHealth + 0x12`

### *int* client_current_time <sup>?</sup>
`?? ?? ?? ?? 04 08 00 00 ?? ?? ?? ?? 00 00 00 00 00 00 00 00 40 18`

### *int* client_current_time (in-game) <sup>?</sup>
`已失效`

~~`?? ?? ?? ?? 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 10 BF ?? ?? ?? ?? 00 00 D0 49 ?? ?? ?? ?? 00 00 18 BF ?? ?? ?? ?? 00 00`~~

### *int* local_player_first_person <sup>?</sup>
~~`有时候不稳定，需调查。`~~

`失效之后直接重新扫描即可`

`"Dragons-Win64-Shipping.exe" + 0x02F746D0, 0x10, 0x28, 0x2A0, 0x740`

### *float* camera_position.x

`"Dragons-Win64-Shipping.exe" + 0x0304B3C0, 0x2D0`

### *float* camera_position.y

`camera_position.x + 0x4`

### *float* camera_position.z

`camera_position.x + 0x8`

### *byte* enemy_health
~~`应该会返回所有非休眠状态的玩家实体，idk，所有玩家全部休眠的时候也能扫到一堆不知道是什么东西的地址。`~~

`行不通，失效实体的内存不会被释放，所有东西都是过时的。`

`[01-C8] ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? ?? 01 00 00 00 C8 00 00 00 00 ?? ?? ?? ?? ?? 00 00 01 00 00 00 00 00 00 00 ?? ?? ?? ?? ?? ?? 00 00 00`
