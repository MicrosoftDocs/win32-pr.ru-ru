---
description: '\_Часовой пояс Win32&\# 8194; Класс WMI представляет сведения о часовом поясе для компьютерной системы под Windows, включая изменения, необходимые для перехода на переход на летнее время.'
ms.assetid: c1c7731e-768f-42ea-a36c-57b00df6848e
ms.tgt_platform: multiple
title: Класс Win32_TimeZone
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_TimeZone
- Win32_TimeZone.Caption
- Win32_TimeZone.Description
- Win32_TimeZone.SettingID
- Win32_TimeZone.Bias
- Win32_TimeZone.DaylightBias
- Win32_TimeZone.DaylightDay
- Win32_TimeZone.DaylightDayOfWeek
- Win32_TimeZone.DaylightHour
- Win32_TimeZone.DaylightMillisecond
- Win32_TimeZone.DaylightMinute
- Win32_TimeZone.DaylightMonth
- Win32_TimeZone.DaylightName
- Win32_TimeZone.DaylightSecond
- Win32_TimeZone.DaylightYear
- Win32_TimeZone.StandardBias
- Win32_TimeZone.StandardDay
- Win32_TimeZone.StandardDayOfWeek
- Win32_TimeZone.StandardHour
- Win32_TimeZone.StandardMillisecond
- Win32_TimeZone.StandardMinute
- Win32_TimeZone.StandardMonth
- Win32_TimeZone.StandardName
- Win32_TimeZone.StandardSecond
- Win32_TimeZone.StandardYear
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 433682f045ca7fb127c7dc69e3a26ed8356371ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895785"
---
# <a name="win32_timezone-class"></a><span data-ttu-id="bd657-103">\_Класс часового пояса Win32</span><span class="sxs-lookup"><span data-stu-id="bd657-103">Win32\_TimeZone class</span></span>

<span data-ttu-id="bd657-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ TimeZone для Win32** представляет сведения о часовом поясе для компьютерной системы под Windows, включая изменения, необходимые для перехода на переход на летнее время.</span><span class="sxs-lookup"><span data-stu-id="bd657-104">The **Win32\_TimeZone** [WMI class](../wmisdk/retrieving-a-class.md) represents the time zone information for a computer system running Windows, which includes the changes required for transitioning to daylight saving time transition.</span></span>

<span data-ttu-id="bd657-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bd657-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bd657-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="bd657-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd657-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd657-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_TimeZone : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  sint32 Bias;
  sint32 DaylightBias;
  uint32 DaylightDay;
  uint8  DaylightDayOfWeek;
  uint32 DaylightHour;
  uint32 DaylightMillisecond;
  uint32 DaylightMinute;
  uint32 DaylightMonth;
  string DaylightName;
  uint32 DaylightSecond;
  uint32 DaylightYear;
  uint32 StandardBias;
  uint32 StandardDay;
  uint8  StandardDayOfWeek;
  uint32 StandardHour;
  uint32 StandardMillisecond;
  uint32 StandardMinute;
  uint32 StandardMonth;
  string StandardName;
  uint32 StandardSecond;
  uint32 StandardYear;
};
```

## <a name="members"></a><span data-ttu-id="bd657-108">Члены</span><span class="sxs-lookup"><span data-stu-id="bd657-108">Members</span></span>

<span data-ttu-id="bd657-109">Класс **\_ часового пояса Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bd657-109">The **Win32\_TimeZone** class has these types of members:</span></span>

-   [<span data-ttu-id="bd657-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd657-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd657-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="bd657-111">Properties</span></span>

<span data-ttu-id="bd657-112">Класс **\_ часового пояса Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bd657-112">The **Win32\_TimeZone** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd657-113">**Смещение**</span><span class="sxs-lookup"><span data-stu-id="bd657-113">**Bias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-114">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bd657-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-116">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| времени структуры времени \| [**часового \_ пояса \_**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="bd657-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-117">Текущий сдвиг для локального перевода времени.</span><span class="sxs-lookup"><span data-stu-id="bd657-117">Current bias for local time translation.</span></span> <span data-ttu-id="bd657-118">Смещение — это разница между всеобщим скоординированным временем (UTC) и местным временем.</span><span class="sxs-lookup"><span data-stu-id="bd657-118">The bias is the difference between Coordinated Universal Time (UTC) and local time.</span></span> <span data-ttu-id="bd657-119">Все переводы между временем в формате UTC и местным временем основаны на следующей формуле: UTC = местное время — смещение.</span><span class="sxs-lookup"><span data-stu-id="bd657-119">All translations between UTC and local time are based on the following formula: UTC = local time - bias.</span></span> <span data-ttu-id="bd657-120">Это свойство обязательно.</span><span class="sxs-lookup"><span data-stu-id="bd657-120">This property is required.</span></span>

</dd> <dt>

<span data-ttu-id="bd657-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="bd657-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd657-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-124">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="bd657-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bd657-125">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="bd657-125">Short textual description of the current object.</span></span>

<span data-ttu-id="bd657-126">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bd657-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd657-127">**дайлигхтбиас**</span><span class="sxs-lookup"><span data-stu-id="bd657-127">**DaylightBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-128">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="bd657-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-130">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтбиас"), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="bd657-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-131">Значение смещения, которое будет использоваться при переводе на летнее время.</span><span class="sxs-lookup"><span data-stu-id="bd657-131">Bias value to be used during local time translations that occur during daylight saving time.</span></span> <span data-ttu-id="bd657-132">Это свойство пропускается, если не указано значение свойства **дайлигхтдай** .</span><span class="sxs-lookup"><span data-stu-id="bd657-132">This property is ignored if a value for the **DaylightDay** property is not supplied.</span></span> <span data-ttu-id="bd657-133">Значение этого свойства добавляется к свойству " **смещение** " для формирования смещения, используемого во время летнего времени.</span><span class="sxs-lookup"><span data-stu-id="bd657-133">The value of this property is added to the **Bias** property to form the bias used during daylight time.</span></span> <span data-ttu-id="bd657-134">В большинстве часовых поясов значение этого свойства равно-60.</span><span class="sxs-lookup"><span data-stu-id="bd657-134">In most time zones, the value of this property is -60.</span></span>

</dd> <dt>

<span data-ttu-id="bd657-135">**дайлигхтдай**</span><span class="sxs-lookup"><span data-stu-id="bd657-135">**DaylightDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-136">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-136">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-138">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вдай")</span><span class="sxs-lookup"><span data-stu-id="bd657-138">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-139">**Дайлигхтдайофвик** **дайлигхтмонс** , когда в этой операционной системе происходит переход со зимнего времени на летнее время.</span><span class="sxs-lookup"><span data-stu-id="bd657-139">**DaylightDayOfWeek** of the **DaylightMonth** when the transition from standard time to daylight saving time occurs on this operating system.</span></span>

<span data-ttu-id="bd657-140">Пример. Если день перехода (**дайлигхтдайофвик**) происходит в воскресенье, значение "1" обозначает первое воскресенье **дайлигхтмонс**, "2" — второе воскресенье и т. д.</span><span class="sxs-lookup"><span data-stu-id="bd657-140">Example: If the transition day (**DaylightDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **DaylightMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="bd657-141">Значение «5» обозначает последний **дайлигхтдайофвик** в месяце.</span><span class="sxs-lookup"><span data-stu-id="bd657-141">The value "5" indicates the last **DaylightDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="bd657-142">**дайлигхтдайофвик**</span><span class="sxs-lookup"><span data-stu-id="bd657-142">**DaylightDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-143">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bd657-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-145">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вдайофвик")</span><span class="sxs-lookup"><span data-stu-id="bd657-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-146">День недели, когда переход со зимнего времени на летнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-146">Day of the week when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="bd657-147">**Воскресенье** (0)</span><span class="sxs-lookup"><span data-stu-id="bd657-147">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="bd657-148">**Понедельник** (1)</span><span class="sxs-lookup"><span data-stu-id="bd657-148">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="bd657-149">**Вторник** (2)</span><span class="sxs-lookup"><span data-stu-id="bd657-149">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="bd657-150">**Среда** (3)</span><span class="sxs-lookup"><span data-stu-id="bd657-150">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="bd657-151">**Четверг** (4)</span><span class="sxs-lookup"><span data-stu-id="bd657-151">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="bd657-152">**Пятница** (5)</span><span class="sxs-lookup"><span data-stu-id="bd657-152">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="bd657-153">**Суббота** (6)</span><span class="sxs-lookup"><span data-stu-id="bd657-153">**Saturday** (6)</span></span>


<span data-ttu-id="bd657-154"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bd657-154"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="bd657-155">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="bd657-155">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="bd657-156">**дайлигхсаур**</span><span class="sxs-lookup"><span data-stu-id="bd657-156">**DaylightHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-159">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вхаур")</span><span class="sxs-lookup"><span data-stu-id="bd657-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-160">Час дня, когда переход со зимнего времени на летнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-160">Hour of the day when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-161">Пример: 2</span><span class="sxs-lookup"><span data-stu-id="bd657-161">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="bd657-162">**дайлигхтмиллисеконд**</span><span class="sxs-lookup"><span data-stu-id="bd657-162">**DaylightMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-163">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-165">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вмиллисекондс")</span><span class="sxs-lookup"><span data-stu-id="bd657-165">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-166">Миллисекунда **дайлигхтсеконд** , когда переход со зимнего времени на летнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-166">Millisecond of the **DaylightSecond** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bd657-167">**дайлигхтминуте**</span><span class="sxs-lookup"><span data-stu-id="bd657-167">**DaylightMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-170">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вминуте")</span><span class="sxs-lookup"><span data-stu-id="bd657-170">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-171">Минута **дайлигхсаур** , когда переход со зимнего времени на летнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-171">Minute of the **DaylightHour** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-172">Пример: 59</span><span class="sxs-lookup"><span data-stu-id="bd657-172">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="bd657-173">**дайлигхтмонс**</span><span class="sxs-lookup"><span data-stu-id="bd657-173">**DaylightMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-174">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-174">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-176">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| вмонс")</span><span class="sxs-lookup"><span data-stu-id="bd657-176">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-177">Месяц, когда переход со зимнего времени на летнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-177">Month when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="bd657-178">**Январь** (1)</span><span class="sxs-lookup"><span data-stu-id="bd657-178">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="bd657-179">**Февраль** (2)</span><span class="sxs-lookup"><span data-stu-id="bd657-179">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="bd657-180">**Март** (3)</span><span class="sxs-lookup"><span data-stu-id="bd657-180">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="bd657-181">**Апрель** (4)</span><span class="sxs-lookup"><span data-stu-id="bd657-181">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="bd657-182">**Май** (5)</span><span class="sxs-lookup"><span data-stu-id="bd657-182">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="bd657-183">**Июнь** (6)</span><span class="sxs-lookup"><span data-stu-id="bd657-183">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="bd657-184">**Июль** (7)</span><span class="sxs-lookup"><span data-stu-id="bd657-184">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="bd657-185">**Август** (8)</span><span class="sxs-lookup"><span data-stu-id="bd657-185">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="bd657-186">**Сентябрь** (9)</span><span class="sxs-lookup"><span data-stu-id="bd657-186">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="bd657-187">**Октябрь** (10)</span><span class="sxs-lookup"><span data-stu-id="bd657-187">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="bd657-188">**Ноябрь** (11)</span><span class="sxs-lookup"><span data-stu-id="bd657-188">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="bd657-189">**Декабрь** (12)</span><span class="sxs-lookup"><span data-stu-id="bd657-189">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd657-190">**дайлигхтнаме**</span><span class="sxs-lookup"><span data-stu-id="bd657-190">**DaylightName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-191">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd657-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-193">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтнаме")</span><span class="sxs-lookup"><span data-stu-id="bd657-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightName")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-194">Часовой пояс, который будет представлен, если действует летнее время.</span><span class="sxs-lookup"><span data-stu-id="bd657-194">Time zone being represented when daylight saving time is in effect.</span></span>

<span data-ttu-id="bd657-195">Пример: "EDT" (восточное время (лето))</span><span class="sxs-lookup"><span data-stu-id="bd657-195">Example: "EDT" (Eastern Daylight Time)</span></span>

</dd> <dt>

<span data-ttu-id="bd657-196">**дайлигхтсеконд**</span><span class="sxs-lookup"><span data-stu-id="bd657-196">**DaylightSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-197">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-199">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| всеконд")</span><span class="sxs-lookup"><span data-stu-id="bd657-199">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-200">Второй из **дайлигхтминуте** , когда переход со зимнего времени на летнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-200">Second of the **DaylightMinute** when the transition from standard time to daylight saving time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-201">Пример: 59</span><span class="sxs-lookup"><span data-stu-id="bd657-201">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="bd657-202">**дайлигхтеар**</span><span class="sxs-lookup"><span data-stu-id="bd657-202">**DaylightYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-203">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-204">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-205">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| дайлигхтдате \| ВЕАР")</span><span class="sxs-lookup"><span data-stu-id="bd657-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|DaylightDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-206">Год, когда действует летнее время.</span><span class="sxs-lookup"><span data-stu-id="bd657-206">Year when daylight saving time is in effect.</span></span> <span data-ttu-id="bd657-207">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bd657-207">This property is not required.</span></span>

<span data-ttu-id="bd657-208">Пример: 1997</span><span class="sxs-lookup"><span data-stu-id="bd657-208">Example: 1997</span></span>

</dd> <dt>

<span data-ttu-id="bd657-209">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd657-209">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd657-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd657-212">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="bd657-212">Textual description of the current object.</span></span>

<span data-ttu-id="bd657-213">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bd657-213">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd657-214">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="bd657-214">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-215">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd657-215">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-216">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-217">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="bd657-217">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bd657-218">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="bd657-218">Identifier by which the current object is known.</span></span>

<span data-ttu-id="bd657-219">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bd657-219">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd657-220">**стандардбиас**</span><span class="sxs-lookup"><span data-stu-id="bd657-220">**StandardBias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-221">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-223">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандардбиас"), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="bd657-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardBias"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-224">Значение смещения, используемое, если переход на летнее время не действует.</span><span class="sxs-lookup"><span data-stu-id="bd657-224">Bias value to use when daylight saving time is not in effect.</span></span> <span data-ttu-id="bd657-225">Это свойство игнорируется, если не указано значение для **стандарддай** .</span><span class="sxs-lookup"><span data-stu-id="bd657-225">This property is ignored if a value for **StandardDay** is not supplied.</span></span> <span data-ttu-id="bd657-226">Значение этого свойства добавляется к свойству " **смещение** " для формирования смещения во время стандартного времени.</span><span class="sxs-lookup"><span data-stu-id="bd657-226">The value of this property is added to the **Bias** property to form the bias during standard time.</span></span>

<span data-ttu-id="bd657-227">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="bd657-227">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="bd657-228">**стандарддай**</span><span class="sxs-lookup"><span data-stu-id="bd657-228">**StandardDay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-229">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-231">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вдай")</span><span class="sxs-lookup"><span data-stu-id="bd657-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDay")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-232">**Стандарддайофвик** **стандардмонс** , когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-232">**StandardDayOfWeek** of the **StandardMonth** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-233">Если день перехода (**стандарддайофвик**) происходит в воскресенье, значение "1" обозначает первое воскресенье **стандардмонс**, "2" — второе воскресенье и т. д.</span><span class="sxs-lookup"><span data-stu-id="bd657-233">If the transition day (**StandardDayOfWeek**) occurs on a Sunday, then the value "1" indicates the first Sunday of the **StandardMonth**, "2" indicates the second Sunday, and so on.</span></span> <span data-ttu-id="bd657-234">Значение «5» обозначает последний **стандарддайофвик** в месяце.</span><span class="sxs-lookup"><span data-stu-id="bd657-234">The value "5" indicates the last **StandardDayOfWeek** in the month.</span></span>

</dd> <dt>

<span data-ttu-id="bd657-235">**стандарддайофвик**</span><span class="sxs-lookup"><span data-stu-id="bd657-235">**StandardDayOfWeek**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-236">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bd657-236">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-238">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вдайофвик")</span><span class="sxs-lookup"><span data-stu-id="bd657-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wDayOfWeek")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-239">День недели, когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-239">Day of the week when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

<span data-ttu-id="bd657-240">**Воскресенье** (0)</span><span class="sxs-lookup"><span data-stu-id="bd657-240">**Sunday** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

<span data-ttu-id="bd657-241">**Понедельник** (1)</span><span class="sxs-lookup"><span data-stu-id="bd657-241">**Monday** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

<span data-ttu-id="bd657-242">**Вторник** (2)</span><span class="sxs-lookup"><span data-stu-id="bd657-242">**Tuesday** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

<span data-ttu-id="bd657-243">**Среда** (3)</span><span class="sxs-lookup"><span data-stu-id="bd657-243">**Wednesday** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

<span data-ttu-id="bd657-244">**Четверг** (4)</span><span class="sxs-lookup"><span data-stu-id="bd657-244">**Thursday** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

<span data-ttu-id="bd657-245">**Пятница** (5)</span><span class="sxs-lookup"><span data-stu-id="bd657-245">**Friday** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

<span data-ttu-id="bd657-246">**Суббота** (6)</span><span class="sxs-lookup"><span data-stu-id="bd657-246">**Saturday** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd657-247">**стандардхаур**</span><span class="sxs-lookup"><span data-stu-id="bd657-247">**StandardHour**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-248">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-248">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-250">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вхаур")</span><span class="sxs-lookup"><span data-stu-id="bd657-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wHour")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-251">Час дня, когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-251">Hour of the day when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-252">Пример: 11</span><span class="sxs-lookup"><span data-stu-id="bd657-252">Example: 11</span></span>

</dd> <dt>

<span data-ttu-id="bd657-253">**стандардмиллисеконд**</span><span class="sxs-lookup"><span data-stu-id="bd657-253">**StandardMillisecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-254">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-256">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вмиллисекондс")</span><span class="sxs-lookup"><span data-stu-id="bd657-256">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMilliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-257">Миллисекунда **стандардсеконд** , когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-257">Millisecond of the **StandardSecond** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

</dd> <dt>

<span data-ttu-id="bd657-258">**стандардминуте**</span><span class="sxs-lookup"><span data-stu-id="bd657-258">**StandardMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-259">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-259">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-261">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вминуте")</span><span class="sxs-lookup"><span data-stu-id="bd657-261">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMinute")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-262">Минута **стандарддай** , когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-262">Minute of the **StandardDay** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-263">Пример: 59</span><span class="sxs-lookup"><span data-stu-id="bd657-263">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="bd657-264">**стандардмонс**</span><span class="sxs-lookup"><span data-stu-id="bd657-264">**StandardMonth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-265">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-265">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-267">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| вмонс")</span><span class="sxs-lookup"><span data-stu-id="bd657-267">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wMonth")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-268">Месяц, когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-268">Month when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

<span data-ttu-id="bd657-269">**Январь** (1)</span><span class="sxs-lookup"><span data-stu-id="bd657-269">**January** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

<span data-ttu-id="bd657-270">**Февраль** (2)</span><span class="sxs-lookup"><span data-stu-id="bd657-270">**February** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

<span data-ttu-id="bd657-271">**Март** (3)</span><span class="sxs-lookup"><span data-stu-id="bd657-271">**March** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

<span data-ttu-id="bd657-272">**Апрель** (4)</span><span class="sxs-lookup"><span data-stu-id="bd657-272">**April** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

<span data-ttu-id="bd657-273">**Май** (5)</span><span class="sxs-lookup"><span data-stu-id="bd657-273">**May** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

<span data-ttu-id="bd657-274">**Июнь** (6)</span><span class="sxs-lookup"><span data-stu-id="bd657-274">**June** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

<span data-ttu-id="bd657-275">**Июль** (7)</span><span class="sxs-lookup"><span data-stu-id="bd657-275">**July** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

<span data-ttu-id="bd657-276">**Август** (8)</span><span class="sxs-lookup"><span data-stu-id="bd657-276">**August** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

<span data-ttu-id="bd657-277">**Сентябрь** (9)</span><span class="sxs-lookup"><span data-stu-id="bd657-277">**September** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

<span data-ttu-id="bd657-278">**Октябрь** (10)</span><span class="sxs-lookup"><span data-stu-id="bd657-278">**October** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

<span data-ttu-id="bd657-279">**Ноябрь** (11)</span><span class="sxs-lookup"><span data-stu-id="bd657-279">**November** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

<span data-ttu-id="bd657-280">**Декабрь** (12)</span><span class="sxs-lookup"><span data-stu-id="bd657-280">**December** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd657-281">**StandardName**</span><span class="sxs-lookup"><span data-stu-id="bd657-281">**StandardName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-282">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bd657-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-284">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| StandardName")</span><span class="sxs-lookup"><span data-stu-id="bd657-284">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardName")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-285">Имя часового пояса, представленного в результате использования стандартного времени.</span><span class="sxs-lookup"><span data-stu-id="bd657-285">Name of the time zone being represented when standard time is in effect.</span></span>

<span data-ttu-id="bd657-286">Пример: "EST" (восточное стандартное время)</span><span class="sxs-lookup"><span data-stu-id="bd657-286">Example: "EST" (Eastern Standard Time)</span></span>

</dd> <dt>

<span data-ttu-id="bd657-287">**стандардсеконд**</span><span class="sxs-lookup"><span data-stu-id="bd657-287">**StandardSecond**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-288">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-288">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-290">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| всеконд")</span><span class="sxs-lookup"><span data-stu-id="bd657-290">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wSecond")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-291">Второй из **стандардминуте** , когда переход с летнего времени на зимнее время происходит в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bd657-291">Second of the **StandardMinute** when the transition from daylight saving time to standard time occurs on an operating system.</span></span>

<span data-ttu-id="bd657-292">Пример: 59</span><span class="sxs-lookup"><span data-stu-id="bd657-292">Example: 59</span></span>

</dd> <dt>

<span data-ttu-id="bd657-293">**стандардеар**</span><span class="sxs-lookup"><span data-stu-id="bd657-293">**StandardYear**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd657-294">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd657-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd657-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bd657-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd657-296">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры времени Win32API \| [**\_ \_ сведения о часовом поясе**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) \| стандарддате \| ВЕАР")</span><span class="sxs-lookup"><span data-stu-id="bd657-296">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information)\|StandardDate\|wYear")</span></span>
</dt> </dl>

<span data-ttu-id="bd657-297">Год, когда действует стандартное время.</span><span class="sxs-lookup"><span data-stu-id="bd657-297">Year when standard time is in effect.</span></span> <span data-ttu-id="bd657-298">Это свойство не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bd657-298">This property is not required.</span></span>

<span data-ttu-id="bd657-299">Пример: 1997</span><span class="sxs-lookup"><span data-stu-id="bd657-299">Example: 1997</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd657-300">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd657-300">Remarks</span></span>

<span data-ttu-id="bd657-301">Класс **\_ часового пояса Win32** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bd657-301">The **Win32\_TimeZone** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="bd657-302">При написании запросов WMI нельзя использовать стандартные форматы даты и времени, например 10/18/2002.</span><span class="sxs-lookup"><span data-stu-id="bd657-302">You cannot use standard date-time formats - such as 10/18/2002 - when writing WMI queries.</span></span> <span data-ttu-id="bd657-303">Вместо этого необходимо преобразовать все даты, используемые в запросах, в формат UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-303">Instead, you need to convert any dates used in your queries to UTC format.</span></span> <span data-ttu-id="bd657-304">Для этого требуется два шага: 1) необходимо определить смещение (разница в минутах) между часовым поясом и временем по Гринвичу, а 2) необходимо преобразовать 10/18/2002 в значение времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-304">This requires two steps: 1) You must determine the offset (difference in minutes) between your time zone and Greenwich Mean Time, and 2) you must convert 10/18/2002 to a UTC value.</span></span>

<span data-ttu-id="bd657-305">Определение смещения относительно среднего времени по Гринвичу</span><span class="sxs-lookup"><span data-stu-id="bd657-305">Determining the Offset from Greenwich Mean Time</span></span>

<span data-ttu-id="bd657-306">Следует признать, что инструментарий WMI затрудняет работу с датами и временем. к счастью, Инструментарий WMI, как минимум, упрощает определение смещения между часовым поясом и временем по Гринвичу.</span><span class="sxs-lookup"><span data-stu-id="bd657-306">Admittedly, WMI makes it difficult to work with dates and times; fortunately, WMI at least makes it easy to determine the offset between your time zone and Greenwich Mean Time.</span></span> <span data-ttu-id="bd657-307">Часовой пояс Win32 класса WMI \_ включает сдвиг свойства, который возвращает смещение GMT.</span><span class="sxs-lookup"><span data-stu-id="bd657-307">The WMI class Win32\_TimeZone includes a property - Bias - that returns the GMT offset.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 Wscript.Echo "Offset: "& objTimeZone.Bias
Next
```



<span data-ttu-id="bd657-308">Преобразование даты в значение в формате UTC</span><span class="sxs-lookup"><span data-stu-id="bd657-308">Converting a Date to a UTC Value</span></span>

<span data-ttu-id="bd657-309">После определения смещения GMT необходимо преобразовать стандартную дату, например 10/18/2002, в дату в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-309">After you determine the GMT offset, you must then convert a standard date such as 10/18/2002 to a UTC date.</span></span> <span data-ttu-id="bd657-310">Чтобы преобразовать стандартную дату в дату в формате UTC, можно использовать функции даты VBScript, такие как год, месяц и день, чтобы изолировать отдельные компоненты, которые составляют дату в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-310">To convert a standard date to a UTC date, you can use VBScript date functions such as Year, Month, and Day to isolate the individual components that make up a UTC date.</span></span> <span data-ttu-id="bd657-311">После создания отдельных значений для этих компонентов их можно объединить так же, как и любые другие строковые значения.</span><span class="sxs-lookup"><span data-stu-id="bd657-311">After you have individual values for these components, you can concatenate them in the same manner as you would any other string value.</span></span> <span data-ttu-id="bd657-312">Даты в формате UTC обрабатываются как строки, так как смещение GMT должно быть добавлено к концу.</span><span class="sxs-lookup"><span data-stu-id="bd657-312">UTC dates are treated as strings because the GMT offset must be appended to the end.</span></span> <span data-ttu-id="bd657-313">Если дата показана в виде числа, это значение:</span><span class="sxs-lookup"><span data-stu-id="bd657-313">If the date were seen as a number, this value:</span></span>

`20011018113047.000000-480`

<span data-ttu-id="bd657-314">Будет ошибочно рассматриваться как математическое уравнение (для ясности добавлены круглые скобки):</span><span class="sxs-lookup"><span data-stu-id="bd657-314">Would be erroneously treated as a mathematical equation (parentheses added for clarity):</span></span>

`(20011018113047.000000) - (480)`

<span data-ttu-id="bd657-315">Например, в дате 10/18/2002 отдельные компоненты:</span><span class="sxs-lookup"><span data-stu-id="bd657-315">For example, in the date 10/18/2002, the individual components are:</span></span>

-   <span data-ttu-id="bd657-316">Год: 2002</span><span class="sxs-lookup"><span data-stu-id="bd657-316">Year: 2002</span></span>
-   <span data-ttu-id="bd657-317">Месяц: 10</span><span class="sxs-lookup"><span data-stu-id="bd657-317">Month: 10</span></span>
-   <span data-ttu-id="bd657-318">День: 18</span><span class="sxs-lookup"><span data-stu-id="bd657-318">Day: 18</span></span>

<span data-ttu-id="bd657-319">Скрипту потребуется объединить эти три значения, строку "113047,000000" (представляющую время, включая миллисекунды) и смещение GMT для получения даты в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-319">The script would need to combine these three values, the string "113047.000000" (representing the time, including milliseconds), and the GMT offset to derive a UTC date.</span></span> <span data-ttu-id="bd657-320">Например, для ясности добавлены скобки.</span><span class="sxs-lookup"><span data-stu-id="bd657-320">For example, (parentheses again added for clarity):</span></span>

`(2002) & (10) & (18) & (113047.000000) & (-480)`

> [!Note]  
> <span data-ttu-id="bd657-321">Для преобразования временной части даты в формате UTC можно использовать функции VBScript час, минуту и секунду.</span><span class="sxs-lookup"><span data-stu-id="bd657-321">You can use the VBScript functions Hour, Minute, and Second to convert the time portion of a UTC date.</span></span> <span data-ttu-id="bd657-322">Таким образом, такое время, как 11:30:47 утра</span><span class="sxs-lookup"><span data-stu-id="bd657-322">Thus, a time such as 11:30:47 A.M.</span></span> <span data-ttu-id="bd657-323">будет преобразовано в 113047.</span><span class="sxs-lookup"><span data-stu-id="bd657-323">would be converted to 113047.</span></span>

 

<span data-ttu-id="bd657-324">Существует один усложненный фактор.</span><span class="sxs-lookup"><span data-stu-id="bd657-324">There is one complicating factor.</span></span> <span data-ttu-id="bd657-325">Месяц должен занимать в строке позиции 5 и 6; день должен занимать 7 и 8 единиц.</span><span class="sxs-lookup"><span data-stu-id="bd657-325">The month must take up positions 5 and 6 in the string; the day must take up positions 7 and 8.</span></span> <span data-ttu-id="bd657-326">Это не проблема с 10 и 18-го дня.</span><span class="sxs-lookup"><span data-stu-id="bd657-326">This is no problem with month 10 and day 18.</span></span> <span data-ttu-id="bd657-327">Но как получить 5 июля (месяц 7, день 5), чтобы заполнить позиции необходимых условий?</span><span class="sxs-lookup"><span data-stu-id="bd657-327">But how do you get July 5 (month 7, day 5) to fill up the requisite positions?</span></span> <span data-ttu-id="bd657-328">Ответ заключается в том, чтобы добавить к каждому значению ноль в начале, что приведет к изменению 7 на 07 и 5 на 05.</span><span class="sxs-lookup"><span data-stu-id="bd657-328">The answer is to add a leading zero to each value, thus changing the 7 to 07 and the 5 to 05.</span></span>

<span data-ttu-id="bd657-329">Для этого используйте функцию "len" языка VBScript, чтобы проверить длину (число символов) в месяце и день.</span><span class="sxs-lookup"><span data-stu-id="bd657-329">To do this, use the VBScript Len function to check the length (number of characters) in the month and the day.</span></span> <span data-ttu-id="bd657-330">Если длина равна 1 (это означает, что имеется только один символ), добавьте начальный нуль.</span><span class="sxs-lookup"><span data-stu-id="bd657-330">If the length is 1 (meaning that there is just one character), add a leading zero.</span></span> <span data-ttu-id="bd657-331">Следовательно</span><span class="sxs-lookup"><span data-stu-id="bd657-331">Thus:</span></span>


```VB
If Len(dtmMonth) = 1 Then
    dtmMonth = "0" & dtmMonth
End If
```



## <a name="examples"></a><span data-ttu-id="bd657-332">Примеры</span><span class="sxs-lookup"><span data-stu-id="bd657-332">Examples</span></span>

<span data-ttu-id="bd657-333">В следующем примере на языке VBScript текущая дата преобразуется в дату в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-333">The following VBScript example converts the current date to a UTC date.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = Date
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)
```



<span data-ttu-id="bd657-334">Следующий сценарий VBScript сампледетерминес смещение GMT, а затем преобразует указанную текущую дату (в данном случае 10/18/2002) в формат даты и времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="bd657-334">The following VBScript sampledetermines the GMT offset, and then converts a specified current date (in this case, 10/18/2002) to UTC date-time format.</span></span> <span data-ttu-id="bd657-335">После преобразования даты это значение используется для поиска компьютера и возвращает список всех папок, созданных после 10/18/2002.</span><span class="sxs-lookup"><span data-stu-id="bd657-335">After the date has been converted, that value is used to search a computer and returns a list of all the folders that were created after 10/18/2002.</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colTimeZone = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_TimeZone")
For Each objTimeZone in colTimeZone
 strBias = objTimeZone.Bias
Next

dtmCurrentDate = "10/18/2002"
dtmTargetDate = Year(dtmCurrentDate)

dtmMonth = Month(dtmCurrentDate)
If Len(dtmMonth) = 1 Then
 dtmMonth = "0" & dtmMonth
End If

dtmTargetDate = dtmTargetDate & dtmMonth

dtmDay = Day(dtmCurrentDate)
If Len(dtmDay) = 1 Then
 dtmDay = "0" & dtmDay
End If

dtmTargetDate = dtmTargetDate & dtmDay & "000000.000000"
dtmTargetDate = dtmTargetDate & Cstr(strBias)

Set colFolders = objSWbemServices.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE CreationDate < '" & _
 dtmtargetDate & "'")
For Each objFolder in colFolders
 Wscript.Echo objFolder.Name
Next
```



<span data-ttu-id="bd657-336">В следующем примере кода VBScript отображаются параметры для \_ экземпляров часового пояса Win32.</span><span class="sxs-lookup"><span data-stu-id="bd657-336">The following VBScript code example displays the settings for Win32\_TimeZone instances.</span></span>


```VB
Dim arDayOrWeek(7)
arDayOrWeek(0) = "Sunday"
arDayOrWeek(1) = "Monday"
arDayOrWeek(2) = "Tuesday"
arDayOrWeek(3) = "Wednesday"
arDayOrWeek(4) = "Thursday"
arDayOrWeek(5) = "Friday"
arDayOrWeek(6) = "Saturday"

Dim arMonth(13)
arMonth(1) = "January"
arMonth(2) = "Feburary"
arMonth(3) = "March"
arMonth(4) = "April"
arMonth(5) = "May"
arMonth(6) = "June"
arMonth(7) = "July"
arMonth(8) = "August"
arMonth(9) = "September"
arMonth(10) = "October"
arMonth(11) = "November"
arMonth(12) = "December"

strComputer = "."
wmiQuery = "Select * from Win32_TimeZone"
Set objWMIService = GetObject("winmgmts:\\" & _
    strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery(wmiQuery)

For Each objItem in colItems
    WScript.Echo "Day of Week setting is: " _
        & objItem.dayLightDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.DaylightHour 
    WScript.Echo "Month: " & objItem.DaylightMonth _
        & " which is: " & arMonth(objItem.DaylightMonth )
    WScript.Echo "Description: " & objItem.DaylightName 
    WScript.Echo "The transition from DLS to Standard occurs: " 
    WScript.Echo "Day of Week setting is: " _
        & objItem.standardDayOfWeek _
        & " which is: " & arDayOrWeek(objItem.DaylightDayOfWeek)
    WScript.Echo "Hour: " & objItem.StandardHour 
    WScript.Echo "Month: " & objItem.StandardMonth _ 
        & " which is: " & arMonth(objItem.StandardMonth )
    WScript.Echo "Description: " & objItem.StandardName 
Next

```



## <a name="requirements"></a><span data-ttu-id="bd657-337">Требования</span><span class="sxs-lookup"><span data-stu-id="bd657-337">Requirements</span></span>



| <span data-ttu-id="bd657-338">Требование</span><span class="sxs-lookup"><span data-stu-id="bd657-338">Requirement</span></span> | <span data-ttu-id="bd657-339">Значение</span><span class="sxs-lookup"><span data-stu-id="bd657-339">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd657-340">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd657-340">Minimum supported client</span></span><br/> | <span data-ttu-id="bd657-341">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd657-341">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd657-342">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd657-342">Minimum supported server</span></span><br/> | <span data-ttu-id="bd657-343">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd657-343">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd657-344">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bd657-344">Namespace</span></span><br/>                | <span data-ttu-id="bd657-345">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bd657-345">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd657-346">MOF</span><span class="sxs-lookup"><span data-stu-id="bd657-346">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd657-347"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd657-347"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd657-348">DLL</span><span class="sxs-lookup"><span data-stu-id="bd657-348">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd657-349"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd657-349"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd657-350">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd657-350">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd657-351">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="bd657-351">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="bd657-352">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="bd657-352">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="bd657-353">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="bd657-353">**SWbemDateTime**</span></span>](../wmisdk/swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="bd657-354">Формат даты и времени</span><span class="sxs-lookup"><span data-stu-id="bd657-354">Date and Time Format</span></span>](../wmisdk/date-and-time-format.md)
</dt> <dt>

[<span data-ttu-id="bd657-355">Задачи WMI: даты и время</span><span class="sxs-lookup"><span data-stu-id="bd657-355">WMI Tasks: Dates and Times</span></span>](../wmisdk/wmi-tasks--dates-and-times.md)
</dt> </dl>

 

 
