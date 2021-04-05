---
description: Функция Виаадддевице вызывает пользовательский интерфейс мастера установки сканера и камеры. Он эквивалентен запуску &\# 0034; rundll32.exe сти \_ci.dll AddDevice&\# 0034; из командной строки.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Функция Виаадддевице (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809964"
---
# <a name="wiaadddevice-function"></a>Функция Виаадддевице

Функция **виаадддевице** вызывает пользовательский интерфейс мастера установки сканера и камеры. Он эквивалентен запуску "rundll32.exe сти \_ci.dll AddDevice" из командной строки.

## <a name="syntax"></a>Синтаксис


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a>Параметры

У этой функции нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Эта функция не возвращает значение.

## <a name="remarks"></a>Комментарии

Эта функция должна вызываться с учетными данными администратора. При работе в режиме управления учетными записями пользователей (LUA) процесс должен быть повышен.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                   |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| Библиотека<br/>                  | <dl> <dt>Виагуид. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инсталлвиадевице**](-wia-installwiadevice.md)
</dt> </dl>

 

 




