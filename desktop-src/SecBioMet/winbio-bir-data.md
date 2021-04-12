---
title: Структура WINBIO_BIR_DATA (Винбио \_ types. h)
description: Задает размер в байтах и смещение блока биометрических данных.
ms.assetid: 2f73eb1f-f1a1-4831-a8f7-eec28aa51645
keywords:
- API структуры WINBIO_BIR_DATA биометрическая платформа Windows
topic_type:
- apiref
api_name:
- WINBIO_BIR_DATA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ebf7b157c5bd806442cdc120350a89ce646f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415472"
---
# <a name="winbio_bir_data-structure"></a>\_ \_ Структура данных винбио Бир

Структура **\_ \_ данных винбио Бир** определяет размер в байтах и смещение блока биометрических данных. Эта структура используется структурой [**винбио \_ Бир**](winbio-bir.md) , чтобы указать, где находятся различные части записи биометрической информации.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _WINBIO_BIR_DATA {
  ULONG Size;
  ULONG Offset;
} WINBIO_BIR_DATA;
```



## <a name="members"></a>Члены

<dl> <dt>

**Размер**
</dt> <dd>

Размер биометрической информации в байтах.

</dd> <dt>

**Offset**
</dt> <dd>

Смещение (в байтах от начала структуры [**винбио \_ Бир**](winbio-bir.md) ) биометрической информации.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Использование смещений вместо указателей позволяет легко сериализовать Бир и для менее сложного перевода между 32 и 64-разрядными средами или между пользователем и режимом ядра.

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

[**ВИНБИО \_ Бир**](winbio-bir.md)
</dt> <dt>

[**\_заголовок винбио Бир \_**](winbio-bir-header.md)
</dt> </dl>

 

 





