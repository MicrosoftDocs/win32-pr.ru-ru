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
ms.openlocfilehash: 49cc76f4db1a5fae76678ee2d81f3e2fff0a6c5ca3d5c5532adebaec23f48215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050714"
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

## <a name="remarks"></a>Remarks

Чтобы включить это событие, необходимо задать \_ флаг дксмперф видеоренд в параметре *енаблефлаг* при вызове **енаблетраце**. этот флаг определен в файле заголовка дксмперф. h, который включен в DirectShow базовых классов.

чтобы заносить это событие из фильтра DirectShow, используйте макрос **перфлог \_ видеоренд** , который определен в дксмперф. h.

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

 

 




