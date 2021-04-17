---
description: Представляет сведения о целевых объектах вызова для защиты потока управления (CFG).
ms.assetid: 8DEF907F-3F23-4122-95CE-F413FC7FD96B
title: Структура CFG_CALL_TARGET_INFO (Нтммапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFG_CALL_TARGET_INFO
api_type:
- HeaderDef
api_location:
- ntmmapi.h
ms.openlocfilehash: 66177f6b478264a10c1ce0e50297d943a16407c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673685"
---
# <a name="cfg_call_target_info-structure"></a>\_ \_ \_ Структура сведений о цели вызова cfg

Представляет сведения о целевых объектах вызова для защиты потока управления (CFG).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _CFG_CALL_TARGET_INFO {
  ULONG_PTR Offset;
  ULONG_PTR Flags;
} CFG_CALL_TARGET_INFO, *PCFG_CALL_TARGET_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Offset**
</dt> <dd>

Смещение относительно указанного (начального) виртуального адреса. Это смещение должно быть равно 16 байтам.

</dd> <dt>

**Флаги**
</dt> <dd>

Флаги, описывающие операцию, которая должна быть выполнена с адресом. Если задана **\_ \_ \_ допустимая цель вызова cfg** , адрес будет ПОМЕЧЕН как допустимый для cfg. В противном случае он будет помечен как недопустимый целевой объект вызова.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2016\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Нтммапи. h</dt> </dl> |



 

 




