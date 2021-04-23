---
description: Класс CIM \_ фисикалекстент представляет реализацию SCC RAID.
ms.assetid: d1950464-e17a-4651-aa53-6385659994ff
ms.tgt_platform: multiple
title: Класс CIM_PhysicalExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalExtent
- CIM_PhysicalExtent.Access
- CIM_PhysicalExtent.Availability
- CIM_PhysicalExtent.BlockSize
- CIM_PhysicalExtent.Caption
- CIM_PhysicalExtent.ConfigManagerErrorCode
- CIM_PhysicalExtent.ConfigManagerUserConfig
- CIM_PhysicalExtent.CreationClassName
- CIM_PhysicalExtent.Description
- CIM_PhysicalExtent.DeviceID
- CIM_PhysicalExtent.ErrorCleared
- CIM_PhysicalExtent.ErrorDescription
- CIM_PhysicalExtent.ErrorMethodology
- CIM_PhysicalExtent.InstallDate
- CIM_PhysicalExtent.LastErrorCode
- CIM_PhysicalExtent.Name
- CIM_PhysicalExtent.NumberOfBlocks
- CIM_PhysicalExtent.PNPDeviceID
- CIM_PhysicalExtent.PowerManagementCapabilities
- CIM_PhysicalExtent.PowerManagementSupported
- CIM_PhysicalExtent.Purpose
- CIM_PhysicalExtent.Status
- CIM_PhysicalExtent.StatusInfo
- CIM_PhysicalExtent.SystemCreationClassName
- CIM_PhysicalExtent.SystemName
- CIM_PhysicalExtent.UnitsBeforeCheckDataInterleave
- CIM_PhysicalExtent.UnitsOfCheckData
- CIM_PhysicalExtent.UnitsOfUserData
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 31e05d3b339d64fd640460716376c3d8b538fa95
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807036"
---
# <a name="cim_physicalextent-class"></a><span data-ttu-id="043b3-103">\_Класс CIM фисикалекстент</span><span class="sxs-lookup"><span data-stu-id="043b3-103">CIM\_PhysicalExtent class</span></span>

<span data-ttu-id="043b3-104">Класс **CIM \_ фисикалекстент** представляет реализацию SCC RAID.</span><span class="sxs-lookup"><span data-stu-id="043b3-104">The **CIM\_PhysicalExtent** class represents an SCC RAID implementation.</span></span> <span data-ttu-id="043b3-105">Он определяет последовательные адреса блочных адресов на одном запоминающем устройстве, которые обрабатываются как единая область хранения в одном классе [**CIM \_ сторажередунданциграуп**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="043b3-105">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="043b3-106">Альтернативой, при использовании автоматической конфигурации, является создание экземпляра или расширение класса [**CIM \_ аггрегатепекстент**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="043b3-106">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="043b3-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="043b3-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="043b3-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="043b3-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="043b3-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="043b3-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="043b3-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="043b3-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="043b3-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="043b3-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979E-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalExtent : CIM_StorageExtent
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
  string   Purpose;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint64   UnitsBeforeCheckDataInterleave;
  uint64   UnitsOfCheckData;
  uint64   UnitsOfUserData;
};
```

## <a name="members"></a><span data-ttu-id="043b3-112">Члены</span><span class="sxs-lookup"><span data-stu-id="043b3-112">Members</span></span>

<span data-ttu-id="043b3-113">Класс **CIM \_ фисикалекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="043b3-113">The **CIM\_PhysicalExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="043b3-114">Методы</span><span class="sxs-lookup"><span data-stu-id="043b3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="043b3-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="043b3-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="043b3-116">Методы</span><span class="sxs-lookup"><span data-stu-id="043b3-116">Methods</span></span>

<span data-ttu-id="043b3-117">Класс **CIM \_ фисикалекстент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="043b3-117">The **CIM\_PhysicalExtent** class has these methods.</span></span>



| <span data-ttu-id="043b3-118">Метод</span><span class="sxs-lookup"><span data-stu-id="043b3-118">Method</span></span>                                                                    | <span data-ttu-id="043b3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="043b3-119">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="043b3-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="043b3-120">**Reset**</span></span>](reset-method-in-class-cim-physicalextent.md)                 | <span data-ttu-id="043b3-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="043b3-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="043b3-122">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="043b3-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="043b3-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-physicalextent.md) | <span data-ttu-id="043b3-124">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="043b3-124">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="043b3-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="043b3-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="043b3-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="043b3-126">Properties</span></span>

<span data-ttu-id="043b3-127">Класс **CIM \_ фисикалекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="043b3-127">The **CIM\_PhysicalExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="043b3-128">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="043b3-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b3-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-131">Чтение и запись свойств носителя.</span><span class="sxs-lookup"><span data-stu-id="043b3-131">Read/write properties of the media.</span></span>

<span data-ttu-id="043b3-132">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b3-133">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="043b3-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="043b3-134">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="043b3-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="043b3-135">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="043b3-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="043b3-136">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="043b3-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="043b3-137">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="043b3-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="043b3-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="043b3-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b3-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-141">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="043b3-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-142">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-142">Availability and status of the device.</span></span>

<span data-ttu-id="043b3-143">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="043b3-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="043b3-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b3-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="043b3-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="043b3-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="043b3-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-147">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="043b3-147">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="043b3-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="043b3-148"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="043b3-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="043b3-149"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="043b3-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="043b3-150"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="043b3-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="043b3-151"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="043b3-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="043b3-152"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="043b3-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="043b3-153"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="043b3-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="043b3-154"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="043b3-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="043b3-155"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="043b3-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="043b3-156"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="043b3-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="043b3-157"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-158">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="043b3-158">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="043b3-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="043b3-159"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-160">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="043b3-160">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="043b3-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="043b3-161"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-162">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="043b3-162">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="043b3-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="043b3-163"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="043b3-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="043b3-164"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-165">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="043b3-165">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="043b3-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="043b3-166"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-167">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="043b3-167">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="043b3-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="043b3-168"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-169">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="043b3-169">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="043b3-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="043b3-170"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-171">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="043b3-171">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="043b3-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="043b3-172"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-173">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="043b3-173">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="043b3-174">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="043b3-174">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-175">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="043b3-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-177">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("размер"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Физические экстенты DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="043b3-177">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("BlockSize"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-178">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="043b3-178">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="043b3-179">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="043b3-179">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="043b3-180">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="043b3-180">If the block size is unknown or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one) .</span></span>

<span data-ttu-id="043b3-181">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="043b3-182">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="043b3-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-183">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="043b3-183">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-186">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="043b3-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-187">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="043b3-187">Short textual description of the object.</span></span>

<span data-ttu-id="043b3-188">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-188">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-189">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="043b3-189">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-190">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="043b3-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-192">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="043b3-192">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-193">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="043b3-193">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="043b3-194">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="043b3-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="043b3-195"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="043b3-196"> (0)</span><span class="sxs-lookup"><span data-stu-id="043b3-196">(0)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-197">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="043b3-197">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="043b3-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="043b3-198"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="043b3-199">(1)</span><span class="sxs-lookup"><span data-stu-id="043b3-199">(1)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-200">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="043b3-200">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="043b3-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-201"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="043b3-202">(2)</span><span class="sxs-lookup"><span data-stu-id="043b3-202">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="043b3-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="043b3-203"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="043b3-204">(3)</span><span class="sxs-lookup"><span data-stu-id="043b3-204">(3)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-205">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="043b3-205">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="043b3-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="043b3-206"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="043b3-207">(4)</span><span class="sxs-lookup"><span data-stu-id="043b3-207">(4)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-208">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="043b3-208">Device is not working properly.</span></span> <span data-ttu-id="043b3-209">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="043b3-209">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="043b3-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="043b3-210"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="043b3-211">(5)</span><span class="sxs-lookup"><span data-stu-id="043b3-211">(5)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-212">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="043b3-212">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="043b3-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="043b3-213"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="043b3-214"> (6)</span><span class="sxs-lookup"><span data-stu-id="043b3-214">(6)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-215">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="043b3-215">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="043b3-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="043b3-216"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="043b3-217">(7)</span><span class="sxs-lookup"><span data-stu-id="043b3-217">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="043b3-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-218"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="043b3-219">(8)</span><span class="sxs-lookup"><span data-stu-id="043b3-219">(8)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-220">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-220">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="043b3-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-221"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="043b3-222">(9)</span><span class="sxs-lookup"><span data-stu-id="043b3-222">(9)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-223">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="043b3-223">Device is not working properly.</span></span> <span data-ttu-id="043b3-224">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-224">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="043b3-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="043b3-225"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="043b3-226">(10)</span><span class="sxs-lookup"><span data-stu-id="043b3-226">(10)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-227">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="043b3-227">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="043b3-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-228"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="043b3-229">(11)</span><span class="sxs-lookup"><span data-stu-id="043b3-229">(11)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-230">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-230">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="043b3-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="043b3-231"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="043b3-232">(12)</span><span class="sxs-lookup"><span data-stu-id="043b3-232">(12)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-233">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="043b3-233">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="043b3-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-234"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="043b3-235">(13)</span><span class="sxs-lookup"><span data-stu-id="043b3-235">(13)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-236">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-236">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="043b3-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="043b3-237"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="043b3-238">(14)</span><span class="sxs-lookup"><span data-stu-id="043b3-238">(14)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-239">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="043b3-239">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="043b3-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="043b3-240"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="043b3-241">(15)</span><span class="sxs-lookup"><span data-stu-id="043b3-241">(15)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-242">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="043b3-242">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="043b3-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="043b3-243"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="043b3-244">(16)</span><span class="sxs-lookup"><span data-stu-id="043b3-244">(16)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-245">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="043b3-245">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="043b3-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="043b3-246"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="043b3-247">(17)</span><span class="sxs-lookup"><span data-stu-id="043b3-247">(17)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-248">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="043b3-248">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="043b3-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-249"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="043b3-250">(18)</span><span class="sxs-lookup"><span data-stu-id="043b3-250">(18)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-251">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="043b3-251">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="043b3-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="043b3-252"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="043b3-253">(19)</span><span class="sxs-lookup"><span data-stu-id="043b3-253">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="043b3-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="043b3-254"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="043b3-255">(20)</span><span class="sxs-lookup"><span data-stu-id="043b3-255">(20)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-256">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="043b3-256">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="043b3-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="043b3-257"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="043b3-258">(21)</span><span class="sxs-lookup"><span data-stu-id="043b3-258">(21)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-259">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="043b3-259">System failure.</span></span> <span data-ttu-id="043b3-260">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="043b3-260">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="043b3-261">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="043b3-261">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="043b3-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="043b3-262"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="043b3-263">(22)</span><span class="sxs-lookup"><span data-stu-id="043b3-263">(22)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-264">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="043b3-264">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="043b3-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="043b3-265"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="043b3-266">(23)</span><span class="sxs-lookup"><span data-stu-id="043b3-266">(23)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-267">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="043b3-267">System failure.</span></span> <span data-ttu-id="043b3-268">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="043b3-268">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="043b3-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="043b3-269"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="043b3-270">(24)</span><span class="sxs-lookup"><span data-stu-id="043b3-270">(24)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-271">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="043b3-271">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="043b3-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="043b3-272"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="043b3-273">(25)</span><span class="sxs-lookup"><span data-stu-id="043b3-273">(25)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-274">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="043b3-274">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="043b3-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="043b3-275"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="043b3-276">(26)</span><span class="sxs-lookup"><span data-stu-id="043b3-276">(26)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-277">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="043b3-277">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="043b3-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="043b3-278"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="043b3-279">(27)</span><span class="sxs-lookup"><span data-stu-id="043b3-279">(27)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-280">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="043b3-280">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="043b3-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="043b3-281"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="043b3-282">(28)</span><span class="sxs-lookup"><span data-stu-id="043b3-282">(28)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-283">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="043b3-283">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="043b3-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="043b3-284"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="043b3-285">(29)</span><span class="sxs-lookup"><span data-stu-id="043b3-285">(29)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-286">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="043b3-286">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="043b3-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="043b3-287"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="043b3-288">(30)</span><span class="sxs-lookup"><span data-stu-id="043b3-288">(30)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-289">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="043b3-289">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="043b3-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="043b3-290"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="043b3-291">1-31</span><span class="sxs-lookup"><span data-stu-id="043b3-291">(31)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-292">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="043b3-292">Device is not working properly.</span></span> <span data-ttu-id="043b3-293">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="043b3-293">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="043b3-294">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="043b3-294">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-295">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="043b3-295">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-296">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-296">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-297">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="043b3-297">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-298">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="043b3-298">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="043b3-299">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-299">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-300">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="043b3-300">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-301">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-303">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b3-303">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b3-304">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="043b3-304">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="043b3-305">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="043b3-305">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="043b3-306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-307">**Описание**</span><span class="sxs-lookup"><span data-stu-id="043b3-307">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-308">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-308">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-309">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-310">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="043b3-310">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-311">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="043b3-311">Textual description of the object.</span></span>

<span data-ttu-id="043b3-312">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-312">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-313">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="043b3-313">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-314">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-314">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-315">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-315">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-316">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b3-316">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b3-317">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-317">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="043b3-318">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-318">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-319">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="043b3-319">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-320">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="043b3-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-321">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-322">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="043b3-322">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="043b3-323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-324">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="043b3-324">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-325">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-327">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="043b3-327">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="043b3-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-329">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="043b3-329">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-331">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-332">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="043b3-332">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="043b3-333">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-333">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-334">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="043b3-334">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-335">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="043b3-335">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-337">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="043b3-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-338">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="043b3-338">Date and time the object was installed.</span></span> <span data-ttu-id="043b3-339">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="043b3-339">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="043b3-340">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-341">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="043b3-341">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-342">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="043b3-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-343">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-344">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="043b3-344">Last error code reported by the logical device.</span></span>

<span data-ttu-id="043b3-345">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-345">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-346">**Name**</span><span class="sxs-lookup"><span data-stu-id="043b3-346">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-347">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-347">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-348">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-348">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-349">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="043b3-349">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-350">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="043b3-350">Label by which the object is known.</span></span> <span data-ttu-id="043b3-351">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="043b3-351">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="043b3-352">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-352">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-353">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="043b3-353">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-354">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="043b3-354">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-356">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нумберофблоккс"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Физические экстенты DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="043b3-356">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-357">Общее число последовательных блоков, каждый из которых блокирует размер значения, содержащегося в **свойстве, которое** формирует эту область хранения.</span><span class="sxs-lookup"><span data-stu-id="043b3-357">Total number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, which form this storage extent.</span></span> <span data-ttu-id="043b3-358">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="043b3-358">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="043b3-359">Если **значение параметра DataSize равно 1** , это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="043b3-359">If the value of **BlockSize** is 1, this property is the total size of the storage extent.</span></span>

<span data-ttu-id="043b3-360">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-360">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="043b3-361">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="043b3-361">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-362">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="043b3-362">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-363">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-363">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-364">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-365">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="043b3-365">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-366">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-366">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="043b3-367">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-367">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="043b3-368">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="043b3-368">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="043b3-369">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="043b3-369">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-370">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="043b3-370">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="043b3-371">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-372">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="043b3-372">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="043b3-373">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-373">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b3-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="043b3-374"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="043b3-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="043b3-375"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="043b3-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="043b3-376"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="043b3-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="043b3-377"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-378">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="043b3-378">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="043b3-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="043b3-379"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-380">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="043b3-380">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="043b3-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="043b3-381"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-382">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="043b3-382">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="043b3-383">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="043b3-383">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="043b3-384">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="043b3-384">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="043b3-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="043b3-385"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-386">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="043b3-386">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="043b3-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="043b3-387"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="043b3-388">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="043b3-388">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="043b3-389">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="043b3-389">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-390">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="043b3-390">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-392">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="043b3-392">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="043b3-393">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="043b3-393">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="043b3-394">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="043b3-394">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="043b3-395">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="043b3-395">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="043b3-396">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-397">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="043b3-397">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-398">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-398">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="043b3-400">Строка свободной формы, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="043b3-400">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="043b3-401">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-401">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-402">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="043b3-402">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-403">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-404">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-405">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="043b3-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-406">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="043b3-406">Current status of the object.</span></span>

<span data-ttu-id="043b3-407">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-407">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="043b3-408">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="043b3-408">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="043b3-409">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="043b3-409">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="043b3-410">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="043b3-410">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="043b3-411">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="043b3-411">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b3-412">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="043b3-412">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="043b3-413">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="043b3-413">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="043b3-414">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="043b3-414">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="043b3-415">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="043b3-415">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="043b3-416">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="043b3-416">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="043b3-417">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="043b3-417">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="043b3-418">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="043b3-418">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="043b3-419">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="043b3-419">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="043b3-420">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="043b3-420">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="043b3-421">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="043b3-421">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-422">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="043b3-422">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-423">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-424">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="043b3-424">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-425">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="043b3-425">State of the logical device.</span></span> <span data-ttu-id="043b3-426">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="043b3-426">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="043b3-427">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="043b3-428">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="043b3-428">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="043b3-429">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="043b3-429">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="043b3-430">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="043b3-430">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="043b3-431">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="043b3-431">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="043b3-432">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="043b3-432">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="043b3-433">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="043b3-433">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-434">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-435">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-436">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b3-436">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b3-437">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="043b3-437">Scoping system's creation class name.</span></span>

<span data-ttu-id="043b3-438">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-438">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-439">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="043b3-439">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-440">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="043b3-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-441">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-442">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="043b3-442">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="043b3-443">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="043b3-443">Scoping system's name.</span></span>

<span data-ttu-id="043b3-444">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="043b3-444">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-445">**унитсбефоречеккдатаинтерлеаве**</span><span class="sxs-lookup"><span data-stu-id="043b3-445">**UnitsBeforeCheckDataInterleave**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-446">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="043b3-446">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-447">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-447">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-448">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Физические экстенты DMTF \| 001,6 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="043b3-448">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-449">Число байтов данных пользователя, которые необходимо пропустить перед началом извлечения данных после записи.</span><span class="sxs-lookup"><span data-stu-id="043b3-449">Number of user data bytes to skip before starting the check-data interleave.</span></span>

<span data-ttu-id="043b3-450">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="043b3-450">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-451">**унитсофчеккдата**</span><span class="sxs-lookup"><span data-stu-id="043b3-451">**UnitsOfCheckData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-452">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="043b3-452">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-454">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Физические экстенты DMTF \| 001,7 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="043b3-454">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-455">Число байтов, которое должно быть зарезервировано для проверки данных.</span><span class="sxs-lookup"><span data-stu-id="043b3-455">Number of bytes to be reserved for check data.</span></span>

<span data-ttu-id="043b3-456">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="043b3-456">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="043b3-457">**унитсофусердата**</span><span class="sxs-lookup"><span data-stu-id="043b3-457">**UnitsOfUserData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="043b3-458">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="043b3-458">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="043b3-459">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="043b3-459">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="043b3-460">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Физические экстенты DMTF \| 001,8 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" байт ")</span><span class="sxs-lookup"><span data-stu-id="043b3-460">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Extent\|001.8"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="043b3-461">Число байтов, которое должно быть зарезервировано для данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="043b3-461">Number of bytes to be reserved for user data.</span></span>

<span data-ttu-id="043b3-462">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="043b3-462">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="043b3-463">Комментарии</span><span class="sxs-lookup"><span data-stu-id="043b3-463">Remarks</span></span>

<span data-ttu-id="043b3-464">Класс **CIM \_ фисикалекстент** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="043b3-464">The **CIM\_PhysicalExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="043b3-465">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="043b3-465">WMI does not implement this class.</span></span>

<span data-ttu-id="043b3-466">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="043b3-466">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="043b3-467">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="043b3-467">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="043b3-468">Требования</span><span class="sxs-lookup"><span data-stu-id="043b3-468">Requirements</span></span>



| <span data-ttu-id="043b3-469">Требование</span><span class="sxs-lookup"><span data-stu-id="043b3-469">Requirement</span></span> | <span data-ttu-id="043b3-470">Значение</span><span class="sxs-lookup"><span data-stu-id="043b3-470">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="043b3-471">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="043b3-471">Minimum supported client</span></span><br/> | <span data-ttu-id="043b3-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="043b3-472">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="043b3-473">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="043b3-473">Minimum supported server</span></span><br/> | <span data-ttu-id="043b3-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="043b3-474">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="043b3-475">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="043b3-475">Namespace</span></span><br/>                | <span data-ttu-id="043b3-476">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="043b3-476">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="043b3-477">MOF</span><span class="sxs-lookup"><span data-stu-id="043b3-477">MOF</span></span><br/>                      | <dl> <span data-ttu-id="043b3-478"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="043b3-478"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="043b3-479">DLL</span><span class="sxs-lookup"><span data-stu-id="043b3-479">DLL</span></span><br/>                      | <dl> <span data-ttu-id="043b3-480"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="043b3-480"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="043b3-481">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="043b3-481">See also</span></span>

<dl> <dt>

[<span data-ttu-id="043b3-482">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="043b3-482">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> </dl>

 

