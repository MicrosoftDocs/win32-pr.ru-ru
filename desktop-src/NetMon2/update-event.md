---
description: Обновление \_ структуры событий обновляет события. Эта структура передается обратно вызывающему приложению через процедуру обратного вызова состояния события НПП.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Структура UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673576"
---
# <a name="update_event-structure"></a>ОБНОВИТЬ \_ структуру событий

**Обновление структуры \_ событий** обновляет события. Эта структура передается обратно вызывающему приложению через процедуру обратного вызова состояния события НПП.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Событие**
</dt> <dd>

Регистрируется фактическое событие.

</dd> <dt>

**Действие**
</dt> <dd>

Предпринимаемое действие.

</dd> <dt>

**Состояние**
</dt> <dd>

Указание состояния сети.

</dd> <dt>

**Значение**
</dt> <dd>

Вспомогательная переменная счетчика.

</dd> <dt>

**TimeStamp**
</dt> <dd>

Помеченные события в микросекундах.

</dd> <dt>

**лпусерконтекст**
</dt> <dd>

Контекст пользователя, заданный приложением.

</dd> <dt>

**lpReserved**
</dt> <dd>

Использование драйвера или NAL.

</dd> <dt>

**фрамесдроппед**
</dt> <dd>

Кадры RTF отброшены в указанном буфере.

</dd> <dt>

**Reserved**
</dt> <dd>

Данные не возвращаются с помощью этого параметра.

</dd> <dt>

**лпфраметабле**
</dt> <dd>

Только RTF.

</dd> <dt>

**лппаккеткуеуе**
</dt> <dd>

Для передачи.

</dd> <dt>

**секуритиреспонсе**
</dt> <dd>

Ответ монитора удаленной безопасности.

</dd> <dt>

**лпфиналстатс**
</dt> <dd>

Этот параметр заполняется только для остановок, не связанных с безопасностью (например, триггеров).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Пользователи C++ должны отметить, что объявление для этого обратного вызова должно находиться в открытой части файла заголовка:

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

Реализация должна находиться в защищенном разделе CPP файла:

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




