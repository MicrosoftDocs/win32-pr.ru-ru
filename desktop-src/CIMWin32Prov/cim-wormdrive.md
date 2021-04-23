---
description: Класс CIM \_ вормдриве представляет возможности и управление накопителем-червем, подтипом устройства доступа к носителю.
ms.assetid: df77084a-01f2-4cca-b395-d74ee64ef526
ms.tgt_platform: multiple
title: Класс CIM_WORMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WORMDrive
- CIM_WORMDrive.Availability
- CIM_WORMDrive.Capabilities
- CIM_WORMDrive.CapabilityDescriptions
- CIM_WORMDrive.Caption
- CIM_WORMDrive.CompressionMethod
- CIM_WORMDrive.ConfigManagerErrorCode
- CIM_WORMDrive.ConfigManagerUserConfig
- CIM_WORMDrive.CreationClassName
- CIM_WORMDrive.DefaultBlockSize
- CIM_WORMDrive.Description
- CIM_WORMDrive.DeviceID
- CIM_WORMDrive.ErrorCleared
- CIM_WORMDrive.ErrorDescription
- CIM_WORMDrive.ErrorMethodology
- CIM_WORMDrive.InstallDate
- CIM_WORMDrive.LastErrorCode
- CIM_WORMDrive.MaxBlockSize
- CIM_WORMDrive.MaxMediaSize
- CIM_WORMDrive.MinBlockSize
- CIM_WORMDrive.Name
- CIM_WORMDrive.NeedsCleaning
- CIM_WORMDrive.NumberOfMediaSupported
- CIM_WORMDrive.PNPDeviceID
- CIM_WORMDrive.PowerManagementCapabilities
- CIM_WORMDrive.PowerManagementSupported
- CIM_WORMDrive.Status
- CIM_WORMDrive.StatusInfo
- CIM_WORMDrive.SystemCreationClassName
- CIM_WORMDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 08133d1abdcb6fc401ee4ad730d82ef97fb30200
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141067"
---
# <a name="cim_wormdrive-class"></a><span data-ttu-id="b06bf-103">\_Класс CIM вормдриве</span><span class="sxs-lookup"><span data-stu-id="b06bf-103">CIM\_WORMDrive class</span></span>

<span data-ttu-id="b06bf-104">Класс **CIM \_ вормдриве** представляет возможности и управление НАКОПИТЕЛем-червем, подтипом устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="b06bf-104">The **CIM\_WORMDrive** class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b06bf-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b06bf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b06bf-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b06bf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b06bf-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b06bf-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b06bf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b06bf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b06bf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FFB58B9A-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_WORMDrive : CIM_MediaAccessDevice
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

## <a name="members"></a><span data-ttu-id="b06bf-110">Члены</span><span class="sxs-lookup"><span data-stu-id="b06bf-110">Members</span></span>

<span data-ttu-id="b06bf-111">Класс **CIM \_ вормдриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b06bf-111">The **CIM\_WORMDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="b06bf-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b06bf-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b06bf-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b06bf-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b06bf-114">Методы</span><span class="sxs-lookup"><span data-stu-id="b06bf-114">Methods</span></span>

<span data-ttu-id="b06bf-115">Класс **CIM \_ вормдриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b06bf-115">The **CIM\_WORMDrive** class has these methods.</span></span>



| <span data-ttu-id="b06bf-116">Метод</span><span class="sxs-lookup"><span data-stu-id="b06bf-116">Method</span></span>                                                               | <span data-ttu-id="b06bf-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b06bf-117">Description</span></span>                                                                                                                              |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b06bf-118">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b06bf-118">**Reset**</span></span>](reset-method-in-class-cim-wormdrive.md)                 | <span data-ttu-id="b06bf-119">Запрашивает сброс логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-119">Requests a reset of the logical device.</span></span> <span data-ttu-id="b06bf-120">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b06bf-120">Not implemented by WMI.</span></span><br/>                                                               |
| [<span data-ttu-id="b06bf-121">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="b06bf-121">**SetPowerState**</span></span>](setpowerstate-method-in-class-cim-wormdrive.md) | <span data-ttu-id="b06bf-122">Определяет требуемое состояние электропитания для логического устройства, а также когда устройство должно быть переведено в это состояние.</span><span class="sxs-lookup"><span data-stu-id="b06bf-122">Defines the desired power state for a logical device and when a device should be put into that state.</span></span> <span data-ttu-id="b06bf-123">Не реализовано инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="b06bf-123">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b06bf-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="b06bf-124">Properties</span></span>

<span data-ttu-id="b06bf-125">Класс **CIM \_ вормдриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-125">The **CIM\_WORMDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b06bf-126">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="b06bf-126">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b06bf-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="b06bf-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-130">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-130">Availability and status of the device.</span></span>

<span data-ttu-id="b06bf-131">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-131">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b06bf-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b06bf-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06bf-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b06bf-133"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="b06bf-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="b06bf-134"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-135">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="b06bf-135">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="b06bf-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="b06bf-136"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="b06bf-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="b06bf-137"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b06bf-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="b06bf-138"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="b06bf-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="b06bf-139"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="b06bf-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="b06bf-140"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="b06bf-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="b06bf-141"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b06bf-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="b06bf-142"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="b06bf-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="b06bf-143"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="b06bf-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="b06bf-144"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="b06bf-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="b06bf-145"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-146">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="b06bf-146">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="b06bf-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="b06bf-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-148">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="b06bf-148">The device is in a power save state but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="b06bf-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="b06bf-149"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-150">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="b06bf-150">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="b06bf-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="b06bf-151"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="b06bf-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="b06bf-152"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-153">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b06bf-153">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="b06bf-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="b06bf-154"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-155">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="b06bf-155">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="b06bf-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="b06bf-156"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-157">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="b06bf-157">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="b06bf-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="b06bf-158"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-159">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="b06bf-159">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="b06bf-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="b06bf-160"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-161">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="b06bf-161">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-162">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="b06bf-162">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-163">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b06bf-163">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-165">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="b06bf-165">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-166">Возможности устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="b06bf-166">Capabilities of the media access device.</span></span> <span data-ttu-id="b06bf-167">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-167">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06bf-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b06bf-168"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b06bf-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b06bf-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="b06bf-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="b06bf-170"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="b06bf-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="b06bf-171"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="b06bf-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="b06bf-172"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="b06bf-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="b06bf-173"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="b06bf-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="b06bf-174"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="b06bf-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="b06bf-175"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-176">Съемный носитель.</span><span class="sxs-lookup"><span data-stu-id="b06bf-176">Removable media.</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="b06bf-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="b06bf-177"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="b06bf-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="b06bf-178"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="b06bf-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="b06bf-179"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="b06bf-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="b06bf-180"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-181">Различает устройство, которое может получить доступ к обеим сторонам двусторонних носителей с устройства, которое считывает только одну сторону и требует включения носителя.</span><span class="sxs-lookup"><span data-stu-id="b06bf-181">Distinguishes a device that can access both sides of dual-sided media from a device that reads only a single side and requires the media to be turned over.</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="b06bf-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="b06bf-182"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-183">Указывает, что носитель не обязательно должен быть явно извлечен с устройства перед обращением к элементу выбора.</span><span class="sxs-lookup"><span data-stu-id="b06bf-183">Indicates that the media does not have to be explicitly ejected from the device before being accessed by a picker element.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-184">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="b06bf-184">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-185">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="b06bf-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-187">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="b06bf-187">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-188">Строки свободной формы, содержащие подробные описания функций доступа к устройствам, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b06bf-188">Free-form strings that provide detailed descriptions for the access device features indicated in the **Capabilities** array.</span></span>

> [!Note]  
> <span data-ttu-id="b06bf-189">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="b06bf-189">Each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

 

<span data-ttu-id="b06bf-190">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-190">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-191">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="b06bf-191">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-192">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-193">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-194">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b06bf-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-195">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b06bf-195">Short textual description of the object.</span></span>

<span data-ttu-id="b06bf-196">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-196">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-197">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="b06bf-197">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-200">Произвольная строка, указывающая алгоритм или инструмент, используемый для сжатия логического файла.</span><span class="sxs-lookup"><span data-stu-id="b06bf-200">Free-form string that indicates the algorithm or tool used to compress the logical file.</span></span> <span data-ttu-id="b06bf-201">Если схема сжатия неизвестна или не описана, используйте "Unknown".</span><span class="sxs-lookup"><span data-stu-id="b06bf-201">If the compression scheme is unknown or not described, use "Unknown".</span></span> <span data-ttu-id="b06bf-202">Если логический файл сжат, но схема сжатия неизвестна или не описана, используйте "сжатый".</span><span class="sxs-lookup"><span data-stu-id="b06bf-202">If the logical file is compressed, but the compression scheme is unknown or not described, use "Compressed".</span></span> <span data-ttu-id="b06bf-203">Если логический файл не сжат, используйте параметр NOT сжатый.</span><span class="sxs-lookup"><span data-stu-id="b06bf-203">If the logical file is not compressed, use "Not Compressed".</span></span>

<span data-ttu-id="b06bf-204">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-204">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="b06bf-205">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b06bf-205">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-206">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="b06bf-206">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="b06bf-207">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="b06bf-207">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-208">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="b06bf-208">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="b06bf-209">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="b06bf-209">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-210">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="b06bf-210">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-211">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b06bf-211">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-212">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b06bf-212">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-214">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b06bf-214">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-215">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="b06bf-215">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="b06bf-216">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-216">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="b06bf-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-217"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="b06bf-218"> (0)</span><span class="sxs-lookup"><span data-stu-id="b06bf-218">(0)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-219">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="b06bf-219">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="b06bf-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-220"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="b06bf-221">(1)</span><span class="sxs-lookup"><span data-stu-id="b06bf-221">(1)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-222">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="b06bf-222">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b06bf-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-223"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="b06bf-224">(2)</span><span class="sxs-lookup"><span data-stu-id="b06bf-224">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="b06bf-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-225"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="b06bf-226">(3)</span><span class="sxs-lookup"><span data-stu-id="b06bf-226">(3)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-227">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b06bf-227">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b06bf-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-228"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="b06bf-229">(4)</span><span class="sxs-lookup"><span data-stu-id="b06bf-229">(4)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-230">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b06bf-230">Device is not working properly.</span></span> <span data-ttu-id="b06bf-231">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b06bf-231">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="b06bf-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-232"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="b06bf-233">(5)</span><span class="sxs-lookup"><span data-stu-id="b06bf-233">(5)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-234">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="b06bf-234">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="b06bf-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-235"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="b06bf-236"> (6)</span><span class="sxs-lookup"><span data-stu-id="b06bf-236">(6)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-237">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="b06bf-237">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="b06bf-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-238"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="b06bf-239">(7)</span><span class="sxs-lookup"><span data-stu-id="b06bf-239">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="b06bf-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-240"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="b06bf-241">(8)</span><span class="sxs-lookup"><span data-stu-id="b06bf-241">(8)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-242">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-242">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="b06bf-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-243"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="b06bf-244">(9)</span><span class="sxs-lookup"><span data-stu-id="b06bf-244">(9)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-245">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b06bf-245">Device is not working properly.</span></span> <span data-ttu-id="b06bf-246">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-246">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="b06bf-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-247"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="b06bf-248">(10)</span><span class="sxs-lookup"><span data-stu-id="b06bf-248">(10)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-249">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="b06bf-249">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="b06bf-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-250"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="b06bf-251">(11)</span><span class="sxs-lookup"><span data-stu-id="b06bf-251">(11)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-252">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-252">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="b06bf-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-253"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="b06bf-254">(12)</span><span class="sxs-lookup"><span data-stu-id="b06bf-254">(12)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-255">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="b06bf-255">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="b06bf-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-256"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="b06bf-257">(13)</span><span class="sxs-lookup"><span data-stu-id="b06bf-257">(13)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-258">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-258">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="b06bf-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-259"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="b06bf-260">(14)</span><span class="sxs-lookup"><span data-stu-id="b06bf-260">(14)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-261">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="b06bf-261">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="b06bf-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-262"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="b06bf-263">(15)</span><span class="sxs-lookup"><span data-stu-id="b06bf-263">(15)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-264">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="b06bf-264">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="b06bf-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-265"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="b06bf-266">(16)</span><span class="sxs-lookup"><span data-stu-id="b06bf-266">(16)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-267">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b06bf-267">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="b06bf-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-268"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="b06bf-269">(17)</span><span class="sxs-lookup"><span data-stu-id="b06bf-269">(17)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-270">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="b06bf-270">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b06bf-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-271"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="b06bf-272">(18)</span><span class="sxs-lookup"><span data-stu-id="b06bf-272">(18)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-273">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b06bf-273">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="b06bf-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-274"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="b06bf-275">(19)</span><span class="sxs-lookup"><span data-stu-id="b06bf-275">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="b06bf-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-276"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="b06bf-277">(20)</span><span class="sxs-lookup"><span data-stu-id="b06bf-277">(20)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-278">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="b06bf-278">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="b06bf-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-279"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="b06bf-280">(21)</span><span class="sxs-lookup"><span data-stu-id="b06bf-280">(21)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-281">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b06bf-281">System failure.</span></span> <span data-ttu-id="b06bf-282">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b06bf-282">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="b06bf-283">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="b06bf-283">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="b06bf-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-284"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="b06bf-285">(22)</span><span class="sxs-lookup"><span data-stu-id="b06bf-285">(22)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-286">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b06bf-286">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="b06bf-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-287"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="b06bf-288">(23)</span><span class="sxs-lookup"><span data-stu-id="b06bf-288">(23)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-289">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="b06bf-289">System failure.</span></span> <span data-ttu-id="b06bf-290">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="b06bf-290">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="b06bf-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-291"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="b06bf-292">(24)</span><span class="sxs-lookup"><span data-stu-id="b06bf-292">(24)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-293">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="b06bf-293">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b06bf-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-294"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b06bf-295">(25)</span><span class="sxs-lookup"><span data-stu-id="b06bf-295">(25)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-296">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b06bf-296">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="b06bf-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-297"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="b06bf-298">(26)</span><span class="sxs-lookup"><span data-stu-id="b06bf-298">(26)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-299">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="b06bf-299">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="b06bf-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-300"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="b06bf-301">(27)</span><span class="sxs-lookup"><span data-stu-id="b06bf-301">(27)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-302">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="b06bf-302">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="b06bf-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-303"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="b06bf-304">(28)</span><span class="sxs-lookup"><span data-stu-id="b06bf-304">(28)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-305">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="b06bf-305">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="b06bf-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-306"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="b06bf-307">(29)</span><span class="sxs-lookup"><span data-stu-id="b06bf-307">(29)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-308">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="b06bf-308">Device is disabled.</span></span> <span data-ttu-id="b06bf-309">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b06bf-309">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="b06bf-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-310"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="b06bf-311">(30)</span><span class="sxs-lookup"><span data-stu-id="b06bf-311">(30)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-312">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="b06bf-312">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="b06bf-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="b06bf-313"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="b06bf-314">1-31</span><span class="sxs-lookup"><span data-stu-id="b06bf-314">(31)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-315">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="b06bf-315">Device is not working properly.</span></span> <span data-ttu-id="b06bf-316">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="b06bf-316">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-317">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="b06bf-317">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-318">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b06bf-318">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-319">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-319">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-320">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b06bf-320">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-321">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="b06bf-321">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="b06bf-322">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-322">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-323">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b06bf-323">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-324">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-325">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-326">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06bf-326">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-327">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b06bf-327">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b06bf-328">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="b06bf-328">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="b06bf-329">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-329">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-330">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="b06bf-330">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-331">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b06bf-331">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-332">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-333">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b06bf-333">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-334">Размер блока по умолчанию для устройства (в байтах).</span><span class="sxs-lookup"><span data-stu-id="b06bf-334">Default block size, in bytes, for the device.</span></span>

<span data-ttu-id="b06bf-335">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-335">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b06bf-336">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b06bf-336">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-337">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b06bf-337">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-338">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-338">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-339">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-339">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-340">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="b06bf-340">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-341">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="b06bf-341">Textual description of the object.</span></span>

<span data-ttu-id="b06bf-342">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-343">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="b06bf-343">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-345">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-345">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-346">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06bf-346">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-347">Адрес или другие идентифицирующие сведения для уникального имени логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-347">Address or other identifying information to uniquely name the logical device.</span></span>

<span data-ttu-id="b06bf-348">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-348">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-349">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="b06bf-349">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-350">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b06bf-350">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-351">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-352">Если **значение — true**, сообщение об ошибке, переданное в свойстве **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="b06bf-352">If **TRUE**, the error reported in the **LastErrorCode** property is now cleared.</span></span>

<span data-ttu-id="b06bf-353">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-354">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="b06bf-354">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-356">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-357">Произвольная строка, которая предоставляет сведения об ошибке, записанной в свойстве **ластерроркоде** , и корректирующие действия, которые необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="b06bf-357">Free-form string that supplies information about the error recorded in the **LastErrorCode** property and corrective actions to perform.</span></span>

<span data-ttu-id="b06bf-358">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-359">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="b06bf-359">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-360">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-361">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-362">Произвольная строка, описывающая типы обнаружения ошибок и исправления, поддерживаемые устройством.</span><span class="sxs-lookup"><span data-stu-id="b06bf-362">Free-form string that describes the types of error detection and correction supported by the device.</span></span>

<span data-ttu-id="b06bf-363">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-363">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-364">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b06bf-364">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-365">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b06bf-365">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-366">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-367">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="b06bf-367">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-368">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="b06bf-368">Date and time the object was installed.</span></span> <span data-ttu-id="b06bf-369">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="b06bf-369">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="b06bf-370">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-370">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-371">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="b06bf-371">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-372">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b06bf-372">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-373">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-374">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="b06bf-374">Last error code reported by the logical device.</span></span>

<span data-ttu-id="b06bf-375">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-375">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-376">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="b06bf-376">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-377">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b06bf-377">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-378">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-379">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b06bf-379">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-380">Максимальный размер блока в байтах для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="b06bf-380">Maximum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b06bf-381">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-381">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b06bf-382">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b06bf-382">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-383">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="b06bf-383">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-384">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b06bf-384">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-386">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="b06bf-386">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-387">Максимальный размер носителя, поддерживаемого устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="b06bf-387">Maximum size, in kilobytes, of media supported by the device.</span></span> <span data-ttu-id="b06bf-388">Килобайты интерпретируется как число байтов, умноженное на 1000 (а не на число байтов, умноженное на 1024).</span><span class="sxs-lookup"><span data-stu-id="b06bf-388">Kilobytes are interpreted as the number of bytes multiplied by 1000 (not the number of bytes multiplied by 1024).</span></span>

<span data-ttu-id="b06bf-389">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b06bf-390">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b06bf-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-391">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="b06bf-391">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-392">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="b06bf-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-394">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="b06bf-394">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-395">Минимальный размер блока (в байтах) для носителя, доступного устройству.</span><span class="sxs-lookup"><span data-stu-id="b06bf-395">Minimum block size, in bytes, for media accessed by the device.</span></span>

<span data-ttu-id="b06bf-396">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b06bf-397">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="b06bf-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-398">**Name**</span><span class="sxs-lookup"><span data-stu-id="b06bf-398">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-399">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-401">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="b06bf-401">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-402">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="b06bf-402">Label by which the object is known.</span></span> <span data-ttu-id="b06bf-403">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="b06bf-403">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b06bf-404">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-405">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="b06bf-405">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-406">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b06bf-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-408">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="b06bf-408">If **TRUE**, the media access device needs cleaning.</span></span> <span data-ttu-id="b06bf-409">Возможность ручной или автоматической очистки указывается в свойстве массива **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="b06bf-409">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** array property.</span></span>

<span data-ttu-id="b06bf-410">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-410">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-411">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="b06bf-411">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-412">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b06bf-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-413">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-413">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-414">Если устройство доступа к носителю поддерживает несколько отдельных носителей, это свойство определяет максимальное число, которое может быть поддерживается или вставлено.</span><span class="sxs-lookup"><span data-stu-id="b06bf-414">When the media access device supports multiple individual media, this property defines the maximum number that can be supported or inserted.</span></span>

<span data-ttu-id="b06bf-415">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-415">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-416">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="b06bf-416">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-417">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-417">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-418">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-418">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-419">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="b06bf-419">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-420">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-420">Windows Plug and Play device identifier of the logical device.</span></span> <span data-ttu-id="b06bf-421">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-421">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="b06bf-422">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="b06bf-422">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-423">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="b06bf-423">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-424">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="b06bf-424">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-426">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="b06bf-426">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="b06bf-427">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-427">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06bf-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="b06bf-428"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="b06bf-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="b06bf-429"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-430">Для этого устройства не поддерживаются мощности, связанные с питанием.</span><span class="sxs-lookup"><span data-stu-id="b06bf-430">Power-related capacities are not supported for this device.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b06bf-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="b06bf-431"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b06bf-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b06bf-432"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-433">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="b06bf-433">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="b06bf-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="b06bf-434"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-435">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="b06bf-435">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="b06bf-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="b06bf-436"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-437">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="b06bf-437">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="b06bf-438">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="b06bf-438">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="b06bf-439">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="b06bf-439">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="b06bf-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="b06bf-440"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-441">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="b06bf-441">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="b06bf-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="b06bf-442"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="b06bf-443">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="b06bf-443">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-444">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="b06bf-444">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-445">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b06bf-445">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-447">Если **значение — true**, устройство может управляться питанием, то есть перевести в состояние энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="b06bf-447">If **TRUE**, the device can be power managed, that is, put into a power-save state.</span></span> <span data-ttu-id="b06bf-448">Если **false**, то целочисленное значение 1 ("не поддерживается") должно быть единственной записью в массиве **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b06bf-448">If **FALSE**, the integer value 1 ("Not Supported") should be the only entry in the **PowerManagementCapabilities** array.</span></span>

<span data-ttu-id="b06bf-449">Это свойство не указывает, включены ли функции управления питанием в настоящее время, или, если они включены, какие функции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b06bf-449">This property does not indicate whether power management features are currently enabled, or if enabled, which features are supported.</span></span> <span data-ttu-id="b06bf-450">Дополнительные сведения см. в разделе массив **поверманажементкапабилитиес** .</span><span class="sxs-lookup"><span data-stu-id="b06bf-450">For more information, see the **PowerManagementCapabilities** array.</span></span> <span data-ttu-id="b06bf-451">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-451">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-452">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="b06bf-452">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-453">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-453">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-455">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="b06bf-455">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-456">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="b06bf-456">Current status of the object.</span></span> <span data-ttu-id="b06bf-457">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-457">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b06bf-458">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="b06bf-458">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b06bf-459">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="b06bf-459">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b06bf-460">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="b06bf-460">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b06bf-461">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="b06bf-461">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06bf-462">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="b06bf-462">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b06bf-463">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="b06bf-463">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b06bf-464">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="b06bf-464">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b06bf-465">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="b06bf-465">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b06bf-466">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="b06bf-466">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b06bf-467">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="b06bf-467">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b06bf-468">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="b06bf-468">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b06bf-469">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="b06bf-469">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b06bf-470">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="b06bf-470">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-471">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="b06bf-471">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-472">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b06bf-472">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-473">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-473">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-474">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="b06bf-474">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-475">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="b06bf-475">State of the logical device.</span></span> <span data-ttu-id="b06bf-476">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="b06bf-476">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="b06bf-477">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-477">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b06bf-478">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="b06bf-478">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b06bf-479">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="b06bf-479">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b06bf-480">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="b06bf-480">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b06bf-481">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="b06bf-481">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="b06bf-482">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="b06bf-482">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b06bf-483">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="b06bf-483">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-484">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-485">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-485">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-486">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06bf-486">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-487">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="b06bf-487">Scoping system's creation class name.</span></span>

<span data-ttu-id="b06bf-488">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-488">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="b06bf-489">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="b06bf-489">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b06bf-490">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="b06bf-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-491">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b06bf-491">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b06bf-492">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b06bf-492">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b06bf-493">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="b06bf-493">Scoping system's name.</span></span>

<span data-ttu-id="b06bf-494">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="b06bf-494">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b06bf-495">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b06bf-495">Remarks</span></span>

<span data-ttu-id="b06bf-496">Класс **CIM \_ вормдриве** является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="b06bf-496">The **CIM\_WORMDrive** class is derived from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="b06bf-497">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b06bf-497">WMI does not implement this class.</span></span>

<span data-ttu-id="b06bf-498">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b06bf-498">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b06bf-499">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b06bf-499">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b06bf-500">Требования</span><span class="sxs-lookup"><span data-stu-id="b06bf-500">Requirements</span></span>



| <span data-ttu-id="b06bf-501">Требование</span><span class="sxs-lookup"><span data-stu-id="b06bf-501">Requirement</span></span> | <span data-ttu-id="b06bf-502">Значение</span><span class="sxs-lookup"><span data-stu-id="b06bf-502">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b06bf-503">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b06bf-503">Minimum supported client</span></span><br/> | <span data-ttu-id="b06bf-504">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b06bf-504">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b06bf-505">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b06bf-505">Minimum supported server</span></span><br/> | <span data-ttu-id="b06bf-506">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b06bf-506">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b06bf-507">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b06bf-507">Namespace</span></span><br/>                | <span data-ttu-id="b06bf-508">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b06bf-508">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b06bf-509">MOF</span><span class="sxs-lookup"><span data-stu-id="b06bf-509">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b06bf-510"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b06bf-510"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b06bf-511">DLL</span><span class="sxs-lookup"><span data-stu-id="b06bf-511">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b06bf-512"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b06bf-512"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b06bf-513">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b06bf-513">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b06bf-514">**\_МЕДИААКЦЕССДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="b06bf-514">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

