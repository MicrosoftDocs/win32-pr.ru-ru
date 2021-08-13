---
title: Структура WINBIO_REGISTERED_FORMAT (Винбио \_ types. h)
description: Задает зарегистрированный формат данных в виде пары "владелец-формат".
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- API структуры WINBIO_REGISTERED_FORMAT биометрическая платформа Windows
- PWINBIO_REGISTERED_FORMAT API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fcf871f3fc5f258de22e033e8a388968ab58c1a35e19829bf3d02a97ca60c53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909372"
---
# <a name="winbio_registered_format-structure"></a>ВИНБИО \_ зарегистрированная \_ Структура формата

В **винбионой структуре \_ \_ формата** зарегистрированный формат данных указывается как пара "владелец-формат".

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Члены

<dl> <dt>

**Владелец**
</dt> <dd>

ИБИА (Международная ассоциация биометрической отрасли) назначает значение владельца.

</dd> <dt>

**Type**
</dt> <dd>

Формат, которому назначен владелец.

</dd> </dl>

## <a name="remarks"></a>Remarks

поскольку Windows в настоящее время поддерживает только средства чтения отпечатков пальцев, в **винбио \_ зарегистрированной структуре \_ формата** должны использоваться следующие значения.



| Константа                                    | Значение                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ Владелец формата винбио ANSI \_ 381<br/> | Международный комитет для технического комитета по стандартам информационных технологий (ИНЦИТС) M1 (Биометрия).<br/> |
| \_ \_ \_ Тип формата винбио ANSI \_ 381<br/>  | Формат обмена данными с изображением пальца ANSI ИНЦИТС 381.<br/>                                                |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Винбио \_ types. h (include винбио. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры клиентских приложений](client-application-structures.md)
</dt> <dt>

[**\_ \_ \_ Константы формата ANSI 381 винбио**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**\_Заголовок винбио БДБ \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**\_заголовок винбио Бир \_**](winbio-bir-header.md)
</dt> </dl>

 

 





