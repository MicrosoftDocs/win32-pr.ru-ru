---
title: Структура DRM_OUTPUT_PROTECTION_EX (Вмдрмсдк. h)
description: Структура для \_ защиты выходных данных DRM \_ \_ содержит сведения о технологии защиты выходных данных. Эта структура расширяет \_ защиту выхода DRM \_ путем добавления номера версии.
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- Формат DRM_OUTPUT_PROTECTION_EX структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708573"
---
# <a name="drm_output_protection_ex-structure"></a>\_Структура для \_ защиты \_ вывода DRM

Структура **для \_ защиты выходных данных \_ \_ DRM** содержит сведения о технологии защиты выходных данных. Эта структура расширяет **\_ \_ защиту выхода DRM** путем добавления номера версии.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**двверсион**
</dt> <dd>

Номер версии.

</dd> <dt>

**guidId**
</dt> <dd>

Идентификатор GUID, определяющий технологию защиты выходных данных.

</dd> <dt>

**двконфигдата**
</dt> <dd>

Данные конфигурации для технологии.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**DRM \_ Защита звука с аудио \_ и \_ \_** защитой, например, в инструкциях **typedef** определяется как **\_ \_ Защита выходных данных DRM** . **\_ \_ \_ \_**

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Защита вывода \_ DRM**](drm-output-protection.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





