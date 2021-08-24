---
description: Фактический кадр из драйвера.
ms.assetid: 867082c1-196a-4580-ba24-187b0752f6f8
title: Структура ФРЕЙМа (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7447e0ba8e13a593af6ac346ad47f8fe992b4a3187f0c46e8ee8fc28ddeb5646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910954"
---
# <a name="frame-structure"></a>Структура ФРЕЙМа

Структура **фрейма** — это фактический кадр из драйвера.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _FRAME {
  __int64 TimeStamp;
  DWORD   FrameLength;
  DWORD   nBytesAvail;
  BYTE    MacFrame[];
} FRAME, *LPFRAME, *ULPFRAME;
```



## <a name="members"></a>Члены

<dl> <dt>

**TimeStamp**
</dt> <dd>

Затраченное время (в микросекундах) между началом записи и временем записи кадра.

</dd> <dt>

**фрамеленгс**
</dt> <dd>

Длина фрейма MAC.

</dd> <dt>

**нбитесаваил**
</dt> <dd>

Фактическая длина кадра скопирована.

</dd> <dt>

**макфраме**
</dt> <dd>

Данные кадра.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




