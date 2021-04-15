---
title: Структура WINBIO_VERSION (Винбио \_ types. h)
description: Содержит номер версии программного обеспечения для компонента биометрической службы поставщика.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- API структуры WINBIO_VERSION биометрическая платформа Windows
- PWINBIO_VERSION API биометрическая платформа Windows указателя структуры
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493017"
---
# <a name="winbio_version-structure"></a>\_Структура версии винбио

Структура **\_ версии винбио** содержит номер версии программного обеспечения для компонента биометрической службы поставщика.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>Члены

<dl> <dt>

**MajorVersion**
</dt> <dd>

Значение **типа DWORD** , содержащее основной номер версии.

</dd> <dt>

**MinorVersion**
</dt> <dd>

Значение **типа DWORD** , содержащее дополнительный номер версии.

</dd> </dl>

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

[**\_схема винбио BSP \_**](winbio-bsp-schema.md)
</dt> <dt>

[**\_схема единицы \_ винбио**](winbio-unit-schema.md)
</dt> </dl>

 

 





