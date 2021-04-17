---
title: Структура WMDRMNET_POLICY_GLOBAL_REQUIREMENTS (Вмдрмсдк. h)
description: '\_ \_ Структура глобальных требований политики вмдрмнет \_ содержит глобальные требования для Windows Media DRM для сетевых устройств.'
ms.assetid: 140b3a6f-ccba-4735-b48a-2e990f5ec570
keywords:
- Формат WMDRMNET_POLICY_GLOBAL_REQUIREMENTS структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_GLOBAL_REQUIREMENTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ccf13c881c9696d970a00ac902f3f8d08f13c58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694672"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_ \_ Структура глобальных требований политики вмдрмнет \_

Структура **\_ \_ глобальных \_ требований политики вмдрмнет** содержит глобальные требования для Windows Media DRM для сетевых устройств.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRMNET_POLICY_GLOBAL_REQUIREMENTS {
  WMDRMNET_POLICY_MINIMUM_ENVIRONMENT MinimumEnvironment;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**минимуменвиронмент**
</dt> <dd>

[**Вмдрмнет \_ \_Минимальная структура \_ среды**](wmdrmnet-policy-minimum-environment.md) , содержащая минимальные требования к безопасности для Windows Media DRM для сетевых устройств.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> <dt>

[**\_Политика вмдрмнет**](wmdrmnet-policy.md)
</dt> </dl>

 

 





