---
title: Структура DRM_OUTPUT_PROTECTION (Вмдрмсдк. h)
description: '\_Структура защиты выходных данных DRM \_ содержит сведения о технологии защиты выходных данных.'
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- Формат DRM_OUTPUT_PROTECTION структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704528"
---
# <a name="drm_output_protection-structure"></a>\_Структура защиты выходных данных DRM \_

Структура **\_ \_ защиты выходных данных DRM** содержит сведения о технологии защиты выходных данных.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**guidId**
</dt> <dd>

Идентификатор GUID, определяющий технологию защиты выходных данных.

</dd> <dt>

**бконфигдата**
</dt> <dd>

Данные конфигурации для технологии.

</dd> </dl>

## <a name="remarks"></a>Комментарии

**DRM \_ Защита \_ аудио \_** и **\_ видео \_ \_ DRM** в инструкциях **typedef** определяется как **\_ \_ Защита выходных данных DRM** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Защита вывода DRM, \_ \_ пример**](drm-output-protection-ex.md)
</dt> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





