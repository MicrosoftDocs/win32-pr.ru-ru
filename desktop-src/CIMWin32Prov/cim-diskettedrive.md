---
description: Класс CIM \_ дискеттедриве представляет возможности и управление флоппи-дисководом.
ms.assetid: 6c1bf597-ca67-4c37-8f90-d13afee0fab3
ms.tgt_platform: multiple
title: Класс CIM_DisketteDrive (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisketteDrive
- CIM_DisketteDrive.Availability
- CIM_DisketteDrive.Capabilities
- CIM_DisketteDrive.CapabilityDescriptions
- CIM_DisketteDrive.Caption
- CIM_DisketteDrive.CompressionMethod
- CIM_DisketteDrive.ConfigManagerErrorCode
- CIM_DisketteDrive.ConfigManagerUserConfig
- CIM_DisketteDrive.CreationClassName
- CIM_DisketteDrive.DefaultBlockSize
- CIM_DisketteDrive.Description
- CIM_DisketteDrive.DeviceID
- CIM_DisketteDrive.ErrorCleared
- CIM_DisketteDrive.ErrorDescription
- CIM_DisketteDrive.ErrorMethodology
- CIM_DisketteDrive.InstallDate
- CIM_DisketteDrive.LastErrorCode
- CIM_DisketteDrive.MaxBlockSize
- CIM_DisketteDrive.MaxMediaSize
- CIM_DisketteDrive.MinBlockSize
- CIM_DisketteDrive.Name
- CIM_DisketteDrive.NeedsCleaning
- CIM_DisketteDrive.NumberOfMediaSupported
- CIM_DisketteDrive.PNPDeviceID
- CIM_DisketteDrive.PowerManagementCapabilities
- CIM_DisketteDrive.PowerManagementSupported
- CIM_DisketteDrive.Status
- CIM_DisketteDrive.StatusInfo
- CIM_DisketteDrive.SystemCreationClassName
- CIM_DisketteDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 62570333225112bf734bf1a70a35f450be9df0ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655959"
---
# <a name="cim_diskettedrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="8361e-103">Класс CIM_DisketteDrive (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8361e-103">CIM_DisketteDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8361e-104">Класс **CIM \_ дискеттедриве** представляет возможности и управление флоппи-дисководом.</span><span class="sxs-lookup"><span data-stu-id="8361e-104">The **CIM\_DisketteDrive** class represents the capabilities and management of a diskette drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8361e-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8361e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8361e-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8361e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8361e-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8361e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8361e-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8361e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8361e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8361e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{F27851CD-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_DisketteDrive : CIM_MediaAccessDevice
{
  uint16   Availability;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CompressionMethod;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint64   DefaultBlockSize;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorMethodology;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  string   Name;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="8361e-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8361e-110">Members</span></span>

<span data-ttu-id="8361e-111">Класс **CIM \_ дискеттедриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8361e-111">The **CIM\_DisketteDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="8361e-112">Методы</span><span class="sxs-lookup"><span data-stu-id="8361e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="8361e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8361e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8361e-114">Методы</span><span class="sxs-lookup"><span data-stu-id="8361e-114">Methods</span></span>

<span data-ttu-id="8361e-115">Класс **CIM \_ дискеттедриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8361e-115">The **CIM\_DisketteDrive** class has these methods.</span></span>



| <span data-ttu-id="8361e-116">Метод</span><span class="sxs-lookup"><span data-stu-id="8361e-116">Method</span></span>                                                                | <span data-ttu-id="8361e-117">Описание</span><span class="sxs-lookup"><span data-stu-id="8361e-117">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8361e-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="8361e-118">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="8361e-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="8361e-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="8361e-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="8361e-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="8361e-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="8361e-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="8361e-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="8361e-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="8361e-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8361e-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="8361e-124">Properties</span></span>

<span data-ttu-id="8361e-125">Класс **CIM \_ дискеттедриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8361e-125">The **CIM\_DisketteDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8361e-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="8361e-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8361e-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="8361e-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-130">Availability and status of the device.</span></span>

<span data-ttu-id="8361e-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8361e-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8361e-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8361e-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="8361e-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="8361e-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="8361e-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="8361e-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="8361e-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="8361e-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="8361e-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8361e-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="8361e-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="8361e-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="8361e-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="8361e-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="8361e-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="8361e-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="8361e-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8361e-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="8361e-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="8361e-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="8361e-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="8361e-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="8361e-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="8361e-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="8361e-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="8361e-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="8361e-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="8361e-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="8361e-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="8361e-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="8361e-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="8361e-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="8361e-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="8361e-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="8361e-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="8361e-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="8361e-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="8361e-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="8361e-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="8361e-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="8361e-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="8361e-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="8361e-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="8361e-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="8361e-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="8361e-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="8361e-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="8361e-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="8361e-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="8361e-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-162">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8361e-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8361e-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-164">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="8361e-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-165">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="8361e-165">Capabilities of the media access device.</span></span> <span data-ttu-id="8361e-166">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-166">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8361e-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8361e-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-168">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="8361e-168">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8361e-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8361e-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-170">Другое</span><span class="sxs-lookup"><span data-stu-id="8361e-170">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="8361e-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="8361e-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-172">Последовательный доступ.</span><span class="sxs-lookup"><span data-stu-id="8361e-172">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="8361e-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="8361e-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-174">Произвольный доступ.</span><span class="sxs-lookup"><span data-stu-id="8361e-174">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="8361e-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="8361e-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-176">Запись.</span><span class="sxs-lookup"><span data-stu-id="8361e-176">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="8361e-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="8361e-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-178">Шифрование.</span><span class="sxs-lookup"><span data-stu-id="8361e-178">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="8361e-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="8361e-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-180">Сжатие.</span><span class="sxs-lookup"><span data-stu-id="8361e-180">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="8361e-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="8361e-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-182">Съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="8361e-182">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="8361e-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="8361e-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-184">Очистка вручную.</span><span class="sxs-lookup"><span data-stu-id="8361e-184">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="8361e-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="8361e-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-186">Автоматическая очистка.</span><span class="sxs-lookup"><span data-stu-id="8361e-186">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="8361e-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="8361e-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-188">ИНТЕЛЛЕКТУАЛЬНое уведомление.</span><span class="sxs-lookup"><span data-stu-id="8361e-188">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="8361e-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="8361e-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-190">Различает устройство, которое может получить доступ к обеим сторонам двусторонних носителей с устройства, которое считывает только одну сторону и требует включения носителя.</span><span class="sxs-lookup"><span data-stu-id="8361e-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="8361e-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="8361e-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-192">Указывает, что носитель не обязательно должен быть явно извлечен с устройства перед обращением к элементу выбора.</span><span class="sxs-lookup"><span data-stu-id="8361e-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-193">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="8361e-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-194">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="8361e-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8361e-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-196">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="8361e-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-197">Массив строк произвольной формы, которые содержат подробные пояснения для доступа к функциям устройств, указанным в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="8361e-197">Array of free-form strings that provide detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="8361e-198">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="8361e-198">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="8361e-199">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-199">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-200">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="8361e-200">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-203">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8361e-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-204">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8361e-204">Short textual description of the object.</span></span>

<span data-ttu-id="8361e-205">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-206">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="8361e-206">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-209">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="8361e-209">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="8361e-210">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="8361e-210">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="8361e-211">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="8361e-211">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="8361e-212">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="8361e-212">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="8361e-213">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-213">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="8361e-214">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8361e-214">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="8361e-215">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="8361e-215">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="8361e-216">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="8361e-216">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="8361e-217">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="8361e-217">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="8361e-218">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="8361e-218">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="8361e-219">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="8361e-219">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-220">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="8361e-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-221">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8361e-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-223">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8361e-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-224">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8361e-224">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="8361e-225">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="8361e-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="8361e-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="8361e-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="8361e-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-228">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="8361e-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="8361e-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="8361e-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="8361e-230">(1)</span><span class="sxs-lookup"><span data-stu-id="8361e-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-231">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="8361e-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8361e-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="8361e-233">(2)</span><span class="sxs-lookup"><span data-stu-id="8361e-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="8361e-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="8361e-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="8361e-235">(3)</span><span class="sxs-lookup"><span data-stu-id="8361e-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-236">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8361e-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8361e-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="8361e-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="8361e-238">(4)</span><span class="sxs-lookup"><span data-stu-id="8361e-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-239">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="8361e-239">Device is not working properly.</span></span> <span data-ttu-id="8361e-240">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="8361e-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="8361e-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="8361e-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="8361e-242">(5)</span><span class="sxs-lookup"><span data-stu-id="8361e-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-243">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="8361e-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="8361e-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="8361e-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="8361e-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="8361e-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-246">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="8361e-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="8361e-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="8361e-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="8361e-248">(7)</span><span class="sxs-lookup"><span data-stu-id="8361e-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="8361e-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="8361e-250">(8)</span><span class="sxs-lookup"><span data-stu-id="8361e-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-251">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="8361e-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="8361e-253">(9)</span><span class="sxs-lookup"><span data-stu-id="8361e-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-254">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-254">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="8361e-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="8361e-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="8361e-256">(10)</span><span class="sxs-lookup"><span data-stu-id="8361e-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-257">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="8361e-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="8361e-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="8361e-259">(11)</span><span class="sxs-lookup"><span data-stu-id="8361e-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-260">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="8361e-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="8361e-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="8361e-262">(12)</span><span class="sxs-lookup"><span data-stu-id="8361e-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-263">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="8361e-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="8361e-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="8361e-265">(13)</span><span class="sxs-lookup"><span data-stu-id="8361e-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-266">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="8361e-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="8361e-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="8361e-268">(14)</span><span class="sxs-lookup"><span data-stu-id="8361e-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-269">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="8361e-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="8361e-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="8361e-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="8361e-271">(15)</span><span class="sxs-lookup"><span data-stu-id="8361e-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-272">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="8361e-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="8361e-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="8361e-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="8361e-274">(16)</span><span class="sxs-lookup"><span data-stu-id="8361e-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-275">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="8361e-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="8361e-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="8361e-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="8361e-277">(17)</span><span class="sxs-lookup"><span data-stu-id="8361e-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-278">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="8361e-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8361e-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="8361e-280">(18)</span><span class="sxs-lookup"><span data-stu-id="8361e-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-281">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="8361e-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="8361e-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="8361e-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="8361e-283">(19)</span><span class="sxs-lookup"><span data-stu-id="8361e-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="8361e-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="8361e-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="8361e-285">(20)</span><span class="sxs-lookup"><span data-stu-id="8361e-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-286">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="8361e-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="8361e-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="8361e-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="8361e-288">(21)</span><span class="sxs-lookup"><span data-stu-id="8361e-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-289">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="8361e-289">System failure.</span></span> <span data-ttu-id="8361e-290">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="8361e-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="8361e-291">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="8361e-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="8361e-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="8361e-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="8361e-293">(22)</span><span class="sxs-lookup"><span data-stu-id="8361e-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-294">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="8361e-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="8361e-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="8361e-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="8361e-296">(23)</span><span class="sxs-lookup"><span data-stu-id="8361e-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-297">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="8361e-297">System failure.</span></span> <span data-ttu-id="8361e-298">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="8361e-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="8361e-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="8361e-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="8361e-300">(24)</span><span class="sxs-lookup"><span data-stu-id="8361e-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-301">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="8361e-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8361e-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="8361e-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8361e-303">(25)</span><span class="sxs-lookup"><span data-stu-id="8361e-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-304">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="8361e-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="8361e-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="8361e-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="8361e-306">(26)</span><span class="sxs-lookup"><span data-stu-id="8361e-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-307">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="8361e-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="8361e-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="8361e-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="8361e-309">(27)</span><span class="sxs-lookup"><span data-stu-id="8361e-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-310">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="8361e-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="8361e-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="8361e-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="8361e-312">(28)</span><span class="sxs-lookup"><span data-stu-id="8361e-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-313">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="8361e-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="8361e-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="8361e-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="8361e-315">(29)</span><span class="sxs-lookup"><span data-stu-id="8361e-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-316">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="8361e-316">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="8361e-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="8361e-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="8361e-318">(30)</span><span class="sxs-lookup"><span data-stu-id="8361e-318">(30)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-319">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="8361e-319">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="8361e-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="8361e-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="8361e-321">1-31</span><span class="sxs-lookup"><span data-stu-id="8361e-321">(31)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-322">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="8361e-322">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-323">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="8361e-323">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-324">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8361e-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-326">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8361e-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-327">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="8361e-327">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="8361e-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-329">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8361e-329">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-332">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8361e-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8361e-333">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="8361e-333">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="8361e-334">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="8361e-334">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="8361e-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-336">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="8361e-336">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-337">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8361e-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-339">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="8361e-339">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-340">D</span><span class="sxs-lookup"><span data-stu-id="8361e-340">D</span></span>

<span data-ttu-id="8361e-341">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="8361e-341">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="8361e-342">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-342">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="8361e-343">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8361e-343">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-344">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8361e-344">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-345">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-346">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-346">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-347">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="8361e-347">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-348">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="8361e-348">Textual description of the object.</span></span>

<span data-ttu-id="8361e-349">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-349">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-350">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="8361e-350">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-351">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-353">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8361e-353">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8361e-354">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-354">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="8361e-355">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-356">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="8361e-356">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-357">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8361e-357">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-359">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="8361e-359">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="8361e-360">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-361">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="8361e-361">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-364">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="8361e-364">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="8361e-365">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-365">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-366">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="8361e-366">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-367">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-368">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-369">Произвольная строка, описывающая тип обнаружения и исправления ошибок, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="8361e-369">Free-form string that describes the type of error detection and correction supported by the device.</span></span>

<span data-ttu-id="8361e-370">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-370">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-371">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8361e-371">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-372">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8361e-372">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-374">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="8361e-374">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-375">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="8361e-375">Date and time when the object was installed.</span></span> <span data-ttu-id="8361e-376">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="8361e-376">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8361e-377">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-377">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-378">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="8361e-378">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-379">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8361e-379">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-380">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-381">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="8361e-381">Last error code reported by the logical device.</span></span>

<span data-ttu-id="8361e-382">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-382">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-383">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="8361e-383">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-384">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8361e-384">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-386">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="8361e-386">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-387">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="8361e-387">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="8361e-388">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-388">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="8361e-389">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8361e-389">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-390">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="8361e-390">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-391">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8361e-391">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-393">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="8361e-393">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-394">Максимальный размер носителя, поддерживаемого устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="8361e-394">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="8361e-395">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="8361e-395">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="8361e-396">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="8361e-397">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8361e-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-398">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="8361e-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-399">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8361e-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-401">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="8361e-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-402">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="8361e-402">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="8361e-403">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="8361e-404">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8361e-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-405">**Name**</span><span class="sxs-lookup"><span data-stu-id="8361e-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-408">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="8361e-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-409">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="8361e-409">Label by which the object is known.</span></span> <span data-ttu-id="8361e-410">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="8361e-410">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="8361e-411">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-412">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="8361e-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-413">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8361e-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-415">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="8361e-415">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="8361e-416">Возможность ручной или автоматической очистки указывается в свойстве массива **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="8361e-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="8361e-417">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-418">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="8361e-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-419">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8361e-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-421">Если устройство доступа к носителю поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может быть поддерживается или вставлено.</span><span class="sxs-lookup"><span data-stu-id="8361e-421">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="8361e-422">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="8361e-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-426">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="8361e-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-427">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-427">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="8361e-428">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="8361e-429">Пример: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="8361e-429">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="8361e-430">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="8361e-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-431">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="8361e-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8361e-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-433">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="8361e-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="8361e-434">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8361e-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="8361e-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="8361e-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="8361e-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-437">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="8361e-437">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8361e-438"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="8361e-438"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8361e-439"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="8361e-439"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-440">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="8361e-440">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="8361e-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="8361e-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-442">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="8361e-442">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="8361e-443"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="8361e-443"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-444">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="8361e-444">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="8361e-445">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="8361e-445">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="8361e-446">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="8361e-446">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="8361e-447"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="8361e-447"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-448">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="8361e-448">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="8361e-449"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="8361e-449"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="8361e-450">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="8361e-450">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-451">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8361e-451">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-452">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8361e-452">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-453">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-453">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8361e-454">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="8361e-454">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="8361e-455">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="8361e-455">If **False**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="8361e-456">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="8361e-456">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="8361e-457">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="8361e-457">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="8361e-458">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-458">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-459">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="8361e-459">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-460">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-461">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-461">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-462">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="8361e-462">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-463">Указывает текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="8361e-463">Indicates the current status of the object.</span></span>

<span data-ttu-id="8361e-464">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-464">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8361e-465">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="8361e-465">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8361e-466">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="8361e-466">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8361e-467">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="8361e-467">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8361e-468">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="8361e-468">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8361e-469">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="8361e-469">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8361e-470">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="8361e-470">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8361e-471">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="8361e-471">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8361e-472">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="8361e-472">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8361e-473">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="8361e-473">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8361e-474">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="8361e-474">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8361e-475">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="8361e-475">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8361e-476">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="8361e-476">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8361e-477">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="8361e-477">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-478">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="8361e-478">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-479">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8361e-479">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-480">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-481">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="8361e-481">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="8361e-482">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="8361e-482">State of the logical device.</span></span> <span data-ttu-id="8361e-483">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="8361e-483">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="8361e-484">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-484">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="8361e-485">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="8361e-485">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8361e-486">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="8361e-486">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="8361e-487">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="8361e-487">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="8361e-488">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="8361e-488">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="8361e-489">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="8361e-489">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="8361e-490">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="8361e-490">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-491">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-491">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-492">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-492">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-493">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8361e-493">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8361e-494">Свойство свойства **CreationClassName** системы.</span><span class="sxs-lookup"><span data-stu-id="8361e-494">Scoping system's **CreationClassName** property.</span></span>

<span data-ttu-id="8361e-495">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-495">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="8361e-496">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8361e-496">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8361e-497">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="8361e-497">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8361e-498">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8361e-498">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8361e-499">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8361e-499">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8361e-500">Свойство **имени** системы области.</span><span class="sxs-lookup"><span data-stu-id="8361e-500">Scoping system's **Name** property.</span></span>

<span data-ttu-id="8361e-501">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="8361e-501">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8361e-502">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8361e-502">Remarks</span></span>

<span data-ttu-id="8361e-503">Класс **CIM \_ дискеттедриве** является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-503">The **CIM\_DisketteDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="8361e-504">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="8361e-504">WMI does not implement this class.</span></span> <span data-ttu-id="8361e-505">Классы, производные от **CIM \_ дискеттедриве**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8361e-505">For classes derived from **CIM\_DisketteDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8361e-506">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8361e-506">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8361e-507">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8361e-507">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8361e-508">Требования</span><span class="sxs-lookup"><span data-stu-id="8361e-508">Requirements</span></span>



| <span data-ttu-id="8361e-509">Требование</span><span class="sxs-lookup"><span data-stu-id="8361e-509">Requirement</span></span> | <span data-ttu-id="8361e-510">Значение</span><span class="sxs-lookup"><span data-stu-id="8361e-510">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8361e-511">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8361e-511">Minimum supported client</span></span><br/> | <span data-ttu-id="8361e-512">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8361e-512">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8361e-513">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8361e-513">Minimum supported server</span></span><br/> | <span data-ttu-id="8361e-514">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8361e-514">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8361e-515">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8361e-515">Namespace</span></span><br/>                | <span data-ttu-id="8361e-516">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8361e-516">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8361e-517">MOF</span><span class="sxs-lookup"><span data-stu-id="8361e-517">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8361e-518"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8361e-518"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8361e-519">DLL</span><span class="sxs-lookup"><span data-stu-id="8361e-519">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8361e-520"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8361e-520"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8361e-521">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8361e-521">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8361e-522">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="8361e-522">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

