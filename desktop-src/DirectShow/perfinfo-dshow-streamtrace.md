---
description: структура перфинфо \_ DSHOW \_ стреамтраце содержит данные для события трассировки DirectShow типа GUID \_ стреамтраце.
ms.assetid: 41fbf95c-e86c-4c64-898f-01fbf5f8839c
title: Структура PERFINFO_DSHOW_STREAMTRACE (Перфструкт. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PERFINFO_DSHOW_STREAMTRACE
api_type:
- HeaderDef
api_location:
- Perfstruct.h
ms.openlocfilehash: e17d013d90b133f9c6819b8d9ddf4b5970582cae
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477009"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>\_ \_ Структура стреамтраце перфинфо DSHOW

`PERFINFO_DSHOW_STREAMTRACE`структура содержит данные для DirectShow события трассировки типа GUID \_ стреамтраце.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a>Члены

<dl> <dt>

**id**
</dt> <dd>

Идентификатор события. См. заметки.

</dd> <dt>

**процессу**
</dt> <dd>

Зарезервировано. Задайте нулевое значение.

</dd> <dt>

**дшовклокк**
</dt> <dd>

Время потока для этого события в единицах измерения 100-наносекундных. Это значение является необязательным и может равняться нулю.

</dd> <dt>

**data**
</dt> <dd>

Необязательные данные события, состоящие из четырех **улонглонг** значений. Значение этих данных зависит от идентификатора события.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Определены следующие идентификаторы событий.




| Идентификатор события | Описание | 
|------------------|-------------|
| PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION | Записывается в журнал, когда фильтр <a href="mpeg-2-demultiplexer.md">демультиплексора MPEG-2</a> преобразует отметку времени презентации (PTS) в потоковое время.<ul><li><strong>данные</strong>[0]: время начала преобразовано.</li><li><strong>данные</strong>[1]: превышено время отмены.</li><li><strong>данные</strong>[2]. Идентификатор потока для входного ПИН-кода.</li><li><strong>данные</strong>[3]: PTS, которые были преобразованы.</li></ul> | 
| PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE | Записывается в журнал, когда демультиплексор MPEG-2 получает пример.<ul><li><strong>данные</strong>[0]: текущее время, возвращенное <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE | Регистрируется, когда VMR планирует пример для подготовки к просмотру, непосредственно перед вызовом VMR <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>иреференцеклокк:: адвисетиме</strong></a>.<ul><li><strong>данные</strong>[0]: время начала потоковой передачи, соответствующее нулевому времени потока.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE | Регистрируется, когда VMR начинает операцию декодирования, то есть когда декодер вызывает <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>иамвидеоакцелератор:: бегинфраме</strong></a>. Нет данных события. | 
| PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE | Регистрируется, когда VMR начинает операцию разчередования или композиции видео. Нет данных события. | 
| PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME | Регистрируется, когда VMR удаляет кадр; Например, если образец был последним.<ul><li><strong>данные</strong>[0]: время начала выборки.</li><li><strong>данные</strong>[1]: время окончания выборки.</li></ul> | 
| PERFINFO_STREAMTRACE_VMR_END_ADVISE | Записывается в журнал, когда VMR получает уведомление о получении из ссылочного времени. Нет данных события. | 
| PERFINFO_STREAMTRACE_VMR_END_DECODE | Регистрируется, когда VMR завершает операцию декодирования, то есть когда декодер вызывает <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>иамвидеоакцелератор:: ендфраме</strong></a>. Нет данных события. | 
| PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE | Регистрируется, когда VMR завершает операцию разчередования или композицию видео. Нет данных события. | 
| PERFINFO_STREAMTRACE_VMR_RECEIVE | Регистрируется, когда VMR получает новый пример. Нет данных события. | 
| PERFINFO_STREAMTRACE_VMR_RENDER_TIME | Регистрируется, когда VMR заканчивает отрисовку кадра.<ul><li><strong>данные</strong>[0]: время, затраченное на визуализацию этого кадра.</li><li><strong>данные</strong>[1]: среднее время отрисовки кадров.</li></ul> | 




 

чтобы заносить это событие из фильтра DirectShow, используйте функцию **\_ стреамтраце перфлог** , которая определена в файле заголовка дксмперф. h. этот заголовок включен в DirectShow базовых классов.

## <a name="requirements"></a>Требования



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

 

 
