---
description: Базовый класс для классов счетчиков производительности Win32 \_ перфравдата и Win32 \_ перфформаттеддата.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Класс Win32_Perf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656009"
---
# <a name="win32_perf-class"></a><span data-ttu-id="db46b-103">\_Класс производительности Win32</span><span class="sxs-lookup"><span data-stu-id="db46b-103">Win32\_Perf class</span></span>

<span data-ttu-id="db46b-104">Базовый класс для классов счетчиков производительности [**Win32 \_ Перфравдата**](win32-perfrawdata.md) и [**Win32 \_ перфформаттеддата**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="db46b-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="db46b-105">**Win32 \_** Производительность определяет требуемые свойства timestamp и Frequency, используемые в алгоритмах [**CounterType**](../wmisdk/countertype-qualifier.md) для классов счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="db46b-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="db46b-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="db46b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="db46b-107">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="db46b-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="db46b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db46b-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="db46b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="db46b-109">Members</span></span>

<span data-ttu-id="db46b-110">Класс **\_ производительности Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="db46b-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="db46b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="db46b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="db46b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="db46b-112">Properties</span></span>

<span data-ttu-id="db46b-113">Класс **\_ производительности Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="db46b-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="db46b-114">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="db46b-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db46b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db46b-117">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="db46b-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="db46b-118">Краткое текстовое описание для статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="db46b-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="db46b-119">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="db46b-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="db46b-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db46b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-123">Текстовое описание статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="db46b-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="db46b-124">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="db46b-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-125">**Frequency, \_ объект**</span><span class="sxs-lookup"><span data-stu-id="db46b-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db46b-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-128">Частота в тактах в секунду для свойства **\_ объекта timestamp** .</span><span class="sxs-lookup"><span data-stu-id="db46b-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="db46b-129">При наличии подклассов поставщик определяет это свойство.</span><span class="sxs-lookup"><span data-stu-id="db46b-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="db46b-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db46b-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-131">**Частота \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="db46b-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-132">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db46b-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-134">Частота в тактах в секунду для свойства **Frequency \_ перфтиме** .</span><span class="sxs-lookup"><span data-stu-id="db46b-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="db46b-135">Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="db46b-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="db46b-136">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db46b-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-137">**Частота \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="db46b-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-138">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db46b-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-140">Частота в тактах в секунду для свойства **timestamp \_ Sys100NS** (10000000).</span><span class="sxs-lookup"><span data-stu-id="db46b-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="db46b-141">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db46b-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-142">**Name**</span><span class="sxs-lookup"><span data-stu-id="db46b-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="db46b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="db46b-145">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="db46b-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="db46b-146">Метка, на которой известна статистика или метрика.</span><span class="sxs-lookup"><span data-stu-id="db46b-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="db46b-147">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="db46b-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="db46b-148">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="db46b-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-149">**\_Объект timestamp**</span><span class="sxs-lookup"><span data-stu-id="db46b-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-150">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db46b-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-152">Отметка времени, определяемая объектом.</span><span class="sxs-lookup"><span data-stu-id="db46b-152">Object-defined timestamp.</span></span> <span data-ttu-id="db46b-153">Поставщик определяет его свойство.</span><span class="sxs-lookup"><span data-stu-id="db46b-153">The provider defines his property.</span></span>

<span data-ttu-id="db46b-154">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db46b-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-155">**Метка времени \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="db46b-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-156">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db46b-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-158">Метка времени счетчика высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="db46b-158">High Performance counter timestamp.</span></span> <span data-ttu-id="db46b-159">Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="db46b-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="db46b-160">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db46b-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="db46b-161">**Метка времени \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="db46b-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="db46b-162">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="db46b-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="db46b-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="db46b-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="db46b-164">Значение метки времени в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="db46b-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="db46b-165">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db46b-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db46b-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db46b-166">Remarks</span></span>

<span data-ttu-id="db46b-167">Класс **\_ производительности Win32** является производным от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="db46b-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db46b-168">Требования</span><span class="sxs-lookup"><span data-stu-id="db46b-168">Requirements</span></span>



| <span data-ttu-id="db46b-169">Требование</span><span class="sxs-lookup"><span data-stu-id="db46b-169">Requirement</span></span> | <span data-ttu-id="db46b-170">Значение</span><span class="sxs-lookup"><span data-stu-id="db46b-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="db46b-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db46b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="db46b-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db46b-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="db46b-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db46b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="db46b-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db46b-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="db46b-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db46b-175">Namespace</span></span><br/>                | <span data-ttu-id="db46b-176">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="db46b-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="db46b-177">DLL</span><span class="sxs-lookup"><span data-stu-id="db46b-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db46b-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db46b-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db46b-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db46b-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db46b-180">**\_СТАТИСТИКАЛИНФОРМАТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="db46b-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="db46b-181">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="db46b-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="db46b-182">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="db46b-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="db46b-183">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="db46b-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="db46b-184">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="db46b-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
