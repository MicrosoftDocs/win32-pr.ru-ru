---
description: Представляет компьютерную систему под Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Класс Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141167"
---
# <a name="win32_computersystem-class"></a><span data-ttu-id="d1e8d-103">\_Класс Win32 ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="d1e8d-103">Win32\_ComputerSystem class</span></span>

<span data-ttu-id="d1e8d-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ComputerSystem** представляет компьютер, работающий под Windows.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-104">The **Win32\_ComputerSystem** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a computer system running Windows.</span></span>

<span data-ttu-id="d1e8d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1e8d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1e8d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a><span data-ttu-id="d1e8d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d1e8d-107">Members</span></span>

<span data-ttu-id="d1e8d-108">Класс **Win32 \_ ComputerSystem** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1e8d-108">The **Win32\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="d1e8d-109">Методы</span><span class="sxs-lookup"><span data-stu-id="d1e8d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1e8d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1e8d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1e8d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d1e8d-111">Methods</span></span>

<span data-ttu-id="d1e8d-112">Класс **Win32 \_ ComputerSystem** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-112">The **Win32\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="d1e8d-113">Метод</span><span class="sxs-lookup"><span data-stu-id="d1e8d-113">Method</span></span>                                                                                          | <span data-ttu-id="d1e8d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d1e8d-114">Description</span></span>                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1e8d-115">**жоиндомаинорворкграуп**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-115">**JoinDomainOrWorkgroup**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | <span data-ttu-id="d1e8d-116">Добавляет компьютерную систему в домен или рабочую группу.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-116">Adds a computer system to a domain or workgroup.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="d1e8d-117">**Имени**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-117">**Rename**</span></span>](rename-method-in-class-win32-computersystem.md)                                   | <span data-ttu-id="d1e8d-118">Переименовывает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-118">Renames a local computer.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="d1e8d-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-119">**SetPowerState**</span></span>                                                                               | <span data-ttu-id="d1e8d-120">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-120">Not implemented.</span></span> <span data-ttu-id="d1e8d-121">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-121">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span><br/> |
| [<span data-ttu-id="d1e8d-122">**унжоиндомаинорворкграуп**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-122">**UnjoinDomainOrWorkgroup**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | <span data-ttu-id="d1e8d-123">Удаляет компьютерную систему из домена или рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-123">Removes a computer system from a domain or workgroup.</span></span><br/>                                                                                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="d1e8d-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1e8d-124">Properties</span></span>

<span data-ttu-id="d1e8d-125">Класс **Win32 \_ ComputerSystem** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-125">The **Win32\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1e8d-126">**админпассвордстатус**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-126">**AdminPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| админпассвордстатус")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|AdminPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-130">Параметры безопасности оборудования системы для состояния пароля администратора.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-130">System hardware security settings for administrator password status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1e8d-131">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-131">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1e8d-132">**Включено** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-132">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="d1e8d-133">**Не реализовано** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-133">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-134">**Неизвестно** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-134">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-135">**аутоматикманажедпажефиле**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-135">**AutomaticManagedPagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-137">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-139">Если **значение — true**, система управляет файлом подкачки.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-139">If **True**, the system manages the page file.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-140">**аутоматикресетбутоптион**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-140">**AutomaticResetBootOption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-141">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-141">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| rereboot")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SYSTEM\\\\CurrentControlSet\\\\Control\\\\CrashControl\|AutoReboot")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-144">Если задано **значение true**, то включен режим автоматической перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-144">If **True**, the automatic reset boot option is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-145">**аутоматикресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-145">**AutomaticResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-146">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-149">Если задано **значение true**, автоматический сброс включен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-149">If **True**, the automatic reset is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-150">**бутоптиононлимит**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-150">**BootOptionOnLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-153">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| возможности \| загрузки при ограничении")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-153">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilites\|Boot Option on Limit")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-154">Параметр загрузки имеет значение ON.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-154">Boot option limit is ON.</span></span> <span data-ttu-id="d1e8d-155">Определяет системное действие при достижении значения **ресетлимит** .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-155">Identifies the system action when the **ResetLimit** value is reached.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d1e8d-156">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-156">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="d1e8d-157">**Операционная система** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-157">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="d1e8d-158">**Системные служебные программы** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-158">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="d1e8d-159">Не **перезагружать** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-159">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-160">**бутоптиононватчдог**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-160">**BootOptionOnWatchDog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-161">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-163">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| возможностей \| загрузки")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-163">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Capabilities\|Boot Option")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-164">Тип действия перезагрузки после истечения времени таймера наблюдения.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-164">Type of reboot action after the time on the watchdog timer is elapsed.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d1e8d-165">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-165">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

<span data-ttu-id="d1e8d-166">**Операционная система** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-166">**Operating system** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

<span data-ttu-id="d1e8d-167">**Системные служебные программы** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-167">**System utilities** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

<span data-ttu-id="d1e8d-168">Не **перезагружать** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-168">**Do not reboot** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-169">**бутромсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-169">**BootROMSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-170">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-172">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-173">Если **значение — true**, указывает, поддерживается ли загрузочное ПЗУ.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-173">If **True**, indicates whether a boot ROM is supported.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-174">**бутстатус**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-174">**BootStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-175">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d1e8d-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-177">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 32. \| состояние загрузки системной информации \| ")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-177">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 32\|System Boot Information\|Boot Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-178">Состояние и дополнительные поля данных, которые указывают состояние загрузки.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-178">Status and Additional Data fields that identify the boot status.</span></span>

<span data-ttu-id="d1e8d-179">Это значение берется из элемента **состояние загрузки** в структуре **сведений о загрузке системы** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-179">This value comes from the **Boot Status** member of the **System Boot Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d1e8d-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-181">**бутупстате**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-181">**BootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-184">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ клеанбут")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)\|SM\_CLEANBOOT")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-185">Система запущена.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-185">System is started.</span></span> <span data-ttu-id="d1e8d-186">Безошибочная Загрузка обходит файлы запуска пользователей, также называемые SafeBoot.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-186">Fail-safe boot bypasses the user startup files also called SafeBoot.</span></span>

<span data-ttu-id="d1e8d-187">В следующем списке содержатся необходимые значения:</span><span class="sxs-lookup"><span data-stu-id="d1e8d-187">The following list contains the required values:</span></span>

<dl> <dd><span data-ttu-id="d1e8d-188">"Обычная загрузка"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-188">"Normal boot"</span></span></dd> <dd><span data-ttu-id="d1e8d-189">"Неудачно безопасный запуск"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-189">"Fail-safe boot"</span></span></dd> <dd><span data-ttu-id="d1e8d-190">"Безопасный режим с сетевой загрузкой"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-190">"Fail-safe with network boot"</span></span></dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

<span data-ttu-id="d1e8d-191">**Обычная загрузка** ("Обычная загрузка")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-191">**Normal boot** ("Normal boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

<span data-ttu-id="d1e8d-192">**Отказоустойчивая загрузка** ("неудачно безопасный запуск")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-192">**Fail-safe boot** ("Fail-safe boot")</span></span>


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

<span data-ttu-id="d1e8d-193">**Отказоустойчивость с сетевой загрузкой** ("отказоустойчивость с сетевой загрузкой")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-193">**Fail-safe with network boot** ("Fail-safe with network boot")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-194">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-194">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-195">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-197">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-197">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-198">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-198">Short description of the object a one-line string.</span></span>

<span data-ttu-id="d1e8d-199">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-199">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-200">**чассисбутупстате**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-200">**ChassisBootupState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-201">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-201">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-203">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3, \| загрузочное состояние")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-203">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Bootup State")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-204">Загрузка состояния корпуса.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-204">Boot up state of the chassis.</span></span>

<span data-ttu-id="d1e8d-205">Это значение берется из элемента **состояние загрузки** в структуре **корпуса или шасси** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-205">This value comes from the **Boot-up State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1e8d-206">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-206">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-207">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-207">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="d1e8d-208">**Безопасность** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-208">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d1e8d-209">**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-209">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d1e8d-210">**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-210">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="d1e8d-211">**Без возможности восстановления** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-211">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-212">**чассисскунумбер**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-212">**ChassisSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-215">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3 \| - \| номера SKU корпуса")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|Chassis\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-216">Номер SKU шасси или корпуса в виде строки.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-216">The chassis or enclosure SKU number as a string.</span></span>

<span data-ttu-id="d1e8d-217">Это значение берется из **номера SKU** в структуре **System корпуса или корпуса** в информации SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-217">This value comes from the **SKU Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d1e8d-218">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-218">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-219">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-219">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-222">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-222">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-223">Имя первого конкретного класса в цепочке наследования экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-223">Name of the first concrete class in the inheritance chain of an instance.</span></span> <span data-ttu-id="d1e8d-224">Это свойство можно использовать с другими свойствами класса для обнаружения всех экземпляров класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-224">You can use this property with other properties of the class to identify all instances of the class and its subclasses.</span></span>

<span data-ttu-id="d1e8d-225">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-225">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-226">**курренттимезоне**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-226">**CurrentTimeZone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-227">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-227">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-228">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-228">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-229">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| времени структуры времени \| [**часового \_ пояса \_**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-229">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Structures\|[**TIME\_ZONE\_INFORMATION**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information)\|Bias"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("minutes")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-230">Время, в течение которого единая система компьютера смещается со времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-230">Amount of time the unitary computer system is offset from Coordinated Universal Time (UTC).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-231">**дайлигхтинеффект**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-231">**DaylightInEffect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-232">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-232">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-234">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции времени Win32API \| [**жеттимезонеинформатион**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Time Functions\|[**GetTimeZoneInformation**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-235">Если задано **значение true**, режим летнего сбережения включен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-235">If **True**, the daylight savings mode is ON.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-236">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-236">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-237">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-239">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-239">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-240">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-240">Description of the object.</span></span>

<span data-ttu-id="d1e8d-241">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-241">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-242">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-242">**DNSHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-243">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-245">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| предполагался сбой getcomputernameex \| компутернамедншостнаме")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|GetComputerNameEx\|ComputerNameDnsHostname")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-246">Имя локального компьютера в соответствии с именем сервера доменных имен (DNS).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-246">Name of local computer according to the domain name server (DNS).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-247">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-247">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-248">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-249">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-250">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**вкста \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ ланграуп")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-250">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**WKSTA\_INFO\_100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100)\|wki100\_langroup")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-251">Имя домена, к которому принадлежит компьютер.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-251">Name of the domain to which a computer belongs.</span></span>

> [!Note]  
> <span data-ttu-id="d1e8d-252">Если компьютер не входит в домен, возвращается имя рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-252">If the computer is not part of a domain, then the name of the workgroup is returned.</span></span>

 

</dd> <dt>

<span data-ttu-id="d1e8d-253">**DomainRole**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-253">**DomainRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-254">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-254">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-255">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-256">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (DS) Structures \| [**дсроле \_ основной \_ домен \_ сведения \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**дсроле \_ Machine \_ Role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| мачинероле")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-256">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Directory Service (Ds) Structures\| [**DSROLE\_PRIMARY\_DOMAIN\_INFO\_BASIC**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic)\|[**DSROLE\_MACHINE\_ROLE**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role)\| MachineRole")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-257">Роль компьютера в назначенной Рабочей группе домена.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-257">Role of a computer in an assigned domain workgroup.</span></span> <span data-ttu-id="d1e8d-258">Доменная Рабочая группа — это коллекция компьютеров в одной сети.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-258">A domain workgroup is a collection of computers on the same network.</span></span> <span data-ttu-id="d1e8d-259">Например, свойство **DomainRole** может показывать, что компьютер является членом рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-259">For example, a **DomainRole** property may show that a computer is a member workstation.</span></span>

<span data-ttu-id="d1e8d-260">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-260">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

<span data-ttu-id="d1e8d-261">**Автономная рабочая станция** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-261">**Standalone Workstation** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

<span data-ttu-id="d1e8d-262">**Рядовая Рабочая станция** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-262">**Member Workstation** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

<span data-ttu-id="d1e8d-263">**Изолированный сервер** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-263">**Standalone Server** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

<span data-ttu-id="d1e8d-264">**Рядовой сервер** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-264">**Member Server** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="d1e8d-265">**Резервный контроллер домена** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-265">**Backup Domain Controller** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

<span data-ttu-id="d1e8d-266">**Основной контроллер домена** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-266">**Primary Domain Controller** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-267">**енабледайлигхтсавингстиме**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-267">**EnableDaylightSavingsTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-268">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-269">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-269">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-270">Включает летнее время (DST) на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-270">Enables daylight savings time (DST) on a computer.</span></span> <span data-ttu-id="d1e8d-271">Значение **true** указывает, что системное время меняется на час вперед или назад при начале или ОКОНЧАНИи летнего времени.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-271">A value of **True** indicates that the system time changes to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="d1e8d-272">Значение **false** указывает, что системное время не меняется на час впереди или после окончания летнего времени.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-272">A value of **False** indicates that the system time does not change to an hour ahead or behind when DST starts or ends.</span></span> <span data-ttu-id="d1e8d-273">Значение **null** указывает, что состояние DST неизвестно в системе.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-273">A value of **NULL** indicates that the DST status is unknown on a system.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-274">**фронтпанелресетстатус**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-274">**FrontPanelResetStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-275">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-275">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-277">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| фронтпанелресетстатус")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|FrontPanelResetStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-278">В следующей таблице перечислены параметры безопасности оборудования для кнопки Сброс на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-278">The following table lists the hardware security settings for the reset button on a computer.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1e8d-279">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-279">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1e8d-280">**Включено** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-280">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="d1e8d-281">**Не реализовано** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-281">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-282">**Неизвестно** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-282">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-283">**хипервисорпресент**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-283">**HypervisorPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-284">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-286">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-286">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-287">Если задано **значение true**, низкоуровневая оболочка.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-287">If **True**, a hypervisor is present.</span></span>

<span data-ttu-id="d1e8d-288">**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 8 и Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-288">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8 and Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-289">**инфраредсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-289">**InfraredSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-290">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-292">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-292">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-293">**Значение true** показывает, что инфракрасный порт (IR) существует в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-293">If **True**, an infrared (IR) port exists on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-294">**инитиаллоадинфо**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-294">**InitialLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-295">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-295">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-296">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-297">Данные, необходимые для поиска устройства начальной загрузки или службы загрузки для запроса запуска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-297">Data required to find the initial load device or boot service to request that the operating system start up.</span></span>

<span data-ttu-id="d1e8d-298">Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-298">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<span data-ttu-id="d1e8d-299">**Windows Server 2008 R2:** Это свойство доступно, но пусто.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-299">**Windows Server 2008 R2:** This property is available, but empty.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-301">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-303">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-304">Объект установлен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-304">Object is installed.</span></span> <span data-ttu-id="d1e8d-305">Для объекта не требуется значение, указывающее, что он установлен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-305">An object does not need a value to indicate that it is installed.</span></span>

<span data-ttu-id="d1e8d-306">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-307">**кэйбоардпассвордстатус**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-307">**KeyboardPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-308">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-308">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-310">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| кэйбоардпассвордстатус")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-310">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|KeyboardPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-311">Параметры безопасности оборудования системы для состояния пароля клавиатуры.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-311">System hardware security settings for Keyboard Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1e8d-312">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-312">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1e8d-313">**Включено** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-313">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="d1e8d-314">**Не реализовано** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-314">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-315">**Неизвестно** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-315">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-316">**ластлоадинфо**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-316">**LastLoadInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-317">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-317">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-318">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-318">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-319">Элемент массива свойства **инитиаллоадинфо** , содержащего данные для запуска загруженной операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-319">Array entry of the **InitialLoadInfo** property that contains the data to start the loaded operating system.</span></span>

<span data-ttu-id="d1e8d-320">Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-320">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-321">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-321">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-322">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-323">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-324">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| поставщик сведений о системе SMBIOS Type 1 \| )"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-324">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-325">Имя изготовителя компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-325">Name of a computer manufacturer.</span></span>

<span data-ttu-id="d1e8d-326">Пример: Adventure Works</span><span class="sxs-lookup"><span data-stu-id="d1e8d-326">Example: Adventure Works</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-327">**Модель**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-327">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-328">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-329">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-330">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 1 \| системная информация \| Название продукта")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-330">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Product Name")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-331">Название продукта, которое изготовитель передает компьютеру.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-331">Product name that a manufacturer gives to a computer.</span></span> <span data-ttu-id="d1e8d-332">Это свойство должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-332">This property must have a value.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-333">**Name**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-333">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-335">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-336">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-336">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-337">Ключ экземпляра [**\_ системы CIM**](cim-system.md) в корпоративной среде.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-337">Key of a [**CIM\_System**](cim-system.md) instance in an enterprise environment.</span></span>

<span data-ttu-id="d1e8d-338">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-339">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-339">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-342">Значение **имени** системы компьютера, создаваемое автоматически.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-342">Computer system **Name** value that is generated automatically.</span></span> <span data-ttu-id="d1e8d-343">Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) и его производные являются объектами верхнего уровня модель CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-343">The [**CIM\_ComputerSystem**](cim-computersystem.md) object and its derivatives are top-level objects of the Common Information Model (CIM).</span></span> <span data-ttu-id="d1e8d-344">Они предоставляют область для нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-344">They provide the scope for several components.</span></span> <span data-ttu-id="d1e8d-345">Требуются [**уникальные \_ системные ключи CIM**](cim-system.md) , но можно определить эвристику для создания имени **CIM \_ ComputerSystem** , создающего то же имя, и оно не зависит от протокола обнаружения.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-345">Unique [**CIM\_System**](cim-system.md) keys are required, but you can define a heuristic to create the **CIM\_ComputerSystem** name that generates the same name, and is independent from the discovery protocol.</span></span> <span data-ttu-id="d1e8d-346">Это предотвращает проблемы с инвентаризацией и управлением, когда один и тот же ресурс или сущность обнаруживается несколько раз, но не может быть разрешена в один объект.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-346">This prevents inventory and management problems when the same asset or entity is discovered multiple times, but cannot be resolved to one object.</span></span> <span data-ttu-id="d1e8d-347">Рекомендуется использовать эвристический подход, но это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-347">Using a heuristic is recommended, but not required.</span></span>

<span data-ttu-id="d1e8d-348">Эвристический алгоритм описан в спецификации общей модели CIM V2 и предполагает, что для определения и назначения имени используются документированные правила.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-348">The heuristic is outlined in the CIM V2 Common Model specification, and assumes that the documented rules are used to determine and assign a name.</span></span> <span data-ttu-id="d1e8d-349">Список значений **намеформат** определяет порядок назначения имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-349">The **NameFormat** values list defines the order to assign a computer system name.</span></span> <span data-ttu-id="d1e8d-350">Несколько правил сопоставляются с одним и тем же значением.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-350">Several rules map to the same value.</span></span>

<span data-ttu-id="d1e8d-351">Значение [**\_ имени системы CIM**](cim-computersystem.md) , которое вычисляется с помощью эвристики, является ключевым значением в системе.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-351">The [**CIM\_ComputerSystem Name**](cim-computersystem.md) value that is calculated using the heuristic is the key value of the system.</span></span> <span data-ttu-id="d1e8d-352">Однако используйте псевдонимы, чтобы назначить другое имя для **CIM \_ ComputerSystem**, которое может быть более уникальным для вашей компании.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-352">However, use aliases to assign a different name for **CIM\_ComputerSystem**, which can be more unique to your company.</span></span>

<span data-ttu-id="d1e8d-353">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-353">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="d1e8d-354">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d1e8d-354">Values include the following:</span></span>

<dt>

<span id="IP"></span><span id="ip"></span>

<span data-ttu-id="d1e8d-355">**IP-адрес** ("IP")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-355">**IP** ("IP")</span></span>


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

<span data-ttu-id="d1e8d-356">**Набрать номер** ("набрать")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-356">**Dial** ("Dial")</span></span>


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

<span data-ttu-id="d1e8d-357">**HID** (HID)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-357">**HID** ("HID")</span></span>


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

<span data-ttu-id="d1e8d-358">**НВА** ("НВА")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-358">**NWA** ("NWA")</span></span>


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

<span data-ttu-id="d1e8d-359">**Хва** ("Хва")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-359">**HWA** ("HWA")</span></span>


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

<span data-ttu-id="d1e8d-360">**X25** ("x25")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-360">**X25** ("X25")</span></span>


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

<span data-ttu-id="d1e8d-361">**ISDN** (ISDN)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-361">**ISDN** ("ISDN")</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="d1e8d-362">**IPX** ("IPX")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-362">**IPX** ("IPX")</span></span>


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

<span data-ttu-id="d1e8d-363">**ДКК** ("ДКК")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-363">**DCC** ("DCC")</span></span>


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

<span data-ttu-id="d1e8d-364">**ICD** ("ICD")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-364">**ICD** ("ICD")</span></span>


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

<span data-ttu-id="d1e8d-365">**E. 164** ("E. 164")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-365">**E.164** ("E.164")</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="d1e8d-366">**SNA** ("SNA")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-366">**SNA** ("SNA")</span></span>


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

<span data-ttu-id="d1e8d-367">**OID/OSI** ("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-367">**OID/OSI** ("OID/OSI")</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1e8d-368">**Другое** ("другое")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-368">**Other** ("Other")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-369">**нетворксервермодинаблед**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-369">**NetworkServerModeEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-370">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-370">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-372">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| ОКП \_ Type \_ Server")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-372">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Network Management Structures\|[**SERVER\_INFO\_101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101)\|sv101\_type\|SV\_TYPE\_SERVER")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-373">**Значение true** показывает, что режим сетевого сервера включен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-373">If **True**, the network Server Mode is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-374">**нумберофлогикалпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-374">**NumberOfLogicalProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-375">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-377">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-377">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-378">Число логических процессоров, доступных на компьютере.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-378">Number of logical processors available on the computer.</span></span>

<span data-ttu-id="d1e8d-379">Можно использовать **нумберофлогикалпроцессорс** и **NumberOfProcessors** , чтобы определить, является ли компьютер технологией Hyper-Threading.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-379">You can use **NumberOfLogicalProcessors** and **NumberOfProcessors** to determine if the computer is hyperthreading.</span></span> <span data-ttu-id="d1e8d-380">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d1e8d-380">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-381">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-381">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-382">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-382">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-383">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-384">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| двнумберофпроцессорс")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-384">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|dwNumberOfProcessors")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-385">Число физических процессоров, доступных в данный момент в системе.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-385">Number of physical processors currently available on a system.</span></span> <span data-ttu-id="d1e8d-386">Это число включенных в систему процессоров, которые не включают отключенные процессоры.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-386">This is the number of enabled processors for a system, which does not include the disabled processors.</span></span> <span data-ttu-id="d1e8d-387">Если компьютерная система содержит два физических процессора, каждый из которых содержит два логических процессора, значение **NumberOfProcessors** равно 2, а **нумберофлогикалпроцессорс** — 4.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-387">If a computer system has two physical processors each containing two logical processors, then the value of **NumberOfProcessors** is 2 and **NumberOfLogicalProcessors** is 4.</span></span> <span data-ttu-id="d1e8d-388">Процессоры могут быть многоядерными, или же они могут быть процессорами технологии Hyper.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-388">The processors may be multicore or they may be hyperthreading processors.</span></span> <span data-ttu-id="d1e8d-389">Дополнительные сведения см. в подразделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="d1e8d-389">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-390">**оемлогобитмап**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-390">**OEMLogoBitmap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-391">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-391">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-393">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-394">Список данных для точечного рисунка, создаваемого изготовителем оборудования (OEM).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-394">List of data for a bitmap that the original equipment manufacturer (OEM) creates.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-395">**оемстрингаррай**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-395">**OEMStringArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-396">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-396">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-397">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-398">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 11: \| строки OEM")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-398">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 11\|OEM Strings")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-399">Список произвольных строк, определяемых изготовителем оборудования.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-399">List of free-form strings that an OEM defines.</span></span> <span data-ttu-id="d1e8d-400">Например, изготовитель оборудования определяет номера частей для справочных документов по системе, контактные данные производителя и т. д.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-400">For example, an OEM defines the part numbers for system reference documents, manufacturer contact information, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-401">**партофдомаин**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-401">**PartOfDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-402">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-402">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-403">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-403">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-404">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-404">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-405">**Значение true** показывает, что компьютер является частью домена.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-405">If **True**, the computer is part of a domain.</span></span> <span data-ttu-id="d1e8d-406">Если значение равно **null**, компьютер не находится в домене или состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-406">If the value is **NULL**, the computer is not in a domain or the status is unknown.</span></span> <span data-ttu-id="d1e8d-407">Если удалить компьютер из домена, значение будет **равно false**.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-407">If you remove the computer from a domain, the value becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-408">**паусеафтерресет**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-408">**PauseAfterReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-409">Тип данных: **sint64**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-409">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-411">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| timeout"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунд")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-411">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|Timeout"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-412">Временная задержка перед инициацией перезагрузки в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-412">Time delay before a reboot is initiated in milliseconds.</span></span> <span data-ttu-id="d1e8d-413">Он используется после системного цикла питания, локального или удаленного сброса системы и автоматического сброса системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-413">It is used after a system power cycle, local or remote system reset, and automatic system reset.</span></span> <span data-ttu-id="d1e8d-414">Значение 1 (минус единица) указывает на то, что значение приостановки неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-414">A value of  1 (minus one) indicates that the pause value is unknown.</span></span>

<span data-ttu-id="d1e8d-415">**Windows Vista:** Это свойство может возвращать неизвестное число.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-415">**Windows Vista:** This property may return an unknown number.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-416">**пксистемтипе**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-416">**PCSystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-417">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-417">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-419">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-419">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-420">Тип используемого компьютера, например портативный компьютер, Настольный компьютер или планшетный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-420">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="d1e8d-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>Не **указано** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-421"><span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="d1e8d-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Рабочий стол** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-422"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="d1e8d-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Мобильные устройства** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-423"><span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="d1e8d-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Рабочая станция** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-424"><span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="d1e8d-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Корпоративный сервер** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-425"><span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="d1e8d-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Сервер локальной** сети (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-426"><span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**SOHO Server** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-427">Небольшой офисный и домашний офисный сервер</span><span class="sxs-lookup"><span data-stu-id="d1e8d-427">Small Office and Home Office (SOHO) Server</span></span>

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="d1e8d-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Устройство PC** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-428"><span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="d1e8d-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Сервер производительности** (7)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-429"><span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="d1e8d-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (8)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-430"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-431">**пксистемтипикс**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-431">**PCSystemTypeEx**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-432">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-434">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-435">Тип используемого компьютера, например портативный компьютер, Настольный компьютер или планшетный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-435">Type of the computer in use, such as laptop, desktop, or Tablet.</span></span>

<span data-ttu-id="d1e8d-436">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 8.1 и Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-436">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 8.1 and Windows Server 2012 R2.</span></span>

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span data-ttu-id="d1e8d-437">Не **указано** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-437">**Unspecified** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="d1e8d-438">**Рабочий стол** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-438">**Desktop** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span data-ttu-id="d1e8d-439">**Мобильные устройства** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-439">**Mobile** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span data-ttu-id="d1e8d-440">**Рабочая станция** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-440">**Workstation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span data-ttu-id="d1e8d-441">**Корпоративный сервер** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-441">**Enterprise Server** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span data-ttu-id="d1e8d-442">**Сервер локальной** сети (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-442">**SOHO Server** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span data-ttu-id="d1e8d-443">**Устройство PC** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-443">**Appliance PC** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span data-ttu-id="d1e8d-444">**Сервер производительности** (7)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-444">**Performance Server** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

<span data-ttu-id="d1e8d-445">**Содержание** (8)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-445">**Slate** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="d1e8d-446">**Максимум** (9)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-446">**Maximum** (9)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-447">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-447">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-448">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d1e8d-448">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-450">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Элементы управления питанием системы DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-450">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-451">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-451">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="d1e8d-452">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-452">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-453"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d1e8d-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-454"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1e8d-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-455"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1e8d-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-456"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-457">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-457">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d1e8d-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-458"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-459">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-459">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d1e8d-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-460"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-461">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-461">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="d1e8d-462">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-462">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="d1e8d-463">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-463">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d1e8d-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-464"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-465">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-465">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d1e8d-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-466"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-467">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="d1e8d-467">Timed Power-On Supported</span></span>

<span data-ttu-id="d1e8d-468">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-468">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-469">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-469">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-470">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-470">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-471">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-471">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-472">Если **true**, устройство может управляться с помощью управления питанием, например, устройство может быть переведено в режим приостановки и т. д.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-472">If **True**, device can be power-managed, for example, a device can be put into suspend mode, and so on.</span></span> <span data-ttu-id="d1e8d-473">Это свойство не указывает, что функции управления питанием включены в настоящее время, но это означает, что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-473">This property does not indicate that power management features are enabled currently, but it does indicate that the logical device is capable of power management.</span></span>

<span data-ttu-id="d1e8d-474">Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-474">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-475">**поверонпассвордстатус**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-475">**PowerOnPasswordStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-476">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-476">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-477">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-477">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-478">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| поверонпассвордстатус")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-478">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 24\|Hardware Security Settings\|PowerOnPasswordStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-479">Параметры безопасности оборудования системы для Power-On состояние пароля.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-479">System hardware security settings for Power-On Password Status.</span></span>

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1e8d-480">**Отключено** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-480">**Disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1e8d-481">**Включено** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-481">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="d1e8d-482">**Не реализовано** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-482">**Not Implemented** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-483">**Неизвестно** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-483">**Unknown** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-484">**Установлен**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-484">**PowerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-485">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-485">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-486">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-486">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-487">Текущее состояние электропитания компьютера и связанной с ним операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-487">Current power state of a computer and its associated operating system.</span></span> <span data-ttu-id="d1e8d-488">Состояния энергосбережения имеют следующие значения: значение 4 (неизвестно) указывает, что система находится в режиме энергосбережения, но ее точное состояние в этом режиме неизвестно. 2 (режим низкого энергопотребления) указывает, что система находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности. 3 (в режиме ожидания) указывает, что система не работает, но ее можно быстро включить в полную мощность. и 7 (предупреждение) означает, что компьютерная система находится в состоянии предупреждения и режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-488">The power saving states have the following values: Value 4 (Unknown) indicates that the system is known to be in a power save mode, but its exact status in this mode is unknown; 2 (Low Power Mode) indicates that the system is in a power save state, but still functioning and may exhibit degraded performance; 3 (Standby) indicates that the system is not functioning, but could be brought to full power quickly; and 7 (Warning) indicates that the computer system is in a warning state and a power save mode.</span></span>

<span data-ttu-id="d1e8d-489">Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-489">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-490"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span data-ttu-id="d1e8d-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-491"><span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Full Power** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d1e8d-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-492"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d1e8d-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-493"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d1e8d-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-494"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d1e8d-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-495"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d1e8d-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-496"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d1e8d-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (7)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-497"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span data-ttu-id="d1e8d-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Энергосбережение **— режим гибернации** (8)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-498"><span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>**Power Save - Hibernate** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-499">Power Save Гибернация.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-499">Power save   hibernate.</span></span>

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span data-ttu-id="d1e8d-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Энергосбережение **— мягкое отключение** (9)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-500"><span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>**Power Save - Soft Off** (9)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-501">Энергосбережение с мягким отключением.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-501">Power save   soft off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-502">**поверсупплистате**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-502">**PowerSupplyState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-503">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-503">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-504">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-504">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-505">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3 \| системного корпуса или \| состояние источника питания корпуса")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-505">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Power Supply State")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-506">Состояние источника питания или поставляется при последней загрузке.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-506">State of the power supply or supplies when last booted.</span></span>

<span data-ttu-id="d1e8d-507">Это значение берется из элемента **состояния источника питания** в структуре **корпуса или шасси** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-507">This value comes from the **Power Supply State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d1e8d-508">В следующем списке указаны значения для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-508">The following list identifies the values for this property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1e8d-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-509"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-510"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="d1e8d-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Безопасность** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-511"><span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d1e8d-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-512"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d1e8d-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-513"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="d1e8d-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Без возможности восстановления** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-514"><span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Non-recoverable** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-515">Произошла неустранимая</span><span class="sxs-lookup"><span data-stu-id="d1e8d-515">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-516">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-516">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-517">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-518">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-518">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-519">Контактные данные для владельца первичной системы, например номер телефона, адрес электронной почты и т. д.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-519">Contact information for the primary system owner, for example, phone number, email address, and so on.</span></span>

<span data-ttu-id="d1e8d-520">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-520">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-521">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-521">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-522">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-523">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-524">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-524">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-525">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-525">Name of the primary system owner.</span></span>

<span data-ttu-id="d1e8d-526">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-526">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-527">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-527">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-528">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-529">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-529">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-530">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Security аппаратная безопасность \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-530">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-531">Если параметр включен, то значение равно 4, а единая система компьютера может быть сброшена с помощью кнопок включения и выключения.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-531">If enabled, the value is 4 and the unitary computer system can be reset using the power and reset buttons.</span></span> <span data-ttu-id="d1e8d-532">Если параметр отключен, значение равно 3, а сброс не разрешен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-532">If disabled, the value is 3, and a reset is not allowed.</span></span>

<span data-ttu-id="d1e8d-533">Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-533">This property is inherited from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1e8d-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-534"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-535"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d1e8d-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-536"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d1e8d-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-537"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="d1e8d-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Не реализовано** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-538"><span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Not Implemented** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d1e8d-539">Произошла неустранимая</span><span class="sxs-lookup"><span data-stu-id="d1e8d-539">Nonrecoverable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-540">**ресеткаунт**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-540">**ResetCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-541">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-541">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-542">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-543">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| Счетчик сброса системных сбросов \| ")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\|Reset Count")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-544">Число автоматических сбросов с момента последнего сброса.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-544">Number of automatic resets since the last reset.</span></span> <span data-ttu-id="d1e8d-545">Значение 1 (минус единица) указывает на то, что счетчик неизвестен.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-545">A value of  1 (minus one) indicates that the count is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-546">**ресетлимит**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-546">**ResetLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-547">Тип данных: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-547">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-548">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-548">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-549">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| \| Превышено ограничение на сброс системы")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-549">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 23\|System Reset\| Reset Limit")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-550">Число последовательных попыток сброса системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-550">Number of consecutive times a system reset is attempted.</span></span> <span data-ttu-id="d1e8d-551">Значение 1 (минус единица) указывает на то, что ограничение неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-551">A value of  1 (minus one) indicates that the limit is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-552">**Роли**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-552">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-553">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-553">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-554">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-555">Список, указывающий роли системы в среде информационных технологий.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-555">List that specifies the roles of a system in the information technology environment.</span></span>

<span data-ttu-id="d1e8d-556">Это свойство наследуется [**от \_ системы CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-556">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-557">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-557">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-558">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-558">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-559">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-559">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-560">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-560">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-561">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-561">Current status of an object.</span></span>

<span data-ttu-id="d1e8d-562">Для Win32_ComputerSystem состояние всегда равно «ОК».</span><span class="sxs-lookup"><span data-stu-id="d1e8d-562">For Win32_ComputerSystem, the Status is always “OK”.</span></span>

<span data-ttu-id="d1e8d-563">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-563">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dl>

</dd> <dt>

<span data-ttu-id="d1e8d-564">**суппортконтактдескриптион**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-564">**SupportContactDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-565">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-565">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-566">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-566">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-567">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| [](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| сведения о поддержке Win32API жетприватепрофилестринг")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-567">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileString**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring)\|Support Information")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-568">Список контактных данных службы поддержки для операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-568">List of the support contact information for the Windows operating system.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-569">**системфамили**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-569">**SystemFamily**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-570">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-570">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-571">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-571">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-572">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| семейство системных сведений SMBIOS Type 1 \| ")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-572">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Family")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-573">Семейство, к которому принадлежит определенный компьютер.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-573">The family to which a particular computer belongs.</span></span> <span data-ttu-id="d1e8d-574">Семейство относится к набору компьютеров, которые похожи, но не идентичны с точки зрения оборудования или программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-574">A family refers to a set of computers that are similar but not identical from a hardware or software point of view.</span></span>

<span data-ttu-id="d1e8d-575">Это значение берется из члена **семьи** структуры **сведений о системе** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-575">This value comes from the **Family** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d1e8d-576">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-576">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-577">**системскунумбер**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-577">**SystemSKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-578">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-578">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-579">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-579">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-580">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 1 \| системы, \| номер SKU")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-580">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|SKU Number")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-581">Определяет конфигурацию конкретного компьютера для продажи.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-581">Identifies a particular computer configuration for sale.</span></span> <span data-ttu-id="d1e8d-582">Иногда он также называется ИДЕНТИФИКАТОРом продукта или номером заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-582">It is sometimes also called a product ID or purchase order number.</span></span>

<span data-ttu-id="d1e8d-583">Это значение берется из **номера SKU** в структуре **сведений о системе** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-583">This value comes from the **SKU Number** member of the **System Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="d1e8d-584">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-584">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-585">**системстартупделай**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-585">**SystemStartupDelay**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-586">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-586">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-587">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-587">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-588">Квалификаторы: [**устаревшие**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**привилегии**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Сесистеменвиронментпривилеже"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**жетприватепрофилеинт**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| \| время ожидания загрузки"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-588">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileInt**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint)\|Boot Loader\|timeout"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-589">**Системстартупделай** больше не доступен для использования, так как Boot.ini не используется для настройки запуска системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-589">**SystemStartupDelay** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="d1e8d-590">Вместо этого используйте [классы BCD](/previous-versions/windows/desktop/bcd/bcd-classes) , предоставляемые поставщиком WMI данные конфигурации загрузки (BCD) или команду **BCDEdit** .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-590">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-591">**системстартупоптионс**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-591">**SystemStartupOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-592">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-592">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-593">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-593">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-594">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**привилегии**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Сесистеменвиронментпривилеже"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**жетприватепрофилесектион**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| операционные системы")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-594">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|[**GetPrivateProfileSection**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection)\|Operating Systems")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-595">**Системстартупоптионс** больше не доступен для использования, так как Boot.ini не используется для настройки запуска системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-595">**SystemStartupOptions** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="d1e8d-596">Вместо этого используйте [классы BCD](/previous-versions/windows/desktop/bcd/bcd-classes) , предоставляемые поставщиком WMI данные конфигурации загрузки (BCD) или команду **BCDEdit** .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-596">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-597">**системстартупсеттинг**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-597">**SystemStartupSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-598">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-598">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-599">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-599">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-600">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**привилегии**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Сесистеменвиронментпривилеже"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-600">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Privileges**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("SeSystemEnvironmentPrivilege"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-601">**Системстартупсеттинг** больше не доступен для использования, так как Boot.ini не используется для настройки запуска системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-601">**SystemStartupSetting** is no longer available for use because Boot.ini is not used to configure system startup.</span></span> <span data-ttu-id="d1e8d-602">Вместо этого используйте [классы BCD](/previous-versions/windows/desktop/bcd/bcd-classes) , предоставляемые поставщиком WMI данные конфигурации загрузки (BCD) или команду **BCDEdit** .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-602">Instead, use the [BCD classes](/previous-versions/windows/desktop/bcd/bcd-classes) supplied by the Boot Configuration Data (BCD) WMI provider or the **Bcdedit** command.</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-603">**SystemType**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-603">**SystemType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-604">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-605">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-605">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-606">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| впроцессорарчитектуре")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-606">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Structures\|[**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info)\|wProcessorArchitecture")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-607">Система на компьютере под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-607">System running on the Windows-based computer.</span></span> <span data-ttu-id="d1e8d-608">Это свойство должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-608">This property must have a value.</span></span>

<span data-ttu-id="d1e8d-609">В следующем списке указаны некоторые из возможных значений этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-609">The following list identifies some of the possible values for this property.</span></span>

<dl> <dd><span data-ttu-id="d1e8d-610">"компьютер на базе x64"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-610">"x64-based PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-611">"Компьютер на базе x86"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-611">"X86-based PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-612">"ПК на основе MIPS"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-612">"MIPS-based PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-613">"ПК на базе Alpha"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-613">"Alpha-based PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-614">"Power PC"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-614">"Power PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-615">«КОМПЬЮТЕР SH-x»</span><span class="sxs-lookup"><span data-stu-id="d1e8d-615">"SH-x PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-616">"Стронгарм ПК"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-616">"StrongARM PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-617">"64-разрядный Intel PC"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-617">"64-bit Intel PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-618">"64-разрядный ПК Alpha"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-618">"64-bit Alpha PC"</span></span></dd> <dd><span data-ttu-id="d1e8d-619">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="d1e8d-619">"Unknown"</span></span></dd> <dd><span data-ttu-id="d1e8d-620">"X86-Nec98 PC"</span><span class="sxs-lookup"><span data-stu-id="d1e8d-620">"X86-Nec98 PC"</span></span></dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

<span data-ttu-id="d1e8d-621">**Компьютер на базе x86** ("ПК на базе x86")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-621">**X86-based PC** ("X86-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

<span data-ttu-id="d1e8d-622">**Компьютер на основе MIPS** ("ПК на основе MIPS")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-622">**MIPS-based PC** ("MIPS-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

<span data-ttu-id="d1e8d-623">**ПК на базе Alpha** ("ПК на основе Alpha")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-623">**Alpha-based PC** ("Alpha-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

<span data-ttu-id="d1e8d-624">**Power PC** ("Power PC")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-624">**Power PC** ("Power PC")</span></span>


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

<span data-ttu-id="d1e8d-625">**Компьютер SH-x** («компьютер SH-x»)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-625">**SH-x PC** ("SH-x PC")</span></span>


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

<span data-ttu-id="d1e8d-626">**СТРОНГАРМ ПК** ("стронгарм PC")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-626">**StrongARM PC** ("StrongARM PC")</span></span>


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

<span data-ttu-id="d1e8d-627">**64-разрядный компьютер Intel** ("64-разрядный Intel PC")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-627">**64-bit Intel PC** ("64-bit Intel PC")</span></span>


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

<span data-ttu-id="d1e8d-628">**компьютер на базе x64** ("ПК на базе x64")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-628">**x64-based PC** ("x64-based PC")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-629">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-629">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

<span data-ttu-id="d1e8d-630">**X86-NEC98 PC** ("x86-Nec98 PC")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-630">**X86-Nec98 PC** ("X86-Nec98 PC")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-631">**сермалстате**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-631">**ThermalState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-632">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-632">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-633">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-633">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-634">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3 \| системного корпуса или \| термальное состояние корпуса")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-634">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 3\|System Enclosure or Chassis\|Thermal State")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-635">Состояние температуры системы при последней загрузке.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-635">Thermal state of the system when last booted.</span></span>

<span data-ttu-id="d1e8d-636">Это значение берется из элемента " **состояние тепловой температуры** " в структуре **корпуса или** в данных SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-636">This value comes from the **Thermal State** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1e8d-637">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-637">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-638">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-638">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span data-ttu-id="d1e8d-639">**Безопасность** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-639">**Safe** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d1e8d-640">**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-640">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d1e8d-641">**Критическая** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-641">**Critical** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span data-ttu-id="d1e8d-642">**Без возможности восстановления** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-642">**Non-recoverable** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-643">**TotalPhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-643">**TotalPhysicalMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-644">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-644">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-645">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-645">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-646">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| структуры управления памятью \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| двтоталфис"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-646">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Memory Management Structures\|[**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus)\|dwTotalPhys"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-647">Общий размер физической памяти.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-647">Total size of physical memory.</span></span> <span data-ttu-id="d1e8d-648">Имейте в виду, что в некоторых обстоятельствах это свойство может не возвращать точное значение физической памяти.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-648">Be aware that, under some circumstances, this property may not return an accurate value for the physical memory.</span></span> <span data-ttu-id="d1e8d-649">Например, неточна, если BIOS использует часть физической памяти.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-649">For example, it is not accurate if the BIOS is using some of the physical memory.</span></span> <span data-ttu-id="d1e8d-650">Чтобы получить точное значение, используйте вместо этого свойство **Capacity** в [**Win32 \_ фисикалмемори**](win32-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-650">For an accurate value, use the **Capacity** property in [**Win32\_PhysicalMemory**](win32-physicalmemory.md) instead.</span></span>

<span data-ttu-id="d1e8d-651">Пример: 67108864</span><span class="sxs-lookup"><span data-stu-id="d1e8d-651">Example: 67108864</span></span>

<span data-ttu-id="d1e8d-652">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-652">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-653">**UserName**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-653">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-654">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-654">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-655">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-655">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-656">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information functions- \| [**username**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-656">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Information Functions\|[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-657">Имя пользователя, выполнившего вход в систему.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-657">Name of a user that is logged on currently.</span></span> <span data-ttu-id="d1e8d-658">Это свойство должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-658">This property must have a value.</span></span> <span data-ttu-id="d1e8d-659">В сеансе служб терминалов **username** возвращает имя пользователя, вошедшего в консоль, а не пользователя, вошедшего в систему во время сеанса службы терминалов.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-659">In a terminal services session, **UserName** returns the name of the user that is logged on to the console not the user logged on during the terminal service session.</span></span>

<span data-ttu-id="d1e8d-660">Пример: жеффсмис</span><span class="sxs-lookup"><span data-stu-id="d1e8d-660">Example: jeffsmith</span></span>

</dd> <dt>

<span data-ttu-id="d1e8d-661">**вакеуптипе**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-661">**WakeUpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-662">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-662">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-663">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1e8d-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-664">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип SMBIOS \| 1 \| системная информация о \| типе пробуждения")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-664">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|System Information\|Wake-up Type")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-665">Событие, которое приводит к включению системы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-665">Event that causes the system to power up.</span></span>

<span data-ttu-id="d1e8d-666">Это значение берется из члена **типа пробуждения** в структуре **сведений о системе** в сведениях SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-666">This value comes from the **Wake-up Type** member of the **System Information** structure in the SMBIOS information.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="d1e8d-667">**Зарезервировано** (0)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-667">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d1e8d-668">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-668">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d1e8d-669">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-669">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

<span data-ttu-id="d1e8d-670">**Таймер APM** (3)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-670">**APM Timer** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

<span data-ttu-id="d1e8d-671">**Кольцо модема** (4)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-671">**Modem Ring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

<span data-ttu-id="d1e8d-672">**Удаленная локальная сеть** (5)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-672">**LAN Remote** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

<span data-ttu-id="d1e8d-673">**Выключатель питания** (6)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-673">**Power Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

<span data-ttu-id="d1e8d-674">**PCI PME \#** 7</span><span class="sxs-lookup"><span data-stu-id="d1e8d-674">**PCI PME\#** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

<span data-ttu-id="d1e8d-675">**Питание от сети восстановлено** (8)</span><span class="sxs-lookup"><span data-stu-id="d1e8d-675">**AC Power Restored** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1e8d-676">**Группе**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-676">**Workgroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1e8d-677">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-678">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d1e8d-678">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d1e8d-679">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span><span class="sxs-lookup"><span data-stu-id="d1e8d-679">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("")</span></span>
</dt> </dl>

<span data-ttu-id="d1e8d-680">Имя рабочей группы для этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-680">Name of the workgroup for this computer.</span></span> <span data-ttu-id="d1e8d-681">Если свойство **партофдомаин** имеет значение **false**, то возвращается имя рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-681">If the value of the **PartOfDomain** property is **False**, then the name of the workgroup is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1e8d-682">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1e8d-682">Remarks</span></span>

<span data-ttu-id="d1e8d-683">Чтобы определить общее число экземпляров процессора, связанных с объектом системы компьютера, используйте класс сопоставления [**Win32 \_ компутерсистемпроцессор**](win32-computersystemprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-683">To determine the total number of processor instances associated with a computer system object, use the [**Win32\_ComputerSystemProcessor**](win32-computersystemprocessor.md) association class.</span></span>

<span data-ttu-id="d1e8d-684">Экземпляр **Win32 \_ ComputerSystem** с несколькими физическими процессорами связан с несколькими экземплярами [**\_ процессора Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-684">A **Win32\_ComputerSystem** instance that has multiple physical processors has multiple [**Win32\_Processor**](win32-processor.md) instances associated with it.</span></span> <span data-ttu-id="d1e8d-685">Если значение **нумберофлогикалпроцессорс** больше, чем значение **NumberOfProcessors** , то компьютерная система является либо многоядерной системой, либо для нее включен один или несколько процессоров.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-685">If the value of **NumberOfLogicalProcessors** is greater than the value of **NumberOfProcessors** then the computer system is either a multicore system or has one or more processors enabled for hyperthreading.</span></span> <span data-ttu-id="d1e8d-686">Дополнительные сведения см. в разделе **нумберофлогикалпроцессорс** and **нумберофкорес** Properties and remarks статьи **Win32 \_ Processor**.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-686">For more information, see the **NumberOfLogicalProcessors** and **NumberOfCores** properties and Remarks section in **Win32\_Processor**.</span></span>

<span data-ttu-id="d1e8d-687">Класс **Win32 \_ ComputerSystem** является производным от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).</span><span class="sxs-lookup"><span data-stu-id="d1e8d-687">The **Win32\_ComputerSystem** class is derived from [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d1e8d-688">Примеры</span><span class="sxs-lookup"><span data-stu-id="d1e8d-688">Examples</span></span>

<span data-ttu-id="d1e8d-689">Следующий [пример кода](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) в центре сценариев использует **Win32 \_ ComputerSystem** для получения информации из нескольких компьютерных систем и отображает их в графическом интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-689">The following Scripting Center [code example](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) uses the **Win32\_ComputerSystem** to retrieve information from a number of computer systems, and display them in a GUI.</span></span>

<span data-ttu-id="d1e8d-690">Пример сценария, который получает данные об операционной системе и процессоре из **Win32 \_ ComputerSystem**, [**\_ процессора Win32**](win32-processor.md)и Win32 Operating, [**можно \_**](win32-operatingsystem.md) найти в примерах, посвященных [**\_ процессору Win32**](win32-processor.md) .</span><span class="sxs-lookup"><span data-stu-id="d1e8d-690">You can find an example script that obtains operating system and processor data from **Win32\_ComputerSystem**, [**Win32\_Processor**](win32-processor.md), and [**Win32\_OperatingSystem**](win32-operatingsystem.md) in the [**Win32\_Processor**](win32-processor.md) topic examples.</span></span>

<span data-ttu-id="d1e8d-691">Следующий пример сценария VBScript описывает, как получить доменное имя локального компьютера из экземпляров **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-691">The following VBScript sample describes how to retrieve the domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



<span data-ttu-id="d1e8d-692">В следующем образце Perl показано, как получить имя локального компьютера из экземпляров **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-692">The following Perl sample describes how to retrieve the local machine name from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="d1e8d-693">В следующем образце Perl описывается получение доменного имени DNS локального компьютера из экземпляров **Win32 \_ ComputerSystem**.</span><span class="sxs-lookup"><span data-stu-id="d1e8d-693">The following Perl sample describes how to retrieve the DNS domain name of the local machine from instances of **Win32\_ComputerSystem**.</span></span>


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="d1e8d-694">Требования</span><span class="sxs-lookup"><span data-stu-id="d1e8d-694">Requirements</span></span>



| <span data-ttu-id="d1e8d-695">Требование</span><span class="sxs-lookup"><span data-stu-id="d1e8d-695">Requirement</span></span> | <span data-ttu-id="d1e8d-696">Значение</span><span class="sxs-lookup"><span data-stu-id="d1e8d-696">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e8d-697">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1e8d-697">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e8d-698">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1e8d-698">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1e8d-699">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1e8d-699">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e8d-700">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1e8d-700">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1e8d-701">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1e8d-701">Namespace</span></span><br/>                | <span data-ttu-id="d1e8d-702">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1e8d-702">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1e8d-703">MOF</span><span class="sxs-lookup"><span data-stu-id="d1e8d-703">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1e8d-704"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1e8d-704"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1e8d-705">DLL</span><span class="sxs-lookup"><span data-stu-id="d1e8d-705">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1e8d-706"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1e8d-706"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1e8d-707">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1e8d-707">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e8d-708">**\_УНИТАРИКОМПУТЕРСИСТЕМ CIM**</span><span class="sxs-lookup"><span data-stu-id="d1e8d-708">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dt>

<span data-ttu-id="d1e8d-709">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d1e8d-709">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d1e8d-710">Задачи WMI: учетные записи и домены</span><span class="sxs-lookup"><span data-stu-id="d1e8d-710">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d1e8d-711">Задачи WMI: оборудование компьютера</span><span class="sxs-lookup"><span data-stu-id="d1e8d-711">WMI Tasks: Computer Hardware</span></span>](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[<span data-ttu-id="d1e8d-712">Задачи WMI: управление рабочим столом</span><span class="sxs-lookup"><span data-stu-id="d1e8d-712">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

