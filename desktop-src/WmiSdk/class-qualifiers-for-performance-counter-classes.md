---
description: Укажите сведения об объекте производительности, с которым сопоставлен класс счетчика производительности WMI.
ms.assetid: 7b8b7f00-95d8-4c1e-8638-157d0f4c7c32
ms.tgt_platform: multiple
title: Квалификаторы классов для классов счетчиков производительности
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4910af88ce7f96fda1b5f9b7ecd7a33479fc130
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712476"
---
# <a name="class-qualifiers-for-performance-counter-classes"></a><span data-ttu-id="85519-103">Квалификаторы классов для классов счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="85519-103">Class Qualifiers for Performance Counter Classes</span></span>

<span data-ttu-id="85519-104">Квалификаторы класса указывают сведения об объекте производительности, с которым сопоставлен [класс счетчика производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI.</span><span class="sxs-lookup"><span data-stu-id="85519-104">Class qualifiers specify information about the performance object to which the WMI [performance counter class](/windows/desktop/CIMWin32Prov/performance-counter-classes) is mapped.</span></span> <span data-ttu-id="85519-105">Дополнительные сведения см. в разделе [наблюдение за данными производительности](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="85519-105">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

-   [<span data-ttu-id="85519-106">Квалификаторы для необработанных и форматированных Перформанцеклассес</span><span class="sxs-lookup"><span data-stu-id="85519-106">Qualifiers for Raw and Formatted PerformanceClasses</span></span>](#qualifiers-for-raw-and-formatted-performanceclasses)
-   [<span data-ttu-id="85519-107">Квалификаторы для необработанных классов производительности</span><span class="sxs-lookup"><span data-stu-id="85519-107">Qualifiers for Raw Performance Classes</span></span>](#)
-   [<span data-ttu-id="85519-108">Квалификаторы для отформатированных классов производительности</span><span class="sxs-lookup"><span data-stu-id="85519-108">Qualifiers for Formatted Performance Classes</span></span>](#)
-   [<span data-ttu-id="85519-109">См. также</span><span class="sxs-lookup"><span data-stu-id="85519-109">Related topics</span></span>](#related-topics)


<span data-ttu-id="85519-110">Счетчик производительности — конкретные квалификаторы автоматически присоединяются поставщиком "Вбемперфкласс" к классам и свойствам [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) в корневом \\ CIMv2.</span><span class="sxs-lookup"><span data-stu-id="85519-110">Performance counter–specific qualifiers are automatically attached by the "WbemPerfClass" provider to [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes and properties in Root\\CIMv2.</span></span>

<span data-ttu-id="85519-111">Эти сведения применяются ко всем экземплярам класса.</span><span class="sxs-lookup"><span data-stu-id="85519-111">This information applies to all instances of the class.</span></span> <span data-ttu-id="85519-112">Некоторые квалификаторы с **логическими** значениями, которые всегда имеют **значение false** , могут отсутствовать в определенных классах.</span><span class="sxs-lookup"><span data-stu-id="85519-112">Some qualifiers with **Boolean** values that are always **False** may not be present on specific classes.</span></span>

## <a name="qualifiers-for-raw-and-formatted-performanceclasses"></a><span data-ttu-id="85519-113">Квалификаторы для необработанных и форматированных Перформанцеклассес</span><span class="sxs-lookup"><span data-stu-id="85519-113">Qualifiers for Raw and Formatted PerformanceClasses</span></span>

<span data-ttu-id="85519-114">Следующие квалификаторы применяются ко всем классам, производным от [**Win32 \_ Перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) и [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="85519-114">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="85519-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Обработанные**</span><span class="sxs-lookup"><span data-stu-id="85519-115"><span id="Cooked"></span><span id="cooked"></span><span id="COOKED"></span>**Cooked**</span></span>
</dt> <dd>

<span data-ttu-id="85519-116">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-116">**boolean**</span></span>

<span data-ttu-id="85519-117">Указывает, содержит ли класс данные обработанные.</span><span class="sxs-lookup"><span data-stu-id="85519-117">Indicates whether the class contains cooked data.</span></span>

</dd> <dt>

<span data-ttu-id="85519-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="85519-118"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="85519-119">**string**</span><span class="sxs-lookup"><span data-stu-id="85519-119">**string**</span></span>

<span data-ttu-id="85519-120">Имя объекта производительности.</span><span class="sxs-lookup"><span data-stu-id="85519-120">Performance object name.</span></span> <span data-ttu-id="85519-121">Дополнительные сведения см. в статье [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="85519-121">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

</dd> <dt>

<span data-ttu-id="85519-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**детаиллевел**</span><span class="sxs-lookup"><span data-stu-id="85519-122"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="85519-123">**sint32**</span><span class="sxs-lookup"><span data-stu-id="85519-123">**sint32**</span></span>

<span data-ttu-id="85519-124">Не предоставляет подробные данные.</span><span class="sxs-lookup"><span data-stu-id="85519-124">Does not provide detail data.</span></span> <span data-ttu-id="85519-125">Всегда содержит значение 100.</span><span class="sxs-lookup"><span data-stu-id="85519-125">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="85519-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Платформе**</span><span class="sxs-lookup"><span data-stu-id="85519-126"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>**Dynamic**</span></span>
</dt> <dd>

<span data-ttu-id="85519-127">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-127">**boolean**</span></span>

<span data-ttu-id="85519-128">Всегда имеет значение **true** , так как экземпляры всегда являются динамическими.</span><span class="sxs-lookup"><span data-stu-id="85519-128">Always set to **True** because instances are always dynamic.</span></span>

</dd> <dt>

<span data-ttu-id="85519-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**женерикперфктр**</span><span class="sxs-lookup"><span data-stu-id="85519-129"><span id="GenericPerfCtr"></span><span id="genericperfctr"></span><span id="GENERICPERFCTR"></span>**GenericPerfCtr**</span></span>
</dt> <dd>

<span data-ttu-id="85519-130">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-130">**boolean**</span></span>

<span data-ttu-id="85519-131">Указывает, поступает ли класс из устаревшей библиотеки производительности.</span><span class="sxs-lookup"><span data-stu-id="85519-131">Indicates whether the class comes from a legacy performance library.</span></span> <span data-ttu-id="85519-132">Всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="85519-132">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="85519-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**хелпиндекс**</span><span class="sxs-lookup"><span data-stu-id="85519-133"><span id="HelpIndex"></span><span id="helpindex"></span><span id="HELPINDEX"></span>**HelpIndex**</span></span>
</dt> <dd>

<span data-ttu-id="85519-134">**sint32**</span><span class="sxs-lookup"><span data-stu-id="85519-134">**sint32**</span></span>

<span data-ttu-id="85519-135">Индексы больше не действительны.</span><span class="sxs-lookup"><span data-stu-id="85519-135">Indexes are no longer valid.</span></span> <span data-ttu-id="85519-136">Этот квалификатор всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="85519-136">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="85519-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="85519-137"><span id="HiPerf_"></span><span id="hiperf_"></span><span id="HIPERF_"></span>**HiPerf**</span></span> 
</dt> <dd>

<span data-ttu-id="85519-138">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-138">**boolean**</span></span>

<span data-ttu-id="85519-139">Указывает, что класс является классом высокой производительности.</span><span class="sxs-lookup"><span data-stu-id="85519-139">Indicates that the class is a high-performance class.</span></span> <span data-ttu-id="85519-140">Всегда имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="85519-140">Always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="85519-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Языкового стандарта**</span><span class="sxs-lookup"><span data-stu-id="85519-141"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="85519-142">**sint32**</span><span class="sxs-lookup"><span data-stu-id="85519-142">**sint32**</span></span>

<span data-ttu-id="85519-143">Идентификатор языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="85519-143">Locale identifier.</span></span> <span data-ttu-id="85519-144">Значение всегда равно 1033 (Английский (США)).</span><span class="sxs-lookup"><span data-stu-id="85519-144">Value is always 1033 (U.S. English).</span></span>

</dd> <dt>

<span data-ttu-id="85519-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**перфиндекс**</span><span class="sxs-lookup"><span data-stu-id="85519-145"><span id="PerfIndex"></span><span id="perfindex"></span><span id="PERFINDEX"></span>**PerfIndex**</span></span>
</dt> <dd>

<span data-ttu-id="85519-146">**int32**</span><span class="sxs-lookup"><span data-stu-id="85519-146">**int32**</span></span>

<span data-ttu-id="85519-147">Индексы больше не действительны.</span><span class="sxs-lookup"><span data-stu-id="85519-147">Indexes are no longer valid.</span></span> <span data-ttu-id="85519-148">Этот квалификатор всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="85519-148">This qualifier is always zero.</span></span>

</dd> <dt>

<span data-ttu-id="85519-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Поставщики**</span><span class="sxs-lookup"><span data-stu-id="85519-149"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="85519-150">**string**</span><span class="sxs-lookup"><span data-stu-id="85519-150">**string**</span></span>

<span data-ttu-id="85519-151">Имя поставщика экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85519-151">Name of the instance provider.</span></span> <span data-ttu-id="85519-152">Значение — "WbemPerfV2".</span><span class="sxs-lookup"><span data-stu-id="85519-152">Value is "WbemPerfV2".</span></span>

</dd> <dt>

<span data-ttu-id="85519-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span><span class="sxs-lookup"><span data-stu-id="85519-153"><span id="RegistryKey"></span><span id="registrykey"></span><span id="REGISTRYKEY"></span>**RegistryKey**</span></span>
</dt> <dd>

<span data-ttu-id="85519-154">**string**</span><span class="sxs-lookup"><span data-stu-id="85519-154">**string**</span></span>

<span data-ttu-id="85519-155">Имя драйвера в разделе **hKey \_ Local \_ Machine \\ CurrentControlSet \\ Services** , в котором можно найти ключ производительности.</span><span class="sxs-lookup"><span data-stu-id="85519-155">Name of the driver in the **HKEY\_LOCAL\_MACHINE\\CurrentControlSet\\Services** key, under which the performance key can be located.</span></span> <span data-ttu-id="85519-156">Это имя также является именем службы, предоставляющей счетчик производительности.</span><span class="sxs-lookup"><span data-stu-id="85519-156">This name is also the name of the service that provides the performance counter.</span></span>

</dd> <dt>

<span data-ttu-id="85519-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Единый**</span><span class="sxs-lookup"><span data-stu-id="85519-157"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="85519-158">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-158">**boolean**</span></span>

<span data-ttu-id="85519-159">Если **значение — true**, указывает, что существует только один экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="85519-159">If **True**, indicates that only a single instance of the class exists.</span></span>

</dd> </dl>

## <a name="qualifiers-for-raw-performance-classes"></a><span data-ttu-id="85519-160">Квалификаторы для необработанных классов производительности</span><span class="sxs-lookup"><span data-stu-id="85519-160">Qualifiers for Raw Performance Classes</span></span>

<span data-ttu-id="85519-161">Следующие квалификаторы применяются ко всем классам, производным от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span><span class="sxs-lookup"><span data-stu-id="85519-161">The following qualifiers apply to all classes that are derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata).</span></span>

<dl> <dt>

<span data-ttu-id="85519-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Требуют**</span><span class="sxs-lookup"><span data-stu-id="85519-162"><span id="Costly"></span><span id="costly"></span><span id="COSTLY"></span>**Costly**</span></span>
</dt> <dd>

<span data-ttu-id="85519-163">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-163">**boolean**</span></span>

<span data-ttu-id="85519-164">Указывает, является ли получение экземпляров этого класса дорогостоящей операцией.</span><span class="sxs-lookup"><span data-stu-id="85519-164">Indicates whether obtaining instances of this class is a costly operation.</span></span> <span data-ttu-id="85519-165">Всегда имеет значение **true** для классов с \_ добавлением "дорогостоящих" к концу имени класса.</span><span class="sxs-lookup"><span data-stu-id="85519-165">Always set to **True** for classes with "\_Costly" appended to the end of the class name.</span></span>

</dd> <dt>

<span data-ttu-id="85519-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**детаиллевел**</span><span class="sxs-lookup"><span data-stu-id="85519-166"><span id="DetailLevel"></span><span id="detaillevel"></span><span id="DETAILLEVEL"></span>**DetailLevel**</span></span>
</dt> <dd>

<span data-ttu-id="85519-167">**uint32**</span><span class="sxs-lookup"><span data-stu-id="85519-167">**uint32**</span></span>

<span data-ttu-id="85519-168">Не предоставляет подробные данные.</span><span class="sxs-lookup"><span data-stu-id="85519-168">Does not provide detail data.</span></span> <span data-ttu-id="85519-169">Всегда содержит значение 100.</span><span class="sxs-lookup"><span data-stu-id="85519-169">Always contains value of 100.</span></span>

</dd> <dt>

<span data-ttu-id="85519-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**перфдефаулт**</span><span class="sxs-lookup"><span data-stu-id="85519-170"><span id="PerfDefault"></span><span id="perfdefault"></span><span id="PERFDEFAULT"></span>**PerfDefault**</span></span>
</dt> <dd>

<span data-ttu-id="85519-171">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85519-171">**boolean**</span></span>

<span data-ttu-id="85519-172">Значение всегда равно **false**.</span><span class="sxs-lookup"><span data-stu-id="85519-172">Value is always **False**.</span></span>

</dd> </dl>

## <a name="qualifiers-for-formatted-performance-classes"></a><span data-ttu-id="85519-173">Квалификаторы для отформатированных классов производительности</span><span class="sxs-lookup"><span data-stu-id="85519-173">Qualifiers for Formatted Performance Classes</span></span>

<span data-ttu-id="85519-174">Следующие квалификаторы применяются ко всем классам, производным от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="85519-174">The following qualifiers apply to all classes that are derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span>

<dl> <dt>

<span data-ttu-id="85519-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**Автокука**</span><span class="sxs-lookup"><span data-stu-id="85519-175"><span id="AutoCook"></span><span id="autocook"></span><span id="AUTOCOOK"></span>**AutoCook**</span></span>
</dt> <dd>

<span data-ttu-id="85519-176">**int32**</span><span class="sxs-lookup"><span data-stu-id="85519-176">**int32**</span></span>

<span data-ttu-id="85519-177">Указывает, что значения в экземплярах класса автоматически вычисляются на основе соответствующего класса необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="85519-177">Indicates that the values in class instances are automatically calculated from the corresponding raw data class.</span></span> <span data-ttu-id="85519-178">Значение всегда равно 1.</span><span class="sxs-lookup"><span data-stu-id="85519-178">Value is always 1.</span></span>

</dd> <dt>

<span data-ttu-id="85519-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**\_Равкласс**</span><span class="sxs-lookup"><span data-stu-id="85519-179"><span id="AutoCook_RawClass"></span><span id="autocook_rawclass"></span><span id="AUTOCOOK_RAWCLASS"></span>**AutoCook\_RawClass**</span></span>
</dt> <dd>

<span data-ttu-id="85519-180">**string**</span><span class="sxs-lookup"><span data-stu-id="85519-180">**string**</span></span>

<span data-ttu-id="85519-181">Имя необработанного класса, используемое для вычисления для форматированного класса.</span><span class="sxs-lookup"><span data-stu-id="85519-181">Name of the raw class to use for calculation for the formatted class.</span></span> <span data-ttu-id="85519-182">Этот квалификатор является обязательным.</span><span class="sxs-lookup"><span data-stu-id="85519-182">This qualifier is required.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="85519-183">См. также</span><span class="sxs-lookup"><span data-stu-id="85519-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85519-184">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="85519-184">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="85519-185">Квалификаторы, относящиеся к классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="85519-185">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="85519-186">Классы счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="85519-186">Performance Counter Classes</span></span>](/windows/desktop/CIMWin32Prov/performance-counter-classes)
</dt> <dt>

[<span data-ttu-id="85519-187">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="85519-187">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="85519-188">Задачи WMI: Мониторинг производительности</span><span class="sxs-lookup"><span data-stu-id="85519-188">WMI Tasks: Performance Monitoring</span></span>](wmi-tasks--performance-monitoring.md)
</dt> </dl>

 

 
