---
description: Квалификаторы свойств указывают сведения о счетчике производительности, с которым сопоставляется свойство.
ms.assetid: f1761f71-af4e-4b89-aba7-b7f294c30ffc
ms.tgt_platform: multiple
title: Квалификаторы свойств для классов счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e060d072c34d248f9faf634aec7710f5638721b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272436"
---
# <a name="property-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="6bab3-103">Квалификаторы свойств для классов счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-103">Property Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="6bab3-104">Квалификаторы свойств указывают сведения о счетчике производительности, с которым сопоставляется свойство.</span><span class="sxs-lookup"><span data-stu-id="6bab3-104">Property qualifiers specify information about the performance counter to which the property maps.</span></span>

-   [<span data-ttu-id="6bab3-105">Квалификаторы свойств для необработанных и отформатированных классов производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-105">Property Qualifiers for Raw and Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="6bab3-106">Квалификаторы свойств для необработанных классов производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-106">Property Qualifiers for Raw Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="6bab3-107">Квалификаторы свойств для отформатированных классов производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-107">Property Qualifiers for Formatted Performance Classes</span></span>](#property-qualifiers-for-raw-and-formatted-performance-classes)
-   [<span data-ttu-id="6bab3-108">Как интерпретировать квалификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="6bab3-108">How to Interpret Property Qualifiers</span></span>](#how-to-interpret-property-qualifiers)
-   [<span data-ttu-id="6bab3-109">См. также</span><span class="sxs-lookup"><span data-stu-id="6bab3-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="6bab3-110">Счетчик производительности является частью объекта производительности, представленного в счетчике производительности [класса счетчика производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI. квалификаторы, относящиеся к конкретному числу, автоматически присоединяются поставщиком вбемперфкласс к классам и свойствам [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) в корневом \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="6bab3-110">The performance counter is part of a performance object represented by a WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) Performance counter–specific qualifiers are automatically attached by the WbemPerfClass provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="6bab3-111">Эти сведения применяются ко всем экземплярам класса Performance.</span><span class="sxs-lookup"><span data-stu-id="6bab3-111">This information applies to all instances of the performance class.</span></span> <span data-ttu-id="6bab3-112">Некоторые квалификаторы с **логическими** значениями, которые всегда имеют значение false, могут отсутствовать в определенных классах.</span><span class="sxs-lookup"><span data-stu-id="6bab3-112">Some qualifiers with **Boolean** values that are always false may not be present on specific classes.</span></span>

## <a name="property-qualifiers-for-raw-and-formatted-performance-classes"></a><span data-ttu-id="6bab3-113">Квалификаторы свойств для необработанных и отформатированных классов производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-113">Property Qualifiers for Raw and Formatted Performance Classes</span></span>

<span data-ttu-id="6bab3-114">В следующем списке перечислены квалификаторы, применяемые к свойствам в классах, которые являются производными от [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) или [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="6bab3-114">The following list lists qualifiers that apply to properties in classes that are derived either from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) or [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="6bab3-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6bab3-115"><span id="CounterType"></span><span id="countertype"></span><span id="COUNTERTYPE"></span>[**CounterType**](countertype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-116">**sint32**</span><span class="sxs-lookup"><span data-stu-id="6bab3-116">**sint32**</span></span>

<span data-ttu-id="6bab3-117">Целочисленное значение в перечислении типов счетчиков, определенное в Винперф. h или PerfLib. h.</span><span class="sxs-lookup"><span data-stu-id="6bab3-117">Integer value in the counter type enumeration, as defined in Winperf.h or Perflib.h.</span></span> <span data-ttu-id="6bab3-118">Квалификатор [**CounterType**](countertype-qualifier.md)указывает формулу или алгоритм, используемый для вычисления значения, отображаемого в системном мониторе для счетчика, который представляет свойство.</span><span class="sxs-lookup"><span data-stu-id="6bab3-118">The [**CounterType**](countertype-qualifier.md)qualifier indicates the formula or algorithm used to calculate the value shown in System Monitor for the counter which the property represents.</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6bab3-119"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-120">**string**</span><span class="sxs-lookup"><span data-stu-id="6bab3-120">**string**</span></span>

<span data-ttu-id="6bab3-121">Имя счетчика производительности, как указано в модуле поддержки данных производительности (PDH).</span><span class="sxs-lookup"><span data-stu-id="6bab3-121">The performance Counter name, as specified by Performance Data Helper (PDH).</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**хелпиндекс**</span><span class="sxs-lookup"><span data-stu-id="6bab3-122"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="6bab3-123">**sint32**</span></span>

<span data-ttu-id="6bab3-124">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6bab3-124">Not used.</span></span> <span data-ttu-id="6bab3-125">Всегда содержит 0.</span><span class="sxs-lookup"><span data-stu-id="6bab3-125">Always contains 0.</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**перфиндекс**</span><span class="sxs-lookup"><span data-stu-id="6bab3-126"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-127">**sint32**</span><span class="sxs-lookup"><span data-stu-id="6bab3-127">**sint32**</span></span>

<span data-ttu-id="6bab3-128">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6bab3-128">Not used.</span></span> <span data-ttu-id="6bab3-129">Всегда содержит 0.</span><span class="sxs-lookup"><span data-stu-id="6bab3-129">Always contains 0.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-raw-performance-classes"></a><span data-ttu-id="6bab3-130">Квалификаторы свойств для необработанных классов производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-130">Property Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="6bab3-131">В следующем списке перечислены квалификаторы, применяемые ко всем свойствам классов, которые являются производными от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="6bab3-131">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="6bab3-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**перфдефаулт**</span><span class="sxs-lookup"><span data-stu-id="6bab3-132"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-133">**boolean**</span><span class="sxs-lookup"><span data-stu-id="6bab3-133">**boolean**</span></span>

<span data-ttu-id="6bab3-134">Указывает, является ли это свойство счетчиком по умолчанию для использования в списках.</span><span class="sxs-lookup"><span data-stu-id="6bab3-134">Indicates whether this property is the default counter to use in list boxes.</span></span> <span data-ttu-id="6bab3-135">По умолчанию этот квалификатор **имеет значение false** для счетчиков производительности версии 6,0, так как они не предоставляют для них данные.</span><span class="sxs-lookup"><span data-stu-id="6bab3-135">This qualifier defaults to **False** for Performance Counters Version 6.0 because they do not supply data for it.</span></span> <span data-ttu-id="6bab3-136">Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="6bab3-136">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**дефаултскале**</span><span class="sxs-lookup"><span data-stu-id="6bab3-137"><span id="DefaultScale"></span><span id="defaultscale"></span><span id="DEFAULTSCALE"></span>**DefaultScale**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-138">**sint32**</span><span class="sxs-lookup"><span data-stu-id="6bab3-138">**sint32**</span></span>

<span data-ttu-id="6bab3-139">Мощность 10, используемая для вывода счетчика.</span><span class="sxs-lookup"><span data-stu-id="6bab3-139">Power of 10 to use for display of the counter.</span></span> <span data-ttu-id="6bab3-140">Для нуля оценочный максимум равен 10 ^ 0 или 1.</span><span class="sxs-lookup"><span data-stu-id="6bab3-140">For zero, the estimated maximum is 10^0, or 1.</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**перфдетаил**](perfdetail-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="6bab3-141"><span id="PerfDetail"></span><span id="perfdetail"></span><span id="PERFDETAIL"></span>[**PerfDetail**](perfdetail-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="6bab3-142">**sint32**</span></span>

<span data-ttu-id="6bab3-143">Уровень знаний аудитории.</span><span class="sxs-lookup"><span data-stu-id="6bab3-143">Audience level of knowledge.</span></span> <span data-ttu-id="6bab3-144">Не используется.</span><span class="sxs-lookup"><span data-stu-id="6bab3-144">Not used.</span></span> <span data-ttu-id="6bab3-145">Значение всегда равно 100.</span><span class="sxs-lookup"><span data-stu-id="6bab3-145">The value is always 100.</span></span>

</dd> </dl>

## <a name="property-qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="6bab3-146">Квалификаторы свойств для отформатированных классов производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-146">Property Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="6bab3-147">В следующем списке перечислены квалификаторы, применяемые ко всем свойствам классов, которые являются производными от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="6bab3-147">The following list lists qualifiers that apply to all properties of classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="6bab3-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**кукингтипе**</span><span class="sxs-lookup"><span data-stu-id="6bab3-148"><span id="CookingType"></span><span id="cookingtype"></span><span id="COOKINGTYPE"></span>**CookingType**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-149">**string**</span><span class="sxs-lookup"><span data-stu-id="6bab3-149">**string**</span></span>

<span data-ttu-id="6bab3-150">Тип формулы, используемый для получения результата.</span><span class="sxs-lookup"><span data-stu-id="6bab3-150">Formula type used to produce the result.</span></span> <span data-ttu-id="6bab3-151">Каждый тип счетчика использует другие квалификаторы свойств для вычисления результата, отображаемого в качестве значения текущего свойства.</span><span class="sxs-lookup"><span data-stu-id="6bab3-151">Each counter type uses the other property qualifiers to calculate the result shown as the value of the current property.</span></span> <span data-ttu-id="6bab3-152">Квалификаторы **Counter**, **перфтиместамп** и **перфтимефрек** сопоставляются со свойствами в необработанном классе, которые предоставляют данные.</span><span class="sxs-lookup"><span data-stu-id="6bab3-152">The **Counter**, **PerfTimeStamp**, and **PerfTimeFreq** qualifiers map to properties in a raw class which supply the data.</span></span>

<span data-ttu-id="6bab3-153">Дополнительные сведения см. в разделе [квалификатор CounterType](countertype-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="6bab3-153">For more information, see [CounterType Qualifier](countertype-qualifier.md).</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Подписан**</span><span class="sxs-lookup"><span data-stu-id="6bab3-154"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-155">**string**</span><span class="sxs-lookup"><span data-stu-id="6bab3-155">**string**</span></span>

<span data-ttu-id="6bab3-156">Имя обязательного свойства в соответствующем необработанном классе для использования в качестве значения счетчика в формуле приготовления.</span><span class="sxs-lookup"><span data-stu-id="6bab3-156">Name of a required property in the corresponding raw class to use as the counter value in the cooking formula.</span></span> <span data-ttu-id="6bab3-157">Значение должно быть именем свойства источника данных в соответствующем необработанном классе.</span><span class="sxs-lookup"><span data-stu-id="6bab3-157">The value must be the property name of the data source property in the corresponding raw class.</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**перфтиместамп**</span><span class="sxs-lookup"><span data-stu-id="6bab3-158"><span id="PerfTimeStamp"></span><span id="perftimestamp"></span><span id="PERFTIMESTAMP"></span>**PerfTimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-159">**string**</span><span class="sxs-lookup"><span data-stu-id="6bab3-159">**string**</span></span>

<span data-ttu-id="6bab3-160">Имя свойства в необработанном классе для использования в качестве частоты в формуле приготовления.</span><span class="sxs-lookup"><span data-stu-id="6bab3-160">Name of a property in a raw class to use as a frequency in the cooking formula.</span></span> <span data-ttu-id="6bab3-161">Если этот квалификатор отсутствует для свойства, будет использоваться соответствующее значение по умолчанию на уровне класса.</span><span class="sxs-lookup"><span data-stu-id="6bab3-161">The appropriate default value at the class level will be used if this qualifier is not present for the property.</span></span> <span data-ttu-id="6bab3-162">Частота представляет такты в секунду штампа времени.</span><span class="sxs-lookup"><span data-stu-id="6bab3-162">The frequency represents the ticks per second of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="6bab3-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**перфтимефрек**</span><span class="sxs-lookup"><span data-stu-id="6bab3-163"><span id="PerfTimeFreq"></span><span id="perftimefreq"></span><span id="PERFTIMEFREQ"></span>**PerfTimeFreq**</span></span>
</dt> <dd>

<span data-ttu-id="6bab3-164">**string**</span><span class="sxs-lookup"><span data-stu-id="6bab3-164">**string**</span></span>

<span data-ttu-id="6bab3-165">Имя свойства в необработанном классе для использования в качестве метки времени в формуле приготовления.</span><span class="sxs-lookup"><span data-stu-id="6bab3-165">Name of a property in a raw class to use as a timestamp in the cooking formula.</span></span> <span data-ttu-id="6bab3-166">Если этот квалификатор отсутствует для свойства, используется соответствующее значение по умолчанию на уровне класса.</span><span class="sxs-lookup"><span data-stu-id="6bab3-166">The appropriate default value at the class level is used if this qualifier is not present for the property.</span></span> <span data-ttu-id="6bab3-167">Автоматически создаваемая отметка времени может привести к ошибке в вычислении, так как отметка времени является приближенной и не учитывает дополнительную нагрузку, связанную с упаковкой и фактическим сбором данных.</span><span class="sxs-lookup"><span data-stu-id="6bab3-167">An automatically generated time stamp may introduce error in a calculation because the timestamp is an approximation and does not account for overhead incurred by marshaling and actual data collection.</span></span>

</dd> </dl>

## <a name="how-to-interpret-property-qualifiers"></a><span data-ttu-id="6bab3-168">Как интерпретировать квалификаторы свойств</span><span class="sxs-lookup"><span data-stu-id="6bab3-168">How to Interpret Property Qualifiers</span></span>

<span data-ttu-id="6bab3-169">Свойства в классах [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) содержат вычисляемые данные, предоставляемые [поставщиком данных о производительности](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6bab3-169">Properties in the [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes contain the calculated data supplied by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span> <span data-ttu-id="6bab3-170">Значение свойства является окончательным вычисленным результатом.</span><span class="sxs-lookup"><span data-stu-id="6bab3-170">The property value is the final calculated result.</span></span> <span data-ttu-id="6bab3-171">Квалификаторы предоставляют рецепт.</span><span class="sxs-lookup"><span data-stu-id="6bab3-171">The qualifiers supply a recipe.</span></span>

<span data-ttu-id="6bab3-172">Квалификаторы **Counter** и **base** указывают на источники данных, а **кукингтипе** указывает формулу, используемую для получения результата.</span><span class="sxs-lookup"><span data-stu-id="6bab3-172">The **Counter** and **Base** qualifiers point to the sources of data and **CookingType** specifies the formula used to produce the result.</span></span> <span data-ttu-id="6bab3-173">Отметка времени и периодичность выборки также берутся из соответствующего необработанного класса и именуются в **перфтиместамп** и **перфтимефрек**.</span><span class="sxs-lookup"><span data-stu-id="6bab3-173">The timestamp and sample frequency also come from the corresponding raw class and are named in **PerfTimeStamp** and **PerfTimeFreq**.</span></span>

<span data-ttu-id="6bab3-174">Например, один из форматированных классов, предоставляемый WMI, [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), содержит свойство с именем **авгдискбитесперреад**.</span><span class="sxs-lookup"><span data-stu-id="6bab3-174">For example, one of the formatted classes supplied by WMI, [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md), contains a property named **AvgDiskBytesPerRead**.</span></span> <span data-ttu-id="6bab3-175">Имя свойства в форматированном классе должно совпадать со свойством в необработанном классе.</span><span class="sxs-lookup"><span data-stu-id="6bab3-175">The name of the property in the formatted class must be the same as the property in the raw class.</span></span> <span data-ttu-id="6bab3-176">Свойство **авгдискбитесперреад** имеет следующие квалификаторы.</span><span class="sxs-lookup"><span data-stu-id="6bab3-176">The **AvgDiskBytesPerRead** property has the following qualifiers.</span></span>

<span data-ttu-id="6bab3-177">В следующем списке перечислены доступные квалификаторы свойств для свойств всех классов, производных от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="6bab3-177">The following list lists the available property qualifiers for properties of all classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>



| <span data-ttu-id="6bab3-178">Квалификатор</span><span class="sxs-lookup"><span data-stu-id="6bab3-178">Qualifier</span></span>         | <span data-ttu-id="6bab3-179">Значение</span><span class="sxs-lookup"><span data-stu-id="6bab3-179">Value</span></span>                     |
|-------------------|---------------------------|
| <span data-ttu-id="6bab3-180">**кукингтипе**</span><span class="sxs-lookup"><span data-stu-id="6bab3-180">**CookingType**</span></span>   | <span data-ttu-id="6bab3-181">Средний показатель производительности \_ \_</span><span class="sxs-lookup"><span data-stu-id="6bab3-181">PERF\_AVERAGE\_BULK</span></span>       |
| <span data-ttu-id="6bab3-182">**Счетчик**</span><span class="sxs-lookup"><span data-stu-id="6bab3-182">**Counter**</span></span>       | <span data-ttu-id="6bab3-183">авгдискбитесперреад</span><span class="sxs-lookup"><span data-stu-id="6bab3-183">AvgDiskBytesPerRead</span></span>       |
| <span data-ttu-id="6bab3-184">**перфтиместамп**</span><span class="sxs-lookup"><span data-stu-id="6bab3-184">**PerfTimeStamp**</span></span> | <span data-ttu-id="6bab3-185">Метка времени \_ перфтиме</span><span class="sxs-lookup"><span data-stu-id="6bab3-185">Timestamp\_PerfTime</span></span>       |
| <span data-ttu-id="6bab3-186">**перфтимефрек**</span><span class="sxs-lookup"><span data-stu-id="6bab3-186">**PerfTimeFreq**</span></span>  | <span data-ttu-id="6bab3-187">Частота \_ перфтиме</span><span class="sxs-lookup"><span data-stu-id="6bab3-187">Frequency\_PerfTime</span></span>       |
| <span data-ttu-id="6bab3-188">**перфиндекс**</span><span class="sxs-lookup"><span data-stu-id="6bab3-188">**PerfIndex**</span></span>     | <span data-ttu-id="6bab3-189">408</span><span class="sxs-lookup"><span data-stu-id="6bab3-189">408</span></span>                       |
| <span data-ttu-id="6bab3-190">**хелпиндекс**</span><span class="sxs-lookup"><span data-stu-id="6bab3-190">**HelpIndex**</span></span>     | <span data-ttu-id="6bab3-191">409</span><span class="sxs-lookup"><span data-stu-id="6bab3-191">409</span></span>                       |
| <span data-ttu-id="6bab3-192">**Из**</span><span class="sxs-lookup"><span data-stu-id="6bab3-192">**Base**</span></span>          | <span data-ttu-id="6bab3-193">\_Базовый авгдискбитесперреад</span><span class="sxs-lookup"><span data-stu-id="6bab3-193">AvgDiskBytesPerRead\_Base</span></span> |



 

<span data-ttu-id="6bab3-194">Свойство **авгдискбитесперреад** Возвращает среднее число байтов, передаваемых с диска во время операций чтения.</span><span class="sxs-lookup"><span data-stu-id="6bab3-194">The **AvgDiskBytesPerRead** property reports the average number of bytes transferred from the disk during read operations.</span></span> <span data-ttu-id="6bab3-195">Формула для \_ среднего значения производительности \_ :</span><span class="sxs-lookup"><span data-stu-id="6bab3-195">The formula for PERF\_AVERAGE\_BULK is:</span></span>

<span data-ttu-id="6bab3-196">(Sample2-sample1)/(Base sample2 — Base sample1)</span><span class="sxs-lookup"><span data-stu-id="6bab3-196">(Sample2 - Sample1) / (Base Sample2 - Base Sample1)</span></span>

<span data-ttu-id="6bab3-197">Операция чтения выдается с частотой, указанной параметром **перфтимефрек** со значением **перфтиместамп** , указывающим на последний пример.</span><span class="sxs-lookup"><span data-stu-id="6bab3-197">The read operation is sampled at the frequency specified by **PerfTimeFreq** with the **PerfTimeStamp** value indicating the most recent sample.</span></span> <span data-ttu-id="6bab3-198">Необработанные данные счетчика в байтах берутся из свойства **авгдискбитесперреад** класса [**\_ \_ \_ LogicalDisk Win32 перфравдата перфдиск**](./retrieving-raw-and-formatted-performance-data.md) .</span><span class="sxs-lookup"><span data-stu-id="6bab3-198">The raw counter data in bytes is taken from the **AvgDiskBytesPerRead** property in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class.</span></span> <span data-ttu-id="6bab3-199">Базовое количество данных операций берется из **\_ базового свойства авгдискбитесперреад** в этом же классе.</span><span class="sxs-lookup"><span data-stu-id="6bab3-199">The base number of operations data is taken from the **AvgDiskBytesPerRead\_Base** property in that same class.</span></span>

<span data-ttu-id="6bab3-200">Дополнительные сведения см. в разделе [получение статистических данных о производительности](obtaining-statistical-performance-data.md) и [мониторинг данных производительности](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="6bab3-200">For more information, see [Obtaining Statistical Performance Data](obtaining-statistical-performance-data.md) and [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6bab3-201">См. также</span><span class="sxs-lookup"><span data-stu-id="6bab3-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bab3-202">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-202">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="6bab3-203">Квалификаторы, относящиеся к классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="6bab3-203">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="6bab3-204">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-204">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="6bab3-205">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="6bab3-205">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="6bab3-206">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="6bab3-206">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
