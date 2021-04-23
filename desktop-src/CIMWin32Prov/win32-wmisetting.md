---
description: '\_Класс WMI Win32 вмисеттинг Singleton содержит рабочие параметры для службы WMI. Этот класс может иметь только один экземпляр, который всегда существует для каждой системы Windows и не может быть удален. Невозможно создать дополнительные экземпляры.'
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Класс Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895450"
---
# <a name="win32_wmisetting-class"></a><span data-ttu-id="dfef2-105">\_Класс Win32 вмисеттинг</span><span class="sxs-lookup"><span data-stu-id="dfef2-105">Win32\_WMISetting class</span></span>

<span data-ttu-id="dfef2-106">[Класс WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ вмисеттинг** Singleton содержит рабочие параметры для службы WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-106">The **Win32\_WMISetting** singleton [WMI class](../wmisdk/retrieving-a-class.md) contains the operational parameters for the WMI service.</span></span> <span data-ttu-id="dfef2-107">Этот класс может иметь только один экземпляр, который всегда существует для каждой системы Windows и не может быть удален.</span><span class="sxs-lookup"><span data-stu-id="dfef2-107">This class can only have one instance, which always exists for each Windows system and cannot be deleted.</span></span> <span data-ttu-id="dfef2-108">Невозможно создать дополнительные экземпляры.</span><span class="sxs-lookup"><span data-stu-id="dfef2-108">Additional instances cannot be created.</span></span>

<span data-ttu-id="dfef2-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dfef2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dfef2-110">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="dfef2-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfef2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dfef2-111">Syntax</span></span>

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a><span data-ttu-id="dfef2-112">Члены</span><span class="sxs-lookup"><span data-stu-id="dfef2-112">Members</span></span>

<span data-ttu-id="dfef2-113">Класс **Win32 \_ вмисеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dfef2-113">The **Win32\_WMISetting** class has these types of members:</span></span>

-   [<span data-ttu-id="dfef2-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="dfef2-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dfef2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="dfef2-115">Properties</span></span>

<span data-ttu-id="dfef2-116">Класс **Win32 \_ вмисеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dfef2-116">The **Win32\_WMISetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dfef2-117">**аспскриптдефаултнамеспаце**</span><span class="sxs-lookup"><span data-stu-id="dfef2-117">**ASPScriptDefaultNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-120">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| по умолчанию Namespace")</span><span class="sxs-lookup"><span data-stu-id="dfef2-120">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Default Namespace")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-121">Пространство имен скрипта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfef2-121">Default script namespace.</span></span> <span data-ttu-id="dfef2-122">Это свойство содержит пространство имен, используемое вызовами из API скриптов для WMI, если в вызывающей стороне не указано ни одного объекта.</span><span class="sxs-lookup"><span data-stu-id="dfef2-122">This property contains the namespace used by calls from the Scripting API for WMI if none is specified by the caller.</span></span>

<span data-ttu-id="dfef2-123">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-123">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-124">**HKey \_ \_** \\  \\  \\  \\ **\| Пространство имен по умолчанию сценариев** Microsoft WBEM по локальному компьютеру    </span><span class="sxs-lookup"><span data-stu-id="dfef2-124">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **scripting\|Default Namespace**</span></span>

<span data-ttu-id="dfef2-125">Пример: root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfef2-125">Example: root\\cimv2</span></span>

<span data-ttu-id="dfef2-126">Пример сценария, в котором используется это свойство, см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="dfef2-126">For an example script that uses this property, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-127">**аспскриптенаблед**</span><span class="sxs-lookup"><span data-stu-id="dfef2-127">**ASPScriptEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-128">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfef2-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-130">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| включения for ASP")</span><span class="sxs-lookup"><span data-stu-id="dfef2-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\scripting\|Enable for ASP")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-131">Если **значение — true**, скрипты WMI можно использовать на Active Server страницах (ASP).</span><span class="sxs-lookup"><span data-stu-id="dfef2-131">If **True**, WMI scripting can be used on Active Server Pages (ASP).</span></span> <span data-ttu-id="dfef2-132">Это свойство допустимо только в системах с неподдерживаемыми версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="dfef2-132">This property is valid on systems running unsupported versions of Windows only.</span></span> <span data-ttu-id="dfef2-133">Для поддерживаемых систем Windows сценарии WMI всегда разрешены в ASP.</span><span class="sxs-lookup"><span data-stu-id="dfef2-133">For supported Windows systems, WMI scripting is always allowed on ASP.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-134">**ауторековермофс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-134">**AutorecoverMofs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-135">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dfef2-135">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-137">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Автовосстановление MOF")</span><span class="sxs-lookup"><span data-stu-id="dfef2-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Autorecover MOFs")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-138">Список полных имен MOF-файлов, используемых для инициализации или восстановления репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-138">List of fully qualified MOF file names used to initialize or recover the WMI repository.</span></span> <span data-ttu-id="dfef2-139">Этот список определяет порядок, в котором компилируются MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="dfef2-139">The list determines the order in which MOF files are compiled.</span></span>

<span data-ttu-id="dfef2-140">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-140">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-141">**HKey \_ Локальное \_** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| Автовосстановление MOF**    </span><span class="sxs-lookup"><span data-stu-id="dfef2-141">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Autorecover MOFs**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-142">**AutoStartWin9X**</span><span class="sxs-lookup"><span data-stu-id="dfef2-142">**AutoStartWin9X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-144">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-145">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")</span><span class="sxs-lookup"><span data-stu-id="dfef2-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|AutostartWin9X")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-146">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfef2-146">Not supported.</span></span>

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

<span data-ttu-id="dfef2-147">**Не запускать** (0)</span><span class="sxs-lookup"><span data-stu-id="dfef2-147">**Don't start** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

<span data-ttu-id="dfef2-148">**Автозапуск** (1)</span><span class="sxs-lookup"><span data-stu-id="dfef2-148">**Autostart** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

<span data-ttu-id="dfef2-149">**Запуск при перезагрузке** (2)</span><span class="sxs-lookup"><span data-stu-id="dfef2-149">**Start on reboot** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dfef2-150">**Тот**</span><span class="sxs-lookup"><span data-stu-id="dfef2-150">**BackupInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-152">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-153">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM, \\ \\ \| пороговое значение интервала резервного копирования"), [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="dfef2-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Backup Interval Threshold"), [**Units**](../wmisdk/standard-qualifiers.md) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-154">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfef2-154">Not supported.</span></span> <span data-ttu-id="dfef2-155">Вместо этого создайте резервную копию репозитория WMI вручную.</span><span class="sxs-lookup"><span data-stu-id="dfef2-155">Instead, backup the WMI repository manually.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-156">**баккупласттиме**</span><span class="sxs-lookup"><span data-stu-id="dfef2-156">**BackupLastTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-157">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dfef2-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-159">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции времени Win32API \| жеттимезонеинформатион")</span><span class="sxs-lookup"><span data-stu-id="dfef2-159">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Time Functions\|GetTimeZoneInformation")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-160">Дата и время последнего выполнения резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="dfef2-160">Date and time the last backup was performed.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-161">**BuildVersion**</span><span class="sxs-lookup"><span data-stu-id="dfef2-161">**BuildVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-164">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Build")</span><span class="sxs-lookup"><span data-stu-id="dfef2-164">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Build")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-165">Сведения о версии текущей установленной службы WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-165">Version information for the currently installed WMI service.</span></span>

<span data-ttu-id="dfef2-166">Интервал времени между резервными копиями базы данных WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-166">Length of time that elapses between backups of the WMI database.</span></span>

<span data-ttu-id="dfef2-167">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-167">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-168">**HKey \_ По для локального \_ компьютера** \\  \\  \\ **\| Сборка Microsoft WBEM**</span><span class="sxs-lookup"><span data-stu-id="dfef2-168">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Build**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-169">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="dfef2-169">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-172">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="dfef2-172">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-173">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="dfef2-173">Short textual description of the current object.</span></span>

<span data-ttu-id="dfef2-174">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="dfef2-174">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-175">**датабаседиректори**</span><span class="sxs-lookup"><span data-stu-id="dfef2-175">**DatabaseDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-176">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-178">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| каталог репозитория")</span><span class="sxs-lookup"><span data-stu-id="dfef2-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Repository Directory")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-179">Путь к каталогу, который содержит репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-179">Directory path that contains the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-180">**датабасемакссизе**</span><span class="sxs-lookup"><span data-stu-id="dfef2-180">**DatabaseMaxSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-181">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-181">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-183">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB size"), [**Units**](../wmisdk/standard-qualifiers.md) ("килобайты")</span><span class="sxs-lookup"><span data-stu-id="dfef2-183">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max DB Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-184">Максимальный размер репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-184">Maximum size of the WMI repository.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-185">**Описание**</span><span class="sxs-lookup"><span data-stu-id="dfef2-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-188">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="dfef2-188">Textual description of the current object.</span></span>

<span data-ttu-id="dfef2-189">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="dfef2-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-190">**EnableAnonWin9xConnections**</span><span class="sxs-lookup"><span data-stu-id="dfef2-190">**EnableAnonWin9xConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-191">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfef2-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-193">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| енаблеанонконнектионс")</span><span class="sxs-lookup"><span data-stu-id="dfef2-193">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableAnonConnections")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-194">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="dfef2-194">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-195">**EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="dfef2-195">**EnableEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfef2-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-198">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")</span><span class="sxs-lookup"><span data-stu-id="dfef2-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableEvents")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-199">Если **значение — true**, подсистема событий WMI должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="dfef2-199">If **True**, the WMI event subsystem should be enabled.</span></span>

<span data-ttu-id="dfef2-200">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-200">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-201">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**</span><span class="sxs-lookup"><span data-stu-id="dfef2-201">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|EnableEvents**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-202">**енаблестартуфеаппреаллокатион**</span><span class="sxs-lookup"><span data-stu-id="dfef2-202">**EnableStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-203">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="dfef2-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-204">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-204">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-205">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| енаблестартуфеаппреаллокатион")</span><span class="sxs-lookup"><span data-stu-id="dfef2-205">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|EnableStartupHeapPreallocation")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-206">Если **значение — true**, Инструментарий WMI создает предварительно распределенную кучу с размером значения **ЛАСТСТАРТУФЕАППРЕАЛЛОКАТИОН** при инициализации WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-206">If **True**, WMI creates a pre-allocated heap with the size of the **LastStartupHeapPreallocation** value when WMI is initialized.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-207">**хигхсрешолдонклиентобжектс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-207">**HighThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-208">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-209">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-210">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM, \\ \\ \| Высокая пороговое значение для клиентских объектов"), [**единиц**](../wmisdk/standard-qualifiers.md) ("объектов в секунду")</span><span class="sxs-lookup"><span data-stu-id="dfef2-210">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-211">Максимальная скорость, с которой объекты, созданные поставщиком, могут доставляться клиентам.</span><span class="sxs-lookup"><span data-stu-id="dfef2-211">Maximum rate at which provider-created objects can be delivered to clients.</span></span> <span data-ttu-id="dfef2-212">Для поддержки разностных резервных копий между поставщиками и клиентами Инструментарий WMI хранит объекты в очередях перед их доставкой потребителям.</span><span class="sxs-lookup"><span data-stu-id="dfef2-212">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="dfef2-213">Для повышения эффективности потребители должны собираются объекты в темпе, соответствующем поставщику.</span><span class="sxs-lookup"><span data-stu-id="dfef2-213">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="dfef2-214">Если память, удерживаемая несобранными объектами, достигает **ловсрешолдонобжектс**, WMI замедляет добавление новых объектов в очередь.</span><span class="sxs-lookup"><span data-stu-id="dfef2-214">If the memory held by uncollected objects reaches **LowThresholdOnObjects**, then WMI slows down the addition of new objects into the queue.</span></span> <span data-ttu-id="dfef2-215">Если несобранные события продолжают накапливаться, а максимальное время ожидания доставки событий в **максваитонклиентобжектс** достигается в то время, когда используемая память находится в значении **хигхсрешолдонклиентобжектс**, Инструментарий WMI не принимает больше объектов от поставщиков и не возвращает клиенту **WBEM \_ \_ о нехватке \_ \_ памяти** для клиентов.</span><span class="sxs-lookup"><span data-stu-id="dfef2-215">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnClientObjects** is reached while the memory used is at the value in **HighThresholdOnClientObjects**, then WMI accepts no more objects from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-216">**хигхсрешолдоневентс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-216">**HighThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-217">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-218">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-218">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-219">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Высокая пороговое значение для событий"), [**единиц**](../wmisdk/standard-qualifiers.md) ("событий в секунду")</span><span class="sxs-lookup"><span data-stu-id="dfef2-219">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|High Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-220">Максимальная скорость доставки событий клиентам.</span><span class="sxs-lookup"><span data-stu-id="dfef2-220">Maximum rate at which events are to be delivered to clients.</span></span> <span data-ttu-id="dfef2-221">Для поддержки разностных резервных копий между поставщиками и клиентами события очередей WMI перед доставкой их клиентам.</span><span class="sxs-lookup"><span data-stu-id="dfef2-221">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="dfef2-222">Для повышения эффективности потребители должны собираются события в темпе, соответствующем поставщику.</span><span class="sxs-lookup"><span data-stu-id="dfef2-222">For more efficiency, consumers must collect the events at a pace that matches the provider.</span></span> <span data-ttu-id="dfef2-223">Если память, удерживаемая несобранными событиями, достигает **ловсрешолдонобжектс**, WMI замедляет добавление новых событий в очередь.</span><span class="sxs-lookup"><span data-stu-id="dfef2-223">If the memory held by uncollected events reaches **LowThresholdOnObjects**, then WMI slows down the addition of new events into the queue.</span></span> <span data-ttu-id="dfef2-224">Если несобранные события продолжают накапливаться, а максимальное ожидание доставки событий в **максваитоневентс** достигается в то время, когда используемая память находится на значении в **хигхсрешолдоневентс**, WMI не принимает больше событий от поставщиков и не возвращает **WBEM по \_ \_ нехватке \_ \_ памяти** клиентам.</span><span class="sxs-lookup"><span data-stu-id="dfef2-224">If uncollected events continue to accumulate and the maximum wait to deliver events in **MaxWaitOnEvents** is reached while the memory used is at the value in **HighThresholdOnEvents**, WMI accepts no more events from providers and returns **WBEM\_E\_OUT\_OF\_MEMORY** to the clients.</span></span>

> [!Note]  
> <span data-ttu-id="dfef2-225">Регулирование выполняется только для постоянных потребителей событий, поэтому временные потребители не должны ждать регулирования при резервном копировании событий в очереди внутренних событий WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-225">Throttling is only done for Permanent Event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="dfef2-226">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-226">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-227">**HKey \_ Локальное \_** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM**, \\ **\| Высокая пороговое значение для клиентских объектов (B)**    </span><span class="sxs-lookup"><span data-stu-id="dfef2-227">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-228">**InstallationDirectory**</span><span class="sxs-lookup"><span data-stu-id="dfef2-228">**InstallationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-229">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-230">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-231">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| Installation Directory")</span><span class="sxs-lookup"><span data-stu-id="dfef2-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|Installation Directory")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-232">Путь к каталогу, в который было установлено программное обеспечение WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-232">Directory path where the WMI software has been installed.</span></span> <span data-ttu-id="dfef2-233">Расположение по умолчанию — \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="dfef2-233">The default location is \\System32\\Wbem.</span></span>

<span data-ttu-id="dfef2-234">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-234">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-235">**HKey \_ \_** \\  \\  \\ **\| Каталог установки Microsoft WBEM** по локальному компьютеру</span><span class="sxs-lookup"><span data-stu-id="dfef2-235">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|Installation Directory**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-236">**ластстартуфеаппреаллокатион**</span><span class="sxs-lookup"><span data-stu-id="dfef2-236">**LastStartupHeapPreallocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-237">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-239">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| ластстартуфеаппреаллокатион"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="dfef2-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-240">Размер предварительно выделенной кучи, созданной WMI во время инициализации.</span><span class="sxs-lookup"><span data-stu-id="dfef2-240">Size of the pre-allocated heap created by WMI during initialization.</span></span>

<span data-ttu-id="dfef2-241">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-241">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-242">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM \| CIMOM \| ластстартуфеаппреаллокатион**</span><span class="sxs-lookup"><span data-stu-id="dfef2-242">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|LastStartupHeapPreallocation**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-243">**логгингдиректори**</span><span class="sxs-lookup"><span data-stu-id="dfef2-243">**LoggingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-244">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-245">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-245">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-246">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging Directory")</span><span class="sxs-lookup"><span data-stu-id="dfef2-246">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging Directory")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-247">Путь к каталогу, который содержит расположение файлов системного журнала WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-247">Directory path that contains the location of the WMI system log files.</span></span>

<span data-ttu-id="dfef2-248">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-248">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-249">**HKey \_ Каталог программы локального \_ компьютера** для \\  \\  \\ **\| \| ведения журнала Microsoft WBEM CIMOM**</span><span class="sxs-lookup"><span data-stu-id="dfef2-249">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging Directory**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-250">**LoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="dfef2-250">**LoggingLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-251">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-251">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-252">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-252">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-253">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Logging")</span><span class="sxs-lookup"><span data-stu-id="dfef2-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Logging")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-254">Включение ведения журнала событий и уровня детализации используемого журнала.</span><span class="sxs-lookup"><span data-stu-id="dfef2-254">Enabling of event logging and the verbosity level of logging used.</span></span>

<span data-ttu-id="dfef2-255">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-255">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-256">**HKey \_ \_** \\  \\  \\ **\| \| Ведение журнала Microsoft WBEM CIMOM** по локальному компьютеру</span><span class="sxs-lookup"><span data-stu-id="dfef2-256">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Logging**</span></span>

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="dfef2-257">**Выкл** . (0)</span><span class="sxs-lookup"><span data-stu-id="dfef2-257">**Off** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

<span data-ttu-id="dfef2-258">**Ведение журнала ошибок** (1)</span><span class="sxs-lookup"><span data-stu-id="dfef2-258">**Error logging** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

<span data-ttu-id="dfef2-259">**Подробное ведение журнала ошибок** (2)</span><span class="sxs-lookup"><span data-stu-id="dfef2-259">**Verbose Error logging** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="dfef2-260">**ловсрешолдонклиентобжектс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-260">**LowThresholdOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-261">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-261">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-262">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-263">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM, \\ \\ \| низкое пороговое значение для клиентских объектов"), [**единиц**](../wmisdk/standard-qualifiers.md) ("объектов в секунду")</span><span class="sxs-lookup"><span data-stu-id="dfef2-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Client Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-264">Скорость, с которой WMI начинает замедлять создание новых объектов, создаваемых для клиентов.</span><span class="sxs-lookup"><span data-stu-id="dfef2-264">Rate at which WMI starts to slow the creation of new objects created for clients.</span></span> <span data-ttu-id="dfef2-265">Для поддержки разностных резервных копий между поставщиками и клиентами Инструментарий WMI хранит объекты в очередях перед их доставкой потребителям.</span><span class="sxs-lookup"><span data-stu-id="dfef2-265">To accommodate speed differentials between providers and clients, WMI holds objects in queues before delivering them to consumers.</span></span> <span data-ttu-id="dfef2-266">Для повышения эффективности потребители должны собираются объекты в темпе, соответствующем поставщику.</span><span class="sxs-lookup"><span data-stu-id="dfef2-266">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="dfef2-267">Если скорость запросов для объектов достигает **ловсрешолдонклиентобжектс**, WMI постепенно замедляет создание новых объектов в соответствии с частотой использования клиента.</span><span class="sxs-lookup"><span data-stu-id="dfef2-267">If the rate of requests for objects reaches **LowThresholdOnClientObjects**, then WMI gradually slows down the creation of new objects to match the client's rate of use.</span></span> <span data-ttu-id="dfef2-268">Это замедление начинается, когда скорость создания объектов превышает значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="dfef2-268">This slowdown starts when the rate at which objects are being created exceeds the value of this property.</span></span> <span data-ttu-id="dfef2-269">См. **хигхсрешолдонклиентобжектс**.</span><span class="sxs-lookup"><span data-stu-id="dfef2-269">See **HighThresholdOnClientObjects**.</span></span>

<span data-ttu-id="dfef2-270">Это свойство отражает значение реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-270">This property reflects the registry value.</span></span>

<span data-ttu-id="dfef2-271">**Ключ \_ Локальное \_** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM**, \\ **\| Высокая пороговое значение для клиентских объектов (B)**    </span><span class="sxs-lookup"><span data-stu-id="dfef2-271">**KEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects (B)**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-272">**ловсрешолдоневентс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-272">**LowThresholdOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-274">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-274">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-275">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| низкая пороговое значение для событий"), [**единиц**](../wmisdk/standard-qualifiers.md) ("событий в секунду")</span><span class="sxs-lookup"><span data-stu-id="dfef2-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Low Threshold On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("events per second")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-276">Скорость, с которой WMI начинает замедлять доставку новых событий.</span><span class="sxs-lookup"><span data-stu-id="dfef2-276">Rate at which WMI starts to slow the delivery of new events.</span></span> <span data-ttu-id="dfef2-277">Для поддержки разностных резервных копий между поставщиками и клиентами события очередей WMI перед доставкой их клиентам.</span><span class="sxs-lookup"><span data-stu-id="dfef2-277">To accommodate speed differentials between providers and clients, WMI queues events before delivering them to consumers.</span></span> <span data-ttu-id="dfef2-278">Для повышения эффективности потребители должны собираются объекты в темпе, соответствующем поставщику.</span><span class="sxs-lookup"><span data-stu-id="dfef2-278">For more efficiency, consumers must collect the objects at a pace that matches the provider.</span></span> <span data-ttu-id="dfef2-279">Если очередь выходит за пределы контроля, регулирование WMI — замедляет работу, а доставка событий постепенно соответствует частоте клиента.</span><span class="sxs-lookup"><span data-stu-id="dfef2-279">If the queue grows out of control, WMI throttles—slows down—the delivery of events gradually to align with the client rate.</span></span> <span data-ttu-id="dfef2-280">Это замедление начинается, когда частота создания событий превышает значение этого свойства.</span><span class="sxs-lookup"><span data-stu-id="dfef2-280">This slowdown starts when the rate at which events are generated exceeds the value of this property.</span></span> <span data-ttu-id="dfef2-281">См. **хигхсрешолдоневентс**.</span><span class="sxs-lookup"><span data-stu-id="dfef2-281">See **HighThresholdOnEvents**.</span></span>

> [!Note]  
> <span data-ttu-id="dfef2-282">Регулирование выполняется только для постоянных потребителей событий, поэтому временные потребители не должны ждать регулирования при резервном копировании событий в очереди внутренних событий WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-282">Throttling is only done for permanent event consumers, so temporary consumers should not expect throttling when events get backed up in the WMI internal event queue.</span></span>

 

<span data-ttu-id="dfef2-283">Это свойство отражает значение реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-283">This property reflects the registry value.</span></span>

<span data-ttu-id="dfef2-284">**HKey \_ Локальное \_** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM**, \\ **\| Высокая пороговое значение для клиентских объектов {B}**    </span><span class="sxs-lookup"><span data-stu-id="dfef2-284">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|High Threshold On Client Objects {B}**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-285">**макслогфилесизе**</span><span class="sxs-lookup"><span data-stu-id="dfef2-285">**MaxLogFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-286">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-286">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-287">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-288">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| файл журнала максимальный размер"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")</span><span class="sxs-lookup"><span data-stu-id="dfef2-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Log File Max Size"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-289">Максимальный размер файлов журналов, создаваемых службой WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-289">Maximum size of the log files produced by the WMI service.</span></span>

<span data-ttu-id="dfef2-290">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-290">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-291">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера. \\  \\ **\| файл журнала Microsoft WBEM CIMOM \| максимальный размер**</span><span class="sxs-lookup"><span data-stu-id="dfef2-291">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|Log File Max Size**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-292">**максваитонклиентобжектс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-292">**MaxWaitOnClientObjects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-293">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-293">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-294">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-294">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-295">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM, \\ \\ \| Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="dfef2-295">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-296">Время, в течение которого созданный объект ожидает использования клиентом до его удаления, и возвращается значение ошибки.</span><span class="sxs-lookup"><span data-stu-id="dfef2-296">Amount of time a newly created object waits to be used by the client before it is discarded and an error value is returned.</span></span> <span data-ttu-id="dfef2-297">Это свойство взаимодействует с свойствами **ловсрешолдонклиентобжектс** и **хигхсрешолдонклиентобжектс** для регулирования — замедляется — доставка объектов потребителям, когда потребитель получает объекты слишком медленно.</span><span class="sxs-lookup"><span data-stu-id="dfef2-297">This property interacts with the **LowThresholdOnClientObjects** and **HighThresholdOnClientObjects** properties to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-298">**максваитоневентс**</span><span class="sxs-lookup"><span data-stu-id="dfef2-298">**MaxWaitOnEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-299">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dfef2-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-300">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dfef2-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-301">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM, \\ \\ \| Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="dfef2-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\\\\CIMOM\|Max Wait On Events"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-302">Время, в течение которого событие, отправленное клиенту, помещается в очередь перед отброшенным.</span><span class="sxs-lookup"><span data-stu-id="dfef2-302">Amount of time for which an event sent to a client is queued before being discarded.</span></span> <span data-ttu-id="dfef2-303">Это свойство interacts0 с **ловсрешолдоневентс** и **хигхсрешолдоневентс** для регулирования — замедляется — доставка объектов потребителям, когда потребитель получает объекты слишком медленно.</span><span class="sxs-lookup"><span data-stu-id="dfef2-303">This property interacts0 with **LowThresholdOnEvents** and **HighThresholdOnEvents** to throttle—slow down—the delivery of objects to consumers when the consumer is receiving the objects too slowly.</span></span>

<span data-ttu-id="dfef2-304">Это свойство отражает значение реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-304">This property reflects the registry value.</span></span>

<span data-ttu-id="dfef2-305">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **Microsoft** \\ **WBEM**, \\ **\| Максимальное время ожидания событий (МС)**    </span><span class="sxs-lookup"><span data-stu-id="dfef2-305">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\    **CIMOM\|Max Wait On Events (ms)**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-306">**мофселфинсталлдиректори**</span><span class="sxs-lookup"><span data-stu-id="dfef2-306">**MofSelfInstallDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-309">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")</span><span class="sxs-lookup"><span data-stu-id="dfef2-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\WBEM\|MOF Self-Install Directory")</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-310">Путь к каталогу для приложений, которые устанавливают MOF-файлы в репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-310">Directory path for applications that install MOF files to the WMI repository.</span></span> <span data-ttu-id="dfef2-311">Инструментарий WMI автоматически компилирует все MOF-файлы, размещенные в этом каталоге, и, в зависимости от его успешности, перемещает MOF в подкаталог, помеченный как хороший или плохой.</span><span class="sxs-lookup"><span data-stu-id="dfef2-311">WMI automatically compiles any MOF files placed in this directory and, depending on its success, moves the MOF to a subdirectory labeled good or bad.</span></span> <span data-ttu-id="dfef2-312">Если \# включена команда [pragma автосохранения](../wmisdk/pragma-autorecover.md) , полное имя файла добавляется в список **ауторековермофс** , используемый при инициализации или восстановлении репозитория WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-312">If the \# [pragma autorecover](../wmisdk/pragma-autorecover.md) command is included, the fully qualified file name is added to the **AutorecoverMofs** list used when WMI is initializing or recovering the repository.</span></span> <span data-ttu-id="dfef2-313">Этот список определяет порядок, в котором компилируются MOF.</span><span class="sxs-lookup"><span data-stu-id="dfef2-313">The list determines the order in which MOFs are compiled.</span></span>

<span data-ttu-id="dfef2-314">Это свойство отражает значение в разделе реестра.</span><span class="sxs-lookup"><span data-stu-id="dfef2-314">This property reflects the value in the registry key.</span></span>

<span data-ttu-id="dfef2-315">**HKey \_ По локального \_ компьютера** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM \| \| MOF Self = каталог установки**</span><span class="sxs-lookup"><span data-stu-id="dfef2-315">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM\|CIMOM\|MOF Self=Install Directory**</span></span>

</dd> <dt>

<span data-ttu-id="dfef2-316">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="dfef2-316">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dfef2-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dfef2-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dfef2-318">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dfef2-319">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="dfef2-319">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="dfef2-320">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="dfef2-320">Identifier by which the current object is known.</span></span>

<span data-ttu-id="dfef2-321">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="dfef2-321">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dfef2-322">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dfef2-322">Remarks</span></span>

<span data-ttu-id="dfef2-323">Класс **Win32 \_ вмисеттинг** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="dfef2-323">The **Win32\_WMISetting** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span> <span data-ttu-id="dfef2-324">На компьютере может существовать только один экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="dfef2-324">Only one instance of this class can exist on a computer.</span></span>

<span data-ttu-id="dfef2-325">Знание того, как инструментарий WMI настроен на компьютере, может быть очень полезен при отладке скриптов или при устранении неполадок в самой службе WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-325">Knowing how WMI is configured on a computer can be very useful when you are debugging scripts or troubleshooting problems with the WMI service itself.</span></span> <span data-ttu-id="dfef2-326">Например, многие сценарии WMI написаны с учетом предположения, что корневой \\ CIMV2 является пространством имен по умолчанию на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfef2-326">For example, many WMI scripts are written under the assumption that root\\cimv2 is the default namespace on the target computer.</span></span> <span data-ttu-id="dfef2-327">В результате авторы сценариев, которым требуется доступ к классу в "root \\ CIMv2", часто не могут включить пространство имен в моникер объекта GetObject, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="dfef2-327">As a result, script writers who need to access a class in "Root\\CIMv2" often fail to include the namespace in the GetObject moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

<span data-ttu-id="dfef2-328">Если корневой \\ CIMV2 не является пространством имен по умолчанию на конечном компьютере, этот сценарий завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dfef2-328">If root\\cimv2 is not the default namespace on the target computer, this script will fail.</span></span> <span data-ttu-id="dfef2-329">Чтобы избежать этого, корневой CIMV2 пространства имен \\ необходимо добавить в моникер, как показано в следующем примере кода:</span><span class="sxs-lookup"><span data-stu-id="dfef2-329">To prevent this from happening, the namespace root\\cimv2 must be included in the moniker, as shown in the following code sample:</span></span>

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

<span data-ttu-id="dfef2-330">Если пространство имен по умолчанию на целевом компьютере отличается от пространства имен, предполагаемого сценарием, сценарий завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="dfef2-330">If the default namespace on the target computer is different from the namespace assumed by a script, the script will fail.</span></span> <span data-ttu-id="dfef2-331">Поверх этого пользователю будет присвоено неверное сообщение об ошибке "недопустимый класс".</span><span class="sxs-lookup"><span data-stu-id="dfef2-331">On top of that, the user will be presented with the somewhat misleading error message "Invalid class."</span></span> <span data-ttu-id="dfef2-332">В действительности, сбой не происходит из-за того, что класс является недопустимым, но не найден в пространстве имен по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dfef2-332">In truth, the failure is not because the class is invalid but because the class cannot be found in the default namespace.</span></span> <span data-ttu-id="dfef2-333">Это сложная проблема для устранения неполадок, так как вы, скорее всего, сможете исследовать возможные проблемы с классом, а не проблемы с пространством имен, которое было указано (или, в данном случае, не было).</span><span class="sxs-lookup"><span data-stu-id="dfef2-333">This is a difficult problem to troubleshoot, because you are likely to investigate possible problems with the class rather than problems with the namespace that was (or, in this case, was not) specified.</span></span>

<span data-ttu-id="dfef2-334">Для определения того, как инструментарий WMI настроен на компьютере, можно использовать класс **Win32 \_ вмисеттинг** .</span><span class="sxs-lookup"><span data-stu-id="dfef2-334">You can use the **Win32\_WMISetting** class to determine how WMI has been configured on a computer.</span></span> <span data-ttu-id="dfef2-335">Сведения о конфигурации, такие как пространство имен по умолчанию или номер построения WMI, могут быть полезны при устранении неполадок в сценариях.</span><span class="sxs-lookup"><span data-stu-id="dfef2-335">Configuration details such as the default namespace or the WMI build number can be useful in troubleshooting script problems.</span></span> <span data-ttu-id="dfef2-336">Эти параметры также предоставляют важную административную информацию, например, как или даже на том, что ошибки WMI регистрируются на компьютере и какие поставщики WMI будут автоматически перезагружены, если необходимо перестроить репозиторий WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-336">These settings also provide important administrative information such as how, or even whether, WMI errors are logged on a computer and which WMI providers will automatically be reloaded if you need to rebuild the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="dfef2-337">Примеры</span><span class="sxs-lookup"><span data-stu-id="dfef2-337">Examples</span></span>

<span data-ttu-id="dfef2-338">Пример кода VBScript для [изменения параметров WMI](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) в коллекции TechNet использует класс **Win32 \_ вмисеттинг** для настройки интервала резервного копирования WMI и уровня ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="dfef2-338">The [Modify WMI Settings](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to configure the WMI backup interval and logging level.</span></span>

<span data-ttu-id="dfef2-339">В [списке в примере кода VBScript пространства имен по умолчанию](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) в коллекции TechNet используется класс **Win32 \_ вмисеттинг** для извлечения и вывода текущего параметра WMI "пространство имен по умолчанию для сценариев".</span><span class="sxs-lookup"><span data-stu-id="dfef2-339">The [List the Default Namespace](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) VBScript code example on the TechNet Gallery uses the **Win32\_WMISetting** class to retrieve and display the current WMI "Default namespace for scripting" setting.</span></span>

<span data-ttu-id="dfef2-340">Пример кода VBScript [по пространству имен WMI по умолчанию](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) в коллекции TechNet использует свойство **аспскриптдефаултнамеспаце** , чтобы установить для параметра Namespace инструментария WMI "пространство имен по умолчанию для скриптов" значение "root \\ CIMV2".</span><span class="sxs-lookup"><span data-stu-id="dfef2-340">The [Modify the Default WMI Namespace](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) VBScript code example on the TechNet Gallery uses the **ASPScriptDefaultNamespace** property to set the WMI "Default namespace for scripting" setting to "root\\cimv2".</span></span>

<span data-ttu-id="dfef2-341">В [списке всех параметров WMI в](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) примере кода VBSCript используется ряд свойств в **Win32 \_ вмисеттинг** для возврата списка параметров WMI, настроенных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfef2-341">The [List All the WMI Settings](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) VBSCript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="dfef2-342">В примере кода JavaScript [сведения о параметрах WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) используется ряд свойств в **Win32 \_ вмисеттинг** для возврата списка параметров WMI, настроенных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfef2-342">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) JavaScript code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="dfef2-343">В примере кода Python [сведения о параметрах WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) используется ряд свойств в **Win32 \_ вмисеттинг** для возврата списка параметров WMI, настроенных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfef2-343">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) Python code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="dfef2-344">В примере кода РЕКСКС объекта [Information WMI List](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) используется ряд свойств в **Win32 \_ вмисеттинг** для возврата списка параметров WMI, настроенных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfef2-344">The [List WMI Setting Information](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) Object REXX code example uses a number of properties on **Win32\_WMISetting** to return a list of WMI settings configured on a computer.</span></span>

<span data-ttu-id="dfef2-345">В следующем примере кода VBScript показано, как получить версию инструментария WMI, работающего на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="dfef2-345">The following VBScript code example shows how to obtain the version of WMI running on the local computer.</span></span> <span data-ttu-id="dfef2-346">"Win32 \_ вмисеттинг = @" обозначает единственный экземпляр класса.</span><span class="sxs-lookup"><span data-stu-id="dfef2-346">The "Win32\_WMISetting=@" indicates the single instance of the class.</span></span> <span data-ttu-id="dfef2-347">Дополнительные сведения см. в разделе версии WMI.</span><span class="sxs-lookup"><span data-stu-id="dfef2-347">For more information, see WMI versions.</span></span>


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a><span data-ttu-id="dfef2-348">Требования</span><span class="sxs-lookup"><span data-stu-id="dfef2-348">Requirements</span></span>



| <span data-ttu-id="dfef2-349">Требование</span><span class="sxs-lookup"><span data-stu-id="dfef2-349">Requirement</span></span> | <span data-ttu-id="dfef2-350">Значение</span><span class="sxs-lookup"><span data-stu-id="dfef2-350">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfef2-351">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dfef2-351">Minimum supported client</span></span><br/> | <span data-ttu-id="dfef2-352">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfef2-352">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dfef2-353">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dfef2-353">Minimum supported server</span></span><br/> | <span data-ttu-id="dfef2-354">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfef2-354">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dfef2-355">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dfef2-355">Namespace</span></span><br/>                | <span data-ttu-id="dfef2-356">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dfef2-356">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dfef2-357">MOF</span><span class="sxs-lookup"><span data-stu-id="dfef2-357">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfef2-358"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfef2-358"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfef2-359">DLL</span><span class="sxs-lookup"><span data-stu-id="dfef2-359">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfef2-360"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfef2-360"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfef2-361">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dfef2-361">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfef2-362">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="dfef2-362">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="dfef2-363">Классы управления службами WMI</span><span class="sxs-lookup"><span data-stu-id="dfef2-363">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
