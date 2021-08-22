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
ms.openlocfilehash: 01978cf55d90e217aa50fb8fad696f6af90b33ab9e59975a901daa99db633181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911049"
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

## <a name="remarks"></a>Remarks

Использование смещений вместо указателей позволяет легко сериализовать Бир и для менее сложного перевода между 32 и 64-разрядными средами или между пользователем и режимом ядра.

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

[**ВИНБИО \_ Бир**](winbio-bir.md)
</dt> <dt>

[**\_заголовок винбио Бир \_**](winbio-bir-header.md)
</dt> </dl>

 

 





