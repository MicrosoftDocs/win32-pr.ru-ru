---
description: '&Win32 \_ осрековериконфигуратион \# 8194; Класс WMI представляет типы данных, которые будут собраны из памяти при сбое операционной системы. Сюда входят сбои загрузки и сбои системы.'
ms.assetid: 0c8a2aeb-2fd9-44b7-8f91-d19afb8d2de6
ms.tgt_platform: multiple
title: Класс Win32_OSRecoveryConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OSRecoveryConfiguration
- Win32_OSRecoveryConfiguration.Caption
- Win32_OSRecoveryConfiguration.Description
- Win32_OSRecoveryConfiguration.SettingID
- Win32_OSRecoveryConfiguration.AutoReboot
- Win32_OSRecoveryConfiguration.DebugFilePath
- Win32_OSRecoveryConfiguration.DebugInfoType
- Win32_OSRecoveryConfiguration.ExpandedDebugFilePath
- Win32_OSRecoveryConfiguration.ExpandedMiniDumpDirectory
- Win32_OSRecoveryConfiguration.KernelDumpOnly
- Win32_OSRecoveryConfiguration.MiniDumpDirectory
- Win32_OSRecoveryConfiguration.Name
- Win32_OSRecoveryConfiguration.OverwriteExistingDebugFile
- Win32_OSRecoveryConfiguration.SendAdminAlert
- Win32_OSRecoveryConfiguration.WriteDebugInfo
- Win32_OSRecoveryConfiguration.WriteToSystemLog
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2371ba7ee449497e2d695e60d75c59454282d54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656014"
---
# <a name="win32_osrecoveryconfiguration-class"></a><span data-ttu-id="bb632-104">\_Класс Win32 осрековериконфигуратион</span><span class="sxs-lookup"><span data-stu-id="bb632-104">Win32\_OSRecoveryConfiguration class</span></span>

<span data-ttu-id="bb632-105"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ осрековериконфигуратион для Win32** представляет типы данных, которые будут собраны из памяти при сбое операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bb632-105">The **Win32\_OSRecoveryConfiguration** [WMI class](../wmisdk/retrieving-a-class.md) represents the types of information that will be gathered from memory when the operating system fails.</span></span> <span data-ttu-id="bb632-106">Сюда входят сбои загрузки и сбои системы.</span><span class="sxs-lookup"><span data-stu-id="bb632-106">This includes boot failures and system crashes.</span></span>

<span data-ttu-id="bb632-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bb632-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bb632-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="bb632-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb632-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb632-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4E8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OSRecoveryConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AutoReboot;
  string  DebugFilePath;
  uint32  DebugInfoType;
  string  ExpandedDebugFilePath;
  string  ExpandedMiniDumpDirectory;
  boolean KernelDumpOnly;
  string  MiniDumpDirectory;
  string  Name;
  boolean OverwriteExistingDebugFile;
  boolean SendAdminAlert;
  boolean WriteDebugInfo;
  boolean WriteToSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="bb632-110">Члены</span><span class="sxs-lookup"><span data-stu-id="bb632-110">Members</span></span>

<span data-ttu-id="bb632-111">Класс **Win32 \_ осрековериконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bb632-111">The **Win32\_OSRecoveryConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="bb632-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb632-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bb632-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="bb632-113">Properties</span></span>

<span data-ttu-id="bb632-114">Класс **Win32 \_ осрековериконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bb632-114">The **Win32\_OSRecoveryConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bb632-115">**Перезагрузка**</span><span class="sxs-lookup"><span data-stu-id="bb632-115">**AutoReboot**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-116">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb632-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-117">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-118">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| rereboot")</span><span class="sxs-lookup"><span data-stu-id="bb632-118">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-119">Во время операции восстановления система будет автоматически перезагружена.</span><span class="sxs-lookup"><span data-stu-id="bb632-119">System will automatically reboot during a recovery operation.</span></span>

</dd> <dt>

<span data-ttu-id="bb632-120">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="bb632-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb632-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb632-123">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="bb632-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bb632-124">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="bb632-124">Short textual description of the current object.</span></span>

<span data-ttu-id="bb632-125">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bb632-125">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb632-126">**дебугфилепас**</span><span class="sxs-lookup"><span data-stu-id="bb632-126">**DebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-129">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| DumpFile (")</span><span class="sxs-lookup"><span data-stu-id="bb632-129">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|DumpFile")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-130">Полный путь к файлу отладки.</span><span class="sxs-lookup"><span data-stu-id="bb632-130">Full path to the debug file.</span></span> <span data-ttu-id="bb632-131">После сбоя компьютера создается файл отладки с состоянием памяти компьютера.</span><span class="sxs-lookup"><span data-stu-id="bb632-131">A debug file is created with the memory state of the computer after a computer failure.</span></span>

<span data-ttu-id="bb632-132">Пример: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="bb632-132">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="bb632-133">**дебугинфотипе**</span><span class="sxs-lookup"><span data-stu-id="bb632-133">**DebugInfoType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bb632-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb632-136">Тип отладочной информации, записанной в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="bb632-136">Type of debugging information written to the log file.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="bb632-137">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="bb632-137">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Complete_memory_dump"></span><span id="complete_memory_dump"></span><span id="COMPLETE_MEMORY_DUMP"></span>

<span data-ttu-id="bb632-138">**Полный дамп памяти** (1)</span><span class="sxs-lookup"><span data-stu-id="bb632-138">**Complete memory dump** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Kernel_memory_dump"></span><span id="kernel_memory_dump"></span><span id="KERNEL_MEMORY_DUMP"></span>

<span data-ttu-id="bb632-139">**Дамп памяти ядра** (2)</span><span class="sxs-lookup"><span data-stu-id="bb632-139">**Kernel memory dump** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Small_memory_dump"></span><span id="small_memory_dump"></span><span id="SMALL_MEMORY_DUMP"></span>

<span data-ttu-id="bb632-140">**Малый дамп памяти** (3)</span><span class="sxs-lookup"><span data-stu-id="bb632-140">**Small memory dump** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bb632-141">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bb632-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb632-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bb632-144">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="bb632-144">Textual description of the current object.</span></span>

<span data-ttu-id="bb632-145">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bb632-145">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb632-146">**експандеддебугфилепас**</span><span class="sxs-lookup"><span data-stu-id="bb632-146">**ExpandedDebugFilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb632-149">Расширенная версия свойства **дебугфилепас** .</span><span class="sxs-lookup"><span data-stu-id="bb632-149">Expanded version of the **DebugFilePath** property.</span></span>

<span data-ttu-id="bb632-150">Пример: "C: \\ Windows \\ Memory. dmp"</span><span class="sxs-lookup"><span data-stu-id="bb632-150">Example: "C:\\Windows\\Memory.dmp"</span></span>

</dd> <dt>

<span data-ttu-id="bb632-151">**експандедминидумпдиректори**</span><span class="sxs-lookup"><span data-stu-id="bb632-151">**ExpandedMiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-153">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bb632-154">Расширенная версия свойства **минидумпдиректори** .</span><span class="sxs-lookup"><span data-stu-id="bb632-154">Expanded version of the **MiniDumpDirectory** property.</span></span>

<span data-ttu-id="bb632-155">Пример: "C: \\ \\ Малый дамп Windows"</span><span class="sxs-lookup"><span data-stu-id="bb632-155">Example: "C:\\Windows\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="bb632-156">**кернелдумпонли**</span><span class="sxs-lookup"><span data-stu-id="bb632-156">**KernelDumpOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-157">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb632-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-159">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| кернелдумпонли")</span><span class="sxs-lookup"><span data-stu-id="bb632-159">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|KernelDumpOnly")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-160">В файл журнала отладки будут записываться только отладочные данные ядра.</span><span class="sxs-lookup"><span data-stu-id="bb632-160">Only kernel debug information will be written to the debug log file.</span></span> <span data-ttu-id="bb632-161">Если **значение — true**, то только состояние ядра записывается в файл в случае сбоя системы.</span><span class="sxs-lookup"><span data-stu-id="bb632-161">If **TRUE**, then only the state of the kernel is written to a file in the event of a system failure.</span></span> <span data-ttu-id="bb632-162">Если задано **значение false**, система попытается зарегистрировать состояние памяти и все устройства, которые могут предоставлять сведения о системе при сбое.</span><span class="sxs-lookup"><span data-stu-id="bb632-162">If **FALSE**, the system will try to log the state of the memory, and any devices that can provide information about the system when it failed.</span></span>

</dd> <dt>

<span data-ttu-id="bb632-163">**минидумпдиректори**</span><span class="sxs-lookup"><span data-stu-id="bb632-163">**MiniDumpDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-165">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-166">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| минидумпдир")</span><span class="sxs-lookup"><span data-stu-id="bb632-166">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|MiniDumpDir")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-167">Каталог, в котором будут записываться и накапливаться небольшие файлы дампа памяти.</span><span class="sxs-lookup"><span data-stu-id="bb632-167">Directory where small memory dump files will be recorded and accumulated.</span></span>

<span data-ttu-id="bb632-168">Пример: "% systemRoot% \\ минидампа"</span><span class="sxs-lookup"><span data-stu-id="bb632-168">Example: "%systemRoot%\\MiniDump"</span></span>

</dd> <dt>

<span data-ttu-id="bb632-169">**Name**</span><span class="sxs-lookup"><span data-stu-id="bb632-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb632-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb632-172">Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="bb632-172">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-173">Имя этого экземпляра класса **\_ осрековериконфигуратион Win32** .</span><span class="sxs-lookup"><span data-stu-id="bb632-173">Identifying name for this instance of the **Win32\_OSRecoveryConfiguration** class.</span></span>

</dd> <dt>

<span data-ttu-id="bb632-174">**овервритиксистингдебугфиле**</span><span class="sxs-lookup"><span data-stu-id="bb632-174">**OverwriteExistingDebugFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-175">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb632-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-177">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| overwrite")</span><span class="sxs-lookup"><span data-stu-id="bb632-177">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|Overwrite")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-178">Новый файл отладки перезапишет существующий.</span><span class="sxs-lookup"><span data-stu-id="bb632-178">New debug file will overwrite an existing one.</span></span>

</dd> <dt>

<span data-ttu-id="bb632-179">**сендадминалерт**</span><span class="sxs-lookup"><span data-stu-id="bb632-179">**SendAdminAlert**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb632-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-182">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| сендалерт")</span><span class="sxs-lookup"><span data-stu-id="bb632-182">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|SendAlert")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-183">Предупреждающее сообщение будет отправлено системному администратору в случае сбоя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bb632-183">Alert message will be sent to the system administrator in the event of an operating system failure.</span></span>

</dd> <dt>

<span data-ttu-id="bb632-184">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="bb632-184">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="bb632-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb632-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bb632-187">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="bb632-187">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bb632-188">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="bb632-188">Identifier by which the current object is known.</span></span>

<span data-ttu-id="bb632-189">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bb632-189">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb632-190">**вритедебугинфо**</span><span class="sxs-lookup"><span data-stu-id="bb632-190">**WriteDebugInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-191">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb632-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-192">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-192">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-193">Квалификаторы: не [**рекомендуется**](../wmisdk/standard-wmi-qualifiers.md), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| крашдумпенаблед")</span><span class="sxs-lookup"><span data-stu-id="bb632-193">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|CrashDumpEnabled")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-194">Отладочная информация должна быть записана в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="bb632-194">Debugging information is to be written to a log file.</span></span>

</dd> <dt>

<span data-ttu-id="bb632-195">**вритетосистемлог**</span><span class="sxs-lookup"><span data-stu-id="bb632-195">**WriteToSystemLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bb632-196">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="bb632-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bb632-197">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="bb632-197">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bb632-198">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| LogEvent")</span><span class="sxs-lookup"><span data-stu-id="bb632-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|LogEvent")</span></span>
</dt> </dl>

<span data-ttu-id="bb632-199">События будут записываться в системный журнал.</span><span class="sxs-lookup"><span data-stu-id="bb632-199">Events will be written to a system log.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb632-200">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb632-200">Remarks</span></span>

<span data-ttu-id="bb632-201">Класс **Win32 \_ осрековериконфигуратион** является производным от [**\_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="bb632-201">The **Win32\_OSRecoveryConfiguration** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bb632-202">Требования</span><span class="sxs-lookup"><span data-stu-id="bb632-202">Requirements</span></span>



| <span data-ttu-id="bb632-203">Требование</span><span class="sxs-lookup"><span data-stu-id="bb632-203">Requirement</span></span> | <span data-ttu-id="bb632-204">Значение</span><span class="sxs-lookup"><span data-stu-id="bb632-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb632-205">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb632-205">Minimum supported client</span></span><br/> | <span data-ttu-id="bb632-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb632-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb632-207">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb632-207">Minimum supported server</span></span><br/> | <span data-ttu-id="bb632-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb632-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb632-209">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb632-209">Namespace</span></span><br/>                | <span data-ttu-id="bb632-210">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bb632-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bb632-211">MOF</span><span class="sxs-lookup"><span data-stu-id="bb632-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb632-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb632-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb632-213">DLL</span><span class="sxs-lookup"><span data-stu-id="bb632-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb632-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb632-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb632-215">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb632-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb632-216">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="bb632-216">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="bb632-217">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="bb632-217">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
