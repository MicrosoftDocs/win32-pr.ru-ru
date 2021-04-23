---
description: Класс набора \_ ТОМОВ CIM представляет непрерывный диапазон логических блоков, представленных в операционной среде для чтения и записи пользовательских данных.
ms.assetid: f0350185-6210-4f95-a2a2-23de61b1af1f
ms.tgt_platform: multiple
title: Класс CIM_VolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VolumeSet
- CIM_VolumeSet.Access
- CIM_VolumeSet.Availability
- CIM_VolumeSet.BlockSize
- CIM_VolumeSet.Caption
- CIM_VolumeSet.ConfigManagerErrorCode
- CIM_VolumeSet.ConfigManagerUserConfig
- CIM_VolumeSet.CreationClassName
- CIM_VolumeSet.Description
- CIM_VolumeSet.DeviceID
- CIM_VolumeSet.ErrorCleared
- CIM_VolumeSet.ErrorDescription
- CIM_VolumeSet.ErrorMethodology
- CIM_VolumeSet.InstallDate
- CIM_VolumeSet.LastErrorCode
- CIM_VolumeSet.Name
- CIM_VolumeSet.NumberOfBlocks
- CIM_VolumeSet.PNPDeviceID
- CIM_VolumeSet.PowerManagementCapabilities
- CIM_VolumeSet.PowerManagementSupported
- CIM_VolumeSet.PSExtentInterleaveDepth
- CIM_VolumeSet.PSExtentStripeLength
- CIM_VolumeSet.Purpose
- CIM_VolumeSet.Status
- CIM_VolumeSet.StatusInfo
- CIM_VolumeSet.SystemCreationClassName
- CIM_VolumeSet.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7ee8cd96381901250c9a15e544ee1963470565b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655723"
---
# <a name="cim_volumeset-class"></a><span data-ttu-id="95da2-103">\_Класс многотомногоing в CIM</span><span class="sxs-lookup"><span data-stu-id="95da2-103">CIM\_VolumeSet class</span></span>

<span data-ttu-id="95da2-104">Класс **набора \_ томов CIM** представляет непрерывный диапазон логических блоков, представленных в операционной среде для чтения и записи пользовательских данных.</span><span class="sxs-lookup"><span data-stu-id="95da2-104">The **CIM\_VolumeSet** class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span> <span data-ttu-id="95da2-105">Наборы томов не должны перекрывать друг друга и основаны на одном или нескольких физических экстентах, защищенных экстентах или агрегатных экстентах (все они одного типа).</span><span class="sxs-lookup"><span data-stu-id="95da2-105">Volume sets should not overlap one another and are based on one or more physical extents, protected space extents, or aggregate extents (all of the same type).</span></span> <span data-ttu-id="95da2-106">При необходимости экземпляры на основе сопоставления должны быть созданы или подклассаны.</span><span class="sxs-lookup"><span data-stu-id="95da2-106">The based-on associations should be instantiated or subclassed as needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="95da2-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="95da2-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="95da2-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="95da2-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="95da2-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="95da2-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="95da2-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="95da2-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95da2-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95da2-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{35E25AA5-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_VolumeSet : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint64   PSExtentInterleaveDepth;
  uint64   PSExtentStripeLength;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="95da2-112">Члены</span><span class="sxs-lookup"><span data-stu-id="95da2-112">Members</span></span>

<span data-ttu-id="95da2-113">Класс **набора \_ томов CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="95da2-113">The **CIM\_VolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="95da2-114">Методы</span><span class="sxs-lookup"><span data-stu-id="95da2-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="95da2-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="95da2-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="95da2-116">Методы</span><span class="sxs-lookup"><span data-stu-id="95da2-116">Methods</span></span>

<span data-ttu-id="95da2-117">Класс **\_ томов CIM** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="95da2-117">The **CIM\_VolumeSet** class has these methods.</span></span>



| <span data-ttu-id="95da2-118">Метод</span><span class="sxs-lookup"><span data-stu-id="95da2-118">Method</span></span>                                                               | <span data-ttu-id="95da2-119">Описание</span><span class="sxs-lookup"><span data-stu-id="95da2-119">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95da2-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="95da2-120">**Reset**</span></span>](reset-method-in-class-cim-volumeset.md)                 | <span data-ttu-id="95da2-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="95da2-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="95da2-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="95da2-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="95da2-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-volumeset.md) | <span data-ttu-id="95da2-124">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="95da2-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="95da2-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="95da2-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="95da2-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="95da2-126">Properties</span></span>

<span data-ttu-id="95da2-127">Класс **\_ тома CIM** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="95da2-127">The **CIM\_VolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95da2-128">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="95da2-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95da2-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-131">Чтение и запись свойств носителя.</span><span class="sxs-lookup"><span data-stu-id="95da2-131">Read/write properties of the media.</span></span>

<span data-ttu-id="95da2-132">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95da2-133">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="95da2-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="95da2-134">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="95da2-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="95da2-135">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="95da2-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="95da2-136">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="95da2-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="95da2-137">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="95da2-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95da2-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="95da2-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95da2-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-141">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="95da2-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-142">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-142">Availability and status of the device.</span></span>

<span data-ttu-id="95da2-143">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95da2-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="95da2-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95da2-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="95da2-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="95da2-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="95da2-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="95da2-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="95da2-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="95da2-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="95da2-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95da2-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="95da2-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="95da2-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="95da2-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="95da2-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="95da2-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="95da2-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="95da2-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95da2-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="95da2-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="95da2-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="95da2-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="95da2-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="95da2-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="95da2-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="95da2-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-157">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="95da2-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="95da2-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="95da2-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-159">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="95da2-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="95da2-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="95da2-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-161">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="95da2-161">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="95da2-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="95da2-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="95da2-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="95da2-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-164">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="95da2-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="95da2-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="95da2-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-166">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="95da2-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="95da2-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="95da2-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-168">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="95da2-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="95da2-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="95da2-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-170">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="95da2-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="95da2-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="95da2-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-172">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="95da2-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95da2-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="95da2-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-174">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95da2-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-176">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="95da2-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-177">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="95da2-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="95da2-178">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="95da2-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="95da2-179">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="95da2-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="95da2-180">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-180">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="95da2-181">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="95da2-181">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-182">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="95da2-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-185">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="95da2-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-186">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="95da2-186">Short textual description of the object.</span></span>

<span data-ttu-id="95da2-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-188">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="95da2-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-189">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95da2-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-191">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="95da2-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-192">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="95da2-192">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="95da2-193">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="95da2-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="95da2-194"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="95da2-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="95da2-195">(0)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-196">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="95da2-196">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="95da2-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="95da2-197"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="95da2-198">(1)</span><span class="sxs-lookup"><span data-stu-id="95da2-198">(1)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-199">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="95da2-199">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="95da2-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-200"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="95da2-201">(2)</span><span class="sxs-lookup"><span data-stu-id="95da2-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="95da2-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="95da2-202"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="95da2-203">(3)</span><span class="sxs-lookup"><span data-stu-id="95da2-203">(3)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-204">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95da2-204">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="95da2-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="95da2-205"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="95da2-206">(4)</span><span class="sxs-lookup"><span data-stu-id="95da2-206">(4)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-207">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="95da2-207">Device is not working properly.</span></span> <span data-ttu-id="95da2-208">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="95da2-208">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="95da2-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="95da2-209"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="95da2-210">(5)</span><span class="sxs-lookup"><span data-stu-id="95da2-210">(5)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-211">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="95da2-211">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="95da2-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="95da2-212"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="95da2-213"> (6)</span><span class="sxs-lookup"><span data-stu-id="95da2-213">(6)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-214">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="95da2-214">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="95da2-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="95da2-215"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="95da2-216">(7)</span><span class="sxs-lookup"><span data-stu-id="95da2-216">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="95da2-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-217"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="95da2-218">(8)</span><span class="sxs-lookup"><span data-stu-id="95da2-218">(8)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-219">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-219">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="95da2-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-220"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="95da2-221">(9)</span><span class="sxs-lookup"><span data-stu-id="95da2-221">(9)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-222">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="95da2-222">Device is not working properly.</span></span> <span data-ttu-id="95da2-223">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-223">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="95da2-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="95da2-224"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="95da2-225">(10)</span><span class="sxs-lookup"><span data-stu-id="95da2-225">(10)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-226">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="95da2-226">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="95da2-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-227"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="95da2-228">(11)</span><span class="sxs-lookup"><span data-stu-id="95da2-228">(11)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-229">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-229">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="95da2-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="95da2-230"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="95da2-231">(12)</span><span class="sxs-lookup"><span data-stu-id="95da2-231">(12)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-232">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="95da2-232">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="95da2-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-233"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="95da2-234">(13)</span><span class="sxs-lookup"><span data-stu-id="95da2-234">(13)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-235">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-235">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="95da2-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="95da2-236"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="95da2-237">(14)</span><span class="sxs-lookup"><span data-stu-id="95da2-237">(14)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-238">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="95da2-238">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="95da2-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="95da2-239"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="95da2-240">(15)</span><span class="sxs-lookup"><span data-stu-id="95da2-240">(15)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-241">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="95da2-241">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="95da2-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="95da2-242"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="95da2-243">(16)</span><span class="sxs-lookup"><span data-stu-id="95da2-243">(16)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-244">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="95da2-244">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="95da2-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="95da2-245"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="95da2-246">(17)</span><span class="sxs-lookup"><span data-stu-id="95da2-246">(17)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-247">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="95da2-247">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="95da2-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-248"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="95da2-249">(18)</span><span class="sxs-lookup"><span data-stu-id="95da2-249">(18)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-250">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="95da2-250">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="95da2-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="95da2-251"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="95da2-252">(19)</span><span class="sxs-lookup"><span data-stu-id="95da2-252">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="95da2-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="95da2-253"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="95da2-254">(20)</span><span class="sxs-lookup"><span data-stu-id="95da2-254">(20)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-255">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="95da2-255">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="95da2-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="95da2-256"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="95da2-257">(21)</span><span class="sxs-lookup"><span data-stu-id="95da2-257">(21)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-258">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="95da2-258">System failure.</span></span> <span data-ttu-id="95da2-259">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="95da2-259">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="95da2-260">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="95da2-260">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="95da2-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="95da2-261"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="95da2-262">(22)</span><span class="sxs-lookup"><span data-stu-id="95da2-262">(22)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-263">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="95da2-263">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="95da2-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="95da2-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="95da2-265">(23)</span><span class="sxs-lookup"><span data-stu-id="95da2-265">(23)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-266">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="95da2-266">System failure.</span></span> <span data-ttu-id="95da2-267">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="95da2-267">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="95da2-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="95da2-268"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="95da2-269">(24)</span><span class="sxs-lookup"><span data-stu-id="95da2-269">(24)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-270">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="95da2-270">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="95da2-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="95da2-271"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="95da2-272">(25)</span><span class="sxs-lookup"><span data-stu-id="95da2-272">(25)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-273">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="95da2-273">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="95da2-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="95da2-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="95da2-275">(26)</span><span class="sxs-lookup"><span data-stu-id="95da2-275">(26)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-276">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="95da2-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="95da2-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="95da2-277"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="95da2-278">(27)</span><span class="sxs-lookup"><span data-stu-id="95da2-278">(27)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-279">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="95da2-279">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="95da2-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="95da2-280"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="95da2-281">(28)</span><span class="sxs-lookup"><span data-stu-id="95da2-281">(28)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-282">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="95da2-282">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="95da2-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="95da2-283"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="95da2-284">(29)</span><span class="sxs-lookup"><span data-stu-id="95da2-284">(29)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-285">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="95da2-285">Device is disabled.</span></span> <span data-ttu-id="95da2-286">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="95da2-286">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="95da2-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="95da2-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="95da2-288">(30)</span><span class="sxs-lookup"><span data-stu-id="95da2-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-289">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="95da2-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="95da2-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="95da2-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="95da2-291">1-31</span><span class="sxs-lookup"><span data-stu-id="95da2-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-292">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="95da2-292">Device is not working properly.</span></span> <span data-ttu-id="95da2-293">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="95da2-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95da2-294">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="95da2-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-295">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="95da2-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-297">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="95da2-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-298">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="95da2-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="95da2-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="95da2-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-303">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95da2-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95da2-304">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="95da2-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="95da2-305">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="95da2-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="95da2-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-307">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95da2-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-310">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="95da2-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-311">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="95da2-311">Textual description of the object.</span></span>

<span data-ttu-id="95da2-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="95da2-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-316">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95da2-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95da2-317">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="95da2-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-319">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="95da2-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-320">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="95da2-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-322">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="95da2-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="95da2-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="95da2-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-327">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="95da2-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="95da2-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-329">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="95da2-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-332">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="95da2-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="95da2-333">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="95da2-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-335">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="95da2-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="95da2-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-338">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="95da2-338">Date and time the object was installed.</span></span> <span data-ttu-id="95da2-339">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="95da2-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="95da2-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-341">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="95da2-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-342">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="95da2-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-344">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="95da2-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="95da2-345">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-346">**Name**</span><span class="sxs-lookup"><span data-stu-id="95da2-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-349">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="95da2-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-350">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="95da2-350">Label by which the object is known.</span></span> <span data-ttu-id="95da2-351">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="95da2-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="95da2-352">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="95da2-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-354">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95da2-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-356">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="95da2-356">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-357">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="95da2-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="95da2-358">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="95da2-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="95da2-359">Если **значение параметра DataSize равно 1** (один), это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="95da2-359">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="95da2-360">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="95da2-361">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="95da2-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="95da2-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-365">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="95da2-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-366">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="95da2-367">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="95da2-368">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="95da2-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="95da2-369">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="95da2-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-370">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="95da2-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="95da2-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-372">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="95da2-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="95da2-373">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95da2-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="95da2-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="95da2-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="95da2-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95da2-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="95da2-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="95da2-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="95da2-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-378">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="95da2-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="95da2-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="95da2-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-380">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="95da2-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="95da2-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="95da2-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-382">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="95da2-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="95da2-383">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="95da2-383">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="95da2-384">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="95da2-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="95da2-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="95da2-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-386">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="95da2-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="95da2-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="95da2-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="95da2-388">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="95da2-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="95da2-389">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="95da2-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-390">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="95da2-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-392">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="95da2-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="95da2-393">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="95da2-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="95da2-394">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="95da2-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="95da2-395">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="95da2-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="95da2-396">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-397">**псекстентинтерлеаведепс**</span><span class="sxs-lookup"><span data-stu-id="95da2-397">**PSExtentInterleaveDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-398">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95da2-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-400">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Volume Set \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="95da2-400">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-401">Количество экстентов защищенного пространства, которое можно распределить как совокупный набор.</span><span class="sxs-lookup"><span data-stu-id="95da2-401">Number of protected space extents to stripe as a collective set.</span></span> <span data-ttu-id="95da2-402">В SCC это значение определяется как число полос, подлежащих подсчету, прежде чем продолжить соотнесение со следующим непрерывным набором экстентов, за пределами текущей полосы.</span><span class="sxs-lookup"><span data-stu-id="95da2-402">In SCC, this value is defined as the number of stripes to count before continuing to map into the next contiguous set of extents, beyond the current stripe.</span></span>

<span data-ttu-id="95da2-403">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="95da2-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-404">**псекстентстрипеленгс**</span><span class="sxs-lookup"><span data-stu-id="95da2-404">**PSExtentStripeLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-405">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="95da2-405">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-407">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| Volume Set \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="95da2-407">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Volume Set\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-408">Количество смежных областей защищенного пространства, подсчитанных до возвращения в первую область защищенного пространства текущей полосы.</span><span class="sxs-lookup"><span data-stu-id="95da2-408">Number of contiguous protected space extents counted before looping back to the first protected space extent of the current stripe.</span></span> <span data-ttu-id="95da2-409">Это количество экстентов, формирующих полосу данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="95da2-409">It is the number of extents forming the user data stripe.</span></span>

<span data-ttu-id="95da2-410">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="95da2-410">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-411">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="95da2-411">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-412">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="95da2-414">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="95da2-414">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="95da2-415">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-415">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-416">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="95da2-416">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-417">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-419">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="95da2-419">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-420">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="95da2-420">Current status of the object.</span></span> <span data-ttu-id="95da2-421">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="95da2-422">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="95da2-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="95da2-423">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="95da2-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="95da2-424">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="95da2-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="95da2-425">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="95da2-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95da2-426">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="95da2-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="95da2-427">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="95da2-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="95da2-428">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="95da2-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="95da2-429">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="95da2-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="95da2-430">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="95da2-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="95da2-431">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="95da2-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="95da2-432">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="95da2-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="95da2-433">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="95da2-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="95da2-434">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="95da2-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95da2-435">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="95da2-435">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-436">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="95da2-436">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-437">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-438">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="95da2-438">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="95da2-439">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="95da2-439">State of the logical device.</span></span> <span data-ttu-id="95da2-440">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="95da2-440">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="95da2-441">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-441">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="95da2-442">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="95da2-442">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="95da2-443">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="95da2-443">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="95da2-444">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="95da2-444">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="95da2-445">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="95da2-445">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="95da2-446">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="95da2-446">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="95da2-447">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="95da2-447">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-448">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-449">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-449">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-450">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95da2-450">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95da2-451">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="95da2-451">Scoping system's creation class name.</span></span>

<span data-ttu-id="95da2-452">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-452">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="95da2-453">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="95da2-453">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95da2-454">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="95da2-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="95da2-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="95da2-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95da2-456">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="95da2-456">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="95da2-457">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="95da2-457">Scoping system's name.</span></span>

<span data-ttu-id="95da2-458">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="95da2-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95da2-459">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95da2-459">Remarks</span></span>

<span data-ttu-id="95da2-460">Класс **\_ тома CIM** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="95da2-460">The **CIM\_VolumeSet** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="95da2-461">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="95da2-461">WMI does not implement this class.</span></span>

<span data-ttu-id="95da2-462">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="95da2-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="95da2-463">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="95da2-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="95da2-464">Требования</span><span class="sxs-lookup"><span data-stu-id="95da2-464">Requirements</span></span>



| <span data-ttu-id="95da2-465">Требование</span><span class="sxs-lookup"><span data-stu-id="95da2-465">Requirement</span></span> | <span data-ttu-id="95da2-466">Значение</span><span class="sxs-lookup"><span data-stu-id="95da2-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95da2-467">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95da2-467">Minimum supported client</span></span><br/> | <span data-ttu-id="95da2-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95da2-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95da2-469">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95da2-469">Minimum supported server</span></span><br/> | <span data-ttu-id="95da2-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95da2-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95da2-471">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="95da2-471">Namespace</span></span><br/>                | <span data-ttu-id="95da2-472">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="95da2-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95da2-473">MOF</span><span class="sxs-lookup"><span data-stu-id="95da2-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95da2-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95da2-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95da2-475">DLL</span><span class="sxs-lookup"><span data-stu-id="95da2-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95da2-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95da2-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95da2-477">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95da2-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95da2-478">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="95da2-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

