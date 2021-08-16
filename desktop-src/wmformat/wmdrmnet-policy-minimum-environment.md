---
title: Структура WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (Вмдрмсдк. h)
description: '\_ \_ структура минимальной среды политики вмдрмнет \_ содержит минимальные требования к безопасности для Windows Media DRM для сетевых устройств.'
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Формат WMDRMNET_POLICY_MINIMUM_ENVIRONMENT структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c11cf02d7cfcd2e3ab62c4e6b110e2c20b77cf6f79251a23f642b38d4df553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027465"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a>\_ \_ Минимальная \_ Структура среды политики вмдрмнет

структура **\_ \_ минимальной \_ среды политики вмдрмнет** содержит минимальные требования к безопасности для Windows Media DRM для сетевых устройств.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**вминимумсекуритилевел**
</dt> <dd>

Требуется минимальный уровень безопасности приложения.

</dd> <dt>

**двминимумаппревокатионлистверсион**
</dt> <dd>

Требуется версия минимального списка отзыва сертификатов приложений.

</dd> <dt>

**двминимумдевицеревокатионлистверсион**
</dt> <dd>

Требуется минимальный список отзыва сертификатов устройства.

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

 

 





