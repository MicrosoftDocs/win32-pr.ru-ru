---
description: Объект SWbemDateTime — это вспомогательный объект для синтаксического анализа и установки значений DateTime модель CIM (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Объект SWbemDateTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 65f3f9836b52693e3f74bac5cfd94553e02d7bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702363"
---
# <a name="swbemdatetime-object"></a><span data-ttu-id="ea512-103">Объект SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="ea512-103">SWbemDateTime object</span></span>

<span data-ttu-id="ea512-104">Объект **SWbemDateTime** — это вспомогательный объект для синтаксического анализа и установки значений [DateTime](datetime.md) модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="ea512-104">The **SWbemDateTime** object is a helper object to parse and set Common Information Model (CIM) [datetime](datetime.md) values.</span></span> <span data-ttu-id="ea512-105">Он играет роль, аналогичную [**свбемобжектпас**](swbemobjectpath.md), которая обеспечивает поддержку форматирования и интерпретации путей к объектам.</span><span class="sxs-lookup"><span data-stu-id="ea512-105">It plays a role similar to [**SWbemObjectPath**](swbemobjectpath.md), which provides assistance to format and interpret object paths.</span></span> <span data-ttu-id="ea512-106">Для создания объекта **SWbemDateTime** можно использовать вызов функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript.</span><span class="sxs-lookup"><span data-stu-id="ea512-106">You can use the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call to create the **SWbemDateTime** object.</span></span>

<span data-ttu-id="ea512-107">Объект **SWbemDateTime** можно инициализировать из и отформатировать в значениях **VT \_** или **fileTime** с помощью методов объекта.</span><span class="sxs-lookup"><span data-stu-id="ea512-107">An **SWbemDateTime** object can be initialized from and formatted in either **VT\_DATE** or **FILETIME** values using methods on the object.</span></span> <span data-ttu-id="ea512-108">С помощью свойств объекта значение может быть проанализировано в год, месяц, день, час, минуты, секунды или микросекунды.</span><span class="sxs-lookup"><span data-stu-id="ea512-108">Using properties of the object, the value can be parsed into component year, month, day, hour, minutes, seconds, or microseconds.</span></span> <span data-ttu-id="ea512-109">Объект **SWbemDateTime** можно отформатировать как локальное значение, так и в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="ea512-109">The **SWbemDateTime** object can be formatted into either local or Coordinated Universal Time (UTC) values.</span></span> <span data-ttu-id="ea512-110">Дополнительные сведения см. в разделе [Формат даты и времени](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="ea512-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="ea512-111">**SWbemDateTime** — это единственный объект скрипта инструментарий управления Windows (WMI) (WMI), помеченный как надежный для инициализации и скриптов, выполняющихся на HTML-страницах в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ea512-111">**SWbemDateTime** is the only Windows Management Instrumentation (WMI) scripting object that is marked safe for initialization and scripts running on HTML pages in Internet Explorer.</span></span>

## <a name="members"></a><span data-ttu-id="ea512-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="ea512-112">Members</span></span>

<span data-ttu-id="ea512-113">Объект **SWbemDateTime** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ea512-113">The **SWbemDateTime** object has these types of members:</span></span>

-   [<span data-ttu-id="ea512-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ea512-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ea512-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="ea512-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ea512-116">Методы</span><span class="sxs-lookup"><span data-stu-id="ea512-116">Methods</span></span>

<span data-ttu-id="ea512-117">Объект **SWbemDateTime** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="ea512-117">The **SWbemDateTime** object has these methods.</span></span>



| <span data-ttu-id="ea512-118">Метод</span><span class="sxs-lookup"><span data-stu-id="ea512-118">Method</span></span>                                           | <span data-ttu-id="ea512-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ea512-119">Description</span></span>                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea512-120">**Функции getFileTime**</span><span class="sxs-lookup"><span data-stu-id="ea512-120">**GetFileTime**</span></span>](swbemdatetime-getfiletime.md) | <span data-ttu-id="ea512-121">Преобразует дату и время **fileTime** , выраженные в виде **BSTR**, в формат [DateTime](datetime.md) WMI.</span><span class="sxs-lookup"><span data-stu-id="ea512-121">Converts a **FILETIME** date and time, expressed as a **BSTR**, to a WMI [DATETIME](datetime.md) format.</span></span><br/> |
| [<span data-ttu-id="ea512-122">**GetVarDate**</span><span class="sxs-lookup"><span data-stu-id="ea512-122">**GetVarDate**</span></span>](swbemdatetime-getvardate.md)   | <span data-ttu-id="ea512-123">Преобразует значение даты и времени в формате WMI [DateTime](datetime.md) в **\_ дату VT**.</span><span class="sxs-lookup"><span data-stu-id="ea512-123">Converts a WMI [DATETIME](datetime.md) formatted date and time value to a **VT\_DATE**.</span></span><br/>                  |
| [<span data-ttu-id="ea512-124">**сетфилетиме**</span><span class="sxs-lookup"><span data-stu-id="ea512-124">**SetFileTime**</span></span>](swbemdatetime-setfiletime.md) | <span data-ttu-id="ea512-125">Преобразует формат [DateTime](datetime.md) WMI в значение даты и времени **fileTime** , выраженное в виде **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ea512-125">Converts a WMI [DATETIME](datetime.md) format to a **FILETIME** date and time, expressed as a **BSTR**.</span></span><br/>  |
| [<span data-ttu-id="ea512-126">**сетвардате**</span><span class="sxs-lookup"><span data-stu-id="ea512-126">**SetVarDate**</span></span>](swbemdatetime-setvardate.md)   | <span data-ttu-id="ea512-127">Преобразует дату и время в формате **\_ VT** в [значение DateTime](datetime.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="ea512-127">Converts a **VT\_DATE** formatted date and time to a WMI [DATETIME](datetime.md).</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="ea512-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="ea512-128">Properties</span></span>

<span data-ttu-id="ea512-129">Объект **SWbemDateTime** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ea512-129">The **SWbemDateTime** object has these properties.</span></span>



| <span data-ttu-id="ea512-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="ea512-130">Property</span></span>                                                                        | <span data-ttu-id="ea512-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ea512-131">Access type</span></span>           | <span data-ttu-id="ea512-132">Описание</span><span class="sxs-lookup"><span data-stu-id="ea512-132">Description</span></span>                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ea512-133">**День**</span><span class="sxs-lookup"><span data-stu-id="ea512-133">**Day**</span></span>](swbemdatetime-day.md)<br/>                                     | <span data-ttu-id="ea512-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-134">Read/write</span></span><br/> | <span data-ttu-id="ea512-135">Компонент дня для значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-135">The day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="ea512-136">**дайспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-136">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)<br/>                   | <span data-ttu-id="ea512-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-137">Read/write</span></span><br/> | <span data-ttu-id="ea512-138">Указывает, указан ли день в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-138">Indicates whether the day is specified or left as a wildcard.</span></span><br/>                                                        |
| [<span data-ttu-id="ea512-139">**Hours**</span><span class="sxs-lookup"><span data-stu-id="ea512-139">**Hours**</span></span>](swbemdatetime-hours.md)<br/>                                 | <span data-ttu-id="ea512-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-140">Read/write</span></span><br/> | <span data-ttu-id="ea512-141">Часы компонента дня в значении [даты и времени](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-141">The hours of the day component of a CIM [datetime](datetime.md) value.</span></span><br/>                                              |
| [<span data-ttu-id="ea512-142">**хаурсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-142">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)<br/>               | <span data-ttu-id="ea512-143">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-143">Read/write</span></span><br/> | <span data-ttu-id="ea512-144">Указывает, указан ли час или оставлен в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-144">Indicates whether the hour is specified or left as a wildcard.</span></span><br/>                                                       |
| [<span data-ttu-id="ea512-145">**Параметр "интервал"**</span><span class="sxs-lookup"><span data-stu-id="ea512-145">**IsInterval**</span></span>](swbemdatetime-isinterval.md)<br/>                       | <span data-ttu-id="ea512-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-146">Read/write</span></span><br/> | <span data-ttu-id="ea512-147">Указывает, что хотя бы один компонент [даты и времени](datetime.md) CIM представляет интервал, а не дату.</span><span class="sxs-lookup"><span data-stu-id="ea512-147">Indicates that at least one component of the CIM [datetime](datetime.md) represents an interval rather than a date.</span></span><br/> |
| [<span data-ttu-id="ea512-148">**Микросекундах**</span><span class="sxs-lookup"><span data-stu-id="ea512-148">**Microseconds**</span></span>](swbemdatetime-microseconds.md)<br/>                   | <span data-ttu-id="ea512-149">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-149">Read/write</span></span><br/> | <span data-ttu-id="ea512-150">Компонент микросекунд для значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-150">The microseconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                  |
| [<span data-ttu-id="ea512-151">**микросекондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-151">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)<br/> | <span data-ttu-id="ea512-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-152">Read/write</span></span><br/> | <span data-ttu-id="ea512-153">Указывает, указан ли компонент микросекунд в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-153">Indicates whether the microseconds component is specified or left as a wildcard.</span></span><br/>                                     |
| [<span data-ttu-id="ea512-154">**Минуты**</span><span class="sxs-lookup"><span data-stu-id="ea512-154">**Minutes**</span></span>](swbemdatetime-minutes.md)<br/>                             | <span data-ttu-id="ea512-155">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-155">Read/write</span></span><br/> | <span data-ttu-id="ea512-156">Компонент минут для значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-156">The minutes component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="ea512-157">**минутесспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-157">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)<br/>           | <span data-ttu-id="ea512-158">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-158">Read/write</span></span><br/> | <span data-ttu-id="ea512-159">Указывает, указан ли компонент минут или оставлен в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-159">Indicates whether the minutes component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="ea512-160">**Месяц**</span><span class="sxs-lookup"><span data-stu-id="ea512-160">**Month**</span></span>](swbemdatetime-month.md)<br/>                                 | <span data-ttu-id="ea512-161">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-161">Read/write</span></span><br/> | <span data-ttu-id="ea512-162">Компонент месяца для значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-162">The month component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                         |
| [<span data-ttu-id="ea512-163">**монсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-163">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)<br/>               | <span data-ttu-id="ea512-164">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-164">Read/write</span></span><br/> | <span data-ttu-id="ea512-165">Указывает, указан ли месяц или Left в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-165">Indicates whether the month is specified or left as a wildcard.</span></span><br/>                                                      |
| [<span data-ttu-id="ea512-166">**Секунды**</span><span class="sxs-lookup"><span data-stu-id="ea512-166">**Seconds**</span></span>](swbemdatetime-seconds.md)<br/>                             | <span data-ttu-id="ea512-167">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-167">Read/write</span></span><br/> | <span data-ttu-id="ea512-168">Компонент секунд для значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-168">The seconds component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                       |
| [<span data-ttu-id="ea512-169">**секондсспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-169">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)<br/>           | <span data-ttu-id="ea512-170">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-170">Read/write</span></span><br/> | <span data-ttu-id="ea512-171">Указывает, указан ли компонент секунд или является его левым в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-171">Indicates whether the seconds component is specified or left as a wildcard.</span></span><br/>                                          |
| [<span data-ttu-id="ea512-172">**ФОРМАТА**</span><span class="sxs-lookup"><span data-stu-id="ea512-172">**UTC**</span></span>](swbemdatetime-utc.md)<br/>                                     | <span data-ttu-id="ea512-173">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-173">Read/write</span></span><br/> | <span data-ttu-id="ea512-174">Компонент времени в формате UTC значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-174">The UTC component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                           |
| [<span data-ttu-id="ea512-175">**уткспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-175">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)<br/>                   | <span data-ttu-id="ea512-176">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-176">Read/write</span></span><br/> | <span data-ttu-id="ea512-177">Указывает, указан ли компонент времени в формате UTC или является его левым в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-177">Indicates whether the UTC component is specified or left as a wildcard.</span></span><br/>                                              |
| [<span data-ttu-id="ea512-178">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ea512-178">**Value**</span></span>](swbemdatetime-value.md)<br/>                                 | <span data-ttu-id="ea512-179">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-179">Read/write</span></span><br/> | <span data-ttu-id="ea512-180">Полное значение [даты и времени](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-180">The full CIM [datetime](datetime.md) value.</span></span><br/>                                                                         |
| [<span data-ttu-id="ea512-181">**Год**</span><span class="sxs-lookup"><span data-stu-id="ea512-181">**Year**</span></span>](swbemdatetime-year.md)<br/>                                   | <span data-ttu-id="ea512-182">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-182">Read/write</span></span><br/> | <span data-ttu-id="ea512-183">Компонент года для значения [DateTime](datetime.md) CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-183">The year component of a CIM [datetime](datetime.md) value.</span></span><br/>                                                          |
| [<span data-ttu-id="ea512-184">**еарспеЦифиед**</span><span class="sxs-lookup"><span data-stu-id="ea512-184">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)<br/>                 | <span data-ttu-id="ea512-185">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ea512-185">Read/write</span></span><br/> | <span data-ttu-id="ea512-186">Указывает, указан ли год или нет в качестве подстановочного знака.</span><span class="sxs-lookup"><span data-stu-id="ea512-186">Indicates whether or not the year is specified or left as a wildcard.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="ea512-187">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea512-187">Remarks</span></span>

<span data-ttu-id="ea512-188">WMI записывает отметки времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="ea512-188">WMI records timestamps in universal time coordinate (UTC) format.</span></span> <span data-ttu-id="ea512-189">Время в формате UTC не используется большинство разработчиков и ИТ-администраторов.</span><span class="sxs-lookup"><span data-stu-id="ea512-189">UTC is not the format that most developers and IT administrators use.</span></span> <span data-ttu-id="ea512-190">Поэтому распространенной проблемой является определение способа перевода времени в формате UTC в более удобочитаемый формат.</span><span class="sxs-lookup"><span data-stu-id="ea512-190">Therefore, a common issue is determining how to translate UTC into something more readable.</span></span> <span data-ttu-id="ea512-191">Дополнительные сведения о работе со временем в формате UTC см. в разделе [задачи WMI: даты и времени](wmi-tasks--dates-and-times.md) и [Работа с датами и временем с помощью WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="ea512-191">For more information on how to work with UTC, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md) and [Working with Dates and Times using WMI](/previous-versions/tn-archive/ee198928(v=technet.10)).</span></span> <span data-ttu-id="ea512-192">Кроме того, можно прочитать [сведения о времени (и о датах)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) , а также о том, [как вычесть указанное число дней из значения времени в формате UTC?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) записи блога для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="ea512-192">You can also read the [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) and [How Can I Subtract a Specified Number of Days from a UTC Value?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) blog posts for additional information.</span></span>

<span data-ttu-id="ea512-193">Любое числовое поле может иметь подстановочное значение, [**Если свойство ISNUMERIC**](swbemdatetime-isinterval.md) имеет значение **false**.</span><span class="sxs-lookup"><span data-stu-id="ea512-193">Any numeric field can have a wildcard value if the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span> <span data-ttu-id="ea512-194">Поля с подстановочными значениями содержат звездочки во всем поле.</span><span class="sxs-lookup"><span data-stu-id="ea512-194">Fields with wildcard values contain asterisks in the entire field.</span></span>

<span data-ttu-id="ea512-195">Каждое свойство, например [**Day**](swbemdatetime-day.md), имеет соответствующее заданное логическое значение, например [**дайспеЦифиед**](swbemdatetime-dayspecified.md).</span><span class="sxs-lookup"><span data-stu-id="ea512-195">Each property, for example [**Day**](swbemdatetime-day.md), has a corresponding specified Boolean value, such as [**DaySpecified**](swbemdatetime-dayspecified.md).</span></span> <span data-ttu-id="ea512-196">Если **дайспеЦифиед** имеет значение **false**, то значение интерпретируется как интервал, а не число от 01 до 31.</span><span class="sxs-lookup"><span data-stu-id="ea512-196">When **DaySpecified** is **FALSE**, then the value is interpreted as an interval rather than a number between 01 and 31.</span></span> <span data-ttu-id="ea512-197">Если интервал используется в любом месте в значении [даты и времени](datetime.md) CIM [**, то параметру IsTrue также присваивается**](swbemdatetime-isinterval.md) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ea512-197">If an interval is used anywhere in the CIM [datetime](datetime.md) value, then [**IsInterval**](swbemdatetime-isinterval.md) is also set to **TRUE**.</span></span> <span data-ttu-id="ea512-198">По умолчанию значение DateTime в CIM должно содержать дату, а не один или несколько интервалов.</span><span class="sxs-lookup"><span data-stu-id="ea512-198">The default is for a CIM datetime value to contain a date rather than one or more intervals.</span></span>

<span data-ttu-id="ea512-199">Например, если [**SWbemDateTime. дайспеЦифиед**](swbemdatetime-dayspecified.md) имеет **значение true**, то [**SWbemDateTime. Value**](swbemdatetime-value.md) включает текущее значение [**SWbemDateTime. Day**](swbemdatetime-day.md), в противном случае это значение с подстановочным знаком.</span><span class="sxs-lookup"><span data-stu-id="ea512-199">For example, if [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) is **TRUE**, then [**SWbemDateTime.Value**](swbemdatetime-value.md) includes the current value of [**SWbemDateTime.Day**](swbemdatetime-day.md), otherwise it is a wildcard value.</span></span> <span data-ttu-id="ea512-200">В [**любом случае свойство**](swbemdatetime-isinterval.md) **IsFalse имеет значение false** .</span><span class="sxs-lookup"><span data-stu-id="ea512-200">The [**IsInterval**](swbemdatetime-isinterval.md) property is **FALSE** in either case.</span></span>

## <a name="examples"></a><span data-ttu-id="ea512-201">Примеры</span><span class="sxs-lookup"><span data-stu-id="ea512-201">Examples</span></span>

<span data-ttu-id="ea512-202">В следующем примере кода скрипта показано, как использовать объект **SWbemDateTime** для анализа значения свойства DateTime, считанного из репозитория WMI, свойства **инсталлдате** в [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="ea512-202">The following script code example shows how to use an **SWbemDateTime** object to parse a datetime property value read from the WMI repository, the **InstallDate** property in [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span>


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



<span data-ttu-id="ea512-203">В следующем примере показано, как создать объект **SWbemDateTime** , сохранить значение даты в объекте, отобразить дату в виде местного времени (UTC) и сохранить значение во вновь созданном классе и свойстве.</span><span class="sxs-lookup"><span data-stu-id="ea512-203">The following example shows how to create an **SWbemDateTime** object, store a date value in the object, display the date as local and Coordinated Universal Time (UTC), and store the value in a newly created class and property.</span></span> <span data-ttu-id="ea512-204">Дополнительные сведения о константной **вбемЦимтипедатетиме** см. в разделе [вбемЦимтипинум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span><span class="sxs-lookup"><span data-stu-id="ea512-204">For more information about the constant **wbemCimtypeDatetime**, see [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).</span></span>


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



<span data-ttu-id="ea512-205">В следующем примере кода скрипта показано, как использовать объект **SWbemDateTime** для изменения значения интервала в свойстве, которое считывается из репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="ea512-205">The following script code example shows how to use an **SWbemDateTime** object to modify an interval value on a property that is read from the WMI repository.</span></span>


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



<span data-ttu-id="ea512-206">В следующем примере кода скрипта показано, как использовать объект **свбемдате** для считывания значения **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="ea512-206">The following script code example shows how to use an **SWbemDate** object to read a **FILETIME** value.</span></span>


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



<span data-ttu-id="ea512-207">Следующий код PowerShell создает экземпляр объекта SWbemDateTime, получает дату установки ОС и преобразует дату в другой формат.</span><span class="sxs-lookup"><span data-stu-id="ea512-207">The following PowerShell code creates an instance of a SWbemDateTime object, retrieves the OS install date, and converts the date to a different format</span></span>


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



<span data-ttu-id="ea512-208">Следующий код PowerShell преобразует код в формат, готовый для использования поставщиком CIM.</span><span class="sxs-lookup"><span data-stu-id="ea512-208">The following Powershell code translates the code into a format ready to be consumed by a CIM provider.</span></span>


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a><span data-ttu-id="ea512-209">Требования</span><span class="sxs-lookup"><span data-stu-id="ea512-209">Requirements</span></span>



| <span data-ttu-id="ea512-210">Требование</span><span class="sxs-lookup"><span data-stu-id="ea512-210">Requirement</span></span> | <span data-ttu-id="ea512-211">Значение</span><span class="sxs-lookup"><span data-stu-id="ea512-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea512-212">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea512-212">Minimum supported client</span></span><br/> | <span data-ttu-id="ea512-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ea512-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ea512-214">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea512-214">Minimum supported server</span></span><br/> | <span data-ttu-id="ea512-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea512-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ea512-216">Header</span><span class="sxs-lookup"><span data-stu-id="ea512-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea512-217"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea512-217"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea512-218">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ea512-218">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea512-219"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea512-219"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea512-220">DLL</span><span class="sxs-lookup"><span data-stu-id="ea512-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea512-221"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea512-221"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea512-222">CLSID</span><span class="sxs-lookup"><span data-stu-id="ea512-222">CLSID</span></span><br/>                    | <span data-ttu-id="ea512-223">\_SWBEMDATETIME CLSID</span><span class="sxs-lookup"><span data-stu-id="ea512-223">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="ea512-224">IID</span><span class="sxs-lookup"><span data-stu-id="ea512-224">IID</span></span><br/>                      | <span data-ttu-id="ea512-225">IID \_ исвбемдатетиме</span><span class="sxs-lookup"><span data-stu-id="ea512-225">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ea512-226">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea512-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea512-227">вбемЦимтипинум</span><span class="sxs-lookup"><span data-stu-id="ea512-227">WbemCimtypeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[<span data-ttu-id="ea512-228">DATETIME</span><span class="sxs-lookup"><span data-stu-id="ea512-228">DATETIME</span></span>](datetime.md)
</dt> <dt>

[<span data-ttu-id="ea512-229">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="ea512-229">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

