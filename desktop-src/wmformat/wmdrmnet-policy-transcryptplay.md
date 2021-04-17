---
title: Структура WMDRMNET_POLICY_TRANSCRYPTPLAY (Вмдрмсдк. h)
description: '\_ \_ Структура ТРАНСКРИПТПЛАЙ политики вмдрмнет содержит сведения о политике для воспроизведения содержимого с помощью Windows Media DRM для сетевых устройств.'
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
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647962"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a>\_ \_ Структура ТРАНСКРИПТПЛАЙ политики вмдрмнет

Структура **\_ \_ транскриптплай политики вмдрмнет** содержит сведения о политике для воспроизведения содержимого с помощью Windows Media DRM для сетевых устройств.

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

 

 





