---
description: Структура ПЕРФИНФО \_ DSHOW \_ авренд содержит данные для события трассировки типа GUID \_ видеоренд. VMR регистрирует это событие непосредственно перед отрисовкой кадра.
ms.assetid: 95deda21-0ef4-4bf0-9fa3-826a813757b9
title: Структура PERFINFO_DSHOW_AVREND (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_AVREND
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: ee2d944d086f9c1a4ea7944f023321dfbc06d547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689283"
---
# <a name="perfinfo_dshow_avrend-structure"></a>\_ \_ Структура авренд перфинфо DSHOW

`PERFINFO_DSHOW_AVREND`Структура содержит данные для события трассировки типа GUID \_ видеоренд.

VMR регистрирует это событие непосредственно перед отрисовкой кадра.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct PERFINFO_DSHOW_AVREND {
  ULONGLONG cycleCounter;
  ULONGLONG dshowClock;
  ULONGLONG sampleTime;
} PERFINFO_DSHOW_AVREND, *PPERFINFO_DSHOW_AVREND;
```



## <a name="members"></a>Члены

<dl> <dt>

**циклекаунтер**
</dt> <dd>

Последнее число циклов тактовой разницы (инструкция RDTSC).

</dd> <dt>

**дшовклокк**
</dt> <dd>

Текущее время ссылки, возвращаемое методом [**иреференцеклокк:: Time**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) .

</dd> <dt>

**самплетиме**
</dt> <dd>

Время начала примера.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы включить это событие, необходимо задать \_ флаг дксмперф видеоренд в параметре *енаблефлаг* при вызове **енаблетраце**. Этот флаг определен в файле заголовка Дксмперф. h, который включен в базовые классы DirectShow.

Чтобы заносить это событие из фильтра DirectShow, используйте макрос **перфлог \_ видеоренд** , который определен в дксмперф. h.

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

 

 




