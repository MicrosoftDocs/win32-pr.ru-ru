---
description: Представляет возможности и емкость управления секционированной области физического диска в компьютерной системе под управлением Windows.
ms.assetid: 7e78be3f-bae4-4374-abbf-7c4e63ba7593
ms.tgt_platform: multiple
title: Класс Win32_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskPartition
- Win32_DiskPartition.AdditionalAvailability
- Win32_DiskPartition.Availability
- Win32_DiskPartition.PowerManagementCapabilities
- Win32_DiskPartition.IdentifyingDescriptions
- Win32_DiskPartition.MaxQuiesceTime
- Win32_DiskPartition.OtherIdentifyingInfo
- Win32_DiskPartition.StatusInfo
- Win32_DiskPartition.PowerOnHours
- Win32_DiskPartition.TotalPowerOnHours
- Win32_DiskPartition.Access
- Win32_DiskPartition.BlockSize
- Win32_DiskPartition.Bootable
- Win32_DiskPartition.BootPartition
- Win32_DiskPartition.Caption
- Win32_DiskPartition.ConfigManagerErrorCode
- Win32_DiskPartition.ConfigManagerUserConfig
- Win32_DiskPartition.CreationClassName
- Win32_DiskPartition.Description
- Win32_DiskPartition.DeviceID
- Win32_DiskPartition.DiskIndex
- Win32_DiskPartition.ErrorCleared
- Win32_DiskPartition.ErrorDescription
- Win32_DiskPartition.ErrorMethodology
- Win32_DiskPartition.HiddenSectors
- Win32_DiskPartition.Index
- Win32_DiskPartition.InstallDate
- Win32_DiskPartition.LastErrorCode
- Win32_DiskPartition.Name
- Win32_DiskPartition.NumberOfBlocks
- Win32_DiskPartition.PNPDeviceID
- Win32_DiskPartition.PowerManagementSupported
- Win32_DiskPartition.PrimaryPartition
- Win32_DiskPartition.Purpose
- Win32_DiskPartition.RewritePartition
- Win32_DiskPartition.Size
- Win32_DiskPartition.StartingOffset
- Win32_DiskPartition.Status
- Win32_DiskPartition.SystemCreationClassName
- Win32_DiskPartition.SystemName
- Win32_DiskPartition.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4f9a9c16f58d0119c8027848c481479985e7505e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896277"
---
# <a name="win32_diskpartition-class"></a><span data-ttu-id="098ce-103">\_Класс Win32 дискпартитион</span><span class="sxs-lookup"><span data-stu-id="098ce-103">Win32\_DiskPartition class</span></span>

<span data-ttu-id="098ce-104">Класс **WMI \_ дискпартитион** [инструментария](/windows/desktop/WmiSdk/retrieving-a-class) Win32 представляет возможности и Управление емкостью секционированной области физического диска в компьютерной системе под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="098ce-104">The **Win32\_DiskPartition** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the capabilities and management capacity of a partitioned area of a physical disk on a computer system running Windows.</span></span> <span data-ttu-id="098ce-105">Пример: диск \# 0, раздел \# 1.</span><span class="sxs-lookup"><span data-stu-id="098ce-105">Example: Disk \#0, Partition \#1.</span></span>

<span data-ttu-id="098ce-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="098ce-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="098ce-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="098ce-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="098ce-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="098ce-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskPartition : CIM_DiskPartition
{
  unit16   AdditionalAvailability;
  uint16   Availability;
  uint16   PowerManagementCapabilities[];
  string   IdentifyingDescriptions[1];
  uint64   MaxQuiesceTime;
  uint64   OtherIdentifyingInfo;
  uint16   StatusInfo;
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  uint16   Access;
  uint64   BlockSize;
  boolean  Bootable;
  boolean  BootPartition;
  string.  Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string.  CreationClassName;
  string   Description;
  string   DeviceID;
  uint32   DiskIndex;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  uint32   HiddenSectors;
  uint32   Index;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  boolean  PrimaryPartition;
  string   Purpose;
  boolean  RewritePartition;
  uint64   Size;
  uint64   StartingOffset;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  string   Type;
};
```

## <a name="members"></a><span data-ttu-id="098ce-109">Члены</span><span class="sxs-lookup"><span data-stu-id="098ce-109">Members</span></span>

<span data-ttu-id="098ce-110">Класс **Win32 \_ дискпартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="098ce-110">The **Win32\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="098ce-111">Методы</span><span class="sxs-lookup"><span data-stu-id="098ce-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="098ce-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="098ce-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="098ce-113">Методы</span><span class="sxs-lookup"><span data-stu-id="098ce-113">Methods</span></span>

<span data-ttu-id="098ce-114">Класс **Win32 \_ дискпартитион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="098ce-114">The **Win32\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="098ce-115">Метод</span><span class="sxs-lookup"><span data-stu-id="098ce-115">Method</span></span>                                                     | <span data-ttu-id="098ce-116">Описание</span><span class="sxs-lookup"><span data-stu-id="098ce-116">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="098ce-117">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="098ce-117">**Reset**</span></span>](win32-diskpartition-reset.md)                 | <span data-ttu-id="098ce-118">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-118">Requests a reset of the logical device.</span></span><br/>                                                            |
| [<span data-ttu-id="098ce-119">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="098ce-119">**SetPowerState**</span></span>](win32-diskpartition-setpowerstate.md) | <span data-ttu-id="098ce-120">Задает требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="098ce-120">Sets the desired power state for a logical device and when a device should be put into that state.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="098ce-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="098ce-121">Properties</span></span>

<span data-ttu-id="098ce-122">Класс **Win32 \_ дискпартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="098ce-122">The **Win32\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="098ce-123">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="098ce-123">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="098ce-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-126">Доступ к носителю доступен.</span><span class="sxs-lookup"><span data-stu-id="098ce-126">Media access available.</span></span>

<span data-ttu-id="098ce-127">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-127">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="098ce-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="098ce-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="098ce-129"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="098ce-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="098ce-130"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-131">Возможность записи</span><span class="sxs-lookup"><span data-stu-id="098ce-131">Writable</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="098ce-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="098ce-132"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="098ce-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="098ce-133"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-134">**аддитионалаваилабилити**</span><span class="sxs-lookup"><span data-stu-id="098ce-134">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-135">Тип данных: **unit16**</span><span class="sxs-lookup"><span data-stu-id="098ce-135">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-136">Тип доступа: только для записи</span><span class="sxs-lookup"><span data-stu-id="098ce-136">Access type: Write-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-137">Дополнительные доступность и состояние устройства, кроме указанного в свойстве Availability.</span><span class="sxs-lookup"><span data-stu-id="098ce-137">Additional availability and status of the Device, beyond that specified in the Availability property.</span></span> <span data-ttu-id="098ce-138">Свойство **Availability** указывает основное состояние и доступность устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-138">The **Availability** property denotes the primary status and availability of the Device.</span></span> <span data-ttu-id="098ce-139">В некоторых случаях это не будет достаточно для обозначения полного состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-139">In some cases, this will not be sufficient to denote the complete status of the Device.</span></span> <span data-ttu-id="098ce-140">В таких случаях для предоставления дополнительных сведений можно использовать свойство **аддитионалаваилабилити** .</span><span class="sxs-lookup"><span data-stu-id="098ce-140">In those cases, the **AdditionalAvailability** property can be used to provide further information.</span></span> <span data-ttu-id="098ce-141">Например, основная **доступность** устройства может быть отключена (значение = 8), но она может также находиться в состоянии низкого энергопотребления (**аддитоналаваилабилити** value = 14), либо на устройстве может выполняться диагностика (**Аддитионалаваилабилити** значение = 5, в тесте).</span><span class="sxs-lookup"><span data-stu-id="098ce-141">For example, a Device's primary **Availability** may be Off line (value=8), but it may also be in a low power state (**AdditonalAvailability** value=14), or the Device could be running Diagnostics (**AdditionalAvailability** value=5, In Test)."</span></span>

<span data-ttu-id="098ce-142">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-142">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="098ce-143">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="098ce-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-144">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="098ce-144">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="098ce-145">**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="098ce-145">**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="098ce-146">**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="098ce-146">**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="098ce-147">**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="098ce-147">**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="098ce-148">**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="098ce-148">**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="098ce-149">**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="098ce-149">**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="098ce-150">Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="098ce-150">**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="098ce-151">Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="098ce-151">**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="098ce-152">**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="098ce-152">**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="098ce-153">**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="098ce-153">**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="098ce-154">**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="098ce-154">**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="098ce-155">Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="098ce-155">**Power Save - Unknown** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="098ce-156">Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="098ce-156">**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="098ce-157">Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="098ce-157">**Power Save - Standby** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="098ce-158">**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="098ce-158">**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="098ce-159">Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="098ce-159">**Power Save - Warning** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="098ce-160">**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="098ce-160">**Paused** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="098ce-161">**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="098ce-161">**Not Ready** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="098ce-162">**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="098ce-162">**Not Configured** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="098ce-163">**Замораживание** (21)</span><span class="sxs-lookup"><span data-stu-id="098ce-163">**Quiesce** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-164">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="098ce-164">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-165">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="098ce-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-167">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="098ce-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-168">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-168">Availability and status of the device.</span></span>

<span data-ttu-id="098ce-169">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-169">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="098ce-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="098ce-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="098ce-171"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="098ce-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="098ce-172"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="098ce-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="098ce-173"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="098ce-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="098ce-174"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="098ce-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="098ce-175"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="098ce-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="098ce-176"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="098ce-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="098ce-177"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="098ce-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="098ce-178"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="098ce-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="098ce-179"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="098ce-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="098ce-180"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="098ce-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="098ce-181"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="098ce-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="098ce-182"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-183">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="098ce-183">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="098ce-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="098ce-184"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-185">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="098ce-185">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="098ce-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="098ce-186"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-187">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="098ce-187">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="098ce-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="098ce-188"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="098ce-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="098ce-189"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-190">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="098ce-190">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="098ce-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="098ce-191"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-192">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="098ce-192">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="098ce-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="098ce-193"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-194">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="098ce-194">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="098ce-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="098ce-195"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-196">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="098ce-196">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="098ce-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="098ce-197"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-198">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="098ce-198">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-199">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="098ce-199">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-200">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-202">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="098ce-202">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-203">Размер в байтах блоков, образующих эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="098ce-203">Size in bytes of the blocks which form this storage extent.</span></span> <span data-ttu-id="098ce-204">Если значение неизвестно или если концепция блока является недопустимой (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="098ce-204">If unknown or if a block concept is not valid (for example, for aggregate extents, memory or logical disks), enter a 1.</span></span>

<span data-ttu-id="098ce-205">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="098ce-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="098ce-206">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-206">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-207">**Загружаемый**</span><span class="sxs-lookup"><span data-stu-id="098ce-207">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-208">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-208">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-210">Указывает, может ли компьютер загружаться из этого раздела.</span><span class="sxs-lookup"><span data-stu-id="098ce-210">Indicates whether the computer can be booted from this partition.</span></span>

<span data-ttu-id="098ce-211">Это свойство наследуется от [**CIM \_ дискпартитион**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-211">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-212">**бутпартитион**</span><span class="sxs-lookup"><span data-stu-id="098ce-212">**BootPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-213">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-215">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="098ce-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-216">Секция — это активный раздел.</span><span class="sxs-lookup"><span data-stu-id="098ce-216">Partition is the active partition.</span></span> <span data-ttu-id="098ce-217">Операционная система использует активный раздел при загрузке с жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="098ce-217">The operating system uses the active partition when booting from a hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="098ce-218">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="098ce-218">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-219">Тип данных: **String.**</span><span class="sxs-lookup"><span data-stu-id="098ce-219">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-221">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="098ce-221">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-222">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="098ce-222">Short description of the object.</span></span>

<span data-ttu-id="098ce-223">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-223">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-224">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="098ce-224">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-225">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="098ce-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-227">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="098ce-227">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-228">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="098ce-228">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="098ce-229">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-229">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="098ce-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="098ce-230"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="098ce-231"> (0)</span><span class="sxs-lookup"><span data-stu-id="098ce-231">(0)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-232">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="098ce-232">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="098ce-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="098ce-233"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="098ce-234">(1)</span><span class="sxs-lookup"><span data-stu-id="098ce-234">(1)</span></span>


</dt> <dd>

<span data-ttu-id="098ce-235">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="098ce-235">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="098ce-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-236"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="098ce-237">(2)</span><span class="sxs-lookup"><span data-stu-id="098ce-237">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="098ce-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="098ce-238"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="098ce-239">(3)</span><span class="sxs-lookup"><span data-stu-id="098ce-239">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="098ce-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="098ce-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="098ce-241">(4)</span><span class="sxs-lookup"><span data-stu-id="098ce-241">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="098ce-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="098ce-242"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="098ce-243">(5)</span><span class="sxs-lookup"><span data-stu-id="098ce-243">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="098ce-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="098ce-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="098ce-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="098ce-245">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="098ce-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="098ce-246"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="098ce-247">(7)</span><span class="sxs-lookup"><span data-stu-id="098ce-247">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="098ce-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-248"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="098ce-249">(8)</span><span class="sxs-lookup"><span data-stu-id="098ce-249">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="098ce-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-250"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="098ce-251">(9)</span><span class="sxs-lookup"><span data-stu-id="098ce-251">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="098ce-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="098ce-252"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="098ce-253">(10)</span><span class="sxs-lookup"><span data-stu-id="098ce-253">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="098ce-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-254"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="098ce-255">(11)</span><span class="sxs-lookup"><span data-stu-id="098ce-255">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="098ce-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="098ce-256"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="098ce-257">(12)</span><span class="sxs-lookup"><span data-stu-id="098ce-257">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="098ce-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="098ce-259">(13)</span><span class="sxs-lookup"><span data-stu-id="098ce-259">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="098ce-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="098ce-260"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="098ce-261">(14)</span><span class="sxs-lookup"><span data-stu-id="098ce-261">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="098ce-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="098ce-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="098ce-263">(15)</span><span class="sxs-lookup"><span data-stu-id="098ce-263">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="098ce-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="098ce-264"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="098ce-265">(16)</span><span class="sxs-lookup"><span data-stu-id="098ce-265">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="098ce-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="098ce-266"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="098ce-267">(17)</span><span class="sxs-lookup"><span data-stu-id="098ce-267">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="098ce-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-268"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="098ce-269">(18)</span><span class="sxs-lookup"><span data-stu-id="098ce-269">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="098ce-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="098ce-270"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="098ce-271">(19)</span><span class="sxs-lookup"><span data-stu-id="098ce-271">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="098ce-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="098ce-272"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="098ce-273">(20)</span><span class="sxs-lookup"><span data-stu-id="098ce-273">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="098ce-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="098ce-274"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="098ce-275">(21)</span><span class="sxs-lookup"><span data-stu-id="098ce-275">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="098ce-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="098ce-276"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="098ce-277">(22)</span><span class="sxs-lookup"><span data-stu-id="098ce-277">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="098ce-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="098ce-278"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="098ce-279">(23)</span><span class="sxs-lookup"><span data-stu-id="098ce-279">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="098ce-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="098ce-280"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="098ce-281">(24)</span><span class="sxs-lookup"><span data-stu-id="098ce-281">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="098ce-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="098ce-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="098ce-283">(25)</span><span class="sxs-lookup"><span data-stu-id="098ce-283">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="098ce-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="098ce-284"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="098ce-285">(26)</span><span class="sxs-lookup"><span data-stu-id="098ce-285">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="098ce-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="098ce-286"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="098ce-287">(27)</span><span class="sxs-lookup"><span data-stu-id="098ce-287">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="098ce-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="098ce-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="098ce-289">(28)</span><span class="sxs-lookup"><span data-stu-id="098ce-289">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="098ce-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="098ce-290"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="098ce-291">(29)</span><span class="sxs-lookup"><span data-stu-id="098ce-291">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="098ce-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="098ce-292"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="098ce-293">(30)</span><span class="sxs-lookup"><span data-stu-id="098ce-293">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="098ce-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="098ce-294"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="098ce-295">1-31</span><span class="sxs-lookup"><span data-stu-id="098ce-295">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-296">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="098ce-296">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-297">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-297">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-298">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-298">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-299">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="098ce-299">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-300">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="098ce-300">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="098ce-301">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-301">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-302">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="098ce-302">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-303">Тип данных: **String.**</span><span class="sxs-lookup"><span data-stu-id="098ce-303">Data type: **string.**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-304">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-305">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="098ce-305">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="098ce-306">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="098ce-306">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="098ce-307">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="098ce-307">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="098ce-308">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-308">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-309">**Описание**</span><span class="sxs-lookup"><span data-stu-id="098ce-309">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-310">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-311">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-312">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="098ce-312">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-313">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="098ce-313">Description of the object.</span></span>

<span data-ttu-id="098ce-314">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-315">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="098ce-315">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-316">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-317">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-318">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceID"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="098ce-318">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-319">Уникальный идентификатор диска и раздела из остальной части системы.</span><span class="sxs-lookup"><span data-stu-id="098ce-319">Unique identifier of the disk drive and partition, from the rest of the system.</span></span>

</dd> <dt>

<span data-ttu-id="098ce-320">**DiskIndex**</span><span class="sxs-lookup"><span data-stu-id="098ce-320">**DiskIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-321">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="098ce-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-323">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile")</span><span class="sxs-lookup"><span data-stu-id="098ce-323">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-324">Номер индекса диска, содержащего этот раздел.</span><span class="sxs-lookup"><span data-stu-id="098ce-324">Index number of the disk containing this partition.</span></span>

<span data-ttu-id="098ce-325">Пример: 0</span><span class="sxs-lookup"><span data-stu-id="098ce-325">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="098ce-326">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="098ce-326">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-327">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-327">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-329">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="098ce-329">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="098ce-330">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-330">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-331">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="098ce-331">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-332">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-332">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-334">Сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="098ce-334">Information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="098ce-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-336">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="098ce-336">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-339">Тип обнаружения и исправления ошибок, поддерживаемый этой областью хранения.</span><span class="sxs-lookup"><span data-stu-id="098ce-339">Type of error detection and correction supported by this storage extent.</span></span>

<span data-ttu-id="098ce-340">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-340">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-341">**хидденсекторс**</span><span class="sxs-lookup"><span data-stu-id="098ce-341">**HiddenSectors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-342">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="098ce-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-344">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span><span class="sxs-lookup"><span data-stu-id="098ce-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-345">Число скрытых секторов в секции.</span><span class="sxs-lookup"><span data-stu-id="098ce-345">Number of hidden sectors in the partition.</span></span>

<span data-ttu-id="098ce-346">Пример: 63</span><span class="sxs-lookup"><span data-stu-id="098ce-346">Example: 63</span></span>

</dd> <dt>

<span data-ttu-id="098ce-347">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="098ce-347">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-348">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="098ce-348">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="098ce-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-350">Массив строк произвольной формы, предоставляющий объяснения и подробные сведения, лежащие в основе записей в массиве Осеридентифингинфо.</span><span class="sxs-lookup"><span data-stu-id="098ce-350">An array of free-form strings providing explanations and details behind the entries in the OtherIdentifyingInfo array.</span></span> <span data-ttu-id="098ce-351">Обратите внимание, что каждая запись этого массива связана с записью в Осеридентифингинфо, расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="098ce-351">Note, each entry of this array is related to the entry in OtherIdentifyingInfo that is located at the same index.</span></span>

<span data-ttu-id="098ce-352">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-353">**Index**</span><span class="sxs-lookup"><span data-stu-id="098ce-353">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-354">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="098ce-354">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-356">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="098ce-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-357">Номер индекса секции.</span><span class="sxs-lookup"><span data-stu-id="098ce-357">Index number of the partition.</span></span>

<span data-ttu-id="098ce-358">Пример: 1</span><span class="sxs-lookup"><span data-stu-id="098ce-358">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="098ce-359">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="098ce-359">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-360">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="098ce-360">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-362">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="098ce-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-363">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="098ce-363">Date the object was installed.</span></span> <span data-ttu-id="098ce-364">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="098ce-364">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="098ce-365">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-365">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-366">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="098ce-366">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-367">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="098ce-367">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-369">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="098ce-369">Last error code reported by the logical device.</span></span>

<span data-ttu-id="098ce-370">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-370">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-371">**макскуиесцетиме**</span><span class="sxs-lookup"><span data-stu-id="098ce-371">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-372">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-372">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-374">Квалификаторы: **поддерживается**</span><span class="sxs-lookup"><span data-stu-id="098ce-374">Qualifiers: **Depricated**</span></span>
</dt> </dl>

<span data-ttu-id="098ce-375">Максимальное время в миллисекундах, в течение которого устройство может работать в замороженном состоянии.</span><span class="sxs-lookup"><span data-stu-id="098ce-375">Maximum time in milliseconds, that a Device can run in a Quiesced state.</span></span> <span data-ttu-id="098ce-376">Состояние устройства определяется в его свойствах Availability и Аддитионалаваилабилити, где заморожено передает значение 21.</span><span class="sxs-lookup"><span data-stu-id="098ce-376">A Device's state is defined in its Availability and AdditionalAvailability properties, where Quiesced is conveyed by the value 21.</span></span> <span data-ttu-id="098ce-377">Что происходит в конце предельного времени, зависит от устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-377">What occurs at the end of the time limit is device-specific.</span></span> <span data-ttu-id="098ce-378">Устройство может разморозьте, находиться в автономном режиме или предпринимать другие действия.</span><span class="sxs-lookup"><span data-stu-id="098ce-378">The Device may unquiesce, may offline or take other action.</span></span> <span data-ttu-id="098ce-379">Значение 0 указывает, что устройство может оставаться замороженным в неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="098ce-379">A value of 0 indicates that a Device can remain quiesced indefinitely.</span></span>

> [!Note]
>
> <span data-ttu-id="098ce-380">"Свойство Макскуиесцетиме не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="098ce-380">"The MaxQuiesceTime property has been deprecated.</span></span> <span data-ttu-id="098ce-381">При оценке использования замораживания было определено, что это единственное свойство не подходит для описания, когда устройство будет автоматически выходить из состояния загружена.</span><span class="sxs-lookup"><span data-stu-id="098ce-381">When evaluating the use of Quiesce, it was determine that this single property is not adequate for describing when a device will automatically exit a quiescent state.</span></span> <span data-ttu-id="098ce-382">Фактически, наиболее вероятный сценарий для выхода устройства из состояния загружена был определен на основе числа ожидающих запросов в очереди, а не в течение максимального времени.</span><span class="sxs-lookup"><span data-stu-id="098ce-382">In fact, the most likely scenario for a device to exit a quiescent state was determined to be based on the number of outstanding requests queued rather than on a maximum time.</span></span> <span data-ttu-id="098ce-383">Оно будет повторно вычислено и перепозиционировано позже.</span><span class="sxs-lookup"><span data-stu-id="098ce-383">This will be re-evaluated and repositioned later.</span></span> <span data-ttu-id="098ce-384">\\n</span><span class="sxs-lookup"><span data-stu-id="098ce-384">\\n</span></span>

 

<span data-ttu-id="098ce-385">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-385">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-386">**Name**</span><span class="sxs-lookup"><span data-stu-id="098ce-386">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-387">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-388">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-389">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="098ce-389">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-390">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="098ce-390">Label by which the object is known.</span></span> <span data-ttu-id="098ce-391">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="098ce-391">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="098ce-392">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-393">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="098ce-393">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-394">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-394">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-395">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-396">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="098ce-396">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-397">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="098ce-397">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="098ce-398">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="098ce-398">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="098ce-399">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="098ce-399">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="098ce-400">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="098ce-400">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="098ce-401">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-402">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="098ce-402">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-403">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-403">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-405">Массив, который фиксирует дополнительные данные, помимо сведений о DeviceID, которые можно использовать для обнаружения объектного типа.</span><span class="sxs-lookup"><span data-stu-id="098ce-405">Array that captures additional data, beyond DeviceID information, that could be used to identify a LogicalDevice.</span></span> <span data-ttu-id="098ce-406">Одним из примеров является хранение понятного имени операционной системы для устройства в этом свойстве.</span><span class="sxs-lookup"><span data-stu-id="098ce-406">One example would be to hold the Operating System's user friendly name for the Device in this property.</span></span> <span data-ttu-id="098ce-407">Максимальная длина — 256.</span><span class="sxs-lookup"><span data-stu-id="098ce-407">Maximum length is 256.</span></span>

<span data-ttu-id="098ce-408">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-409">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="098ce-409">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-410">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-412">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="098ce-412">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-413">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-413">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="098ce-414">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="098ce-414">Example: "\*PNP030b"</span></span>

<span data-ttu-id="098ce-415">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-415">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-416">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="098ce-416">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-417">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="098ce-417">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="098ce-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-419">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="098ce-419">Indicates the specific power-related capabilities of the logical device.</span></span> <span data-ttu-id="098ce-420">Значения массива 0 = "Unknown", 1 = "не поддерживается" и 2 = "Disabled" являются понятными.</span><span class="sxs-lookup"><span data-stu-id="098ce-420">The array values, 0="Unknown", 1="Not Supported" and 2="Disabled" are self-explanatory.</span></span> <span data-ttu-id="098ce-421">Значение 3 = "включено" указывает на то, что функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="098ce-421">The value, 3="Enabled" indicates that the power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span> <span data-ttu-id="098ce-422">"Режим энергосбережения задается автоматически" (4). описывает, что устройство может изменить свое состояние электропитания в зависимости от использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="098ce-422">"Power Saving Modes Entered Automatically" (4) describes that a device can change its power state based on usage or other criteria.</span></span> <span data-ttu-id="098ce-423">"Состояние электропитания, устанавливаемое" (5) указывает, что метод SetPowerState поддерживается.</span><span class="sxs-lookup"><span data-stu-id="098ce-423">"Power State Settable" (5) indicates that the SetPowerState method is supported.</span></span> <span data-ttu-id="098ce-424">"Цикл электропитания поддерживается" (6) указывает, что метод SetPowerState может быть вызван с помощью входной переменной PowerState, установленной в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="098ce-424">"Power Cycling Supported" (6) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle").</span></span> <span data-ttu-id="098ce-425">"Поддержка по времени ожидания" (7) указывает, что метод SetPowerState может быть вызван с помощью входной переменной PowerState, установленной в значение 5 ("цикл электропитания"), а параметр времени установлен на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="098ce-425">"Timed Power On Supported" (7) indicates that the SetPowerState method can be invoked with the PowerState input variable set to 5 ("Power Cycle") and the Time parameter set to a specific date and time, or interval, for power-on.</span></span>

<span data-ttu-id="098ce-426">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-426">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-427">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="098ce-427">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="098ce-428">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="098ce-428">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="098ce-429">**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="098ce-429">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="098ce-430">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="098ce-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="098ce-431">**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="098ce-431">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="098ce-432">**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="098ce-432">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="098ce-433">**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="098ce-433">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="098ce-434">**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="098ce-434">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-435">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="098ce-435">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-436">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-436">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-437">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-438">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="098ce-438">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="098ce-439">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="098ce-439">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="098ce-440">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-441">**поверонхаурс**</span><span class="sxs-lookup"><span data-stu-id="098ce-441">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-442">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-442">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-443">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-443">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-444">Число последовательных часов, в течение которых устройство было включено с момента последнего цикла электропитания.</span><span class="sxs-lookup"><span data-stu-id="098ce-444">The number of consecutive hours that this Device has been powered, since its last power cycle.</span></span>

<span data-ttu-id="098ce-445">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-445">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-446">**Основной раздел**</span><span class="sxs-lookup"><span data-stu-id="098ce-446">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-447">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-447">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-449">**Значение true**, если это основной раздел.</span><span class="sxs-lookup"><span data-stu-id="098ce-449">If **True**, this is the primary partition.</span></span>

<span data-ttu-id="098ce-450">Это свойство наследуется от [**CIM \_ дискпартитион**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-450">This property is inherited from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-451">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="098ce-451">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-452">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-454">Описание носителя и его использование.</span><span class="sxs-lookup"><span data-stu-id="098ce-454">Description of the media and its use.</span></span>

<span data-ttu-id="098ce-455">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-455">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-456">**ревритепартитион**</span><span class="sxs-lookup"><span data-stu-id="098ce-456">**RewritePartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-457">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="098ce-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-458">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-458">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-459">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API" \| входные и выходные структуры " \| [**\_ сведения о секции**](/windows/desktop/api/winioctl/ns-winioctl-partition_information) \| ревритепартитион")</span><span class="sxs-lookup"><span data-stu-id="098ce-459">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Device Input and Output Structures\|[**PARTITION\_INFORMATION**](/windows/desktop/api/winioctl/ns-winioctl-partition_information)\|RewritePartition")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-460">Если **значение — true**, сведения о секции изменились.</span><span class="sxs-lookup"><span data-stu-id="098ce-460">If **True**, the partition information has changed.</span></span> <span data-ttu-id="098ce-461">При изменении раздела (с [**\_ \_ \_ \_ разметкой**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)диска с помощью ioctl) система использует это свойство, чтобы определить, какие секции изменились и требуется перезаписывать их сведения.</span><span class="sxs-lookup"><span data-stu-id="098ce-461">When you change a partition (with [**IOCTL\_DISK\_SET\_DRIVE\_LAYOUT**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_disk_set_drive_layout)), the system uses this property to determine which partitions have changed and need their information rewritten.</span></span> <span data-ttu-id="098ce-462">Если **значение равно true**, необходимо перезаписывать секцию.</span><span class="sxs-lookup"><span data-stu-id="098ce-462">If **TRUE**, the partition must be rewritten.</span></span>

</dd> <dt>

<span data-ttu-id="098ce-463">**Размер**</span><span class="sxs-lookup"><span data-stu-id="098ce-463">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-464">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-464">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-465">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-465">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-466">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="098ce-466">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-467">Общий размер секции.</span><span class="sxs-lookup"><span data-stu-id="098ce-467">Total size of the partition.</span></span>

<span data-ttu-id="098ce-468">Пример: 1059045376</span><span class="sxs-lookup"><span data-stu-id="098ce-468">Example: 1059045376</span></span>

<span data-ttu-id="098ce-469">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="098ce-469">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-470">**стартингоффсет**</span><span class="sxs-lookup"><span data-stu-id="098ce-470">**StartingOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-471">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-471">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-473">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| File functions \| ReadFile"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span><span class="sxs-lookup"><span data-stu-id="098ce-473">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|File Functions\|ReadFile"), [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-474">Начальное смещение секции (в байтах).</span><span class="sxs-lookup"><span data-stu-id="098ce-474">Starting offset (in bytes) of the partition.</span></span>

<span data-ttu-id="098ce-475">Пример: 32256</span><span class="sxs-lookup"><span data-stu-id="098ce-475">Example: 32256</span></span>

<span data-ttu-id="098ce-476">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="098ce-476">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-477">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="098ce-477">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-478">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-480">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="098ce-480">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-481">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="098ce-481">Current status of the object.</span></span> <span data-ttu-id="098ce-482">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="098ce-482">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="098ce-483">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="098ce-483">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="098ce-484">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="098ce-484">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="098ce-485">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="098ce-485">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="098ce-486">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="098ce-486">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="098ce-487">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-487">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="098ce-488">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="098ce-488">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="098ce-489">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="098ce-489">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="098ce-490">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="098ce-490">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="098ce-491">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="098ce-491">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-492">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="098ce-492">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="098ce-493">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="098ce-493">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="098ce-494">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="098ce-494">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="098ce-495">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="098ce-495">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="098ce-496">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="098ce-496">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="098ce-497">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="098ce-497">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="098ce-498">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="098ce-498">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="098ce-499">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="098ce-499">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="098ce-500">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="098ce-500">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-501">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="098ce-501">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-502">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="098ce-502">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-503">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-503">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-504">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="098ce-504">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-505">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="098ce-505">State of the logical device.</span></span> <span data-ttu-id="098ce-506">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="098ce-506">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="098ce-507">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-507">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="098ce-508">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="098ce-508">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-509">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="098ce-509">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="098ce-510">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="098ce-510">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="098ce-511">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="098ce-511">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="098ce-512">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="098ce-512">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="098ce-513">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="098ce-513">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-514">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-515">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-515">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-516">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="098ce-516">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="098ce-517">Имя класса создания для системы области.</span><span class="sxs-lookup"><span data-stu-id="098ce-517">Creation class name of the scoping system.</span></span>

<span data-ttu-id="098ce-518">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-518">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-519">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="098ce-519">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-520">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-521">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-522">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="098ce-522">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="098ce-523">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="098ce-523">Name of the scoping system.</span></span>

<span data-ttu-id="098ce-524">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-524">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-525">**тоталповеронхаурс**</span><span class="sxs-lookup"><span data-stu-id="098ce-525">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-526">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="098ce-526">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-527">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="098ce-528">Общее количество часов, в течение которых устройство было включено.</span><span class="sxs-lookup"><span data-stu-id="098ce-528">The total number of hours that this device has been powered.</span></span>

<span data-ttu-id="098ce-529">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="098ce-529">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="098ce-530">**Тип**</span><span class="sxs-lookup"><span data-stu-id="098ce-530">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="098ce-531">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="098ce-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="098ce-532">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="098ce-532">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="098ce-533">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| партитионрекорд \| двпартитионтипе")</span><span class="sxs-lookup"><span data-stu-id="098ce-533">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|PartitionRecord\|dwPartitionType")</span></span>
</dt> </dl>

<span data-ttu-id="098ce-534">Тип секции.</span><span class="sxs-lookup"><span data-stu-id="098ce-534">Type of the partition.</span></span>

<span data-ttu-id="098ce-535">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="098ce-535">The values are:</span></span>

<dl> <dd><span data-ttu-id="098ce-536">Использующ</span><span class="sxs-lookup"><span data-stu-id="098ce-536">"Unused"</span></span></dd> <dd><span data-ttu-id="098ce-537">"12-разрядная система FAT"</span><span class="sxs-lookup"><span data-stu-id="098ce-537">"12-bit FAT"</span></span></dd> <dd><span data-ttu-id="098ce-538">"XENIX тип 1"</span><span class="sxs-lookup"><span data-stu-id="098ce-538">"Xenix Type 1"</span></span></dd> <dd><span data-ttu-id="098ce-539">"XENIX тип 2"</span><span class="sxs-lookup"><span data-stu-id="098ce-539">"Xenix Type 2"</span></span></dd> <dd><span data-ttu-id="098ce-540">16-разрядная система FAT</span><span class="sxs-lookup"><span data-stu-id="098ce-540">"16-bit FAT"</span></span></dd> <dd><span data-ttu-id="098ce-541">"Расширенный раздел"</span><span class="sxs-lookup"><span data-stu-id="098ce-541">"Extended Partition"</span></span></dd> <dd><span data-ttu-id="098ce-542">"MS-DOS v4 огромный"</span><span class="sxs-lookup"><span data-stu-id="098ce-542">"MS-DOS V4 Huge"</span></span></dd> <dd><span data-ttu-id="098ce-543">"Устанавливаемая файловая система"</span><span class="sxs-lookup"><span data-stu-id="098ce-543">"Installable File System"</span></span></dd> <dd><span data-ttu-id="098ce-544">"Эталонная платформа PowerPC"</span><span class="sxs-lookup"><span data-stu-id="098ce-544">"PowerPC Reference Platform"</span></span></dd> <dd><span data-ttu-id="098ce-545">UNIX</span><span class="sxs-lookup"><span data-stu-id="098ce-545">"UNIX"</span></span></dd> <dd><span data-ttu-id="098ce-546">NTFS</span><span class="sxs-lookup"><span data-stu-id="098ce-546">"NTFS"</span></span></dd> <dd><span data-ttu-id="098ce-547">"Win95 w/Extended INT 13"</span><span class="sxs-lookup"><span data-stu-id="098ce-547">"Win95 w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="098ce-548">"Расширенное w/Extended INT 13"</span><span class="sxs-lookup"><span data-stu-id="098ce-548">"Extended w/Extended Int 13"</span></span></dd> <dd><span data-ttu-id="098ce-549">"Диспетчер логических дисков"</span><span class="sxs-lookup"><span data-stu-id="098ce-549">"Logical Disk Manager"</span></span></dd> <dd><span data-ttu-id="098ce-550">Неизвестный</span><span class="sxs-lookup"><span data-stu-id="098ce-550">"Unknown"</span></span></dd> </dl>

<dt>

<span id="Unused"></span><span id="unused"></span><span id="UNUSED"></span>

<span data-ttu-id="098ce-551">Не **используется** ("не используется")</span><span class="sxs-lookup"><span data-stu-id="098ce-551">**Unused** ("Unused")</span></span>


</dt> <dd></dd> <dt>

<span id="12-bit_FAT"></span><span id="12-bit_fat"></span><span id="12-BIT_FAT"></span>

<span data-ttu-id="098ce-552">**12-разрядная система FAT** ("12-РАЗРЯДНАЯ система FAT")</span><span class="sxs-lookup"><span data-stu-id="098ce-552">**12-bit FAT** ("12-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_1"></span><span id="xenix_type_1"></span><span id="XENIX_TYPE_1"></span>

<span data-ttu-id="098ce-553">**Тип XENIX 1** ("тип XENIX 1")</span><span class="sxs-lookup"><span data-stu-id="098ce-553">**Xenix Type 1** ("Xenix Type 1")</span></span>


</dt> <dd></dd> <dt>

<span id="Xenix_Type_2"></span><span id="xenix_type_2"></span><span id="XENIX_TYPE_2"></span>

<span data-ttu-id="098ce-554">**Тип XENIX 2** ("XENIX тип 2")</span><span class="sxs-lookup"><span data-stu-id="098ce-554">**Xenix Type 2** ("Xenix Type 2")</span></span>


</dt> <dd></dd> <dt>

<span id="16-bit_FAT"></span><span id="16-bit_fat"></span><span id="16-BIT_FAT"></span>

<span data-ttu-id="098ce-555">**16-разрядная система FAT** (16-РАЗРЯДНАЯ система FAT)</span><span class="sxs-lookup"><span data-stu-id="098ce-555">**16-bit FAT** ("16-bit FAT")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_Partition"></span><span id="extended_partition"></span><span id="EXTENDED_PARTITION"></span>

<span data-ttu-id="098ce-556">**Расширенный раздел** ("Расширенный раздел")</span><span class="sxs-lookup"><span data-stu-id="098ce-556">**Extended Partition** ("Extended Partition")</span></span>


</dt> <dd></dd> <dt>

<span id="MS-DOS_V4_Huge"></span><span id="ms-dos_v4_huge"></span><span id="MS-DOS_V4_HUGE"></span>

<span data-ttu-id="098ce-557">**MS-DOS v4 огромный** ("MS-DOS v4 огромный")</span><span class="sxs-lookup"><span data-stu-id="098ce-557">**MS-DOS V4 Huge** ("MS-DOS V4 Huge")</span></span>


</dt> <dd></dd> <dt>

<span id="Installable_File_System"></span><span id="installable_file_system"></span><span id="INSTALLABLE_FILE_SYSTEM"></span>

<span data-ttu-id="098ce-558">**Устанавливаемая файловая система** ("устанавливаемая файловая система")</span><span class="sxs-lookup"><span data-stu-id="098ce-558">**Installable File System** ("Installable File System")</span></span>


</dt> <dd></dd> <dt>

<span id="PowerPC_Reference_Platform"></span><span id="powerpc_reference_platform"></span><span id="POWERPC_REFERENCE_PLATFORM"></span>

<span data-ttu-id="098ce-559">**Эталонная платформа PowerPC** ("Эталонная платформа PowerPC")</span><span class="sxs-lookup"><span data-stu-id="098ce-559">**PowerPC Reference Platform** ("PowerPC Reference Platform")</span></span>


</dt> <dd></dd> <dt>

<span id="UNIX"></span><span id="unix"></span>

<span data-ttu-id="098ce-560">**UNIX** (UNIX)</span><span class="sxs-lookup"><span data-stu-id="098ce-560">**UNIX** ("UNIX")</span></span>


</dt> <dd></dd> <dt>

<span id="NTFS"></span><span id="ntfs"></span>

<span data-ttu-id="098ce-561">**NTFS** ("NTFS")</span><span class="sxs-lookup"><span data-stu-id="098ce-561">**NTFS** ("NTFS")</span></span>


</dt> <dd></dd> <dt>

<span id="Win95_w_Extended_Int_13"></span><span id="win95_w_extended_int_13"></span><span id="WIN95_W_EXTENDED_INT_13"></span>

<span data-ttu-id="098ce-562">**Win95 с расширенным INT 13** ("Win95 w/Extended INT 13")</span><span class="sxs-lookup"><span data-stu-id="098ce-562">**Win95 w/Extended Int 13** ("Win95 w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Extended_w_Extended_Int_13"></span><span id="extended_w_extended_int_13"></span><span id="EXTENDED_W_EXTENDED_INT_13"></span>

<span data-ttu-id="098ce-563">**Расширенное w/Extended INT 13** ("расширенное w/Extended INT 13")</span><span class="sxs-lookup"><span data-stu-id="098ce-563">**Extended w/Extended Int 13** ("Extended w/Extended Int 13")</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk_Manager"></span><span id="logical_disk_manager"></span><span id="LOGICAL_DISK_MANAGER"></span>

<span data-ttu-id="098ce-564">**Диспетчер логических дисков** ("Диспетчер логических дисков")</span><span class="sxs-lookup"><span data-stu-id="098ce-564">**Logical Disk Manager** ("Logical Disk Manager")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="098ce-565">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="098ce-565">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="098ce-566"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="098ce-566"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="098ce-567">Комментарии</span><span class="sxs-lookup"><span data-stu-id="098ce-567">Remarks</span></span>

<span data-ttu-id="098ce-568">Класс **Win32 \_ дискпартитион** является производным от [**CIM \_ дискпартитион**](cim-diskpartition.md).</span><span class="sxs-lookup"><span data-stu-id="098ce-568">The **Win32\_DiskPartition** class is derived from [**CIM\_DiskPartition**](cim-diskpartition.md).</span></span>

<span data-ttu-id="098ce-569">Секция — это структурное разделение физического диска.</span><span class="sxs-lookup"><span data-stu-id="098ce-569">A partition is a structural division of a physical disk drive.</span></span> <span data-ttu-id="098ce-570">Хотя диск может содержать один раздел, большие тома часто делятся на несколько разделов.</span><span class="sxs-lookup"><span data-stu-id="098ce-570">Although a drive can contain a single partition, larger volumes are often divided into multiple partitions.</span></span> <span data-ttu-id="098ce-571">Именно поэтому у вас могут быть диски C, D и E, даже если компьютер имеет только один физический жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="098ce-571">This is why you might have drives C, D, and E even though your computer has only a single physical hard disk.</span></span>

<span data-ttu-id="098ce-572">Windows поддерживает следующие типы разделов:</span><span class="sxs-lookup"><span data-stu-id="098ce-572">Windows supports the following partition types:</span></span>

-   <span data-ttu-id="098ce-573">Основной раздел.</span><span class="sxs-lookup"><span data-stu-id="098ce-573">Primary partition.</span></span> <span data-ttu-id="098ce-574">Это единственный тип раздела, на котором может быть установлена операционная система.</span><span class="sxs-lookup"><span data-stu-id="098ce-574">This is the only type of partition that can have an operating system installed.</span></span> <span data-ttu-id="098ce-575">Каждый диск может иметь до четырех основных разделов, каждому из которых назначена другая буква диска.</span><span class="sxs-lookup"><span data-stu-id="098ce-575">Each drive can have as many as four primary partitions, each assigned a different drive letter.</span></span>
-   <span data-ttu-id="098ce-576">Дополнительный раздел.</span><span class="sxs-lookup"><span data-stu-id="098ce-576">Extended partition.</span></span> <span data-ttu-id="098ce-577">Дополнительный раздел, который можно разделить на несколько логических дисков, каждому из которых назначена уникальная буква диска.</span><span class="sxs-lookup"><span data-stu-id="098ce-577">An additional partition that can be subdivided into multiple logical drives, each assigned a unique drive letter.</span></span> <span data-ttu-id="098ce-578">На диске может быть только один дополнительный раздел; Тем не менее этот раздел можно разделить на несколько логических дисков.</span><span class="sxs-lookup"><span data-stu-id="098ce-578">A drive can have only one extended partition; however, you can divide this partition into multiple logical drives.</span></span> <span data-ttu-id="098ce-579">Это позволяет диску иметь не более четырех допустимых первичных разделов.</span><span class="sxs-lookup"><span data-stu-id="098ce-579">This enables a disk to have more than just the four allowed primary partitions.</span></span>
-   <span data-ttu-id="098ce-580">Системный раздел.</span><span class="sxs-lookup"><span data-stu-id="098ce-580">System partition.</span></span> <span data-ttu-id="098ce-581">Любой основной раздел, содержащий операционную систему.</span><span class="sxs-lookup"><span data-stu-id="098ce-581">Any primary partition containing an operating system.</span></span>

<span data-ttu-id="098ce-582">Разделы могут сообщить, как фактически используется физический диск.</span><span class="sxs-lookup"><span data-stu-id="098ce-582">Partitions can tell you how a physical disk drive is actually being used.</span></span> <span data-ttu-id="098ce-583">Изучив физические разделы на диске, можно определить следующие типы действий:</span><span class="sxs-lookup"><span data-stu-id="098ce-583">By examining the physical partitions on a disk, you can determine the following types of things:</span></span>

-   <span data-ttu-id="098ce-584">Как диск делится на логические диски.</span><span class="sxs-lookup"><span data-stu-id="098ce-584">How the disk has been divided into logical drives.</span></span>
-   <span data-ttu-id="098ce-585">Если на диске доступно несекционированное пространство,</span><span class="sxs-lookup"><span data-stu-id="098ce-585">If there is unpartitioned space available on the disk.</span></span> <span data-ttu-id="098ce-586">Это можно определить путем вычитания размера всех разделов на диске из размера самого диска.</span><span class="sxs-lookup"><span data-stu-id="098ce-586">This can be determined by subtracting the size of all the partitions on a disk from the size of the disk itself.</span></span>
-   <span data-ttu-id="098ce-587">Если можно загрузить компьютер с этого диска (то есть диск содержит загрузочный раздел).</span><span class="sxs-lookup"><span data-stu-id="098ce-587">If you can boot the computer from that disk (that is, does the disk contain a boot partition).</span></span>

<span data-ttu-id="098ce-588">Все эти вопросы можно устранить с помощью класса **Win32 \_ дискпартитион** .</span><span class="sxs-lookup"><span data-stu-id="098ce-588">All these questions can be resolved by using the **Win32\_DiskPartition** class.</span></span>

## <a name="examples"></a><span data-ttu-id="098ce-589">Примеры</span><span class="sxs-lookup"><span data-stu-id="098ce-589">Examples</span></span>

<span data-ttu-id="098ce-590">Следующий пример кода PowerShell проверяет выравнивание дисков на компьютере: Если смещение имеет дробное значение, диск не выровнен правильно.</span><span class="sxs-lookup"><span data-stu-id="098ce-590">The following PowerShell code sample checks the alignment of disks on a computer: if the offset is fractional, the disk is not aligned correctly.</span></span>


```PowerShell
$wql = "SELECT DiskIndex,Index,StartingOffset FROM Win32_DiskPartition"
Get-WmiObject -Query $wql -ComputerName '.' | Select-Object DiskIndex,Index,@{Name='Offset (KB)';Expression={$_.StartingOffset / 1024}} | Format-Table -AutoSize
```



## <a name="requirements"></a><span data-ttu-id="098ce-591">Требования</span><span class="sxs-lookup"><span data-stu-id="098ce-591">Requirements</span></span>



| <span data-ttu-id="098ce-592">Требование</span><span class="sxs-lookup"><span data-stu-id="098ce-592">Requirement</span></span> | <span data-ttu-id="098ce-593">Значение</span><span class="sxs-lookup"><span data-stu-id="098ce-593">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="098ce-594">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="098ce-594">Minimum supported client</span></span><br/> | <span data-ttu-id="098ce-595">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="098ce-595">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="098ce-596">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="098ce-596">Minimum supported server</span></span><br/> | <span data-ttu-id="098ce-597">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="098ce-597">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="098ce-598">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="098ce-598">Namespace</span></span><br/>                | <span data-ttu-id="098ce-599">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="098ce-599">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="098ce-600">MOF</span><span class="sxs-lookup"><span data-stu-id="098ce-600">MOF</span></span><br/>                      | <dl> <span data-ttu-id="098ce-601"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="098ce-601"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="098ce-602">DLL</span><span class="sxs-lookup"><span data-stu-id="098ce-602">DLL</span></span><br/>                      | <dl> <span data-ttu-id="098ce-603"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="098ce-603"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098ce-604">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="098ce-604">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098ce-605">**\_ДИСКПАРТИТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="098ce-605">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dt>

<span data-ttu-id="098ce-606">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="098ce-606">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="098ce-607">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="098ce-607">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

