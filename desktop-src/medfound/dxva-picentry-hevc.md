---
description: Задает ссылку на несжатую поверхность.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Структура DXVA_PicEntry_HEVC (Дксва. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647151"
---
# <a name="dxva_picentry_hevc-structure"></a>\_ \_ Структура HEVC пицентри дксва

Задает ссылку на несжатую поверхность.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>Члены

<dl> <dt>

**Index7Bits**
</dt> <dd>

Индекс, определяющий несжатую поверхность.

</dd> <dt>

**ассоЦиатедфлаг** 
</dt> <dd>

Необязательный 1-разрядный флаг, связанный с поверхностью. Значение флага зависит от контекста. Например, он может указать, является ли ссылочный кадр долгосрочной ссылкой или краткосрочной ссылкой.

</dd> <dt>

**бпицентри**
</dt> <dd>

Обращается ко всем 8 битам объединения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                      |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                           |
| Header<br/>                   | <dl> <dt>Дксва. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




