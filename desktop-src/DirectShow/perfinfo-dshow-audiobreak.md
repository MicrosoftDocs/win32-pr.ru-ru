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
ms.openlocfilehash: c7b8f83fffaa718c27e0333d864a564282228c0943f4d77fb653dc1800a6ddd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928194"
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

## <a name="remarks"></a>Remarks

Чтобы включить это событие, необходимо задать \_ флаг битов аудиобреак в параметре *енаблефлаг* при вызове **енаблетраце**. этот флаг определен в файле заголовка дксмперф. h, который включен в DirectShow базовых классов.

чтобы заносить это событие из фильтра DirectShow, используйте макрос **перфлог \_ аудиобреак** , который определен в дксмперф. h.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Перфструкт. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DirectShow Сотрудник](directshow-structures.md)
</dt> <dt>

[Трассировка событий в DirectShow](event-tracing-in-directshow.md)
</dt> <dt>

[Идентификаторы GUID событий трассировки](trace-guids.md)
</dt> </dl>

 

 




