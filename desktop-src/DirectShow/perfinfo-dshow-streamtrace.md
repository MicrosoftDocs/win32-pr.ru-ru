---
description: Структура ПЕРФИНФО \_ DSHOW \_ стреамтраце содержит данные для события трассировки DIRECTSHOW типа GUID \_ стреамтраце.
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
ms.openlocfilehash: 2bee4f3c11cf8462c8292cc412a6da5d9f9bfa78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685259"
---
# <a name="perfinfo_dshow_streamtrace-structure"></a>\_ \_ Структура стреамтраце перфинфо DSHOW

`PERFINFO_DSHOW_STREAMTRACE`Структура содержит данные для события трассировки DirectShow типа GUID \_ стреамтраце.

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



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Идентификатор события</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</td>
<td>Записывается в журнал, когда фильтр <a href="mpeg-2-demultiplexer.md">демультиплексора MPEG-2</a> преобразует отметку времени презентации (PTS) в потоковое время.
<ul>
<li><strong>data</strong>[0]: Converted start time.</li>
<li><strong>data</strong>[1]: Converted stop time.</li>
<li><strong>данные</strong>[2]. Идентификатор потока для входного ПИН-кода.</li>
<li><strong>data</strong>[3]: PTS that was converted.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</td>
<td>Записывается в журнал, когда демультиплексор MPEG-2 получает пример.
<ul>
<li><strong>данные</strong> [0]: Current time returned by  <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</td>
<td>Регистрируется, когда VMR планирует пример для подготовки к просмотру, непосредственно перед вызовом VMR <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>иреференцеклокк:: адвисетиме</strong></a>.
<ul>
<li><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</li>
</ul></td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</td>
<td>Регистрируется, когда VMR начинает операцию декодирования, то есть когда декодер вызывает <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>иамвидеоакцелератор:: бегинфраме</strong></a>. Нет данных события.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</td>
<td>Регистрируется, когда VMR начинает операцию разчередования или композиции видео. Нет данных события.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</td>
<td>Регистрируется, когда VMR удаляет кадр; Например, если образец был последним.
<ul>
<li><strong>data</strong>[0]: Sample start time.</li>
<li><strong>data</strong>[1]: Sample end time.</li>
</ul></td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_ADVISE</td>
<td>Записывается в журнал, когда VMR получает уведомление о получении из ссылочного времени. Нет данных события.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_END_DECODE</td>
<td>Регистрируется, когда VMR завершает операцию декодирования, то есть когда декодер вызывает <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>иамвидеоакцелератор:: ендфраме</strong></a>. Нет данных события.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</td>
<td>Регистрируется, когда VMR завершает операцию разчередования или композицию видео. Нет данных события.</td>
</tr>
<tr class="even">
<td>PERFINFO_STREAMTRACE_VMR_RECEIVE</td>
<td>Регистрируется, когда VMR получает новый пример. Нет данных события.</td>
</tr>
<tr class="odd">
<td>PERFINFO_STREAMTRACE_VMR_RENDER_TIME</td>
<td>Регистрируется, когда VMR заканчивает отрисовку кадра.
<ul>
<li><strong>data</strong>[0]: Time that it took to render this frame.</li>
<li><strong>data</strong>[1]: Running average of frame rendering times.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Чтобы заносить это событие из фильтра DirectShow, используйте функцию **перфлог \_ стреамтраце** , которая определена в файле заголовка дксмперф. h. Этот заголовок включен в базовые классы DirectShow.

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

 

 
