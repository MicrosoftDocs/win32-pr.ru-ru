---
title: Структура WMDRMNET_POLICY_GLOBAL_REQUIREMENTS (Вмдрмсдк. h)
description: '\_ \_ структура глобальных требований политики вмдрмнет \_ содержит глобальные требования для Windows Media DRM для сетевых устройств.'
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
ms.openlocfilehash: 4e2a8dc7be95638e171126eb4a55c50744ee3e5126d3e0b49eb8f229ec0257e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843975"
---
# <a name="wmdrmnet_policy_global_requirements-structure"></a>\_ \_ Структура глобальных требований политики вмдрмнет \_

структура **\_ \_ глобальных \_ требований политики вмдрмнет** содержит глобальные требования для Windows Media DRM для сетевых устройств.

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

[**Вмдрмнет \_ \_минимальная структура \_ среды**](wmdrmnet-policy-minimum-environment.md) , содержащая минимальные требования к безопасности для Windows Media DRM для сетевых устройств.

</dd> </dl>

## <a name="remarks"></a>Remarks

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> <dt>

[**\_Политика вмдрмнет**](wmdrmnet-policy.md)
</dt> </dl>

 

 





