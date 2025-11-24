# 地点（Location）配置参数说明

## 参数说明

| 参数 | 类型 | 说明 |
|------|------|------|
| `timeNotifyShow` | `int` | 通知显示的时长（秒） |
| `itemInInvetory` | `array` | 激活信息点所需玩家背包中必须存在的物品列表 |
| `adminSteamID` | `array<string>` | 拥有特殊权限（可看到所有地点）的管理员 SteamID 列表 |
| `infoPoints` | `array<object>` | 信息点（地点触发器）列表 |

---

## `infoPoint` 对象参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `name` | `string` | 地点或兴趣点名称 |
| `iconPath` | `string` | 地图上显示的图标路径 |
| `stayVisible` | `bool` | 玩家在范围内时是否始终显示（适用于安全区） |
| `notifySound` | `string` | 通知出现时播放的声音名称；填 `None` 则无声音 |
| `layoutPath` | `string` | 自定义通知 UI 布局路径 |
| `radiusToCheck` | `number` | 与地点交互的检测半径（米） |
| `position` | `array[3]` | 点的世界坐标：[X, Y, Z] |
| `polygonPoints` | `array[vector]` | 多边形区域的点列表（不自动闭合，需要按顺序填写） |
| `markersList` | `array<object>` | 此信息点下的地图标记列表 |

---

## `markersList` 对象参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `markerTitle` | `string` | 标记名称 |
| `iconPath` | `string` | 地图显示用的图标路径 |
| `layoutPath` | `string` | 自定义标记 UI 布局路径 |
| `markerPosition` | `array[3]` | 标记坐标：[X, Y, Z] |

---

## layoutPath 可用的通知界面（UI 预览）

| 参数 | 预览 |
|------|------|
| `relife_LocationInfo/layout/LocNotificationDanger.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/93e6f5f7-27ed-4482-bc51-3ed939b763ab" /> |
| `relife_LocationInfo/layout/LocNotificationSafe.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/38e3f808-4be7-414d-ac2e-d5b003bc8a3b" /> |
| `relife_LocationInfo/layout/LocNotification.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/f3f58713-1363-4d17-9f88-21c79d8a6a48" /> |
| `relife_LocationInfo/layout/LocNotificationStalkerOld.layout` | <img width="250" alt="image" src="https://github.com/user-attachments/assets/6c882557-1292-482d-a4bd-395a2b5876f4" /> |

---

# 完整 JSON 示例（原始结构 + 完整有效）

```json
{
    "timeNotifyShow": 5,
    "itemInInvetory": [],
    "adminSteamID": [
        "76561199479047427"
    ],
    "infoPoints": [
        {
            "name": "Какой-то дом",
            "iconPath": "relife_LocationInfo/images/nearIcon.edds",
            "layoutPath": "relife_LocationInfo/layout/LocNotificationSafe.layout",
            "radiusToCheck": 150,
            "notifySound": "locShowNotifyDanger_SoundSet",
            "stayVisible": 1,
            "position": [
                12078.75,
                0,
                3558.75
            ],
            "markersList": [
                {
                    "markerTitle": "Какое-то место",
                    "iconPath": "relife_Core/images/icons/greek-temple.edds",
                    "layoutPath": "relife_LocationInfo/layout/MarkersWidget/ScreenIconWidget.layout",
                    "markerPosition": [
                        8146.01,
                        6.09406,
                        3204.26
                    ]
                }
            ],
            "polygonPoints": [
                [
                    8142.18,
                    6.02169,
                    3210.39
                ],
                [
                    8148.95,
                    6.02204,
                    3207.8
                ],
                [
                    8146.07,
                    5.99,
                    3198.31
                ],
                [
                    8138.99,
                    6.01499,
                    3200.8
                ]
            ]
        },
        {
            "name": "ВНЗ Круг",
            "iconPath": "relife_LocationInfo/images/nearIcon.edds",
            "radiusToCheck": 200,
            "position": [
                1082.67,
                0.0,
                1100.27
            ]
        }
    ]
}
```

