---
description: Абстрактный базовый класс для всех конкретных классов необработанных счетчиков производительности.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Класс Win32_PerfRawData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539356"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="19571-103">\_Класс Win32 перфравдата</span><span class="sxs-lookup"><span data-stu-id="19571-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="19571-104">Абстрактный базовый класс для всех конкретных классов необработанных счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="19571-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="19571-105">Для отображения в системном мониторе классы счетчиков производительности должны быть добавлены в корневое \\ пространство имен CIMV2 и быть производными от **Win32 \_ перфравдата**.</span><span class="sxs-lookup"><span data-stu-id="19571-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="19571-106">Данные в этих классах предоставляются [поставщиком счетчиков производительности](../wmisdk/performance-counter-provider.md)высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="19571-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="19571-107">Следующие свойства наследуются, если класс является производным от **Win32 \_ перфравдата**:</span><span class="sxs-lookup"><span data-stu-id="19571-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="19571-108">**Метка времени \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="19571-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="19571-109">**Метка времени \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="19571-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="19571-110">**\_Объект timestamp**</span><span class="sxs-lookup"><span data-stu-id="19571-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="19571-111">**Частота \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="19571-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="19571-112">**Частота \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="19571-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="19571-113">**Frequency, \_ объект**</span><span class="sxs-lookup"><span data-stu-id="19571-113">**Frequency\_Object**</span></span>

<span data-ttu-id="19571-114">В каждом случае свойства должны быть заполнены поставщиком, или класс не может быть отображен в системном мониторе.</span><span class="sxs-lookup"><span data-stu-id="19571-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="19571-115">Эти свойства используются для вычисления формул типа счетчика потребителями данных производительности.</span><span class="sxs-lookup"><span data-stu-id="19571-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="19571-116">Следующий синтаксис упрощен из MOF-кода и содержит все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="19571-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19571-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19571-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="19571-118">Члены</span><span class="sxs-lookup"><span data-stu-id="19571-118">Members</span></span>

<span data-ttu-id="19571-119">Класс **Win32 \_ перфравдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="19571-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="19571-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="19571-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19571-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="19571-121">Properties</span></span>

<span data-ttu-id="19571-122">Класс **Win32 \_ перфравдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="19571-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19571-123">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="19571-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19571-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19571-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19571-126">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="19571-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="19571-127">Краткое текстовое описание для статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="19571-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="19571-128">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="19571-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19571-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19571-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19571-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-132">Текстовое описание статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="19571-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="19571-133">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="19571-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-134">**Frequency, \_ объект**</span><span class="sxs-lookup"><span data-stu-id="19571-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19571-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19571-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-137">Частота в тактах в секунду для свойства **\_ объекта timestamp** .</span><span class="sxs-lookup"><span data-stu-id="19571-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="19571-138">При наличии подклассов поставщик определяет это свойство.</span><span class="sxs-lookup"><span data-stu-id="19571-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="19571-139">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19571-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="19571-140">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="19571-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-141">**Частота \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="19571-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-142">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19571-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19571-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-144">Частота в тактах в секунду для свойства **Frequency \_ перфтиме** .</span><span class="sxs-lookup"><span data-stu-id="19571-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="19571-145">Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="19571-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="19571-146">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19571-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="19571-147">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="19571-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-148">**Частота \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="19571-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-149">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19571-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19571-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-151">Частота в тактах в секунду для свойства **timestamp \_ Sys100NS** (10000000).</span><span class="sxs-lookup"><span data-stu-id="19571-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="19571-152">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19571-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="19571-153">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="19571-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-154">**Name**</span><span class="sxs-lookup"><span data-stu-id="19571-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="19571-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="19571-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19571-157">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="19571-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="19571-158">Метка, на которой известна статистика или метрика.</span><span class="sxs-lookup"><span data-stu-id="19571-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="19571-159">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="19571-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="19571-160">Это свойство наследуется от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="19571-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-161">**\_Объект timestamp**</span><span class="sxs-lookup"><span data-stu-id="19571-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-162">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19571-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19571-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-164">Отметка времени, определяемая объектом.</span><span class="sxs-lookup"><span data-stu-id="19571-164">Object-defined timestamp.</span></span> <span data-ttu-id="19571-165">Поставщик определяет его свойство.</span><span class="sxs-lookup"><span data-stu-id="19571-165">The provider defines his property.</span></span>

<span data-ttu-id="19571-166">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19571-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="19571-167">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="19571-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-168">**Метка времени \_ перфтиме**</span><span class="sxs-lookup"><span data-stu-id="19571-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-169">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19571-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19571-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-171">Метка времени счетчика высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="19571-171">High Performance counter timestamp.</span></span> <span data-ttu-id="19571-172">Значение можно получить, вызвав функцию Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="19571-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="19571-173">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19571-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="19571-174">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="19571-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="19571-175">**Метка времени \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="19571-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19571-176">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="19571-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="19571-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19571-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="19571-178">Значение метки времени в единицах 100 нс.</span><span class="sxs-lookup"><span data-stu-id="19571-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="19571-179">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="19571-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="19571-180">Это свойство наследуется из [**Win32 \_ Perf**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="19571-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19571-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19571-181">Remarks</span></span>

<span data-ttu-id="19571-182">Класс **Win32 \_ перфравдата** является производным от [**Win32 \_ Perf**](win32-perf.md), который является производным от [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="19571-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="19571-183">Все классы, производные от [**\_ производительности Win32**](win32-perf.md) , предназначены для использования с объектом [*обновления*](../wmisdk/gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="19571-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="19571-184">Дополнительные сведения о создании и использовании объекта обновления на языке программирования C++ см. в разделе [доступ к данным производительности в c++](../wmisdk/accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="19571-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="19571-185">Дополнительные сведения о создании и использовании объекта обновления в языке программирования сценариев см. [в разделе Обновление данных WMI в скриптах](../wmisdk/refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="19571-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19571-186">Требования</span><span class="sxs-lookup"><span data-stu-id="19571-186">Requirements</span></span>



| <span data-ttu-id="19571-187">Требование</span><span class="sxs-lookup"><span data-stu-id="19571-187">Requirement</span></span> | <span data-ttu-id="19571-188">Значение</span><span class="sxs-lookup"><span data-stu-id="19571-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="19571-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19571-189">Minimum supported client</span></span><br/> | <span data-ttu-id="19571-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19571-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="19571-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19571-191">Minimum supported server</span></span><br/> | <span data-ttu-id="19571-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19571-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="19571-193">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="19571-193">Namespace</span></span><br/>                | <span data-ttu-id="19571-194">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19571-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="19571-195">MOF</span><span class="sxs-lookup"><span data-stu-id="19571-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19571-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19571-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="19571-197">DLL</span><span class="sxs-lookup"><span data-stu-id="19571-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19571-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19571-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19571-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19571-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19571-200">**Производительность \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="19571-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="19571-201">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="19571-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="19571-202">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="19571-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="19571-203">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="19571-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="19571-204">Доступ к данным о производительности в скрипте</span><span class="sxs-lookup"><span data-stu-id="19571-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
