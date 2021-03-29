---
description: Абстрактный базовый класс для предустановленных вычисляемых классов данных.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Класс Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990725"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="cdd5e-103">\_Класс Win32 перфформаттеддата</span><span class="sxs-lookup"><span data-stu-id="cdd5e-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="cdd5e-104">Абстрактный базовый класс для предустановленных вычисляемых классов данных.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="cdd5e-105">Примером такого класса является [**Win32 \_ перфформаттеддата \_ перфдиск \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="cdd5e-106">Эти классы содержат вычисляемые значения, предоставляемые [поставщиком данных о производительности](../wmisdk/formatted-performance-data-provider.md)с высокой производительностью.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="cdd5e-107">Следующий синтаксис упрощен из MOF-кода и показывает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdd5e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cdd5e-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="cdd5e-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cdd5e-109">Members</span></span>

<span data-ttu-id="cdd5e-110">Класс **Win32 \_ перфформаттеддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cdd5e-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="cdd5e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdd5e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdd5e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="cdd5e-112">Properties</span></span>

<span data-ttu-id="cdd5e-113">Класс **Win32 \_ перфформаттеддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdd5e-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-117">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cdd5e-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-118">Краткое текстовое описание для статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="cdd5e-119">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-123">Текстовое описание статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="cdd5e-124">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-125">**Frequency, \_ объект**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-128">Частота в тактах в секунду для свойства **\_ объекта timestamp** .</span><span class="sxs-lookup"><span data-stu-id="cdd5e-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="cdd5e-129">При наличии подклассов поставщик определяет это свойство.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="cdd5e-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="cdd5e-131">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-132">**Частота \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-135">Частота в тактах в секунду для свойства **Frequency \_ перфтиме** .</span><span class="sxs-lookup"><span data-stu-id="cdd5e-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="cdd5e-136">Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="cdd5e-137">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="cdd5e-138">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-139">**Частота \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-140">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-142">Частота в тактах в секунду для свойства **timestamp \_ Sys100NS** (10000000).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="cdd5e-143">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="cdd5e-144">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-145">**Name**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-148">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cdd5e-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-149">Метка, на которой известна статистика или метрика.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="cdd5e-150">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="cdd5e-151">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-152">**\_Объект timestamp**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-153">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-155">Отметка времени, определяемая объектом.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-155">Object-defined timestamp.</span></span> <span data-ttu-id="cdd5e-156">Поставщик определяет его свойство.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-156">The provider defines his property.</span></span>

<span data-ttu-id="cdd5e-157">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="cdd5e-158">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-159">**Метка времени \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-160">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-162">Метка времени счетчика высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-162">High Performance counter timestamp.</span></span> <span data-ttu-id="cdd5e-163">Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="cdd5e-164">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="cdd5e-165">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="cdd5e-166">**Метка времени \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdd5e-167">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="cdd5e-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cdd5e-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cdd5e-169">Значение метки времени в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="cdd5e-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="cdd5e-170">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="cdd5e-171">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdd5e-172">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdd5e-172">Remarks</span></span>

<span data-ttu-id="cdd5e-173">Класс **Win32 \_ перфформаттеддата** является производным от [**Win32 \_ Perf**](win32-perf.md), который является производным от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="cdd5e-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="cdd5e-174">Класс находится в **корневом пространстве имен \\ CIMV2** .</span><span class="sxs-lookup"><span data-stu-id="cdd5e-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdd5e-175">Требования</span><span class="sxs-lookup"><span data-stu-id="cdd5e-175">Requirements</span></span>



| <span data-ttu-id="cdd5e-176">Требование</span><span class="sxs-lookup"><span data-stu-id="cdd5e-176">Requirement</span></span> | <span data-ttu-id="cdd5e-177">Значение</span><span class="sxs-lookup"><span data-stu-id="cdd5e-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd5e-178">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdd5e-178">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd5e-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdd5e-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="cdd5e-180">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdd5e-180">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd5e-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdd5e-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="cdd5e-182">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cdd5e-182">Namespace</span></span><br/>                | <span data-ttu-id="cdd5e-183">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cdd5e-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="cdd5e-184">MOF</span><span class="sxs-lookup"><span data-stu-id="cdd5e-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdd5e-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdd5e-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="cdd5e-186">DLL</span><span class="sxs-lookup"><span data-stu-id="cdd5e-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdd5e-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdd5e-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd5e-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdd5e-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd5e-189">**Производительность \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="cdd5e-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="cdd5e-190">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="cdd5e-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="cdd5e-191">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="cdd5e-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="cdd5e-192">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="cdd5e-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="cdd5e-193">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="cdd5e-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
