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
# <a name="perfinfo_dshow_streamtrace-structure"></a><span data-ttu-id="cb197-103">\_ \_ Структура стреамтраце перфинфо DSHOW</span><span class="sxs-lookup"><span data-stu-id="cb197-103">PERFINFO\_DSHOW\_STREAMTRACE structure</span></span>

<span data-ttu-id="cb197-104">`PERFINFO_DSHOW_STREAMTRACE`Структура содержит данные для события трассировки DirectShow типа GUID \_ стреамтраце.</span><span class="sxs-lookup"><span data-stu-id="cb197-104">The `PERFINFO_DSHOW_STREAMTRACE` structure contains data for a DirectShow trace event of type GUID\_STREAMTRACE.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb197-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb197-105">Syntax</span></span>


```C++
typedef struct _PERFINFO_DSHOW_STREAMTRACE {
  ULONG     id;
  ULONG     reserved;
  ULONGLONG dshowClock;
  ULONGLONG data[4];
} PERFINFO_DSHOW_STREAMTRACE, *PPERFINFO_DSHOW_STREAMTRACE;
```



## <a name="members"></a><span data-ttu-id="cb197-106">Члены</span><span class="sxs-lookup"><span data-stu-id="cb197-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cb197-107">**id**</span><span class="sxs-lookup"><span data-stu-id="cb197-107">**id**</span></span>
</dt> <dd>

<span data-ttu-id="cb197-108">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="cb197-108">Event identifier.</span></span> <span data-ttu-id="cb197-109">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="cb197-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="cb197-110">**процессу**</span><span class="sxs-lookup"><span data-stu-id="cb197-110">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="cb197-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="cb197-111">Reserved.</span></span> <span data-ttu-id="cb197-112">Задайте нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="cb197-112">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb197-113">**дшовклокк**</span><span class="sxs-lookup"><span data-stu-id="cb197-113">**dshowClock**</span></span>
</dt> <dd>

<span data-ttu-id="cb197-114">Время потока для этого события в единицах измерения 100-наносекундных.</span><span class="sxs-lookup"><span data-stu-id="cb197-114">Stream time for this event, in 100-nanosecond units.</span></span> <span data-ttu-id="cb197-115">Это значение является необязательным и может равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cb197-115">This value is optional and can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cb197-116">**data**</span><span class="sxs-lookup"><span data-stu-id="cb197-116">**data**</span></span>
</dt> <dd>

<span data-ttu-id="cb197-117">Необязательные данные события, состоящие из четырех **улонглонг** значений.</span><span class="sxs-lookup"><span data-stu-id="cb197-117">Optional event data consisting of four **ULONGLONG** values.</span></span> <span data-ttu-id="cb197-118">Значение этих данных зависит от идентификатора события.</span><span class="sxs-lookup"><span data-stu-id="cb197-118">The meaning of this data depends on the event identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb197-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb197-119">Remarks</span></span>

<span data-ttu-id="cb197-120">Определены следующие идентификаторы событий.</span><span class="sxs-lookup"><span data-stu-id="cb197-120">The following event identifiers are defined.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb197-121">Идентификатор события</span><span class="sxs-lookup"><span data-stu-id="cb197-121">Event identifier</span></span></th>
<th><span data-ttu-id="cb197-122">Описание</span><span class="sxs-lookup"><span data-stu-id="cb197-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb197-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span><span class="sxs-lookup"><span data-stu-id="cb197-123">PERFINFO_STREAMTRACE_MPEG2DEMUX_PTS_TRANSLATION</span></span></td>
<td><span data-ttu-id="cb197-124">Записывается в журнал, когда фильтр <a href="mpeg-2-demultiplexer.md">демультиплексора MPEG-2</a> преобразует отметку времени презентации (PTS) в потоковое время.</span><span class="sxs-lookup"><span data-stu-id="cb197-124">Logged when the <a href="mpeg-2-demultiplexer.md">MPEG-2 Demultiplexer</a> filter converts a presentation time stamp (PTS) to stream time.</span></span>
<ul>
<li><span data-ttu-id="cb197-125"><strong>data</strong>[0]: Converted start time.</span><span class="sxs-lookup"><span data-stu-id="cb197-125"><strong>data</strong>[0]: Converted start time.</span></span></li>
<li><span data-ttu-id="cb197-126"><strong>data</strong>[1]: Converted stop time.</span><span class="sxs-lookup"><span data-stu-id="cb197-126"><strong>data</strong>[1]: Converted stop time.</span></span></li>
<li><span data-ttu-id="cb197-127"><strong>данные</strong>[2].</span><span class="sxs-lookup"><span data-stu-id="cb197-127"><strong>data</strong>[2].</span></span> <span data-ttu-id="cb197-128">Идентификатор потока для входного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cb197-128">Stream identifier for the input pin.</span></span></li>
<li><span data-ttu-id="cb197-129"><strong>data</strong>[3]: PTS that was converted.</span><span class="sxs-lookup"><span data-stu-id="cb197-129"><strong>data</strong>[3]: PTS that was converted.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb197-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="cb197-130">PERFINFO_STREAMTRACE_MPEG2DEMUX_SAMPLE_RECEIVE</span></span></td>
<td><span data-ttu-id="cb197-131">Записывается в журнал, когда демультиплексор MPEG-2 получает пример.</span><span class="sxs-lookup"><span data-stu-id="cb197-131">Logged when MPEG-2 Demultiplexer receives a sample.</span></span>
<ul>
<li><span data-ttu-id="cb197-132"><strong>данные</strong> [0]: Current time returned by  <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb197-132"><strong>data</strong>[0]: Current time returned by <a href="/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter"><strong>QueryPerformanceCounter</strong></a>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb197-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span><span class="sxs-lookup"><span data-stu-id="cb197-133">PERFINFO_STREAMTRACE_VMR_BEGIN_ADVISE</span></span></td>
<td><span data-ttu-id="cb197-134">Регистрируется, когда VMR планирует пример для подготовки к просмотру, непосредственно перед вызовом VMR <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>иреференцеклокк:: адвисетиме</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb197-134">Logged when the VMR schedules a sample for rendering, immediately before the VMR calls <a href="/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime"><strong>IReferenceClock::AdviseTime</strong></a>.</span></span>
<ul>
<li><span data-ttu-id="cb197-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span><span class="sxs-lookup"><span data-stu-id="cb197-135"><strong>data</strong>[0]: Reference time when streaming began, which corresponds to stream time zero.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb197-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span><span class="sxs-lookup"><span data-stu-id="cb197-136">PERFINFO_STREAMTRACE_VMR_BEGIN_DECODE</span></span></td>
<td><span data-ttu-id="cb197-137">Регистрируется, когда VMR начинает операцию декодирования, то есть когда декодер вызывает <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>иамвидеоакцелератор:: бегинфраме</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb197-137">Logged when the VMR begins a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe"><strong>IAMVideoAccelerator::BeginFrame</strong></a>.</span></span> <span data-ttu-id="cb197-138">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cb197-138">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb197-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="cb197-139">PERFINFO_STREAMTRACE_VMR_BEGIN_DEINTERLACE</span></span></td>
<td><span data-ttu-id="cb197-140">Регистрируется, когда VMR начинает операцию разчередования или композиции видео.</span><span class="sxs-lookup"><span data-stu-id="cb197-140">Logged when the VMR begins a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="cb197-141">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cb197-141">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb197-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span><span class="sxs-lookup"><span data-stu-id="cb197-142">PERFINFO_STREAMTRACE_VMR_DROPPED_FRAME</span></span></td>
<td><span data-ttu-id="cb197-143">Регистрируется, когда VMR удаляет кадр; Например, если образец был последним.</span><span class="sxs-lookup"><span data-stu-id="cb197-143">Logged when the VMR drops a frame; for example, if a sample was late.</span></span>
<ul>
<li><span data-ttu-id="cb197-144"><strong>data</strong>[0]: Sample start time.</span><span class="sxs-lookup"><span data-stu-id="cb197-144"><strong>data</strong>[0]: Sample start time.</span></span></li>
<li><span data-ttu-id="cb197-145"><strong>data</strong>[1]: Sample end time.</span><span class="sxs-lookup"><span data-stu-id="cb197-145"><strong>data</strong>[1]: Sample end time.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb197-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span><span class="sxs-lookup"><span data-stu-id="cb197-146">PERFINFO_STREAMTRACE_VMR_END_ADVISE</span></span></td>
<td><span data-ttu-id="cb197-147">Записывается в журнал, когда VMR получает уведомление о получении из ссылочного времени.</span><span class="sxs-lookup"><span data-stu-id="cb197-147">Logged when the VMR receives an advise notification from the reference clock.</span></span> <span data-ttu-id="cb197-148">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cb197-148">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb197-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span><span class="sxs-lookup"><span data-stu-id="cb197-149">PERFINFO_STREAMTRACE_VMR_END_DECODE</span></span></td>
<td><span data-ttu-id="cb197-150">Регистрируется, когда VMR завершает операцию декодирования, то есть когда декодер вызывает <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>иамвидеоакцелератор:: ендфраме</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cb197-150">Logged when the VMR ends a decoding operation—that is, when the decoder calls <a href="/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe"><strong>IAMVideoAccelerator::EndFrame</strong></a>.</span></span> <span data-ttu-id="cb197-151">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cb197-151">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb197-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span><span class="sxs-lookup"><span data-stu-id="cb197-152">PERFINFO_STREAMTRACE_VMR_END_DEINTERLACE</span></span></td>
<td><span data-ttu-id="cb197-153">Регистрируется, когда VMR завершает операцию разчередования или композицию видео.</span><span class="sxs-lookup"><span data-stu-id="cb197-153">Logged when the VMR completes a deinterlacing or video compositing operation.</span></span> <span data-ttu-id="cb197-154">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cb197-154">No event data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb197-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span><span class="sxs-lookup"><span data-stu-id="cb197-155">PERFINFO_STREAMTRACE_VMR_RECEIVE</span></span></td>
<td><span data-ttu-id="cb197-156">Регистрируется, когда VMR получает новый пример.</span><span class="sxs-lookup"><span data-stu-id="cb197-156">Logged when the VMR receives a new sample.</span></span> <span data-ttu-id="cb197-157">Нет данных события.</span><span class="sxs-lookup"><span data-stu-id="cb197-157">No event data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb197-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span><span class="sxs-lookup"><span data-stu-id="cb197-158">PERFINFO_STREAMTRACE_VMR_RENDER_TIME</span></span></td>
<td><span data-ttu-id="cb197-159">Регистрируется, когда VMR заканчивает отрисовку кадра.</span><span class="sxs-lookup"><span data-stu-id="cb197-159">Logged when the VMR finishes rendering a frame.</span></span>
<ul>
<li><span data-ttu-id="cb197-160"><strong>data</strong>[0]: Time that it took to render this frame.</span><span class="sxs-lookup"><span data-stu-id="cb197-160"><strong>data</strong>[0]: Time that it took to render this frame.</span></span></li>
<li><span data-ttu-id="cb197-161"><strong>data</strong>[1]: Running average of frame rendering times.</span><span class="sxs-lookup"><span data-stu-id="cb197-161"><strong>data</strong>[1]: Running average of frame rendering times.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cb197-162">Чтобы заносить это событие из фильтра DirectShow, используйте функцию **перфлог \_ стреамтраце** , которая определена в файле заголовка дксмперф. h.</span><span class="sxs-lookup"><span data-stu-id="cb197-162">To log this event from a DirectShow filter, use the **PERFLOG\_STREAMTRACE** function, which is defined in the header file Dxmperf.h.</span></span> <span data-ttu-id="cb197-163">Этот заголовок включен в базовые классы DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cb197-163">This header is included in the DirectShow base classes.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb197-164">Требования</span><span class="sxs-lookup"><span data-stu-id="cb197-164">Requirements</span></span>



| <span data-ttu-id="cb197-165">Требование</span><span class="sxs-lookup"><span data-stu-id="cb197-165">Requirement</span></span> | <span data-ttu-id="cb197-166">Значение</span><span class="sxs-lookup"><span data-stu-id="cb197-166">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb197-167">Header</span><span class="sxs-lookup"><span data-stu-id="cb197-167">Header</span></span><br/> | <dl> <span data-ttu-id="cb197-168"><dt>Перфструкт. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb197-168"><dt>Perfstruct.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb197-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb197-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb197-170">Структуры DirectShow</span><span class="sxs-lookup"><span data-stu-id="cb197-170">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="cb197-171">Трассировка событий в DirectShow</span><span class="sxs-lookup"><span data-stu-id="cb197-171">Event Tracing in DirectShow</span></span>](event-tracing-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="cb197-172">Идентификаторы GUID событий трассировки</span><span class="sxs-lookup"><span data-stu-id="cb197-172">Trace Event GUIDs</span></span>](trace-guids.md)
</dt> </dl>

 

 
