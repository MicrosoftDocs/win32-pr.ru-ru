---
description: Структура НМЕВЕНТДАТА содержит сведения о состоянии события, которое передается сетевой монитор для вставки строки в средство просмотра экспертов.
ms.assetid: 35cda410-d45a-4a51-91b7-8bd4a0c9957f
title: Структура НМЕВЕНТДАТА (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMEVENTDATA
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 6258b1b1bfde5b159165de2efb9a010053c0421a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897798"
---
# <a name="nmeventdata-structure"></a><span data-ttu-id="a1b9a-103">Структура НМЕВЕНТДАТА</span><span class="sxs-lookup"><span data-stu-id="a1b9a-103">NMEVENTDATA structure</span></span>

<span data-ttu-id="a1b9a-104">Структура **нмевентдата** содержит сведения о состоянии события, которое передается сетевой монитор для вставки строки в средство просмотра экспертов.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-104">The **NMEVENTDATA** structure contains information about an event condition that is passed to Network Monitor to insert a line in the expert viewer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b9a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1b9a-105">Syntax</span></span>


```C++
typedef struct {
  BYTE         Version;
  DWORD        EventIdent;
  DWORD        Flags;
  DWORD        Severity;
  BYTE         NumColumns;
  LPSTR        szSourceName;
  LPSTR        szEventName;
  LPSTR        szDescription;
  LPSTR        szMachine;
  JTYPE        Justification;
  LPSTR        szUrl;
  SYSTEMTIME   SysTime;
  NMCOLUMNINFO Column[];
} NMEVENTDATA, *PNMEVENTDATA;
```



## <a name="members"></a><span data-ttu-id="a1b9a-106">Члены</span><span class="sxs-lookup"><span data-stu-id="a1b9a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1b9a-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-108">Номер версии структуры **нмевентдата** .</span><span class="sxs-lookup"><span data-stu-id="a1b9a-108">Version number of the **NMEVENTDATA** structure.</span></span> <span data-ttu-id="a1b9a-109">Номер версии должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-109">The version number must be zero.</span></span> <span data-ttu-id="a1b9a-110">Будущие версии сетевой монитор могут поддерживать более высокий номер версии.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-110">Future versions of Network Monitor may support a higher version number.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-111">**евентидент**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-111">**EventIdent**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-112">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-112">Identifier of the event.</span></span> <span data-ttu-id="a1b9a-113">**Евентидент** является уникальным для каждого эксперта и ссылается на [страницу ссылки на событие](event-reference-page.md).</span><span class="sxs-lookup"><span data-stu-id="a1b9a-113">**EventIdent** is unique to each expert, and references an [event reference page](event-reference-page.md).</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-114">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-114">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-115">Набор флагов, описывающих, кто отправляет данные о событии и как отображается событие.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-115">A set of flags that describes who sends the event data, and how the event is displayed.</span></span>



| <span data-ttu-id="a1b9a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a1b9a-116">Value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="a1b9a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a1b9a-117">Meaning</span></span>                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EVENT_FLAG_EXPERT"></span><span id="event_flag_expert"></span><dl> <span data-ttu-id="a1b9a-118"><dt>**\_эксперт по флагам событий \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-118"><dt>**EVENT\_FLAG\_EXPERT**</dt></span></span> </dl>                                                                         | <span data-ttu-id="a1b9a-119">Это событие поступило от эксперта.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-119">The event came from an expert.</span></span> <br/>                                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SEVERITY"></span><span id="nmeventflag_do_not_display_severity"></span><dl> <span data-ttu-id="a1b9a-120"><dt>**НМЕВЕНТФЛАГ \_ не \_ \_ отображают \_ серьезность**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-120"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SEVERITY**</dt></span></span> </dl>                 | <span data-ttu-id="a1b9a-121">Не отображать уровень серьезности для события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-121">Do not display the severity level for the event.</span></span> <br/>                                                                                                                |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_SOURCE"></span><span id="nmeventflag_do_not_display_source"></span><dl> <span data-ttu-id="a1b9a-122"><dt>**НМЕВЕНТФЛАГ \_ \_ не \_ отображать \_ Исходный код**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-122"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_SOURCE**</dt></span></span> </dl>                       | <span data-ttu-id="a1b9a-123">Не показывать имя источника для события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-123">Do not display the source name for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_EVENT_NAME"></span><span id="nmeventflag_do_not_display_event_name"></span><dl> <span data-ttu-id="a1b9a-124"><dt>**НМЕВЕНТФЛАГ \_ \_ не \_ отображать \_ имя события \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-124"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_EVENT\_NAME**</dt></span></span> </dl>          | <span data-ttu-id="a1b9a-125">Не отображать имя события для события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-125">Do not display the event name for the event.</span></span> <br/>                                                                                                                    |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_DESCRIPTION"></span><span id="nmeventflag_do_not_display_description"></span><dl> <span data-ttu-id="a1b9a-126"><dt>**НМЕВЕНТФЛАГ \_ \_ не \_ отображать \_ Описание**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-126"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_DESCRIPTION**</dt></span></span> </dl>        | <span data-ttu-id="a1b9a-127">Не отображать описание события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-127">Do not display the description for the event.</span></span> <br/>                                                                                                                   |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_MACHINE"></span><span id="nmeventflag_do_not_display_machine"></span><dl> <span data-ttu-id="a1b9a-128"><dt>**НМЕВЕНТФЛАГ \_ \_ не \_ отображать \_ компьютер**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-128"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_MACHINE**</dt></span></span> </dl>                    | <span data-ttu-id="a1b9a-129">Не отображать имя компьютера для события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-129">Do not display the machine name for the event.</span></span> <br/>                                                                                                                  |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_TIME"></span><span id="nmeventflag_do_not_display_time"></span><dl> <span data-ttu-id="a1b9a-130"><dt>**НМЕВЕНТФЛАГ \_ не \_ \_ Показывать \_ время**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-130"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_TIME**</dt></span></span> </dl>                             | <span data-ttu-id="a1b9a-131">Не показывать время события</span><span class="sxs-lookup"><span data-stu-id="a1b9a-131">Do not display the time for the event</span></span> <br/>                                                                                                                           |
| <span id="NMEVENTFLAG_DO_NOT_DISPLAY_FIXED_COLUMNS"></span><span id="nmeventflag_do_not_display_fixed_columns"></span><dl> <span data-ttu-id="a1b9a-132"><dt>**НМЕВЕНТФЛАГ \_ \_ не \_ отображают \_ фиксированные \_ столбцы**</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-132"><dt>**NMEVENTFLAG\_DO\_NOT\_DISPLAY\_FIXED\_COLUMNS**</dt></span></span> </dl> | <span data-ttu-id="a1b9a-133">Не отображать столбцы серьезности, источник, имя события, описание, компьютер или время.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-133">Do not display the Severity, Source, Event Name, Description, Machine, or Time columns.</span></span> <span data-ttu-id="a1b9a-134">Это не один флаг, но это объединение предыдущих шести флагов.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-134">This is not a single flag, but it is a union of the previous six flags.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="a1b9a-135">**Уровень серьезности**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-135">**Severity**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-136">Уровень серьезности события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-136">Severity level of the event.</span></span> <span data-ttu-id="a1b9a-137">Степень серьезности может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a1b9a-137">The severity level can have one of the following values:</span></span>

<span data-ttu-id="a1b9a-138">НМЕВЕНТ \_ SEVERITY \_ нмевент \_ Severity \_ warning нмевент \_ серьезность критическое \_ \_ предупреждение нмевент \_ серьезность \_ Ошибка нмевент серьезность ошибки нмевент Severity \_ \_ \_ \_ \_ критическая \_ Ошибка</span><span class="sxs-lookup"><span data-stu-id="a1b9a-138">NMEVENT\_SEVERITY\_INFORMATIONAL NMEVENT\_SEVERITY\_WARNING NMEVENT\_SEVERITY\_STRONG\_WARNING NMEVENT\_SEVERITY\_ERROR NMEVENT\_SEVERITY\_SEVERE\_ERROR NMEVENT\_SEVERITY\_CRITICAL\_ERROR</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-139">**нумколумнс**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-139">**NumColumns**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-140">Число столбцов, выделенных в текущей структуре.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-140">Number of columns designated in the current structure.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-141">**сзсаурценаме**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-141">**szSourceName**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-142">Имя отображаемого эксперта.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-142">Name of the expert that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-143">**сзевентнаме**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-143">**szEventName**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-144">Имя отображаемого события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-144">Name of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-145">**сздескриптион**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-145">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-146">Описание события, которое отображается.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-146">Description of the event that is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-147">**сзмачине**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-147">**szMachine**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-148">Устаревший параметр, должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-148">Obsolete, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-149">**Обоснование**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-149">**Justification**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-150">Сведения, отображаемые во втором окне Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-150">Information displayed in the second window of the Event Viewer.</span></span> <span data-ttu-id="a1b9a-151">Элемент **обоснования** может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-151">The **Justification** member may be **NULL**.</span></span> <span data-ttu-id="a1b9a-152">Если значение равно **null**, второе окно не будет видимым.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-152">If it is **NULL**, the second window is not be visible.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-153">**сзурл**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-153">**szUrl**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-154">Процессу Этот элемент должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-154">Reserved; this member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-155">**систиме**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-155">**SysTime**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-156">Время возникновения условия события.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-156">Time at which the event condition occurs.</span></span> <span data-ttu-id="a1b9a-157">Время измеряется относительно начала записи.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-157">The time is measured relative to the beginning of the capture.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-158">**Столбец**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-158">**Column**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-159">Таблица структур столбцов, отображаемых в верхней области Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-159">Table of column structures that appears in the top pane of the Event Viewer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1b9a-160">Требования</span><span class="sxs-lookup"><span data-stu-id="a1b9a-160">Requirements</span></span>



| <span data-ttu-id="a1b9a-161">Требование</span><span class="sxs-lookup"><span data-stu-id="a1b9a-161">Requirement</span></span> | <span data-ttu-id="a1b9a-162">Значение</span><span class="sxs-lookup"><span data-stu-id="a1b9a-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a1b9a-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1b9a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a1b9a-164">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1b9a-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a1b9a-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1b9a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a1b9a-166">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a1b9a-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a1b9a-167">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a1b9a-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1b9a-168"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1b9a-168"><dt>Netmon.h</dt></span></span> </dl> |



 

 




