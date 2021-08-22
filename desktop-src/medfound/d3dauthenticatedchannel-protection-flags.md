---
description: Задает уровень защиты содержимого видео.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Структура D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1d1b76a6fea0dd6b966bd72001efb187a7a3a14e75b4d41d631e5a1ea163fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974713"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>\_ \_ Структура флагов защиты D3DAUTHENTICATEDCHANNEL

Задает уровень защиты содержимого видео.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>Члены

<dl> <dt>

**протектионенаблед**
</dt> <dd>

Если значение равно 1, защита содержимого видео включена.

</dd> <dt>

**оверлайорфуллскринрекуиред**
</dt> <dd>

Если задано значение 1, приложение должно отображать видео с помощью наложения оборудования или полноэкранного режима монопольного доступа.

</dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано. Задайте для всех битов значение 0.

</dd> <dt>

**Значение**
</dt> <dd>

Используйте этот элемент для доступа ко всем битам в объединении.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




