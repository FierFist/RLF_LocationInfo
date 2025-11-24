# 地点（Location）配置参数说明

## 参数说明

| 参数 | 类型 | 说明 |
|------|------|------|
| `timeNotifyShow` | `int` | 通知显示的时长（秒） |
| `itemInInvetory` | `array` | 激活信息点所需玩家背包中必须存在的物品列表 |

---

## `infoPoint` 对象参数

| 参数 | 类型 | 说明 |
|------|------|------|
| `name` | `string` | 地点或兴趣点名称 |
| `iconPath` | `string` | 地图上显示的图标路径 |
| `stayVisible` | `bool` | 是否在玩家位于范围内时始终显示（适用于安全区） |
| `notifySound` | `string` | 出现通知时播放的声音名称；若填 `None` 则无声音 |
| `layoutPath` | `string` | 自定义通知 UI 布局路径 |
| `radiusToCheck` | `number` | 与地点交互的检测半径（米） |
| `position` | `array[3]` | 点的世界坐标：[X, Y, Z] |
| `polygonPoints` | `array[vector]` | 多边形区域的点列表（不自动闭合，需要按顺序填写） |

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

