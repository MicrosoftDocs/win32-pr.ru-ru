---
title: Структура WMDRMNET_POLICY_TRANSCRYPTPLAY (Вмдрмсдк. h)
description: '\_ \_ структура транскриптплай политики вмдрмнет содержит сведения о политике для воспроизведения содержимого с помощью Windows Media DRM для сетевых устройств.'
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Формат WMDRMNET_POLICY_TRANSCRYPTPLAY структуры Windows Media
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe64c796a1f2f15e4733e7dd3d82e918306fb95d78c61fb85ad2d813d946d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195509"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_ \_ Структура ТРАНСКРИПТПЛАЙ политики вмдрмнет

структура **\_ \_ транскриптплай политики вмдрмнет** содержит сведения о политике для воспроизведения содержимого с помощью Windows Media DRM для сетевых устройств.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**Globals**
</dt> <dd>

Структура глобальной политики.

</dd> <dt>

**плайоплс**
</dt> <dd>

Уровни защиты выходных данных для воспроизведения. **Вмдрмнет \_ ПОЛИТИКА \_ Play \_ ОПЛ** — это тип, определенный как [**DRM \_ Play \_ ОПЛ \_ ex**](drm-play-opl-ex.md).

</dd> </dl>

## <a name="remarks"></a>Remarks

Нет.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> <dt>

[**\_Политика вмдрмнет**](wmdrmnet-policy.md)
</dt> </dl>

 

 





