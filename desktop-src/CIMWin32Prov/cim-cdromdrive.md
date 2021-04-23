---
description: Класс CIM \_ кдромдриве представляет устройство чтения компакт-дисков на компьютере.
ms.assetid: 044c9687-fc25-4a8c-b2ef-bd7ea332af7b
ms.tgt_platform: multiple
title: Класс CIM_CDROMDrive (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive
- CIM_CDROMDrive.Caption
- CIM_CDROMDrive.Description
- CIM_CDROMDrive.InstallDate
- CIM_CDROMDrive.Name
- CIM_CDROMDrive.Status
- CIM_CDROMDrive.Availability
- CIM_CDROMDrive.ConfigManagerErrorCode
- CIM_CDROMDrive.ConfigManagerUserConfig
- CIM_CDROMDrive.CreationClassName
- CIM_CDROMDrive.DeviceID
- CIM_CDROMDrive.PowerManagementCapabilities
- CIM_CDROMDrive.ErrorCleared
- CIM_CDROMDrive.ErrorDescription
- CIM_CDROMDrive.LastErrorCode
- CIM_CDROMDrive.PNPDeviceID
- CIM_CDROMDrive.PowerManagementSupported
- CIM_CDROMDrive.StatusInfo
- CIM_CDROMDrive.SystemCreationClassName
- CIM_CDROMDrive.SystemName
- CIM_CDROMDrive.Capabilities
- CIM_CDROMDrive.CapabilityDescriptions
- CIM_CDROMDrive.CompressionMethod
- CIM_CDROMDrive.DefaultBlockSize
- CIM_CDROMDrive.ErrorMethodology
- CIM_CDROMDrive.MaxBlockSize
- CIM_CDROMDrive.MaxMediaSize
- CIM_CDROMDrive.MinBlockSize
- CIM_CDROMDrive.NeedsCleaning
- CIM_CDROMDrive.NumberOfMediaSupported
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 499607e050124533465a40da9e73d433142e6515
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896121"
---
# <a name="cim_cdromdrive-class-cimwin32-wmi-providers"></a><span data-ttu-id="9ff6e-103">Класс CIM_CDROMDrive (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-103">CIM_CDROMDrive class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="9ff6e-104">Класс **CIM \_ кдромдриве** представляет устройство чтения компакт-дисков на компьютере.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-104">The **CIM\_CDROMDrive** class represents a CD-ROM drive on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="9ff6e-105">Имя диска не соответствует букве логического диска, назначенной устройству. это имя логического устройства хранения, которое зависит от диска.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-105">The name of the drive does not correspond to the logical drive letter assigned to the device, which is the name of the logical storage device that is dependent on the drive.</span></span>

 

> [!IMPORTANT]
> <span data-ttu-id="9ff6e-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9ff6e-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9ff6e-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9ff6e-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff6e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ff6e-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C52B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_CDROMDrive : CIM_MediaAccessDevice
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
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   CompressionMethod;
  uint64   DefaultBlockSize;
  string   ErrorMethodology;
  uint64   MaxBlockSize;
  uint64   MaxMediaSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  uint32   NumberOfMediaSupported;
};
```

## <a name="members"></a><span data-ttu-id="9ff6e-111">Члены</span><span class="sxs-lookup"><span data-stu-id="9ff6e-111">Members</span></span>

<span data-ttu-id="9ff6e-112">Класс **CIM \_ кдромдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ff6e-112">The **CIM\_CDROMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="9ff6e-113">Методы</span><span class="sxs-lookup"><span data-stu-id="9ff6e-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="9ff6e-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ff6e-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9ff6e-115">Методы</span><span class="sxs-lookup"><span data-stu-id="9ff6e-115">Methods</span></span>

<span data-ttu-id="9ff6e-116">Класс **CIM \_ кдромдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-116">The **CIM\_CDROMDrive** class has these methods.</span></span>



| <span data-ttu-id="9ff6e-117">Метод</span><span class="sxs-lookup"><span data-stu-id="9ff6e-117">Method</span></span>                                                                | <span data-ttu-id="9ff6e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="9ff6e-118">Description</span></span>                                                                                                                              |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ff6e-119">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-119">**Reset**</span></span>](reset-method-in-class-cim-cdromdrive.md)                 | <span data-ttu-id="9ff6e-120">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-120">Requests a reset of the logical device.</span></span> <span data-ttu-id="9ff6e-121">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-121">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="9ff6e-122">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-122">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-cdromdrive.md) | <span data-ttu-id="9ff6e-123">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-123">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="9ff6e-124">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-124">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9ff6e-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ff6e-125">Properties</span></span>

<span data-ttu-id="9ff6e-126">Класс **CIM \_ кдромдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-126">The **CIM\_CDROMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ff6e-127">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-127">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-128">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-130">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-131">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-131">Availability and status of the device.</span></span>

<span data-ttu-id="9ff6e-132">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-132">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ff6e-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-133"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ff6e-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-134"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="9ff6e-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-135"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="9ff6e-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="9ff6e-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9ff6e-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="9ff6e-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="9ff6e-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="9ff6e-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ff6e-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="9ff6e-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="9ff6e-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="9ff6e-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-146">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="9ff6e-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-148">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="9ff6e-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-150">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-150">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="9ff6e-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="9ff6e-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-153">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="9ff6e-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-155">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="9ff6e-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-157">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="9ff6e-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-159">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="9ff6e-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-161">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-163">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9ff6e-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-165">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-166">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-166">Capabilities of the media access device.</span></span>

<span data-ttu-id="9ff6e-167">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ff6e-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-169">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-169">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ff6e-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-170"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-171">Другое</span><span class="sxs-lookup"><span data-stu-id="9ff6e-171">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="9ff6e-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-172"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-173">Последовательный доступ.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-173">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="9ff6e-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-174"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-175">Произвольный доступ.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-175">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="9ff6e-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-176"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-177">Запись.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-177">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="9ff6e-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-179">Шифрование.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-179">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="9ff6e-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-180"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-181">Сжатие.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-181">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="9ff6e-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-182"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-183">Съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-183">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="9ff6e-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-184"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-185">Очистка вручную.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-185">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="9ff6e-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-186"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-187">Автоматическая очистка.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-187">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="9ff6e-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-188"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-189">ИНТЕЛЛЕКТУАЛЬНое уведомление.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-189">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="9ff6e-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-190"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-191">Различает устройство, которое может получить доступ к обеим сторонам двусторонних носителей с устройства, которое считывает только одну сторону и требует включения носителя.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-191">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="9ff6e-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-192"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-193">Указывает, что носитель не обязательно должен быть явно извлечен с устройства перед обращением к элементу выбора.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-193">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-194">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-194">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-195">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-195">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-196">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-197">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-197">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-198">Массив строк произвольной формы, который содержит подробные пояснения для доступа к функциям устройств, указанным в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-198">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="9ff6e-199">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-199">Each entry of this array is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="9ff6e-200">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-200">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-201">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-201">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-204">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-204">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-205">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-205">A short textual description of the object.</span></span>

<span data-ttu-id="9ff6e-206">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-207">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-207">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-210">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-210">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="9ff6e-211">Если невозможно описать схему сжатия (так как она неизвестна), используйте следующую команду: Если, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="9ff6e-211">If it is not possible to describe the compression scheme (because it is unknown), use the following:If , use "Unknown".</span></span> <span data-ttu-id="9ff6e-212">Если значение равно, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="9ff6e-212">If , use "Compressed".</span></span> <span data-ttu-id="9ff6e-213">, используйте "not сжатый".</span><span class="sxs-lookup"><span data-stu-id="9ff6e-213">, use "Not Compressed".</span></span>

<span data-ttu-id="9ff6e-214">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-214">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="9ff6e-215">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-215">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-216">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-216">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="9ff6e-217">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-217">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-218">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="9ff6e-218">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="9ff6e-219">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-219">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-220">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="9ff6e-220">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-221">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-221">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-222">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-223">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-224">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-224">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-225">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-225">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="9ff6e-226">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-226">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="9ff6e-227">**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-227">**This device is working properly.**</span></span> <span data-ttu-id="9ff6e-228"> (0)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-228">(0)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="9ff6e-229">**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-229">**This device is not configured correctly.**</span></span> <span data-ttu-id="9ff6e-230">(1)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-230">(1)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ff6e-231">**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-231">**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="9ff6e-232">(2)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-232">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="9ff6e-233">**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-233">**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="9ff6e-234">(3)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-234">(3)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9ff6e-235">**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-235">**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="9ff6e-236">(4)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-236">(4)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="9ff6e-237">**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-237">**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="9ff6e-238">(5)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-238">(5)</span></span>


</dt> <dd></dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="9ff6e-239">**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-239">**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="9ff6e-240"> (6)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-240">(6)</span></span>


</dt> <dd></dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="9ff6e-241">**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-241">**Cannot filter.**</span></span> <span data-ttu-id="9ff6e-242">(7)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-242">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="9ff6e-243">**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-243">**The driver loader for the device is missing.**</span></span> <span data-ttu-id="9ff6e-244">(8)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-244">(8)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="9ff6e-245">**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-245">**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="9ff6e-246">(9)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-246">(9)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="9ff6e-247">**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-247">**This device cannot start.**</span></span> <span data-ttu-id="9ff6e-248">(10)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-248">(10)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="9ff6e-249">**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-249">**This device failed.**</span></span> <span data-ttu-id="9ff6e-250">(11)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-250">(11)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="9ff6e-251">**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-251">**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="9ff6e-252">(12)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-252">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="9ff6e-253">**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-253">**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="9ff6e-254">(13)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-254">(13)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="9ff6e-255">**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-255">**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="9ff6e-256">(14)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-256">(14)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="9ff6e-257">**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-257">**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="9ff6e-258">(15)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-258">(15)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="9ff6e-259">**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-259">**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="9ff6e-260">(16)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-260">(16)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="9ff6e-261">**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-261">**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="9ff6e-262">(17)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-262">(17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ff6e-263">**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-263">**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="9ff6e-264">(18)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-264">(18)</span></span>


</dt> <dd></dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="9ff6e-265">**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-265">**Failure using the VxD loader.**</span></span> <span data-ttu-id="9ff6e-266">(19)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-266">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="9ff6e-267">**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-267">**Your registry might be corrupted.**</span></span> <span data-ttu-id="9ff6e-268">(20)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-268">(20)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="9ff6e-269">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-269">**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="9ff6e-270">(21)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-270">(21)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="9ff6e-271">**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-271">**This device is disabled.**</span></span> <span data-ttu-id="9ff6e-272">(22)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-272">(22)</span></span>


</dt> <dd></dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="9ff6e-273">**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-273">**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="9ff6e-274">(23)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-274">(23)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="9ff6e-275">**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-275">**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="9ff6e-276">(24)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-276">(24)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9ff6e-277">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-277">**Windows is still setting up this device.**</span></span> <span data-ttu-id="9ff6e-278">(25)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-278">(25)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="9ff6e-279">**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-279">**Windows is still setting up this device.**</span></span> <span data-ttu-id="9ff6e-280">(26)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-280">(26)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="9ff6e-281">**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-281">**This device does not have valid log configuration.**</span></span> <span data-ttu-id="9ff6e-282">(27)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-282">(27)</span></span>


</dt> <dd></dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="9ff6e-283">**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-283">**The drivers for this device are not installed.**</span></span> <span data-ttu-id="9ff6e-284">(28)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-284">(28)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="9ff6e-285">**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-285">**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="9ff6e-286">(29)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-286">(29)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="9ff6e-287">**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-287">**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="9ff6e-288">(30)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-288">(30)</span></span>


</dt> <dd></dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="9ff6e-289">**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-289">**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="9ff6e-290">1-31</span><span class="sxs-lookup"><span data-stu-id="9ff6e-290">(31)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-291">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-291">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-292">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-292">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-293">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-293">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-294">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-294">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-295">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-295">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="9ff6e-296">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-296">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-297">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-297">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-298">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-300">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-300">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-301">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-301">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="9ff6e-302">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-302">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="9ff6e-303">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-303">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-304">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-304">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-305">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-305">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-307">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-307">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-308">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-308">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="9ff6e-309">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-309">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9ff6e-310">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-310">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-311">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-311">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-312">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-313">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-314">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-314">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-315">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-315">A textual description of the object.</span></span>

<span data-ttu-id="9ff6e-316">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-317">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-317">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-318">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-320">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-320">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-321">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-321">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="9ff6e-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-323">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-323">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-324">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-325">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-326">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-326">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="9ff6e-327">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-327">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-328">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-328">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-329">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-330">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-330">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-331">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-331">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="9ff6e-332">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-332">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-333">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-333">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-334">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-335">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-335">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-336">Произвольная строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые устройством.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-336">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="9ff6e-337">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-338">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-338">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-339">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-339">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-340">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-340">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-341">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-341">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-342">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-342">Indicates when the object was installed.</span></span> <span data-ttu-id="9ff6e-343">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-343">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9ff6e-344">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-345">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-345">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-346">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-346">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-347">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-348">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-348">Last error code reported by the logical device.</span></span>

<span data-ttu-id="9ff6e-349">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-349">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-350">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-350">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-351">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-351">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-353">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-353">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-354">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-354">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="9ff6e-355">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-355">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9ff6e-356">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-356">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-357">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-357">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-358">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-359">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-359">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-360">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-360">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-361">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-361">Maximum size, in kilobytes, of media supported by this device.</span></span> <span data-ttu-id="9ff6e-362">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-362">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="9ff6e-363">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-363">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9ff6e-364">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-364">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-365">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-365">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-366">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-366">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-368">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-368">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-369">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-369">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="9ff6e-370">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-370">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9ff6e-371">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-371">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-372">**Name**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-372">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-373">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-374">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-374">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-375">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-375">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-376">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-376">Label by which the object is known.</span></span> <span data-ttu-id="9ff6e-377">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-377">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="9ff6e-378">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-378">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-379">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-379">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-380">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-380">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-382">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-382">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="9ff6e-383">Возможность ручной или автоматической очистки указывается в свойстве массива **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-383">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="9ff6e-384">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-384">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-385">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-385">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-386">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-386">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-387">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-387">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-388">Максимальное количество отдельных носителей, которые могут быть поддерживаются или вставлены.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-388">Maximum number of multiple individual media that can be supported or inserted.</span></span>

<span data-ttu-id="9ff6e-389">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-390">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-390">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-391">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-392">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-392">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-393">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-393">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-394">Указывает идентификатор устройства Win32 самонастраивающийся для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-394">Indicates the Win32 Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="9ff6e-395">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="9ff6e-395">Example: "\*PNP030b"</span></span>

<span data-ttu-id="9ff6e-396">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-396">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-397">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-397">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-398">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="9ff6e-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-400">Указывает конкретные возможности логического устройства, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-400">Indicates the specific power-related capabilities of the logical device.</span></span>

<span data-ttu-id="9ff6e-401">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-401">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ff6e-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-402"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-403">Емкость, связанная с питанием, неизвестна.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-403">The power-related capacities are unknown.</span></span>

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="9ff6e-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-404"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-405">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-405">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9ff6e-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-406"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-407">Мощности, связанные с питанием, отключены.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-407">Power-related capacities have been disabled.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9ff6e-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-408"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-409">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-409">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="9ff6e-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-410"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-411">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-411">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="9ff6e-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-412"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-413">Поддерживается метод **SetPowerState** .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-413">The **SetPowerState** method is supported.</span></span> <span data-ttu-id="9ff6e-414">Этот метод находится в родительском классе [**класса \_ CIM**](cim-logicaldevice.md) и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-414">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="9ff6e-415">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-415">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="9ff6e-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-416"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-417">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания").</span><span class="sxs-lookup"><span data-stu-id="9ff6e-417">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle").</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="9ff6e-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-418"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="9ff6e-419">Метод **SetPowerState** может быть вызван с параметром *PowerState* , установленным в значение 5 ("цикл электропитания"), и параметром *времени* , установленным на определенную дату и время (или интервал) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-419">The **SetPowerState** method can be invoked with the *PowerState* parameter set to 5 ("Power Cycle") and the *Time* parameter set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-420">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-420">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-421">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-421">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-422">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-422">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-423">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-423">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="9ff6e-424">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-424">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9ff6e-425">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-425">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="9ff6e-426">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="9ff6e-426">For more information, see the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="9ff6e-427">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-428">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-428">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-429">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-431">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-431">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-432">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-432">String that indicates the current status of the object.</span></span> <span data-ttu-id="9ff6e-433">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-433">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9ff6e-434">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="9ff6e-434">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9ff6e-435">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-435">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9ff6e-436">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="9ff6e-436">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9ff6e-437">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-437">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9ff6e-438">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-438">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9ff6e-439">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9ff6e-440">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="9ff6e-440">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9ff6e-441">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-441">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9ff6e-442">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-442">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9ff6e-443">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-443">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ff6e-444">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-444">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9ff6e-445">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-445">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9ff6e-446">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-446">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9ff6e-447">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-447">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9ff6e-448">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-448">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9ff6e-449">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-449">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9ff6e-450">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-450">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9ff6e-451">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-451">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9ff6e-452">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-452">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-453">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-453">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-454">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-454">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-455">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-455">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-456">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="9ff6e-456">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-457">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-457">State of the logical device.</span></span> <span data-ttu-id="9ff6e-458">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="9ff6e-458">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="9ff6e-459">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-459">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="9ff6e-460">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-460">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9ff6e-461">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-461">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9ff6e-462">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-462">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9ff6e-463">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-463">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="9ff6e-464">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-464">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9ff6e-465">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-465">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-466">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-467">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-467">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-468">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-468">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-469">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-469">The scoping system's creation class name.</span></span>

<span data-ttu-id="9ff6e-470">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-470">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="9ff6e-471">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-471">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ff6e-472">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-473">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ff6e-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ff6e-474">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9ff6e-474">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9ff6e-475">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-475">The scoping system's name.</span></span>

<span data-ttu-id="9ff6e-476">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-476">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ff6e-477">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ff6e-477">Remarks</span></span>

<span data-ttu-id="9ff6e-478">Класс **CIM \_ кдромдриве** является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-478">The **CIM\_CDROMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="9ff6e-479">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-479">WMI does not implement this class.</span></span> <span data-ttu-id="9ff6e-480">Дополнительные сведения о классах, производных от **CIM \_ кдромдриве**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9ff6e-480">For more information about classes derived from **CIM\_CDROMDrive**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9ff6e-481">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-481">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9ff6e-482">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="9ff6e-482">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ff6e-483">Требования</span><span class="sxs-lookup"><span data-stu-id="9ff6e-483">Requirements</span></span>



| <span data-ttu-id="9ff6e-484">Требование</span><span class="sxs-lookup"><span data-stu-id="9ff6e-484">Requirement</span></span> | <span data-ttu-id="9ff6e-485">Значение</span><span class="sxs-lookup"><span data-stu-id="9ff6e-485">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff6e-486">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ff6e-486">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff6e-487">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ff6e-487">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ff6e-488">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ff6e-488">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff6e-489">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ff6e-489">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ff6e-490">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ff6e-490">Namespace</span></span><br/>                | <span data-ttu-id="9ff6e-491">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="9ff6e-491">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9ff6e-492">MOF</span><span class="sxs-lookup"><span data-stu-id="9ff6e-492">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ff6e-493"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ff6e-493"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ff6e-494">DLL</span><span class="sxs-lookup"><span data-stu-id="9ff6e-494">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ff6e-495"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ff6e-495"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ff6e-496">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ff6e-496">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff6e-497">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="9ff6e-497">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

