---
description: Структура ПЕРФИНФО \_ DSHOW \_ аудиобреак содержит данные для события трассировки типа GUID \_ аудиобреак. Фильтр модуля подготовки отчетов DirectSound регистрирует это событие при разрыве в потоке аудио.
ms.assetid: 9e7abdca-7d4c-4006-997f-9605f8d18e1d
title: Структура PERFINFO_DSHOW_AUDIOBREAK (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AUDIOBREAK
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: 599befea67b28acbedffd5c98ebce84aadf70838
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689285"
---
# <a name="perfinfo_dshow_audiobreak-structure"></a>\_ \_ Структура аудиобреак перфинфо DSHOW

`PERFINFO_DSHOW_AUDIOBREAK`Структура содержит данные для события трассировки типа GUID \_ аудиобреак.

Фильтр модуля [подготовки отчетов DirectSound](directsound-renderer-filter.md) регистрирует это событие при разрыве в потоке аудио.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct PERFINFO_DSHOW_AUDIOBREAK {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
  ULONGLONG sampleDuration;
} PERFINFO_DSHOW_AUDIOBREAK, *PPERFINFO_DSHOW_AUDIOBREAK;
```



## <a name="members"></a>Члены

<dl> <dt>

**циклекаунтер**
</dt> <dd>

Последнее число циклов тактовой разницы (инструкция RDTSC).

</dd> <dt>

**дшовклокк**
</dt> <dd>

Текущее расположение записи в буфере DirectSound.

</dd> <dt>

**самплетиме**
</dt> <dd>

Начало разрыва звука в буфере DirectSound.

</dd> <dt>

**сампледуратион**
</dt> <dd>

Продолжительность перерыва в миллисекундах.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы включить это событие, необходимо задать \_ флаг битов аудиобреак в параметре *енаблефлаг* при вызове **енаблетраце**. Этот флаг определен в файле заголовка Дксмперф. h, который включен в базовые классы DirectShow.

Чтобы заносить это событие из фильтра DirectShow, используйте макрос **перфлог \_ аудиобреак** , который определен в дксмперф. h.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Перфструкт. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Структуры DirectShow](directshow-structures.md)
</dt> <dt>

[Трассировка событий в DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[Идентификаторы GUID событий трассировки](trace-guids.md)
</dt> </dl>

 

 




