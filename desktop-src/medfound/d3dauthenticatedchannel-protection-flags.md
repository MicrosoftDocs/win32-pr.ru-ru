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
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692062"
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                             |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Видеоструктуры Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




