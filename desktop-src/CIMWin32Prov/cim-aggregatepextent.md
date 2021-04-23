---
description: Класс CIM \_ аггрегатепекстент предоставляет сводные сведения об адресных логических блоках, которые находятся в одной группе избыточности хранилища и расположены на одном физическом носителе.
ms.assetid: c8def347-e8d7-48d5-94d0-f6e704e7b40e
ms.tgt_platform: multiple
title: Класс CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent
- CIM_AggregatePExtent.Caption
- CIM_AggregatePExtent.Description
- CIM_AggregatePExtent.InstallDate
- CIM_AggregatePExtent.Name
- CIM_AggregatePExtent.Status
- CIM_AggregatePExtent.Availability
- CIM_AggregatePExtent.ConfigManagerErrorCode
- CIM_AggregatePExtent.ConfigManagerUserConfig
- CIM_AggregatePExtent.CreationClassName
- CIM_AggregatePExtent.DeviceID
- CIM_AggregatePExtent.PowerManagementCapabilities
- CIM_AggregatePExtent.ErrorCleared
- CIM_AggregatePExtent.ErrorDescription
- CIM_AggregatePExtent.LastErrorCode
- CIM_AggregatePExtent.PNPDeviceID
- CIM_AggregatePExtent.PowerManagementSupported
- CIM_AggregatePExtent.StatusInfo
- CIM_AggregatePExtent.SystemCreationClassName
- CIM_AggregatePExtent.SystemName
- CIM_AggregatePExtent.Access
- CIM_AggregatePExtent.BlockSize
- CIM_AggregatePExtent.ErrorMethodology
- CIM_AggregatePExtent.Purpose
- CIM_AggregatePExtent.NumberOfBlocks
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2f1b2b5b7e08876317888d02d4830cd72659bc0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539080"
---
# <a name="cim_aggregatepextent-class"></a><span data-ttu-id="08717-103">\_Класс CIM аггрегатепекстент</span><span class="sxs-lookup"><span data-stu-id="08717-103">CIM\_AggregatePExtent class</span></span>

<span data-ttu-id="08717-104">Класс **CIM \_ аггрегатепекстент** предоставляет сводные сведения об адресных логических блоках, которые находятся в одной группе избыточности хранилища и расположены на одном физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="08717-104">The **CIM\_AggregatePExtent** class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

<span data-ttu-id="08717-105">Класс **CIM \_ аггрегатепекстент** является альтернативным группированием для физических экстентов, когда требуются только сводные данные или используется автоматическая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="08717-105">The **CIM\_AggregatePExtent** class is an alternative grouping for physical extents when only summary information is needed, or when automatic configuration is used.</span></span> <span data-ttu-id="08717-106">Автоматическая настройка может привести к определению тысяч физических экстентов.</span><span class="sxs-lookup"><span data-stu-id="08717-106">Automatic configuration can result in thousands of physical extents being defined.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08717-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="08717-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="08717-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="08717-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="08717-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="08717-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="08717-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="08717-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="08717-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08717-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{9565979F-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AggregatePExtent : CIM_StorageExtent
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   DeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  ErrorCleared;
  string   ErrorDescription;
  uint32   LastErrorCode;
  string   PNPDeviceID;
  boolean  PowerManagementSupported;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Access;
  uint64   BlockSize;
  string   ErrorMethodology;
  string   Purpose;
  uint64   NumberOfBlocks;
};
```

## <a name="members"></a><span data-ttu-id="08717-112">Члены</span><span class="sxs-lookup"><span data-stu-id="08717-112">Members</span></span>

<span data-ttu-id="08717-113">Класс **CIM \_ аггрегатепекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="08717-113">The **CIM\_AggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="08717-114">Методы</span><span class="sxs-lookup"><span data-stu-id="08717-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="08717-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="08717-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08717-116">Методы</span><span class="sxs-lookup"><span data-stu-id="08717-116">Methods</span></span>

<span data-ttu-id="08717-117">Класс **CIM \_ аггрегатепекстент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="08717-117">The **CIM\_AggregatePExtent** class has these methods.</span></span>



| <span data-ttu-id="08717-118">Метод</span><span class="sxs-lookup"><span data-stu-id="08717-118">Method</span></span>                                                                      | <span data-ttu-id="08717-119">Описание</span><span class="sxs-lookup"><span data-stu-id="08717-119">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08717-120">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="08717-120">**Reset**</span></span>](reset-method-in-class-cim-aggregatepextent.md)                 | <span data-ttu-id="08717-121">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="08717-121">Requests a reset of the logical device.</span></span> <span data-ttu-id="08717-122">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="08717-122">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="08717-123">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="08717-123">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepextent.md) | <span data-ttu-id="08717-124">Определяет требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="08717-124">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="08717-125">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="08717-125">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="08717-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="08717-126">Properties</span></span>

<span data-ttu-id="08717-127">Класс **CIM \_ аггрегатепекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="08717-127">The **CIM\_AggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="08717-128">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="08717-128">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-129">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08717-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08717-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-131">Описание свойств чтения и записи носителя.</span><span class="sxs-lookup"><span data-stu-id="08717-131">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="08717-132">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="08717-132">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08717-133">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="08717-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="08717-134">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="08717-134">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="08717-135">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="08717-135">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="08717-136">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="08717-136">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="08717-137">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="08717-137">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08717-138">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="08717-138">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08717-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08717-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-141">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="08717-141">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="08717-142">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="08717-142">Availability and status of the device.</span></span>

<span data-ttu-id="08717-143">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-143">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="08717-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="08717-144"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08717-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="08717-145"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="08717-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="08717-146"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="08717-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="08717-147"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="08717-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="08717-148"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="08717-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="08717-149"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="08717-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="08717-150"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="08717-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="08717-151"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="08717-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="08717-152"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="08717-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="08717-153"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="08717-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="08717-154"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="08717-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="08717-155"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="08717-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="08717-156"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="08717-157">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="08717-157">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="08717-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="08717-158"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="08717-159">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="08717-159">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="08717-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="08717-160"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="08717-161">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="08717-161">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="08717-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="08717-162"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="08717-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="08717-163"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="08717-164">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="08717-164">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="08717-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="08717-165"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="08717-166">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="08717-166">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="08717-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="08717-167"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="08717-168">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="08717-168">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="08717-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="08717-169"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="08717-170">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="08717-170">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="08717-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="08717-171"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="08717-172">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="08717-172">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08717-173">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="08717-173">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-174">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08717-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08717-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-176">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="08717-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="08717-177">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="08717-177">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="08717-178">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="08717-178">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="08717-179">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="08717-179">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="08717-180">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="08717-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="08717-181">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="08717-181">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-182">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="08717-182">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-184">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-185">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="08717-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="08717-186">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="08717-186">A short textual description of the object.</span></span>

<span data-ttu-id="08717-187">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08717-187">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-188">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="08717-188">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-189">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08717-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08717-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-191">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="08717-191">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="08717-192">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="08717-192">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="08717-193">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-193">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="08717-194">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="08717-194">**This device is working properly.**</span></span> <span data-ttu-id="08717-195"> (0)</span><span class="sxs-lookup"><span data-stu-id="08717-195">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="08717-196">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="08717-196">**This device is not configured correctly.**</span></span> <span data-ttu-id="08717-197">(1)</span><span class="sxs-lookup"><span data-stu-id="08717-197">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="08717-198">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-198">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="08717-199">(2)</span><span class="sxs-lookup"><span data-stu-id="08717-199">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="08717-200">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="08717-200">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="08717-201">(3)</span><span class="sxs-lookup"><span data-stu-id="08717-201">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="08717-202">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="08717-202">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="08717-203">(4)</span><span class="sxs-lookup"><span data-stu-id="08717-203">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="08717-204">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="08717-204">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="08717-205">(5)</span><span class="sxs-lookup"><span data-stu-id="08717-205">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="08717-206">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="08717-206">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="08717-207"> (6)</span><span class="sxs-lookup"><span data-stu-id="08717-207">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="08717-208">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="08717-208">**Cannot filter.**</span></span> <span data-ttu-id="08717-209">(7)</span><span class="sxs-lookup"><span data-stu-id="08717-209">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="08717-210">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-210">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="08717-211">(8)</span><span class="sxs-lookup"><span data-stu-id="08717-211">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="08717-212">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-212">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="08717-213">(9)</span><span class="sxs-lookup"><span data-stu-id="08717-213">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="08717-214">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="08717-214">**This device cannot start.**</span></span> <span data-ttu-id="08717-215">(10)</span><span class="sxs-lookup"><span data-stu-id="08717-215">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="08717-216">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-216">**This device failed.**</span></span> <span data-ttu-id="08717-217">(11)</span><span class="sxs-lookup"><span data-stu-id="08717-217">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="08717-218">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="08717-218">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="08717-219">(12)</span><span class="sxs-lookup"><span data-stu-id="08717-219">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="08717-220">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-220">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="08717-221">(13)</span><span class="sxs-lookup"><span data-stu-id="08717-221">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="08717-222">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="08717-222">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="08717-223">(14)</span><span class="sxs-lookup"><span data-stu-id="08717-223">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="08717-224">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="08717-224">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="08717-225">(15)</span><span class="sxs-lookup"><span data-stu-id="08717-225">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="08717-226">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="08717-226">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="08717-227">(16)</span><span class="sxs-lookup"><span data-stu-id="08717-227">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="08717-228">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="08717-228">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="08717-229">(17)</span><span class="sxs-lookup"><span data-stu-id="08717-229">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="08717-230">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-230">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="08717-231">(18)</span><span class="sxs-lookup"><span data-stu-id="08717-231">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="08717-232">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="08717-232">**Failure using the VxD loader.**</span></span> <span data-ttu-id="08717-233">(19)</span><span class="sxs-lookup"><span data-stu-id="08717-233">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="08717-234">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="08717-234">**Your registry might be corrupted.**</span></span> <span data-ttu-id="08717-235">(20)</span><span class="sxs-lookup"><span data-stu-id="08717-235">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="08717-236">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="08717-236">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="08717-237">(21)</span><span class="sxs-lookup"><span data-stu-id="08717-237">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="08717-238">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="08717-238">**This device is disabled.**</span></span> <span data-ttu-id="08717-239">(22)</span><span class="sxs-lookup"><span data-stu-id="08717-239">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="08717-240">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="08717-240">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="08717-241">(23)</span><span class="sxs-lookup"><span data-stu-id="08717-241">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="08717-242">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="08717-242">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="08717-243">(24)</span><span class="sxs-lookup"><span data-stu-id="08717-243">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="08717-244">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="08717-244">**Windows is still setting up this device.**</span></span> <span data-ttu-id="08717-245">(25)</span><span class="sxs-lookup"><span data-stu-id="08717-245">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="08717-246">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="08717-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="08717-247">(26)</span><span class="sxs-lookup"><span data-stu-id="08717-247">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="08717-248">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="08717-248">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="08717-249">(27)</span><span class="sxs-lookup"><span data-stu-id="08717-249">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="08717-250">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="08717-250">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="08717-251">(28)</span><span class="sxs-lookup"><span data-stu-id="08717-251">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="08717-252">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="08717-252">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="08717-253">(29)</span><span class="sxs-lookup"><span data-stu-id="08717-253">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="08717-254">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="08717-254">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="08717-255">(30)</span><span class="sxs-lookup"><span data-stu-id="08717-255">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="08717-256">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="08717-256">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="08717-257">1-31</span><span class="sxs-lookup"><span data-stu-id="08717-257">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08717-258">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="08717-258">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-259">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="08717-259">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08717-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-261">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="08717-261">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="08717-262">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="08717-262">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="08717-263">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-263">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-264">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="08717-264">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-265">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-266">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-266">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-267">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08717-267">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08717-268">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="08717-268">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="08717-269">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="08717-269">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="08717-270">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-270">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-271">**Описание**</span><span class="sxs-lookup"><span data-stu-id="08717-271">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-272">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-273">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-274">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="08717-274">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="08717-275">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="08717-275">A textual description of the object.</span></span>

<span data-ttu-id="08717-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08717-276">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-277">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="08717-277">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-278">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-278">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-279">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-279">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-280">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08717-280">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08717-281">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="08717-281">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="08717-282">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-282">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-283">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="08717-283">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-284">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="08717-284">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08717-285">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-286">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="08717-286">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="08717-287">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-287">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-288">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="08717-288">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-291">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="08717-291">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="08717-292">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-292">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-293">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="08717-293">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-296">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="08717-296">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="08717-297">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="08717-297">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-298">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="08717-298">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-299">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="08717-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="08717-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-301">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="08717-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="08717-302">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="08717-302">Indicates when the object was installed.</span></span> <span data-ttu-id="08717-303">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="08717-303">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="08717-304">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08717-304">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-305">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="08717-305">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-306">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="08717-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="08717-307">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-307">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-308">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="08717-308">Last error code reported by the logical device.</span></span>

<span data-ttu-id="08717-309">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-309">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-310">**Name**</span><span class="sxs-lookup"><span data-stu-id="08717-310">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-311">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-311">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-312">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-313">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="08717-313">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="08717-314">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="08717-314">Label by which the object is known.</span></span> <span data-ttu-id="08717-315">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="08717-315">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="08717-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08717-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-317">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="08717-317">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-318">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="08717-318">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="08717-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-320">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("нумберофблоккс"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Статистическое вычисление физического экстента DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="08717-320">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NumberOfBlocks"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Aggregate Physical Extent\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="08717-321">Общее число блоков (включая блоки данных проверки), содержащихся в этой статистической физической области.</span><span class="sxs-lookup"><span data-stu-id="08717-321">Total number of blocks (including the check data blocks) contained in this aggregate physical extent.</span></span> <span data-ttu-id="08717-322">Размер блока (унаследованное свойство) должен иметь то же значение, что и устройство доступа к носителю, связанное с этим экстентом.</span><span class="sxs-lookup"><span data-stu-id="08717-322">The block size (an inherited property) should be set to the same value as for the media access device associated with this extent.</span></span>

</dd> <dt>

<span data-ttu-id="08717-323">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="08717-323">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-326">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="08717-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="08717-327">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="08717-327">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="08717-328">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="08717-328">Example: "\*PNP030b"</span></span>

<span data-ttu-id="08717-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-330">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="08717-330">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-331">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="08717-331">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="08717-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-333">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="08717-333">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="08717-334">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08717-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="08717-335"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="08717-336">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="08717-336">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="08717-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="08717-337"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="08717-338">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="08717-338">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="08717-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="08717-339"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="08717-340">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="08717-340">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="08717-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="08717-341"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="08717-342">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="08717-342">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="08717-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="08717-343"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="08717-344">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="08717-344">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="08717-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="08717-345"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="08717-346">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="08717-346">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="08717-347">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="08717-347">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="08717-348">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="08717-348">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="08717-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="08717-349"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="08717-350">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="08717-350">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="08717-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="08717-351"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="08717-352">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="08717-352">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="08717-353">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="08717-353">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-354">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="08717-354">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08717-355">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-355">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-356">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="08717-356">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="08717-357">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="08717-357">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="08717-358">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="08717-358">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="08717-359">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="08717-359">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="08717-360">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-361">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="08717-361">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="08717-364">Строка свободной формы, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="08717-364">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="08717-365">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="08717-365">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-366">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="08717-366">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-369">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="08717-369">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="08717-370">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="08717-370">String that indicates the current status of the object.</span></span> <span data-ttu-id="08717-371">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="08717-371">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="08717-372">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="08717-372">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="08717-373">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="08717-373">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="08717-374">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="08717-374">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="08717-375">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="08717-375">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="08717-376">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="08717-376">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="08717-377">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="08717-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="08717-378">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="08717-378">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="08717-379">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="08717-379">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="08717-380">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="08717-380">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="08717-381">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="08717-381">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08717-382">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="08717-382">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="08717-383">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="08717-383">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="08717-384">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="08717-384">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="08717-385">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="08717-385">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="08717-386">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="08717-386">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="08717-387">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="08717-387">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="08717-388">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="08717-388">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="08717-389">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="08717-389">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="08717-390">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="08717-390">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08717-391">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="08717-391">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-392">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="08717-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="08717-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="08717-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="08717-395">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="08717-395">State of the logical device.</span></span> <span data-ttu-id="08717-396">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="08717-396">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="08717-397">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="08717-398">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="08717-398">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="08717-399">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="08717-399">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="08717-400">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="08717-400">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="08717-401">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="08717-401">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="08717-402">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="08717-402">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="08717-403">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="08717-403">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-404">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-405">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-406">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08717-406">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08717-407">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="08717-407">The scoping system's creation class name.</span></span>

<span data-ttu-id="08717-408">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-408">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="08717-409">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="08717-409">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08717-410">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="08717-410">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08717-411">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="08717-411">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08717-412">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="08717-412">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="08717-413">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="08717-413">The scoping system's name.</span></span>

<span data-ttu-id="08717-414">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="08717-414">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08717-415">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08717-415">Remarks</span></span>

<span data-ttu-id="08717-416">Класс **CIM \_ аггрегатепекстент** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="08717-416">The **CIM\_AggregatePExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="08717-417">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="08717-417">WMI does not implement this class.</span></span>

<span data-ttu-id="08717-418">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="08717-418">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="08717-419">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="08717-419">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="08717-420">Требования</span><span class="sxs-lookup"><span data-stu-id="08717-420">Requirements</span></span>



| <span data-ttu-id="08717-421">Требование</span><span class="sxs-lookup"><span data-stu-id="08717-421">Requirement</span></span> | <span data-ttu-id="08717-422">Значение</span><span class="sxs-lookup"><span data-stu-id="08717-422">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08717-423">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08717-423">Minimum supported client</span></span><br/> | <span data-ttu-id="08717-424">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08717-424">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08717-425">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08717-425">Minimum supported server</span></span><br/> | <span data-ttu-id="08717-426">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08717-426">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08717-427">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="08717-427">Namespace</span></span><br/>                | <span data-ttu-id="08717-428">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="08717-428">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08717-429">MOF</span><span class="sxs-lookup"><span data-stu-id="08717-429">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08717-430"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08717-430"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08717-431">DLL</span><span class="sxs-lookup"><span data-stu-id="08717-431">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08717-432"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08717-432"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08717-433">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08717-433">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08717-434">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="08717-434">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="08717-435">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="08717-435">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

