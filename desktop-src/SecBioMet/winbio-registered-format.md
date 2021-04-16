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
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534193"
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

**Тип**
</dt> <dd>

Формат, которому назначен владелец.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Так как Windows в настоящее время поддерживает только средства чтения отпечатков пальцев, в **винбио \_ зарегистрированной структуре \_ формата** должны использоваться следующие значения.



| Константа                                    | Значение                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ Владелец формата винбио ANSI \_ 381<br/> | Международный комитет для технического комитета по стандартам информационных технологий (ИНЦИТС) M1 (Биометрия).<br/> |
| \_ \_ \_ Тип формата винбио ANSI \_ 381<br/>  | Формат обмена данными с изображением пальца ANSI ИНЦИТС 381.<br/>                                                |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                                    |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                                       |
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

 

 





