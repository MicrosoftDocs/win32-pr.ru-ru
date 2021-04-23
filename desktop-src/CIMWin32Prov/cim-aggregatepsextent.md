---
description: Класс CIM \_ аггрегатепсекстент определяет количество адресацических логических блоков на одном запоминающем устройстве, исключая логические блоки, сопоставленные как проверочные данные.
ms.assetid: 6c188955-a963-414d-94f9-b7e1cb5960ed
ms.tgt_platform: multiple
title: Класс CIM_AggregatePSExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent
- CIM_AggregatePSExtent.Caption
- CIM_AggregatePSExtent.Description
- CIM_AggregatePSExtent.InstallDate
- CIM_AggregatePSExtent.Name
- CIM_AggregatePSExtent.Status
- CIM_AggregatePSExtent.Availability
- CIM_AggregatePSExtent.ConfigManagerErrorCode
- CIM_AggregatePSExtent.ConfigManagerUserConfig
- CIM_AggregatePSExtent.CreationClassName
- CIM_AggregatePSExtent.DeviceID
- CIM_AggregatePSExtent.PowerManagementCapabilities
- CIM_AggregatePSExtent.ErrorCleared
- CIM_AggregatePSExtent.ErrorDescription
- CIM_AggregatePSExtent.LastErrorCode
- CIM_AggregatePSExtent.PNPDeviceID
- CIM_AggregatePSExtent.PowerManagementSupported
- CIM_AggregatePSExtent.StatusInfo
- CIM_AggregatePSExtent.SystemCreationClassName
- CIM_AggregatePSExtent.SystemName
- CIM_AggregatePSExtent.Access
- CIM_AggregatePSExtent.BlockSize
- CIM_AggregatePSExtent.ErrorMethodology
- CIM_AggregatePSExtent.NumberOfBlocks
- CIM_AggregatePSExtent.Purpose
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: edc3f5b91bc39e18321778dbfdbc53446c6c27d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807690"
---
# <a name="cim_aggregatepsextent-class"></a><span data-ttu-id="d0535-103">\_Класс CIM аггрегатепсекстент</span><span class="sxs-lookup"><span data-stu-id="d0535-103">CIM\_AggregatePSExtent class</span></span>

<span data-ttu-id="d0535-104">Класс **CIM \_ аггрегатепсекстент** определяет количество адресацических логических блоков на одном запоминающем устройстве, исключая логические блоки, сопоставленные как проверочные данные.</span><span class="sxs-lookup"><span data-stu-id="d0535-104">The **CIM\_AggregatePSExtent** class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="d0535-105">Если определены наборы томов, логические блоки содержатся в одном наборе томов.</span><span class="sxs-lookup"><span data-stu-id="d0535-105">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="d0535-106">Это альтернативный вариант группировки для [**CIM \_ протектедспацеекстент**](cim-protectedspaceextent.md), когда требуются только сводные данные или используется автоматическая конфигурация.</span><span class="sxs-lookup"><span data-stu-id="d0535-106">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

<span data-ttu-id="d0535-107">Автоматическая настройка может привести к определению тысяч классов [**CIM \_ протектедспацеекстент**](cim-protectedspaceextent.md) .</span><span class="sxs-lookup"><span data-stu-id="d0535-107">Automatic configuration can result in thousands of [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) classes being defined.</span></span> <span data-ttu-id="d0535-108">Класс **CIM \_ аггрегатепсекстент** был определен таким образом, чтобы отдельные экстенты не требовались для моделирования.</span><span class="sxs-lookup"><span data-stu-id="d0535-108">The **CIM\_AggregatePSExtent** class was defined so that individual extents would not have to be modeled.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0535-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d0535-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d0535-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d0535-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d0535-111">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d0535-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d0535-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d0535-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0535-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0535-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D0E255C-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AggregatePSExtent : CIM_StorageExtent
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
  uint64   NumberOfBlocks;
  string   Purpose;
};
```

## <a name="members"></a><span data-ttu-id="d0535-114">Члены</span><span class="sxs-lookup"><span data-stu-id="d0535-114">Members</span></span>

<span data-ttu-id="d0535-115">Класс **CIM \_ аггрегатепсекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d0535-115">The **CIM\_AggregatePSExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="d0535-116">Методы</span><span class="sxs-lookup"><span data-stu-id="d0535-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="d0535-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0535-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d0535-118">Методы</span><span class="sxs-lookup"><span data-stu-id="d0535-118">Methods</span></span>

<span data-ttu-id="d0535-119">Класс **CIM \_ аггрегатепсекстент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d0535-119">The **CIM\_AggregatePSExtent** class has these methods.</span></span>



| <span data-ttu-id="d0535-120">Метод</span><span class="sxs-lookup"><span data-stu-id="d0535-120">Method</span></span>                                                                       | <span data-ttu-id="d0535-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d0535-121">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0535-122">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="d0535-122">**Reset**</span></span>](reset-method-in-class-cim-aggregatepsextent.md)                 | <span data-ttu-id="d0535-123">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d0535-123">Requests a reset of the logical device.</span></span> <span data-ttu-id="d0535-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d0535-124">Not implemented by WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="d0535-125">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="d0535-125">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-aggregatepsextent.md) | <span data-ttu-id="d0535-126">Определяет требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="d0535-126">Defines the desired power state for a logical device and when the device should be put into that state.</span></span> <span data-ttu-id="d0535-127">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="d0535-127">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d0535-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0535-128">Properties</span></span>

<span data-ttu-id="d0535-129">Класс **CIM \_ аггрегатепсекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d0535-129">The **CIM\_AggregatePSExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0535-130">**Доступ**</span><span class="sxs-lookup"><span data-stu-id="d0535-130">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0535-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-133">Описание свойств чтения и записи носителя.</span><span class="sxs-lookup"><span data-stu-id="d0535-133">Describes the read/write properties of the media.</span></span>

<span data-ttu-id="d0535-134">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-134">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0535-135">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d0535-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="d0535-136">**Для чтения** (1)</span><span class="sxs-lookup"><span data-stu-id="d0535-136">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="d0535-137">**Доступный для записи** (2)</span><span class="sxs-lookup"><span data-stu-id="d0535-137">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="d0535-138">**Поддерживается чтение и запись** (3)</span><span class="sxs-lookup"><span data-stu-id="d0535-138">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span data-ttu-id="d0535-139">**Однократная запись** (4)</span><span class="sxs-lookup"><span data-stu-id="d0535-139">**Write Once** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0535-140">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="d0535-140">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0535-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-143">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="d0535-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-144">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="d0535-144">Availability and status of the device.</span></span>

<span data-ttu-id="d0535-145">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-145">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d0535-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d0535-146"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0535-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d0535-147"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="d0535-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="d0535-148"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="d0535-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="d0535-149"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="d0535-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="d0535-150"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d0535-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="d0535-151"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="d0535-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="d0535-152"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="d0535-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="d0535-153"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="d0535-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="d0535-154"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0535-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="d0535-155"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="d0535-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="d0535-156"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="d0535-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="d0535-157"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="d0535-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="d0535-158"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-159">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="d0535-159">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="d0535-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="d0535-160"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-161">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="d0535-161">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="d0535-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="d0535-162"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-163">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="d0535-163">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="d0535-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="d0535-164"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="d0535-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="d0535-165"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-166">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="d0535-166">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="d0535-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="d0535-167"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-168">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="d0535-168">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="d0535-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="d0535-169"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-170">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="d0535-170">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="d0535-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="d0535-171"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-172">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="d0535-172">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="d0535-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="d0535-173"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-174">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="d0535-174">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0535-175">**BlockSize**</span><span class="sxs-lookup"><span data-stu-id="d0535-175">**BlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-176">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d0535-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-177">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-178">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Host-Resources-MIB. хрсторажеаллокатионунитс "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")</span><span class="sxs-lookup"><span data-stu-id="d0535-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageAllocationUnits"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-179">Размер (в байтах) блоков, образующих экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="d0535-179">Size, in bytes, of the blocks that form the storage extent.</span></span> <span data-ttu-id="d0535-180">Если размер блока переменной, то должен быть указан максимальный размер блока в байтах.</span><span class="sxs-lookup"><span data-stu-id="d0535-180">If variable block size, then the maximum block size, in bytes, should be specified.</span></span> <span data-ttu-id="d0535-181">Если размер блока неизвестен или не является допустимым понятием блока (например, для агрегатных экстентов, памяти или логических дисков), введите 1 (один).</span><span class="sxs-lookup"><span data-stu-id="d0535-181">If the block size is unknown, or if a block concept is not valid (for example, for aggregate extents, memory, or logical disks), enter a 1 (one).</span></span>

<span data-ttu-id="d0535-182">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d0535-182">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d0535-183">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-183">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-184">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d0535-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-187">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="d0535-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-188">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d0535-188">A short textual description of the object.</span></span>

<span data-ttu-id="d0535-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-190">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="d0535-190">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-191">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0535-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-193">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d0535-193">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-194">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="d0535-194">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="d0535-195">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-195">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="d0535-196">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="d0535-196">**This device is working properly.**</span></span> <span data-ttu-id="d0535-197"> (0)</span><span class="sxs-lookup"><span data-stu-id="d0535-197">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="d0535-198">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="d0535-198">**This device is not configured correctly.**</span></span> <span data-ttu-id="d0535-199">(1)</span><span class="sxs-lookup"><span data-stu-id="d0535-199">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d0535-200">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-200">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="d0535-201">(2)</span><span class="sxs-lookup"><span data-stu-id="d0535-201">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="d0535-202">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="d0535-202">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="d0535-203">(3)</span><span class="sxs-lookup"><span data-stu-id="d0535-203">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d0535-204">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="d0535-204">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="d0535-205">(4)</span><span class="sxs-lookup"><span data-stu-id="d0535-205">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="d0535-206">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="d0535-206">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="d0535-207">(5)</span><span class="sxs-lookup"><span data-stu-id="d0535-207">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="d0535-208">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="d0535-208">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="d0535-209"> (6)</span><span class="sxs-lookup"><span data-stu-id="d0535-209">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="d0535-210">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="d0535-210">**Cannot filter.**</span></span> <span data-ttu-id="d0535-211">(7)</span><span class="sxs-lookup"><span data-stu-id="d0535-211">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="d0535-212">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-212">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="d0535-213">(8)</span><span class="sxs-lookup"><span data-stu-id="d0535-213">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="d0535-214">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-214">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="d0535-215">(9)</span><span class="sxs-lookup"><span data-stu-id="d0535-215">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="d0535-216">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="d0535-216">**This device cannot start.**</span></span> <span data-ttu-id="d0535-217">(10)</span><span class="sxs-lookup"><span data-stu-id="d0535-217">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="d0535-218">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-218">**This device failed.**</span></span> <span data-ttu-id="d0535-219">(11)</span><span class="sxs-lookup"><span data-stu-id="d0535-219">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="d0535-220">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="d0535-220">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="d0535-221">(12)</span><span class="sxs-lookup"><span data-stu-id="d0535-221">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="d0535-222">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-222">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="d0535-223">(13)</span><span class="sxs-lookup"><span data-stu-id="d0535-223">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="d0535-224">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="d0535-224">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="d0535-225">(14)</span><span class="sxs-lookup"><span data-stu-id="d0535-225">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="d0535-226">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="d0535-226">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="d0535-227">(15)</span><span class="sxs-lookup"><span data-stu-id="d0535-227">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="d0535-228">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="d0535-228">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="d0535-229">(16)</span><span class="sxs-lookup"><span data-stu-id="d0535-229">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="d0535-230">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="d0535-230">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="d0535-231">(17)</span><span class="sxs-lookup"><span data-stu-id="d0535-231">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d0535-232">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-232">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="d0535-233">(18)</span><span class="sxs-lookup"><span data-stu-id="d0535-233">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="d0535-234">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="d0535-234">**Failure using the VxD loader.**</span></span> <span data-ttu-id="d0535-235">(19)</span><span class="sxs-lookup"><span data-stu-id="d0535-235">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="d0535-236">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="d0535-236">**Your registry might be corrupted.**</span></span> <span data-ttu-id="d0535-237">(20)</span><span class="sxs-lookup"><span data-stu-id="d0535-237">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="d0535-238">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="d0535-238">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="d0535-239">(21)</span><span class="sxs-lookup"><span data-stu-id="d0535-239">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="d0535-240">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="d0535-240">**This device is disabled.**</span></span> <span data-ttu-id="d0535-241">(22)</span><span class="sxs-lookup"><span data-stu-id="d0535-241">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="d0535-242">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="d0535-242">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="d0535-243">(23)</span><span class="sxs-lookup"><span data-stu-id="d0535-243">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="d0535-244">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="d0535-244">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="d0535-245">(24)</span><span class="sxs-lookup"><span data-stu-id="d0535-245">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d0535-246">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="d0535-246">**Windows is still setting up this device.**</span></span> <span data-ttu-id="d0535-247">(25)</span><span class="sxs-lookup"><span data-stu-id="d0535-247">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="d0535-248">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="d0535-248">**Windows is still setting up this device.**</span></span> <span data-ttu-id="d0535-249">(26)</span><span class="sxs-lookup"><span data-stu-id="d0535-249">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="d0535-250">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="d0535-250">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="d0535-251">(27)</span><span class="sxs-lookup"><span data-stu-id="d0535-251">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="d0535-252">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="d0535-252">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="d0535-253">(28)</span><span class="sxs-lookup"><span data-stu-id="d0535-253">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="d0535-254">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="d0535-254">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="d0535-255">(29)</span><span class="sxs-lookup"><span data-stu-id="d0535-255">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="d0535-256">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="d0535-256">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="d0535-257">(30)</span><span class="sxs-lookup"><span data-stu-id="d0535-257">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="d0535-258">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="d0535-258">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="d0535-259">1-31</span><span class="sxs-lookup"><span data-stu-id="d0535-259">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0535-260">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="d0535-260">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-261">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d0535-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-262">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-263">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d0535-263">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-264">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d0535-264">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="d0535-265">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-265">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-266">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="d0535-266">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-268">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-269">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d0535-269">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d0535-270">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="d0535-270">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="d0535-271">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="d0535-271">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="d0535-272">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-272">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-273">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d0535-273">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-274">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-275">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-276">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="d0535-276">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-277">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="d0535-277">A textual description of the object.</span></span>

<span data-ttu-id="d0535-278">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-278">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-279">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="d0535-279">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-280">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-281">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-282">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d0535-282">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d0535-283">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d0535-283">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="d0535-284">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-284">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-285">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="d0535-285">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-286">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d0535-286">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-287">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-287">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-288">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="d0535-288">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="d0535-289">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-289">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-290">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="d0535-290">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-291">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-291">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-292">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-293">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="d0535-293">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="d0535-294">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-294">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-295">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="d0535-295">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-296">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-297">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-297">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-298">Произвольная строка, описывающая тип обнаружения ошибок и исправления, поддерживаемые экстентом хранения.</span><span class="sxs-lookup"><span data-stu-id="d0535-298">Free-form string that describes the type of error detection and correction supported by the storage extent.</span></span>

<span data-ttu-id="d0535-299">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-299">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-300">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d0535-300">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-301">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d0535-301">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-303">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="d0535-303">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-304">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="d0535-304">Indicates when the object was installed.</span></span> <span data-ttu-id="d0535-305">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="d0535-305">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d0535-306">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-306">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-307">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="d0535-307">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-308">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0535-308">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-309">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-310">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="d0535-310">Last error code reported by the logical device.</span></span>

<span data-ttu-id="d0535-311">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-311">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-312">**Name**</span><span class="sxs-lookup"><span data-stu-id="d0535-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-315">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="d0535-315">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-316">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="d0535-316">Label by which the object is known.</span></span> <span data-ttu-id="d0535-317">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="d0535-317">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="d0535-318">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-318">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-319">**NumberOfBlocks**</span><span class="sxs-lookup"><span data-stu-id="d0535-319">**NumberOfBlocks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-320">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d0535-320">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-322">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Основной узел IETF-Resources-MIB. хрсторажесизе ")</span><span class="sxs-lookup"><span data-stu-id="d0535-322">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|HOST-RESOURCES-MIB.hrStorageSize")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-323">Количество последовательных блоков, каждый из которых заблокирует размер значения, содержащегося **в свойстве, которое** формирует экстент хранения.</span><span class="sxs-lookup"><span data-stu-id="d0535-323">Number of consecutive blocks, each block the size of the value contained in the **BlockSize** property, that form the storage extent.</span></span> <span data-ttu-id="d0535-324">Общий размер области хранения можно вычислить путем умножения **значения свойства размерности на значение** этого свойства.</span><span class="sxs-lookup"><span data-stu-id="d0535-324">Total size of the storage extent can be calculated by multiplying the value of the **BlockSize** property by the value of this property.</span></span> <span data-ttu-id="d0535-325">Если **значение параметра DataSize равно 1** (один), это свойство является общим размером экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="d0535-325">If the value of **BlockSize** is 1 (one), this property is the total size of the storage extent.</span></span>

<span data-ttu-id="d0535-326">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="d0535-326">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="d0535-327">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-327">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-328">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="d0535-328">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-331">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="d0535-331">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-332">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d0535-332">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="d0535-333">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="d0535-333">Example: "\*PNP030b"</span></span>

<span data-ttu-id="d0535-334">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-335">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="d0535-335">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-336">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="d0535-336">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d0535-337">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-337">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-338">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="d0535-338">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="d0535-339">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-339">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0535-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d0535-340"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-341">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="d0535-341">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="d0535-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="d0535-342"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-343">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="d0535-343">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d0535-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="d0535-344"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-345">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="d0535-345">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d0535-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="d0535-346"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-347">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="d0535-347">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="d0535-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="d0535-348"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-349">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="d0535-349">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="d0535-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="d0535-350"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-351">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="d0535-351">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="d0535-352">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="d0535-352">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="d0535-353">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="d0535-353">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="d0535-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="d0535-354"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-355">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="d0535-355">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="d0535-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="d0535-356"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d0535-357">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="d0535-357">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0535-358">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="d0535-358">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-359">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d0535-359">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-360">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-360">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-361">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="d0535-361">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="d0535-362">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="d0535-362">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d0535-363">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d0535-363">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="d0535-364">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="d0535-364">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="d0535-365">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-366">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="d0535-366">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0535-369">Строка свободной формы, описывающая носитель и его использование.</span><span class="sxs-lookup"><span data-stu-id="d0535-369">Free form string that describes the media and its use.</span></span>

<span data-ttu-id="d0535-370">Это свойство наследуется от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-370">This property is inherited from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-371">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="d0535-371">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-372">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-374">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="d0535-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-375">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="d0535-375">String that indicates the current status of the object.</span></span> <span data-ttu-id="d0535-376">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="d0535-376">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="d0535-377">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="d0535-377">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="d0535-378">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="d0535-378">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="d0535-379">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="d0535-379">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d0535-380">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="d0535-380">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d0535-381">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="d0535-381">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d0535-382">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-382">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="d0535-383">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="d0535-383">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="d0535-384">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="d0535-384">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="d0535-385">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="d0535-385">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="d0535-386">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="d0535-386">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0535-387">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="d0535-387">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="d0535-388">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="d0535-388">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="d0535-389">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="d0535-389">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="d0535-390">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="d0535-390">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="d0535-391">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="d0535-391">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="d0535-392">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="d0535-392">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="d0535-393">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="d0535-393">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="d0535-394">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="d0535-394">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="d0535-395">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="d0535-395">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0535-396">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="d0535-396">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-397">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d0535-397">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-398">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-399">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="d0535-399">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="d0535-400">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d0535-400">State of the logical device.</span></span> <span data-ttu-id="d0535-401">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="d0535-401">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="d0535-402">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-402">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d0535-403">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d0535-403">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d0535-404">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="d0535-404">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d0535-405">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="d0535-405">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d0535-406">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="d0535-406">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="d0535-407">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="d0535-407">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d0535-408">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="d0535-408">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-409">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-410">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-410">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-411">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d0535-411">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d0535-412">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="d0535-412">The scoping system's creation class name.</span></span>

<span data-ttu-id="d0535-413">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-413">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="d0535-414">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="d0535-414">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0535-415">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0535-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0535-416">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0535-416">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d0535-417">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d0535-417">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d0535-418">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="d0535-418">The scoping system's name.</span></span>

<span data-ttu-id="d0535-419">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="d0535-419">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0535-420">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d0535-420">Remarks</span></span>

<span data-ttu-id="d0535-421">Класс **CIM \_ аггрегатепсекстент** является производным от [**CIM \_ сторажеекстент**](cim-storageextent.md).</span><span class="sxs-lookup"><span data-stu-id="d0535-421">The **CIM\_AggregatePSExtent** class is derived from [**CIM\_StorageExtent**](cim-storageextent.md).</span></span>

<span data-ttu-id="d0535-422">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="d0535-422">WMI does not implement this class.</span></span>

<span data-ttu-id="d0535-423">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d0535-423">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d0535-424">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d0535-424">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0535-425">Требования</span><span class="sxs-lookup"><span data-stu-id="d0535-425">Requirements</span></span>



| <span data-ttu-id="d0535-426">Требование</span><span class="sxs-lookup"><span data-stu-id="d0535-426">Requirement</span></span> | <span data-ttu-id="d0535-427">Значение</span><span class="sxs-lookup"><span data-stu-id="d0535-427">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0535-428">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0535-428">Minimum supported client</span></span><br/> | <span data-ttu-id="d0535-429">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0535-429">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d0535-430">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0535-430">Minimum supported server</span></span><br/> | <span data-ttu-id="d0535-431">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0535-431">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d0535-432">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d0535-432">Namespace</span></span><br/>                | <span data-ttu-id="d0535-433">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d0535-433">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d0535-434">MOF</span><span class="sxs-lookup"><span data-stu-id="d0535-434">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0535-435"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0535-435"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0535-436">DLL</span><span class="sxs-lookup"><span data-stu-id="d0535-436">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0535-437"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0535-437"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0535-438">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0535-438">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0535-439">**\_СТОРАЖЕЕКСТЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="d0535-439">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dt>

[<span data-ttu-id="d0535-440">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="d0535-440">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

