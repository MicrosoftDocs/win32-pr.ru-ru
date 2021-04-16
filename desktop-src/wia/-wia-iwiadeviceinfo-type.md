---
description: Возвращает тип аппаратного устройства для получения образа Windows (WIA).
ms.assetid: 5f10bcd1-03a0-4cd9-8886-e1f957312c3b
title: DeviceInfo. Type, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Type
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 89a322890f035a1865c01be7c4bfb0bbab812fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719369"
---
# <a name="deviceinfotype-property"></a>DeviceInfo. Type, свойство

Возвращает тип аппаратного устройства для получения образа Windows (WIA). Возможны следующие значения:

-   дигиталкамера
-   Сканер
-   стреамингвидео
-   Значение по умолчанию

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = DeviceInfo.Type
```



## <a name="property-value"></a>Значение свойства

Строка, получающая устройство.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (версия 4,90 или более поздняя)</dt> </dl> |



 

 




