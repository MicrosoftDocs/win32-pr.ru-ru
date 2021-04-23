---
description: '\_Класс WMI флоппидриве для Win32 управляет функциями дисковода гибких дисков.'
ms.assetid: 41823eeb-4831-4deb-a798-7b3589ebf3e2
ms.tgt_platform: multiple
title: Класс Win32_FloppyDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_FloppyDrive
- Win32_FloppyDrive.Reset
- Win32_FloppyDrive.SetPowerState
- Win32_FloppyDrive.Availability
- Win32_FloppyDrive.Capabilities
- Win32_FloppyDrive.CapabilityDescriptions
- Win32_FloppyDrive.Caption
- Win32_FloppyDrive.CompressionMethod
- Win32_FloppyDrive.ConfigManagerErrorCode
- Win32_FloppyDrive.ConfigManagerUserConfig
- Win32_FloppyDrive.CreationClassName
- Win32_FloppyDrive.DefaultBlockSize
- Win32_FloppyDrive.Description
- Win32_FloppyDrive.DeviceID
- Win32_FloppyDrive.ErrorCleared
- Win32_FloppyDrive.ErrorDescription
- Win32_FloppyDrive.ErrorMethodology
- Win32_FloppyDrive.InstallDate
- Win32_FloppyDrive.LastErrorCode
- Win32_FloppyDrive.Manufacturer
- Win32_FloppyDrive.MaxBlockSize
- Win32_FloppyDrive.MaxMediaSize
- Win32_FloppyDrive.MinBlockSize
- Win32_FloppyDrive.Name
- Win32_FloppyDrive.NeedsCleaning
- Win32_FloppyDrive.NumberOfMediaSupported
- Win32_FloppyDrive.PNPDeviceID
- Win32_FloppyDrive.PowerManagementCapabilities
- Win32_FloppyDrive.PowerManagementSupported
- Win32_FloppyDrive.Status
- Win32_FloppyDrive.StatusInfo
- Win32_FloppyDrive.SystemCreationClassName
- Win32_FloppyDrive.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 832b5fad0ce54d1436fd6b2e47765af0fabfd2bb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142274"
---
# <a name="win32_floppydrive-class"></a><span data-ttu-id="0d2d2-103">\_Класс Win32 флоппидриве</span><span class="sxs-lookup"><span data-stu-id="0d2d2-103">Win32\_FloppyDrive class</span></span>

<span data-ttu-id="0d2d2-104">\[**Win32 \_ Флоппидриве** больше не доступен для использования в Windows 10 и Windows Server 2016.\]</span><span class="sxs-lookup"><span data-stu-id="0d2d2-104">\[**Win32\_FloppyDrive** is no longer available for use as of Windows 10 and Windows Server 2016.\]</span></span>

<span data-ttu-id="0d2d2-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ флоппидриве для Win32** управляет функциями дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-105">The **Win32\_FloppyDrive** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) manages the functions of a floppy disk drive.</span></span>

<span data-ttu-id="0d2d2-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="0d2d2-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d2d2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d2d2-108">Syntax</span></span>

``` syntax
[Dynamic, provider("CIMWin32"), UUID("{FB1F3A64-BBAC-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_FloppyDrive : CIM_DisketteDrive
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
  string   Manufacturer;
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

## <a name="members"></a><span data-ttu-id="0d2d2-109">Члены</span><span class="sxs-lookup"><span data-stu-id="0d2d2-109">Members</span></span>

<span data-ttu-id="0d2d2-110">Класс **Win32 \_ флоппидриве** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0d2d2-110">The **Win32\_FloppyDrive** class has these types of members:</span></span>

-   [<span data-ttu-id="0d2d2-111">Методы</span><span class="sxs-lookup"><span data-stu-id="0d2d2-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="0d2d2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d2d2-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0d2d2-113">Методы</span><span class="sxs-lookup"><span data-stu-id="0d2d2-113">Methods</span></span>

<span data-ttu-id="0d2d2-114">Класс **Win32 \_ флоппидриве** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-114">The **Win32\_FloppyDrive** class has these methods.</span></span>



| <span data-ttu-id="0d2d2-115">Метод</span><span class="sxs-lookup"><span data-stu-id="0d2d2-115">Method</span></span>            | <span data-ttu-id="0d2d2-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0d2d2-116">Description</span></span>                                                                                                                                                                                                                   |
|:------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2d2-117">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-117">**Reset**</span></span>         | <span data-ttu-id="0d2d2-118">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-118">Not implemented.</span></span> <span data-ttu-id="0d2d2-119">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ дискеттедриве**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-119">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/>                 |
| <span data-ttu-id="0d2d2-120">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-120">**SetPowerState**</span></span> | <span data-ttu-id="0d2d2-121">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-121">Not implemented.</span></span> <span data-ttu-id="0d2d2-122">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ дискеттедриве**](cim-diskettedrive.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-122">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_DisketteDrive**](cim-diskettedrive.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0d2d2-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="0d2d2-123">Properties</span></span>

<span data-ttu-id="0d2d2-124">Класс **Win32 \_ флоппидриве** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-124">The **Win32\_FloppyDrive** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d2d2-125">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-125">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-129">Состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-129">Status of the device.</span></span>

<span data-ttu-id="0d2d2-130">Это свойство унаследовано от [ **CIM \_** -значения.](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-130">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d2d2-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d2d2-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-132"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="0d2d2-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-133"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-134">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="0d2d2-134">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="0d2d2-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-135"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="0d2d2-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-136"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d2d2-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-137"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="0d2d2-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-138"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="0d2d2-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-139"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="0d2d2-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-140"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d2d2-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-141"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="0d2d2-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-142"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="0d2d2-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-143"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="0d2d2-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-144"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-145">Энергосбережение — неизвестно</span><span class="sxs-lookup"><span data-stu-id="0d2d2-145">Power Save - Unknown</span></span>

<span data-ttu-id="0d2d2-146">Устройство в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-146">The device in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="0d2d2-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-147"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-148">Энергосбережение — режим низкого энергопотребления</span><span class="sxs-lookup"><span data-stu-id="0d2d2-148">Power Save - Low Power Mode</span></span>

<span data-ttu-id="0d2d2-149">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-149">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="0d2d2-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-150"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-151">Энергосбережение — ждущий режим</span><span class="sxs-lookup"><span data-stu-id="0d2d2-151">Power Save - Standby</span></span>

<span data-ttu-id="0d2d2-152">Устройство не работает, но может быть быстро восстановлено до полной мощности.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-152">The device is not functioning, but can be quickly restored to full-power.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="0d2d2-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-153"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="0d2d2-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-154"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-155">Энергосбережение — предупреждение</span><span class="sxs-lookup"><span data-stu-id="0d2d2-155">Power Save - Warning</span></span>

<span data-ttu-id="0d2d2-156">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-156">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="0d2d2-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-157"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-158">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-158">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="0d2d2-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-159"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-160">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-160">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="0d2d2-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-161"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-162">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-162">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="0d2d2-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-163"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-164">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-164">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-165">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-165">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-166">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0d2d2-166">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-168">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Устройства хранения DMTF \| 001,9 "," MIF. \|Устройства хранения DMTF \| 001,11 "," MIF. \|Устройства хранения DMTF \| 001,12 "," MIF. \|Диски DMTF \| 003,7 "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Капабилитидескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-168">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-169">Массив возможностей устройства доступа к носителю.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-169">Array of capabilities of the media access device.</span></span> <span data-ttu-id="0d2d2-170">Например, устройство может поддерживать произвольный доступ, съемные носители и автоматическую очистку.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-170">For example, the device may support Random Access, Removable Media, and Automatic Cleaning.</span></span> <span data-ttu-id="0d2d2-171">В этом случае значения 3, 7 и 9 будут записаны в массив.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-171">In this case, the values 3, 7, and 9 would be written to the array.</span></span>

<span data-ttu-id="0d2d2-172">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-172">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d2d2-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-173"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d2d2-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-174"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="0d2d2-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Последовательный доступ** (2)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-175"><span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="0d2d2-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Произвольный доступ** (3)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-176"><span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="0d2d2-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Поддерживает запись** (4)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-177"><span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="0d2d2-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Шифрование** (5)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-178"><span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="0d2d2-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Сжатие** (6)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-179"><span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="0d2d2-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Поддерживает** съемные носители (7)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-180"><span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>**Supports Removeable Media** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-181">Поддержка съемных носителей</span><span class="sxs-lookup"><span data-stu-id="0d2d2-181">Supports Removable Media</span></span>

</dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="0d2d2-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Очистка вручную** (8)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-182"><span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="0d2d2-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Автоматическая очистка** (9)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-183"><span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="0d2d2-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**Интеллектуальное уведомление** (10)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-184"><span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="0d2d2-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Поддержка двусторонних носителей** (11)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-185"><span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>**Supports Dual Sided Media** (11)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-186">Поддержка носителя Dual-Sided</span><span class="sxs-lookup"><span data-stu-id="0d2d2-186">Supports Dual-Sided Media</span></span>

</dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="0d2d2-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Извлечение с отключением не требуется** (12)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-187"><span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-188">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-188">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-189">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-189">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-190">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-191">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-191">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-192">Массив строк произвольной формы, предоставляющий более подробные объяснения для любых функций последовательного контроллера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="0d2d2-192">Array of free-form strings providing more detailed explanations for any of the serial controller features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="0d2d2-193">Обратите внимание, что каждая запись этого массива связана с записью в массиве **capabilities** , расположенном по тому же индексу.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-193">Note, each entry of this array is related to the entry in the **Capabilities** array that is located at the same index.</span></span>

<span data-ttu-id="0d2d2-194">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-194">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-195">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-195">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-196">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-197">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-198">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-198">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-199">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-199">Short description of the object.</span></span>

<span data-ttu-id="0d2d2-200">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-201">**компрессионмесод**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-201">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-202">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-204">Строка свободной формы, указывающая алгоритм или средство, используемые устройством для поддержки сжатия.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-204">Free form string indicating the algorithm or tool used by the device to support compression.</span></span> <span data-ttu-id="0d2d2-205">Если нет возможности описать схему сжатия (возможно, потому, что она неизвестна), используйте "Unknown", чтобы указать, что устройство поддерживает сжатие или нет. "Сжатый" для представления того, что устройство поддерживает возможности сжатия, но либо схема сжатия неизвестна, либо не раскрывается. и "не сжато" для представления того, что устройство не поддерживает возможности сжатия.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-205">If it is not possible or not desired to describe the compression scheme (perhaps because it is not known), use "Unknown" to represent that it is not known whether the device supports compression capabilities or not; "Compressed" to represent that the device supports compression capabilities, but either its compression scheme is not known or not disclosed; and "Not Compressed" to represent that the device does not support compression capabilities.</span></span>

<span data-ttu-id="0d2d2-206">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-206">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<dt>



 <span data-ttu-id="0d2d2-207">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-207">("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-208">Схема сжатия неизвестна или не описана.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-208">The compression scheme is unknown or not described.</span></span>

</dd> <dt>



 <span data-ttu-id="0d2d2-209">("Сжатый")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-209">("Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-210">Логический файл сжат, но схема сжатия неизвестна или не описана</span><span class="sxs-lookup"><span data-stu-id="0d2d2-210">The logical file is compressed, but the compression scheme is unknown or not described</span></span>

</dd> <dt>



 <span data-ttu-id="0d2d2-211">("Не сжато")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-211">("Not Compressed")</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-212">Если логический файл не сжат</span><span class="sxs-lookup"><span data-stu-id="0d2d2-212">If the logical file is not compressed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-213">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-213">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-214">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-216">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-216">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-217">Код ошибки Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-217">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="0d2d2-218">Это свойство унаследовано от [ **CIM \_** -значения.](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-218">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="0d2d2-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-219"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="0d2d2-220"> (0)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-220">(0)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-221">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-221">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="0d2d2-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-222"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="0d2d2-223">(1)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-223">(1)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-224">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-224">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0d2d2-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-225"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="0d2d2-226">(2)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-226">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="0d2d2-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-227"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="0d2d2-228">(3)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-228">(3)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-229">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-229">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0d2d2-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-230"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="0d2d2-231">(4)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-231">(4)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-232">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-232">Device is not working properly.</span></span> <span data-ttu-id="0d2d2-233">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-233">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="0d2d2-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-234"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="0d2d2-235">(5)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-235">(5)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-236">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-236">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="0d2d2-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-237"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="0d2d2-238"> (6)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-238">(6)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-239">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-239">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="0d2d2-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-240"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="0d2d2-241">(7)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-241">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="0d2d2-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-242"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="0d2d2-243">(8)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-243">(8)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-244">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-244">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="0d2d2-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-245"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="0d2d2-246">(9)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-246">(9)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-247">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-247">Device is not working properly.</span></span> <span data-ttu-id="0d2d2-248">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-248">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="0d2d2-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-249"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="0d2d2-250">(10)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-250">(10)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-251">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-251">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="0d2d2-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-252"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="0d2d2-253">(11)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-253">(11)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-254">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-254">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="0d2d2-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-255"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="0d2d2-256">(12)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-256">(12)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-257">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-257">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="0d2d2-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-258"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="0d2d2-259">(13)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-259">(13)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-260">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-260">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="0d2d2-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-261"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="0d2d2-262">(14)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-262">(14)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-263">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-263">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="0d2d2-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-264"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="0d2d2-265">(15)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-265">(15)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-266">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-266">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="0d2d2-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-267"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="0d2d2-268">(16)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-268">(16)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-269">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-269">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="0d2d2-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-270"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="0d2d2-271">(17)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-271">(17)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-272">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-272">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0d2d2-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-273"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="0d2d2-274">(18)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-274">(18)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-275">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-275">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="0d2d2-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-276"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="0d2d2-277">(19)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-277">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="0d2d2-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-278"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="0d2d2-279">(20)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-279">(20)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-280">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-280">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="0d2d2-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-281"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="0d2d2-282">(21)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-282">(21)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-283">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-283">System failure.</span></span> <span data-ttu-id="0d2d2-284">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-284">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="0d2d2-285">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-285">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="0d2d2-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-286"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="0d2d2-287">(22)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-287">(22)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-288">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-288">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="0d2d2-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-289"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="0d2d2-290">(23)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-290">(23)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-291">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-291">System failure.</span></span> <span data-ttu-id="0d2d2-292">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-292">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="0d2d2-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-293"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="0d2d2-294">(24)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-294">(24)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-295">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-295">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0d2d2-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-296"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0d2d2-297">(25)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-297">(25)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-298">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-298">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="0d2d2-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-299"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="0d2d2-300">(26)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-300">(26)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-301">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-301">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="0d2d2-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-302"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="0d2d2-303">(27)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-303">(27)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-304">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-304">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="0d2d2-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-305"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="0d2d2-306">(28)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-306">(28)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-307">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-307">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="0d2d2-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-308"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="0d2d2-309">(29)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-309">(29)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-310">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-310">Device is disabled.</span></span> <span data-ttu-id="0d2d2-311">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-311">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="0d2d2-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-312"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="0d2d2-313">(30)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-313">(30)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-314">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-314">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="0d2d2-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-315"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="0d2d2-316">1-31</span><span class="sxs-lookup"><span data-stu-id="0d2d2-316">(31)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-317">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-317">Device is not working properly.</span></span> <span data-ttu-id="0d2d2-318">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-318">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-319">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-319">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-320">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-320">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-321">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-321">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-322">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-322">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-323">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-323">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="0d2d2-324">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-324">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-325">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-325">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-326">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-326">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-327">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-327">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-328">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-328">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-329">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-329">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="0d2d2-330">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-330">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="0d2d2-331">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-331">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-332">**дефаултблокксизе**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-332">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-333">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-333">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-334">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-335">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-335">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-336">Размер блока по умолчанию (в байтах) для этого устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-336">Default block size, in bytes, for this device.</span></span>

<span data-ttu-id="0d2d2-337">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-337">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0d2d2-338">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-338">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-339">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-339">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-340">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-341">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-342">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-342">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-343">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-343">Description of the object.</span></span>

<span data-ttu-id="0d2d2-344">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-344">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-345">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-345">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-346">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-347">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-347">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-348">Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-348">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-349">Уникальный идентификатор дисковода гибких дисков с другими устройствами в системе.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-349">Unique identifier of the floppy disk drive with other devices on the system.</span></span>

<span data-ttu-id="0d2d2-350">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-350">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-351">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-351">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-352">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-352">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-353">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-353">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-354">Если **значение — true**, то ошибка, сообщаемая в **ластерроркоде** , теперь удаляется.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-354">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="0d2d2-355">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-355">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-356">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-356">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-357">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-357">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-358">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-358">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-359">Произвольная строка, которая предоставляет дополнительные сведения об ошибке, записанной в **ластерроркоде**, и сведения о любых корректирующих действиях, которые могут быть предприняты.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-359">Free-form string that supplies more information about the error recorded in **LastErrorCode**, and information on any corrective actions that may be taken.</span></span>

<span data-ttu-id="0d2d2-360">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-360">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-361">**еррормесодологи**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-361">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-362">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-363">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-364">Произвольная строка, описывающая тип обнаружения и исправления ошибок, поддерживаемых этим устройством.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-364">Free-form string that describes the type of error detection and correction supported by this device.</span></span>

<span data-ttu-id="0d2d2-365">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-365">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-366">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-366">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-367">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-367">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-368">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-369">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-369">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-370">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-370">Date and time the object was installed.</span></span> <span data-ttu-id="0d2d2-371">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-371">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="0d2d2-372">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-372">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-373">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-373">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-374">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-375">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-376">Код последней ошибки, сообщаемый логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-376">Last error code reported by the logical device.</span></span>

<span data-ttu-id="0d2d2-377">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-377">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-378">**Производителя**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-378">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-379">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-380">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-381">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-381">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-382">Имя производителя дисковода гибких дисков.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-382">Name of the manufacturer of the floppy disk drive.</span></span>

<span data-ttu-id="0d2d2-383">Пример: ACME</span><span class="sxs-lookup"><span data-stu-id="0d2d2-383">Example: "Acme"</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-384">**максблокксизе**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-384">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-385">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-385">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-386">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-386">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-387">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-387">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-388">Максимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-388">Maximum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="0d2d2-389">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-389">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0d2d2-390">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-390">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-391">**максмедиасизе**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-391">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-392">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-392">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-393">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-394">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Устройства с последовательным доступом DMTF \| 001,2 "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) (" килобайтах ")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-395">Максимальный размер носителя, поддерживаемого этим устройством (в килобайтах).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-395">Maximum size, in kilobytes, of media supported by this device.</span></span>

<span data-ttu-id="0d2d2-396">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-396">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0d2d2-397">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-397">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-398">**минблокксизе**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-398">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-399">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-399">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-400">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-401">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-401">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-402">Минимальный размер блока в байтах для носителя, доступного этому устройству.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-402">Minimum block size, in bytes, for media accessed by this device.</span></span>

<span data-ttu-id="0d2d2-403">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-403">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

<span data-ttu-id="0d2d2-404">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-404">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-405">**Name**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-405">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-408">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-408">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-409">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-409">Label by which the object is known.</span></span> <span data-ttu-id="0d2d2-410">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-410">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="0d2d2-411">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-411">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-412">**нидсклеанинг**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-412">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-413">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-413">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-414">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-415">Если задано **значение true**, устройству доступа к носителю требуется очистка.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-415">If **True**, the media access device requires cleaning.</span></span> <span data-ttu-id="0d2d2-416">Возможность ручной или автоматической очистки указывается в свойстве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="0d2d2-416">Whether manual or automatic cleaning is possible is indicated in the **Capabilities** property.</span></span>

<span data-ttu-id="0d2d2-417">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-417">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-418">**нумберофмедиасуппортед**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-418">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-419">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-419">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-420">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-421">Максимальное число отдельных носителей, которые могут поддерживаться или вставляться на устройстве доступа к носителю (если поддерживается).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-421">Maximum number of individual media which can be supported or inserted in the media access device (when supported).</span></span>

<span data-ttu-id="0d2d2-422">Это свойство наследуется от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-422">This property is inherited from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-423">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-423">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-424">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-425">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-425">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-426">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-426">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-427">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-427">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="0d2d2-428">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-428">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0d2d2-429">Пример: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="0d2d2-429">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-430">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-430">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-431">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="0d2d2-431">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-432">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-432">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-433">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-433">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="0d2d2-434">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-434">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d2d2-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-435"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="0d2d2-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-436"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d2d2-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-437"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d2d2-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-438"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-439">Активировано</span><span class="sxs-lookup"><span data-stu-id="0d2d2-439">Enabled</span></span>

<span data-ttu-id="0d2d2-440">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-440">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="0d2d2-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-441"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-442">Режимы энергосбережения записываются автоматически</span><span class="sxs-lookup"><span data-stu-id="0d2d2-442">Power Saving Modes Entered Automatically</span></span>

<span data-ttu-id="0d2d2-443">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-443">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="0d2d2-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-444"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-445">Устанавливаемое состояние питания</span><span class="sxs-lookup"><span data-stu-id="0d2d2-445">Power State Settable</span></span>

<span data-ttu-id="0d2d2-446">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="0d2d2-446">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="0d2d2-447">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-447">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="0d2d2-448">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-448">For more information, see [Designing Managed Object Format (MOF) Classes](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="0d2d2-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-449"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-450">Поддержка циклов электропитания</span><span class="sxs-lookup"><span data-stu-id="0d2d2-450">Power Cycling Supported</span></span>

<span data-ttu-id="0d2d2-451">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-451">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="0d2d2-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-452"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="0d2d2-453">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="0d2d2-453">Timed Power-On Supported</span></span>

<span data-ttu-id="0d2d2-454">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-454">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-455">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-455">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-456">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-456">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-457">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-458">Если **значение — true**, устройство может управляться с помощью питания (может быть переведено в режим приостановки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-458">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="0d2d2-459">Свойство не указывает на то, что функции управления питанием в настоящее время включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-459">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="0d2d2-460">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-460">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-461">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-461">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-462">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-462">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-463">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-463">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-464">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-464">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-465">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-465">Current status of the object.</span></span> <span data-ttu-id="0d2d2-466">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-466">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0d2d2-467">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например, жесткий диск с поддержкой SMART), может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-467">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly, but predicting a failure in the near future).</span></span> <span data-ttu-id="0d2d2-468">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="0d2d2-468">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0d2d2-469">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-469">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0d2d2-470">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-470">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0d2d2-471">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-471">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="0d2d2-472">Значения качества производительности:</span><span class="sxs-lookup"><span data-stu-id="0d2d2-472">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="0d2d2-473">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-473">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="0d2d2-474">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-474">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="0d2d2-475">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-475">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d2d2-476">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-476">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="0d2d2-477">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-477">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="0d2d2-478">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-478">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="0d2d2-479">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-479">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="0d2d2-480">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-480">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="0d2d2-481">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-481">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="0d2d2-482">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-482">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="0d2d2-483">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-483">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="0d2d2-484">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-484">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-485">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-485">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-486">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-487">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-487">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-488">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="0d2d2-488">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-489">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-489">State of the logical device.</span></span> <span data-ttu-id="0d2d2-490">Если это свойство не применяется к логическому устройству, следует использовать значение 5 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="0d2d2-490">If this property does not apply to the logical device, the value 5 ("Not Applicable") should be used.</span></span>

<span data-ttu-id="0d2d2-491">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0d2d2-492">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-492">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0d2d2-493">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-493">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0d2d2-494">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-494">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0d2d2-495">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-495">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0d2d2-496">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-496">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0d2d2-497">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-497">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-498">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-498">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-499">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-499">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-500">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-500">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-501">Значение **Свойства "** область видимости компьютера".</span><span class="sxs-lookup"><span data-stu-id="0d2d2-501">Value of the scoping computer **CreationClassName** property.</span></span> <span data-ttu-id="0d2d2-502">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-502">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="0d2d2-503">Это свойство унаследовано от [ **CIM \_** -значения.](cim-logicaldevice.md)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-503">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md)</span></span>

</dd> <dt>

<span data-ttu-id="0d2d2-504">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-504">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d2d2-505">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-506">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0d2d2-506">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d2d2-507">Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d2d2-507">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d2d2-508">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-508">Name of the scoping system.</span></span>

<span data-ttu-id="0d2d2-509">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-509">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d2d2-510">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d2d2-510">Remarks</span></span>

<span data-ttu-id="0d2d2-511">Класс **Win32 \_ флоппидриве** является производным от [**CIM \_ дискеттедриве**](cim-diskettedrive.md) , который является производным от [**CIM \_ медиаакцессдевице**](cim-mediaaccessdevice.md).</span><span class="sxs-lookup"><span data-stu-id="0d2d2-511">The **Win32\_FloppyDrive** class is derived from [**CIM\_DisketteDrive**](cim-diskettedrive.md) which derives from [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md).</span></span> <span data-ttu-id="0d2d2-512">Класс **CIM \_ медиаакцессдевице** является производным от [**CIM \_**](cim-logicaldevice.md)с параметром.</span><span class="sxs-lookup"><span data-stu-id="0d2d2-512">The **CIM\_MediaAccessDevice** class derives from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d2d2-513">Требования</span><span class="sxs-lookup"><span data-stu-id="0d2d2-513">Requirements</span></span>



| <span data-ttu-id="0d2d2-514">Требование</span><span class="sxs-lookup"><span data-stu-id="0d2d2-514">Requirement</span></span> | <span data-ttu-id="0d2d2-515">Значение</span><span class="sxs-lookup"><span data-stu-id="0d2d2-515">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2d2-516">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d2d2-516">Minimum supported client</span></span><br/> | <span data-ttu-id="0d2d2-517">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d2d2-517">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d2d2-518">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d2d2-518">Minimum supported server</span></span><br/> | <span data-ttu-id="0d2d2-519">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d2d2-519">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d2d2-520">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0d2d2-520">End of client support</span></span><br/>    | <span data-ttu-id="0d2d2-521">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0d2d2-521">Windows 8.1</span></span><br/>                                                                  |
| <span data-ttu-id="0d2d2-522">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="0d2d2-522">End of server support</span></span><br/>    | <span data-ttu-id="0d2d2-523">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0d2d2-523">Windows Server 2012 R2</span></span><br/>                                                       |
| <span data-ttu-id="0d2d2-524">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0d2d2-524">Namespace</span></span><br/>                | <span data-ttu-id="0d2d2-525">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0d2d2-525">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0d2d2-526">MOF</span><span class="sxs-lookup"><span data-stu-id="0d2d2-526">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d2d2-527"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d2d2-527"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d2d2-528">DLL</span><span class="sxs-lookup"><span data-stu-id="0d2d2-528">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d2d2-529"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d2d2-529"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d2d2-530">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d2d2-530">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2d2-531">**\_ДИСКЕТТЕДРИВЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="0d2d2-531">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dt>

[<span data-ttu-id="0d2d2-532">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="0d2d2-532">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

