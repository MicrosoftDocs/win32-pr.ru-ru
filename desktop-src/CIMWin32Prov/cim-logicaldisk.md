---
description: Класс CIM \_ LogicalDisk представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля DeviceID (ключ) диска.
ms.assetid: 1c2fd0bf-a1e3-4706-9f84-5dd4d371a167
ms.tgt_platform: multiple
title: Класс CIM_LogicalDisk (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDisk
- CIM_LogicalDisk.Access
- CIM_LogicalDisk.Availability
- CIM_LogicalDisk.BlockSize
- CIM_LogicalDisk.Caption
- CIM_LogicalDisk.ConfigManagerErrorCode
- CIM_LogicalDisk.ConfigManagerUserConfig
- CIM_LogicalDisk.CreationClassName
- CIM_LogicalDisk.Description
- CIM_LogicalDisk.DeviceID
- CIM_LogicalDisk.ErrorCleared
- CIM_LogicalDisk.ErrorDescription
- CIM_LogicalDisk.ErrorMethodology
- CIM_LogicalDisk.FreeSpace
- CIM_LogicalDisk.InstallDate
- CIM_LogicalDisk.LastErrorCode
- CIM_LogicalDisk.Name
- CIM_LogicalDisk.NumberOfBlocks
- CIM_LogicalDisk.PNPDeviceID
- CIM_LogicalDisk.PowerManagementCapabilities
- CIM_LogicalDisk.PowerManagementSupported
- CIM_LogicalDisk.Purpose
- CIM_LogicalDisk.Size
- CIM_LogicalDisk.Status
- CIM_LogicalDisk.StatusInfo
- CIM_LogicalDisk.SystemCreationClassName
- CIM_LogicalDisk.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd28ab0b9982606278e65705273a9965cfb9b396
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807120"
---
# <a name="cim_logicaldisk-class-cimwin32-wmi-providers"></a><span data-ttu-id="112f4-103">Класс CIM_LogicalDisk (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="112f4-103">CIM_LogicalDisk class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="112f4-104">Класс **CIM \_ LogicalDisk** представляет непрерывный диапазон логических блоков, идентифицируемый файловой системой с помощью поля **DeviceID** (ключ) диска.</span><span class="sxs-lookup"><span data-stu-id="112f4-104">The **CIM\_LogicalDisk** class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="112f4-105">Например, в среде Windows поле **DeviceID** содержит букву диска; в среде UNIX она содержит путь доступа. и в среде NetWare он содержит имя тома.</span><span class="sxs-lookup"><span data-stu-id="112f4-105">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="112f4-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="112f4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="112f4-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="112f4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="112f4-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="112f4-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="112f4-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="112f4-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="112f4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="112f4-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C539-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDisk : CIM_StorageExtent
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
  uint64   FreeSpace;
  datetime InstallDate;
  uint32   LastErrorCode;
  string   Name;
  uint64   NumberOfBlocks;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint64   Size;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="112f4-111">Члены</span><span class="sxs-lookup"><span data-stu-id="112f4-111">Members</span></span>

<span data-ttu-id="112f4-112">Класс **CIM \_ LogicalDisk** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="112f4-112">The **CIM\_LogicalDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="112f4-113">Методы</span><span class="sxs-lookup"><span data-stu-id="112f4-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="112f4-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="112f4-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="112f4-115">Методы</span><span class="sxs-lookup"><span data-stu-id="112f4-115">Methods</span></span>

<span data-ttu-id="112f4-116">Класс логического логического класса **CIM \_** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="112f4-116">The **CIM\_LogicalDisk** class has these methods.</span></span>



| <span data-ttu-id="112f4-117">Метод</span><span class="sxs-lookup"><span data-stu-id="112f4-117">Method</span></span>                                                                 | <span data-ttu-id="112f4-118">Описание</span><span class="sxs-lookup"><span data-stu-id="112f4-118">Description</span></span>                                                                                                                              |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="112f4-119">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="112f4-119">**Reset**</span></span>](reset-method-in-class-cim-logicaldisk.md)                 | <span data-ttu-id="112f4-120">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="112f4-121">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="112f4-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="112f4-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="112f4-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-logicaldisk.md) | <span data-ttu-id="112f4-123">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="112f4-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="112f4-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="112f4-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="112f4-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="112f4-125">Properties</span></span>

<span data-ttu-id="112f4-126">Класс логического логического класса **CIM \_** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="112f4-126">The **CIM\_LogicalDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="112f4-127">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="112f4-127">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="112f4-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-130">Содержит сведения о том, доступен ли носитель для чтения, записи или и то, и другое, например.</span><span class="sxs-lookup"><span data-stu-id="112f4-130">Describes whether the media is readable, writable, or both, for example.</span></span> <span data-ttu-id="112f4-131">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-131">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="112f4-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="112f4-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-133">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="112f4-133">Unknown.</span></span>

</dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="112f4-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="112f4-134"><span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Readable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-135">Чтения.</span><span class="sxs-lookup"><span data-stu-id="112f4-135">Readable.</span></span>

</dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="112f4-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="112f4-136"><span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Writeable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-137">Записывать.</span><span class="sxs-lookup"><span data-stu-id="112f4-137">Writable.</span></span>

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="112f4-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="112f4-138"><span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Read/Write Supported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-139">Поддерживается чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="112f4-139">Read/write supported.</span></span>

</dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="112f4-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="112f4-140"><span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Write Once** (4)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-141">Однократная запись.</span><span class="sxs-lookup"><span data-stu-id="112f4-141">Write once.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="112f4-142">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="112f4-142">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-143">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="112f4-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-145">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="112f4-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-146">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-146">Availability and status of the device.</span></span>

<span data-ttu-id="112f4-147">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-147">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="112f4-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="112f4-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="112f4-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="112f4-149"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="112f4-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="112f4-150"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="112f4-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="112f4-151"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="112f4-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="112f4-152"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="112f4-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="112f4-153"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="112f4-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="112f4-154"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="112f4-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="112f4-155"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="112f4-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="112f4-156"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="112f4-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="112f4-157"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="112f4-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="112f4-158"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="112f4-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="112f4-159"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="112f4-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="112f4-160"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-161">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="112f4-161">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="112f4-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="112f4-162"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-163">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="112f4-163">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="112f4-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="112f4-164"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-165">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="112f4-165">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="112f4-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="112f4-166"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="112f4-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="112f4-167"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-168">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="112f4-168">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="112f4-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="112f4-169"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-170">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="112f4-170">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="112f4-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="112f4-171"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-172">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="112f4-172">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="112f4-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="112f4-173"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-174">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="112f4-174">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="112f4-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="112f4-175"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-176">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="112f4-176">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="112f4-177">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="112f4-177">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-178">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="112f4-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-180">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="112f4-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-181">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="112f4-181">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="112f4-182">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="112f4-182">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="112f4-183">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1.</span><span class="sxs-lookup"><span data-stu-id="112f4-183">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1.</span></span>

<span data-ttu-id="112f4-184">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-184">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="112f4-185">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="112f4-185">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-186">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="112f4-186">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-187">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-189">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="112f4-189">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-190">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="112f4-190">Short textual description of the object.</span></span>

<span data-ttu-id="112f4-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-192">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="112f4-192">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="112f4-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-195">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="112f4-195">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-196">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="112f4-196">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="112f4-197">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-197">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="112f4-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="112f4-198"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="112f4-199"> (0)</span><span class="sxs-lookup"><span data-stu-id="112f4-199">(0)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-200">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="112f4-200">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="112f4-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="112f4-201"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="112f4-202">(1)</span><span class="sxs-lookup"><span data-stu-id="112f4-202">(1)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-203">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="112f4-203">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="112f4-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-204"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="112f4-205">(2)</span><span class="sxs-lookup"><span data-stu-id="112f4-205">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="112f4-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="112f4-206"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="112f4-207">(3)</span><span class="sxs-lookup"><span data-stu-id="112f4-207">(3)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-208">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="112f4-208">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="112f4-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="112f4-209"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="112f4-210">(4)</span><span class="sxs-lookup"><span data-stu-id="112f4-210">(4)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-211">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="112f4-211">Device is not working properly.</span></span> <span data-ttu-id="112f4-212">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="112f4-212">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="112f4-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="112f4-213"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="112f4-214">(5)</span><span class="sxs-lookup"><span data-stu-id="112f4-214">(5)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-215">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="112f4-215">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="112f4-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="112f4-216"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="112f4-217"> (6)</span><span class="sxs-lookup"><span data-stu-id="112f4-217">(6)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-218">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="112f4-218">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="112f4-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="112f4-219"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="112f4-220">(7)</span><span class="sxs-lookup"><span data-stu-id="112f4-220">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="112f4-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-221"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="112f4-222">(8)</span><span class="sxs-lookup"><span data-stu-id="112f4-222">(8)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-223">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-223">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="112f4-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-224"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="112f4-225">(9)</span><span class="sxs-lookup"><span data-stu-id="112f4-225">(9)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-226">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-226">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="112f4-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="112f4-227"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="112f4-228">(10)</span><span class="sxs-lookup"><span data-stu-id="112f4-228">(10)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-229">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="112f4-229">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="112f4-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-230"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="112f4-231">(11)</span><span class="sxs-lookup"><span data-stu-id="112f4-231">(11)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-232">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-232">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="112f4-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="112f4-233"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="112f4-234">(12)</span><span class="sxs-lookup"><span data-stu-id="112f4-234">(12)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-235">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="112f4-235">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="112f4-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-236"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="112f4-237">(13)</span><span class="sxs-lookup"><span data-stu-id="112f4-237">(13)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-238">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-238">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="112f4-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="112f4-239"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="112f4-240">(14)</span><span class="sxs-lookup"><span data-stu-id="112f4-240">(14)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-241">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="112f4-241">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="112f4-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="112f4-242"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="112f4-243">(15)</span><span class="sxs-lookup"><span data-stu-id="112f4-243">(15)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-244">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="112f4-244">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="112f4-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="112f4-245"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="112f4-246">(16)</span><span class="sxs-lookup"><span data-stu-id="112f4-246">(16)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-247">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="112f4-247">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="112f4-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="112f4-248"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="112f4-249">(17)</span><span class="sxs-lookup"><span data-stu-id="112f4-249">(17)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-250">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="112f4-250">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="112f4-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-251"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="112f4-252">(18)</span><span class="sxs-lookup"><span data-stu-id="112f4-252">(18)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-253">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="112f4-253">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="112f4-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="112f4-254"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="112f4-255">(19)</span><span class="sxs-lookup"><span data-stu-id="112f4-255">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="112f4-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="112f4-256"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="112f4-257">(20)</span><span class="sxs-lookup"><span data-stu-id="112f4-257">(20)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-258">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="112f4-258">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="112f4-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="112f4-259"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="112f4-260">(21)</span><span class="sxs-lookup"><span data-stu-id="112f4-260">(21)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-261">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="112f4-261">System failure.</span></span> <span data-ttu-id="112f4-262">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="112f4-262">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="112f4-263">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="112f4-263">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="112f4-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="112f4-264"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="112f4-265">(22)</span><span class="sxs-lookup"><span data-stu-id="112f4-265">(22)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-266">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="112f4-266">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="112f4-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="112f4-267"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="112f4-268">(23)</span><span class="sxs-lookup"><span data-stu-id="112f4-268">(23)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-269">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="112f4-269">System failure.</span></span> <span data-ttu-id="112f4-270">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="112f4-270">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="112f4-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="112f4-271"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="112f4-272">(24)</span><span class="sxs-lookup"><span data-stu-id="112f4-272">(24)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-273">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="112f4-273">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="112f4-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="112f4-274"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="112f4-275">(25)</span><span class="sxs-lookup"><span data-stu-id="112f4-275">(25)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-276">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="112f4-276">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="112f4-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="112f4-277"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="112f4-278">(26)</span><span class="sxs-lookup"><span data-stu-id="112f4-278">(26)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-279">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="112f4-279">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="112f4-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="112f4-280"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="112f4-281">(27)</span><span class="sxs-lookup"><span data-stu-id="112f4-281">(27)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-282">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="112f4-282">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="112f4-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="112f4-283"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="112f4-284">(28)</span><span class="sxs-lookup"><span data-stu-id="112f4-284">(28)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-285">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="112f4-285">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="112f4-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="112f4-286"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="112f4-287">(29)</span><span class="sxs-lookup"><span data-stu-id="112f4-287">(29)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-288">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="112f4-288">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="112f4-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="112f4-289"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="112f4-290">(30)</span><span class="sxs-lookup"><span data-stu-id="112f4-290">(30)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-291">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="112f4-291">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="112f4-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="112f4-292"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="112f4-293">1-31</span><span class="sxs-lookup"><span data-stu-id="112f4-293">(31)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-294">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="112f4-294">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="112f4-295">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="112f4-295">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-296">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="112f4-296">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-298">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="112f4-298">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-299">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="112f4-299">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="112f4-300">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-300">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-301">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="112f4-301">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-302">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-303">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-304">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="112f4-304">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="112f4-305">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="112f4-305">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="112f4-306">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="112f4-306">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="112f4-307">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-307">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-308">**Описание**</span><span class="sxs-lookup"><span data-stu-id="112f4-308">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-311">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="112f4-311">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-312">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="112f4-312">Textual description of the object.</span></span>

<span data-ttu-id="112f4-313">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-314">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="112f4-314">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-315">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-315">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-317">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="112f4-317">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="112f4-318">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-318">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="112f4-319">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-319">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-320">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="112f4-320">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-321">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="112f4-321">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-323">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="112f4-323">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="112f4-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-325">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="112f4-325">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-328">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="112f4-328">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="112f4-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-330">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="112f4-330">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-331">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-333">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="112f4-333">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="112f4-334">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-334">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-335">**FreeSpace**</span><span class="sxs-lookup"><span data-stu-id="112f4-335">**FreeSpace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-336">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="112f4-336">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-338">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="112f4-338">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-339">Доступное свободное место на логическом диске (в байтах).</span><span class="sxs-lookup"><span data-stu-id="112f4-339">Available free space, in bytes, on the logical disk.</span></span>

<span data-ttu-id="112f4-340">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="112f4-340">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-341">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="112f4-341">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-342">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="112f4-342">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-343">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-344">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="112f4-344">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-345">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="112f4-345">Date and time the object was installed.</span></span> <span data-ttu-id="112f4-346">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="112f4-346">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="112f4-347">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-348">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="112f4-348">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-349">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="112f4-349">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-350">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-350">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-351">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="112f4-351">Last error code reported by the logical device.</span></span>

<span data-ttu-id="112f4-352">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-352">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-353">**Name**</span><span class="sxs-lookup"><span data-stu-id="112f4-353">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-354">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-356">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="112f4-356">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-357">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="112f4-357">Label by which the object is known.</span></span> <span data-ttu-id="112f4-358">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="112f4-358">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="112f4-359">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-359">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-360">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="112f4-360">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-361">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="112f4-361">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-363">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="112f4-363">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-364">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="112f4-364">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form the storage extent.</span></span> <span data-ttu-id="112f4-365">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="112f4-365">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="112f4-366">Если значение свойства размерности равно 1, **это свойство является** общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="112f4-366">If the value of the **BlockSize** property is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="112f4-367">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-367">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="112f4-368">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="112f4-368">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-369">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="112f4-369">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-370">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-371">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-372">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="112f4-372">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-373">Идентификатор устройства Win32 самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-373">Win32 Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="112f4-374">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-374">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="112f4-375">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="112f4-375">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="112f4-376">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="112f4-376">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-377">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="112f4-377">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="112f4-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-378">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-379">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="112f4-379">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="112f4-380">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-380">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="112f4-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="112f4-381"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="112f4-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="112f4-382"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="112f4-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="112f4-383"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="112f4-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="112f4-384"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-385">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="112f4-385">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="112f4-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="112f4-386"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-387">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="112f4-387">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="112f4-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="112f4-388"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-389">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="112f4-389">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="112f4-390">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="112f4-390">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="112f4-391">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="112f4-391">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="112f4-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="112f4-392"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-393">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="112f4-393">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="112f4-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="112f4-394"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="112f4-395">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="112f4-395">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="112f4-396">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="112f4-396">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-397">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="112f4-397">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-398">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-399">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="112f4-399">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="112f4-400">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="112f4-400">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="112f4-401">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="112f4-401">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="112f4-402">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="112f4-402">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="112f4-403">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-403">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-404">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="112f4-404">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-406">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="112f4-407">Произвольная строка, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="112f4-407">Free-form string that describes the media and its use.</span></span>

<span data-ttu-id="112f4-408">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-408">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-409">**Размер**</span><span class="sxs-lookup"><span data-stu-id="112f4-409">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-410">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="112f4-410">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-412">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="112f4-412">Qualifiers: [**units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-413">Размер логического диска в байтах.</span><span class="sxs-lookup"><span data-stu-id="112f4-413">Size of the logical disk, in bytes.</span></span>

<span data-ttu-id="112f4-414">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="112f4-414">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-415">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="112f4-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-416">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-418">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="112f4-418">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-419">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="112f4-419">Current status of the object.</span></span>

<span data-ttu-id="112f4-420">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-420">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="112f4-421">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="112f4-421">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="112f4-422">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="112f4-422">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="112f4-423">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="112f4-423">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="112f4-424">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="112f4-424">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="112f4-425">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="112f4-425">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="112f4-426">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="112f4-426">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="112f4-427">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="112f4-427">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="112f4-428">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="112f4-428">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="112f4-429">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="112f4-429">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="112f4-430">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="112f4-430">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="112f4-431">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="112f4-431">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="112f4-432">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="112f4-432">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="112f4-433">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="112f4-433">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="112f4-434">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="112f4-434">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-435">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="112f4-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-436">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-437">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="112f4-437">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="112f4-438">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="112f4-438">State of the logical device.</span></span> <span data-ttu-id="112f4-439">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="112f4-439">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="112f4-440">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-440">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="112f4-441">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="112f4-441">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="112f4-442">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="112f4-442">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="112f4-443">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="112f4-443">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="112f4-444">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="112f4-444">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="112f4-445">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="112f4-445">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="112f4-446">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="112f4-446">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-447">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-447">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-448">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-449">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="112f4-449">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="112f4-450">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="112f4-450">Scoping system's creation class name.</span></span>

<span data-ttu-id="112f4-451">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="112f4-452">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="112f4-452">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="112f4-453">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="112f4-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="112f4-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="112f4-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="112f4-455">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="112f4-455">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="112f4-456">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="112f4-456">Scoping system's name.</span></span>

<span data-ttu-id="112f4-457">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="112f4-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="112f4-458">Комментарии</span><span class="sxs-lookup"><span data-stu-id="112f4-458">Remarks</span></span>

<span data-ttu-id="112f4-459">Класс **CIM \_ LogicalDisk** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-459">The **CIM\_LogicalDisk** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="112f4-460">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="112f4-460">WMI does not implement this class.</span></span> <span data-ttu-id="112f4-461">Классы, производные от **CIM \_ LogicalDisk**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="112f4-461">For classes derived from **CIM\_LogicalDisk**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="112f4-462">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="112f4-462">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="112f4-463">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="112f4-463">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="112f4-464">Требования</span><span class="sxs-lookup"><span data-stu-id="112f4-464">Requirements</span></span>



| <span data-ttu-id="112f4-465">Требование</span><span class="sxs-lookup"><span data-stu-id="112f4-465">Requirement</span></span> | <span data-ttu-id="112f4-466">Значение</span><span class="sxs-lookup"><span data-stu-id="112f4-466">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="112f4-467">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="112f4-467">Minimum supported client</span></span><br/> | <span data-ttu-id="112f4-468">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="112f4-468">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="112f4-469">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="112f4-469">Minimum supported server</span></span><br/> | <span data-ttu-id="112f4-470">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="112f4-470">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="112f4-471">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="112f4-471">Namespace</span></span><br/>                | <span data-ttu-id="112f4-472">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="112f4-472">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="112f4-473">MOF</span><span class="sxs-lookup"><span data-stu-id="112f4-473">MOF</span></span><br/>                      | <dl> <span data-ttu-id="112f4-474"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="112f4-474"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="112f4-475">DLL</span><span class="sxs-lookup"><span data-stu-id="112f4-475">DLL</span></span><br/>                      | <dl> <span data-ttu-id="112f4-476"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="112f4-476"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="112f4-477">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="112f4-477">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112f4-478">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="112f4-478">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

