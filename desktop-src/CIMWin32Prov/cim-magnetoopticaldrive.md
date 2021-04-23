---
description: Класс CIM \_ магнетуптикалдриве представляет возможности и управление дисководом для магнитооптических дисков, подтипом устройства доступа к носителю.
ms.assetid: 82a4604d-3bef-4378-812b-550849e30b8c
ms.tgt_platform: multiple
title: Класс CIM_MagnetoOpticalDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MagnetoOpticalDrive
- CIM_MagnetoOpticalDrive.Availability
- CIM_MagnetoOpticalDrive.Capabilities
- CIM_MagnetoOpticalDrive.CapabilityDescriptions
- CIM_MagnetoOpticalDrive.Caption
- CIM_MagnetoOpticalDrive.CompressionMethod
- CIM_MagnetoOpticalDrive.ConfigManagerErrorCode
- CIM_MagnetoOpticalDrive.ConfigManagerUserConfig
- CIM_MagnetoOpticalDrive.CreationClassName
- CIM_MagnetoOpticalDrive.DefaultBlockSize
- CIM_MagnetoOpticalDrive.Description
- CIM_MagnetoOpticalDrive.DeviceID
- CIM_MagnetoOpticalDrive.ErrorCleared
- CIM_MagnetoOpticalDrive.ErrorDescription
- CIM_MagnetoOpticalDrive.ErrorMethodology
- CIM_MagnetoOpticalDrive.InstallDate
- CIM_MagnetoOpticalDrive.LastErrorCode
- CIM_MagnetoOpticalDrive.MaxBlockSize
- CIM_MagnetoOpticalDrive.MaxMediaSize
- CIM_MagnetoOpticalDrive.MinBlockSize
- CIM_MagnetoOpticalDrive.Name
- CIM_MagnetoOpticalDrive.NeedsCleaning
- CIM_MagnetoOpticalDrive.NumberOfMediaSupported
- CIM_MagnetoOpticalDrive.PNPDeviceID
- CIM_MagnetoOpticalDrive.PowerManagementCapabilities
- CIM_MagnetoOpticalDrive.PowerManagementSupported
- CIM_MagnetoOpticalDrive.Status
- CIM_MagnetoOpticalDrive.StatusInfo
- CIM_MagnetoOpticalDrive.SystemCreationClassName
- CIM_MagnetoOpticalDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: abc5acdf25a2920fa53c6315109264180b6e7c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496278"
---
# <a name="cim_magnetoopticaldrive-class"></a><span data-ttu-id="b83d0-103">\_Класс CIM магнетуптикалдриве</span><span class="sxs-lookup"><span data-stu-id="b83d0-103">CIM\_MagnetoOpticalDrive class</span></span>

<span data-ttu-id="b83d0-104">Класс **CIM \_ магнетуптикалдриве** представляет возможности и управление дисководом для магнитооптических дисков, подтипом устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="b83d0-104">The **CIM\_MagnetoOpticalDrive** class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b83d0-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b83d0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b83d0-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b83d0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b83d0-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b83d0-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b83d0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b83d0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b83d0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{F62037D8-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_MagnetoOpticalDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="b83d0-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b83d0-110">Members</span></span>

<span data-ttu-id="b83d0-111">Класс **CIM \_ магнетуптикалдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b83d0-111">The **CIM\_MagnetoOpticalDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b83d0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b83d0-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b83d0-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b83d0-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b83d0-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b83d0-114">Methods</span></span>

<span data-ttu-id="b83d0-115">Класс **CIM \_ магнетуптикалдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b83d0-115">The **CIM\_MagnetoOpticalDrive** class has these methods.</span></span>



| <span data-ttu-id="b83d0-116">Метод</span><span class="sxs-lookup"><span data-stu-id="b83d0-116">Method</span></span>                                                                         | <span data-ttu-id="b83d0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b83d0-117">Description</span></span>                                                                                                                              |
|:-------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b83d0-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b83d0-118">**Reset**</span></span>](reset-method-in-class-cim-magnetoopticaldrive.md)                 | <span data-ttu-id="b83d0-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b83d0-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b83d0-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b83d0-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b83d0-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-magnetoopticaldrive.md) | <span data-ttu-id="b83d0-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="b83d0-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b83d0-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b83d0-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b83d0-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="b83d0-124">Properties</span></span>

<span data-ttu-id="b83d0-125">Класс **CIM \_ магнетуптикалдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-125">The **CIM\_MagnetoOpticalDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b83d0-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b83d0-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b83d0-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b83d0-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-130">Availability and status of the device.</span></span>

<span data-ttu-id="b83d0-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b83d0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b83d0-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b83d0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b83d0-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b83d0-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b83d0-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b83d0-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b83d0-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b83d0-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b83d0-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b83d0-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b83d0-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b83d0-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b83d0-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b83d0-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b83d0-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b83d0-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b83d0-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b83d0-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b83d0-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b83d0-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b83d0-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b83d0-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b83d0-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b83d0-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b83d0-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-145">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b83d0-145">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b83d0-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b83d0-146"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-147">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b83d0-147">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b83d0-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b83d0-148"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-149">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b83d0-149">The device is not functioning but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b83d0-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b83d0-150"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b83d0-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b83d0-151"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-152">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b83d0-152">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b83d0-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b83d0-153"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-154">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b83d0-154">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b83d0-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b83d0-155"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-156">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b83d0-156">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b83d0-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b83d0-157"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-158">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b83d0-158">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b83d0-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b83d0-159"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-160">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b83d0-160">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-161">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="b83d0-161">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-162">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b83d0-162">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-164">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="b83d0-164">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-165">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="b83d0-165">Capabilities of the media access device.</span></span>

<span data-ttu-id="b83d0-166">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-166">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b83d0-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b83d0-167"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-168">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b83d0-168">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b83d0-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b83d0-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-170">Другое</span><span class="sxs-lookup"><span data-stu-id="b83d0-170">Other.</span></span>

</dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="b83d0-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="b83d0-171"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-172">Последовательный доступ.</span><span class="sxs-lookup"><span data-stu-id="b83d0-172">Sequential access.</span></span>

</dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="b83d0-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="b83d0-173"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-174">Произвольный доступ.</span><span class="sxs-lookup"><span data-stu-id="b83d0-174">Random access.</span></span>

</dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="b83d0-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="b83d0-175"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-176">Запись.</span><span class="sxs-lookup"><span data-stu-id="b83d0-176">Writing.</span></span>

</dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="b83d0-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="b83d0-177"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-178">Шифрование.</span><span class="sxs-lookup"><span data-stu-id="b83d0-178">Encryption.</span></span>

</dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="b83d0-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="b83d0-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-180">Сжатие.</span><span class="sxs-lookup"><span data-stu-id="b83d0-180">Compression.</span></span>

</dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="b83d0-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="b83d0-181"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-182">Съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="b83d0-182">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="b83d0-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="b83d0-183"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-184">Очистка вручную.</span><span class="sxs-lookup"><span data-stu-id="b83d0-184">Manual cleaning.</span></span>

</dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="b83d0-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="b83d0-185"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-186">Автоматическая очистка.</span><span class="sxs-lookup"><span data-stu-id="b83d0-186">Automatic cleaning.</span></span>

</dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="b83d0-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="b83d0-187"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-188">ИНТЕЛЛЕКТУАЛЬНое уведомление.</span><span class="sxs-lookup"><span data-stu-id="b83d0-188">SMART notification.</span></span>

</dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="b83d0-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="b83d0-189"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-190">Различает устройство, которое может получить доступ к обеим сторонам двусторонних носителей с устройства, которое считывает только одну сторону и требует включения носителя.</span><span class="sxs-lookup"><span data-stu-id="b83d0-190">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="b83d0-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="b83d0-191"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-192">Указывает, что носитель не обязательно должен быть явно извлечен с устройства перед обращением к элементу выбора.</span><span class="sxs-lookup"><span data-stu-id="b83d0-192">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-193">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="b83d0-193">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-194">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b83d0-194">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-196">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="b83d0-196">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-197">Массив строк произвольной формы, который содержит подробные пояснения для доступа к функциям устройств, указанным в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b83d0-197">Array of free-form strings that provides detailed explanations for access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="b83d0-198">Каждая запись массива связана с записью в массиве **capabilities** , расположенной по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="b83d0-198">Each array entry is related to the entry in the **Capabilities** array, located at the same index.</span></span>

 

<span data-ttu-id="b83d0-199">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-199">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-200">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b83d0-200">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-201">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-203">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b83d0-203">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-204">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b83d0-204">Short textual description of the object.</span></span>

<span data-ttu-id="b83d0-205">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-205">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-206">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="b83d0-206">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-209">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="b83d0-209">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b83d0-210">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="b83d0-210">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="b83d0-211">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="b83d0-211">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="b83d0-212">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="b83d0-212">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="b83d0-213">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-213">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="b83d0-214">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b83d0-214">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-215">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="b83d0-215">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="b83d0-216">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="b83d0-216">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-217">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="b83d0-217">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="b83d0-218">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="b83d0-218">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-219">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="b83d0-219">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-220">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b83d0-220">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-221">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b83d0-221">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-222">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-223">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b83d0-223">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-224">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b83d0-224">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b83d0-225">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-225">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b83d0-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-226"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b83d0-227"> (0)</span><span class="sxs-lookup"><span data-stu-id="b83d0-227">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-228">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b83d0-228">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b83d0-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-229"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b83d0-230">(1)</span><span class="sxs-lookup"><span data-stu-id="b83d0-230">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-231">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b83d0-231">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b83d0-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-232"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b83d0-233">(2)</span><span class="sxs-lookup"><span data-stu-id="b83d0-233">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b83d0-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-234"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b83d0-235">(3)</span><span class="sxs-lookup"><span data-stu-id="b83d0-235">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-236">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b83d0-236">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b83d0-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-237"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b83d0-238">(4)</span><span class="sxs-lookup"><span data-stu-id="b83d0-238">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-239">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b83d0-239">Device is not working properly.</span></span> <span data-ttu-id="b83d0-240">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b83d0-240">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b83d0-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-241"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b83d0-242">(5)</span><span class="sxs-lookup"><span data-stu-id="b83d0-242">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-243">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b83d0-243">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b83d0-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-244"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b83d0-245"> (6)</span><span class="sxs-lookup"><span data-stu-id="b83d0-245">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-246">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b83d0-246">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b83d0-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-247"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b83d0-248">(7)</span><span class="sxs-lookup"><span data-stu-id="b83d0-248">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b83d0-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-249"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b83d0-250">(8)</span><span class="sxs-lookup"><span data-stu-id="b83d0-250">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-251">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-251">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b83d0-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-252"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b83d0-253">(9)</span><span class="sxs-lookup"><span data-stu-id="b83d0-253">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-254">Устройство работает неправильно; встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-254">Device is not working properly; the controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b83d0-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-255"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b83d0-256">(10)</span><span class="sxs-lookup"><span data-stu-id="b83d0-256">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-257">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b83d0-257">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b83d0-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-258"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b83d0-259">(11)</span><span class="sxs-lookup"><span data-stu-id="b83d0-259">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-260">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-260">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b83d0-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-261"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b83d0-262">(12)</span><span class="sxs-lookup"><span data-stu-id="b83d0-262">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-263">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b83d0-263">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b83d0-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-264"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b83d0-265">(13)</span><span class="sxs-lookup"><span data-stu-id="b83d0-265">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-266">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-266">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b83d0-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-267"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b83d0-268">(14)</span><span class="sxs-lookup"><span data-stu-id="b83d0-268">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-269">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b83d0-269">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b83d0-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-270"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b83d0-271">(15)</span><span class="sxs-lookup"><span data-stu-id="b83d0-271">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-272">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b83d0-272">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b83d0-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-273"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b83d0-274">(16)</span><span class="sxs-lookup"><span data-stu-id="b83d0-274">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-275">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b83d0-275">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b83d0-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-276"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b83d0-277">(17)</span><span class="sxs-lookup"><span data-stu-id="b83d0-277">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-278">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b83d0-278">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b83d0-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-279"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b83d0-280">(18)</span><span class="sxs-lookup"><span data-stu-id="b83d0-280">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-281">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b83d0-281">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b83d0-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-282"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b83d0-283">(19)</span><span class="sxs-lookup"><span data-stu-id="b83d0-283">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b83d0-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-284"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b83d0-285">(20)</span><span class="sxs-lookup"><span data-stu-id="b83d0-285">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-286">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b83d0-286">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b83d0-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b83d0-288">(21)</span><span class="sxs-lookup"><span data-stu-id="b83d0-288">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-289">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b83d0-289">System failure.</span></span> <span data-ttu-id="b83d0-290">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b83d0-290">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b83d0-291">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b83d0-291">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b83d0-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-292"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b83d0-293">(22)</span><span class="sxs-lookup"><span data-stu-id="b83d0-293">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-294">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b83d0-294">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b83d0-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-295"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b83d0-296">(23)</span><span class="sxs-lookup"><span data-stu-id="b83d0-296">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-297">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b83d0-297">System failure.</span></span> <span data-ttu-id="b83d0-298">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b83d0-298">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b83d0-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-299"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b83d0-300">(24)</span><span class="sxs-lookup"><span data-stu-id="b83d0-300">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-301">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b83d0-301">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b83d0-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-302"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b83d0-303">(25)</span><span class="sxs-lookup"><span data-stu-id="b83d0-303">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-304">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b83d0-304">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b83d0-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-305"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b83d0-306">(26)</span><span class="sxs-lookup"><span data-stu-id="b83d0-306">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-307">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b83d0-307">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b83d0-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-308"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b83d0-309">(27)</span><span class="sxs-lookup"><span data-stu-id="b83d0-309">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-310">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b83d0-310">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b83d0-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-311"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b83d0-312">(28)</span><span class="sxs-lookup"><span data-stu-id="b83d0-312">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-313">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b83d0-313">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b83d0-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-314"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b83d0-315">(29)</span><span class="sxs-lookup"><span data-stu-id="b83d0-315">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-316">Устройство отключено; встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b83d0-316">Device is disabled; the device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b83d0-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-317"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b83d0-318">(30)</span><span class="sxs-lookup"><span data-stu-id="b83d0-318">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-319">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b83d0-319">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b83d0-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b83d0-320"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b83d0-321">1-31</span><span class="sxs-lookup"><span data-stu-id="b83d0-321">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-322">Устройство работает неправильно; Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b83d0-322">Device is not working properly; Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-323">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b83d0-323">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-324">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b83d0-324">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-326">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b83d0-326">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-327">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b83d0-327">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b83d0-328">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-328">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-329">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b83d0-329">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-330">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-331">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-332">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b83d0-332">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-333">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b83d0-333">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b83d0-334">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b83d0-334">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b83d0-335">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-335">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-336">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="b83d0-336">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-337">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b83d0-337">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-339">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b83d0-339">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-340">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="b83d0-340">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="b83d0-341">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-341">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b83d0-342">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b83d0-342">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-343">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b83d0-343">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-346">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b83d0-346">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-347">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b83d0-347">Textual description of the object.</span></span>

<span data-ttu-id="b83d0-348">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-348">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-349">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b83d0-349">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-350">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-352">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b83d0-352">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-353">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-353">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b83d0-354">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-354">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-355">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b83d0-355">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-356">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b83d0-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-357">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-357">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-358">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b83d0-358">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b83d0-359">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-359">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-360">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b83d0-360">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-362">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-363">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b83d0-363">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b83d0-364">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-364">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-365">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="b83d0-365">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-366">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-366">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-367">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-367">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-368">Произвольная строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b83d0-368">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="b83d0-369">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-369">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-370">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b83d0-370">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-371">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b83d0-371">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-372">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-373">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b83d0-373">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-374">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b83d0-374">Date and time the object was installed.</span></span> <span data-ttu-id="b83d0-375">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b83d0-375">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b83d0-376">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-376">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-377">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b83d0-377">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-378">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b83d0-378">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-379">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-379">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-380">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b83d0-380">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b83d0-381">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-381">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-382">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="b83d0-382">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-383">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b83d0-383">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-384">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-385">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b83d0-385">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-386">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="b83d0-386">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b83d0-387">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-387">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b83d0-388">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b83d0-388">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-389">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="b83d0-389">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-390">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b83d0-390">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-391">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-391">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-392">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="b83d0-392">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-393">Максимальный размер носителя, поддерживаемого устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="b83d0-393">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="b83d0-394">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="b83d0-394">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="b83d0-395">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-395">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b83d0-396">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b83d0-396">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-397">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="b83d0-397">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-398">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b83d0-398">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-399">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-399">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-400">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b83d0-400">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-401">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="b83d0-401">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b83d0-402">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-402">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b83d0-403">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b83d0-403">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-404">**Name**</span><span class="sxs-lookup"><span data-stu-id="b83d0-404">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-405">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-405">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-406">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-406">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-407">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b83d0-407">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-408">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b83d0-408">Label by which the object is known.</span></span> <span data-ttu-id="b83d0-409">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b83d0-409">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b83d0-410">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-410">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-411">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="b83d0-411">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-412">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b83d0-412">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-414">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="b83d0-414">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="b83d0-415">Возможность ручной или автоматической очистки указывается в свойстве массива **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b83d0-415">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="b83d0-416">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-416">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-417">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="b83d0-417">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-418">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b83d0-418">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-419">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-419">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-420">Если устройство доступа к носителю поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может быть поддерживается или вставлено.</span><span class="sxs-lookup"><span data-stu-id="b83d0-420">If the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="b83d0-421">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-421">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-422">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b83d0-422">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-423">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-423">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-424">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-424">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-425">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b83d0-425">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-426">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-426">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b83d0-427">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-427">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b83d0-428">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b83d0-428">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-429">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b83d0-429">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-430">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b83d0-430">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-432">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b83d0-432">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b83d0-433">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-433">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b83d0-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b83d0-434"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b83d0-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b83d0-435"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-436">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="b83d0-436">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b83d0-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b83d0-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b83d0-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b83d0-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-439">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b83d0-439">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b83d0-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b83d0-440"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-441">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b83d0-441">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b83d0-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b83d0-442"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-443">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b83d0-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b83d0-444">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b83d0-444">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b83d0-445">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b83d0-445">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b83d0-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b83d0-446"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-447">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b83d0-447">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b83d0-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b83d0-448"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b83d0-449">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b83d0-449">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-450">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b83d0-450">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-451">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b83d0-451">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-452">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-453">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b83d0-453">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b83d0-454">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b83d0-454">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b83d0-455">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b83d0-455">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b83d0-456">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b83d0-456">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b83d0-457">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-457">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-458">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b83d0-458">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-459">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-459">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-460">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-460">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-461">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b83d0-461">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-462">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b83d0-462">Current status of the object.</span></span>

<span data-ttu-id="b83d0-463">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-463">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b83d0-464">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b83d0-464">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b83d0-465">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b83d0-465">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b83d0-466">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b83d0-466">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b83d0-467">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b83d0-467">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b83d0-468">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b83d0-468">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b83d0-469">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b83d0-469">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b83d0-470">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b83d0-470">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b83d0-471">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b83d0-471">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b83d0-472">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b83d0-472">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b83d0-473">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b83d0-473">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b83d0-474">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b83d0-474">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b83d0-475">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b83d0-475">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b83d0-476">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b83d0-476">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-477">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b83d0-477">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-478">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b83d0-478">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-479">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-479">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-480">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b83d0-480">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-481">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b83d0-481">State of the logical device.</span></span> <span data-ttu-id="b83d0-482">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b83d0-482">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b83d0-483">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-483">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b83d0-484">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b83d0-484">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b83d0-485">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b83d0-485">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b83d0-486">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b83d0-486">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b83d0-487">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b83d0-487">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b83d0-488">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b83d0-488">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b83d0-489">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b83d0-489">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-490">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-491">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-492">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b83d0-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-493">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b83d0-493">Scoping system's creation class name.</span></span>

<span data-ttu-id="b83d0-494">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b83d0-495">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b83d0-495">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b83d0-496">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b83d0-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b83d0-497">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b83d0-498">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b83d0-498">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b83d0-499">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b83d0-499">Scoping system's name.</span></span>

<span data-ttu-id="b83d0-500">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b83d0-500">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b83d0-501">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83d0-501">Remarks</span></span>

<span data-ttu-id="b83d0-502">Класс **CIM \_ магнетуптикалдриве** является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b83d0-502">The **CIM\_MagnetoOpticalDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b83d0-503">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b83d0-503">WMI does not implement this class.</span></span>

<span data-ttu-id="b83d0-504">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b83d0-504">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b83d0-505">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b83d0-505">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b83d0-506">Требования</span><span class="sxs-lookup"><span data-stu-id="b83d0-506">Requirements</span></span>



| <span data-ttu-id="b83d0-507">Требование</span><span class="sxs-lookup"><span data-stu-id="b83d0-507">Requirement</span></span> | <span data-ttu-id="b83d0-508">Значение</span><span class="sxs-lookup"><span data-stu-id="b83d0-508">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b83d0-509">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b83d0-509">Minimum supported client</span></span><br/> | <span data-ttu-id="b83d0-510">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b83d0-510">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b83d0-511">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b83d0-511">Minimum supported server</span></span><br/> | <span data-ttu-id="b83d0-512">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b83d0-512">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b83d0-513">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b83d0-513">Namespace</span></span><br/>                | <span data-ttu-id="b83d0-514">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b83d0-514">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b83d0-515">MOF</span><span class="sxs-lookup"><span data-stu-id="b83d0-515">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b83d0-516"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b83d0-516"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b83d0-517">DLL</span><span class="sxs-lookup"><span data-stu-id="b83d0-517">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b83d0-518"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b83d0-518"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b83d0-519">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b83d0-519">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b83d0-520">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="b83d0-520">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

