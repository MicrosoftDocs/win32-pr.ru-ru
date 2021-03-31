---
description: Класс CIM \_ дискпартитион представляет непрерывный диапазон логических блоков, идентифицируемый операционной системой посредством полей типа и подтипа секции.
ms.assetid: 22a0e5be-c66b-40a2-9a7a-047d2edc0278
ms.tgt_platform: multiple
title: Класс CIM_DiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskPartition
- CIM_DiskPartition.Access
- CIM_DiskPartition.Availability
- CIM_DiskPartition.BlockSize
- CIM_DiskPartition.Bootable
- CIM_DiskPartition.Caption
- CIM_DiskPartition.ConfigManagerErrorCode
- CIM_DiskPartition.ConfigManagerUserConfig
- CIM_DiskPartition.CreationClassName
- CIM_DiskPartition.Description
- CIM_DiskPartition.DeviceID
- CIM_DiskPartition.ErrorCleared
- CIM_DiskPartition.ErrorDescription
- CIM_DiskPartition.ErrorMethodology
- CIM_DiskPartition.InstallDate
- CIM_DiskPartition.LastErrorCode
- CIM_DiskPartition.Name
- CIM_DiskPartition.NumberOfBlocks
- CIM_DiskPartition.PNPDeviceID
- CIM_DiskPartition.PowerManagementCapabilities
- CIM_DiskPartition.PowerManagementSupported
- CIM_DiskPartition.PrimaryPartition
- CIM_DiskPartition.Purpose
- CIM_DiskPartition.Status
- CIM_DiskPartition.StatusInfo
- CIM_DiskPartition.SystemCreationClassName
- CIM_DiskPartition.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d1761e140813c26e67594872df5a8d2f7361768b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896165"
---
# <a name="cim_diskpartition-class"></a><span data-ttu-id="20ac7-103">\_Класс CIM дискпартитион</span><span class="sxs-lookup"><span data-stu-id="20ac7-103">CIM\_DiskPartition class</span></span>

<span data-ttu-id="20ac7-104">Класс **CIM \_ дискпартитион** представляет непрерывный диапазон логических блоков, идентифицируемый операционной системой посредством полей типа и подтипа секции.</span><span class="sxs-lookup"><span data-stu-id="20ac7-104">The **CIM\_DiskPartition** class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="20ac7-105">Разделы диска должны быть непосредственно реализованы физическим носителем (обозначено ассоциацией [**CIM \_ реализесдискпартитион**](cim-realizesdiskpartition.md) ) или созданы на томах хранения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-105">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="20ac7-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="20ac7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="20ac7-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="20ac7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="20ac7-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="20ac7-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="20ac7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ac7-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20ac7-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C541-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DiskPartition : CIM_StorageExtent
{
  uint16   Access;
  uint16   Availability;
  uint64   BlockSize;
  boolean  Bootable;
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
  boolean  PrimaryPartition;
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="20ac7-111">Члены</span><span class="sxs-lookup"><span data-stu-id="20ac7-111">Members</span></span>

<span data-ttu-id="20ac7-112">Класс **CIM \_ дискпартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="20ac7-112">The **CIM\_DiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="20ac7-113">Методы</span><span class="sxs-lookup"><span data-stu-id="20ac7-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="20ac7-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="20ac7-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20ac7-115">Методы</span><span class="sxs-lookup"><span data-stu-id="20ac7-115">Methods</span></span>

<span data-ttu-id="20ac7-116">Класс **CIM \_ дискпартитион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="20ac7-116">The **CIM\_DiskPartition** class has these methods.</span></span>



| <span data-ttu-id="20ac7-117">Метод</span><span class="sxs-lookup"><span data-stu-id="20ac7-117">Method</span></span>                                                                   | <span data-ttu-id="20ac7-118">Описание</span><span class="sxs-lookup"><span data-stu-id="20ac7-118">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20ac7-119">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="20ac7-119">**Reset**</span></span>](reset-method-in-class-cim-diskpartition.md)                 | <span data-ttu-id="20ac7-120">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="20ac7-121">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="20ac7-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="20ac7-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="20ac7-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-diskpartition.md) | <span data-ttu-id="20ac7-123">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="20ac7-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="20ac7-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="20ac7-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="20ac7-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="20ac7-125">Properties</span></span>

<span data-ttu-id="20ac7-126">Класс **CIM \_ дискпартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-126">The **CIM\_DiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20ac7-127">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="20ac7-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20ac7-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-130">Указывает, например, доступен ли носитель для чтения, записи или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="20ac7-130">Specifies whether the media is readable, writeable, or both, for example.</span></span> <span data-ttu-id="20ac7-131">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20ac7-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="20ac7-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-133">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="20ac7-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="20ac7-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="20ac7-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-135">Чтения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="20ac7-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="20ac7-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-137">Возможностью записи.</span><span class="sxs-lookup"><span data-stu-id="20ac7-137">Writeable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="20ac7-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="20ac7-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-139">Поддерживается чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="20ac7-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="20ac7-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="20ac7-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-141">Однократная запись.</span><span class="sxs-lookup"><span data-stu-id="20ac7-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20ac7-142">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="20ac7-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20ac7-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="20ac7-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-146">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-146">Availability and status of the device.</span></span>

<span data-ttu-id="20ac7-147">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20ac7-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="20ac7-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20ac7-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="20ac7-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="20ac7-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="20ac7-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="20ac7-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="20ac7-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="20ac7-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="20ac7-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20ac7-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="20ac7-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="20ac7-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="20ac7-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="20ac7-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="20ac7-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="20ac7-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="20ac7-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20ac7-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="20ac7-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="20ac7-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="20ac7-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="20ac7-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="20ac7-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="20ac7-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="20ac7-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-161">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="20ac7-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="20ac7-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="20ac7-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-163">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="20ac7-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="20ac7-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="20ac7-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-165">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="20ac7-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="20ac7-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="20ac7-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="20ac7-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="20ac7-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-168">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="20ac7-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="20ac7-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-170">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="20ac7-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="20ac7-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="20ac7-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-172">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="20ac7-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="20ac7-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="20ac7-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-174">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="20ac7-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="20ac7-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="20ac7-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-176">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="20ac7-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20ac7-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="20ac7-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-178">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20ac7-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-180">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="20ac7-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-181">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="20ac7-182">Если это переменный размер блока, следует указать максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="20ac7-182">If it is a variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="20ac7-183">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите значение 1.</span><span class="sxs-lookup"><span data-stu-id="20ac7-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter the value 1.</span></span>

<span data-ttu-id="20ac7-184">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="20ac7-185">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20ac7-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-186">**Загружаемый**</span><span class="sxs-lookup"><span data-stu-id="20ac7-186">**Bootable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-187">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="20ac7-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-189">Если **значение — true**, раздел диска помечается как загрузочный.</span><span class="sxs-lookup"><span data-stu-id="20ac7-189">If **TRUE**, the disk partition is labeled as bootable.</span></span> <span data-ttu-id="20ac7-190">Это не означает, что операционная система загружена в раздел.</span><span class="sxs-lookup"><span data-stu-id="20ac7-190">This does not mean that an operating system is loaded on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-191">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="20ac7-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-194">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="20ac7-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-195">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="20ac7-195">Short textual description of the object.</span></span>

<span data-ttu-id="20ac7-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-197">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="20ac7-197">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-198">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20ac7-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-200">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20ac7-200">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-201">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="20ac7-201">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="20ac7-202">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-202">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="20ac7-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-203"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="20ac7-204"> (0)</span><span class="sxs-lookup"><span data-stu-id="20ac7-204">(0)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-205">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="20ac7-205">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="20ac7-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-206"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="20ac7-207">(1)</span><span class="sxs-lookup"><span data-stu-id="20ac7-207">(1)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-208">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="20ac7-208">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20ac7-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-209"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="20ac7-210">(2)</span><span class="sxs-lookup"><span data-stu-id="20ac7-210">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="20ac7-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-211"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="20ac7-212">(3)</span><span class="sxs-lookup"><span data-stu-id="20ac7-212">(3)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-213">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20ac7-213">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="20ac7-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-214"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="20ac7-215">(4)</span><span class="sxs-lookup"><span data-stu-id="20ac7-215">(4)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-216">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="20ac7-216">Device is not working properly.</span></span> <span data-ttu-id="20ac7-217">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="20ac7-217">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="20ac7-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-218"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="20ac7-219">(5)</span><span class="sxs-lookup"><span data-stu-id="20ac7-219">(5)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-220">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="20ac7-220">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="20ac7-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-221"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="20ac7-222"> (6)</span><span class="sxs-lookup"><span data-stu-id="20ac7-222">(6)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-223">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="20ac7-223">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="20ac7-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-224"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="20ac7-225">(7)</span><span class="sxs-lookup"><span data-stu-id="20ac7-225">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="20ac7-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-226"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="20ac7-227">(8)</span><span class="sxs-lookup"><span data-stu-id="20ac7-227">(8)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-228">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-228">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="20ac7-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-229"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="20ac7-230">(9)</span><span class="sxs-lookup"><span data-stu-id="20ac7-230">(9)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-231">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-231">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="20ac7-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-232"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="20ac7-233">(10)</span><span class="sxs-lookup"><span data-stu-id="20ac7-233">(10)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-234">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="20ac7-234">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="20ac7-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-235"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="20ac7-236">(11)</span><span class="sxs-lookup"><span data-stu-id="20ac7-236">(11)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-237">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-237">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="20ac7-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-238"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="20ac7-239">(12)</span><span class="sxs-lookup"><span data-stu-id="20ac7-239">(12)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-240">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="20ac7-240">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="20ac7-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-241"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="20ac7-242">(13)</span><span class="sxs-lookup"><span data-stu-id="20ac7-242">(13)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-243">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-243">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="20ac7-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-244"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="20ac7-245">(14)</span><span class="sxs-lookup"><span data-stu-id="20ac7-245">(14)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-246">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="20ac7-246">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="20ac7-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-247"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="20ac7-248">(15)</span><span class="sxs-lookup"><span data-stu-id="20ac7-248">(15)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-249">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="20ac7-249">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="20ac7-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-250"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="20ac7-251">(16)</span><span class="sxs-lookup"><span data-stu-id="20ac7-251">(16)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-252">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="20ac7-252">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="20ac7-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-253"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="20ac7-254">(17)</span><span class="sxs-lookup"><span data-stu-id="20ac7-254">(17)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-255">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="20ac7-255">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20ac7-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-256"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="20ac7-257">(18)</span><span class="sxs-lookup"><span data-stu-id="20ac7-257">(18)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-258">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="20ac7-258">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="20ac7-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-259"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="20ac7-260">(19)</span><span class="sxs-lookup"><span data-stu-id="20ac7-260">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="20ac7-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-261"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="20ac7-262">(20)</span><span class="sxs-lookup"><span data-stu-id="20ac7-262">(20)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-263">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="20ac7-263">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="20ac7-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-264"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="20ac7-265">(21)</span><span class="sxs-lookup"><span data-stu-id="20ac7-265">(21)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-266">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="20ac7-266">System failure.</span></span> <span data-ttu-id="20ac7-267">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="20ac7-267">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="20ac7-268">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="20ac7-268">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="20ac7-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-269"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="20ac7-270">(22)</span><span class="sxs-lookup"><span data-stu-id="20ac7-270">(22)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-271">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="20ac7-271">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="20ac7-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-272"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="20ac7-273">(23)</span><span class="sxs-lookup"><span data-stu-id="20ac7-273">(23)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-274">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="20ac7-274">System failure.</span></span> <span data-ttu-id="20ac7-275">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="20ac7-275">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="20ac7-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-276"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="20ac7-277">(24)</span><span class="sxs-lookup"><span data-stu-id="20ac7-277">(24)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-278">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="20ac7-278">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="20ac7-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-279"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="20ac7-280">(25)</span><span class="sxs-lookup"><span data-stu-id="20ac7-280">(25)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-281">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="20ac7-281">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="20ac7-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-282"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="20ac7-283">(26)</span><span class="sxs-lookup"><span data-stu-id="20ac7-283">(26)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-284">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="20ac7-284">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="20ac7-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-285"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="20ac7-286">(27)</span><span class="sxs-lookup"><span data-stu-id="20ac7-286">(27)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-287">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="20ac7-287">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="20ac7-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-288"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="20ac7-289">(28)</span><span class="sxs-lookup"><span data-stu-id="20ac7-289">(28)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-290">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="20ac7-290">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="20ac7-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-291"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="20ac7-292">(29)</span><span class="sxs-lookup"><span data-stu-id="20ac7-292">(29)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-293">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="20ac7-293">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="20ac7-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-294"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="20ac7-295">(30)</span><span class="sxs-lookup"><span data-stu-id="20ac7-295">(30)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-296">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="20ac7-296">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="20ac7-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="20ac7-297"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="20ac7-298">1-31</span><span class="sxs-lookup"><span data-stu-id="20ac7-298">(31)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-299">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="20ac7-299">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20ac7-300">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="20ac7-300">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-301">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="20ac7-301">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-303">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20ac7-303">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-304">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="20ac7-304">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="20ac7-305">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-305">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-306">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="20ac7-306">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-307">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-308">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-309">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20ac7-309">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-310">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="20ac7-310">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="20ac7-311">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="20ac7-311">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="20ac7-312">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-312">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-313">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20ac7-313">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-316">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="20ac7-316">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-317">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="20ac7-317">Textual description of the object.</span></span>

<span data-ttu-id="20ac7-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-319">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="20ac7-319">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-320">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-320">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-322">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20ac7-322">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-323">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-323">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="20ac7-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-325">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="20ac7-325">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-326">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="20ac7-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-328">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="20ac7-328">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="20ac7-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-330">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="20ac7-330">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-333">Произвольная строка, в которой содержатся дополнительные сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="20ac7-333">Free-form string that supplies more information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="20ac7-334">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-335">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="20ac7-335">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-336">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-338">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-338">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="20ac7-339">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-339">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-340">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20ac7-340">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-341">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20ac7-341">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-342">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-343">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="20ac7-343">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-344">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="20ac7-344">Date and time the object was installed.</span></span> <span data-ttu-id="20ac7-345">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="20ac7-345">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="20ac7-346">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-346">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-347">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="20ac7-347">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-348">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20ac7-348">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-349">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-349">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-350">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="20ac7-350">Last error code reported by the logical device.</span></span>

<span data-ttu-id="20ac7-351">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-351">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-352">**Name**</span><span class="sxs-lookup"><span data-stu-id="20ac7-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-355">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="20ac7-355">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-356">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="20ac7-356">Label by which the object is known.</span></span> <span data-ttu-id="20ac7-357">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="20ac7-357">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="20ac7-358">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-358">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-359">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="20ac7-359">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-360">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="20ac7-360">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-361">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-362">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="20ac7-362">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-363">Количество последовательных блоков, каждый из которых заблокирует размер значения, содержащегося **в свойстве, которое** образует экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-363">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which forms the storage extent.</span></span> <span data-ttu-id="20ac7-364">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-364">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="20ac7-365">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-365">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="20ac7-366">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-366">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="20ac7-367">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="20ac7-367">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-368">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="20ac7-368">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-369">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-370">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-371">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="20ac7-371">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-372">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-372">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="20ac7-373">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-373">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="20ac7-374">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="20ac7-374">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-375">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="20ac7-375">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-376">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="20ac7-376">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-378">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="20ac7-378">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="20ac7-379">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-379">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20ac7-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="20ac7-380"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="20ac7-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="20ac7-381"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="20ac7-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="20ac7-382"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="20ac7-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="20ac7-383"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-384">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="20ac7-384">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="20ac7-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="20ac7-385"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-386">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="20ac7-386">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="20ac7-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="20ac7-387"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-388">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="20ac7-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="20ac7-389">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="20ac7-389">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="20ac7-390">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="20ac7-390">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="20ac7-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="20ac7-391"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-392">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="20ac7-392">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="20ac7-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="20ac7-393"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="20ac7-394">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="20ac7-394">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20ac7-395">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="20ac7-395">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-396">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="20ac7-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-397">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-398">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-398">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="20ac7-399">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="20ac7-399">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="20ac7-400">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="20ac7-400">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="20ac7-401">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="20ac7-401">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="20ac7-402">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-403">**Основной раздел**</span><span class="sxs-lookup"><span data-stu-id="20ac7-403">**PrimaryPartition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-404">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="20ac7-404">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-406">Если **значение — true**, раздел диска помечается как основной раздел для компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="20ac7-406">If **TRUE**, the disk partition is labeled as the primary partition for a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-407">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="20ac7-407">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-408">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-408">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-409">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-409">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-410">Описывает носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="20ac7-410">Describes the media and its use.</span></span>

<span data-ttu-id="20ac7-411">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-411">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-412">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="20ac7-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-413">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-415">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="20ac7-415">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-416">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="20ac7-416">Current status of the object.</span></span>

<span data-ttu-id="20ac7-417">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-417">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="20ac7-418">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="20ac7-418">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="20ac7-419">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="20ac7-419">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="20ac7-420">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="20ac7-420">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="20ac7-421">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="20ac7-421">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20ac7-422">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="20ac7-422">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="20ac7-423">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="20ac7-423">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="20ac7-424">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="20ac7-424">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="20ac7-425">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="20ac7-425">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="20ac7-426">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="20ac7-426">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="20ac7-427">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="20ac7-427">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="20ac7-428">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="20ac7-428">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="20ac7-429">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="20ac7-429">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="20ac7-430">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="20ac7-430">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20ac7-431">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="20ac7-431">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-432">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="20ac7-432">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-433">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-433">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-434">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="20ac7-434">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-435">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="20ac7-435">State of the logical device.</span></span> <span data-ttu-id="20ac7-436">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="20ac7-436">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="20ac7-437">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-437">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="20ac7-438">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="20ac7-438">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="20ac7-439">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="20ac7-439">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="20ac7-440">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="20ac7-440">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="20ac7-441">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="20ac7-441">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="20ac7-442">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="20ac7-442">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20ac7-443">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="20ac7-443">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-444">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-444">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-445">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-445">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-446">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20ac7-446">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-447">Свойство свойства **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="20ac7-447">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="20ac7-448">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-448">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="20ac7-449">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="20ac7-449">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20ac7-450">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="20ac7-450">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-451">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20ac7-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20ac7-452">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20ac7-452">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20ac7-453">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="20ac7-453">Scoping system's **Name** property.</span></span>

<span data-ttu-id="20ac7-454">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="20ac7-454">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20ac7-455">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20ac7-455">Remarks</span></span>

<span data-ttu-id="20ac7-456">Класс **CIM \_ дискпартитион** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-456">The **CIM\_DiskPartition** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="20ac7-457">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="20ac7-457">WMI does not implement this class.</span></span> <span data-ttu-id="20ac7-458">Классы, производные от **CIM \_ дискпартитион**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="20ac7-458">For classes derived from **CIM\_DiskPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="20ac7-459">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="20ac7-459">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="20ac7-460">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="20ac7-460">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ac7-461">Требования</span><span class="sxs-lookup"><span data-stu-id="20ac7-461">Requirements</span></span>



| <span data-ttu-id="20ac7-462">Требование</span><span class="sxs-lookup"><span data-stu-id="20ac7-462">Requirement</span></span> | <span data-ttu-id="20ac7-463">Значение</span><span class="sxs-lookup"><span data-stu-id="20ac7-463">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20ac7-464">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20ac7-464">Minimum supported client</span></span><br/> | <span data-ttu-id="20ac7-465">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20ac7-465">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20ac7-466">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20ac7-466">Minimum supported server</span></span><br/> | <span data-ttu-id="20ac7-467">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20ac7-467">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20ac7-468">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="20ac7-468">Namespace</span></span><br/>                | <span data-ttu-id="20ac7-469">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="20ac7-469">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="20ac7-470">MOF</span><span class="sxs-lookup"><span data-stu-id="20ac7-470">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20ac7-471"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20ac7-471"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="20ac7-472">DLL</span><span class="sxs-lookup"><span data-stu-id="20ac7-472">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20ac7-473"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20ac7-473"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20ac7-474">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20ac7-474">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20ac7-475">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="20ac7-475">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

